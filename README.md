# 📘 Operating Systems – SDE Interview Preparation

A complete, high-value Operating Systems guide designed for **SDE interviews** at companies like **Amazon, Google, Microsoft, Meta, Netflix**, and top product-based startups.

This syllabus covers fundamentals → advanced OS concepts → Linux internals → FAANG-level system design topics.

---

## 📚 1. OS Basics & Fundamentals

- What is an Operating System?  
- Functions and goals of OS  
- Types of OS: Batch, Multiprogramming, Multitasking, Real-time, Distributed  
- User mode vs Kernel mode  
- System Calls: `fork`, `exec`, `wait`, `read`, `write`, `open`, `close`

---

## ⚙️ 2. Processes & Threads

### 2.1 Process Concepts
- Process lifecycle (states)  
- PCB (Process Control Block)  
- Context switching  
- Orphan & zombie processes  
- Inter-process communication (IPC)

### 2.2 Threads
- Process vs Thread  
- User-level vs Kernel-level threads  
- Multithreading models: **1:1**, **M:1**, **M:N**  
- Green threads vs Native threads  

---

## 🧠 3. CPU Scheduling

- Scheduling criteria (waiting time, turnaround, throughput, CPU utilization)  
- Scheduling algorithms:
  - FCFS  
  - SJF  
  - SRTF  
  - Priority Scheduling  
  - Round Robin  
  - Multilevel Queue  
  - Multilevel Feedback Queue (MLFQ)  
- Preemptive vs Non-preemptive scheduling  

---

## 🔒 4. Synchronization & Concurrency

### 4.1 Critical Section
- Race conditions  
- Atomicity  

### 4.2 Synchronization Tools
- Mutex  
- Semaphores  
- Spinlocks  
- Condition Variables  
- Monitors  

### 4.3 Classical Problems
- Producer–Consumer  
- Readers–Writers  
- Dining Philosophers  
- Sleeping Barber  

---

## 🚧 5. Deadlocks

- Coffman conditions  
- Deadlock prevention  
- Deadlock avoidance (Banker’s algorithm)  
- Deadlock detection & recovery  
- Resource Allocation Graph (RAG)

---

## 🗂 6. Memory Management

- Logical vs Physical address  
- MMU (Memory Management Unit)  
- Swapping  
- Contiguous memory allocation  
- Internal & External fragmentation  

### 6.1 Paging
- Page table  
- Multi-level page table  
- Inverted page table  
- TLB (Translation Lookaside Buffer)

### 6.2 Segmentation
- Segment table  
- Segmentation fault  

---

## 💾 7. Virtual Memory

- Demand paging  
- Page fault handling  
- Thrashing  
- Page Replacement Algorithms:
  - FIFO  
  - LRU  
  - LFU  
  - Optimal  
  - Clock / Second Chance  

---

## 📁 8. File System Management

- File attributes  
- File operations (open, read, write, close)  
- Access methods: Sequential, Indexed, Direct  
- Directory structures  
- File system implementation  
- Inodes  
- Allocation methods:
  - Contiguous  
  - Linked  
  - Indexed  
- Journaling file systems (EXT4, NTFS, FAT32)

---

## 💽 9. Disk Management

- Disk scheduling:
  - FCFS  
  - SSTF  
  - SCAN  
  - CSCAN  
- RAID levels  

---

## 🔌 10. I/O System

- I/O devices and drivers  
- Blocking vs Non-blocking I/O  
- Interrupts  
- DMA (Direct Memory Access)  

---

## 🛡️ 11. OS Security & Protection

- Authentication vs Authorization  
- Access control models: DAC, MAC, RBAC  
- Sandboxing  
- ASLR  
- Memory protection  
- Buffer overflow basics  

---

## 🐧 12. Linux System Programming

- `fork()`  
- `exec()`  
- `wait()`  
- `pipe()`  
- `dup()`  
- Signals  
- `/proc` and `/dev` filesystem  
- System call internals  

---

## 🧩 13. High-Level OS System Design Topics

- Lifecycle of a system call  
- How a program runs internally  
- Thread scheduling in OS  
- Linux virtual memory internals  
- How `malloc()` works  
- Kernel vs User space  
- Page cache, swap, and OOM killer  

---

## 🚀 14. Advanced (FAANG-Level) OS Concepts

- Copy-On-Write (COW)  
- `mmap()`  
- Shared Memory  
- Process priority & niceness  
- cgroups & namespaces  
- OS-level virtualization (Docker internals)  

---

## 📝 How to Use This Syllabus

- Study concepts → implement small programs → solve OS interview questions  
- Use Linux terminal to explore real behavior  
- Practice:
  - Producer–Consumer using semaphores  
  - Readers–Writers  
  - Dining Philosophers  
  - LRU Cache  
- Write programs using system calls (`fork`, `exec`, `pipe`, etc.)

---
