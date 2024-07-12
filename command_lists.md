# List of Linux Basic Commands

## File and Directory

### ls (la)
    Descriptions:- list directory contents (including files and folders)
    example:- ls -a
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
     Description:- print name of current/working directory
     Example:- cp password.txt security/
     Output:- /home/kamal/Desktop
 ### mv
     Description:- print name of current/working directory
     Example:- pwd
     Output:- /home/kamal/Desktop
 ### touch
     Description:- print name of current/working directory
     Example:- pwd
     Output:- /home/kamal/Desktop
 ### nano
     Description:- print name of current/working directory
     Example:- pwd
     Output:- /home/kamal/Desktop
 ### gedit
     Description:- print name of current/working directory
     Example:- pwd
     Output:- /home/kamal/Desktop
 ### cat
     Description:- print name of current/working directory
     Example:- pwd
     Output:- /home/kamal/Desktop
 ### tac
     Description:- print name of current/working directory
     Example:- pwd
     Output:- /home/kamal/Desktop
 ### head
     Description:- print name of current/working directory
     Example:- pwd
     Output:- /home/kamal/Desktop
 ### tail
     Description:- print name of current/working directory
     Example:- pwd
     Output:- /home/kamal/Desktop
 ### find
     Description:- print name of current/working directory
     Example:- pwd
     Output:- /home/kamal/Desktop
 ### file
     Description:- print name of current/working directory
     Example:- pwd
     Output:- /home/kamal/Desktop
 ### zip
     Description:- print name of current/working directory
     Example:- pwd
     Output:- /home/kamal/Desktop
 ### unzip
     Description:- print name of current/working directory
     Example:- pwd
     Output:- /home/kamal/Desktop
**--------------------------------------------------------------------------------------------------------------------**
## Networking
### route
### netstat
### whois
### ping
### dig
### host
### hostname
**--------------------------------------------------------------------------------------------------------------------**
## User & Group
### useradd
### userdel
### usermod
### groupadd
### groupdel
### groupmod
### passwd


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
### grep
### history
### reboot
### shutdown
### whatis 
### whereis
