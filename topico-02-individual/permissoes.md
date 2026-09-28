# Permissões aplicadas
## Ambiente utilizado
VM Local num macOS com Linux Ubuntu Server 26.04.1 e Windows 11 no Bitvise SSH Client, com um utilizador normal.

## Utilizador e grupos
$ whoami
amestre

$ id
uid=1000(amestre) gid=1000(amestre) groups=1000(amestre),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),100(users),101(lxd)

$ groups
amestre adm cdrom sudo dip plugdev users lxd

## Ficheiros criados
Pasta de teste: `topico-02-individual/teste/`

- publico.txt: ficheiro de texto que pode ser aberta por todos.
- restrito.txt: ficheiro de texto que só o dono e o grupo devem abir.
- script.sh: pequeno ficheiro script vazio; serve para testar a permissão de execução.

No inicio os três ficheiros foram criados com `rw-rw-r--`

-rw-rw-r-- 1 amestre amestre 0 Sep 21 17:31 publico.txt
-rw-rw-r-- 1 amestre amestre 0 Sep 21 17:31 restrito.txt
-rw-rw-r-- 1 amestre amestre 0 Sep 21 17:31 script.sh

## Permissões aplicadas
| Ficheiro | Permissão | Justificação |
|---|---:|---|
| publico.txt | 644 | `rw-r--r--`: o dono lê e escreve; grupo e outros só leem. É para todos abrirem, mas só o dono a pode alterar. |
| restrito.txt | 640 | `rw-r-----`: o dono lê e escreve; o grupo só lê; os outros utilizadores não têm qualquer acesso. Protege o que não deve ser vista por todos. |
| script.sh | u+x | `rwxrw-r--`: Só o dono recebe permissão de execução. Antes disto, `./script.sh` dava *Permission denied*; depois, executou normalmente. Grupo e outros continuam sem poder executar. |

No fim ficaram com os seguintes privilêgios:

-rw-r--r-- 1 amestre amestre 0 Sep 21 17:31 publico.txt
-rw-r----- 1 amestre amestre 0 Sep 21 17:31 restrito.txt
-rwxrw-r-- 1 amestre amestre 0 Sep 21 17:31 script.sh

## Relação com o princípio do menor privilégio
O princípio do menor privilégio diz que cada utilizador deve ter apenas as autorizações mínimas necessárias para fazer o seu trabalho. Por isso as permissões aplicadas são mais adequadas do que dar permissões totais (777, `rwxrwxrwx`) a todos:

- publico.txt (644): todos podem ler, sendo essa a sua finalidade, mas só o dono o pode alterar ou apagar, o que evita alterações acidentais ou indevidas.
- restrito.txt (640): com 777, qualquer utilizador do sistema poderia ler e alterar o ficheiro. Com 640, os outros (o) não têm acesso nenhum e o grupo só pode ler.
- script.sh (u+x): executar código é uma ação com risco. Só o dono precisa de o executar, pelo que só ele recebe a permissão `x`; com 777, qualquer utilizador poderia executá-lo ou modificá-lo.