# syshello
A script for development of Linux system call.

# Usage
First, clone this repo, change the access permissions of setup.sh, and download Linux kernel source code.
```
$ git clone github.com/w-haibara/sysh…
$ cd syshello
$ sudo su
# chmod 755 setup.sh
# ./setup.sh init
```
Write a function of your call to mycall.c. 
When kernel is builded, mycall.c is expanded in last of kernel/sys.c.

Build kernel with your system call by executing ./setup.sh deploy
```
# ./setup.sh deploy
# reboot
```
If succesfully finished build, you can check the message from your system call. 
```
$ cd ./syshello
$ gcc mycallTest.c
$ ./a.out
$ dmesg | grep hello
```
