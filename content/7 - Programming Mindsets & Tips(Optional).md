
# Functional / Procedural
# Object-Oriented Programming (Lifted Straight From: [[6 - Basic Object Oriented Programming (Class & Objects)]])


# Error-Reading (Lifted Straight From: [[0.3 - Reading Errors (Optional)]])
*Alright! You got a firm grasp of what's going on in Java (Don't worry if you haven't yet though, the last 2 will make more sense as we progress).* **Now it's time to learn what to do when things go horrifically wrong.**

From my previous experiences with teaching programming and debugging the problems of my beginner colleagues, I notice one thing: 🌟 **Most problems could just be solved by learning how to read the errors.** *Once you get the hang of learning how to interpret your errors, then you're essentially going to 10x your understanding of your own projects!*

**This module is more of a mindset change rather than a technical lesson, so it's much better to 🌟 actually take this one to heart rather than to memorize all the terms here.** Anyways, *the terms here are ones that aren't from textbooks but instead are ones that I made up or are derived from others so...* Let's get into it!

In programming, we really only have 2 broad types of errors:🌟 **System & Logical**.

## 🌟 System Errors
**System Errors** are a collection of various errors that **crashes the program.** It encapsulates stuff from *syntax errors and mispelled words* to *infinite recursion and memory leaks.* It's by far **the easiest amongst the 2 to solve, because the computer explicitly tells you what's wrong.**

```java
Main.java:3: error: error: ';' expected
        System.out.println("Hello, world!")
                                           ^
1 error
```
(An error that pertains to a missing semi-colon)

While this may look scary (especially when it's mixed in with a bunch of other errors), you really only need to identify 3 things:

1. 🌟 The line number of the error (Main.java:3, **line 3 has the error**)
2. 🌟 What type of error (error: ';' expected, meaning... **well it expected a semi-colon**)
3. 🌟 The particular line with the error ( System.out.println("Hello, world!") )

You'll encounter various different system errors in your journey, but the 🌟 **4** **main ones you'll be seeing the most is:**
1. 🌟 **error: ';' expected** - You forgot a **semi-colon** on a line, add it
2. 🌟 **error: cannot find symbol** - You made a **typo** or the thing doesn't exist in code
3. 🌟 **error: reached end of file while parsing** - You forgot to add a **"{"** or **"}"** somewhere
4. 🌟 **error: incompatible types: X cannot be converted into Y** - Two or more incompatible data types are **combined**, either convert one to the other data type or remove it entirely 
5. 🌟 **error: bad operand types for binary operator** - Used an **operator on 2 or more incompatible data types**, convert one to the other data type, rewrite, or remove it entirely

When we're working with (slightly) more complex code-bases, you'll see a variety of different errors, it's important to tackle each mistake top to bottom, as an error in one line can cause errors in multiple. 

🌟 **When you encounter an error code that isn't self-explanatory, Google it!**

*(p.s):* Most modern IDES will detect these types of errors while you're writing your code, so make sure to always keep an eye out for **red** underlines (**yellow** underlines are mostly harmless errors, but it does guide you to standard practices)
## 🌟 Logical Errors
**Logical Errors** are a collection of various *intrapersonal* errors that **makes the program behave in a way you don't want to despite it running fine (i.e without crashing).** This is where you'll find bugs like Infinite Money glitches in video games or little behavioral quirks in software. **It's the most annoying amongst the 2, because you'll have to essentially restructure things without much guidance**

```java
public class Main {
    public static void main(String[] args) {
	    System.out.println("I will be subtracting 3 and 5);
        System.out.println(2 + 9); //Incredibly simplified logical error
    }
}
```
(An error that pertains to... well adding 2 of the wrong numbers)

Without being boring and using ChatGPT to solve this, we have a few different ways of trying to solve a logical error:
1. 🌟**Pseudo-code** - It's basically just **writing down the basic idea of each line** in plain English. This really helps when the syntax is really distracting you from the real issue.
2.  **Flowcharts** - A **visual representation of your flow**, it's a bit too abstract and cumbersome in my experience, but if you're a visual learner then give this one a go.
3. 🌟**Brute Force** - You essentially **force the solution** by **dumbing down your logic** to **solve an incredibly specific problem.** I *highly recommend this way of solving because it helps rebuild your logic from the bottom up.*
4. 🌟**Duck** - It's **explaining to an object** (traditionally a rubber duck) about the program and its issues. It's a technique used to double-check your internal logic by explaining it in real-life. *Sounds absurd, but it does work.*
5.  **Braindump** - Grab a notebook, and **write down everything that comes to mind** (even if it's not even about progamming.) This helps offload a ton of mental luggage and may even reveal a hidden Freudian solution. 
# General Tips 
## To Nest or Not To Nest ([[4.4b Mini - Nesting]])
For the *most part* though, it's rather good practice to *avoid **Nesting***, especially if the logic is rather long:
```java
int age = 17;
boolean hasTicket = true;
boolean hasGuardian = false;
boolean isVIP = false;

if (age >= 18) {
    if (hasTicket) {
        if (isVIP) {
            System.out.println("Welcome, VIP!");
        } else {
            System.out.println("Welcome!");
        }
    } else {
        System.out.println("You need a ticket.");
    }
} else {
    if (hasGuardian) {
        if (hasTicket) {
            System.out.println("You may enter with your guardian.");
        } else {
            System.out.println("You still need a ticket.");
        }
    } else {
        System.out.println("You need a guardian to enter.");
    }
}
```

This works, but it's best to rewrite the logic a little bit for easier readability:
```java
int age = 17;
boolean hasTicket = true;
boolean hasGuardian = false;
boolean isVIP = false;

if (age < 18 && !hasGuardian) {
    System.out.println("You are under 18 and need a guardian.");
} else if (!hasTicket) {
    System.out.println("You need a ticket.");
} else if (isVIP) {
    System.out.println("Welcome, VIP!");
} else {
    System.out.println("Welcome!");
}
```

*Personally,* I believe that you shouldn