# Atividade prática individual - Tópico 5

## Nível realizado
Nível 1, Nível 2 e Nível 3

## Objetivo
Acompanhar o estado do sistema, consultar registos, criar um backup e
testar uma recuperação simples do serviço publicado no Tópico 3.

## Serviço analisado
Nginx, a servir o site do Tópico 3 (index.html, sobre.html, style.css),
publicado em `/var/www/html/topico-03/`, já protegido no Tópico 4 com
UFW, Fail2ban, Aide e Lynis.

## Ambiente utilizado
Linux Ubuntu Server, acesso remoto via SSH.

## Ficheiros produzidos
- `comandos.txt`
- `monitorizacao.md` (Nível 1)
- `logs.md` (Nível 1)
- `manutencao.md`
- `backup-recuperacao.md` (Nível 2 & 3)
- `continuidade.md` (Nível 3)

## Resumo do trabalho
- **Nível 1:** verificado o tempo de atividade, memória, disco e estado
  do serviço web, consultados os logs do sistema, identificar evento relevante;
- **Nível 2:** identificado o diretório crítico, criado um backup, 
restaurado numa pasta de teste e confirmada a recuperação.
- **Nível 3:** definido o plano de continuidade operacional - serviço crítico,
  ficheiros/configurações e logs importantes, periodicidade de backup,
  procedimento de recuperação e critérios de validação.

## URLs testados
- http://192.168.4.107/topico-03/index.html

## Evidências produzidas
Prints e outputs de validação guardados na pasta `evidencias/`.

## Link do repositório GitHub
https://github.com/andbasket15-a15y/linux-seguranca-cloud
