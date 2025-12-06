# 📘 Operating Systems — Chapter 1  
### Introduction to Operating Systems + Interview Questions & Answers

This document contains the complete **Chapter 1 (Introduction to OS)** along with **interview-ready answers** commonly asked in SDE interviews at FAANG-level companies.

---

# 🧠 Chapter 1: Introduction to Operating Systems

## 1️⃣ What is an Operating System?

An **Operating System (OS)** is system software that manages hardware and provides services to applications.  
It acts as both:

- **A Resource Manager** – allocates CPU, memory, disk, I/O  
- **An Abstraction Layer** – hides hardware complexity  

Examples: Linux, Windows, macOS, Android.

---

## 2️⃣ Functions of an Operating System

### ✔ 1. Process Management  
Handles creation, scheduling, and termination of processes.

### ✔ 2. Memory Management  
Allocates RAM, manages paging, segmentation, virtual memory.

### ✔ 3. File System Management  
Manages files, directories, storage, metadata.

### ✔ 4. I/O Device Management  
Uses device drivers to interact with hardware devices.

### ✔ 5. Security & Protection  
Authentication, authorization, isolation.

### ✔ 6. Resource Allocation  
Fair distribution of CPU, memory, storage, and I/O.

---

## 3️⃣ Types of Operating Systems

- **Batch OS**  
- **Multitasking / Time-sharing OS**  
- **Multiprogramming OS**  
- **Real-Time OS (RTOS)**  
- **Distributed OS**  

---

## 4️⃣ User Mode vs Kernel Mode

### ⭐ Kernel Mode  
- Full access to hardware  
- Executes privileged instructions  
- OS kernel runs here  

### ⭐ User Mode  
- Restricted access  
- Applications run here  
- Uses system calls to interact with OS  

---

## 5️⃣ System Calls

System calls allow user programs to request services from the OS.

Examples:
- `read()`  
- `write()`  
- `open()`  
- `fork()`  
- `exec()`  
- `wait()`  

**A system call switches CPU from user mode → kernel mode.**

---

## 6️⃣ Kernel Architecture

### ✔ Monolithic Kernel  
All OS services run in kernel space.  
Example: Linux.

### ✔ Microkernel  
Minimal kernel; rest of services run in user space.  
Example: Minix, QNX.

### ✔ Hybrid Kernel  
Mix of both.  
Example: Windows, macOS.

---

## 7️⃣ OS as a Resource Manager  

OS decides:  
- Who gets CPU time  
- How memory is allocated  
- How I/O devices are shared  
- How storage is organized  

---

## 8️⃣ Key Terminology

| Term | Meaning |
|------|---------|
| Program | Static code on disk |
| Process | Running instance of a program |
| Interrupt | Hardware/Software signal to CPU |
| Booting | Process of loading OS into memory |

---

# 📝 Chapter 1 — Interview Questions & Answers

Below are concise, FAANG-style answers.

---

## **Q1. What is an Operating System?**

An OS is software that manages hardware and provides abstraction for applications.  
It acts as a **resource manager** and **interface between user and hardware**.

---

## **Q2. What is a Kernel? Types of Kernels?**

The kernel is the core of OS running in **kernel mode**, handling memory, processes, device drivers, and system calls.

### Types:
- **Monolithic Kernel**
- **Microkernel**
- **Hybrid Kernel**

---

## **Q3. Difference between Program and Process?**

| Program | Process |
|--------|---------|
| Passive file on disk | Active execution in memory |
| No resources | Has CPU, memory, IO resources |
| Static | Dynamic |

---

## **Q4. User Mode vs Kernel Mode**

### User Mode  
- Limited access  
- Apps run here  

### Kernel Mode  
- Full hardware access  
- OS runs here  

---

## **Q5. What is a System Call?**

A system call is an interface that allows a user program to request OS services.  
Examples: `open`, `read`, `write`, `fork`.

---

## **Q6. Multitasking vs Multithreading vs Multiprocessing**

### Multitasking  
Multiple programs run simultaneously.

### Multithreading  
Multiple threads inside one process.

### Multiprocessing  
Multiple CPUs executing tasks in parallel.

---

## **Q7. Why do we need an OS?**

- Manages hardware  
- Provides abstraction  
- Improves security  
- Enables multitasking  

**Short answer:**  
**“The OS makes hardware usable.”**

---

# ✅ Summary

This README covers:

- Introduction to OS  
- Kernel basics  
- System calls  
- Modes of operation  
- OS functions  
- Interview questions with polished answers  

---
