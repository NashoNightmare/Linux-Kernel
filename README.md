# Linux-Kernel
This is the respectively organized notes on Linux Kernel studying

## Contents



## 1.0 Linux Process Creation

Because Linux is a multi-user system, meaning different users can be running various programs on the system, each running instance of a program must be identified uniqely by the kernel. And a program is identified by its Process ID (PID) as well as it's Parent Process ID (PPID), therefore processes can further be categorized into,

- **Parent Processes** : These are the processes that create other processes during run time.
- **Child Processes** : These are the processes that are created by other processes during their run time.

Linux process Creation : [More info](https://subscription.packtpub.com/book/application_development/9781785883057/1/ch01lvl1sec12/process-creation)

### 1.1 The Init Process 
The init process is the mother process of all processes on the system. It's the first program that is executed when the linux system boots up. It manages all other processes in the system. It started by the kernel itself, So in the principle it does not hace a parent process.(PID 1).

Every child process further created (which may in turn create its own child process(es)) are all descendants of the init process. Processes thus created end up in a tree-like structure or a single hierarchy model. The `Shell`, which is one such process, becomes the interface for users to create user processes, when programs are called for execution.

[**Ref 1.0 - Complete Procedure of system startup**](https://github.com/NashoNightmare/Article-Library#ref-10----complete-procedure-of-system-startup)

