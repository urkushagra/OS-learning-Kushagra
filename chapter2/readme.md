# 📘 Operating Systems — Chapter 2  
## Process Management (SDE Interview Preparation)

This chapter covers **Process Management**, one of the most important Operating System topics for **high-paying SDE interviews**.  
It explains how processes are created, scheduled, executed, synchronized, and terminated inside an OS.

---

## 🧠 1. What is a Process?

A **process** is an instance of a program in execution.

A process includes:
- Program code
- CPU registers & program counter
- Stack and heap
- Memory address space
- Open files and I/O resources

### Program vs Process

| Program | Process |
|-------|--------|
| Passive entity | Active entity |
| Stored on disk | Resides in memory |
| No resources | Has CPU, memory, I/O |

---

## 🔄 2. Process States

A process moves through different states during execution.

### Basic States
- **New** – Process is being created  
- **Ready** – Waiting for CPU  
- **Running** – Executing on CPU  
- **Waiting / Blocked** – Waiting for I/O  
- **Terminated** – Execution finished  

### State Transition Flow

New → Ready → Running → Waiting → Ready → Running → Terminated


### Ready vs Waiting

| Ready | Waiting |
|------|--------|
| Waiting for CPU | Waiting for I/O |
| Can run immediately | Cannot run |
| CPU dependent | I/O dependent |

---

## 📦 3. Process Control Block (PCB)

PCB is a data structure maintained by the OS to store **all information about a process**.

### PCB Contains:
- Process ID (PID)
- Process state
- Program counter
- CPU registers
- Memory management info
- Scheduling info
- Open file list

**Interview line:**  
> “PCB is the identity card of a process.”

---

## 🔁 4. Context Switching

Context switching occurs when the CPU switches from one process to another.

### Steps:
1. Save current process state into PCB  
2. Load next process state from PCB  
3. Update CPU registers and program counter  

⚠ **Context switching is pure overhead** — it does no useful work.

---

## 🌱 5. Process Creation — `fork()`

- `fork()` creates a **child process**
- Child is an exact copy of parent (Copy-On-Write)
- Child has a **new PID**

### Return values:
- Parent receives **child PID**
- Child receives **0**

---

## 🔄 6. Executing a New Program — `exec()`

- Replaces the process memory with a new program
- PID remains the same
- Used after `fork()` to run a new program

---

## 🛑 7. Process Termination

- `exit()` – Terminates process
- `wait()` – Parent waits for child to finish
- Prevents zombie processes

---

## 🧟 8. Orphan and Zombie Processes

### Zombie Process
- Child finished execution
- Parent did not call `wait()`
- Process entry remains in process table

### Orphan Process
- Parent terminates before child
- Child is adopted by `init` process

---

## 🧵 9. Process vs Thread

| Process | Thread |
|-------|--------|
| Heavyweight | Lightweight |
| Separate memory | Shared memory |
| Slow creation | Fast creation |
| Slow context switch | Fast context switch |

Threads improve performance via parallelism.

---

## 🔗 10. Inter-Process Communication (IPC)

Used when processes need to communicate.

### IPC Mechanisms:
- Pipes
- Message queues
- Shared memory
- Semaphores
- Sockets

---

## ⏳ 11. Process Scheduling (Basics)

Schedulers decide which process gets CPU.

Types:
- **Long-term scheduler** – selects jobs
- **Short-term scheduler** – selects process for CPU
- **Medium-term scheduler** – swapping

(Detailed scheduling algorithms are covered in Chapter 3.)

---

## 📝 Chapter 2 — Interview Questions

1. What is a process?
2. Program vs process?
3. Explain process states.
4. What is PCB?
5. What is context switching?
6. How does `fork()` work?
7. Difference between `fork()` and `exec()`?
8. What is a zombie process?
9. What is an orphan process?
10. Process vs thread?
11. What is IPC?

---

## ✅ Summary

- A process is a running program
- OS tracks processes using PCB
- Process states help OS scheduling
- Context switching enables multitasking
- `fork()` and `exec()` manage process creation
- IPC enables communication between processes


