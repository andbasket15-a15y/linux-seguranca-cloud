# Plano de continuidade operacional — Nível 3 Avançado

## Serviços críticos
- Não foram identificados nenhum serviço em estado critico com os comandos 

`sudo systemctl list-units --type=service --state=critical`
`sudo systemctl --failed`
A informação apresentada está na pasta /evidencias/Nivel 3/4.png.

- Os serviços críticos para funcionamento do sistema estão todos ativos e 
rodando normalmente.

`sudo systemctl list-units --type=service --state=critical`
Informação apresentada na pasta /evidencias/Nivel 3/6.png

## Ficheiros e configurações críticas
- `/var/www/html/topico-03/` — ficheiros index.html, sobre.html,
  style.css do site.
- `/etc/nginx/sites-available/default` — configuração do Nginx que inclui a
  regra `autoindex off;` Print em /evidencias/Nivel 3/9.png
- `/etc/fail2ban/jail.local` — configuração do Fail2ban, que protege o
  acesso SSH. Prints em /evidencias/Nivel 3/10.png e 11.png.

## Logs importantes
Relatórios dos logs na pasta /evidencias/Nivel 3/12.png
                                                /13.png

