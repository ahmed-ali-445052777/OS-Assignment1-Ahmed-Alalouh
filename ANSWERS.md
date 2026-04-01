# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

In this assignment I used threads because they are much lighter than processes. A process has its own memory but threads inside the same process can share things like the processMap and queue. This makes the simulation faster and uses less CPU resources than creating a full process for every task like P1 or P2.

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

In Round-Robin, if a process doesn't finish within its time quantum, the scheduler stops it and puts it back at the end of the queue. In my simulation, I used processQueue.poll() to take a process out and addProcessToQueue() to put it back if it's not finished. This ensures that every process gets a fair chance to run without any single one blocking the CPU for too long.

Example from my output:
```
▶ P2 executing quantum [4000ms] 
  ⚡ Quantum progress: [███████████████] 100%
  ⏸ P2 completed quantum 4000ms │ Overall progress: [████████░░░░░░░░░░░░] 40%
    Remaining time: 6000ms
  ↻ P2 yields CPU for context switch
```

**Explanation of example:**
In this snippet from my program, P2 ran for its 4000ms quantum Since it still had 6000ms left it couldn't finish so it yielded the CPU and went back to the ready queue to wait for its next turn

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: P1 is in the New state at the very beginning when the code creates the thread object using the line "Thread thread = new Thread(process)" inside the addProcessToQueue method. At this point, the thread is created but hasn't started running yet

2. **Runnable**: P1 becomes Runnable as soon as it is added to the processQueue. In this state, the thread is ready to work and is just waiting in the queue for its turn to be picked by the scheduler loop

3. **Running**: P1 enters the Running state when the main scheduler loop calls "currentThread.start()" This is the stage where the thread is actually using the CPU to execute the logic inside the run() method

4. **Waiting**: P1 goes into a Waiting state (specifically Timed Waiting) during its execution whenever the code calls "Thread.sleep(stepTime)"
This happens while the program is simulating the time it takes for the process to complete its quantum

5. Terminated: P1 reaches the Terminated state when the run() method finishes completely. This happens once the remainingTime reaches zero and the process is done with its execution, or after the main thread calls "currentThread.join()" to confirm it finished



---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:** 

### Example 1: [Web Servers handling many user requests]

**Description**: 
When a popular website gets hundreds of requests at the same time, the server needs a way to handle everyone without crashing or making people wait too long

**Why Round-Robin works well here**: 
It is really fair because it gives every user request a small "slice" of the server's time. This way, if one person is trying to download a huge video, they won't block another person who just wants to load a simple text page. It keeps the website responsive for everyone.
### Example 2: [Multi-tasking in Operating Systems]

**Description**: 
This is like when you are using your laptop and have a music player, a web browser, and a word document all open and running at the same time

**Why Round-Robin works well here**: 
It makes the computer feel fast and smooth. By switching between the different apps very quickly using a time quantum, the music keeps playing without stuttering while you are typing or scrolling. It's predictable and ensures that no single app hogs the entire CPU.

## Summary

**Key concepts I understood through these questions:**
1. How threads move through different states (New, Runnable, etc.) during the scheduling process as explained in the lecture slides.
2. The reason behind using threads instead of processes, mainly because they share resources and are "lighter" for the system
3. The logic of Round-Robin and how the "Time Quantum" ensures every process gets a fair turn

**Concepts I need to study more:**
1. I honestly need to focus more on the "Context Switching" overhead. I understand that the CPU switches between processes, but it's still a bit tricky to understand how much time is actually wasted during these switches in real systems
2. I need to review the part about "Synchronization" from the slides again. It was a bit confusing how to manage multiple threads if they all try to update the same shared data at the exact same time
