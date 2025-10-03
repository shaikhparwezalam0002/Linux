*Name : Shaikh Parwez Alam*
*Email : shaikhparwez0002@gmail.com*
*Github : https://supreme-space-winner-4pp67qpr7rc96v.github.dev/*

# 1. What is Linux ?
*Linux is a kernel is not an OS.*

# 2. What is the difference between Hard Link & Soft Link?
```bash
- Hard link
    1. Both file shared same inode. 
    2. If the original file can be deleted, the content of the file is still be visible and stored in the system.
    3. syntax : ln test.txt newTest.txt

- Soft link
    1. Both file shared different inode.
    2. If the source file/original file is deleted, then content of the file also deleted.
    3. syntax : ln -s test.txt newTest.txt
```
# 3. What is a Kernel in Linux ?

*Main source of the OS. It is free and open source.*

# 4. How do you create a user account?

```bash
dev-member@SUPT:~/DevOpsLrn$ sudo adduser "jhon-doe"
[sudo] password for dev-member:
info: Adding user `jhon-doe' ...
info: Selecting UID/GID from range 1000 to 59999 ...
info: Adding new group `jhon-doe' (1003) ...
info: Adding new user `jhon-doe' (1003) with group `jhon-doe (1003)' ...
info: Creating home directory `/home/jhon-doe' ...
info: Copying files from `/etc/skel' ...
New password:
Retype new password:
passwd: password updated successfully
Changing the user information for jhon-doe
Enter the new value, or press ENTER for the default
        Full Name []: Jhon Doe
        Room Number []:
        Work Phone []:
        Home Phone []:
        Other []:
Is the information correct? [Y/n] Y
info: Adding new user `jhon-doe' to supplemental / extra groups `users' ...
info: Adding user `jhon-doe' to group `users' ...
```
# 5. What is the ‘grep’ command used for in Linux ?

```bash
# used for searching in a file.
dev-member@SUPPORT:~$ cat test1.txt
Hello Team,

        Be available for weakends.

dev-member@SUPPORT:~$ grep "weak" -i test1.txt
        Be available for weakends.
```

# 6. Step1: Create user p1
# Step2: He should be part of 3 groups g1,g2,g3.
# Step3: whenever he creates a file automatically in the group section of file grp g1 should come.

```bash
# Group 1 is created.
dev-member@SUPPORT:~$ sudo addgroup g1  
info: Selecting GID from range 1000 to 59999 ...
info: Adding group `g1' (GID 1005) ...
# Group 2 is created.
dev-member@SUPPORT:~$ sudo addgroup g2
info: Selecting GID from range 1000 to 59999 ...
info: Adding group `g2' (GID 1006) ...
# Group 3 is created.
dev-member@SUPPORT:~$ sudo addgroup g3
info: Selecting GID from range 1000 to 59999 ...
info: Adding group `g3' (GID 1007) ...
# list all the groups
dev-member@SUPPORT:~$ cat /etc/group
g1:x:1005:
g2:x:1006:
g3:x:1007:
#created user p1
dev-member@SUPPORT:~$ sudo adduser p1
info: Adding user `p1' ...
info: Selecting UID/GID from range 1000 to 59999 ...
info: Adding new group `p1' (1008) ...
info: Adding new user `p1' (1008) with group `p1 (1008)' ...
info: Creating home directory `/home/p1' ...
info: Copying files from `/etc/skel' ...
New password:
Retype new password:
passwd: password updated successfully
Changing the user information for p1
Enter the new value, or press ENTER for the default
        Full Name []: AssignmentNo6
        Room Number []:
        Work Phone []:
        Home Phone []:
        Other []:
Is the information correct? [Y/n] Y
info: Adding new user `p1' to supplemental / extra groups `users' ...
info: Adding user `p1' to group `users' ...
# assign groups to p1 user
dev-member@SUPPORT:~$ sudo usermod -aG g1 p1
dev-member@SUPPORT:~$ sudo usermod -aG g2 p1
dev-member@SUPPORT:~$ sudo usermod -aG g3 p1
#print what are the groups associated with p1 user
dev-member@SUPPORT:~$ groups p1
p1 : p1 users g1 g2 g3
```

# 7. Step1: Create directory /tmp/bg as root user and create files inside it. Step2: “abhi” should be the owner of the directory. He should be able to create files and delete files inside the directory and also he should be able to add content to all files inside the directory.

```bash
dev-member@SUPPORT:/tmp/bg$ touch demo.txt
dev-member@SUPPORT:/tmp/bg$ ls -lh
total 0
-rw-r--r-- 1 dev-member dev-member 0 Oct  3 20:31 demo.txt
dev-member@SUPPORT:/tmp/bg$ sudo chown abhi demo.txt
dev-member@SUPPORT:/tmp/bg$ ls -lh
total 0
-rw-r--r-- 1 abhi dev-member 0 Oct  3 20:31 demo.txt
dev-member@SUPPORT:/tmp/bg$ su abhi
Password:
abhi@SUPPORT:/tmp/bg$ chmod u+x demo.txt
abhi@SUPPORT:/tmp/bg$ ls -lh
total 0
-rwxr--r-- 1 abhi dev-member 0 Oct  3 20:31 demo.txt
abhi@SUPPORT:/tmp/bg$ vi demo.txt
abhi@SUPPORT:/tmp/bg$ cat demo.txt
Hello
```

# 8. You suspect that a particular process is consuming excessive CPU resources on your Linux server. How would you identify and terminate this process?

```bash
dev-member@SUPPORT:~$ top
dev-member@SUPPORT:~$ sudo kill 9 903
```