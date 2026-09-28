# Atividade prática individual - Tópico 4

## Nível realizado
Nível 1(Essencial), Nível 2(Intermédio) e Nível 3(Avançado)

## Objetivo
Aplicar medidas iniciais de segurança ao serviço web publicado no Tópico 3.

## Serviço analisado
Nginx, a servir o site simples do Tópico 3 (index.html, sobre.html,
style.css — conteúdo sobre basquetebol), publicado em
`/var/www/html/topico-03/`.

## Ambiente utilizado
Ubuntu Server, acesso remoto via SSH (Bitvise).

## Ficheiros produzidos
- `comandos.txt`
- `superficie-ataque.md` (Nível 1)
- `firewall.md` (Nível 2)
- `hardening.md` (Nível 3)
- `validacao.md` (Nível 2 e 3)

## Resumo do trabalho
- **Nível 1:** identificados os serviços ativos (nginx, ssh), as portas
  abertas (22, 80) e três riscos iniciais.
- **Nível 2:** aplicadas as regras de firewall UFW (SSH e HTTP
  permitidos, HTTPS não aplicado por não estar configurado), UFW ativado
  e serviço validado como continuando acessível.
- **Nível 3:** identificado o serviço (Nginx, site simples), listados os
  riscos específicos e propostas sete medidas de hardening, separadas
  entre as que podem ser aplicadas já e as que ficam para tópicos
  seguintes.

## URLs testados
- http://localhost/topico-03/index.html
- http://localhost/topico-03/sobre.html

## Evidências produzidas
Prints e outputs de validação guardados na pasta `evidencias/`.



## Link do repositório GitHub
https://github.com/andbasket15-a15y/linux-seguranca-cloud
