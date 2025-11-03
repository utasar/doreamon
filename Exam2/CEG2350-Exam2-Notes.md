# CEG 2350 – Exam 2 Study Notes

---

## ✅ Shells
| OS | Common Shells |
|----|---------------|
| Linux | bash, sh, zsh |
| macOS | bash, zsh |
| Windows | PowerShell, cmd |

### SSH
```bash
ssh user@hostname
✅ Private Key: ~/.ssh/id_rsa (must be permission 600)
✅ Public Key: ~/.ssh/id_rsa.pub
✅ Remote authorized keys file: ~/.ssh/authorized_keys

✅ Files & Directories
Common Commands
ls    cp    mv    rm    mkdir    rmdir
cd    pwd   cat   touch head     tail
less  more  ln

Linux Filesystem Structure
Directory	What it Stores
/	Root of everything
/home	User files
/etc	Configuration
/var	Logs + app runtime data
/bin, /usr/bin	Commands & binaries
/dev	Device files
/tmp	Temporary files
✅ File Permissions & Ownership
Symbol	Meaning
r	read
w	write
x	execute
Class	Applies To
u	user/owner
g	group
o	others
Commands
chmod 755 file
chown user:user file
sudo command

✅ Bash Scripting
Variables & Printing
name="Utsav"
echo $name

Arguments
echo $1 $2 $@

Conditions
if [ "$x" -gt 5 ]; then
  echo "big"
fi

Loops
for i in 1 2 3; do echo $i; done

Functions
f() { echo "hello"; }

✅ Environment Setup
Variable	Purpose
PATH	Search path for commands
HOME	User home directory
SHELL	Default shell
USER	Username

Customization files:

~/.bashrc

~/.profile

Create aliases in .bashrc

✅ Redirection & Pipes
Symbol	Meaning
>	redirect output (overwrite)
>>	append output
<	redirect input
`	`
tee	show + save output
✅ Regex and Text Tools
grep "text" file
sed 's/old/new/g'
awk '{print $1}'
wc -l file
sort file
uniq file
find / -name "*.txt"

✅ Hardware & VMs
Component	Role
CPU	Executes instructions
RAM	Fast temp memory
Disk	Long-term storage
GPU	Graphics compute
Motherboard	Connects everything
Hypervisors

Runs virtual machines (VMs)

VM is guest OS inside host OS

✅ Boot Process (Linux)

1️⃣ BIOS/UEFI
2️⃣ POST
3️⃣ Bootloader (GRUB)
4️⃣ Kernel loads
5️⃣ init / systemd starts services

✅ Storage: Disks & Filesystems

Tools:

fdisk
parted
gdisk


Mounting:

mount /dev/sda1 /mnt
umount /mnt


Auto mount on boot:
/etc/fstab

✅ Linux Processes
Key Terms
Term	Meaning
Process	Running program
PID	Process ID
PPID	Parent process ID
Daemon	Background system service

➡ Every process is created using fork + exec
➡ If parent dies → orphan adopted by init/systemd

States
Code	Meaning
R	Running
S	Sleeping
T	Stopped (Ctrl+Z)
D	Uninterruptible sleep
Z	Zombie
Process Commands
ps aux
pgrep NAME
top
htop

Foreground / Background Control
sleep 100 &
jobs
fg %1
bg %1


Stop with:

Ctrl+Z (SIGTSTP)

Bring to foreground:

fg %job

Signals & kill
Signal	Command	Meaning
SIGTERM	kill -15 PID	Graceful stop
SIGINT	kill -2 PID	Interrupt (Ctrl+C)
SIGHUP	kill -1 PID	Restart/reload
SIGKILL	kill -9 PID	Force stop — cannot be blocked
SIGSTOP	kill -19 PID	Pause process
SIGCONT	kill -18 PID	Continue
kill -9 1234

tmux (Keeps programs alive)

Start session:

tmux new -s exam


Detach: Ctrl+B, then D
List:

tmux ls


Reattach:

tmux attach -t exam

✅ Services (systemd)
Task	Command
Status	systemctl status ssh
Start / Stop	systemctl start ssh / systemctl stop ssh
Restart	systemctl restart ssh
Auto-start at boot	systemctl enable ssh

Logs:

journalctl -u ssh
