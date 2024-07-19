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
    Description:- create a new group.
    
    Example:- host google.com
    Output:- google.com has address 142.251.36.238
            google.com has IPv6 address 2a00:1450:4016:80a::200e
            google.com mail is handled by 10 smtp.google.com.

### groupdel
    Description:- delete a group.
    
    Example:- host google.com
    Output:- google.com has address 142.251.36.238
            google.com has IPv6 address 2a00:1450:4016:80a::200e
            google.com mail is handled by 10 smtp.google.com.

### groupmod
    Description:- modify a group definition on the system.
    
    Example:- host google.com
    Output:- google.com has address 142.251.36.238
            google.com has IPv6 address 2a00:1450:4016:80a::200e
            google.com mail is handled by 10 smtp.google.com.




**--------------------------------------------------------------------------------------------------------------------**
## Permission & ownership
### chmod
### chown
### chgrp


**--------------------------------------------------------------------------------------------------------------------**
## Process Management
### ps
### top
### kill
### nice
### systemctl
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
    
    Example - man ls
    (present manual interface for respective commands along with use cases).
### whoami
### clear
### history [!12]
### reboot
### shutdown
### whatis
### date
### time
### help
### uname
### whereis
### which
### hostname
### host google.com
### expr
### bash --version
### cal 2024
### echo > and >>
### ping google.com
### bc
### info echo
### ln test1.txt testhardlinks
### ln -s test1.txt softlinks
### directory loop
### type pwd
### wildcards
### alias
### absolute VS realtive path
### chmod

