# Backup e recuperação simples — Nível 2 Intermédio e Nível 3 Avançado

## Diretório crítico identificado
`/temp/` — é o directório critico por ter todos os privilégios ativados, tal 
como `/var/crash` e `var/temp`.

## Criar backup
```
mkdir -p ~/backup
tar -cvpzf ~/backup/backup.tar.gz ~/var/www/html
ls ~/backup
```
Cria uma cópia completa da pasta `~/var/www/html` para pasta criada
`~/backup` e confirmar a criação do ficheiro de backup backup.tar.gz.
Print nas /evidencias/Nivel 2/2.png

## Criar pasta de teste
```
mkdir -p ~/teste
```
Criação da pasta de teste onde vai ser recupardo o ficheiro de backup. 
Print nas /evidencias/Nivel 2/3.png

## Restaurar o backup na pasta de teste
```
tar -xvpzf ~/backup/backup.tar.gz -C ~/teste
ls ~/teste
```
Restaura do backup feito da pasta `/var/www/html` para a pasta de teste e
confirmação do restauro. Print na pasta /evidencias/Nivel 2/3.png

## Confirmar que os ficheiros foram recuperados
```
diff -r /var/www/html/ ~/teste/var/www/html
```
Vai identificar se há diferenças nos diretórios de origem do backup e 
o diretório de teste. Print nas /evidencias/Nivel 2/4.png

## Nível 3 — Procedimento de recuperação (produção) e agendamento com cron

### Agendamento automático do backup (cron)
Para o backup não depender de ser feito manualmente, foi agendado com o
`cron`:
```
crontab -e
```
Linha adicionada (backup semanal, todos os domingos às 3h da manhã):
```
0 3 * * 0 rsync -a /var/www/html/topico-03/ /home/amestre/backup/topico-03-$(date +\%Y\%m\%d)/ >> /home/amestre/backup/backup.log 2>&1
```
- `0 3 * * 0` — minuto 0, hora 3, todos os dias do mês, todos os meses,
  domingo (dia 0 da semana).
- O resultado é guardado em `backup.log`, para se poder confirmar depois
  que o backup correu sem erros.

Confirmar que a tarefa ficou agendada:
```
crontab -l
```

Confirmar, mais tarde, que o backup correu (depois do domingo seguinte):
```
ls -l ~/backup
cat ~/backup/backup.log
```

### Procedimento de recuperação (restaurar em produção)
Passos a seguir se o site publicado for perdido, apagado ou corrompido:

1. **Confirmar o estado do serviço:**
   ```
   sudo systemctl status nginx
   ```
2. **Identificar o backup mais recente disponível:**
   ```
   ls -lt ~/backup
   ```
3. **Restaurar o backup mais recente para a produção, com rsync:**
   ```
   sudo rsync -av --delete ~/backup/topico-03-<data-mais-recente>/ /var/www/html/topico-03/
   ```
   - `--delete` garante que a pasta de produção fica exatamente igual
     ao backup, removendo qualquer ficheiro que lá tenha ficado por
     engano e que não exista no backup.
4. **Corrigir o dono e as permissões dos ficheiros:**
   ```
   sudo chown -R www-data:www-data /var/www/html/topico-03
   sudo find /var/www/html/topico-03 -type d -exec chmod 755 {} \;
   sudo find /var/www/html/topico-03 -type f -exec chmod 644 {} \;
   ```
5. **Validar a configuração do Nginx antes de reiniciar:**
   ```
   sudo nginx -t
   ```
6. **Reiniciar o serviço:**
   ```
   sudo systemctl restart nginx
   ```
7. **Confirmar que o site voltou a responder:**
   ```
   curl -I http://192.168.4.107/topico-03/index.html
   ```
   Resultado esperado: `HTTP/1.1 200 OK`.
