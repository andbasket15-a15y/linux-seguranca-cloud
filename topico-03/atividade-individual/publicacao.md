# Publicação do site

## Nível escolhido
Nível 2 - Intermédio

## Rota escolhida
Nginx

## Ficheiros criados
- index.html
- sobre.html
- style.css

## Local de publicação
/var/www/html/topico-03/

## Comandos principais utilizados
- sudo apt install nginx -y
- sudo mkdir -p /var/www/html/topico-03
- sudo cp sobre.html /var/www/html/topico-03/
- sudo chown -R www-data:www-data /var/www/html/topico-03
- sudo systemctl restart nginx

(lista completa em comandos.txt e prints na pasta evidencias)

## Resultado obtido
O serviço Nginx ficou ativo e a servir os ficheiros do site (index.html e
sobre.html) a partir de /var/www/html/topico-03/, com a folha de estilos
style.css aplicada corretamente e a ligação entre as duas páginas funcional.

## Limitações encontradas
Nenhuma limitação.