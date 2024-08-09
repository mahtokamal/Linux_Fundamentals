# List of Linux Basic Commands

## File and Directory

### ls (la)
    Descriptions:- list directory contents (including files and folders)
    
    Example:- ls -a
    Output:- Desktop  Documents  Downloads  Music  Pictures  Public  snap  Templates  Videos .ssh .config  
    flags (-a, -l, -h, -r, -t, -R, -i, -I, -v, -f, -t) 
    a - all includes hidden files and folder (directory)
    l - long list
    h - human readable format
    t - sort by time 
    R - Recursive files of folders 
    i - Interactivity (prompt before every removal)
    I - prompt once before removing more than three files, or when removing recursively;
    v - Verbose (prompt shows what is being done)
    f - forcefully 
    t - sort by time
        
> [!NOTE]
> **Flags** are used to modify the behavior of a command. For example ls -a, -a tells the ls executable to list all files in the directoy, including hidden ones. Flags are also called **OPTIONS**.
 
### cd
     Description:- change directory or file
     
     Example:- cd Desktop/, cd, cd ..
     Output: goes to Desktop directory or folder.
 
### dir
     Description:- list directory contents
     
     Example:- dir
     Output:- Desktop  Documents  Downloads  Music  Pictures	Public	snap  Templates  Videos
 
### pwd
     Description:- print name of current/working directory
     
     Example:- pwd
     Output:- /home/kamal/Desktop
 
### mkdir
     Description:- make directories
     
     Example:- mkdir examples/
     Output:- Desktop    Downloads  Music     Public  Templates Documents  examples   Pictures  snap    Videos
 
 ### rmdir
     Description:- remove empty directories
     
     Example:- rmdir examples/ or rm -d examples/
     Output:- Desktop    Downloads  Music     Public  Templates Documents Pictures  snap    Videos
 
 ### rm
     Description:- remove files or directories
     
     Example:- rmdir -iR examples/ or rm password.txt(removes file)
     Output:- Desktop    Downloads  Music     Public  Templates Documents Pictures  snap    Videos
 
 ### cp
     Description:- copy files and directories
     
     Example:- cp password.txt security/ or cp -r kam/ kam2/ 
     Output:- 
> [!NOTE]
> Use flags such as -R -r(recursively copies files or folder inside the directory) while copying directories to another. 
     
 ### mv
     Description:- move (rename) files or directories
     
     Example:- mv k1.txt kam2/ (moving files k1.txt to directory kam2/)
     Example:- mv kam.txt k1.txt (renaming file kam.txt to k1.txt)
     Example:- mv kam/ kam2/ (renaming directory kam/ to kam2/)
     Example:- mv kam/ kam3/ (moving directory kam/ to kam3/)
     Output:-  
 ### touch
     Description:- change file timestamps (create files with empty contents)
     
     Example:- touch hello.txt
     Output:- 
 ### nano
     Description:- open files in nano text-editors
     
     Example:- nano hello.txt
     Output:- 
 ### gedit
     Description:- open files in gedit text-editors
     
     Example:- gedit hello.txt
     Output:- 
 ### cat
     Description:- concatenate files and print on the standard output (to view contents of file)
     
     Example:- cat hello.txt
     Output:-  This is your right time to
               follow your passion.

 ### tac
     Description:- concatenate and print files in reverse 
     
     Example:- tac hello.txt
     Output:-  follow your passion.
               This is your right time to

 ### grep
    Description:- print lines that match patterns
    
    Example:- grep "time" k1.txt
    Output:-  This is your right **time**.
              **time** and tide wait for none.

 ### uniq
     Description:- report or omit(filters-out) repeated lines in a file. Uniq helps to detect the adjacent duplicate lines 
     and also deletes the duplicate lines. 

     -c (count) : Prefix lines by the number of occurrences in the input, followed by a space.
     
     -d (repeated) : Only output lines that are repeated in the input.
     -i (ignore-case) : Ignore differences in case when comparing lines.
     -f (skip-fields=N) : Avoid comparing the first N fields in each line.
     -s (skip-chars=N) : Avoid comparing the first N characters in each line.
     -u (unique) :  Only output lines that are unique in the input.

     
     Example:- cat hello.txt
     Output:-  I love cricket.
               I love cricket.
               I love cricket.

               I love music of Shankar.
               I love music of Shankar.

               Thank You!
     
     Example:- uniq hello.txt
     Output:-  I love cricket.

               I love music of Shankar.

               Thank You!

     Example:- uniq -u hello.txt (shows only unique lines without duplicate lines)
     Output:-  
     
               Thank You!

> [!NOTE]
> uniq isn’t able to detect the duplicate lines unless they are adjacent to each other. The content in the file must be therefore sorted before using uniq or you can simply use sort -u instead of uniq command.
   
 ### diff
     Description:- compare files line by line
     
     Example:- cat a.txt
     Output:-  Gujarat
               Uttar Pradesh
               Kolkata
               Bihar
               Jammu and Kashmir

     Example:- cat b.txt
     Output:-  Tamil Nadu
               Gujarat
               Andhra Pradesh
               Bihar
               Uttar Pradesh

     Example:- 
     Output:- 0a1
            > Tamil Nadu
            2,3c3
            < Uttar Pradesh
            < Kolkata
            ---
            > Andhra Pradesh
            5c5
            < Jammu and Kashmir
            ---
            > Uttar Pradesh
The first line of the diff output will contain:  
- Line numbers corresponding to the first file,
- A special symbol and
- Line numbers corresponding to the second file.

Like in our case, 0a1 which means after lines 0(at the very beginning of file) you have to add Tamil Nadu to match the second file line number 1. It then tells us what those lines are in each file preceded by the symbol:

- Lines preceded by a < are lines from the first file.
- Lines preceded by > are lines from the second file.
- Next line contains 2,3c3 which means from line 2 to line 3 in the first file needs to be changed to match line number 3 in the second file. It then tells us those lines with the above symbols.
- The three dashes (“—“) merely separate the lines of file 1 and file 2.

> [!IMPORTANT]
> As a summary to make both the files identical, first add Tamil Nadu in the first file at very beginning to match line 1 of second file after that change line 2 and 3 of first file i.e. Uttar Pradesh and Kolkata with line 3 of second file i.e. Andhra Pradesh. After that change line 5 of first file i.e. Jammu and Kashmir with line 5 of second file i.e. Uttar Pradesh. 
     
 ### less
     Description:- opposite of more. Less command is a Linux utility that can be used to read the contents of a text file 
     one page (one screen) at a time. It has faster access because if a file is large, it doesn’t access the complete file, 
     but accesses it page by page. 

     For example, if it’s a large file and you are reading it using any text editor, then the complete file will be loaded 
     to the main memory. The less command doesn’t load the entire file but loads it part by part which makes it faster. 

     Example:- less [options/flags] filename
     Example:- 
 
 ### more
     Description:- file perusal filter for crt viewing. more command is used to view the text files in the command prompt, 
     displaying one screen at a time in case the file is large (For example log files). The more command also allows the 
     user do scroll up and down through the page. The syntax along with options and command is as follows. Another 
     application of more is to use it with some other command after a pipe. When the output is large, we can use more 
     command to see output one by one.

     
     Example:- less [options/flags] filename
     Example:- 
 
 ### head
     Description:- output the first part of files
     
     Example:- head -n 20 thousands.txt (print first 20 lines of files)
     Example:- head thousands.txt
     Output:-  1
               2
               3
               4
               5
               6
               7
               8
               9
               10

    for((i=1;i<=100;i++)); do echo $i >> hundreds.txt;done (prints numbers from 1 - 100 and will be saved into hundreds.txt)
    for((i=1;i<=1000;i++)); do echo $i >> thousands.txt;done (prints numbers from 1 - 100 and will be saved into 
    thousands.txt)

> [!NOTE]
> By default head print the first 10 lines of each FILE to standard output.
 
  ### tail
     Description:- output the last part of files
     
     Example:- tail -n 20 thousands.txt (print last 20 lines of files)
     Example:- tail thousands.txt
     Output:- 991
              992
              993
              994
              995
              996
              997
              998
              999
              1000

> [!NOTE]
> By default tail print the last 10 lines of each FILE to standard output.

 ### find
     Description:- search for files in a directory hierarchy
     
     Example:- find *.txt 
     Example:- find k?.txt ('?' represents exactly one character )
     Example:- find kam*.txt ('*' represents any number of character)
     Output:-

 ### file
     Description:- determine file type
     
     Example:- file k1.txt
     Output:- k1.txt: ASCII text

 ### wc
    Description:- print newline, word, and byte counts for each file
    
    Example:- wc k1.txt
    Output:- 1  5 24 k1.txt (lines, words, characters)
> [!NOTE]
> -c(bytes count),-m(characters count),-l(newlines count ),-L, -w(words count)

 ### zip
     Description:- package and compress (archive) files
     
     Example:- zip zipfile.zip k1.txt thousands.txt (it zips the files k1.txt and thousands.txt into zipfile.zip)
     Output:-  adding: k1.txt (deflated 8%)
               adding: thousands.txt (deflated 53%)

 ### unzip
     Description:- list, test and extract compressed files in a ZIP archive
     
     Example:- unzip zipfile.zip (extraction of zipfile.zip)
     Output:-  Archive:  zipfile.zip
               inflating: k1.txt                  
               inflating: thousands.txt
    Example:- unzip zipfile.zip -d ~/Desktop/extracted/ (extraction of zipfile.zip to destination folder)
    Archive:  zipfile.zip
              inflating: /home/kamal/Desktop/extracted/k1.txt  
              inflating: /home/kamal/Desktop/extracted/thousands.txt
 ### tar

https://www.freecodecamp.org/news/how-to-compress-files-in-linux-with-tar-command/
https://www.cyberciti.biz/howto/question/general/compress-file-unix-linux-cheat-sheet.php
https://www.linuxteck.com/linux-compression-and-archiving-command-cheat-sheet/
 
 ### gz

 ### vim
**--------------------------------------------------------------------------------------------------------------------**
## Networking

 ### ifconfig
    Description:- configure a network interface
    
    Example:- ifconfig
    Output:- 
 
 ### route
    Description:- show / manipulate the IP routing table
    
    Example:- route
    Output:- Kernel IP routing table
             Destination     Gateway         Genmask         Flags Metric Ref    Use Iface
             default         192.168.124.2   0.0.0.0         UG    100    0        0 eth0
             192.168.124.0   0.0.0.0         255.255.255.0   U     100    0        0 eth0)
 
 ### netstat
    Description:- Print network connections, routing tables, interface statis‐tics, masquerade connections, and multicast 
    memberships
    
    Example:- netstat
    Example:- nestat -aut (all ports of TCP and UDP)
    Output:- Active Internet connections (servers and established)
             Proto Recv-Q Send-Q Local Address           Foreign Address         State      
             udp        0      0 192.168.124.128:bootpc  192.168.124.254:bootps  ESTABLISHED

 
 ### whois
    Description:- client for the whois directory service. Whois is a command-line utility used in Linux systems to retrieve 
    information about domain names, IP addresses, and network devices registered with the Internet Corporation for Assigned 
    Names and Numbers (ICANN). The data received by Whois consists of the name and contact information of the domain or IP 
    address owner, the registration and expiration date, the domain registrar, and the server information.
    
    Example:- whois geeksforgeeks.org 
    Output:- Domain Name: geeksforgeeks.org
            Registry Domain ID: f507261c73964021b7430545a8b370ee-LROR
            Registrar WHOIS Server: http://whois.publicdomainregistry.com
            Registrar URL: http://www.publicdomainregistry.com
            Updated Date: 2022-04-21T06:36:07Z
            Creation Date: 2009-03-19T06:08:55Z
            Registry Expiry Date: 2030-03-19T06:08:55Z
            Registrar: PDR Ltd. d/b/a PublicDomainRegistry.com
            Registrar IANA ID: 303
            Registrar Abuse Contact Email: abuse@publicdomainregistry.com
            Registrar Abuse Contact Phone: +1.2013775952
            Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited
            Registry Registrant ID: REDACTED FOR PRIVACY
            Registrant Name: REDACTED FOR PRIVACY
            Registrant Organization: Privacy Protect, LLC (PrivacyProtect.org)
            Registrant Street: REDACTED FOR PRIVACY
            Registrant City: REDACTED FOR PRIVACY
            Registrant State/Province: MA
            Registrant Postal Code: REDACTED FOR PRIVACY
            Registrant Country: US


 
 ### ping
    Description:- send ICMP ECHO_REQUEST to network hosts
    
    Example:- ping google.com
    Output:- PING google.com (142.251.36.238) 56(84) bytes of data.
            64 bytes from muc11s22-in-f14.1e100.net (142.251.36.238): icmp_seq=1 ttl=128 time=63.6 ms
            64 bytes from muc11s22-in-f14.1e100.net (142.251.36.238): icmp_seq=2 ttl=128 time=58.9 ms
            64 bytes from muc11s22-in-f14.1e100.net (142.251.36.238): icmp_seq=3 ttl=128 time=53.7 ms
            64 bytes from muc11s22-in-f14.1e100.net (142.251.36.238): icmp_seq=4 ttl=128 time=51.0 ms
            64 bytes from muc11s22-in-f14.1e100.net (142.251.36.238): icmp_seq=5 ttl=128 time=50.2 ms

 
 ### dig
    Description:- DNS lookup utility. dig command stands for Domain Information Groper. It is used for retrieving 
    information about DNS name servers. It is basically used by network administrators. It is used for verifying and 
    troubleshooting DNS problems and to perform DNS lookups. Dig command replaces older tools such as nslookup and the host.
    
    Example:- dig geeksforgeeks.org
    Output:- ; <<>> DiG 9.18.16-1-Debian <<>> geeksforgeeks.org
            ;; global options: +cmd
            ;; Got answer:
            ;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 6320
            ;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1
            
            ;; OPT PSEUDOSECTION:
            ; EDNS: version: 0, flags:; MBZ: 0x0005, udp: 512
            ;; QUESTION SECTION:
            ;geeksforgeeks.org.             IN      A
            
            ;; ANSWER SECTION:
            geeksforgeeks.org.      5       IN      A       34.218.62.116
            
            ;; Query time: 28 msec
            ;; SERVER: 192.168.124.2#53(192.168.124.2) (UDP)
            ;; WHEN: Wed Jul 17 12:50:00 CEST 2024
            ;; MSG SIZE  rcvd: 62

 
 ### host
    Description:- DNS lookup utility.
    
    Example:- host google.com
    Output:- google.com has address 142.251.36.238
            google.com has IPv6 address 2a00:1450:4016:80a::200e
            google.com mail is handled by 10 smtp.google.com.
 
 ### hostname
    Description:- show or set the system's host name
    
    Example:- hostname
    Output:- Ubuntu

**--------------------------------------------------------------------------------------------------------------------**

## User & Group
### users
    Description:- print the user names of users currently logged in to the current host.
    
    Example:- users
    Output:- kamal

### useradd
    Description:- useradd - create a new user or update default new user information.
    
    Example:- sudo useradd sachin
    Output:- [sudo] password for kamal: 

### passwd
    Description:- change user password.
    
    Example:- sudo passwd sachin
    Output:- New password: 
            BAD PASSWORD: The password is shorter than 8 characters
            Retype new password: 
            passwd: password updated successfully.
    
    Example:- cut -d: -f1 /etc/passwd
    Output:- root
            daemon
            bin
            sys
            sync
            games
            man
            lp
            mail
            news
            uucp
            proxy
            www-data
            backup
            list
            irc
            gnats
            nobody
            systemd-network
            systemd-resolve
            messagebus
            systemd-timesync
            syslog
            _apt
            tss
            uuidd
            systemd-oom
            tcpdump
            avahi-autoipd
            usbmux
            dnsmasq
            kernoops
            avahi
            cups-pk-helper
            rtkit
            whoopsie
            sssd
            speech-dispatcher
            fwupd-refresh
            nm-openvpn
            saned
            colord
            geoclue
            pulse
            gnome-initial-setup
            hplip
            gdm
            kamal
            sachin


### userdel
    Description:- delete a user account and related files.
    
    Example:- sudo userdel sachin
    Output:- root
            daemon
            bin
            sys
            sync
            games
            man
            lp
            mail
            news
            uucp
            proxy
            www-data
            backup
            list
            irc
            gnats
            nobody
            systemd-network
            systemd-resolve
            messagebus
            systemd-timesync
            syslog
            _apt
            tss
            uuidd
            systemd-oom
            tcpdump
            avahi-autoipd
            usbmux
            dnsmasq
            kernoops
            avahi
            cups-pk-helper
            rtkit
            whoopsie
            sssd
            speech-dispatcher
            fwupd-refresh
            nm-openvpn
            saned
            colord
            geoclue
            pulse
            gnome-initial-setup
            hplip
            gdm
            kamal

### usermod
    Description:- modify a user account. usermod command or modify user is a command in Linux that is used to change the 
    properties of a user in Linux through the command line. After creating a user we have to sometimes change their 
    attributes like login name, adding to the groups, changing user home directory, password or login directory etc.
    
    Example:- sudo usermod -c "This is a comment examples of a usermode for sachin user" sachin (modifies user sachin by 
    adding comments )

    Example:- sudo cat /etc/passwd | grep sachin
    Output:- sachin:x:1001:1001:This is a comment examples of a usermode for sachin user:/home/sachin:/bin/sh

> [!IMPORTANT]
> The information of a user is stored in the following files:
/etc/passwd, 
/etc/group, 
/etc/shadow, 
/etc/login.defs, 
/etc/gshadow, 
/etc/login.defs

### groups
    Description:- print the groups a user is in.
    
    Example:- groups
    Output:-  kamal adm cdrom sudo dip plugdev lpadmin lxd sambashare

    Example:- groups kamal
    Output:-  kamal : kamal adm cdrom sudo dip plugdev lpadmin lxd sambashare

    Example:- groups sachin
    Output:-  sachin : sachin

### groupadd
    Description:- create a new group. A group is a collection of users with similar permissions or access levels. Groups 
    make it easier to manage and assign permissions to multiple users at once, enhancing security and simplifying 
    administrative tasks.
    
    Example:- sudo groupadd cybersecurity
    Output:- password for kamal: 

    Example:- sudo tail /etc/group
    Output:- colord:x:130:
            geoclue:x:131:
            pulse:x:132:
            pulse-access:x:133:
            gdm:x:134:
            lxd:x:135:kamal
            kamal:x:1000:
            sambashare:x:136:kamal
            sachin:x:1001:
            cybersecurity:x:1002: 

### groupdel
    Description:- delete a group.
    
    Example:- sudo groupdel cybersecurity
    Output:- 

    Example:- sudo tail /etc/group
    Output:- saned:x:129:
            colord:x:130:
            geoclue:x:131:
            pulse:x:132:
            pulse-access:x:133:
            gdm:x:134:
            lxd:x:135:kamal
            kamal:x:1000:
            sambashare:x:136:kamal
            sachin:x:1001:

### groupmod
    Description:- modify a group definition on the system.
    
    Example:- sudo groupmod -n cyberforensic cybersecurity
    Output:- 

    Example:- sudo tail /etc/group
    Output:-  colord:x:130:
            geoclue:x:131:
            pulse:x:132:
            pulse-access:x:133:
            gdm:x:134:
            lxd:x:135:kamal
            kamal:x:1000:
            sambashare:x:136:kamal
            sachin:x:1001:
            cyberforensic:x:1002:

**--------------------------------------------------------------------------------------------------------------------**
## Permission & ownership
### chmod
    Description:- change file mode bits.

**Modes in chmod Command**
1. Symbolic Mode
The following operators can be used with the symbolic mode:

|Operators |Definition |
|----------|----------|
|`+`|Add permissions|
| `-`|Remove permissions |
|`=`|Set the permissions to the specified values|

The following letters that can be used in symbolic mode:
|Letters |Definition |
|----------|----------|
|`r`|Read permission|
| `w`|Write permission |
|`x`|Execute permission|

The following Reference that are used:
|Reference | class |
|----------|----------|
|u|Owner|
| g|Group |
|o|Others|
|a|All (owner,groups,others)|

Examples of Using the Symbolic mode: <br>
Read, write and execute permissions to the file owner: <br>

**Permissiion(before chmod) :-** rw-rw-r-- 1 kamal kamal   27 Mar  9 07:32 t1.txt <br>
**Ex:-** chmod u+rwx t1.txt <br>
**output:-** -rwxrw-r-- 1 kamal kamal   27 Mar  9 07:32 t1.txt <br>

Remove write permission for the group and others: <br>
**Permissiion(before chmod) :-** -rwxrw-r-- 1 kamal kamal   27 Mar  9 07:32 t1.txt <br>
**Ex:-** chmod go-w t1.txt <br>
**output:-** -rwxr--r-- 1 kamal kamal   27 Mar  9 07:32 t1.txt <br>

Read and write for Owner, and Read-only for the group and other: <br>
**Permissiion(before chmod) :-** -rwxr--r-- 1 kamal kamal   27 Mar  9 07:32 t1.txt <br>
**Ex:-** chmod u+rw,go+r t1.txt <br>
**output:-** -rw-r--r-- 1  kamal kamal   27 Mar  9 07:32 t1.txt <br>

2. Octal Mode
 - First digit specify the permission for Owner.
 - Second digit specify the permission for Group. 
 - Third digit specify the permission for Others. 

>[!NOTE]
>The digits are calculated by adding the values of the individual permissions.

|Value | Permisssion |
|----------|----------|
|4|Read Permission|
|2|Write Permission|
|1|Execute Permission|

- 6 represent permission of file Owner which are (rw).
- 7 represent permission of Group which are (rwx).
- 4 represent permission of Other which is (r).
 
**Permissiion(before chmod) :-** -r--r--r-- 1 kamal kamal   27 Mar  9 07:32 t1.txt <br>

  Example:-  chmod 674 t1.txt <br>
  Output:-  -rw-rwxr-- 1 kamal kamal   27 Mar  9 07:32 t1.txt <br>

### chown
    Description:- change file owner and group. This command is particularly useful in scenarios where administrators need 
    to grant or revoke access to specific resources.

**Syntax of chown Command in Linux** <br>
The chown command in Linux has the following syntax: <br>

**chown [options] new_owner[:new_group] file(s)** <br>
Here’s a breakdown of the components: <br>

- `chown`: The base command.
- `options`: Optional flags that modify the behavior of the `chown` command.
- `new_owner[:new_group]`: The new owner and optionally the new group. If `new_group` is omitted, only the owner is changed.
- `file(s)`: The file or files for which ownership is to be changed.

**ownership(before chown) :-** -rw-rwxr-- 1 kamal kamal   27 Mar  9 07:32 t1.txt <br>

To Change the owner of a file in Linux <br>
Syntax:- chown owner_name file_name <br>
Example:- sudo chown sachin t1.txt <br>
Output:-  -rw-rwxr-- 1 sachin kamal   27 Mar  9 07:32 t1.txt <br>

To change the group ownership of a file <br>
Syntax:- chown owner_name file_name <br>
Example:- sudo chown :group1 file1.txt t1.txt <br>
Output:-  -rw-rwxr-- 1 sachin kamal   27 Mar  9 07:32 t1.txt <br>

to Change Owner and Group of the File simultaneously <br>
Syntax:- chown master:group1 file1.txt

### chgrp
    Description:- change group ownership. The `chgrp` command in Linux is used to change the group ownership of a file or 
    directory. All files in Linux belong to an owner and a group. You can set the owner by using “chown” command, and the 
    group by the “chgrp” command.
    
**Group(before chgrp) :-**-rw-rwxr-- 1 sachin kamal   27 Mar  9 07:32 t1.txt <br>

Example:- sudo chgrp sachin t1.txt
Output:- -rw-rwxr-- 1 sachin sachin   27 Mar  9 07:32 t1.txt <br>

**--------------------------------------------------------------------------------------------------------------------**
## Process Management
### ps
    Description:- report a snapshot of the current processes.

    Example:- ps
    Output:-   PID TTY          TIME CMD
              75154 pts/0    00:00:00 bash
              76093 pts/0    00:00:00 ps

    Example:- ps -A or ps -e(to view all running process)
    Output:-   PID TTY          TIME CMD
               1    ?        00:01:36 systemd
               2    ?        00:00:00 kthreadd
               3    ?        00:00:00 rcu_gp
               4    ?        00:00:00 rcu_par_gp
               5    ?        00:00:00 slub_flushwq
               6    ?        00:00:00 netns



Result contains four columns of information. Where, 
- PID:- the unique process ID 
- TTY:- terminal type that the user is logged into 
- TIME:- amount of CPU in minutes and seconds that the process has been running 
- CMD:- name of the command that launched the process. 

    

### top
    Description:- Display Linux processes. It provides a dynamic real-time view of the running system. Usually, this 
    command shows the summary information of the system and the list of processes or threads which are currently managed by 
    the Linux Kernel. As soon as you will run this command it will open an interactive command mode where the top half 
    portion will contain the statistics of processes and resource usage. And Lower half contains a list of the currently 
    running processes. Pressing q will simply exit the command mode.

    Example:- top -v
    Output:-  procps-ng 3.3.17
    Usage:
      top -hv | -bcEeHiOSs1 -d secs -n max -u|U user -p pid(s) -o field -w [cols]

Example:- top <br>
Output:-  <br>

top - 05:01:19 up 14:05,  1 user,  load average: 0.30, 0.27, 0.30 <br>
Tasks: 286 total,   1 running, 285 sleeping,   0 stopped,   0 zombie <br>
%Cpu(s):  4.1 us,  1.9 sy,  0.0 ni, 93.7 id,  0.0 wa,  0.0 hi,  0.3 si,  0.0 st <br>
MiB Mem :   3870.6 total,    322.0 free,   1126.6 used,   2422.1 buff/cache <br>
MiB Swap:   2140.0 total,   2139.5 free,      0.5 used.   2415.9 avail Mem  <br>

PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND  <br>
1719 kamal     20   0 4464628 297848 135508 S   7.2   7.5  25:48.90 gnome-s+  <br>
73906 root      20   0       0      0      0 I   1.6   0.0   0:20.81 kworker+  <br>
75128 kamal     20   0  628328  53580  41272 S   1.6   1.4   0:13.93 gnome-t+  <br>
76369 kamal     20   0   13216   4224   3456 R   1.3   0.1   0:00.54 top       <br>
76251 root      20   0       0      0      0 I   1.0   0.0   0:07.66 kworker+  <br>
749 root      20   0  317440   9212   7676 S   0.7   0.2   8:28.53 vmtoolsd  <br>
2013 kamal     20   0  216988  41260  30124 S   0.7   1.0   6:57.85 vmtoolsd  <br>
27263 systemd+  20   0   14836   6912   6144 S   0.3   0.2   5:07.56 systemd+  <br>
76095 root      20   0       0      0      0 I   0.3   0.0   0:00.42 kworker+  <br>
    1 root      20   0  168004  13312   8320 S   0.0   0.3   1:36.16 systemd   <br>
    2 root      20   0       0      0      0 S   0.0   0.0   0:00.30 kthreadd  <br>
    3 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 rcu_gp    <br>
    4 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 rcu_par+  <br>
    5 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 slub_fl+  <br>
    6 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 netns     <br>
    11 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 mm_perc+  <br>
    12 root      20   0       0      0      0 I   0.0   0.0   0:00.00 rcu_tas+  <br>


- PID: Shows task’s unique process id.
- PR: The process’s priority. The lower the number, the higher the priority.
- VIRT: Total virtual memory used by the task.
- USER: User name of owner of task.
- %CPU: Represents the CPU usage.
- TIME+: CPU Time, the same as ‘TIME’, but reflecting more granularity through hundredths of a second.
- SHR: Represents the Shared Memory size (kb) used by a task.
- NI: Represents a Nice Value of task. A Negative nice value implies higher priority, and positive Nice value means lower priority.
- %MEM: Shows the Memory usage of task.
- RES: How much physical RAM the process is using, measured in kilobytes.
- COMMAND: The name of the command that started the process


**Kill a Process with top** <br>
In the top command, you can kill a process using the k key followed by entering the PID (Process ID) of the process you want to terminate. Here’s how you can do it: <br>

1. Start top by typing top in your terminal. 
2. Locate the process you want to kill using the arrow keys to navigate through the process list.
3. Note down the PID (Process ID) of the process.
4. Press k on your keyboard.
5. Enter the PID of the process you want to kill and press Enter.
6. Confirm the action if prompted.

### kill
    Description:- send a signal to a process.

    Example:- kill 76789 (76789 is PID, which is a process id)
    Output:-  

### nice
    Description:- run a program with modified scheduling priority. nice command in Linux helps in execution of a 
    program/process with modified scheduling priority. It launches a process with a user-defined scheduling priority. In 
    this, if we give a process a higher priority, then Kernel will allocate more CPU time to that process.

    Example:- ps
    Output:-   PID TTY          TIME CMD
              75154 pts/0    00:00:00 bash
              76093 pts/0    00:00:00 ps

1. To check the nice value of a process. 
Example:- ps -el | grep terminal
Output:- 0 S  1000   77289    1540  1  80   0 - 140768 do_pol ?       00:00:05 gnome-terminal-

2. To set the priority of a process.
Example:- nice -10 gnome-terminal
Output:- 

3. To set the negative priority for a process
Example:- nice --10 gnome-terminal
Output:-  

### renice
    Description:- alter priority of running processes. renice command allows you to change and modify the scheduling 
    priority of an already running process.

1. changing priority of the running process.
   Example:- ps -el | grep terminal
   Output:- 0 S  1000   77289    1540  1  80   0 - 140864 do_pol ?       00:00:19 gnome-terminal-

   Example:- renice -n 15 -p 77289
   Output:- 77289 (process ID) old priority 0, new priority 15

   Example:- ps -el | grep terminal
   Outpu:- 0 S  1000   77289    1540  1  95  15 - 140864 do_pol ?       00:00:20 gnome-terminal-

2. To change the priority of all programs of a specific group.
   Example:- sudo renice -n 10 -g 1
   Output:- 1 (process group ID) old priority 15, new priority 10

3. To change the priority of all programs of a specific user. 
   Example:- sudo renice -n 10 -u 0
   Output:- 0 (user ID) old priority -20, new priority 10

### systemctl
    Description:- Control the systemd system and service manager.
Syntax:- systemctl [command] [service] <br>

[command] = The action we want to perform (start, stop, enable, disable, etc.) <br>

[service] = The name of the service we want to perform the action on. <br>

1. Starting and Stopping Services <br>
   Example:- systemctl start sshd (starts SSH service)  <br>
   Output:- <br>
   Example:- systemctl stop sshd <br>

3. Enabling and Disabling Service <br>
   Example:- systemctl enable firewalld <br>
   Output:- <br>
   Exampe:- systemctl disable firewalld <br>

5. Viewing the Staus of Services <br>
   Example:- systemctl status firewalld <br>
   Output:- <br>

6. Restarting and Reloading Services <br>
   Example:- systemctl restart sshd<br>
   Output:-  <br>
   Example:- systemctl reload httpd <br>

7. Masking and Unmasking Services <br>
   Example:- systemctl mask mysqld<br>
   Output:-  <br>
   Example:- systemctl unmask mysqld <br>

8. Changing the Default Target <br>
    Example:- systemctl set-default graphical.target<br>
    Output:-  <br>

9. Listing Unit Files <br>
    Example:- systemctl list-unit-files<br>
    Output:-  <br>

10. Masking and Unmasking Unit Files <br>
    Example:- systemctl mask sshd.service<br>
    Output:-  <br>
    Example:- systemctl unmask sshd.service <br>

### bg

### fg
**----------------------------------------------------------------------------------------------------------------------**

## Disk Space Usage
### df
### du
### free
### fdisk
### findmnt

**----------------------------------------------------------------------------------------------------------------------**
## Other additional Commands
### man
    Description - an interface to the system reference manuals or macros to format man pages.
    
    Example:- man ls
    (present manual interface for respective commands along with use cases).

### whoami
    Description - Print  the  user  name  associated  with the current effective user ID. Same as id -un..
    
    Example:- whoami
    Output:- kamal

### clear
    Description - clear the terminal screen.
    
    Example:- clear
    Output:- 

### history
    Description - GNU History Library.
    
    Example:- history
    Output:- 1934  man whoami
             1935  whoami
             1936  man clear
             1937  clear
             1938  man history 
             1939  history

    then press !1935 (to run whoami command that stored with id 1935 in GNU History library).

### reboot
    Description - Halt, power-off or reboot the machine.
    
    Example - sudo reboot

### shutdown
    Description - Halt, power-off or reboot the machine.
    
    Example - sudo shutdown now

### whatis
    Description - display one-line manual page descriptions.
    
    Example:- wahtis whatis (whatis whoami)
    Output:- 

### date
    Description - print or set the system date and time.
    
    Example:- date
    Output:- Sunday 28 July 2024 05:42:01 AM IST

### time
    Description - run programs and summarize system resource usage.
    
    Example:- time
    Output:- real	0m0.000s
             user	0m0.000s
             sys	0m0.000s

### help
    Description - It helps us to learn about any built-in command.
    
    Example - cd --help

### uname
    Description - print system information.
    
    Example - uname
    Output - Linux

    Example - uname -a or --all (print  all  information)
    Output -  Linux Ubuntu 6.5.0-28-generic #29~22.04.1-Ubuntu SMP PREEMPT_DYNAMIC Thu Apr  4 14:39:20 UTC 2 x86_64 x86_64 
    x86_64 GNU/Linux

    Example - uname -o
    Output - GNU/Linux

    Example - 


### whereis
    Description - locate the binary, source, and manual page files for a command.
    
    Example - whereis mkdir
    Output - mkdir: /usr/bin/mkdir /usr/share/man/man1/mkdir.1.gz

### which
    Description - locate a command.
    
    Example - which mkdir
    Output - /usr/bin/mkdir

### expr
    Description - evaluate expressions.
    
    Example - expr expr 7 + 6
    Output:- 13

### bash --version
    Description - GNU Bourne-Again SHell.
    
    Example - bash --version
    Outpu - bash --version
            GNU bash, version 5.1.16(1)-release (x86_64-pc-linux-gnu)
            Copyright (C) 2020 Free Software Foundation, Inc.
            License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
            
            This is free software; you are free to change and redistribute it.
            There is NO WARRANTY, to the extent permitted by law.

### cal 2024
    Description - cal, ncal — displays a calendar and the date of Easter.
    
    Example - cal
    Output - cal
        July 2024        
        Su Mo Tu We Th Fr Sa  
            1  2  3  4  5  6  
         7  8  9 10 11 12 13  
        14 15 16 17 18 19 20  
        21 22 23 24 25 26 27  
        28 29 30 31 

    Example - cal 09 2024
    Output - al 09 2024
           September 2024     
        Su Mo Tu We Th Fr Sa  
         1  2  3  4  5  6  7  
         8  9 10 11 12 13 14  
        15 16 17 18 19 20 21  
        22 23 24 25 26 27 28  
        29 30               

### echo
    Description - display a line of text.
    
    Example - echo
    Output - echo hello
            hello
    
    Example - echo hello! > tests.txt (> used for overwriting and replacing the existing texts)
    Output  - (it will create a file tests.txt and overwrite hello into that file) 
    echo hello! > tests.txt

    Example - echo hi! >> tests.txt (>> used for appeding at the end of file)
    Output - (it will create a file tests.txt and appends the test "hi!" into that file) 
    echo hi! > tests.txt

### bc
    Description - An arbitrary precision calculator language.
    
    Example - bc
    Output - bc
        bc 1.07.1
        Copyright 1991-1994, 1997, 1998, 2000, 2004, 2006, 2008, 2012-2017 Free Software Foundation, Inc.
        This is free software with ABSOLUTELY NO WARRANTY.
        For details type `warranty'. 
        5 + 6 (you have to enter the expression and it shows the result)
        11
        8 % 3 (give you remainder of given expression)
        2


### info echo
    Description - It reads documentation in the info format. It will give detailed information for a command when compared 
    with the man page. The pages are made using the texinfo tools because of which it can link with other pages, create 
    menus and easy navigation.
    
    Syntax - info [OPTION]... [MENU-ITEM...]
    Example - info dir
    Output -

![Screenshot (384)](https://github.com/user-attachments/assets/24147b7b-d257-486a-8266-cb841a5a8662)

    
    Example - info ls
    Output -

![Screenshot (385)](https://github.com/user-attachments/assets/4f62b5d4-db1a-456f-a369-311754a1a7da)

### ln
     Description - make links between files.

     hardlinks - Hard links in Linux are essentially additional names for an existing file on the filesystem.
     Unlike soft links, hard links are indistinguishable from the file they link to because they are direct references to 
     the inode (the data structure that stores file metadata, including its contents). Creating a hard link to a file does 
     not use additional disk space for the contents of the file. When the original file is deleted, the data remains 
     accessible through any of its hard links until all references (links) to the file are deleted.
     
     Example - ln k1.txt hardlinksexamples
     Output - 

     softlinks - Soft links, also known as symbolic links or symlinks, act as shortcuts(similar to Windows OS) or 
     references to files and directories in Linux. Unlike hard links, soft links are not direct mirrors of the target 
     files. Instead, they point to a specific path in the filesystem where the target files or directories reside. If the 
     target file is moved or deleted, the soft link becomes a ‘dangling’ link, pointing to a non-existent file, which 
     results in errors when accessed.
     
     Example - ln -s k1.txt softlinksexamples
     Output - 

     1180913 -rw-rw-r-- 2 kamal kamal   56 Jul 15 05:01 hardlinksexamples
     1180913 -rw-rw-r-- 2 kamal kamal   56 Jul 15 05:01 k1.txt
     1185130 drwxrwxr-x 2 kamal kamal 4096 Jul 30 19:47 kam2
     1186954 -rw-rw-r-- 2 kamal kamal 9078 Jul 12 04:40 linux_commands
     1186954 -rw-rw-r-- 2 kamal kamal 9078 Jul 12 04:40 linux_hardlinks
     1186958 lrwxrwxrwx 1 kamal kamal   14 Feb 25 09:07 linux_softlinks -> linux_commands
     1185159 lrwxrwxrwx 1 kamal kamal    6 Jul 30 19:44 softlinksexamples -> k1.txt
     1185132 -rw-rw-r-- 1 kamal kamal 2190 Jul 14 04:55 zipfile.zip

![Screenshot (382)](https://github.com/user-attachments/assets/90ffab28-5438-4811-af29-0c28b6305ef1)

![Screenshot (383)](https://github.com/user-attachments/assets/738f354f-d860-4252-9118-adf40d7a1d40)

### directory loop using symbolic(softlink) link
    Description - to create a directory loop using symbolic link. First, make directory a/ then within a/ create another 
    directoy b/ and within b/ we'll make symbolic link of directory b/ named it c(symbolic or shortuts of b). Thus, 
    Looping will be created.
    
    Example - ln -s .. c (type this command on Terminal after going inside b/)

![Screenshot (408)](https://github.com/user-attachments/assets/325d8c8a-a5ca-4b96-ac08-0f9bc59c0496)

![Screenshot (409)](https://github.com/user-attachments/assets/e75cecda-2a91-4d16-bdff-394b55a43b6f)


### type pwd
    Description - The ‘type’ command in Linux is a built-in shell command used to identify the kind of command you are dealing with.
    It helps you determine whether a command is an alias, a shell built-in, a file, or a function.

    Syntax - type [Options] command names
    
    Options:
    -a : This option is used to find out whether it is an alias, keyword or a function and it also displays the path of an executable, if available.
    
    Example - type -a ls
    Output - 

![Screenshot (399)](https://github.com/user-attachments/assets/c4901692-a6e3-497f-8f1d-64cc4191f4a2)


    -t : This option will display a single word as an output.
    alias – if command is a shell alias
    keyword – if command is a shell reserved word
    builtin – if command is a shell builtin
    function – if command is a shell function
    file – if command is a disk file

    Example - type -t pwd
              type -t cp
              type -t ls
              type -t while

    Output -

![Screenshot (397)](https://github.com/user-attachments/assets/b732abe0-cba0-44ab-afee-6d55dea65fb8)

    -p : This option displays the name of the disk file which would be executed by the shell. It will return nothing if the command is not a disk file.

    Example- type -p dash
             type -p pwd

    Output - 

![Screenshot (401)](https://github.com/user-attachments/assets/75637b15-a2bb-4bb9-85b6-60757495f43b)

### wildcards
    Description - Given a text and a wildcard pattern, implement  wildcard pattern matching algorithm that finds if 
    wildcard pattern is matched with text. The matching should cover the entire text (not partial text).
    The wildcard pattern can include the characters ‘?’ and ‘*’. 

    * – This wildcard represents all the characters
    ? – This wildcard represents a single character
    [] – This wildcard represents a range of characters.

    Example - ls ?.txt
    Example - ls *.txt

![Screenshot (402)](https://github.com/user-attachments/assets/7e256759-2570-470a-abac-08bd6461890e)

    Example - ls he*
    Example - ls he*?o

![Screenshot (403)](https://github.com/user-attachments/assets/23a0cac4-d5bd-4ccf-919b-d264eee2de35)

    Example - ls [kam]*.txt
    Example - ls [kam]*.???

![Screenshot (404)](https://github.com/user-attachments/assets/c7c72247-d14a-46f4-bef3-7aa5abc2e81d)

    Example - ls [!kam]*.txt or ls [^kam]*.txt
    Example - ls [[:upper:]]*.txt
    Example - ls [[:lower:]]*.txt
    Example - ls [0-9]*.txt
    Example - ls *[0-9]*.txt
    Example - ls *[0-9].txt
    Example - ls *[[:digit:]]
    Example - ls *[[:digit:]].txt

![Screenshot (405)](https://github.com/user-attachments/assets/b700b50d-e8b0-4b1a-867f-e094723179f7)

![Screenshot (406)](https://github.com/user-attachments/assets/3902228b-cd43-4976-a9c7-2577f1956f4a)

    Example - ls *[[:alpha:]]
    Example - ls *[[:alpha:]].txt
    Example - ls [[:alpha:]]*.txt
    Example - ls [[:alnum:]]*.txt
    Example - ls [[:digit:]]*[[:alpha:]].txt

![Screenshot (407)](https://github.com/user-attachments/assets/ad61cd55-d25f-4619-8cb4-ecfff9cd21ec)

### alias
    Description - before making your own command just check whether it is shell builtin or not, if it's builtin then we 
    can't make aliases. 

    You can create your alias command in terminal. However, after existing terminal session is closed then you cannot use 
    it.
    
    alias copy="cp" 
    unalias copy

    cd ~(Home directory)
    then type ls -a
    next gedit .bashrc (to open it in text editor)
    then paste your alias command and save it for indefinite time.
    NOTE:- it is not recommended, so after making own alias command for learning purpose then delete it from (.bashrc 
    file). 

![Screenshot (395)](https://github.com/user-attachments/assets/0e1e9cae-50df-41ef-ba9e-56243e9f7c07)

![Screenshot (396)](https://github.com/user-attachments/assets/fa37918e-4444-4ae4-bd15-0ff52ae89ab9)

![Screenshot (391)](https://github.com/user-attachments/assets/e662d334-f254-4d3d-8448-c071c38e2023)

![Screenshot (392)](https://github.com/user-attachments/assets/8df71317-2261-4184-a1e3-6e47ad0b2851)

![Screenshot (388)](https://github.com/user-attachments/assets/0b79b314-d359-4e25-90c5-6529d83627b0)

![Screenshot (389)](https://github.com/user-attachments/assets/44d098d0-e527-4b1c-aed0-f4ab36538ea4)

![Screenshot (390)](https://github.com/user-attachments/assets/9f437df5-7c75-4d3f-86c2-36252593f742)

![Screenshot (393)](https://github.com/user-attachments/assets/65b3f95b-3abf-42bb-84a5-314167bcabf4)

### absolute VS realtive path
    absolute path - An absolute path specifies the location of a file or directory from the root directory (/).
    It always starts with a /, indicating the root directory, and provides the full path to the file or directory.

![Screenshot (386)](https://github.com/user-attachments/assets/efa59b5a-ebbc-47f6-a6c5-a97263c8d363)

    
    relative path - A relative path specifies the location of a file or directory in relation to the current working 
    directory. It does not start with a /.
    Instead, it starts from the current directory or a directory relative to the current one.

    .(a single dot) - this represents the current directory.
    ..(two dots) - this represents the parent directory. 

![Screenshot (387)](https://github.com/user-attachments/assets/977e2098-b225-4764-9910-b5b36ba58afd)
