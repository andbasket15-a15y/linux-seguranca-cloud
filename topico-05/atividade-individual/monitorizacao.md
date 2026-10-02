# Monitorização — Nível 1 Essencial

## Tempo de atividade do sistema

`uptime` - Mostra que o servidor está ligado à cerca de mais de +03h30min ativo em 10h23min.
Prints em /evindecias/Nivel 1/1.png

## Memória

`free -h` - Mostra a informação total da memória RAM do sistema. Prints em /evindecias/nivel 1/1.png

## Espaço em disco

`df -h` - Mostra o espaço ocupado e livre em cada partição. Prints em /evindecias/nivel 1/1.png

## Estado do serviço web

`sudo systemctl status nginx` - Confirma se o Nginx(serviço web) está `active (running)`

## Consultar logs recentes do sistema
```
sudo journalctl -n 40
sudo tail -25 /var/log/syslog
sudo tail -n 40 /var/log/auth.log 
```
Esses são comandos para ver os dados de logs dos serviços e das autenticações dos sistemas.
Prints em /evidencias/Nivel 1/2.png, 3.png e 4.png.

## Identificar pelo menos um evento relevante
- kernel: [UFW BLOCK] IN=enp0s3 OUT= MAC=01:00:5e:00:00:01:30:16:9d:ee:0e:ac:08:00 SRC=192.168.4.1 DST=224.0.0.1 LEN=36 - O firewaall desativou o acesso a maquina que estava em controlo SSH do sistema . Print em /evidencia/Nivel 1/2.png
