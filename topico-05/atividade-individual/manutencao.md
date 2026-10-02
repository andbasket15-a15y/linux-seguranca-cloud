# Manutenção

## Atualização de pacotes
```
sudo apt update
sudo apt upgrade -y
```
Deve ser feita com regularidade, para corrigir falhas de segurança
conhecidas.

## Verificação de serviços críticos
```
sudo systemctl status nginx
sudo systemctl status fail2ban
sudo systemctl status ssh
```
Confirma que os três serviços essenciais ao funcionamento e à segurança
do site continuam ativos.

## Limpeza de logs antigos
```
sudo journalctl --vacuum-time=30d
```
Remove registos do journalctl com mais de 30 dias, libertando espaço em
disco.

## Auditoria periódica com Lynis
```
sudo lynis audit system
```
Deve ser corrida periodicamente
para identificar novas recomendações de segurança.

## Verificação de integridade com Aide
```
sudo aide --config=/etc/aide/aide.conf --check
```
Compara o estado atual dos ficheiros do sistema com a base de dados
criada anteriormente pelo Aide, alertando para alterações inesperadas.
