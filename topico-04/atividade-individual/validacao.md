# Validação
Validação realizada depois de aplicadas as medidas dos niveis 2 e 3.
---

## Validação do Nível 2 — Aplicar firewall e validar o serviço

### Estado da firewall continua ativo
```
sudo ufw status verbose
```
**Resultado esperado:** `Status: active`, com `22/tcp` e `80/tcp` em
`ALLOW IN`; `443/tcp` em `DENY IN`.

### Serviço web continua acessível
```
curl -I http://192.168.4.107/topico-03/index.html
curl -I http://192.168.4.107/topico-03/sobre.html
curl -I http://192.168.4.107/topico-03/style.css
```
**Resultado esperado:** `HTTP/1.1 200 OK` nos três pedidos.

### Acesso SSH continua disponível
```
ssh amestre@192.168.4.107
```
**Resultado esperado:** ligação estabelecida com sucesso, confirmando que
a ativação do UFW não bloqueou a administração remota feita a partir do Bitvise.

---

## Validação do Nível 3 — Prop hardening inicial para o serviço publicado

Validação de cada medida do `hardening.md`.

| Medida aplicada | Como validar | Resultado esperado |
|---|---|---|
| Pacotes atualizados | `sudo apt update && apt list --upgradable` | 10 pacotes podem ser atualizados |
| Permissões da pasta pública | `stat -c '%U:%G %a %n' /var/www/html/topico-03 /var/www/html/topico-03/*` | Dono `www-data:www-data`; `755` no diretório e `644` nos ficheiros |
| Listagem de diretório desativada | `grep -n autoindex /etc/nginx/sites-available/default` | Linha `autoindex off;` presente |
| Configuração do Nginx válida | `sudo nginx -t` | `syntax is ok` e `test is successful` |
| Serviço Nginx ativo após alterações | `sudo systemctl status nginx` | `active (running)` |
| Serviço Fail2ban ativo após alterações | `sudo systemctl status fail2ban` | `active (running)` |
| Serviço Lynis pronto para auditoria do sistema | `sudo lynis audit system` | Várias recomendações e alertas do sistema |

### Teste final do serviço após o hardening
```
curl -I http://localhost/topico-03/index.html
```
**Resultado esperado:** `HTTP/1.1 200 OK` — o site continua acessível
depois de todas as medidas aplicadas, sem perda de funcionalidade.

## Observação
Pelo facto de não ter sido usado o Nivel 3 no tópico 3, não foram aplicadas ou levadas em consideração os pontos 
sobre **manter base de dados acessível apenas localmente** e **evitar credenciais fracas no WordPress**.