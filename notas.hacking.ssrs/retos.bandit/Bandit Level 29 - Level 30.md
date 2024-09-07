## Objetivo 
There is a git repository at `ssh://bandit29-git@localhost/home/bandit29-git/repo` via the port `2220`. The password for the user `bandit29-git` is the same as for the user `bandit29`.

Clone the repository and find the password for the next level.

## Commands you may need to solve this level

**git**
## Datos de acceso al nivel 
bandit29
Yz9IpL0sBcCeuG7m9uQFt8ZNpS4HZRcN
## Solución  
```bash 
bandit29@bandit:~$ ls -la
total 20
drwxr-xr-x  2 root root 4096 Jul 17 15:56 .
drwxr-xr-x 70 root root 4096 Jul 17 15:58 ..
-rw-r--r--  1 root root  220 Mar 31 08:41 .bash_logout
-rw-r--r--  1 root root 3771 Mar 31 08:41 .bashrc
-rw-r--r--  1 root root  807 Mar 31 08:41 .profile
bandit29@bandit:~$ ls
bandit29@bandit:~$ mktemp -d
/tmp/tmp.JEhg7zOjsP
bandit29@bandit:~$ cd /tmp/tmp.JEhg7zOjsP
bandit29@bandit:/tmp/tmp.JEhg7zOjsP$ ls
bandit29@bandit:/tmp/tmp.JEhg7zOjsP$ /tmp/tmp.JEhg7zOjsP git clone ssh://bandit29-git@localhost:2220/home/bandit29-git/repo
-bash: /tmp/tmp.JEhg7zOjsP: Is a directory
bandit29@bandit:/tmp/tmp.JEhg7zOjsP$ git clone ssh://bandit29-git@localhost:2220/home/bandit29-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit29/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit29/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit29-git@localhost's password:
remote: Enumerating objects: 16, done.
remote: Counting objects: 100% (16/16), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 16 (delta 2), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (16/16), done.
Resolving deltas: 100% (2/2), done.
bandit29@bandit:/tmp/tmp.JEhg7zOjsP$ ls -la
total 10816
drwx------    3 bandit29 bandit29     4096 Sep  7 20:15 .
drwxrwx-wt 7516 root     root     11063296 Sep  7 20:16 ..
drwxrwxr-x    3 bandit29 bandit29     4096 Sep  7 20:16 repo
bandit29@bandit:/tmp/tmp.JEhg7zOjsP$ ls
repo
bandit29@bandit:/tmp/tmp.JEhg7zOjsP$ cat repo
cat: repo: Is a directory
bandit29@bandit:/tmp/tmp.JEhg7zOjsP$ cd repo
bandit29@bandit:/tmp/tmp.JEhg7zOjsP/repo$ ls
README.md
bandit29@bandit:/tmp/tmp.JEhg7zOjsP/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: <no passwords in production!>

bandit29@bandit:/tmp/tmp.JEhg7zOjsP/repo$ git --help
usage: git [-v | --version] [-h | --help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           [--config-env=<name>=<envvar>] <command> [<args>]

These are common Git commands used in various situations:

start a working area (see also: git help tutorial)
   clone     Clone a repository into a new directory
   init      Create an empty Git repository or reinitialize an existing one

work on the current change (see also: git help everyday)
   add       Add file contents to the index
   mv        Move or rename a file, a directory, or a symlink
   restore   Restore working tree files
   rm        Remove files from the working tree and from the index

examine the history and state (see also: git help revisions)
   bisect    Use binary search to find the commit that introduced a bug
   diff      Show changes between commits, commit and working tree, etc
   grep      Print lines matching a pattern
   log       Show commit logs
   show      Show various types of objects
   status    Show the working tree status

grow, mark and tweak your common history
   branch    List, create, or delete branches
   commit    Record changes to the repository
   merge     Join two or more development histories together
   rebase    Reapply commits on top of another base tip
   reset     Reset current HEAD to the specified state
   switch    Switch branches
   tag       Create, list, delete or verify a tag object signed with GPG

collaborate (see also: git help workflows)
   fetch     Download objects and refs from another repository
   pull      Fetch from and integrate with another repository or a local branch
   push      Update remote refs along with associated objects

'git help -a' and 'git help -g' list available subcommands and some
concept guides. See 'git help <command>' or 'git help <concept>'
to read about a specific subcommand or concept.
See 'git help git' for an overview of the system.
bandit29@bandit:/tmp/tmp.JEhg7zOjsP/repo$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/dev
  remotes/origin/master
  remotes/origin/sploits-dev
bandit29@bandit:/tmp/tmp.JEhg7zOjsP/repo$ git branch -r
  origin/HEAD -> origin/master
  origin/dev
  origin/master
  origin/sploits-dev
bandit29@bandit:/tmp/tmp.JEhg7zOjsP/repo$ git checkout dev
branch 'dev' set up to track 'origin/dev'.
Switched to a new branch 'dev'
bandit29@bandit:/tmp/tmp.JEhg7zOjsP/repo$ git log
commit eef534022d1ecc3b41d6de068501c4db4154b2c7 (HEAD -> dev, origin/dev)
Author: Morla Porla <morla@overthewire.org>
Date:   Wed Jul 17 15:57:31 2024 +0000

    add data needed for development

commit 301cf80fd7d0012c519077fcc5e1568cda8e4b8e
Author: Ben Dover <noone@overthewire.org>
Date:   Wed Jul 17 15:57:31 2024 +0000

    add gif2ascii

commit efa5bd803f8335e5e5e9da5c4c7c876aefc9f8b4 (origin/master, origin/HEAD,
 master)
Author: Ben Dover <noone@overthewire.org>
Date:   Wed Jul 17 15:57:31 2024 +0000

    fix username

commit 5a53eb83a43bac1f0b4e223e469b40ef68a4b6e6
Author: Ben Dover <noone@overthewire.org>
Date:   Wed Jul 17 15:57:31 2024 +0000

    initial commit of README.md
bandit29@bandit:/tmp/tmp.JEhg7zOjsP/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: qp30ex3VLz5MDG1n91YowTv4Q8l7CDZL
```



## Notas Adicionales 



### Referencias
