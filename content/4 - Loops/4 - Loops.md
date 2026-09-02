## Loops
![[Untitled design (4).png]]
### Syntax
```java
// FOR LOOP
for (initialization; condition; update) {
    // Code to be executed repeatedly
}


// WHILE LOOP
while (condition) {
    // Code to be executed repeatedly
}


// DO-WHILE LOOP
do {
    // Code to be executed repeatedly
} while (condition);
```
In the context of programming, a **Loop** is just a series of **iterating and repeating [[3 - If Statements]]. While we have a few different types of looping *(and even one that's oddly psychedelic),* all loops fundamentally do the same 4 steps:
1. **Check** the condition 
2. If true, **execute** the commands within the curly brackets {}
3. Once done, **check** the condition again
4. **Repeat** **until** the condition is **false**

Because of this fundamental process underneath all loops, **every loop type can get the same job done (with varying degrees of simplicity)... so it's only really finding the most convenient tool for the task at hand that we should only be concerned with.** 

In Java, we have 3 basic loops: 
1. [[4.1 - While Loops]] - Keep running as long as the condition is true
2. [[4.2 - Do-While Loops]] - Run once, then run like a while loop
3. [[4.3 - For Loops and Why]] - A special while-loop variation