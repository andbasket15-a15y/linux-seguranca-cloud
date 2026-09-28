## Opção B1
# Acesso remoto por SSH

## O que é SSH?
SSH (Secure Shell) é um protocolo de rede criptografado, usado para se ligar remotamente e de forma segura a um servidor Linux, permitindo executar comandos e gerir ficheiros à distância sem que os dados circulem em texto simples na rede.

## Que informação seria necessária para aceder a um servidor por SSH?
- Utilizador: amestre
- Endereço IP: 192.168.4.106
- Porta: 22
- Palavra-passe ou chave: palavra-passe pessoal

## Exemplo de comando de ligação
ssh amestre@192.168.4.106
Se fosse outra porta não sendo a padrão como está definido, o comando seria `ssh -p <porta> amestre@192.168.4.106`.


## Opção B2
# Acesso remoto por SSH

## Estado do serviço SSH
Estado de serviço ativo para ser executado remotamente via Bitvise SSH Client no W11-
$ systemctl status ssh

Pode ser visto no direcório evidencias 

## Endereço identificado
- Endereço deste ambiente local (`hostname -I`): 192.168.4.106

## Comando de ligação
ssh amestre@192.168.4.106

## Resultado obtido
Conecção estabeleicida como visivel em evidencias.


## Opção B3
# Acesso remoto e chaves SSH

## Diferença entre autenticação por palavra-passe e autenticação por chave

-Palavra-passe é um segredo escrito pelo utilizador ao ligar-se que fica na cabeça do utilizador e no servidor (guardada cifrada, em `/etc/shadow`) que pode ser adivinhada, reutilizada ou atacada por força bruta e tem uma segurança menor, depende da qualidade da palavra-passe.
-Chave SSH é um par de chaves criptográficas: privada e pública que fica privada no cliente; pública no servidor (`~/.ssh/authorized_keys`), onde caso a chave privada for roubada, o atacante pode entrar e tem uma segurança muito maior: não há método simples para adivinhar.

## Chave pública
- Gerada com `ssh-keygen` (ficheiro terminado em `.pub`).
- É segura de partilhar: vai para o servidor, no ficheiro `~/.ssh/authorized_keys` (por exemplo com `ssh-copy-id utilizador@servidor`).
- Chave pública da chave de teste criada:

ssh-ed25519:wkD2******+*****BDxs amestre@skodjidigital


## Chave privada
- Fica apenas no cliente e nunca sai do computador do utilizador.
- Tem de ter permissão "600" (`-rw-------`), e a pasta `~/.ssh` permissão "700" (`drwx------`). O `ls -l ~/.ssh` confirmou ambas.
- É a prova de identidade: quem a tiver consegue entrar como esse utilizador.
- Em utilização real deve ser protegida com *passphrase*. A chave desta atividade foi criada sem *passphrase* por ser apenas de teste.

## Cuidados de segurança
- Nunca partilhar, enviar por email/chat nem publicar a chave privada (nem em repositórios ou capturas de ecrã).
- Usar uma chave por pessoa e contas individuais, nunca contas partilhadas.
- Manter `~/.ssh` com 700 e as chaves privadas com 600.
- No servidor: `PermitRootLogin no` (sem login direto como root, elevar com `sudo`), preferir chaves a palavras-passe e, se possível, mudar a porta 22 para reduzir ataques automáticos.
- Se uma chave for comprometida ou a pessoa sair da equipa, remover a chave pública de `authorized_keys`.

## Evidência segura
No diretório evidencias.
