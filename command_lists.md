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
 
 ### diff
 
 ### less
 
 ### more
 
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
    for((i=1;i<=1000;i++)); do echo $i >> thousands.txt;done (prints numbers from 1 - 100 and will be saved into thousands.txt)

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
 ### gz

 ### vim
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

