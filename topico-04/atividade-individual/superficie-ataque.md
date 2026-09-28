# Superfície-ataque — Nível 1 (Essencial)

## Identificar o serviço web no Tópico 3
No Topico  3 foi usado o Nginx, a publicar o site simples 
(index.html, sobre.html e style.css, com conteúdo sobre basquetebol), 
a partir do diretório /var/www/html/topico-03/.

## Serviços ativos identificados
Foram identificados todos serviços disponíveis, depois todos os serviços ativos, 
e por ultimo foram testados alguns os serviços de forma individual mediante trabalho:
- **nginx.service** — ativo; é o servidor web que publica o site do Tópico 3.
- **ssh.service** — ativo; usado para administração remota do servidor via Bitvise Client.

## Portas abertas ou observadas
| Porta | Serviço | Observação |
|---|---|---|
| 21/tcp | FTP | Usada para acesso e transferência ficheiros na rede|
| 22/tcp | SSH | Usada para administração remota do servidor |
| 80/tcp | HTTP | Serve o site publicado no Tópico 3 |
| 443/tcp | HTTPS | Não está aberta porque HTTPS ainda não está configurado |

## Quais portas são necessárias
- **22 (SSH):**  É a porta responsável apenas para quem administra o servidor que 
uso via Bitvise SSH Client e não deve ficar aberta a qualquer origem sem controlo.
- **80 (HTTP):** É a porta pela qual o serviço publicado no Nginx do website criado 
é acedido publicamente.

## Riscos iniciais identificados
1. **Acesso SSH exposto sem restrição** — sem limitação por IP nem
   autenticação por chave, o serviço fica vulnerável a tentativas indevidas 
   de login por força bruta.
2. **Tráfego HTTP não cifrado** — os dados trocados entre o navegador e o
   servidor podem ser interceptados, por não existir HTTPS que é mais seguro.
3. **Firewall (UFW) inativa por defeito** — numa instalação recente, todas
   as portas do serviço podem ficar expostas sem qualquer controlo até a
   firewall ser configurada e ativada.
