[Home](./README.md)       
[The Growth Mindset](./README2.md)    
[ Practice in the Terminal](./Terminal.md)   
[Introduction to SQL](./sql.md)    
   [Read:Class 01](./Read%3AClass01.md)

# Introduction 
Debugging and Try/Catch blocks are important for learning C# and .NET because they allow you to handle and resolve errors in your code, improving its reliability and stability.

Exception handling helps you identify and gracefully handle unexpected errors, preventing crashes and providing a better user experience.

Understanding debugging and Try/Catch blocks in C# and .NET empowers you to troubleshoot issues effectively, leading to more efficient and robust software development.
 





 ## Answering the questions 

-----
**1- Name one major benefit of being able to trace the call stack.**
- the debugger actively monitors everything that’s happening as the program runs. It also allows you to pause the app at any point to examine its state and then step through your code line by line to watch every detail as it happens.

**2-If you could use try/catch in your day to day life, name an exception you’d like to ‘catch’ and handle.**
- I would like to catch and handle in my day-to-day life is a "DivideByZeroException". This exception occurs when attempting to divide a number by zero, which is mathematically undefined. By catching and handling this exception, I can display a custom error message to the user, such as "Cannot divide by zero. Please enter a non-zero divisor." This helps prevent unexpected crashes and provides clear guidance to the user on how to correct their input.

**3-From an efficiency standpoint, are there downsides to try/catch blocks?**
- Performance impact: The presence of try/catch blocks introduces additional overhead in terms of performance. When an exception occurs, the program flow is interrupted, and the runtime needs to handle the exception, which can result in slower execution compared to error-free code.

- Code readability: Excessive or unnecessary try/catch blocks can make the code harder to read and understand. It's important to strike a balance between error handling and code clarity.


**4-Describe how you explain the .Net approach to exception handling to a non technical friend.**

In .NET, exception handling is like having a safety net for your code. We use try/catch blocks to catch and handle unexpected errors. The try block contains the code that might cause an exception, and the catch block is where we handle the exception by taking appropriate actions. This approach ensures that even if errors occur, the program can continue running smoothly and provide a better user experience.

**5-Name glaring mistakes that were made during the production of these systems.**

- Therac-25: The six documented accidents occurred when the high-current electron beam generated in X-ray mode was delivered directly to patients. Two software faults were to blame. One, when the operator incorrectly selected X-ray mode before quickly changing to electron mode, which allowed the electron beam to be set for X-ray mode without the X-ray target being in place. A second fault allowed the electron beam to activate during field-light mode, during which no beam scanner was active or target was in place. so its all due to the lack of proper interlocks and safety mechanisms. The software allowed the machine to be operated in a dangerous mode where it delivered high doses of radiation without adequate safeguards, leading to multiple incidents of patient overdoses.

- Ariane 5:the reuse of software code from the previous Ariane 4 rocket without appropriate modifications. The Ariane 4 code included data that exceeded the capacity of a 16-bit integer, causing an integer overflow error during the flight of Ariane 5. This led to the rocket's failure and loss of the mission.

## Things I want to know more about 
---
- git to look at more of the Case Studies and how these systems is programmed .