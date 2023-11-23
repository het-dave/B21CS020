# XV Quiz (CSL 3030)

Welcome to the XV Quiz for CSL 3030 - Operating Systems!



## Instructions
- Answer the multiple-choice questions by selecting the correct option.
- For theoretical questions, provide concise and accurate explanations.
- Feel free to use this quiz for self-assessment or educational purposes.

## Multiple-Choice Questions

#### Question 1: Basics
1. What is XV6?
   - a. A programming language
   - b. A Unix-like operating system
   - c. A file system
   - d. An assembly language

#### Question 2: Architecture
2. XV6 is based on which earlier operating system?
   - a. Windows
   - b. Linux
   - c. BSD
   - d. DOS

#### Question 3: File System
3. Which file system is used in XV6?
   - a. FAT32
   - b. NTFS
   - c. ext4
   - d. simple

#### Question 4: System Calls
4. How are system calls implemented in XV6?
   - a. As functions in the C standard library
   - b. As interrupts
   - c. Through the command line
   - d. As external programs

#### Question 5: Processes
5. In XV6, what is the maximum number of processes that can run simultaneously?
   - a. 128
   - b. 256
   - c. 512
   - d. 1024

#### Question 6: Shell
6. What is the name of the shell used in XV6?
   - a. Bash
   - b. Zsh
   - c. Sh
   - d. Fish

#### Question 7: Scheduling
7. How does XV6 handle process scheduling?
   - a. Round-robin scheduling
   - b. Priority-based scheduling
   - c. First-Come-First-Serve (FCFS)
   - d. Random scheduling

#### Question 8: Memory Management
8. Which memory management technique is used in XV6?
   - a. Paging
   - b. Segmentation
   - c. Virtual Memory
   - d. None of the above

#### Question 9: Interrupts
9. How are interrupts handled in XV6?
   - a. Through polling
   - b. Using hardware interrupts
   - c. Using software interrupts
   - d. Both b and c

#### Question 10: Multithreading
10. Does XV6 support multithreading?
    - a. Yes
    - b. No

#### Bonus Question:
11. Who developed XV6?
    - a. Microsoft
    - b. Google
    - c. MIT
    - d. IBM

## Theoretical Questions

#### Question 12: Process States
12. Briefly explain the different states a process can be in within the XV6 operating system.

#### Question 13: File System Structure
13. Describe the structure of the file system in XV6. Include the key components and their roles.

#### Question 14: System Calls vs. Library Functions
14. Explain the difference between system calls and library functions in the context of XV6. Provide examples of each.

#### Question 15: Memory Paging
15. How does memory paging work in XV6? Discuss the benefits of using paging in memory management.

#### Question 16: Shell Commands
16. Name and briefly explain three essential shell commands in the XV6 operating system.

#### Question 17: Process Synchronization
17. Discuss the concept of process synchronization in XV6. Why is it essential, and what mechanisms are used to achieve it?

#### Question 18: Interrupt Handling
18. Explain the role of interrupts in the XV6 operating system. How are interrupts handled, and what is their significance in system operation?

#### Question 19: Virtual Memory
19. What is virtual memory, and how is it implemented in XV6? Discuss the advantages of using virtual memory.

#### Question 20: Boot Process
20. Outline the steps involved in the boot process of XV6. What happens from the moment the computer is powered on to when the XV6 kernel is loaded into memory?

## Answers
Please write your answers here
Q1. B) UNIX Like Operating Systems

Q2. C) BSD

Q3. A) FAT32

Q4. B) As interrupts

Q5. A) 128

Q6. C) Sh

Q7. A) Round-robin scheduling

Q8. A) Paging

Q9. B) Using hardware interrupts

Q10. B) No

Q11. C) MIT

Q12. The different states that a process can be in the xv6 operating system are as follows:
   1. Running: The process is currently running/being executed on the CPU.
   2. Runnable: The process is waiting in the queue for the CPU to be allocated to the process.
   3. Sleeping: The process is waiting for some other event to occur. eg I/O Operation.
   4. Unused: The process has either been created or terminated and is not in use.
   5. Zombie: This is the state when the process has completed execution but its exit status is needed by some parent process and thus it remains in the system until the parent                      retrieves the exit status.
   6. Embryo: The process is being created i.e. is in the early stages of initialization.

Q13. The XV6 file system consists of:
   1. Superblocks: Contains the overall file system information.
   2. Inodes: Data structures representing files and directories.
   3. Inode Table: Array of inodes.
   4. Data Blocks: Store file content.
   5. Directory Entry: Maps filenames to inode numbers.
   6. Bitmaps: Track free/allocated inodes and data blocks.
   7. File Descriptor Table: Per-process table for open files.

Q14. System calls are interfaces between user-level applications and the operating system. They provide a way for user programs to request services from the kernel whereas Library functions are routines provided by libraries that applications link against. They are not part of the operating system kernel but offer additional functionality to user programs. eg. The write system call is used to write data to a file, The printf function from the C library is used for formatted output. 

Q15. In XV6, paging is done using a two level page table. The high level page table maps on the lower level page table and the lower level page table references the physical page frame. Some of the benefits of paging are as follows:
   a. Contiguous Virtual Address Space that helps in simplifying memory allocation
   b. Isolation as each process has its own page table and the other processes cannot access the page table of any other process.

Q16.
   1. ls: the ls command lists all the files in the current working directory
   2. cd: cd is used to change the current working directory.
   3. cp: cp is used to copy files or directories from one location to another.

Q17. Process synchronization is needed when there are concurrent processes running. It is essential for managing shared resources and avoiding conflicts. Mechanisms used in XV6 in order to perform process synchronizations are locks, semaphores, condition variables etc.

Q18. Interrupts are events that alter normal execution flow of the processes. Interrupts play a crucial role in handling external events and ensuring efficient system operation. Interrupts are handled through interrupt service routines (ISRs) triggered by hardware or software events. The significance of interrupt operations are in I/O operations where a process needs to be be interrupted to wait for the I/O to complete. Interrupts are also used for timekeeping, process scheduling, preemptive multitasking and facilitate interaction with external devices by allowing the OS to respond to device-generated signals promptly.

Q19. Virtual memory provides the illusion of a larger memory space than physically available. It is implemented using Page Tables on the xv6 system. The advantages of using virtual memory are as follows:
   1. Increased Address Space
   2. Efficient Utilization of Resources
   3. Ease of Memory Management

Q20.
   1. BIOS/UEFI initialization.
   2. Bootloader (e.g., GRUB) loads XV6 kernel into memory.
   3. Kernel initialization, sets up memory, filesystems, and essential data structures.
   4. Transfer control to the main function, initiating the operating system.
