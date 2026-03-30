# Assignment Questions

## Question 1: Thread vs Process

Your Answer:

A process is an independent program that has its own memory and resources, while a thread is a smaller unit inside a process and shares memory with other threads. One difference is that processes are heavier and take more time to create, while threads are lighter and faster. Another difference is that threads can communicate faster because they share the same memory. In this assignment, we used threads because we needed multiple processes to run at the same time efficiently. For example, in SchedulerSimulation.java, each process is implemented as a thread using Runnable, which makes the simulation faster and easier to manage.

---

## Question 2: Ready Queue Behavior

Your Answer:

In Round-Robin scheduling, if a process does not finish within its time quantum, it is moved to the end of the ready queue. This allows other processes to get CPU time and ensures fairness. The process will return later and continue execution from where it stopped.

Example from my output:
P1 yields CPU for context switch  
P1 added to ready queue  

Explanation of example:
This shows that P1 did not finish in one quantum, so it was placed back in the ready queue. It waited for its turn and continued later. This behavior is important because it prevents one process from taking all CPU time and gives all processes a fair chance.

---

## Question 3: Thread Lifecycle

Your Answer:

1. New: P1 is in the New state when the thread object is created before calling start().

2. Runnable: P1 becomes Runnable when start() is called and it is added to the ready queue.

3. Running: P1 is Running when the CPU selects it and it begins execution.

4. Waiting: P1 goes into Waiting when it is paused using Thread.sleep() or waiting for its next turn after its time quantum.

5. Terminated: P1 becomes Terminated when it finishes execution and its remaining time reaches zero.

---

## Question 4: Real-World Applications

Your Answer:

### Example 1: Web Server

Description:
A web server handles multiple user requests at the same time using threads.

Why Round-Robin works well here:
Round-Robin ensures each request gets CPU time fairly, so no request is delayed too much. This improves responsiveness and user experience.

### Example 2: Game Engine

Description:
A game engine runs multiple tasks like graphics, input, and physics at the same time.

Why Round-Robin works well here:
It allows all tasks to run smoothly by sharing CPU time. This prevents freezing and keeps the game responsive.

---

## Summary

Key concepts I understood through these questions:
1. Difference between thread and process  
2. Round-Robin scheduling behavior  
3. Thread lifecycle states  

Concepts I need to study more:
1. Thread synchronization  
2. Deadlock handling
