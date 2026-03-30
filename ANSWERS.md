# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

[a process is like a full program that runs in the system and it has its own memory and resources while a thread is a smaller part inside the process and shares the same memory with other threads the difference is that processes are heavier and take more time to create while threads are lighter and faster because they share resources with each other in this assignment i used threads instead of processes because it is easier and faster to simulate the scheduling and switching between processes without using too many system resources also threads make it easier to manage multiple tasks in the same program and that is exactly what we needed in this simulation]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

[in round robin scheduling if a process does not finish within its time quantum it will stop and go back to the ready queue so it can wait for its turn again this means the process will not complete immediately but it will run again later when it reaches the front of the queue]

Example from my output:
```
[Paste ? P1 executing quantum [4000ms] 
 ? Quantum progress: [███████████████] 100% 
 ? P1 completed quantum 4000ms │ Overall progress: [███████████████████░] 99% 
    Remaining time: 31ms 
 ? P1 yields CPU for context switch 
 ? P1(priority:2) added to ready queuea relevant snippet from your program output here showing a process being re-queued]
```

**Explanation of example:**
[in this part we can see that P1 ran for its time quantum but it did not finish completely because there was still a small remaining time which is 31ms so instead of finishing the process stopped and gave the cpu to another process and then it was placed again in the ready queue this means it will wait for its turn again and continue later until it finishes, and this is how the round robin system keeps switching between processes]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: [when the process is created but the thread has not started yet it is in the new state]

2. **Runnable**: [after the thread is created and added to the ready queue it becomes runnable and waits for the cpu]

3. **Running**: [when the scheduler picks the thread and it starts executing the run method it is in the running state]

4. **Waiting**: [when the thread is paused or waiting for its next turn after the time quantum it goes into waiting state until it can run again]

5. **Terminated**: [when the process finishes all its execution and remaining time becomes zero the thread is terminated and will not run again]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [online multiplayer games]

**Description**: 
[in online games there are many players connected at the same time and the system needs to update each player actions like movement and shooting continuously]

**Why Round-Robin works well here**: 
[round robin helps by giving each player a small time to update their actions so no player gets delayed and the game feels smooth and fair for everyone]

### Example 2: [printing system in university labs]

**Description**: 
[in computer labs many students send print jobs to the same printer and each job needs to be processed]

**Why Round-Robin works well here**: 
[round robin allows each print job to be processed for a short time then moves to the next job so no one waits too long and all students get fair access to the printer]

---

## Summary

**Key concepts I understood through these questions:**
1.I realized how threads are more practical than processes in this kind of simulation because they are lighter and share resources
2.I understood how round robin actually keeps the system fair by giving each process a chance instead of letting one process take all the time
3.I have got a better idea about how a thread moves step by step from creation until it finishes execution

**Concepts I need to study more:**
1. I still feel I need more practice with calculating waiting time and understanding more in depth 
2. I want to explore more scheduling techniques and see how they are different from round robin in real systems
