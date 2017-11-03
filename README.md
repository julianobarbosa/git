# configure
git config --global merge.tool p4merge
git config --global mergetool.prompt false
git config --global mergetool.keepbackup false
git config --global mergetool.keeptemporaries false


# Add users
Setup SSH:
```console
cd /docker_data/git
mkdir .ssh
chown -R 987:987 .ssh
chmod -R 700 .ssh
touch .ssh/authorized_keys
chmod 600 .ssh/authorized_keys
```

Add user public keys to .ssh/authorized_keys just like you would do for 'normal' SSH.

touch /docker_data/git/.hushlogin to prevent login banners that can confuse git.

# Setup repos

```console
mkdir /docker_data/git/mynewproject.git
cd /docker_data/git/mynewproject.git
git --bare init
chown -R 987:987 .
```

Clone the repo from a client:

```console
git clone ssh://git@myserver:2222/git/mynewproject.git
```

# Setup git-shell-commands

```console
mkdir /docker_data/git/git-shell-commands
chown 987:987 /docker_data/git/git-shell-commands
chmod 700 /docker_data/git/git-shell-commands
```
# List .gitignore
git ls-files --others --ignored --exclude-standard


# Ref:
https://www.perforce.com/downloads/visual-merge-tool

# /usr/local/bin
```console
#!/bin/bash
/opt/p4merge/bin/p4merge
```
