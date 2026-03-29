# Reflection Questions

## Instructions
Answer the following questions about your learning experience. Each answer should be **at least 5-7 sentences** and show your understanding.

---

## Question 1: What did you learn about multithreading?

**Your Answer:**

This assignment taught me that a single program can handle several execution processes simultaneously thanks to multithreading. I comprehended how a class that implements `Runnable` can be used to produce Java threads. Additionally, I discovered that thread control involves utilizing join() and sleep() to coordinate execution in addition to executing start(). I was able to relate the thread lifecycle theory to real-world code and program behavior thanks to this assignment. I discovered that in order to maintain the proper execution order, the scheduler loop relies on precise thread management. Additionally, I discovered that threads are more appropriate for this type of simulation because they are lighter than processes. I now have a more useful understanding of multithreading overall thanks to the assignment.


---

## Question 2: What was the most challenging part of this assignment?

**Your Answer:**
The waiting time feature was the most difficult aspect of this task. The concept was simple to grasp in general, but it was more difficult to determine the precise location of the waiting time measurement in the code. I had to pay close attention to when a process actually begins to run and when it enters the ready queue. Making these modifications without altering the original Round-Robin logic presented another difficulty. Additionally, there was a lot of formatted output in the beginning code, which first made the file appear longer and more complicated. As a result, I had to divide the scheduling logic from the display portion. The functionality was simpler to develop once I had a better understanding of the queue flow.

---

## Question 3: How did you overcome the challenges you faced?

**Your Answer:**
Instead of making all the changes at once, I overcome the obstacles by working incrementally. I started by carefully reading the beginning code, paying close attention to the crucial sections like the scheduler loop, queue management, and process generation. Then, before going on to the next feature, I checked each one separately to make sure it functioned. I used System for the waiting time feature.currentTimeMillis() and monitored the precise time each process joined the ready queue. In order to comprehend what was going on in each round, I also compared the code with the program output. This made it easier for me to identify errors early on and maintain the original functionality. This method ultimately made managing the task much simpler.


---

## Question 4: How can you apply multithreading concepts in real-world applications?

**Your Answer:**
Because many programs must do numerous tasks simultaneously, multithreading is helpful. An excellent example is a web browser, where one thread manages user input while another loads content. Another example is a media player, where multiple threads update the interface and controls while one thread plays video.
Smoother performance and increased responsiveness are made possible via threads. I now have a better understanding of how scheduling allows each work to go without interfering with others thanks to this assignment. Operating systems employ the same concept to distribute CPU time among processes.
All things considered, I can now connect multithreading ideas to actual apps that I use on a regular basis.


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

[Any comments about the assignment? Was it helpful? Too easy/hard? Suggestions for improvement?]
