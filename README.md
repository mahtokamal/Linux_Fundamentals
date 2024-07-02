**-------------------------------------------------------------------------------------------------------------------------------------**
# Linux Fundamental Commands

This is beginner's friendly Linux Fundamental Commands.

Disclaimer : Some of the commands might not found or work in recent versions of Linux distro. If anyone wants to run those
commands then he/she should have to install that command first.


**-------------------------------------------------------------------------------------------------------------------------------------**
## Linux Booting Process

Booting process is when you powered ON your System until you'll get Login GUI interface fully operationals. Having good
knowledge of each boot process step assists us in troubleshootings.

![image-373](https://github.com/mahtokamal/Linux_Fundamentals/assets/62587491/10b5f828-7017-4da8-9dea-45e2be97cd25)

![image-150](https://github.com/mahtokamal/Linux_Fundamentals/assets/62587491/8ff4128b-1613-4109-a644-b91ea890c54d)
### Linux 4 stage Booting Process
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

### 1. BIOS - The First Step
### 2. MBR - Master Boot Record 
### 3. The Bootloader
    - Initial RAM Disk
    - Text-mode Login
    
### 4. The Linux Kernel
### 5. /Sbin/init and Services
    - Startup Alternatives
### 6. Systemd Features


 


**-------------------------------------------------------------------------------------------------------------------------------------**

## CTRL+ALT+T

- shorcuts to open Terminal


**-------------------------------------------------------------------------------------------------------------------------------------**
## CTRL+D

- Close the terminals


**-------------------------------------------------------------------------------------------------------------------------------------**

## time
-


**-------------------------------------------------------------------------------------------------------------------------------------**

## date
-


**-------------------------------------------------------------------------------------------------------------------------------------**

## help (date --help or --h)


**-------------------------------------------------------------------------------------------------------------------------------------**

## man ls


**-------------------------------------------------------------------------------------------------------------------------------------**

## uniq


**-------------------------------------------------------------------------------------------------------------------------------------**

## hostname
(kamal@Ubuntu)
syntax -  hostname
output - Ubuntu


**-------------------------------------------------------------------------------------------------------------------------------------**

## uname
- tells about OS
Syntax - uname
output - Linux

uname -a 
(Shows detailed System informations)


**-------------------------------------------------------------------------------------------------------------------------------------**

## host google.com


**-------------------------------------------------------------------------------------------------------------------------------------**
## expr
- info expr
- expr 3 + 3


**-------------------------------------------------------------------------------------------------------------------------------------**
## bash --version


**-------------------------------------------------------------------------------------------------------------------------------------**

## Cal 2024


**-------------------------------------------------------------------------------------------------------------------------------------**

## whoami


**-------------------------------------------------------------------------------------------------------------------------------------**

## pwd


**-------------------------------------------------------------------------------------------------------------------------------------**

## which

## CTRL + C 
- exits Programs abnormally or forcily
## CTRL + D
- exits the Program normally


**-------------------------------------------------------------------------------------------------------------------------------------**

**-------------------------------------------------------------------------------------------------------------------------------------**

## dir

**-------------------------------------------------------------------------------------------------------------------------------------**
## File and Directory
### ls (la)
    list directory contents 
    example :ls (-a, -l, -h, -r, -t, -R, -i, -I, -v, -f, -t) 
    a - all includes hidden files and folder 
    l - long list
    h - human readable format
    t - sort by time 
    R - Recursive files of folders 
    i - Interactivity 
    I - 
    v - Verbose 
    f - forcefully 
    t - sort by time

 ### cd
 ### dir
 ### pwd
 ### mkdir
 ### rmdir
 ### cp
 ### mv
 ### touch
 ### nano
 ### gedit
 ### cat
 ### tac
 ### head
 ### tail
 ### find
 ### file
 ### zip
 ### unzip
**-------------------------------------------------------------------------------------------------------------------------------------**
## Networking
### route
### netstat
### whois
### ping
### dig
### host
### hostname
**-------------------------------------------------------------------------------------------------------------------------------------**
## User & Group
### useradd
### userdel
### usermod
### groupadd
### groupdel
### groupmod
### passwd


**-------------------------------------------------------------------------------------------------------------------------------------**
## Permission & ownership
### chmod
### chown
### chgrp


**-------------------------------------------------------------------------------------------------------------------------------------**
## Process Management
### ps
### top
### kill
### nice
### systemctl
### bg
### fg
**-------------------------------------------------------------------------------------------------------------------------------------**
## Disk Space Usage
### df
### du
### free
### fdisk
### findmnt

**-------------------------------------------------------------------------------------------------------------------------------------**
## Other additional Commands
### man
### whoami
### clear
### grep
### history
### reboot
### shutdown

**-------------------------------------------------------------------------------------------------------------------------------------**


## echo "hello ho" > file1.txt
## echo "hjkl" >> file1.txt


**-------------------------------------------------------------------------------------------------------------------------------------**

## ping google.com (ping ip)


**-------------------------------------------------------------------------------------------------------------------------------------**

## bc


**-------------------------------------------------------------------------------------------------------------------------------------**

## touch test2.txt

touch .test.txt [This creates a hidden file]


**-------------------------------------------------------------------------------------------------------------------------------------**

## file test2.txt


**-------------------------------------------------------------------------------------------------------------------------------------**

## find *.txt


**-------------------------------------------------------------------------------------------------------------------------------------**

## cat test2.txt


**-------------------------------------------------------------------------------------------------------------------------------------**

## grep "hello" test2.txt

## diff

## passwd
## info echo



**-------------------------------------------------------------------------------------------------------------------------------------**

## cd hello/ 

['/' -> represents the Root directory
'$' -> represents the Standard or regular Users
'~' -> represents the home directory]


**-------------------------------------------------------------------------------------------------------------------------------------**

## mkdir hello1/ hello2/

mkdir .hello/ [This creates a hidden folder]


**-------------------------------------------------------------------------------------------------------------------------------------**

## cp test1.txt hello1/
   - cp -r 


**-------------------------------------------------------------------------------------------------------------------------------------**

## mv test1.txt hello1/
  - mv -i


**-------------------------------------------------------------------------------------------------------------------------------------**

## rm test1.txt


**-------------------------------------------------------------------------------------------------------------------------------------**

## mv hello1 hell


**-------------------------------------------------------------------------------------------------------------------------------------**

## rm -Ri hello1/


**-------------------------------------------------------------------------------------------------------------------------------------**

## rmdir hello1/


**-------------------------------------------------------------------------------------------------------------------------------------**

## ln test1.txt testhardlinks


**-------------------------------------------------------------------------------------------------------------------------------------**

## ln -s test1.txt softlinks


**-------------------------------------------------------------------------------------------------------------------------------------**

## ["directory loop"
mkdir a/ then within a/ create b/
then, within /b 
ln -s .. c]


**-------------------------------------------------------------------------------------------------------------------------------------**

## mkdir 'hello love'
mkdir my\ cat, mkdir my\ \ cat, 
mkdir \$\ "dollars"\'\;\&\|

- Quoting, escaping and filenames using special character including space


**-------------------------------------------------------------------------------------------------------------------------------------**

## gedit test1.txt
## nano test1.txt


**-------------------------------------------------------------------------------------------------------------------------------------**

## history [!12]


**-------------------------------------------------------------------------------------------------------------------------------------**

## less "hell" test1.txt [to view content of the files]

NOTE : opposite of more

## more t1.txt

NOTE : file perusal filter for crt viewing


**-------------------------------------------------------------------------------------------------------------------------------------**

## tac test1

NOTE : in cat, we view the content of file from first to last, however in tac we get content
from the files from last to first.
For example : 
**********************************
with cat , [concatenate files and print on the standard output]
Guten abend!
Good evening!
*****************************************
**************************************
with tac,[concatenate and print files in reverse]
Good evening!
Guten abend!

**************************************


**-------------------------------------------------------------------------------------------------------------------------------------**

## vim


**-------------------------------------------------------------------------------------------------------------------------------------**

## head and tail
for((i=1;i<=1000;i++)); do echo $i >> hundreds.txt;done
for((i=1;i<=1000;i++)); do echo $i >> thousands.txt;done
head thousand (head -n 20 thousand)
tail thousand (tail -n 20 thousand)


**-------------------------------------------------------------------------------------------------------------------------------------**

## wc -l acces.log(wc access.log, wc - W, -C, L hundred)
[Line number, Word, characters/byte numbers]


**-------------------------------------------------------------------------------------------------------------------------------------**

## type pwd (type cd)


**-------------------------------------------------------------------------------------------------------------------------------------**

## whatis cp

- display one-line manual page descriptions for respective command.


**-------------------------------------------------------------------------------------------------------------------------------------**

[combining multiple commands
mkdir numbers;date;cal  ls;pwd
touch text; mv text numbers;date;cal or mkdir hello && cp file1.txt hello/]


**-------------------------------------------------------------------------------------------------------------------------------------**

## [wildcards
* - macthes any number of characters
? - matches single character
cp n* hello/
cp n*ch hello/
cp file?.txt hello/
cp file??.txt hello/
cp f?l*.txt hello/
cp [abc]* dir1/  -> '[]' represents the range
cp [!abc]* dir1/
cp [[:upper:]]* dir1/
cp [[:lower:]]* dir1/
cp [0-9]* dir1/
cp *[[:digit:]] dir1/
cp *[[:alpha:]] dir1/
cp [[:alpha:]]* dir1/
cp [[:alnum:]]* dir1/
cp [[:digit:]]*[[:alpha:]] dir1/

]


**-------------------------------------------------------------------------------------------------------------------------------------**

***********
 ## alias    *
***********
Note -  before making your own command just check whether it is shell builtin or not, if it's builtin then we can't make aliases

type test
type invent

alias invent="cd Desktop;mkdir dir2;touch hello.txt;date;cal"

alias copy="cp"
alias rename="mv"

alias del ="rm -i"
unalias del

cd ~
ls -a
goto .bashrc
gedit .bashrc
open it then paste your alias command to save it indefinite time
#some more user created aliases
alias del ="rm -i"

alias


**-------------------------------------------------------------------------------------------------------------------------------------**
## Absolute VS. Relative Path
Absolute (Complete path from start to end)
cd /home/kamal/kamal/this
Relative (current working directory)
cd kamal

Note - The command with '/' is Absolute path whereas,without '/' is Relative Path


**-------------------------------------------------------------------------------------------------------------------------------------**

## User in Linux
sudo - Super User Do
1.Root (Super user) - Full access to the System
2.Regular (Normal user) - stores all their files in home(~) directory and limited access
3.Service 

sudo apt update/upgrade
sudo apt install apache3


**-------------------------------------------------------------------------------------------------------------------------------------**

## chmod

-Change mode
-It changes file modes in bits

owner 
group
others

r - read
w - write
x - execute

4 - stands for read (r)
2 - stands for write (w)
1 - stands for execute (x)
0 - No permissions

for example - chmod 754 anand (permissions order will be in this order owner, group, others)


chmod 777 anand (rwx,rwx,rwx)

chmode 664 events.txt (rw,rw, r)


**-------------------------------------------------------------------------------------------------------------------------------------**

## top

- display Linux processes

PID - 
USER -
PR - 
NI -
VIRT -
RES - 
SHR -
S -
%CPU - 
%MEM - 
TIME+ -
Command - 

**-------------------------------------------------------------------------------------------------------------------------------------**
## ps
 -report a snapshot of the current processes.

 - ps -a
 - ps -ef
   it displays the full format listing of processes.

 - kill
   kill 6760 (6760 is process_id [pid])


=========================================================================================

**-------------------------------------------------------------------------------------------------------------------------------------**

## users

- shows currently log in username


**-------------------------------------------------------------------------------------------------------------------------------------**
## verifying files using checksum
## Compress and extract tar and gz
## install software using apt -get

## Groups and more
## Setup and Connect SSH server
  - ssh key authentications

**-------------------------------------------------------------------------------------------------------------------------------------**
## Partitions

**-------------------------------------------------------------------------------------------------------------------------------------**
## Process 
- ps ax

**-------------------------------------------------------------------------------------------------------------------------------------**
## Jobs and kill processes

**-------------------------------------------------------------------------------------------------------------------------------------**

    
