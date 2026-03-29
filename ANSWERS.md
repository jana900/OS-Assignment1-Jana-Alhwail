# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

A thread is a smaller execution unit inside a process, whereas a process is a separate program running on its own memory and system resources. Because they share memory and resources, threads within the same process can be created and coordinated more quickly than independent processes. Because the simulation maintains several process objects within a single Java application and threads are better suited for modeling concurrent execution units in the same scheduler, we employed them in this assignment. Separate operating system processes would complicate tracking and communication and add needless overhead. By generating Thread instances for every Process object and keeping them in the ready queue and processMap, the code mirrors this approach.

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

In Round-Robin scheduling, if a process does not finish within its time quantum, it is moved to the end of the ready queue. This allows other processes to get CPU time before it runs again. The process will keep returning to the queue until its remaining time becomes zero. This behavior ensures fairness among all processes. It also prevents one process from monopolizing the CPU.

Example from my output:
```
:
P1 executing quantum [4000ms]
...
Remaining time: 1175ms
P1 yields CPU for context switch
P1 added to ready queue
```

**Explanation of example:**
P1 used its time quantum, however it did not complete execution. It returned to the ready queue after yielding the CPU because it still had time. This implies that it won't get another turn until other processes have finished. This illustrates the equitable cycles of Round-Robin scheduling.

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

 1. New: P1 is in the New state when the thread is created but not yet started.
 2. Runnable: P1 becomes Runnable after being added to the ready queue and is waiting to be scheduled.
 3. Running: P1 enters Running state when it starts executing its time quantum on the CPU.
 4. Waiting: P1 enters Waiting state when the main thread uses join() and waits for the process to finish execution.
 5. Terminated: P1 becomes Terminated when its remaining time reaches zero and it finishes execution.


---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: Web Server

**Description**: 

A web server handles many client requests at the same time, such as loading pages, sending responses, and processing user actions.

**Why Round-Robin works well here**: 

Because it allocates a fair amount of CPU time to each request-handling thread, round-robin scheduling is beneficial. This enhances user responsiveness and keeps one request from blocking all others. This assignment uses the same concept, with each procedure taking a turn and incomplete work being completed later.
### Example 2: Media Player Application

**Description**: 
A media player may need to play video, update the interface, and respond to user input at the same time.

**Why Round-Robin works well here**: 
Because it gives each active task a regular opportunity to complete, Round-Robin performs well. This keeps playback, UI updates, and controls functioning simultaneously while maintaining the application's responsiveness. The program in this assignment, which divides CPU time equally among several threads, is comparable to the scheduling concept.

---

## Summary

**Key concepts I understood through these questions:**
 1. Difference between threads and processes
 2. Round-Robin scheduling behavior
 3. Thread lifecycle

**Concepts I need to study more:**
 1. Synchronization
 2. Advanced scheduling algorithms
