# Ubuntu Basics — Commands & Tips (Quick Reference)

## Assumptions
- Ubuntu 20.04+
- bash shell
- sudo access

## Limitations
- CLI only
- Desktop/server differences ignored
- No distro-specific extras

---

## System
Check OS:
    lsb_release -a

Kernel:
    uname -a

Uptime:
    uptime

---

## Packages (APT)
Update:
    sudo apt update

Upgrade:
    sudo apt upgrade

Full upgrade:
    sudo apt full-upgrade

Install:
    sudo apt install package

Remove:
    sudo apt remove package
    sudo apt purge package

Cleanup:
    sudo apt autoremove
    sudo apt autoclean

---

## Files & Directories
List:
    ls
    ls -la

Change dir:
    cd path
    cd ..
    cd ~

Create dir:
    mkdir dir
    mkdir -p a/b/c

Remove:
    rm file
    rm -r dir
    rm -rf dir

Copy / Move:
    cp src dst
    mv src dst

Disk usage:
    df -h
    du -sh *

---

## View & Edit Files
View:
    cat file
    less file

Head / Tail:
    head file
    tail -f logfile

Edit:
    nano file
    vim file

---

## Permissions
Change mode:
    chmod 755 file
    chmod +x script.sh

Change owner:
    sudo chown user:group file

Notes:
- r = read, w = write, x = execute
- 755 = rwx r-x r-x

---

## Users & Sudo
Current user:
    whoami

Add user:
    sudo adduser username

Grant sudo:
    sudo usermod -aG sudo username

Switch user:
    su - username

---

## Networking
IP info:
    ip a

Connectivity:
    ping google.com

Open ports:
    ss -tulpn

Download:
    wget url
    curl -O url

---

## Processes
List:
    ps aux
    top
    htop

Kill:
    kill PID
    kill -9 PID

Memory:
    free -h

---

## Search
Find files:
    find /path -name "*.log"

Search text:
    grep "text" file
    grep -R "text" dir

---

## Archives
Tar:
    tar -czvf file.tar.gz dir
    tar -xzvf file.tar.gz

Zip:
    zip -r file.zip dir
    unzip file.zip

---

## Environment
Show vars:
    printenv
    echo $PATH

Set var:
    export VAR=value

Reload shell:
    source ~/.bashrc

---

## Services (systemd)
Status:
    systemctl status service

Start / Stop:
    sudo systemctl start service
    sudo systemctl stop service

Enable at boot:
    sudo systemctl enable service

---

## Logs
All logs:
    journalctl

Errors:
    journalctl -xe

Service logs:
    journalctl -u service

---

## Shortcuts
- Ctrl+C → stop
- Ctrl+Z → pause
- Ctrl+R → history search
- !! → rerun last command with sudo
- Tab → autocomplete

---

## Common Failures
Command not found:
- Install package
- Check PATH

Permission denied:
- Use sudo
- Fix chmod/chown

APT locked:
    sudo rm /var/lib/apt/lists/lock
    sudo rm /var/cache/apt/archives/lock
    sudo dpkg --configure -a

---

## Verification
- apt works: sudo apt update
- disk ok: df -h
- network ok: ping
- user ok: whoami
- services ok: systemctl status

---

## Safety
- Never run rm -rf /
- Avoid curl | bash
- Daily work as non-root
- Backup before upgrades
