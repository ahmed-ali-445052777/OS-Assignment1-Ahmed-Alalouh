# Reflection Questions

## Instructions
Answer the following questions about your learning experience. Each answer should be **at least 5-7 sentences** and show your understanding.

---

## Question 1: What did you learn about multithreading?

**Your Answer:**

[I learned that multithreading is a core concept that lets a single program handle many tasks at once by sharing CPU time. I understood the full lifecycle of a thread, moving from the New state when it is created to Terminated when the process finishes. It was interesting to see how threads inside a process share resources like the processMap and processQueue while executing their own run methods. I also learned how thread states like Runnable and Waiting are managed by the scheduler using a time quantum. It was cool to see how fast the context switching happens, making all 10 to 20 processes look like they are running in parallel even though they take turns. This really helped me visualize how real operating systems manage multiple applications.]

---

## Question 2: What was the most challenging part of this assignment?

**Your Answer:**

[The most difficult part for me was definitely trying to get Feature 3 working, especially calculating the totalWaitTime correctly. It was really tricky to track the exact moment each process entered the queue and how much time it spent waiting before its next turn on the CPU. I also struggled quite a bit with the Java syntax, like when I had to modify the constructor to add priority and wait time without breaking the rest of the code. Debugging the final summary table was another headache because it kept printing in the wrong place or showing the wrong numbers at first. On top of that, using Git and VS Code for the first time to commit my changes was confusing and took me a while to get used to the workflow. These challenges really showed me how much detail goes into managing processes and how one small bracket error can stop the whole simulation]

---

## Question 3: How did you overcome the challenges you faced?

**Your Answer:**

[I solved these issues by just going through the code line by line and checking the course slides to see what I missed. For the errors, I spent a lot of time fixing the curly brackets and making sure the variables in the constructor were right. I used System.out.println to see the values of totalWaitTime in the terminal and make sure the math was actually working. Another thing that worked was moving the final table outside the main loop so it only prints once at the end. I also looked up some Java documentation for Thread.join() to understand how the scheduler waits for each process]

---

## Question 4: How can you apply multithreading concepts in real-world applications?

**Your Answer:**

[I see multithreading everywhere in the apps I use every day, especially in Web Browsers and Video Games. For example, in a browser like Chrome, each tab can run as its own thread so that if one website is slow, it doesn't freeze all my other open tabs. In games, it's really useful because one thread can handle the graphics while another thread is busy with the sound or the player's movement at the same time. This assignment showed me that without these threads, our computers would be very slow and could only do one thing at once. Using a time quantum like we did in the code is what makes everything feel fast and responsive for the user. It’s cool to see how the logic we coded is actually what runs big applications in the real world.]

---

## Additional Reflections (Optional)

### What would you like to learn more about?

[Any topics related to threading, concurrency, or operating systems that you're curious about?]

---

### How confident do you feel about multithreading concepts now?

[Rate yourself and explain: Beginner / Intermediate / Confident]

[Explain your rating - what do you understand well? What needs more practice?]

---

### Feedback on the assignment

[This assignment was actually helpful because it wasn't just reading slides; we had to fix and run real code. It was a bit hard at first with the Java syntax, but seeing the progress bars in the terminal made it more fun to finish.]
