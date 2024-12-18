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
![Screenshot (437)](https://github.com/user-attachments/assets/82b5f554-69fb-4b42-a4d5-9ad92e2610e1)


> [!NOTE]
> **Flags** are used to modify the behavior of a command. For example ls -a, -a tells the ls executable to list all files in the directoy, including hidden ones. Flags are also called **OPTIONS**.
 
### cd
     Description:- change directory or file
     
     Example:- cd Desktop/, cd, cd ..
     Output: goes to Desktop directory or folder.
 
 ![Screenshot (438)](https://github.com/user-attachments/assets/fb9550fc-0c9a-496d-8920-bac502521711)

### dir
     Description:- list directory contents
     
     Example:- dir
     Output:- Desktop  Documents  Downloads  Music  Pictures	Public	snap  Templates  Videos
 
 ![Screenshot (439)](https://github.com/user-attachments/assets/eef216c8-b802-47b0-b7b7-f0ff0bf42071)

### pwd
     Description:- print name of current/working directory
     
     Example:- pwd
     Output:- /home/kamal/Desktop
 
 ![Screenshot (440)](https://github.com/user-attachments/assets/872f0209-553b-4bf6-bf2a-a8715219502a)

### mkdir
     Description:- make directories
     
     Example:- mkdir examples/
     Output:- Desktop    Downloads  Music     Public  Templates Documents  examples   Pictures  snap    Videos

![Screenshot (441)](https://github.com/user-attachments/assets/cb7c1ed6-ac90-433f-8d0a-71ba22416319)

 ### rmdir
     Description:- remove empty directories
     
     Example:- rmdir examples/ or rm -d examples/
     Output:- Desktop    Downloads  Music     Public  Templates Documents Pictures  snap    Videos
 
![Screenshot (442)](https://github.com/user-attachments/assets/a7c308ae-9f1a-459f-bd38-0e0c60bec9f4)

![Screenshot (447)](https://github.com/user-attachments/assets/04adfa43-4d94-475e-825b-e50177c821e4)

 ### rm
     Description:- remove files or directories
     
     Example:- rm password.txt(removes file) or rm -ir(remove non-empty directories)
     Output:- Desktop    Downloads  Music     Public  Templates Documents Pictures  snap    Videos
 
![Screenshot (443)](https://github.com/user-attachments/assets/78812ba3-162c-43cd-9622-77dca15ee975)

![Screenshot (446)](https://github.com/user-attachments/assets/f695ec34-174d-4ae2-8803-5fd9795a462e)

 ### cp
     Description:- copy files and directories
     
     Example:- cp password.txt security/ or cp -r kam/ kam2/ 
     Output:- 

![Screenshot (444)](https://github.com/user-attachments/assets/8a0f5a74-450a-4612-b1e1-facedb137155)

![Screenshot (448)](https://github.com/user-attachments/assets/c72e7e09-d232-480a-bfbb-d88ff5c70cae)

> [!NOTE]
> Use flags such as -R -r(recursively copies files or folder inside the directory) while copying directories to another. 
     
 ### mv
     Description:- move (rename) files or directories
     
     Example:- mv k1.txt kam2/ (moving files k1.txt to directory kam2/)
     Example:- mv kam.txt k1.txt (renaming file kam.txt to k1.txt)
     Example:- mv kam/ kam2/ (renaming directory kam/ to kam2/)
     Example:- mv kam/ kam3/ (moving directory kam/ to kam3/)
     Output:-
![Screenshot (449)](https://github.com/user-attachments/assets/a1ef34c6-afe2-471f-b631-e5adb1fad9ed)

![Screenshot (450)](https://github.com/user-attachments/assets/111a3f94-ef4e-40e7-a8d6-11fd430b9d73)

![Screenshot (451)](https://github.com/user-attachments/assets/42f17fab-c8f8-48fe-b90d-0285236205a5)

![Screenshot (452)](https://github.com/user-attachments/assets/6f0446b4-aeea-46e4-8cf3-6f67508be58e)


 ### touch
     Description:- change file timestamps (create files with empty contents)
     
     Example:- touch hello.txt
     Output:- 

 ![Screenshot (453)](https://github.com/user-attachments/assets/0659e2a1-c448-4751-90e9-32462c77b702)

 ### nano
     Description:- open files in nano text-editors
     
     Example:- nano hello.txt
     Output:- 

![Screenshot (454)](https://github.com/user-attachments/assets/9cfeb347-3c58-46d9-b66e-631cb94d40ab)

 ### gedit
     Description:- open files in gedit text-editors
     
     Example:- gedit hello.txt
     Output:- 

![Screenshot (455)](https://github.com/user-attachments/assets/4cfe0abb-3c74-4141-9349-f5292a2243d2)

 ### cat
     Description:- concatenate files and print on the standard output (to view contents of file)
     
     Example:- cat hello.txt
     Output:-  This is your right time to
               follow your passion.

![Screenshot (456)](https://github.com/user-attachments/assets/9f83a098-bb9c-47e8-a45d-327313b998b8)

 ### tac
     Description:- concatenate and print files in reverse 
     
     Example:- tac hello.txt
     Output:-  follow your passion.
               This is your right time to

![Screenshot (463)](https://github.com/user-attachments/assets/fbe147ca-65fb-4468-a63b-65ab6b78e7a3)

 ### grep
    Description:- print lines that match patterns
    
    Example:- grep "time" k1.txt
    Output:-  This is your right **time**.
              **time** and tide wait for none.

![Screenshot (464)](https://github.com/user-attachments/assets/f0e57f65-f106-41ec-904c-cca4d5c08d37)

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

![Screenshot (509)](https://github.com/user-attachments/assets/c9b4c315-30ec-453c-878c-e5ceb2fd284e)
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

     Example:- diff a.txt b.txt
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

![Screenshot (510)](https://github.com/user-attachments/assets/0f4fd49f-e85c-4824-afac-a6783285262d)
![Screenshot (511)](https://github.com/user-attachments/assets/6892f67c-846c-4682-a588-6c362173fd93)

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
     one page (one screen) at a time. It has faster access because if a file is large, it doesn’t access the complete 
     file, 
     but accesses it page by page. 

     For example, if it’s a large file and you are reading it using any text editor, then the complete file will be loaded 
     to the main memory. The less command doesn’t load the entire file but loads it part by part which makes it faster. 

     1. both forward and backward navigation and also has search options. You can go to the beginning and the end of a file instantly.
     Plus you can switch to an editor (like open the file in vi or vim). It is noticeably quicker than editor for when the file is large.
    
     Syntax:- less [options/flags] filename
     Example:- less hundreds.txt
     Example:- less -p 0 hundreds.txt (p flag used for patterns i.e. highlights the text where 0 is available)

![Screenshot (589)](https://github.com/user-attachments/assets/50ca08c6-e00d-4744-bdea-c0d7bc81c401)
![Screenshot (590)](https://github.com/user-attachments/assets/38b396da-e589-421d-9155-70a4d3e8266c)
![Screenshot (592)](https://github.com/user-attachments/assets/1b0dc430-cff0-4e1a-a572-e9774bd3ccbb)
![Screenshot (593)](https://github.com/user-attachments/assets/0b02b6b9-3e27-45a0-9652-c4ac7ae7a2bc)
![Screenshot (594)](https://github.com/user-attachments/assets/7e2db391-445f-4a52-8f83-7cc28b909839)
![Screenshot (595)](https://github.com/user-attachments/assets/373246fd-89fc-4006-b9d6-d852a04ac2e8)

 
 ### more
     Description:- file perusal filter for crt viewing. more command is used to view the text files in the command prompt, 
     displaying one screen at a time in case the file is large (For example log files). The more command also allows the 
     user do scroll up and down through the page. The syntax along with options and command is as follows. Another 
     application of more is to use it with some other command after a pipe. When the output is large, we can use more 
     command to see output one by one.

     1. forward navigation and limited backward navigation.

     
     Syntax:- more [options/flags] filename
     Example:- more -d hundreds.txt
     (-d flag is 'Prompt Navigation Help')
     Use this command in order to help the user to navigate.
     It displays “[Press space to continue, ‘q’ to quit.]” and,
     Displays “[Press ‘h’ for instructions.]” when wrong key is pressed.

![Screenshot (585)](https://github.com/user-attachments/assets/03c18103-e022-4659-ad27-4746e373ba3a)
![Screenshot (586)](https://github.com/user-attachments/assets/a3ef710f-fc56-4de8-ad60-3405f42beac8)
![Screenshot (587)](https://github.com/user-attachments/assets/2f1be798-d7ca-4f12-8bd0-10132eb75589)
![Screenshot (588)](https://github.com/user-attachments/assets/37dc2b74-1b49-41c3-8c79-14b1a89d5bcb)

     

### most
    Description:- most has all the features of more and less but you can also open multiple files, close 1 file at a time when
    you have multiple files open, allows locking and scrolling of the open windows and allows for splitting of open windows.

 
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

![Screenshot (512)](https://github.com/user-attachments/assets/b24174c9-54be-4d50-afe9-0d30032828dd)
![Screenshot (513)](https://github.com/user-attachments/assets/7d963aa4-80b8-49ff-875d-534a915b9715)

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

![Screenshot (514)](https://github.com/user-attachments/assets/cdde3734-6431-4b7c-bd69-f66449296a06)
![Screenshot (515)](https://github.com/user-attachments/assets/8dd189ba-19ae-4107-acf9-32aaf4d4f2e3)

> [!NOTE]
> By default tail print the last 10 lines of each FILE to standard output.

 ### find
     Description:- search for files in a directory hierarchy
     
     Example:- find *.txt 
     Example:- find k?.txt ('?' represents exactly one character )
     Example:- find kam*.txt ('*' represents any number of character)
     Output:-
![Screenshot (516)](https://github.com/user-attachments/assets/98774670-4983-457b-bb66-834153a963bd)
![Screenshot (517)](https://github.com/user-attachments/assets/79032fb1-ece3-4041-8583-875676414621)
![Screenshot (518)](https://github.com/user-attachments/assets/b111b03f-3ae0-47ce-b997-e8975f4f08ea)

 ### file
     Description:- determine file type
     
     Example:- file k1.txt
     Output:- k1.txt: ASCII text
![Screenshot (519)](https://github.com/user-attachments/assets/c0130d22-6fa6-40d0-85d2-944fb2aef193)

 ### wc
    Description:- print newline, word, and byte counts for each file
    
    Example:- wc k1.txt
    Output:- 2  9 48 k1.txt (lines, words, characters)

![Screenshot 51](https://github.com/user-attachments/assets/5b8632ef-8059-454b-b548-e429b8aeb0f4)
> [!NOTE]
> -c(bytes count),-m(characters count),-l(newlines count ),-L, -w(words count)

 ### zip
     Description:- package and compress (archive) files

     Syntax :- zip [options] [file_name.zip] [files_names]
     Syntax :- zip [file_name.zip] [file_name] [for creating zip file]
     
     Example :- zip zipfile.zip k1.txt thousands.txt (it zips the files k1.txt and thousands.txt into zipfile.zip)
     Output :-  adding: k1.txt (deflated 8%)
               adding: thousands.txt (deflated 53%)

![Screenshot (539)](https://github.com/user-attachments/assets/13b67e71-c6df-422f-8533-cc663fc9d797)

 ### unzip
     Description:- list, test and extract compressed files in a ZIP archive
     
     Syntax:- unzip [file_name.zip]
     Example:- unzip zipfile.zip (extraction of zipfile.zip)
     Output:-  Archive:  zipfile.zip
               inflating: k1.txt                  
               inflating: thousands.txt
    
    Syntax:- unzip [file_name] -d [path_to_destination_directory_with_name]
    Example:- unzip zipfile.zip -d ~/Desktop/extracted/ (extraction of zipfile.zip to destination folder)
    Archive:-  zipfile.zip
              inflating: /home/kamal/Desktop/extracted/k1.txt  
              inflating: /home/kamal/Desktop/extracted/thousands.txt

![Screenshot (540](https://github.com/user-attachments/assets/e5a2344d-bc01-48dc-9975-f99ab1b65599)
![Screenshot (540)](https://github.com/user-attachments/assets/4c2d6b80-88d6-43d2-b5a5-aa6acdef75da)


 
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

    Syntax - ifconfig [options] [interface] (interface can be 'eth0, wlan0')
    Example - ifconfig [shows information on all network interfaces]
    Output - 

![Screenshot (620)](https://github.com/user-attachments/assets/4fb9eece-4f08-4082-ab3b-942366747aa4)

 
 ### route
    Description:- show / manipulate the IP routing table
    
    Example:- route (It displays the IP/kernel routing table.)
    Output:- Kernel IP routing table
             Destination     Gateway         Genmask         Flags Metric Ref    Use Iface
             default         192.168.124.2   0.0.0.0         UG    100    0        0 eth0
             192.168.124.0   0.0.0.0         255.255.255.0   U     100    0        0 eth0)

![Screenshot (621)](https://github.com/user-attachments/assets/0a8b7229-99ce-45dd-8d0b-821fdeb1075c)


 ### netstat
    Description:- Print network connections, routing tables, interface statis‐tics, masquerade connections, and multicast 
    memberships
    
    Syntax:- netstat [options]
    Example:- nestat -aut (all ports of TCP and UDP)
    Output:- Active Internet connections (servers and established)
             Proto Recv-Q Send-Q Local Address           Foreign Address         State      
             udp        0      0 192.168.124.128:bootpc  192.168.124.254:bootps  ESTABLISHED
![Screenshot (625)](https://github.com/user-attachments/assets/8bf4e32e-5dd5-49a8-8302-5505baca50c0)

 
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

![Screenshot (626)](https://github.com/user-attachments/assets/4befe18a-f192-4efe-815d-d7e7959f821b)

 
 ### ping
    Description:- send ICMP ECHO_REQUEST to network hosts
    
    Example:- ping google.com
    Output:- PING google.com (142.251.36.238) 56(84) bytes of data.
            64 bytes from muc11s22-in-f14.1e100.net (142.251.36.238): icmp_seq=1 ttl=128 time=63.6 ms
            64 bytes from muc11s22-in-f14.1e100.net (142.251.36.238): icmp_seq=2 ttl=128 time=58.9 ms
            64 bytes from muc11s22-in-f14.1e100.net (142.251.36.238): icmp_seq=3 ttl=128 time=53.7 ms
            64 bytes from muc11s22-in-f14.1e100.net (142.251.36.238): icmp_seq=4 ttl=128 time=51.0 ms
            64 bytes from muc11s22-in-f14.1e100.net (142.251.36.238): icmp_seq=5 ttl=128 time=50.2 ms

![Screenshot (635)](https://github.com/user-attachments/assets/7c6504d3-ca1d-4d5a-8080-c54136e2273c)
![Screenshot (636)](https://github.com/user-attachments/assets/7eb0b11e-3ebb-4f50-bd7f-69598ef68077)

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
![Screenshot (637)](https://github.com/user-attachments/assets/aaa784b4-96cd-47f2-87c4-880498f6aef3)

 
 ### host
    Description:- DNS lookup utility.
    
    Example:- host google.com
    Output:- google.com has address 142.251.36.238
            google.com has IPv6 address 2a00:1450:4016:80a::200e
            google.com mail is handled by 10 smtp.google.com.
![Screenshot (638)](https://github.com/user-attachments/assets/ae37d8ff-32d7-4290-8a03-d8edfd34deb1)

 
 ### hostname
    Description:- show or set the system's host name
    
    Example:- hostname
    Output:- Ubuntu

![Screenshot (639)](https://github.com/user-attachments/assets/74446c37-f0f0-4cf9-aaca-1a1e8f87b79d)

**--------------------------------------------------------------------------------------------------------------------**

## User & Group
### users
    Description:- print the user names of users currently logged in to the current host.
    
    Example:- users
    Output:- kamal
![Screenshot (640)](https://github.com/user-attachments/assets/f1800dda-6ce8-4368-917b-95beee1dfa40)


### useradd
    Description:- useradd - create a new user or update default new user information.

    It makes changes to the following files:

    /etc/passwd
    /etc/shadow
    /etc/group
    /etc/gshadow
    creates a directory for new user in /home
    
    Example:- sudo useradd sachin
    Output:- [sudo] password for kamal: 

![Screenshot (643)](https://github.com/user-attachments/assets/08d5f321-a9a0-4552-bac7-d4403a7168eb)


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

![Screenshot (644)](https://github.com/user-attachments/assets/e96b3a26-8030-4abf-b6e5-a740f2c384a2)
![Screenshot (645)](https://github.com/user-attachments/assets/1a3eb427-8a6c-49b2-ae6e-246842caf3ea)
![Screenshot (646)](https://github.com/user-attachments/assets/659cd8c7-6435-482b-aff3-422d1544b151)


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
![Screenshot (641)](https://github.com/user-attachments/assets/4b7167ba-fab3-4d30-bad0-f3a60fb9405c)

![Screenshot (642)](https://github.com/user-attachments/assets/9d29e215-87f5-4b95-a144-677732e24fdd)


### usermod
    Description:- modify a user account. usermod command or modify user is a command in Linux that is used to change the 
    properties of a user in Linux through the command line. After creating a user we have to sometimes change their 
    attributes like login name, adding to the groups, changing user home directory, password or login directory etc.
    
    Example:- sudo usermod -c "This is a comment examples of a usermode for sachin user" sachin (modifies user sachin by 
    adding comments )

    Example:- sudo cat /etc/passwd | grep sachin
    Output:- sachin:x:1001:1001:This is a comment examples of a usermode for sachin user:/home/sachin:/bin/sh

![Screenshot (647)](https://github.com/user-attachments/assets/7390205d-aa37-498e-a156-9b7a733ad68c)


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

![Screenshot (648)](https://github.com/user-attachments/assets/bd7e2f8d-db59-4f4f-a641-9eefecb96176)


### groupadd
    Description:- create a new group. A group is a collection of users with similar permissions or access levels. Groups 
    make it easier to manage and assign permissions to multiple users at once, enhancing security and simplifying 
    administrative tasks.
    
    Example:- sudo groupadd cybersecurity
    Output:- password for kamal: 

    Example:- sudo tail /etc/group
    Output:-
![Screenshot (649)](https://github.com/user-attachments/assets/8cf5e480-9681-4ab0-baf3-eaf9e039c5df)

### groupdel
    Description:- delete a group.
    
    Example:- sudo groupdel cyberforensic
    Output:- 

    Example:- sudo tail /etc/group
    Output:-

![Screenshot (651)](https://github.com/user-attachments/assets/0bb78a89-ce54-4910-bc3a-54d27a8ec091)


### groupmod
    Description:- modify a group definition on the system.
    
    Example:- sudo groupmod -n socteam cybersecurity
    Output:- 

    Example:- sudo tail /etc/group
    Output:- 

![Screenshot (650)](https://github.com/user-attachments/assets/46cb9e3e-8c1a-45c9-8f11-0134762d7559)


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

**Permissiion(before chmod) :-** rw-rw-r-- 1 kamal kamal 54 Aug  9 17:37 a.txt <br>
**Ex:-** chmod u+rwx a.txt <br>
**output:-** -rwxrw-r-- 1 kamal kamal   54 Aug  9 17:37 a.txt <br>
![Screenshot (661)](https://github.com/user-attachments/assets/d42f6452-6027-4642-a628-0a39c1921e05)
![Screenshot (662)](https://github.com/user-attachments/assets/b7eaad6f-910e-4759-aa20-68a84db605a1)


Remove write permission for the group and others: <br>
**Permissiion(before chmod) :-** -rwxrw-r-- 1 kamal kamal   54 Aug  9 17:37 a.txt <br>
**Ex:-** chmod go-w a.txt <br>
**output:-** -rwxr--r-- 1 kamal kamal   54 Aug  9 17:37 a.txt <br>
![Screenshot (663)](https://github.com/user-attachments/assets/26dd6698-747e-4767-a8ea-fdf50b4434e5)


Read and write for Owner, and Read-only for the group and other: <br>
**Permissiion(before chmod) :-** -rwxr--r-- 1 kamal kamal   54 Aug  9 17:37 a.txt <br>
**Ex:-** chmod u+rw,go+r a.txt <br>
**output:-** -rwxr--r-- 1  kamal kamal   54 Aug  9 17:37 a.txt <br>
![Screenshot (664)](https://github.com/user-attachments/assets/56661716-63d5-4432-92ac-cb2fa5137579)


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
 
**Permissiion(before chmod) :-** -r--r--r-- 1 kamal kamal   54 Aug  9 17:37 a.txt <br>

  Example:-  chmod 674 a.txt <br>
  Output:-  -rw-rwxr-- 1 kamal kamal  54 Aug  9 17:37 a.txt <br>
![Screenshot (665)](https://github.com/user-attachments/assets/b17d296c-d5fd-4d3a-9627-c77a3d7ebeaf)
![Screenshot (666)](https://github.com/user-attachments/assets/e21701d7-81ff-41ed-a357-39fea27af408)

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

**ownership(before chown) :-** -rw-rwxr-- 1 kamal kamal   54 Aug  9 17:37 a.txt <br>

To Change the owner of a file in Linux <br>
Syntax:- chown owner_name  file_name <br>
Example:- sudo chown sachin a.txt <br>
Output:-  -rw-rwxr-- 1 sachin kamal   54 Aug  9 17:37 a.txt <br>

![Screenshot (665)](https://github.com/user-attachments/assets/82e12360-3cb5-4ad1-bace-1926f21a7967)
![Screenshot (667)](https://github.com/user-attachments/assets/fe8df4d0-7959-4f51-ac32-01837b202223)

To change the group ownership of a file <br>
Syntax:- chown :group_name file_name <br>
Example:- sudo chown :sachin b.txt<br>
Output:-  -rw-rwxr-- 1  kamal  sachin 54 Aug  9 17:37 b.txt <br>

![Screenshot (668)](https://github.com/user-attachments/assets/b3e27cfd-5c14-447d-8a8d-31df7585c4f7)
![Screenshot (669)](https://github.com/user-attachments/assets/c6743ca2-6114-48f5-9f82-4a9efccec98b)

to Change Owner and Group of the File simultaneously <br>
Syntax:- chown owner_name:group_name file1.txt <br>
Example:- sudo chown sachin:sachin b.txt <br>
![Screenshot (668)](https://github.com/user-attachments/assets/43f5cf85-68c2-41d5-a282-5663ad3ca4db)

![Screenshot (670)](https://github.com/user-attachments/assets/92f6e03f-bb79-4404-9dfa-ceafa5060ebc)

### chgrp
    Description:- change group ownership. The `chgrp` command in Linux is used to change the group ownership of a file or 
    directory. All files in Linux belong to an owner and a group. You can set the owner by using “chown” command, and the 
    group by the “chgrp” command.
    
**Group(before chgrp) :-**-rw-rwxr-- 1 sachin kamal   54 Aug  9 17:37 a.txt <br>

Example:- sudo chgrp sachin a.txt <br>
Output:- -rw-rwxr-- 1 sachin sachin  54 Aug  9 17:37 a.txtt <br>

![Screenshot (671)](https://github.com/user-attachments/assets/cb885fe2-a420-4198-ae4e-f432d013d11b)
![Screenshot (672)](https://github.com/user-attachments/assets/123c8fe9-91fa-407c-afc5-6deaec1fa82b)

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

![Screenshot (652)](https://github.com/user-attachments/assets/c1a18c2d-f1f8-4b01-aca7-8dfa45f11a2c)

![Screenshot (653)](https://github.com/user-attachments/assets/a5ef693d-8085-4dfb-bbb8-7f257ed2a3c4)




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

![Screenshot (656)](https://github.com/user-attachments/assets/73818a1f-42b5-4fb3-a6bb-a671c01e505f)


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

![Screenshot (654)](https://github.com/user-attachments/assets/1580e0e8-b33a-41c0-817d-83accc43d3f3)

![Screenshot (655)](https://github.com/user-attachments/assets/4b83e729-365f-4e5a-9af3-8cb6861a24eb)


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
In the top command, you can kill a process using the "k" key followed by entering the PID (Process ID) of the process you want to terminate. Here’s how you can do it: <br>

1. Start top by typing top in your terminal. 
2. Locate the process you want to kill using the arrow keys to navigate through the process list.
3. Note down the PID (Process ID) of the process.
4. Press k on your keyboard.
5. Enter the PID of the process you want to kill and press Enter.
6. Confirm the action if prompted.

![Screenshot (676)](https://github.com/user-attachments/assets/4325e141-a735-45cf-bb3a-42992098dcdc)
![Screenshot (677)](https://github.com/user-attachments/assets/8fc6725c-69b1-4a42-b086-5498eeae1392)
![Screenshot (678)](https://github.com/user-attachments/assets/4183b138-5285-4bce-b0af-cd12d1c858c0)


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

![Screenshot (657)](https://github.com/user-attachments/assets/af1d9458-0bfd-4645-a8c0-d56aaba10f82)


1. To check the nice value of a process. <br>
Example:- ps -el | grep terminal <br>
Output:- 0 S  1000   77289    1540  1  80   0 - 140768 do_pol ?       00:00:05 gnome-terminal- <br>

2. To set the priority of a process. <br>
Example:- nice -10 gnome-terminal <br>
Output:- <br>

3. To set the negative priority for a process <br>
Example:- nice --10 gnome-terminal <br>
Output:-  <br>
![Screenshot (658)](https://github.com/user-attachments/assets/10684e37-0796-4d02-887c-5d04c5c345e9)
![Screenshot (659)](https://github.com/user-attachments/assets/114de81d-ed53-41da-85a0-d393767372b3)
![Screenshot (660)](https://github.com/user-attachments/assets/902aff66-b3b6-4b0f-bcd8-a8b8c1dc98d7)

### renice
    Description:- alter priority of running processes. renice command allows you to change and modify the scheduling 
    priority of an already running process.

1. changing priority of the running process. <br>
   Example:- ps -el | grep terminal <br>
   Output:- 0 S  1000    2626    1555  0  80   0 - 139132 do_pol ?       00:00:02 gnome-terminal- <br>
   2626 (is a process id)
    
   Example:- renice -n 15 -p 2626 <br>
   Output:- 77289 (process ID) old priority 0, new priority 15 <br>

   Example:- ps -el | grep terminal <br>
   Output:- 0 S  1000    2626    1555  0  95  15 - 139132 do_pol ?       00:00:03 gnome-terminal- <br>

![Screenshot (679)](https://github.com/user-attachments/assets/b5cdcc69-c558-4c94-a5c6-bd402e513cbc)


2. To change the priority of all programs of a specific group. <br>
   Example:- sudo renice -n 10 -g 1 <br>
   Output:- 1 (process group ID) old priority 15, new priority 10 <br>
![Screenshot (680)](https://github.com/user-attachments/assets/5d6ffba8-2281-4bac-b74f-05763bb543ca)

3. To change the priority of all programs of a specific user. <br>
   Example:- sudo renice -n 10 -u 0 <br>
   Output:- 0 (user ID) old priority -20, new priority 10 <br>
![Screenshot (681)](https://github.com/user-attachments/assets/76919d9c-d90f-4f17-8063-a355be3b6d99)

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

![Screenshot (410)](https://github.com/user-attachments/assets/dcb669c8-c248-42ba-b9f6-6c31cdd1312e)


### whoami
    Description - Print  the  user  name  associated  with the current effective user ID. Same as id -un..
    
    Example:- whoami
    Output:- kamal

![Screenshot (411)](https://github.com/user-attachments/assets/8e31a8f4-ec1f-42d8-9976-507b191de956)

### clear
    Description - clear the terminal screen.
    
    Example:- clear
    Output:- 

![Screenshot (412)](https://github.com/user-attachments/assets/ccb4b4da-67b6-40d8-a230-169aceaa75f6)

![Screenshot (413)](https://github.com/user-attachments/assets/46bda0be-a07e-493e-a012-74a90cd995ec)

### history
    Description - GNU History Library.
    
    Example:- history
    Output:- 1998  whoami
             1999  whoami --help
             2000  clear
             2001  whoami
             2002  clear
             2003  echo welcome to the Linux terminal
             2004  clear
             2005  history


    then press !1998 (to run whoami command that stored with id 1998 in GNU History library).

![Screenshot (414)](https://github.com/user-attachments/assets/a5e316b0-8777-42c4-81d8-a1a4b22010d6)

### reboot
    Description - Halt, power-off or reboot the machine.
    
    Example - sudo reboot

![Screenshot (416)](https://github.com/user-attachments/assets/5c109c4a-3771-4061-9bb8-f7c98a221516)

![Screenshot (415)](https://github.com/user-attachments/assets/321c4d22-6730-4941-ac49-dd08dd08c0fd)

### shutdown
    Description - Halt, power-off or reboot the machine.
    
    Example - sudo shutdown now (it'll prompt you to enter password thereafter it shutdowns the system)

![Screenshot (417)](https://github.com/user-attachments/assets/278a7e4c-9017-40fe-8678-51b7c724b8e4)

### whatis
    Description - display one-line manual page descriptions.
    
    Example:- wahtis whatis (whatis whoami)
    Output:- 

![Screenshot (418)](https://github.com/user-attachments/assets/6e7784a7-5cb1-436e-849a-a067852e76a7)

### date
    Description - print or set the system date and time.
    
    Example:- date
    Output:- Saturday 10 August 2024 06:48:07 PM IST
    
![Screenshot (419)](https://github.com/user-attachments/assets/8a6ba79d-5d05-40ef-9b5c-a651d89120d7)

### time
    Description - run programs and summarize system resource usage.
    
    Example:- time
    Output:- real	0m0.000s
             user	0m0.000s
             sys	0m0.000s

![Screenshot (420)](https://github.com/user-attachments/assets/f74903ab-6391-4701-a645-07496e53c0ce)

### help
    Description - It helps us to learn about any built-in command.
    
    Example - cd --help

![Screenshot (421)](https://github.com/user-attachments/assets/deb4ec8d-f0ac-413f-a4c5-65784cdcde9d)

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

![Screenshot (422)](https://github.com/user-attachments/assets/3757d670-9da1-4ecd-b0ad-e682369e0b3a)


### whereis
    Description - locate the binary, source, and manual page files for a command.
    
    Example - whereis mkdir
    Output - mkdir: /usr/bin/mkdir /usr/share/man/man1/mkdir.1.gz

![Screenshot (423)](https://github.com/user-attachments/assets/c7184196-1a62-440b-a92a-6e0dd6722e6b)

### which
    Description - locate a command.
    
    Example - which mkdir
    Output - /usr/bin/mkdir

![Screenshot (424)](https://github.com/user-attachments/assets/74511b05-09d8-4064-bb17-474c39e76fb1)

### expr
    Description - evaluate expressions.
    
    Example - expr expr 7 + 6
    Output:- 13

![Screenshot (425)](https://github.com/user-attachments/assets/2db719d3-d9f8-4ad8-85d5-49f6ef3fef1d)

### bash --version
    Description - GNU Bourne-Again SHell.
    
    Example - bash --version
    Outpu - bash --version
            GNU bash, version 5.1.16(1)-release (x86_64-pc-linux-gnu)
            Copyright (C) 2020 Free Software Foundation, Inc.
            License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
            
            This is free software; you are free to change and redistribute it.
            There is NO WARRANTY, to the extent permitted by law.

![Screenshot (426)](https://github.com/user-attachments/assets/7d798669-004a-4fb0-9bb7-2e670917c640)

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

![Screenshot (427)](https://github.com/user-attachments/assets/416aacce-ef64-453c-beed-9d0f37eb5c03)

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

    Example - echo hii! > tests.txt

![Screenshot (428)](https://github.com/user-attachments/assets/873f2003-8b63-4797-a721-517635b3b501)

![Screenshot (429)](https://github.com/user-attachments/assets/35bd3332-a986-4925-94e8-9f747515a5c1)

![Screenshot (430)](https://github.com/user-attachments/assets/bfe10f29-4d65-44e1-afda-0247aa7a5604)


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

![Screenshot (431)](https://github.com/user-attachments/assets/624cec76-f207-4211-9033-61c9316f7eb1)

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
