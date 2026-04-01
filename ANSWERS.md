# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

[process is an independent program in execution that has its own memory space and system resources. Each process runs separately and does not share memory with other processes, which makes it more secure but also more expensive in terms of creation and communication.

A thread is a smaller unit of execution within a process. Multiple threads can exist within a single process and share the same memory and resources, which makes them more lightweight and faster compared to processes.

One key difference is that processes have separate memory spaces, while threads share the same memory, allowing faster communication. Another difference is that creating and switching between processes requires more overhead, whereas threads are faster to create and manage.

In this assignment, threads were used instead of processes because the simulation requires frequent context switching between tasks. Threads make this more efficient and faster. Additionally, threads allow shared access to data structures like the ready queue without the need for complex communication mechanisms.]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

[In Round-Robin scheduling, if a process does not finish within its time quantum, it is paused and moved to the end of the ready queue. This ensures that all processes get a fair chance to use the CPU.

When a process uses up its allocated time quantum and still has remaining time, a context switch occurs, and the process is placed at the back of the queue. It will wait until other processes get their turn before it executes again.

For example, in my program output, when a process such as P1 runs and does not finish within its time quantum, it yields the CPU and is re-added to the ready queue. After that, other processes like P2 and P3 are executed before P1 gets another turn.

This behavior is important for fairness because it prevents any single process from monopolizing the CPU. It ensures that all processes make progress and that the system remains responsive when multiple tasks are running.]

Example from my output:
```
[Paste a relevant snippet from your program output here showing a process being re-queued]
```

**Explanation of example:**
[Explain what's happening in the output snippet you pasted]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[A thread goes through several states during its lifecycle. In this simulation, the process P1 transitions through different states based on how the scheduler manages its execution. The following explains each state and when P1 enters it:]

1. **New**: [P1 is in the New state when the Thread object is created using new Thread(process) but before the start() method is called. At this point, the thread has been created but has not yet begun execution.]

2. **Runnable**: [P1 enters the Runnable state when the start() method is called on its thread. This means the thread is ready to run and is waiting for the CPU to be assigned by the scheduler.]

3. **Running**: [P1 is in the Running state when the CPU is assigned to it and the run() method is actively executing. During this time, the process performs its work for the given time quantum.]

4. **Waiting**: [P1 enters the Waiting state when it is paused during execution. This can happen when Thread.sleep() is called inside the run() method to simulate execution time, or when the main thread calls join() and waits for P1 to finish its current quantum.
]

5. **Terminated**: [P1 reaches the Terminated state when it has completed its execution and its remaining time becomes zero. At this point, the thread finishes and cannot be restarted again.]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [ Multi-User Web Server]

**Description**: 
[A web server (like Apache or Nginx) must handle hundreds or thousands of simultaneous incoming HTTP requests from different users at the same time.  ]

**Why Round-Robin works well here**: 
[ Round-Robin provides fairness by ensuring that no single long request (such as a large file download) completely blocks the server from responding to smaller, quicker requests (like fetching a simple webpage). By giving each request "thread" a small time quantum of CPU time, the server remains highly responsive to all users simultaneously. ]

### Example 2: [Modern Game Engine]

**Description**: 
[ In a video game engine, the system must concurrently manage various independent tasks such as physics calculations, artificial intelligence (AI) logic, and audio processing.]

**Why Round-Robin works well here**: 
[ Game engines require predictability and low latency to maintain a steady frame rate. Round-Robin scheduling ensures that the AI thread doesn't "starve" the Audio thread of CPU time, preventing sound glitches or stuttering during complex gameplay. It allows the engine to cycle through all critical tasks within a single frame]

---

## Summary

**Key concepts I understood through these questions:**
1. 
2. 
3. 

**Concepts I need to study more:**
1. 
2. 
