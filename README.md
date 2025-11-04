Scripting
Question 1 (1 point) 
Given the following data containing Name, Age, and Occupation:

John 25 Engineer
Sara 30 Doctor
Mark 22 Artist
Bob 37 Judge
TJ 32 Fireman
Jane 28 Teacher
Which `awk` statement will print only names that begin with the letter J?

Question 1 options:

awk '$0 ~ /J/ { print $1 }'

awk '$0 ~ /J/ { print $0 }'

awk '$1 ~ /^J/ { print $1 }'

awk '$1 ~ /J/ { print $1 }'
Refer to the following script named `eval.sh` to answer the questions in this section:

#!/bin/bash

a=""
b=""

while getopts "n:a:" opt; do
  case $opt in
    n)
      a=$OPTARG
      ;;
    a)
      b=$OPTARG
      ;;
    \?)
      echo "Usage: $0 [-n a] [-a b]"
      exit 1
      ;;
  esac
done

echo "$a"
if [[ $b -gt 55 ]]; then
        echo "bubbles"
else
        echo "b"
fi
Question 2 (1 point) 
Provide a command using `eval.sh` that will output:

Bob
bubbles
Question 2 options:
Question 3 (1 point) 
Provide a command using `eval.sh` that will output:

Sam
b
Question 3 options:
Question 4 (1 point) 
Provide a command using `eval.sh` that will output:

Usage: eval.sh [-n a] [-a b]Question 5 (1 point) 
For the following text:

@ppl3
b@n@n@s
p1n3@ppl3s
Select the right set of `sed` commands that will return the words to normal:

apple
bananas
pineapples
Select 3 correct answer(s)
Question 5 options:

sed 's/e/3/g'

sed 's/1/i/g'

sed 's/[@31]/aei/g'

sed 's/@/a/g'

sed 's/3/e/g'

sed 's/1/I/g'

sed 's/@/a/'
Question 6 (1 point) 
Write a command to search bash history for use of the `rm` command. 

Your answer must use piping for credit

Question 6 options:
uestion 7 (1 point) 
Select all that are true statements about UEFI:

Select 4 correct answer(s)
Question 7 options:

uses bootloaders stored in an EFI partition


supports MBR partition tables


supports GPT partition tables


uses a bootloader stored in the MBR partition located at the first sector of the disk


provides a graphical user interface (GUI) with mouse support before the OS is loaded


provides a text based interface with keyboard support


supports secure boot


does not support secure boot

Question 8 (1 point) 
Select all that are true

The Linux kernel:

Select 5 correct answer(s)
Question 8 options:

manages processes


can be updated without reinstalling the operating system. 


cannot be updated without reinstalling the operating system


is loaded into memory by the bootmgr bootloader


manages user accounts


manages memory


manages filesystem structure


is loaded into memory by the grub bootloader

Question 9 (1 point) 
Select all that are true statements about BIOS:

Select 4 correct answer(s)
Question 9 options:

supports secure boot


uses a bootloader stored in the MBR partition located at the first sector of the disk


does not support secure boot


uses bootloaders stored in an EFI partition


provides a graphical user interface (GUI) with mouse support before the OS is loaded


supports GPT partition tables


provides a text based interface with keyboard support


supports MBR partition tables

Question 10 (1 point) 
Select all that are true

The partition table:

Select 1 correct answer(s)
Question 10 options:

manages disk partitions


manages filesystems


manages OS processes

Page 3 of 8

0 of 32 queThe Basics
`bat` is a real program

Question 11 (1 point) 
`bat` is installed as a program named `batcat`. 

Recommend an implementation that will allow a user to type `bat` to use the program instead of `batcat`

Question 11 options:
Question 12 (1 point) 
The output of `stat` on the program `/usr/bin/batcat` is:

File: /usr/bin/batcat
Size: 5289400         Blocks: 10336      IO Block: 4096   regular file
Device: 202,1   Inode: 2765        Links: 1
Access: (0755/-rwxr-xr-x)  Uid: (    0/    root)   Gid: (    0/    root)
Access: 2025-04-04 01:07:20.900303168 +0000
Modify: 2023-12-04 08:41:05.000000000 +0000
Change: 2025-04-04 01:03:32.370977493 +0000
Birth: 2025-04-04 01:03:32.328977817 +0000
What are valid ways of running the `batcat` program?

Select 2 correct answer(s)
Question 12 options:

~/batcat


bash batcat


/usr/bin/batcat


batcat

Question 13 (Bonus) (1 point) 
[BONUS] Write a command to use `batcat` to print line number next to a file's contents.

Question 13 options:
Question 14 (1 point) 
Write a command to install the program `bat` via the `apt` package manager.  Make sure to acknowledge privilege level to perform the action.

Question 14 options:
Question 15 (1 point) 
The output of `stat` on the program `/usr/bin/batcat` is:

File: /usr/bin/batcat
Size: 5289400         Blocks: 10336      IO Block: 4096   regular file
Device: 202,1   Inode: 2765        Links: 1
Access: (0755/-rwxr-xr-x)  Uid: (    0/    root)   Gid: (    0/    root)
Access: 2025-04-04 01:07:20.900303168 +0000
Modify: 2023-12-04 08:41:05.000000000 +0000
Change: 2025-04-04 01:03:32.370977493 +0000
Birth: 2025-04-04 01:03:32.328977817 +0000
What user(s) can run `batcat`? 

Question 15 options:

Only root


Any user


Only members of the group root


Only non-root users or users not in the root group

Question 16 (1 point) 
The command `which batcat` will show:

Question 16 options:

How to use batcat, the program installed from the bat package


The source code of the batcat program


An ascii art batcat


Where the batcat program is locatedQuestion 17 (1 point) 
Given the following output from running `lscpu` on the AWS sandbox instance:

Architecture:             x86_64
  CPU op-mode(s):         32-bit, 64-bit
  Address sizes:          46 bits physical, 48 bits virtual
  Byte Order:             Little Endian
CPU(s):                   1
  On-line CPU(s) list:    0
Vendor ID:                GenuineIntel
  Model name:             Intel(R) Xeon(R) CPU E5-2686 v4 @ 2.30GHz
    CPU family:           6
    Model:                79
    Thread(s) per core:   1
    Core(s) per socket:   1
    Socket(s):            1
    Stepping:             1
How many CPU cores does the AWS sandbox instance have?

Question 17 options:
Question 18 (1 point) 
The ___ is a software that allocates the underlying host physical computing resources such as CPU and memory to individual virtual machines as required.

Question 18 options:

OS


partition


kernel


hypervisor

Question 19 (1 point) 
Given the following output from running `lsblk` on the AWS sandbox instance:

NAME     MAJ:MIN RM  SIZE RO TYPE MOUNTPOINTS
xvda     202:0    0   16G  0 disk
├─xvda1  202:1    0   15G  0 part /
├─xvda14 202:14   0    4M  0 part
├─xvda15 202:15   0  106M  0 part /boot/efi
└─xvda16 259:0    0  913M  0 part /boot
What is the size of the disk device in gigabytes attached to the AWS sandbox instance?

Question 19 options:
Question 20 (1 point) 
Given the following output from running `lsmem` on the AWS sandbox instance:

RANGE                                 SIZE  STATE REMOVABLE BLOCK
0x0000000000000000-0x000000003fffffff   1G online       yes   0-7

Memory block size:       128M
Total online memory:       1G
Total offline memory:      0B
How much RAM in gigabytes does the AWS sandbox instance have?

Question 20 options:
Question 21 (2 points) 
Match the PC components to their descriptions

Question 21 options:

allows for long-term data storage.  Installed programs, data, and your OS are written on these types of component


performs graphical focused instructions.  Often a dedicated device, although most laptops would integrate this with the CPU to conserve space


Large printed circuit board that distributes electricity & facilitates communication among components


executes instructions of a computer program, such as arithmetic, logic, controlling, and input/output (I/O) operations.  Typically consists of more than one core in addition to built in L caches


component that allows temporary (volatile) storage of processes and data used by those processes

1.	
Motherboard

2.	
CPU

3.	
RAM

4.	
GPU

5.	
HDD, SSD, & NVME

Page 5 of 8

0 of 32 questions save 
What is the name of the first process that begins in Linux?

Question 22 options:

systemd / init


goat


systemctl


service

Use the following snippet of output from `ps` to answer the following questions:

USER         PID    PPID TT       STAT COMMAND
ubuntu      2339    2336 pts/0    Ss   bash
ubuntu      3019    3018 pts/1    Ss   bash
ubuntu      3076    3075 pts/2    Ss   bash
ubuntu      3085    3076 pts/2    S+   tmux: client
ubuntu      3088    3087 pts/3    Ss   bash
ubuntu      3137    3088 pts/3    S+   bash
ubuntu      3138    3137 pts/3    S+   sleep
ubuntu      3180    2339 pts/0    S+   a
ubuntu      3181    3180 pts/0    Z+   b
ubuntu      3182    3019 pts/1    R+   ps
Question 23 (1 point) 
Give a command to kill the process running "sleep"

Question 23 options:
Question 24 (1 point) 
Give the process ID of the Zombie process:

Question 24 options:
Question 25 (1 point) 
What would be the effect of running `kill 3076`?

Question 25 options:

Nothing would happen, it requires a different kill signal


The shell would exit, terminating the child processes


tmux would output an audible panic beep


The zombie process would end.

 
Assuming a service file has been configured and systemctl has been reloaded to detect the service, what command would enable the service to start on boot?

Question 26 options:

sudo systemctl enable service_name


sudo systemctl start service_name


sudo systemctl reload service_name


sudo systemctl stop service_name


sudo systemctl disable service_name

Question 27 (1 point) 
In Linux, if a filesystem should be mounted automatically on system boot, an entry should be added to:

Question 27 options:

/etc/systemd/system


/mnt


/etc/fstab

Question 28 (1 point) 
A new disk to expand available storage is added to a system.  Correctly order the steps below to make the disk usable for file storage.

Question 28 options:

Create a filesystem on the partition

Create a partition table

Create one or more partitions

Mount the filesystem
Question 29 (1 point) 
Um, actually, an operating system is installed to a:

Question 29 options:

partition


BIOS


device


partition table

Question 30 (1 point) 
A new disk to expand available storage is added to a system.  Correctly order the commands below utilized to make the disk usable for file storage.

Question 30 options:

mkfs.ext4 /dev/device_name

gdisk /dev/device_name

mount /mount_location /dev/device_name
Question 31 (1 point) 
Once a filesystem is unmounted, all data stored on the filesystem is lost

Question 31 options:
	True
	False
Question 32 (1 point) 
If a partition table is altered, all data previously stored in filesystems on partitions is now lost.

Question 32 options:
	True
	False
Page 8 of 8

0 of 32 questions 
