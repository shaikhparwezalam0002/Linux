# Linux is a kernel not an os.
# It is a main source of an OS.

# How to check the current directory where you are working 
```bash
    dev-member@QC-SUPPORT:~$ pwd
    /home/dev-member
```

# How to check the current system date

```bash
dev-member@QC-SUPPORT:~$ date +%D
09/28/25
dev-member@QC-SUPPORT:~$ date +%T
12:49:47
dev-member@QC-SUPPORT:~$ date +%H:%M
12:52
```

# list of all the list
```bash
dev-member@QC-SUPPORT:~$ ls
DevOpsLrn  demo  logger.log  text.txt

dev-member@QC-SUPPORT:~$ ls -lt
total 16
-rw-rw-r-- 1 dev-member dev-member  278 Sep 28 12:55 logger.log
-rwxr-xr-x 1 dev-member dev-member    6 Sep 28 08:45 text.txt
drwxrwxr-x 2 dev-member dev-member 4096 Sep 28 08:33 demo
drw-r--r-- 2 dev-member dev-member 4096 Sep 27 20:29 DevOpsLrn

dev-member@QC-SUPPORT:~$ ls -lh
total 16K
drw-r--r-- 2 dev-member dev-member 4.0K Sep 27 20:29 DevOpsLrn
drwxrwxr-x 2 dev-member dev-member 4.0K Sep 28 08:33 demo
-rw-rw-r-- 1 dev-member dev-member  278 Sep 28 12:55 logger.log
-rwxr-xr-x 1 dev-member dev-member    6 Sep 28 08:45 text.txt
```