# Hardening.md — Nível 3 - Avançado

## Serviço identificado
O serviço publicado no Tópico 3 usa **Nginx** a servir um site simples
(HTML + CSS). Não há WordPress nem base de dados envolvidos.

## Listar riscos específicos desse serviço
- Ficheiros de configuração do Nginx (`/etc/nginx/`) poderem ficar
  acessíveis publicamente se colocados por engano dentro de
  `/var/www/html/`.
- Listagem automática de diretório (`autoindex`) ativa, expondo a
  estrutura de diretórios e ficheiros do site.
- Permissões demasiado abertas no diretório público, permitindo escrita por
  utilizadores que não deveriam ter esse acesso.
- Ausência de HTTPS, expondo o tráfego entre cliente e servidor a
  interceção.
- Acesso SSH apenas por password (sem chave), vulnerável a ataques de
  força bruta.

## Propor medidas iniciais de hardening
1. Manter os pacotes do sistema atualizados
   (`sudo apt update && sudo apt upgrade -y`).
2. Rever as permissões em `/var/www/html/topico-03/`
   (dono `www-data`, `755` em diretórios, `644` em ficheiros).
3. Desativar a listagem de diretório no Nginx (`autoindex off;` 
   no bloco `server`).
4. Bloquear na firewall todas as portas que não sejam estritamente
   necessárias.
5. Instalar e configurar `Fail2ban` para proteger com ataques de 
   força bruta banindo os IPs com suspeita de atividade.
6. Evitar o uso direto da conta root — administrar sempre com um
   utilizador normal e `sudo` quando necessário.
7. Instalar ferramentas para detectar Intrusão e para 
   Auditoria como `Aide` e `Lynis`.

## Medidas que podem ser aplicadas agora
- Atualização dos pacotes do sistema.
- Revisão das permissões do diretório público do site.
- Ativação da firewall com as regras mínimas.
- Desativar uso de conta root.
- Autenticação SSH por chave e desativação do login por password.

## Medidas que ficam para tópicos seguintes
- Configuração de HTTPS/TLS.
- Definição de uma política de cópias de segurança (backups).
