Question 1 (2 points) 
Given the following regex pattern:

^[c][ake]{3}\s\$\d{2}\.\d{2}$

In the first blank give a string that WILL match

In the second blank give string that will NOT match
✅ **Match:** `cake $12.50`  
❌ **Does not match:** `cak $12.5`

Question 1 options:
Question 2 (1 point) 
Given:

hello.md
hello.txt
hello.mat
README.txt
foo.sh
foo.m
bar?md
.txt.md
.txt.foo
.md.mat
hello.md.bak
Which regular expression will match only files ending in .md?

Question 2 options:

\.md$


\.[^txt]


\.md


\.[md]


.md$
**Answer:** `\.md$`  
**Explanation:** Matches files ending with `.md`

Question 3 (Bonus) (1 point) 
[BONUS] Detail all parts, and the result of running, the following command.  Score will be all or nothing.

cd "$(dirname "$(find ~ -type f -name README.md | head -1)")"
Question 3 options:
Question 4 (1 point) 
Clients authenticating or connecting via SSH need to have a ___ key file to authenticate to the remote user account

Question 4 options:

public


protected


constrained


private

Question 5 (1 point) 
For Ubuntu Linux, what is the default shell?

Question 5 options:

PowerShell


bash


cmd


sh


zsh

Question 6 (1 point) 
Remote user accounts that clients authenticate and connect to via SSH need to have a ___ key stored in the remote user's authorized_keys file

Question 6 options:

protected


prorated


private


public

Question 7 (1 point) 
Given the following command:

ssh -i .\labkey.pem jsmith@fry.wright.edu
Is the path to the private key file relative or absolute?

Question 7 options:

relative


absolute

Question 8 (1 point) 
Given the following command:

ssh -i .\labkey.pem jsmith@fry.wright.edu
What is the hostname of the remote system?

Question 8 options:
Question 9 (1 point) 
Given the following command:

ssh -i .\labkey.pem jsmith@fry.wright.edu
What is the name of the private key file used for authentication?

Question 9 options:
Question 10 (1 point) 
Given the following command:

ssh -i .\labkey.pem jsmith@fry.wright.edu
What is the username on the remote system?

Question 10 options:
 
Given the following command:

ssh -i .\labkey.pem jsmith@fry.wright.edu
What does the -i flag allow specification of?

Question 11 options:

Identity File (a private key file must be specified afterwards if a non-default name is used in a non-default location)


Verbosity (outputs debug log information about the connection attempt)


Login name (the user to log in as on the remote machine)

Question 12 (1 point) 
If a file contains markdown syntax, what extension notifies applications to render the markdown formatting?

Question 12 options:

.txt


.sh


.md


.docx

Question 13 (1 point) 
I have a repository on GitHub, but do not have a copy of the repository locally on the system I am using.  Assuming SSH authentication with my GitHub account has been set up, what is my next step?

Question 13 options:

git clone repo_URL


git commit repo_URL


git add repo_URL


git pull


git push

Question 14 (1 point) 
A user is working in a git repository folder cloned from GitHub and wants to synchronize their changes to main.java to the GitHub repository.  The output of `git status` is:

On branch main
Your branch is ahead of 'origin/main' by 3 commits.
 (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
  modified: main.java
What commands are needed to synchronize the latest changes in main.java with the GitHub repository?

Question 14 options:
Question 15 (1 point) 
In order to create passwordless SSH authentication with GitHub, we set up SSH authentication on the system using ssh-keygen to create a key pair. 

What is an accurate path to the private key file used for authentication?

Question 15 options:

~/labsuser.pem


~/.ssh/id_ed25519


None of the above


~/keyfile


~/.ssh/id_ed25519.pubQuestion 16 (1 point) 
 Saved
In order to create passwordless SSH authentication with GitHub, we set up SSH authentication on the system using ssh-keygen to create a key pair. 

Which key was added to your GitHub account settings?

Question 16 options:

private key (contents of id_ed25519)


public key (contents of id_ed25519.pub)

Question 17 (1 point) 
 Saved
I created a new file, used `git add file` to track it, used `git commit` to commit my changes in my repo, but on git push I get the following output:

To github.com:pattonsgirl/Spring2022-CEG2350.git
! [rejected]  main (fetch first)
error: failed to push some refs to 'git@github.com:pattonsgirl/Spring2022-CEG2350.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
What command do I need to run next?

Question 17 options:

git pull


git push


git status


git add .


git commit -a

Question 18 (2 points) 
Select true facts about the PATH environment variable

Question 18 options:

used by the system to search through directories in hierarchical order by looking first at directories closest to / (root)


can view value with either `echo PATH` or `printenv $PATH`


can view value with either `echo $PATH` or `printenv PATH`


consists of absolute paths to directories where executables are located


consists of parent directories.  The subdirectory where an executable is located does not need to be specified


uses any symbol as a separator between entries as long as it is consistent, including , ; and /


uses : as a separator


used by system to search through directories in order listed in PATH for an executable that matches the command entered

Question 19 (1 point) 
I have a few aliases that work in my bash shell I want to use persistently instead of setting them up each time I log on.  What file should I enter these aliases in?

Question 19 options:

.git


.profile


.bashrc


.vimrc


.

Question 20 (1 point) 
Fix the following command so that it does search current user's home directory for files named README.md

find README.md ~Question 21 (1 point) 
What does the following command do?

ls ..

Question 21 options:

lists the contents of a directory named ".."


lists the contents of the parent directory relative to the directory you are in


lists the contents of the current directory


lists the hidden files in the current directory

Question 22 (1 point) 
Which of the following will check if the folder exists before creating a file in it?

Question 22 options:

echo "Provide a folder and I'll make you a file!"
read dir

if [[ -d $dir ]]
then
        echo "As promised" > $dir/toldya.txt
else
        echo "Directory does not exist"
fi


echo "Provide a folder and I'll make you a file!"
read dir

if (( -z $dir ))
then
        echo "As promised" < $dir/toldya.txt
else
        echo "Directory does not exist"
fi


echo "Provide a folder and I'll make you a file!"
read dir

if [[ -d dir ]]
then
        echo "As promised" > dir/toldya.txt
else
        echo "Directory does not exist"
fi


echo "Provide a folder and I'll make you a file!"
read dir

if [[ -e $dir ]]
then
        echo "As promised" > $dir/toldya.txt
else
        echo "Directory does not exist"
fi

Question 23 (1 point) 
Given the following information:

A bash script with the interpreter declared located in the ubuntu user's home directory (/home/ubuntu/) and that the current user is ubuntu

The permissions are as follows:

-rw-rw-r--  1 ubuntu devs  197 Feb  4 21:03 tasktrack
And that the value of PATH is:

/home/ubuntu/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
 Select all valid ways to run the script:

Question 23 options:

/home/ubuntu/tasktrack


tasktrack


bash tasktrack


./tasktrack

Question 24 (1 point) 
I have a script that prints hello to standard output.  It has the following permission set:

-rw-rw---- 1 kduncan kduncan 11 Mar  6 21:14 bar.sh

I can run this script by typing:
./bar.sh

OR

/home/kduncan/bar.sh

Question 24 options:
	True
	False
Question 25 (1 point) 
What does the following script do?

#!/bin/bash
c=$2
if [ "$c" -eq 3 ]; then
    echo "Bubbles."
fi
Question 25 options:
Page 5 of 7

7 of 32 queQuestion 26 (1 point) 
Given the following information:

A bash script with the interpreter declared located in the ubuntu user's home directory (/home/ubuntu/) and that the current user is ubuntu

The permissions are as follows:

-rwxrw-r--  1 ubuntu devs  197 Feb  4 21:03 tasktrack
And that the value of PATH is:

/home/ubuntu:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
 Select all valid ways to run the script:

Question 26 options:

/home/ubuntu/tasktrack


tasktrack


./tasktrack


bash tasktrack

Question 27 (2 points) 
Given the following script named `checker`

```

#!/bin/bash
c=$2
if [ "$c" -eq 3 ]; then
    echo "Bubbles."
fi

```

Provide an example of CORRECTLY using the script to meet the condition in the FIRST blank

Provide an example of INCORRECTLY using the script to meet the condition in the SECOND blank

Question 27 options:
Question 28 (1 point) 
Which of the following will let a non-root account use root privileges to override "Permission denied" errors for a given command? 

Assume the non-root account is a member of the required group to enable to command's usage.

Question 28 options:

root command


sudo command


cd command


su command

Question 29 (1 point) 
Given the following information about a file:

-rw-rw-r-- 1 jsmith devs 0 Feb 24 13:29 test.txt
And the following information about the devs group:

$ getent group devs
devs:x:1003:kduncan,scole,ssmith,froberts
The user jsnow can edit test.txt

Question 29 options:
	True
	False
Question 30 (1 point) 
Choose the command that will add the user jsmith to the group friends

Question 30 options:

usermod -a -G jsmith friends

chgrp jsmith friends

chgrp friends jsmith

usermod -a -G friends jsmith
 
jsmith needs access to read and edit a file in the user sjane's home folder.  Which of the following setups provide the least additional privileges?

Question 31 options:

add jsmith to the sudo users group


allow all users access to sjane's folder (read and execute) and give all users access to read and edit the file


add jsmith to a group, allow the group access (read and execute permissions) to sjane's folder, allow that group read and write access to the required file in sjane's folder


add jsmith to a group, allow the group access (read and execute permissions) to sjane's folder, then allow that group read and write access to all files and subdirectories in sjane's folder (recursively)

Question 32 (1 point) 
Find the matching permission translation for the following command:

chmod 436 banana.md
Question 32 options:

user = read write; group = write execute; other = write


user = read; group = write execute; other = read write


user = execute; group = read; other = read write


user = read; group = read write; other = read execute

