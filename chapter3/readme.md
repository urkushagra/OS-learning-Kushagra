# 📘 Operating Systems — Chapter 3  
## CPU Scheduling (SDE Interview Preparation)

CPU Scheduling is one of the **most important chapters** in Operating Systems and is heavily tested in **SDE interviews** and university exams.  
This chapter explains how the OS decides **which process gets the CPU**, when, and for how long.

---

## 🧠 1. What is CPU Scheduling?

**CPU Scheduling** is the mechanism by which the operating system selects one process from the **Ready Queue** to allocate the CPU.

👉 Since multiple processes compete for the CPU, efficient scheduling is required to maximize performance and fairness.

---

## 🎯 2. Scheduling Objectives / Criteria

A good scheduling algorithm aims to:

| Criterion | Description |
|---------|-------------|
| CPU Utilization | Keep CPU as busy as possible |
| Throughput | Number of processes completed per unit time |
| Turnaround Time | Completion time − Arrival time |
| Waiting Time | Time spent waiting in ready queue |
| Response Time | Time until first CPU response |

---

## ⚔️ 3. Preemptive vs Non-Preemptive Scheduling

### 🔹 Non-Preemptive Scheduling
- CPU is not forcibly taken from a process
- Process runs until completion or I/O request

Examples:
- FCFS  
- SJF (non-preemptive)

### 🔹 Preemptive Scheduling
- CPU can be taken away by OS
- Better responsiveness

Examples:
- Round Robin  
- SRTF  
- Priority (preemptive)

---

## 📊 4. CPU Scheduling Algorithms

---

### 4.1 First Come First Serve (FCFS)

**Idea:**  
Process that arrives first gets CPU first.

**Type:** Non-preemptive

**Advantages:**
- Simple
- No starvation

**Disadvantages:**
- Convoy effect
- High average waiting time

📌 *Convoy Effect:*  
Short processes wait behind long processes.

---

### 4.2 Shortest Job First (SJF)

**Idea:**  
Process with the smallest CPU burst time executes first.

**Types:**
- Non-preemptive SJF  
- Preemptive SJF → **SRTF**

**Advantages:**
- Minimum average waiting time (optimal)

**Disadvantages:**
- Burst time prediction required
- Starvation possible

---

### 4.3 Shortest Remaining Time First (SRTF)

**Idea:**  
Preemptive version of SJF.

- If a new process arrives with smaller remaining time, it preempts the current process.

**Disadvantages:**
- Frequent context switching
- Starvation

---

### 4.4 Priority Scheduling

**Idea:**  
CPU is allocated based on priority.

**Types:**
- Preemptive
- Non-preemptive

**Problem:**
- Starvation of low-priority processes

**Solution:**
- **Aging** (gradually increase priority over time)

---

### 4.5 Round Robin (RR)

**Idea:**  
Each process gets CPU for a fixed **time quantum**.

**Best suited for:**
- Time-sharing systems

**Trade-off:**
- Very small quantum → too many context switches  
- Very large quantum → behaves like FCFS

📌 Improves **response time**.

---

### 4.6 Multilevel Queue Scheduling

- Ready queue divided into multiple queues
- Each queue has its own scheduling algorithm
- No movement between queues

Example queues:
- System processes
- Interactive processes
- Batch processes

---

### 4.7 Multilevel Feedback Queue (MLFQ) ⭐

**Most important for interviews & real OS**

**Key Features:**
- Multiple queues with different priorities
- Processes can move between queues
- Prevents starvation
- Learns process behavior dynamically

**Rules:**
1. New processes start at highest priority  
2. Uses full time quantum → moved to lower priority  
3. Yields early → stays or moves to higher priority  

📌 Used in **Linux Scheduler**

---

## 🧮 5. Scheduling Time Calculations

### Important Formulas:
- **Turnaround Time = Completion Time − Arrival Time**
- **Waiting Time = Turnaround Time − Burst Time**
- **Response Time = First CPU Start − Arrival Time**

These are commonly tested in **numerical problems**.

---

## 🔁 6. Context Switching in Scheduling

- Happens when CPU switches from one process to another
- Required in preemptive scheduling
- Considered **pure overhead**

---

## 📝 Chapter 3 — Interview Questions

1. What is CPU scheduling?
2. What are scheduling criteria?
3. Difference between preemptive and non-preemptive scheduling?
4. Explain FCFS and convoy effect.
5. Why is SJF optimal?
6. Difference between SJF and SRTF?
7. What is starvation? How is it solved?
8. Why Round Robin is used?
9. What is time quantum?
10. Explain Multilevel Feedback Queue (MLFQ).

---

## ✅ Summary

- CPU scheduling selects which process gets CPU
- Different algorithms balance fairness and efficiency
- SJF is theoretically optimal
- Round Robin improves responsiveness
- MLFQ is used in real-world operating systems


