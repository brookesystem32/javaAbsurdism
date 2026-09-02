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

Before you read this section, let me tell you this: **yes, it's literally like the term in Math but it's able to hold different types of data *(and you have to be explicit of what type of data it holds)*.** If you already have a decent grasp of it, then feel free to skip to the [[1.1 - The Naming Laws of Variables]]; if not, then lets go to the absolutely mind-boggling definition!

## A variable is just a container for a *single piece* of data (i.e: a box that holds a single item)
*Yes, that's pretty much it...?* 

🌟 ***Practically*** however, I like to think of variables through this mindset: ***What single piece of data that I would like to easily manage?*** Take this scenario for example:

```java
    System.out.println("My age is " + 25);
    
    System.out.println("My twin's age is " + 25);
    
    System.out.println("My 3rd twin's age is " + 25);
    
    System.out.println("My 4th twin's age is " + 25);
```
*For those wondering by the way, the printing of ("My age is" + 27) is allowed through a process of **String Concatenation***

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

This approach makes it so that changing the age of these quadruplets would just be changing a single line, **and I think managing *1 line* is better than handling *4*.

🌟 Heck! you can **even change the value in the middle of the code**!

```java
    int twinsAge = 26; // you could use byte instead of int if you're really fancy
    
    
    System.out.println("My age is " + twinsAge); //26
    
    System.out.println("My twin's age is " + twinsAge); //26
    
    twinsAge = 29; // Change half-way!
    
    System.out.println("My 3rd twin's age is " + twinsAge); //29
    
    System.out.println("My 4th twin's age is " + twinsAge); //29
```

## Going onwards:
[[1.1 - The Naming Laws of Variables]]
# References