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
| System Startup      | BootLoader stage | Kernel Stage      | init stage process |
| ---------------         | ----------- | ----------- | ----------- |
|Power ON             | Boot Device (Boot sector (BIOS/MBR) or .EFI partition file(UEFI/GUID Partition Table (GPT)) | Loading Kernel   | Systemd replaces init by modern OS)|
| BIOS / UEFI         | Bootloader (GRUB2) Present Boot Menu screen (Select OS & respective Kernel) | Initialize System Resource & H/w ,Decompressing Kernel image | System daemons      |
| POST (H/W Integrity tests)| Linux Booting, bootloaders(GRUB) Loads(Kernel image)|Kernel Loads & mounts the initrd or initramfs| Start (Background) Services or Process|
| Locate or find bootdevice   | Kernel image and Inital RAM disk(initrd) or file system(initramfs)        | Temporary Root FS (initramfs) into RAM | Login Screen       |

### 1. System startup
When powered ON BIOS/UEFI firmware first run POST program(Power ON Self Test) to check H/W integrity to ensure all connected H/W device or components connected to the system are working properly or not. If Post runs without having critical errors or H/w failures then control goes to BIOS/UEFI, if not then it gives us error messages(code) or a series of audible beeps(beep code) depending upon the errors.

POST checking examples :- CPU, RAM(memory), Sotrage devices(HDD,SSD,Flash drive,), graphics card, peripheral (Keyboard, Mouse).
The BIOS software is stored on a ROM chip on the motherboard.

After POST successfully completed, BIOS/UEFI looks for bootable device(HDD,SDD,USB,CD-ROM,DVD,Network interfaces) on the system which stores OS(e.g. Linux) using a predetermined boot order(boot priority) that was previously set in the BIOS settings.

Once the boot device has been identified, the BIOS proceeds to search for either the Master Boot Record (MBR) or the GUID Partition Table (GPT) on the storage device. These contain the crucial initial boot loader code. The boot loader is usually stored on one of the hard disks in the system, either in the boot sector (for traditional BIOS/MBR systems) or the EFI partition (for more recent (Unified) Extensible Firmware Interface or EFI/UEFI systems).Thereafter, information on date, time, and the most important peripherals are loaded from the CMOS values (after a technology used for the battery-powered memory store which allows the system to keep track of the date and time even when it is powered off).

### 2. Bootloader stage
In bootloader stage, after detecting boot device it finds the boot sector on storage device on which OS is avaible. It searches first-stage bootloader(primary) and the first stage(first-sector) bootloader, which is a part of the MBR, is a 512-byte image containing the vendor-specific program code and a partition table. The first stage bootloader will find and load the second stage(secondary) bootloader. It does this by searching in the partition table for an active partition. After finding an active partition, first stage bootloader will keep scanning the remaining partitions in the table to ensure that they're all inactive. After this step, the active partition's boot record is read into RAM and executed as the second stage bootloader. The job of the second stage bootloader is to load the Linux kernel image into memory, and optional initial RAM disk.

(GRUB2) GRUB stands for Grand Unified Boot Loader. It's a widely used boot loader in the Linux world, responsible for managing the boot process of a computer.
GRUB2 shows a menu where you can choose between different Linux kernels or even another operating system like Windows.
A boot loader is a program that loads the operating system into the computer's memory during the startup process. GRUB is specifically designed for Unix-like operating systems, especially Linux.
When booting Linux, the boot loader(GRUB2) is responsible for loading the kernel image and the initial RAM disk or filesystem (which contains some critical files and device drivers needed to start the system) into memory(RAM).It also manages the initial RAM disk (initrd/initramfs) that assists the kernel during the boot process.

During the installation of Linux distributions, GRUB is usually installed in the Master Boot Record (MBR) of the hard drive or the EFI system partition (for systems using UEFI). This allows GRUB to take control during boot-up and present its menu interface.

Besides GRUB there are popular bootloaders:
- systemd-boot (formerly Gummiboot)
- SYSLINUX/ISOLINUX
- Das U-Boot (for embedded devices/appliances)
- coreboot
- rEFInd

Historical bootloaders, no longer in common use, include:
- LILO
- GRUB1
- loadlin

### 3. The Kernel Stage
The kernel is the core of the operating system, managing hardware resources, providing abstractions, and controlling interactions between hardware and software.
Kernel initializes system resources and hardware. The kernel uses information provided by the **initrd(initial RAM Disk)** to mount the actual root file system **(rootfs)** (for example, ext4, XFS) specified in the boot parameters. The kernel replaces the **temporary root filesystem(initrd or initramfs) also known as early user space** with the **actual root filesystem(rootfs)** on the hard drive.

The boot loader loads both the kernel and an **initial RAM–based file system (initramfs)** into memory, so it can be used directly by the kernel.
The Linux kernel handles all operating system processes, such as memory management, task scheduling, I/O, interprocess communication, and overall system control. This is loaded in two stages – in the first stage, the kernel (as a compressed image file) is loaded into memory and decompressed, and a few fundamental functions are set up such as basic memory management, minimal amount of hardware setup. It's worth noting that **kernel image is self-decompressed**, which is a part of the kernel image's routine. For some platforms (like ARM 64-bit), kernel decompression has to be performed by the bootloader instead, like U-Boot.During boot-up, the boot loader (such as GRUB) loads the Linux kernel into memory. The kernel then decompresses itself and, if configured to use an initrd, loads the initrd image as a temporary root file system into a predetermined memory location.

After the initrd image completes its tasks, the kernel takes control. It initializes the system hardware, mounts the root file system, and begins the user-space initialization process. An Initial RAM Disk (initrd), also known as an Initial RAM filesystem (initramfs), is a temporary file system loaded into memory during the boot process of a computer before the main operating system takes over. It's an essential component in modern Linux booting.

The primary purpose of the initrd is to provide a minimal set of tools, drivers, and utilities necessary to mount the root file system**(rootfs)**. It contains essential drivers for storage controllers, file systems, and other hardware components that the kernel might need to access the actual root file system. After the kernel initializes and detects hardware, the **initrd's** job is largely complete. It hands control over to the main kernel, which then unmounts the **initrd** and mounts the actual root file 
system **(rootfs)** (specified by the bootloader or kernel parameters).

Traditionally, initrd was used, but modern systems often use initramfs (a more flexible successor). Initramfs is a cpio archive that is uncompressed into a RAM disk at boot time. It's more versatile, allowing for a more modular approach to including essential files and drivers.


The Root File System (rootfs) is a critical component in the booting process of an operating system. It is the top-level directory hierarchy of the file system and contains essential system files and directories.

In the context of the booting process, the root file system is the initial file system that the operating system kernel mounts during the boot sequence.
The root file system is the starting point for the entire file system hierarchy. It is mounted by the kernel during the boot process, and all other file systems are mounted as subdirectories of the root file system.

The bootloader, such as GRUB in many Linux systems, is configured to specify the location of the root file system. This information is crucial for the kernel to know where to find the core files and directories needed to start the operating system.

The **root file system(rootfs)** contains critical directories such as /bin, /etc, /sbin, and /lib. These directories house essential binaries, configuration files, system libraries, and scripts required for system operation. The root file system can be of different types, such as ext4, XFS, or other supported file systems. The choice of the file system type depends on the system administrator's preferences and requirements.
The stability and functionality of the operating system depend on the successful initialization and mounting of the root file system. It provides the foundation for the entire operating system environment.

### 4. init stage process (systemd)
The init process, whether traditional init or systemd, is responsible for starting system services and daemons. These services provide essential functionality to the operating system, such as networking, logging, and hardware-related services. Historically this was the "SysV init", which was just called "init". SysVinit viewed things as a serial process, divided into a series of sequential stages. Each stage required completion before the next could proceed.
More recent Linux distributions are likely to use one of the more modern alternatives such as systemd.

The init system is the first daemon to start (during booting) and the last daemon to terminate (during shutdown).During the boot process, the init or systemd process is responsible for starting system daemons. These daemons are configured to launch automatically at specific runlevels (in the case of traditional init) or as defined in systemd unit files. In a standard Linux system, init is executed with a parameter, known as a runlevel, which takes a value from 0 to 6 and determines which subsystems are made operational. Each runlevel has its own scripts which codify the various processes involved in setting up or leaving the given runlevel, and it is these scripts which are referenced as necessary in the boot process. Init scripts are typically held in directories with names such as "/etc/rc...".

A daemon is a background process that runs independently of user interaction. Daemons perform specific tasks, such as managing hardware, handling system events, or providing network services.

systemd, in particular, introduces parallel initialization, meaning that multiple daemons and services can be started simultaneously, improving boot times by taking advantage of modern multi-core systems.

One thing to note is that **/sbin/init** now just points to **/lib/systemd/systemd;** i.e. **systemd** takes over the **init** process.
One systemd command (systemctl) is used for most basic tasks.

- Starting, stopping, restarting a service (using **httpd**, the Apache web server, as an example) on a currently running system:
**$ sudo systemctl start|stop|restart httpd.service**
- Enabling or disabling a system service from starting up at system boot:
**$ sudo systemctl enable|disable httpd.service**

Examples of system daemons include:

- **Network services:** Daemons like sshd for secure shell access, httpd for web services, and dhcpd for dynamic host configuration protocol.
- **Logging services:** rsyslogd or syslog-ng for handling system logs.
- **cron** (task scheduler)
- **Time synchronization:** ntpd for Network Time Protocol (NTP) synchronization.
- **Printing services:** cupsd for Common Unix Printing System.
- **Hardware management:** udev for device management and acpid for Advanced Configuration and Power Interface events.

Once system daemons are initialized, the system is ready to handle user interactions. For example, network services are available, and users can log in or access various system resources.





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

    
