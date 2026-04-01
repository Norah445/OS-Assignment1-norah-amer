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

### Entry 1 - [April 2, 2026, 11:00 AM]
**What I did**:  Initialized the project structure and created the main class.

**Details**:* Created the Main.java file to serve as the entry point for the assignment.
• Defined the basic class structure and added the public static void main method.
• Verified that the compiler (javac) and JVM (java) are working correctly with the new file.


**Challenges**: Encountered a "class not found" error when trying to run the compiled file from a different directory.

**Solution**:  Navigated to the specific project folder in the terminal and used the correct command: java Main.

**Time spent**: 30 minutes

---

### Entry 2 - [April 4, 2026, 4:30 PM]
**What I did**:  Implemented basic Process management logic using Java.

**Details**: * Researched the ProcessBuilder class to handle system-level commands as required by the OS assignment.
• Wrote a test block to execute simple shell commands like ls (for Linux/Mac) or dir (for Windows).
• Captured the output stream to display the results in the console.

**Challenges**:  Understanding the difference between Runtime.getRuntime().exec() and ProcessBuilder.

**Solution**: Chose ProcessBuilder because it provides better control over the working directory and handling of input/output streams.

**Time spent**:  1 hour 15 minutes

---

### Entry 3 - [April 6, 2026, 8:15 PM]
**What I did**: Debugging environment variables and refining code.

**Details**:* Updated the code to handle IOException when a command fails to execute.
• Tested the program with multiple system commands to ensure stability.
• Updated the README.md file with instructions on how to run the project.
**Challenges**: The program crashed when trying to execute a command that doesn't exist on the system.

**Solution**: Added a try-catch block to gracefully handle exceptions and print a user-friendly error message.

**Time spent**: 45 minutes

---

### Entry 4 - [Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

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
