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
