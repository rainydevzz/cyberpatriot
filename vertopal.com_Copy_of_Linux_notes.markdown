Keep sudo running - su

Update/Upgrade software packages - Sudo apt-get update && apt-get dist-
upgrade

[John]{.underline}

Apt-get \--purge autoremove john

[Services]{.underline}

Service \--status -all

Service vsftpd stop (start or restart)

[Netcat]{.underline}

Apt-get \--purge autoremove netcat \*

[Cron]{.underline}

Ls -la /etc/cron\*

(lists users in the crontab) crontab -

[Apache]{.underline}

Apt-get install apache

[SSH]{.underline}

Nano /etc/ssh/ssh_config

PERMIT ROOT LOGIN NO

X11 Forwarding NO

PERMIT EMPTY PASSWORDS NO

[Common Services]{.underline}

Databases: MySQL, MariaDB

Filesharing: Smbd, vsftp

Networking: Bind9, sshd, Telnet

Webservers: Apache2, jetty, ngnix, tomcat

Backdoors: Netcat, PHPass (rare on linux)

Hacking tools: John, metasploit, aircrack, armitage, hydra, rainbow
crack, hashcat

[Firewall]{.underline}

Ufw enable

Ufw disable

Ufw status

Ufw allow 22

Ufw deny 80

Ufw default deny

[Users]{.underline}

Useradd \[username\]

Userdel \[username\]

Passwd \[username\]

Passwd \[root\]

[/etc/ files]{.underline}

[/etc/passwd #user:leon/home/]{.underline}

[/etc/group adm: leon, alex, nick]{.underline}

[/etc/shadow \$!454545qfgffsgdfgsdf (bad)]{.underline}

[\$4584853jfj (good)]{.underline}

[Hidden Files]{.underline}

Control-H while in a directory

Usually stays on after using once
