# System-Call

Want to create yoyr own System Call, refer this [article...](https://medium.com/anubhav-shrimal/adding-a-hello-world-system-call-to-linux-kernel-dad32875872)

## What is System Call ?
When you run a program which calls `open`, `fork`, `read`, `write` (and many others) you are making a system call.
System calls are how a program enters the kernel to perform some task. Programs use system calls to perform a variety of operations such as: creating processes, doing network and file IO, and much more.

You can find a list of system calls from [here](http://man7.org/linux/man-pages/man2/syscalls.2.html).

There are several different ways for user programs to make system calls and the low-level instructions for making a system call vary among CPU architectures.
As an application developer, you don’t typically need to think about how exactly a system call is made. You simply include the appropriate header file and make the call as if it were a normal function.

`glibc` provides wrapper code which abstracts you away from the underlying code which arranges the arguments you’ve passed and enters the kernel.
Before we can dive into the details of how system calls are made, we’ll need to define some terms and examine some core ideas that will appear later.

### Note:-
```
Type `sudo -s` in your terminal before executing the upcoming commands so that you need not write sudo again and again in the terminal, 
it will give you a super user terminal session.
```


