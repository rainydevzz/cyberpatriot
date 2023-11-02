# **Ubuntu**

**Down Debian version here** [**http://www.webmin.com/download.html**](http://www.webmin.com/download.html)

**Admin Passwords- Cyb3rP4tr10t5Users- P@$$word**

Updates (sudo apt-get install updates/upgrades)

- Update Sudo
- Browsers
- Bash
- Root
- SSH
- Needed services (check readme)

Configure Update settings

Dash home icon\>Software Updates

- Only enable important security and recommended updates
- Check for updates automatically daily
- Download and install security updates immediately
- Display other available updates immediately
- Install Ubuntu updates

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

Dash home icon\>Update manager\>Setttings

- Auto check for updates - Daily
- When there are security updates - Immediately
- Other updates - Immediately
- New Ubuntu Versions - For long term support versions

Ubuntu Firewall

Terminal

Terminal Input\> sudo ufw enable

Terminal Input\> sudo apt-get install update

GUI

Terminal Input\>sudo apt-get install gufw

Status: On or off

Incoming (traffic): Deny or allow (Default is allow)

Other things include Rules, Report, Log

User Accounts

Check for hidden users

Use # to make user not recognized but keep files

gedit /etc/lightdm/lightdm.conf

[SeatDefaults]

greeter-show-manual-login = true

greeter-hide-users = true

allow-guest = false

Enable Audits

- Terminal Input\> apt-get install auditd
- Terminal Input\> auditctl -e 1
- Terminal Input\> gedit /etc/audit/auditd.conf

Finding prohibited Files

- Terminal Input\> find / -name ".XYZ"
- Mp3
- Wav
- Wmv
- Wma
- Mp4
- Gif
- Jpg
- Jpeg
- Png
- Avi

Services

- Apt-get install bum
- Terminal input\> bum
- "Bum" stands for Boot up manager
- Password policy- Terminal input\> apt-get install libpam-cracklib --force-yes-y
- Password History- Terminal input\> gedit /etc/pam.d/common-password

Password Policy

Sudo apt-get install libpam-cracklib --force-yes -y

**To access the common-auth file:**

Sudo gedit /etc/pam.d/common-auth'

**At the end of this file, add:**

auth optional pam\_tally.so deny=5

unlock\_time=900 onerr=fail audit

even\_deny\_root\_account silent

**To see running processes**

ps -a

**To edit SSH files**

Sudo gedit /etc/ssh/sshd\_config

Find where it says **PermitRootLogin=YES** and change it to a no

Or use the command-

$ (sudo) sed -i 's/PermitRootLogin yes/PermitRootLogin no/g' /etc/ssh/sshd\_config

To disable X11 Forwarding

$ (sudo) sed -i 's/X11Forwarding yes/X11Forwarding no/g' /etc/ssh/sshd\_config

_ **NETSTAT** _

**Network Security** :

Linux is usually server based: Incorrect server configuration can often result in a way in for attackers

**Using Super Server Restrictions:**

Network Server Programs directly open network ports and listen for connections

Distributions (including Ubuntu) use a _Super server_ or _super daemon_ which is a program that listens for network connections used by another program. When a connection opens, this _super server_ gives the connection to the server intended for that port.

**Two primary super daemons:**

inetd

xinetd

inetd handles security by using a package called TCP wrappers while xinetd security features are built into itself. The inetd package is also a legacy super daemon; many will not encounter it as it is not usually still installed on Linux and it should not be expected in competitions.

**Setting up inetd:**

(add in later) (not useful enough and too time consuming)

**Updating a programs executable status:**

Using the chmod command, you can adjust a programs executable status by changing the executable bit stored with the file

**Retrieve a command:**

You can press the up arrow on the keyboard to retrieve a previous command. You could also use the Ctrl+P and the Ctrl+N instead of using the up and down arrow keys

**Search for a command** :

Press Ctrl+R to begin a reverse search. You can start typing characters that are in any part of the command, not just the beginning. If you cannot find the correct command, you can either keep typing until it comes up, or you could press Ctrl+R repeatedly until you find it.

The Ctrl+S keystroke is used to search forward in your command history. This can be used while using the Ctrl+R command; this will cause the history search from backward to forward. If Andrew is a donk and passes the command, this can be used to go back to it

**If the Ctrl+S keystroke causes the terminal to hang, press Ctrl+Q to go back and resume. To prevent the terminal from hanging when Ctrl+S is used, type stty -ixon in the terminal.**

If you cannot find the command or wish to stop searching, press Ctrl+G

**Command History:**

Typing history -c will clear your command history **DO NOT DO THIS DURING COMPETITIONS!!!!!!**

**Root account:**

Root accounts usually have shorter paths than other user accounts. Regular use of the root path is discouraged and day to day programs/files are not usually stored in the path in order to lessen the chance of malicious files being run from root. The roots path should also never include the current directory (./). **Placing this in the roots path make it possible for troublemakers to trick root into running replacements for common programs**

**Bash** :

Bash history is stored in a file that can be seen by anyone. The file ~/.bash\_history

7
