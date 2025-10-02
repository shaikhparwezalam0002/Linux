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

# How to create a folder/directory

```bash
    mkdir [path/directory-name]
```

# How to create file

```bash
dev-member@QC-SUPPORT:~/demo$ touch ./demo.txt
dev-member@QC-SUPPORT:~/demo$ ls
demo.txt  test.txt
```

# How to remove fil

```bash
dev-member@QC-SUPPORT:~/demo$ rm -v ./demo.txt
removed './demo.txt'
```

# How to read the file

```bash
dev-member@QC-SUPPORT:~/demo$ cat test.txt
```

```bash
dev-member@QC-SUPPORT:~/demo$ nano demoFile.txt #to write in the demoFile.txt
dev-member@QC-SUPPORT:~/demo$ less demoFile.txt # to see the file content.
dev-member@QC-SUPPORT:~/demo$ more demoFile.txt # to see the file content...
```

# How t change the directory

```bash 
dev-member@QC-SUPPORT:~/demo$ pwd
>>/home/dev-member/demo
dev-member@QC-SUPPORT:~/demo$ cd ..
dev-member@QC-SUPPORT:~$ pwd
>>/home/dev-member
```

# How to move to the root directory

```bash
dev-member@QC-SUPPORT:/$ ls
bin                boot  etc   init  lib.usr-is-merged  lost+found  mnt  proc  run   sbin.usr-is-merged  srv  tmp  var
bin.usr-is-merged  dev   home  lib   lib64              media       opt  root  sbin  snap                sys  usr
```

# how to copy a file from one path to different

```bash

syntax:
dev-member@QC-SUPPORT:~/DevOpsLrn$ cp [FileName] [Destination-Path]

dev-member@QC-SUPPORT:~$ ls
DevOpsLrn  demo  file.txt  text.txt
dev-member@QC-SUPPORT:~$ cd DevOpsLrn
dev-member@QC-SUPPORT:~/DevOpsLrn$ ls
file.txt
dev-member@QC-SUPPORT:~/DevOpsLrn$ pwd
/home/dev-member/DevOpsLrn
dev-member@QC-SUPPORT:~/DevOpsLrn$ cp file.txt /home/dev-member/
dev-member@QC-SUPPORT:~/DevOpsLrn$ ls
file.txt
dev-member@QC-SUPPORT:~/DevOpsLrn$ cd ..
dev-member@QC-SUPPORT:~$ ls
DevOpsLrn  demo  file.txt  text.txt
```

# How to copy of a filcontent to another file

```bash
dev-member@QC-SUPPORT:~$ ls
DevOpsLrn  demo  file.txt  text.txt
dev-member@QC-SUPPORT:~$ cat text.txt
Hello
dev-member@QC-SUPPORT:~$ cp text.txt test1.txt
dev-member@QC-SUPPORT:~$ cat test1.txt
Hello

1.cp [EXISTING-FILE-NAME] [NEW-FILE-NAME]

if the file name or file already exists then it will override it's content.
```

# How to cut / move a file 

```bash
 mv [FILE-NAME] [DESTINATION]
```

# It will list all the file in reverse order.

```bash
dev-member@QC-SUPPORT:~/DevOpsLrn$ ls -r
text.txt  file.txt
```

# How to rename a file

```bash
dev-member@QC-SUPPORT:~/DevOpsLrn$ ls
file.txt  text.txt
dev-member@QC-SUPPORT:~/DevOpsLrn$ mv text.txt test.txt
dev-member@QC-SUPPORT:~/DevOpsLrn$ ls
file.txt  test.txt
```

# How to read top 5 lines from a file.

```bash
dev-member@QC-SUPPORT:~/DevOpsLrn$ cat file.txt
Hello, I want to create file
this is the 2nd line of the file.
dev-member@QC-SUPPORT:~/DevOpsLrn$ head -1 file.txt
Hello, I want to create file

Syntax: head -[no of lines] [File Name]
```

# How to read line of contents from a file.

```bash
dev-member@QC-SUPPORT:~/DevOpsLrn$ cat test.txt
Hello Team,

        Be available for weakends.
dev-member@QC-SUPPORT:~/DevOpsLrn$ tail -1 test.txt
        Be available for weakends.
```

# How to search some content in a file 

```bash
dev-member@QC-SUPPORT:~/DevOpsLrn$ cat test.txt
Hello Team,

        Be available for weakends.
dev-member@QC-SUPPORT:~/DevOpsLrn$ grep "team" test.txt -i # -i for case sensitive
Hello Team,
```

# How to search multiple values in a file 

```bash
dev-member@QC-SUPPORT:~/DevOpsLrn$ cat test.txt
Hello Team,

        Be available for weakends.
dev-member@QC-SUPPORT:~/DevOpsLrn$ egrep "team|ends" test.txt -i
Hello Team,
        Be available for weakends.`bash


SYNTAX : egrep [VAL1 | VAL2] [FILE_NAME]
```

# How to search a particular file start name or extension name

```bash
$ ls li* #file name starts with li
$ ls *.csv #file should be .csv 
```

# How to create file in a single patter in multiple file

```bash
dev-member@QC-SUPPORT:~/DevOpsLrn$ touch filesh{1..5}.txt
dev-member@QC-SUPPORT:~/DevOpsLrn$ ls
file.txt  filesh1.txt  filesh2.txt  filesh3.txt  filesh4.txt  filesh5.txt  test.txt
```

# How to count the number of line present in a file.

```bash
dev-member@QC-SUPPORT:~/DevOpsLrn$ wc -l test.txt
3 test.txt
```

# how to compare two file content in linux

```bash
dev-member@QC-SUPPORT:~$ ls
DevOpsLrn  demo  file1.txt  file2.txt  test1.txt
dev-member@QC-SUPPORT:~$ cat file1.txt
Hello, I want to create file
This is the 2nd line of the file.
Adding new Line.
dev-member@QC-SUPPORT:~$ cat file2.txt
Hello, I want to create file
this is the 2nd line of the file.
dev-member@QC-SUPPORT:~$ cmp file1.txt file2.txt
file1.txt file2.txt differ: byte 30, line 2

- if file is identical no output is return 
```

# How to read the manual of the command

```bash
dev-member@QC-SUPPORT:~$ man mkdir
dev-member@QC-SUPPORT:~$ man rmdir
```

# CHMOD File permissions

```bash
Every file in Linux has the following 3 permissions associated:

1. Read - We can only read a file - Denoted as `R`

2. Write - We can edit a file content - Denoted as `W`

3. Execute - We can execute the file - Denoted as `x`

We can make a file get any combination of permissions i.e. READ WRITE, or READ EXECUTE, OR WRITE, OR EXECUTE, OR READ WRITE EXECUTE and so on.
So a file can may be have all these 3 permissions or a subset of them.

These permissions are associated on different level of ownership. Ownership is based on level, that is includes:

1. users who owns the file

2. user group that owns the file

3. other users who has access to the system

4. all the users of the system.

Note : File any user of the machine we can separetly define what permission they have, like owner of the file can read, write and execute, may be others can only read.

For these permission we have 2 commands

1. chmod # this command helps us to change the permission of a file and directory.
2. chown # this command will help us to change the ownership of the file and directory.
```

# How to play with permission of a file and directory.

```bash
 How to change a user permission

 1. Symbolic Way

 Syntax : chmod [User][Operator][Permission] [FileName]
 User type:
  u - user
  g - group 
  o - others
  a - all

  Operator type:
   + >> for adding the permission 
   - >> for removing the permission
   = >> for adding the perticular permission and removing existing permissions.

   Permission types:
    r - read
    w - write
    x - execute

   Example:
    dev-member@QC-SUPPORT:~$ chmod u+x linux.sh
    dev-member@QC-SUPPORT:~$ chmod g-x g+w test1.txt
    dev-member@QC-SUPPORT:~$ chmod g+x test1.txt
    dev-member@QC-SUPPORT:~$ chmod g-w test1.txt
 2. Numeric Way
    we have range [0-7] and 
    for read - 100 - 4
    for write,execute - 011 - 3
    for read , write, execute - 111 - 7 
    for read , execute - 101 - 5 and so on.

   Syntax : chmod [Numberic(0-7 u)(0-7 g)(0-7 a)] [File Name] 
   Example:
   
    -rw-rw-r-- 1 dev-member dev-member    0 Oct  2 20:19 linux.sh
     # Now we have for user and group have read & write access and others have only read access
    dev-member@QC-SUPPORT:~$ chmod 755 linux.sh
     # for user -7 
     # for group -5 
     # for other -5
```

# CHOWN THIS COMMAND HELP TO MANANGE THE OWNERSHIP OF A DIRECTORY/FILE.

```bash
Syntax : chmod [user/owner] [:group] [FileName]
-rwxr-xr-x 1 dev-member dev-member    0 Oct  2 20:19 linux.sh
dev-member@QC-SUPPORT:~$ sudo chown :developer linux.sh 
-rwxr-xr-x 1 dev-member developer     0 Oct  2 20:19 linux.sh
```

# System Monitoring Commands

# DF COMMAND 

```bash
 #used to display the disk value 
 #and for the manual you can use `man df`
 #to read the data in human understandable add flag `-h` and hidden `-a`

 dev-member@QC-SUPPORT:~$ df
 dev-member@QC-SUPPORT:~$ df -h -a
 # -h for humand readable format
 # -a for hidden files as well
 dev-member@QC-SUPPORT:~$ df -h
 
```
![Disk Details](/image/image.png)

# DU COMMANDS

```bash
# it display the disk uses of all the folder/directory
dev-member@QC-SUPPORT:~$ du

# it display the disk uses of all the folder/directory in human readable format
dev-member@QC-SUPPORT:~$ du -h

# It display a particular folder disk uses in the system.
dev-member@QC-SUPPORT:~$ du -h DevOpsLrn
8.0K    DevOpsLrn
```
![disk uses by a ](/image/image1.png)
![disk uses by a ](/image/image2.png)