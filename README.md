# DBMS
**Disk Scheduling Simulator**  

### **Part 1: Simulation of Disk Scheduling Algorithms**  

You are given a **Megatron 747 disk** with the following specifications:  
- **Average seek time:** 6.46 milliseconds  
- **Rotational latency:** 4.17 milliseconds  
- **Transfer time:** 0.13 milliseconds  
- **Number of tracks (cylinders):** 65,535  
- **Head movement time:**  
  - **1 ms** for start/stop  
  - **1 ms per 4,000 cylinders**  

#### **Task:**  
Write a program that simulates two disk scheduling algorithms:  
1. **Elevator (SCAN) Algorithm**  
2. **First-Come, First-Served (FCFS)**  

#### **Input Format:**  
- First line: Current position of the disk head (**h**)  
- Second line: Number of requests (**k**)  
- Next **k** lines: Requests in the format `s a`, where:  
  - `s` = requested cylinder  
  - `a` = request arrival time  

##### **Example Input:**  
```
8000
6
8000 0
24000 0
56000 0
16000 10
64000 20
40000 30
```
(Head starts at cylinder **8000**, followed by **6 requests**.)  

#### **Output Format:**  
The program should execute both algorithms and output the response time for each request.

##### **Example Output for SCAN Algorithm:**  
```
8000 4.3
24000 13.6
56000 26.9
16000 34.2
64000 45.5
40000 56.8
```

##### **Example Output for FCFS Algorithm:**  
```
8000 4.3
24000 13.6
56000 26.9
16000 42.2
64000 59.5
40000 70.8
```

Finally, compare the results of the two algorithms and analyze their performance.  

---

### **Part 2: Random Request Generation & Performance Analysis**  

Extend your program to **generate random disk I/O requests** (e.g., 1,000 requests) and process them using both algorithms.  

#### **Steps:**  
1. Generate **random disk requests**.  
2. Simulate both **SCAN** and **FCFS** algorithms.  
3. Compare the total response times for different numbers of requests.  

