# Development Log

## Instructions
Document your development process as you work on the assignment. Add entries showing:
- What you worked on
- Problems you encountered
- How you solved them
- Time spent

**Requirements**: Minimum 5 entries showing progression over time.

---

## Example Entry Format:

### Entry 1 - [April 1, 2026, 2:30 PM]
**What I did**: Forked the repository and set up my student ID

**Details**: 
- Created GitHub account with university email
- Forked the starter repository
- Changed student ID on line 92 to my actual ID (441234567)
- Compiled and ran the program successfully

**Challenges**: Had to install JDK first because javac wasn't recognized

**Solution**: Downloaded JDK 17 from Oracle website and set PATH variable

**Time spent**: 30 minutes

---

## Your Development Log:

### Entry 1 - [March 26, 2026, 8:45 PM]
What I did: Set up the project and fixed Java version issues.



Forked the project and cloned it to VS Code.

Changed the student ID to 445052777.

Tried to run the code but it gave me errors about the Java version.

Challenges: My laptop had an old Java version (JDK 8) and the project needed a newer one to run the colors and some functions properly.

Solution: I had to delete the old JDK and download JDK 17. It took some time to fix the Environment Variables (PATH) so VS Code could see the new Java. After that, the code compiled perfectly.

Time spent: about 1 hour .

---

### Entry 2 - [March 26, 2026, 11:30 PM]
What I did: Added the Priority feature.



Added int priority variable to the Process class.

Updated the constructor and added a getter for it.

Made the loop in main create a random priority (1 to 5) for each process.

Updated the print message to show the priority.

Challenges: I got some "red lines" under the code in the main method after I changed the constructor.

Solution: I forgot that I added a new parameter to the Process. I fixed it by passing the priority variable in the new Process() call. Now it shows the priority in the terminal.

Time spent: 1 hour.
---

### Entry 3 - [March 27- 10:40 pm]
Today I worked on the Context Switches feature. I added a simple counter called 'contextSwitches' in the main class. 

I made the counter increase by 1 every time the scheduler pulls a process from the queue to start its quantum. It was a bit confusing at first where to put the ++ exactly, but I put it right before the thread starts to make sure it counts every single switch. At the end, I added a print line to show the total number. 

It's working fine now and showing 31 switches in my last run. 
TTime spent: 45 minutes 

### Entry 4 - [March 29 -8:30 pm]
What I worked on:
Implemented Feature 3 by adding creationTime, lastReadyTime, and totalWaitTime to the Process class. I also developed a final summary table that displays each process’s burst time and total waiting time at the end of the simulation.
Problems I encountered:
I faced several compilation errors due to the constructor changes and bracket issues {} that caused "undefined" errors. Additionally, the summary table was initially repeating multiple times in the terminal instead of appearing just once.
How I solved them:
I refactored the constructor to be compatible with the existing code and carefully fixed the curly brackets to ensure the class structure was correct. I also moved the table printing logic to the end of the main method to ensure a clean final output.
2:30 hours


### Entry 5 - [Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

### Entry 6 - [Optional - Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

## Summary

**Total time spent on assignment**: [X hours]

**Most challenging part**: 

**Most interesting learning**: 

**What I would do differently next time**: 
