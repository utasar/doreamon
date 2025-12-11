Processes & Services
Questions in this section may refer to the following `ps` outputs and snippet of a service status:

USER         PID    PPID %CPU %MEM TT       STAT  STARTED     TIME COMMAND
root         579       1  0.0  0.2 ?        Ss   16:55:57 00:00:01 apache2
www-data    1655     579  0.0  0.1 ?        Sl   00:00:13 00:00:00 apache2
www-data    1656     579  0.0  0.1 ?        Sl   00:00:13 00:00:00 apache2
ubuntu      1780       1  0.0  0.2 ?        Ss   00:08:26 00:00:00 systemd
ubuntu      1783    1780  0.0  0.0 ?        S    00:08:26 00:00:00 (sd-pam)
ubuntu      1890    1775  0.1  0.1 ?        S    00:08:27 00:00:00 sshd
ubuntu      1891    1890  0.0  0.1 pts/0    Ss   00:08:27 00:00:00 bash
bob         1921       1  0.0  0.2 ?        Ss   00:12:03 00:00:00 systemd
bob         1922    1921  0.0  0.0 ?        S    00:12:03 00:00:00 (sd-pam)
bob         1987    1917  0.0  0.1 ?        S    00:12:03 00:00:00 sshd
bob         1988    1987  0.0  0.1 pts/1    Ss   00:12:03 00:00:00 bash
bob         1998    1988  0.0  0.3 pts/1    S+   00:12:08 00:00:00 python3
ubuntu      2158    2111  0.0  0.1 ?        S    00:13:14 00:00:00 sshd
ubuntu      2159    2158  0.0  0.1 pts/2    Ss   00:13:14 00:00:00 bash
sally       2171    2170  0.0  0.1 pts/3    S+   00:13:17 00:00:00 bash
sally       2235    2171  0.0  0.1 pts/3    S+   00:28:28 00:00:00 tmux: client
sally       2237       1  0.0  0.1 ?        Ss   00:28:29 00:00:00 tmux: server
sally       2238    2237  0.0  0.1 pts/4    Ss+  00:28:29 00:00:00 bash
ubuntu      2181    1891  0.0  0.1 pts/0    R+   00:13:29 00:00:00 ps
ubuntu      2182    1891  0.0  0.0 pts/0    S+   00:13:29 00:00:00 grep
    PID    PPID COMMAND
    579       1 apache2
   1655     579 apache2
   1656     579 apache2
   1773       1 sshd
   1775    1773 sshd
   1890    1775 sshd
   1891    1890 bash
   1917    1773 sshd
   1987    1917 sshd
   1988    1987 bash
   2111    1773 sshd
   2158    2111 sshd
   2159    2158 bash
   2314    2313 bash
● apache2.service - The Apache HTTP Server
     Loaded: loaded (/usr/lib/systemd/system/apache2.service; enabled; preset: enabled)
     Active: active (running) since Tue 2025-04-29 16:55:58 UTC; 7h ago
       Docs: https://httpd.apache.org/docs/2.4/
    Process: 537 ExecStart=/usr/sbin/apachectl start (code=exited, status=0/SUCCESS)
    Process: 1649 ExecReload=/usr/sbin/apachectl graceful (code=exited, status=0/SUCCESS)
   Main PID: 579 (apache2)
      Tasks: 55 (limit: 4674)
     Memory: 10.1M (peak: 18.1M)
        CPU: 1.636s
     CGroup: /system.slice/apache2.service
Question 1 (1 point) 
What is the current state of the apache2 service?

Question 1 options:

stopped


disabled


active


zombie

Question 2 (1 point) 
Pick a command to end bob's python3 process with the least other effects on bob's other processes.

Question 2 options:

kill 1988


kill 1987


kill 1998


kill 1917

Question 3 (1 point) 
For each of the following, classify it as a program, process, or service:

Question 3 options:

a daemon that triggers validate.sh to run


the file / script validate.sh on the disk


a running instance of validate.sh

1.	
program

2.	
process

3.	
service

Question 4 (1 point) 
Which process IDs are for services?

Select 2 correct answer(s)
Question 4 options:

579


2111


1655


1775


1917


1773


1656

Question 5 (1 point) 
What user(s) are currently running an ssh session?

Select 2 correct answer(s)
Question 5 options:

root


ubuntu


bob


www-data


sally

Question 6 (1 point) 
apache2 will be started at boot by systemd

Question 6 options:
	True
	False
Page 1 of 10

0 of 50 questions savedMisc.
Question 7 (1 point) 
You are running a VM that seems sluggish, even though your host machine has plenty of RAM and CPU.  What is a good strategy to implement?

Question 7 options:

Download more RAM to the VM


Increase the RAM and/or CPU available to the VM


Buy a new host machine


Install a new CPU to the VM

Question 8 (1 point) 
Given the following ssh command:

ssh -i ~/key ksmith@wsukduncan.com
Which would be a correct entry in a config file?

Question 8 options:

Host exam
  Hostnme wsukduncan.com
  Usr ksmith
  IdentityFile ~/key

Host exam
	User ksmith
	HostName wsukduncan.com
	IdentityFile ~/key

Host exam
  HostName wsukduncan.com
  User ksmith
  IdentityFile ~/.ssh/keys/mykey.pem

Host exam
  HostName wsukduncan.net
  User ksmith
  IdentityFile ~/key
Page 2 of 10

0 of 50 qProgramming
The questions in this section will require the following files:

message.c containing:

#include <stdio.h>

int main() {
    const char *message = "\x54\x68\x65\x20\x77\x6F\x72\x64\x20\x6F\x66\x20\x74\x68\x65\x20\x64\x61\x79\x20\x69\x73\x20\x71\x75\x61\x73\x69";

    printf("%s\n", message);
    return 0;
}
Makefile containing:

CC = gcc

CFLAGS = -Wall

OP = message

SRCS = message.c

all: $(OP)

$(OP): $(SRCS)
        $(CC) $(CFLAGS) -o $(OP) $(SRCS)

clean:
        rm -f $(OP)                                                                                                                                                           clean:                                                                                                         rm -f $(TARGET)
Question 9 (1 point) 
What command would compile and link this program, assuming the file is named message.c

Question 9 options:

gcc message.c

gcc -E message.c

gcc -S message.c

gcc -c message.c
Question 10 (1 point) 
Compile and run the program using the source code of `message.c`.  What is the word of the day?

Question 10 options:
Question 11 (1 point) 
Select all make commands that would compile the program

Select 3 correct answer(s)
Question 11 options:

make


make rm


make message


make message.c


make OP


make SRCS


make all

Question 12 (1 point) 
What is the dependency for the message target?

Question 12 options:

gcc


message


message.c


OP


-Wall


SRCS

Question 13 (1 point) 
Source code files for compiled languages must be executable.

Question 13 options:
	True
	False
Question 14 (1 point) 
What should not be tracked about a program in a version control system

Select 2 correct answer(s)
Question 14 options:

the source code


the compiled executable


who authored the changes


intermediary files from the compilation process

Question 15 (1 point) 
You are given the following file - helloworld.go

package main

import "fmt"

func main() {
    fmt.Println("Hello, world!")
}
To compile this program, you would need

Question 15 options:

Bash


A Java compiler


A Go compiler


A C / C++ compiler


Python

Page 3 of 10

0 of 50 qGit & GitHub
Use the following to complete questions in this section.

The `stuff` GitHub repository:
https://github.com/pattonsgirl/stuff

The following output of `git status`

On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   file1.txt
        new file:   script.js
        deleted:    old_file.py
Question 16 (1 point) 
Refer to the `git status` output.

What git command was used on script.js to have it state this change status?

Question 16 options:

git add script.js

git rm *

git rm script.js

git commit script.js
Question 17 (1 point) 
There will likely be a merge conflict caused by the words.txt file in docs in the stuff repository

Question 17 options:
	True
	False
Question 18 (1 point) 
Refer to the `git status` output.

What git command was used on old_file.py to have it state this change status?

Question 18 options:

git rm *

git commit old_file.py

git rm old_file.py

git add old_file.py
Question 19 (1 point) 
Refer to the `git status` output.

What git commands needs to be performed next for the changes to exist on the remote repository?

Question 19 options:

git add * && git push

git commit -m "changes" && git push

git commit -m "changes" && git push origin dev

git push && git commit -m "changes"
Question 20 (1 point) 
Which command would clone the stuff repository for authentication with ssh?

Question 20 options:

git pull git@github.com:pattonsgirl/stuff.git


git clone git@github.com:pattonsgirl/stuff.git 


git push git@github.com:pattonsgirl/stuff.git


git clone https://github.com/pattonsgirl/stuff

Question 21 (1 point) 
Which image embed syntax would display fix.jpg in the img folder on the test.md page in the docs folder in the stuff repository?

Question 21 options:

!(whale)[../img/fix.jpg]

![whale](/img/fix.jpg)

!(whale)[/img/fix.jpg]

(whale)[../img/fix.jpg]

![whale](../img/fix.jpg)

![whale](stuff/img/fix.jpg)

[whale](../img/fix.jpg)
Question 22 (1 point) 
Why does the README file not render the markdown and only shows the plain text in the stuff repository?

Question 22 options:

GitHub servers are down


Markdown syntax is incorrect


File must have a .md extension


File needs to declare #!/bin/markdown at the top

Question 23 (1 point) 
You have the ability to push changes to the stuff repository 

Question 23 options:
	True
	False
Page 4 of 10

0 of 50 questions savedPractical
NOTE:  Only use this server to complete the questions on this portion of the final exam.  Log off when you are done.  You may reconnect to check answers.

Private key:

-----BEGIN OPENSSH PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAAAMwAAAAtzc2gtZW
QyNTUxOQAAACD11UTwzaj0mnJazwiLxM7UKbSe7o79JmQUciuY0DkJqQAAAIg/X9SPP1/U
jwAAAAtzc2gtZWQyNTUxOQAAACD11UTwzaj0mnJazwiLxM7UKbSe7o79JmQUciuY0DkJqQ
AAAECjpvdSSuL06fjU2k2wB0KljKto+EfD/UQPVthDwa3ebvXVRPDNqPSaclrPCIvEztQp
tJ7ujv0mZBRyK5jQOQmpAAAABGV4YW0B
-----END OPENSSH PRIVATE KEY-----
Windows + Powershell users - don't forget to add a return character at the end of the file.

Username on server: exam

Server IP: 3.94.30.49

The following Security Group configuration associated with the server:

IP Version	Type	Protocol	Port Range	Source
IPv4	ICMP	ICMP	All	0.0.0.0/0
IPv4	SSH	TCP	22	130.108.0.0/16
Question 24 (2 points) 
Provide the absolute / full path to the private key name and location on YOUR system

Question 24 options:
Question 25 (2 points) 
Write the command you used to ssh to the system

Question 25 options:
Question 26 (2 points) 
According to the README, what is your password?

Question 26 options:
Question 27 (2 points) 
Instead of viewing the whole README file, provide a command that will only print the line with your name on it.

Question 27 options:
Protocols & Firewalls
Questions in this section may refer to the following INBOUND Security Group configuration:



Question 28 (1 point) 
Based on the Security Group rules, any source IP can attempt a connection on port 80

Question 28 options:
	True
	False
Question 29 (1 point) 
The following command would attempt to connect to what port on the server for github.com?

ssh -T git@github.com
Question 29 options:

80


22


443

Question 30 (1 point) 
Based on the Security Group rules, a source IP of 130.108.15.32 can attempt a connection on port 22

Question 30 options:
	True
	False
Question 31 (1 point) 
The following command would attempt to connect to what port on the server for github.com?

curl http://github.com
Question 31 options:

22


443


80

Question 32 (1 point) 
The following command would attempt to connect to what port on the server for github.com?

curl https://github.com
Question 32 options:

22


80


443

Question 33 (1 point) 
Based on the Security Group rules, a source IP of 42.91.83.108 can attempt a connection on port 22

Question 33 options:
	True
	False
Page 6 of 10

0 of 50 questions savedPermissions
Utilize the following outputs for questions in this section:

`ls -l`:

-rw-rw-r--  1 alice  staff   1234 Apr 29 10:15 notes.txt
drwxr-xr-x  3 alice  staff     96 Apr 29 10:20 projects
lrwxr-xr-x  1 alice  staff     11 Apr 29 10:22 hosts -> /etc/hosts
-rwxr-xr-x  1 alice  staff   2048 Apr 29 10:30 script.sh
`id alice`:

uid=1001(alice) gid=1001(alice) groups=1001(alice),27(sudo),1002(developers)
`getent group staff`:

staff:x:1002:alice,bob,charlie
`getent group sudo`:

sudo:x:27:alice
Question 34 (1 point) 
What is `hosts`?

Question 34 options:

a regular file


a directory


a compiled program


a symbolic link


a hardlink

Question 35 (1 point) 
The user `bob` can edit `script.sh`

Question 35 options:
	True
	False
Question 36 (1 point) 
Select the valid commands that would remove others from being able to view the `projects` directory - user and group permissions should not be modified

Select 2 correct answer(s)
Question 36 options:

chmod 760 projects


chmod 750 projects


chmod u-x projects


chmod o=rx projects


chmod 600 projects


chmod 777 projects


chmod a-rx projects


chmod o-rx projects

Question 37 (1 point) 
The user `frank` needs to edit `notes.txt`

What method would give least required privilege?

Question 37 options:

Add `frank` to the `alice` group


Add `frank` to the `staff` group


Allow all users to edit the `notes.txt` file


Add `frank` to the `sudo` group


Have Frank ask Charlie to use his account

Question 38 (1 point) 
The user `charlie` can create new files in `projects`

Question 38 options:
	True
	False
Question 39 (1 point) 
Others can run `script.sh`

Question 39 options:
	True
	False
Page 7 of 10

0 Networking
Questions in this section may refer to the following outputs:

`ip a`

1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host noprefixroute
       valid_lft forever preferred_lft forever
2: enX0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 9001 qdisc mq state UP group default qlen 1000
    link/ether 16:ff:d8:d6:0c:c9 brd ff:ff:ff:ff:ff:ff
    inet 10.0.0.172/24 metric 100 brd 10.0.0.255 scope global dynamic enX0
       valid_lft 2644sec preferred_lft 2644sec
    inet6 fe80::14ff:d8ff:fed6:cc9/64 scope link
       valid_lft forever preferred_lft forever
`route`

Kernel IP routing table
Destination     Gateway         Genmask         Flags Metric Ref    Use Iface
default         _gateway        0.0.0.0         UG    100    0        0 enX0
10.0.0.0        0.0.0.0         255.255.255.0   U     100    0        0 enX0
_gateway        0.0.0.0         255.255.255.255 UH    100    0        0 enX0
10.0.0.2        0.0.0.0         255.255.255.255 UH    100    0        0 enX0
`curl ipinfo.io`

{
  "ip": "3.94.30.49",
  "hostname": "ec2-3-94-30-49.compute-1.amazonaws.com",
  "city": "Ashburn",
  "region": "Virginia",
  "country": "US",
  "loc": "39.0437,-77.4875",
  "org": "AS14618 Amazon.com, Inc.",
  "postal": "20147",
  "timezone": "America/New_York",
  "readme": "https://ipinfo.io/missingauth"
}
Question 40 (1 point) 
What is the subnet mask of the enX0 interface?

Question 40 options:
Question 41 (1 point) 
What source IP address would be "seen" in the request packet sent to the server running the site for xkcd.com?

Question 41 options:

3.94.30.49


10.0.0.0


151.101.192.67


127.0.0.1


10.0.0.172


10.0.0.2

Question 42 (1 point) 
What is the MAC address of the enX0 interface?

Question 42 options:
Question 43 (1 point) 
DNS resolves _______ to _______

Question 43 options:

your grade to an A (and vice versa)


routes to gateways (and vice versa)


MAC addresses to IP addresses (and vice versa)


hostnames to ip addresses (and vice versa)

Question 44 (1 point) 
What is the IPv4 address of the enX0 interface?

Question 44 options:
Page 8 of 10

0 of 50 questions savedBonus
Question 45 (Bonus) (1 point) 
Breakdown and then summarize what the following command does:

pwgen -N 10 -y -1
Yes, `pwgen` is a real program

Question 45 options:
Question 45 options:
Page 9 of 10

Scripting & Commands
Questions in the section may refer to the following bash script named `validate.sh`:

#!/bin/bash

pattern="^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$"

usage() {
    echo "Usage: $0 -s <string> [-p <pattern>]"
    echo "  -s  Input string to validate"
    echo "  -p  (Optional) Regex pattern to use"
    exit 1
}

while getopts "s:p:" opt; do
    case "$opt" in
        s) input="$OPTARG" ;;
        p) pattern="$OPTARG" ;;
        *) usage ;;
    esac
done

if [ -z "$input" ]; then
    usage
fi

if [[ "$input" =~ $pattern ]]; then
    echo "✅ Valid input: '$input'"
else
    echo "❌ Invalid input: '$input'"
fi
Question 46 (1 point) 
Provide a NON-match to the regex pattern initialized in the variable pattern

Question 46 options:
Question 47 (1 point) 
Provide a match to the regex pattern initialized in the variable pattern

Question 47 options:
Question 48 (1 point) 
Running the script with:

bash validate.sh -s
# OR 
bash validate.sh -n 
Would print the usage guide and exit the process

Question 48 options:
	True
	False
Question 49 (1 point) 
In order for any user to be able to run "validate", select all validate steps that must be completed

Select 3 correct answer(s)
Question 49 options:

the name of the script must be added to the PATH environment variable


the directory the script is located in must be added to the PATH environment variable


the script must be renamed from `validate.sh` to `validate`


all users must be able to edit the script file


the script must be renamed from `validate.sh` to `validate.bash`


all users must be able to execute the script file

Question 50 (1 point) 
Running the script with:

bash validate.sh -s ohio -p '^[\w].*[\d]?'
Would evaluate to true on line 24

Question 50 options:
	True
	False
Page 10 of 10

0 of 50 questions saved
