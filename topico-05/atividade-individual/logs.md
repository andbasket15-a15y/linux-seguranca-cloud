# Logs — Nível 1 Essencial

## Logs do sistema pelo comando journalctl
out 02 04:50:10 skodjidigital systemd[1]: sysstat-collect.service: Deactivated successfully.
out 02 04:50:10 skodjidigital systemd[1]: Finished sysstat-collect.service - system activity accounting tool.
out 02 04:50:27 skodjidigital sudo[60258]: pam_unix(sudo:session): session opened for user root(uid=0) by amestre(uid=1000)
out 02 04:50:27 skodjidigital sudo[60258]: amestre : TTY=/dev/pts/1 ; PWD=/home/amestre ; USER=root ; COMMAND=/usr/bin/fail2ban-client status
out 02 04:50:27 skodjidigital sudo[60258]: pam_unix(sudo:session): session closed for user root
out 02 04:51:35 skodjidigital kernel: [UFW BLOCK] IN=enp0s3 OUT= MAC=01:00:5e:00:00:01:30:16:9d:ee:0e:ac:08:00 SRC=192.168.4.1 DST=224.0.0.1 LEN=36 TOS=0>
out 02 04:53:40 skodjidigital kernel: [UFW BLOCK] IN=enp0s3 OUT= MAC=01:00:5e:00:00:01:30:16:9d:ee:0e:ac:08:00 SRC=192.168.4.1 DST=224.0.0.1 LEN=36 TOS=0>
out 02 04:53:52 skodjidigital login[1193]: pam_unix(login:session): session opened for user amestre(uid=1000) by amestre(uid=0)
out 02 04:53:52 skodjidigital systemd-logind[1127]: New session '27' of user 'amestre' with class 'user' and type 'tty'.
out 02 04:53:52 skodjidigital systemd[1]: Started session-27.scope - Session 27 of User amestre.
out 02 04:53:52 skodjidigital systemd[4083]: Reached target sound.target - Sound Card.
out 02 04:53:53 skodjidigital 55-scsi-sg3_id.rules[60371]: WARNING: SCSI device sr0 has no device ID, consider changing .SCSI_ID_SERIAL_SRC in 00-scsi-sg>
out 02 04:55:45 skodjidigital kernel: [UFW BLOCK] IN=enp0s3 OUT= MAC=01:00:5e:00:00:01:30:16:9d:ee:0e:ac:08:00 SRC=192.168.4.1 DST=224.0.0.1 LEN=36 TOS=0>
out 02 04:57:37 skodjidigital systemd[1]: Starting fwupd-refresh.service - Refresh fwupd metadata and update motd...
out 02 04:57:37 skodjidigital systemd[1]: fwupd-refresh.service: Deactivated successfully.
out 02 04:57:37 skodjidigital systemd[1]: Finished fwupd-refresh.service - Refresh fwupd metadata and update motd.
out 02 04:57:50 skodjidigital kernel: [UFW BLOCK] IN=enp0s3 OUT= MAC=01:00:5e:00:00:01:30:16:9d:ee:0e:ac:08:00 SRC=192.168.4.1 DST=224.0.0.1 LEN=36 TOS=0>
out 02 04:59:55 skodjidigital kernel: [UFW BLOCK] IN=enp0s3 OUT= MAC=01:00:5e:00:00:01:30:16:9d:ee:0e:ac:08:00 SRC=192.168.4.1 DST=224.0.0.1 LEN=36 TOS=0>
out 02 05:00:44 skodjidigital systemd[1]: Starting sysstat-collect.service - system activity accounting tool...
out 02 05:00:44 skodjidigital systemd[1]: sysstat-collect.service: Deactivated successfully.
out 02 05:00:44 skodjidigital systemd[1]: Finished sysstat-collect.service - system activity accounting tool.
out 02 05:02:00 skodjidigital kernel: [UFW BLOCK] IN=enp0s3 OUT= MAC=01:00:5e:00:00:01:30:16:9d:ee:0e:ac:08:00 SRC=192.168.4.1 DST=224.0.0.1 LEN=36 TOS=0>
out 02 05:03:02 skodjidigital sshd-session[58809]: Read error from remote host 192.168.4.32 port 62443: Connection timed out
out 02 05:03:02 skodjidigital sshd-session[58708]: pam_unix(sshd:session): session closed for user amestre
out 02 05:03:02 skodjidigital systemd[1]: session-16.scope: Deactivated successfully.
out 02 05:03:02 skodjidigital systemd[1]: session-16.scope: Consumed 3.837s CPU time over 2h 23min 48.958s wall clock time, 110.8M memory peak.
out 02 05:03:02 skodjidigital systemd-logind[1127]: Session 16 logged out. Waiting for processes to exit.
out 02 05:03:02 skodjidigital systemd-logind[1127]: Removed session 16.
out 02 05:04:05 skodjidigital kernel: [UFW BLOCK] IN=enp0s3 OUT= MAC=01:00:5e:00:00:01:30:16:9d:ee:0e:ac:08:00 SRC=192.168.4.1 DST=224.0.0.1 LEN=36 TOS=0>
out 02 05:06:10 skodjidigital kernel: [UFW BLOCK] IN=enp0s3 OUT= MAC=01:00:5e:00:00:01:30:16:9d:ee:0e:ac:08:00 SRC=192.168.4.1 DST=224.0.0.1 LEN=36 TOS=0>
out 02 05:08:15 skodjidigital kernel: [UFW BLOCK] IN=enp0s3 OUT= MAC=01:00:5e:00:00:01:30:16:9d:ee:0e:ac:08:00 SRC=192.168.4.1 DST=224.0.0.1 LEN=36 TOS=0>
out 02 05:08:53 skodjidigital sudo[60431]: pam_unix(sudo:session): session opened for user root(uid=0) by amestre(uid=1000)
out 02 05:08:53 skodjidigital sudo[60431]: amestre : TTY=/dev/pts/1 ; PWD=/home/amestre ; USER=root ; COMMAND=/usr/bin/tail -n 25 /var/log/syslog
out 02 05:08:53 skodjidigital sudo[60431]: pam_unix(sudo:session): session closed for user root
out 02 05:10:20 skodjidigital kernel: [UFW BLOCK] IN=enp0s3 OUT= MAC=01:00:5e:00:00:01:30:16:9d:ee:0e:ac:08:00 SRC=192.168.4.1 DST=224.0.0.1 LEN=36 TOS=0>
out 02 05:10:20 skodjidigital systemd[1]: Starting sysstat-collect.service - system activity accounting tool...
out 02 05:10:20 skodjidigital systemd[1]: sysstat-collect.service: Deactivated successfully.
out 02 05:10:20 skodjidigital systemd[1]: Finished sysstat-collect.service - system activity accounting tool.
out 02 05:11:00 skodjidigital sudo[60467]: pam_unix(sudo:session): session opened for user root(uid=0) by amestre(uid=1000)
out 02 05:11:00 skodjidigital sudo[60467]: amestre : TTY=/dev/pts/1 ; PWD=/home/amestre ; USER=root ; COMMAND=/usr/bin/journalctl -n 40
lines 1-40/40 (END)


## Log de autenticação do ficheiro auth-log
2026-10-02T02:43:33.605272+00:00 skodjidigital sshd-session[59053]: Received disconnect from 192.168.4.32 port 51181:11:
2026-10-02T02:43:33.609513+00:00 skodjidigital sshd-session[59053]: Disconnected from user amestre 192.168.4.32 port 51181
2026-10-02T02:43:33.615557+00:00 skodjidigital sshd-session[58932]: pam_unix(sshd:session): session closed for user amestre
2026-10-02T02:43:33.620463+00:00 skodjidigital sshd-session[58931]: pam_unix(sshd:session): session closed for user amestre
2026-10-02T02:43:33.640374+00:00 skodjidigital systemd-logind[1127]: Session 19 logged out. Waiting for processes to exit.
2026-10-02T02:43:33.645065+00:00 skodjidigital systemd-logind[1127]: Removed session 19.
2026-10-02T02:43:33.663061+00:00 skodjidigital systemd-logind[1127]: Session 20 logged out. Waiting for processes to exit.
2026-10-02T02:43:33.669634+00:00 skodjidigital systemd-logind[1127]: Removed session 20.
2026-10-02T02:43:55.990100+00:00 skodjidigital sshd-session[59060]: Accepted password for amestre from 192.168.4.32 port 52018 ssh2
2026-10-02T02:43:55.997659+00:00 skodjidigital sshd-session[59060]: pam_unix(sshd:session): session opened for user amestre(uid=1000) by amestre(uid=0)
2026-10-02T02:43:56.027121+00:00 skodjidigital systemd-logind[1127]: New session '21' of user 'amestre' with class 'user' and type 'tty'.
2026-10-02T03:10:01.029560+00:00 skodjidigital CRON[59467]: pam_unix(cron:session): session opened for user root(uid=0) by root(uid=0)
2026-10-02T03:10:01.037905+00:00 skodjidigital CRON[59467]: pam_unix(cron:session): session closed for user root
2026-10-02T03:11:52.814145+00:00 skodjidigital sshd-session[59475]: Accepted password for amestre from 192.168.4.32 port 61758 ssh2
2026-10-02T03:11:52.821023+00:00 skodjidigital sshd-session[59475]: pam_unix(sshd:session): session opened for user amestre(uid=1000) by amestre(uid=0)
2026-10-02T03:11:52.854126+00:00 skodjidigital systemd-logind[1127]: New session '23' of user 'amestre' with class 'user' and type 'tty'.
2026-10-02T03:17:01.091451+00:00 skodjidigital CRON[59566]: pam_unix(cron:session): session opened for user root(uid=0) by root(uid=0)
2026-10-02T03:17:01.103933+00:00 skodjidigital CRON[59566]: pam_unix(cron:session): session closed for user root
2026-10-02T03:36:06.848647+00:00 skodjidigital sudo: pam_unix(sudo:session): session opened for user root(uid=0) by amestre(uid=1000)
2026-10-02T03:36:06.860561+00:00 skodjidigital sudo: amestre : TTY=/dev/pts/2 ; PWD=/home/amestre ; USER=root ; COMMAND=/usr/bin/systemctl status nginx
2026-10-02T03:36:09.476219+00:00 skodjidigital sudo: pam_unix(sudo:session): session closed for user root
2026-10-02T03:39:16.922275+00:00 skodjidigital sudo: pam_unix(sudo:session): session opened for user root(uid=0) by amestre(uid=1000)
2026-10-02T03:39:16.923420+00:00 skodjidigital sudo: amestre : TTY=/dev/pts/2 ; PWD=/home/amestre ; USER=root ; COMMAND=/usr/bin/tail -n 10 /var/log/nginx/auth.log
2026-10-02T03:39:16.949056+00:00 skodjidigital sudo: pam_unix(sudo:session): session closed for user root
2026-10-02T03:39:49.476912+00:00 skodjidigital sudo: pam_unix(sudo:session): session opened for user root(uid=0) by amestre(uid=1000)
2026-10-02T03:39:49.477476+00:00 skodjidigital sudo: amestre : TTY=/dev/pts/2 ; PWD=/home/amestre ; USER=root ; COMMAND=/usr/bin/tail -n 10 /var/log/auth.log
2026-10-02T03:39:49.500474+00:00 skodjidigital sudo: pam_unix(sudo:session): session closed for user root
2026-10-02T03:40:01.621679+00:00 skodjidigital sshd-session[47331]: Read error from remote host 192.168.4.32 port 51288: Connection timed out
2026-10-02T03:40:01.624292+00:00 skodjidigital sshd-session[47230]: pam_unix(sshd:session): session closed for user amestre
2026-10-02T03:40:01.653235+00:00 skodjidigital sshd-session[47230]: syslogin_perform_logout: logout() returned an error
2026-10-02T03:40:01.672854+00:00 skodjidigital systemd-logind[1127]: Session 13 logged out. Waiting for processes to exit.
2026-10-02T03:40:01.700473+00:00 skodjidigital systemd-logind[1127]: Removed session 13.
2026-10-02T03:44:19.308471+00:00 skodjidigital sudo: pam_unix(sudo:session): session opened for user root(uid=0) by amestre(uid=1000)
2026-10-02T03:44:19.324260+00:00 skodjidigital sudo: amestre : TTY=/dev/pts/2 ; PWD=/home/amestre ; USER=root ; COMMAND=/usr/bin/tail -n 10 journalctl
2026-10-02T03:44:19.335505+00:00 skodjidigital sudo: pam_unix(sudo:session): session closed for user root
2026-10-02T04:01:12.738182+00:00 skodjidigital sudo: pam_unix(sudo:session): session opened for user root(uid=0) by amestre(uid=1000)
2026-10-02T04:01:12.745384+00:00 skodjidigital sudo: amestre : TTY=/dev/pts/2 ; PWD=/home/amestre ; USER=root ; COMMAND=/usr/bin/journalctl -n 50
2026-10-02T04:01:18.451394+00:00 skodjidigital sudo: pam_unix(sudo:session): session closed for user root
2026-10-02T04:07:50.585742+00:00 skodjidigital sudo: pam_unix(sudo:session): session opened for user root(uid=0) by amestre(uid=1000)
2026-10-02T04:07:50.601948+00:00 skodjidigital sudo: amestre : TTY=/dev/pts/2 ; PWD=/home/amestre ; USER=root ; COMMAND=/usr/bin/tail -n 40 /var/log/auth.log

## Log de sistema pela leitura pelo ficheiro syslog
2026-10-02T04:47:25.827400+00:00 skodjidigital kernel: [UFW BLOCK] IN=enp0s3 OUT= MAC=01:00:5e:00:00:01:30:16:9d:ee:0e:ac:08:00 SRC=192.168.4.1 DST=224.0.0.1 LEN=36 TOS=0x00 PREC=0x00 TTL=1 ID=60135 DF PROTO=2
2026-10-02T04:49:30.756064+00:00 skodjidigital kernel: [UFW BLOCK] IN=enp0s3 OUT= MAC=01:00:5e:00:00:01:30:16:9d:ee:0e:ac:08:00 SRC=192.168.4.1 DST=224.0.0.1 LEN=36 TOS=0x00 PREC=0x00 TTL=1 ID=65459 DF PROTO=2
2026-10-02T04:50:10.500610+00:00 skodjidigital systemd[1]: Starting sysstat-collect.service - system activity accounting tool...
2026-10-02T04:50:10.584967+00:00 skodjidigital systemd[1]: sysstat-collect.service: Deactivated successfully.
2026-10-02T04:50:10.585990+00:00 skodjidigital systemd[1]: Finished sysstat-collect.service - system activity accounting tool.
2026-10-02T04:51:35.788675+00:00 skodjidigital kernel: [UFW BLOCK] IN=enp0s3 OUT= MAC=01:00:5e:00:00:01:30:16:9d:ee:0e:ac:08:00 SRC=192.168.4.1 DST=224.0.0.1 LEN=36 TOS=0x00 PREC=0x00 TTL=1 ID=2957 DF PROTO=2
2026-10-02T04:53:40.821036+00:00 skodjidigital kernel: [UFW BLOCK] IN=enp0s3 OUT= MAC=01:00:5e:00:00:01:30:16:9d:ee:0e:ac:08:00 SRC=192.168.4.1 DST=224.0.0.1 LEN=36 TOS=0x00 PREC=0x00 TTL=1 ID=10584 DF PROTO=2
2026-10-02T04:53:52.392433+00:00 skodjidigital systemd[1]: Started session-27.scope - Session 27 of User amestre.
2026-10-02T04:53:52.950052+00:00 skodjidigital systemd[4083]: Reached target sound.target - Sound Card.
2026-10-02T04:53:53.409575+00:00 skodjidigital 55-scsi-sg3_id.rules: WARNING: SCSI device sr0 has no device ID, consider changing .SCSI_ID_SERIAL_SRC in 00-scsi-sg3_config.rules
2026-10-02T04:55:45.849954+00:00 skodjidigital kernel: [UFW BLOCK] IN=enp0s3 OUT= MAC=01:00:5e:00:00:01:30:16:9d:ee:0e:ac:08:00 SRC=192.168.4.1 DST=224.0.0.1 LEN=36 TOS=0x00 PREC=0x00 TTL=1 ID=15263 DF PROTO=2
2026-10-02T04:57:37.509497+00:00 skodjidigital systemd[1]: Starting fwupd-refresh.service - Refresh fwupd metadata and update motd...
2026-10-02T04:57:37.884044+00:00 skodjidigital systemd[1]: fwupd-refresh.service: Deactivated successfully.
2026-10-02T04:57:37.884603+00:00 skodjidigital systemd[1]: Finished fwupd-refresh.service - Refresh fwupd metadata and update motd.
2026-10-02T04:57:50.779049+00:00 skodjidigital kernel: [UFW BLOCK] IN=enp0s3 OUT= MAC=01:00:5e:00:00:01:30:16:9d:ee:0e:ac:08:00 SRC=192.168.4.1 DST=224.0.0.1 LEN=36 TOS=0x00 PREC=0x00 TTL=1 ID=16247 DF PROTO=2
2026-10-02T04:59:55.810005+00:00 skodjidigital kernel: [UFW BLOCK] IN=enp0s3 OUT= MAC=01:00:5e:00:00:01:30:16:9d:ee:0e:ac:08:00 SRC=192.168.4.1 DST=224.0.0.1 LEN=36 TOS=0x00 PREC=0x00 TTL=1 ID=17709 DF PROTO=2
2026-10-02T05:00:44.860650+00:00 skodjidigital systemd[1]: Starting sysstat-collect.service - system activity accounting tool...
2026-10-02T05:00:44.939159+00:00 skodjidigital systemd[1]: sysstat-collect.service: Deactivated successfully.
2026-10-02T05:00:44.940376+00:00 skodjidigital systemd[1]: Finished sysstat-collect.service - system activity accounting tool.
2026-10-02T05:02:00.842160+00:00 skodjidigital kernel: [UFW BLOCK] IN=enp0s3 OUT= MAC=01:00:5e:00:00:01:30:16:9d:ee:0e:ac:08:00 SRC=192.168.4.1 DST=224.0.0.1 LEN=36 TOS=0x00 PREC=0x00 TTL=1 ID=17868 DF PROTO=2
2026-10-02T05:03:02.421531+00:00 skodjidigital systemd[1]: session-16.scope: Deactivated successfully.
2026-10-02T05:03:02.429679+00:00 skodjidigital systemd[1]: session-16.scope: Consumed 3.837s CPU time over 2h 23min 48.958s wall clock time, 110.8M memory peak.
2026-10-02T05:04:05.873005+00:00 skodjidigital kernel: [UFW BLOCK] IN=enp0s3 OUT= MAC=01:00:5e:00:00:01:30:16:9d:ee:0e:ac:08:00 SRC=192.168.4.1 DST=224.0.0.1 LEN=36 TOS=0x00 PREC=0x00 TTL=1 ID=30058 DF PROTO=2
2026-10-02T05:06:10.903922+00:00 skodjidigital kernel: [UFW BLOCK] IN=enp0s3 OUT= MAC=01:00:5e:00:00:01:30:16:9d:ee:0e:ac:08:00 SRC=192.168.4.1 DST=224.0.0.1 LEN=36 TOS=0x00 PREC=0x00 TTL=1 ID=38984 DF PROTO=2
2026-10-02T05:08:15.833051+00:00 skodjidigital kernel: [UFW BLOCK] IN=enp0s3 OUT= MAC=01:00:5e:00:00:01:30:16:9d:ee:0e:ac:08:00 SRC=192.168.4.1 DST=224.0.0.1 LEN=36 TOS=0x00 PREC=0x00 TTL=1 ID=50859 DF PROTO=2