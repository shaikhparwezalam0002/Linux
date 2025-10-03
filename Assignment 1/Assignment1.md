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
# 4. What is the ‘grep’ command used for in Linux ?

```bash
# used for searching in a file.
dev-member@SUPPORT:~$ cat test1.txt
Hello Team,

        Be available for weakends.

dev-member@SUPPORT:~$ grep "weak" -i test1.txt
        Be available for weakends.
```