# Firewall.md — Nível 2 - Intermédio

## Verificar estado do UFW
sudo ufw status verbose - Conjunto de comandos usados para testar o 
estado do firewall `Status: active`.

## Permitir SSH, se aplicável; Permitir HTTP;Permitir HTTS apenas dse estiver configurado
# Regras aplicadas
A permissão para SSH, HTTP já tinha sido concebidas e ativadas com os comandos 
**sudo ufw allow OpenSSH** e **sudo ufw allow 80/tcp** por isso não foi preciso
serem aplicadas. 
O HTTPS foi desativada com comando **sudo ufw deny 443/tcp** sendo que não 
foi configurada nenhum certificado TLS no servidor. Só deve ser aberta 
para uso quando o HTTPS estiver implementado para uma melhor segurança.

- **SSH (22):** permitida
- **HTTP (80):** permitida 
- **HTTPS (443):** não permitida

## Ativar UFW
O firewall já se concontrava ativado como um dos primeiros precessos efeitos anteriormente 
pelo comando **sudo ufw enable** que vou repetido para o trabalho para confirmar apesar
de estar visível a não necessidade de tal ao ver o estado do serviço.

## Validar regras
```
sudo ufw status verbose
```
Resultado esperado:
```
Status: active

To                         Action         From
--                         ------         ----
22/tcp (OpenSSH)           ALLOW IN       Anywhere
80/tcp                     ALLOW IN       Anywhere
443/tcp                    DENY IN        Anywhere
```

## Validar que o serviço web continua acessível
```
curl http://localhost/topico-03/index.html
curl http://localhost/topico-03/sobre.html
```

As validações detalhadas estão documentadas em `validacao.md`.