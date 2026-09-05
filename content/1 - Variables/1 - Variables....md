---
creation date: 2026-06-20 15:06
modification date: Saturday 20th June 2026 15:06:25
date: << [[2026-06-19]] | [[2026-06-21]] >>
---
# What Is A Variable?
![[variables comics.png]]
### Syntax
```java
🌟 // Variable naming is camelCase
dataType variableName = data; 

dataType variableName; // If declaring without data
```

Before you read this section, let me tell you this: **yes, it's literally like the term in Math but it's able to hold different types of data *(and you have to be explicit of what type of data it holds)*.** If you already have a decent grasp of it, then feel free to skip to the [[2 - Courses/Java2/1 - Variables/1.1 - The Naming Laws of Variables]]; if not, then lets go to the absolutely mind-boggling definition!

## A variable is just a container for a *single piece* of data (i.e: a box that holds a single item or even more simply: *data with a nametag*) 
*Yes, that's pretty much it...?* 

🌟 ***Practically*** however, I like to think of variables through this mindset: ***What single piece of data that I would like to easily manage?*** Take this scenario for example:

```java
    System.out.println("My age is " + 25);
    
    System.out.println("My twin's age is " + 25);
    
    System.out.println("My 3rd twin's age is " + 25);
    
    System.out.println("My 4th twin's age is " + 25);
```
*For those wondering by the way, the printing of ("My age is " + 25) is allowed through a process of **String Concatenation***

If your intention is to simply just print out these 4 exact lines with no intention to change it ever in the future, then your work is complete. However, we do live in a world in which every year, we age by one. We *could* solve that issue 
by manually changing each value like so:

```java
    System.out.println("My age is " + 26);
    
    System.out.println("My twin's age is " + 26);
    
    System.out.println("My 3rd twin's age is " + 26);
    
    System.out.println("My 4th twin's age is " + 26);
```

...and this works, but it's also **really really annoying to do this every single time**. As programmers, we must seek the ~~laziest~~ most efficient way to accomplish each task. That's when **variables** come in really handy!

```java
    int twinsAge = 26; // you could use byte instead of int if you're really fancy
    
    
    System.out.println("My age is " + twinsAge); //26
    
    System.out.println("My twin's age is " + twinsAge); //26
    
    System.out.println("My 3rd twin's age is " + twinsAge); //26
    
    System.out.println("My 4th twin's age is " + twinsAge); //26
```

This approach makes it so that changing the age of these quadruplets would just be changing a single line, **and I think managing *1 line* is better than handling *4*.**

🌟 Heck! you can **even change the value in the middle of the code**!

```java
    int twinsAge = 26; // you could use byte instead of int if you're really fancy
    
    
    System.out.println("My age is " + twinsAge); //26
    
    System.out.println("My twin's age is " + twinsAge); //26
    
    twinsAge = 29; // Change half-way!
    
    System.out.println("My 3rd twin's age is " + twinsAge); //29
    
    System.out.println("My 4th twin's age is " + twinsAge); //29
```

# Code Challenges:
*Alright!* Let's set the scene...
*In the middle of writing the setting of your TTRPG, you realized something... You want to change the date where this is all set to **1781**. So, you go back to your notes (which are written in code for some reason? why did you write your story in Java?) and realize that this is going to be a harrowing task. .*
### Instruction: Find a way to make the dates easier to change using variables

```java
	System.out.println("It's the year " +  1781);
	// Gosh... Now I got to change all of these years to 1781... How can I do that without having to manually change them all later if i change my mind AGAIN?
	
	System.out.println("In the year " +  1986 + " we saw the dragons fly for the first time...");
		System.out.println("Gosh! That Siege of Yorktown was so insane, I remember it like it was still " + 1801 + "... Wait it's still " + 1302 "? Ha! My memory must be my old memory"  );
```
## Going onwards:
[[2 - Courses/Java2/1 - Variables/1.1 - The Naming Laws of Variables]]
# References