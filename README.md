# weenix-os
As part of my [CS402 Course](https://merlot.usc.edu/cs402-s25/) at USC, I built Weenix OS. Weenix OS was originally developed at Brown University and you can find out more about it [here](https://brown-cs1690.github.io/brown-cs167-s22/#/). As part of the project I implemented the following portions:

- **PROCS**:- Implemented process management for a uniprocessor with a single thread. The scheduler was a simple non-preemtive FIFO queue. Thread switching happens either when the current process finishes or when it yields voluntarily (through a system call). 
- **VFS**:- Implemented the Virtual File System. This is an interface between the OS and the various file systems implementations that the OS supports (RamFS and SFS). This includes implementing most file related system calls.
- **VM**:- Implemented Virtual Memory to get a user space shell up and running. This meant I implemented the page fault handler, and the virtual memory map required to have Copy-On-Write working, the `fork()`, `brk()` and `mmap()` system calls. 

These are screenshots from my implementation of the OS: 

<img width="426" alt="screenshot of a terminal that shows the starting screen of the weenix os in the weenx shell" src="https://user-images.githubusercontent.com/23412234/166855630-c7ea7240-ea4c-4cd6-b307-f20f31d441c2.png">

The Weenix User Space Shell 

<img width="405" alt="Output of the ls command listing all the contents of the root folder" src="https://user-images.githubusercontent.com/23412234/166855718-b1a32d8a-15e2-40b8-b55d-7a12ff1e1374.png">

Output of the `ls` command

<img width="431" alt="Output of the README file using cat command" src="https://user-images.githubusercontent.com/23412234/166855737-98b6e9d7-7d23-4a99-bb64-60e04f1618ba.png">

Output of the `cat` command showing the contents of the README file. 


<img width="419" alt="A screen showing that all the test cases for VFS passed" src="https://user-images.githubusercontent.com/23412234/166855672-d77b2d0e-a19f-4a44-88cd-f7df77d54b38.png">

Ouptut of the `vfstest` command testing the VFS layer. 

<img width="429" alt="A screen showing that all the test cases for memory passed" src="https://user-images.githubusercontent.com/23412234/166855941-3c224dd6-b2f1-4d66-ade5-2a002965e951.png">

Ouptut of the `memtest` command testing the virtual memory implementation.

<img width="420" alt="A screen showing that the memory stress test passed" src="https://user-images.githubusercontent.com/23412234/166856087-3f53a334-c7a5-49bf-a340-02afbbaa0bca.png">

Output of the `eatmem` command that stress tests the OS by eating at least 10,000 pages. 


<img width="407" alt="A screen showing that forkbomb successfully completed" src="https://user-images.githubusercontent.com/23412234/166856271-4a7ca23c-0b79-4856-9ceb-1b233954ff2e.png">

Output of the `forkbomb limit500` command showing that it successfuly forked 500 processes. 

<img width="405" alt="A screen showing that stress test successfully completed" src="https://user-images.githubusercontent.com/23412234/166856399-fcfe1632-888e-476e-9a09-db14d5d2ad92.png">

Output of the `stress limit500` command showing that it successfuly stress tested the system. 

<img width="417" alt="shutdown screen for weenix" src="https://user-images.githubusercontent.com/23412234/166856028-13df5ec5-df33-4150-bbb0-3c19beee0192.png">

Showing that the OS cleanly halts after running these commands.


The code for this project is governed by a closed source license, but I can email a copy of it if required to potiential employers. 



