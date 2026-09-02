---
creation date: 2026-06-20 15:06
modification date: Saturday 20th June 2026 15:06:25
date: << [[2026-06-19]] | [[2026-06-21]] >>
---
## Arrays
![[You did ask for the 1st box!.png]]
```java
// arrayNaming is camelCase
dataType[] name = {element1, element2, element3}; 
dataType[] name = new dataType[numberOfItems]; // When creating an empty array
```
Alright suppose that you're tired from earlier, don't worry! Arrays are actually far simpler now that we got variables under our ctrl key. 

(psstttt, the *public static void main (String[] args) thing? Yeah, you see that String[] args text? That's an array!*)

🌟 An **Array** is just a **fixed sized collection of simple data values with the same data type** (ie: a collection of [[1 - Variables...]] of the same type), think of it as the shelf of an incredibly organized person, indexes and all (but for some reason, 🌟 **the guy marked the first item as *0*, then the second item as *1*, and so forth.)**

*🌟 Since it's fundamentally a collection of [[1 - Variables...]], then it's a given that it has the same [[1.2 - and Data Types...]]!*

Lets get back to the code from before... but now everyone had a DNA test and turns out everyone was just some guy and their ages were totally off... Oopsies!
```java
    int age = 26; // you could use byte instead of int if you're really fancy

    int secondDudeAge = 21;
    int thirdDudeAge = 20;
    int fourthDudeAge = 19;
    
    System.out.println("My age is " + age);
    
    System.out.println("My brother's age is " + secondBrotherAge);
    
    System.out.println("My third brother's age is " + thirdBrotherAge);
    
    System.out.println("My fourth brother's age is " + fourthBrotherAge);
```
This actually is pretty readable (and for some professionals, this is the recommended way to go about this),

but now if we want to change their values, **we would have to change each line again!** Ugh, *the pain never stops with this programming shtick.*.. could **Arrays** help alleviate the pain?
```java
    int[] ages = {26, 21, 20, 19};
    
    System.out.println("My age is " + ages[0]); // My age is 26
    
    System.out.println("The 2nd person's age is " + ages[1]); // My 1st brother's age is 21
    
    System.out.println("The 3rd person's age is " + ages[2]); // My 2nd brother's age is 20
    
    System.out.println("The 4th person's age is " + ages[3]); // My 3rd brother's age is 20
    
    System.out.println("The 5th person's age is  " + ages[4]); // Throws an error since there's no 5th item of the ages array
```

Aha! and we even threw in an error into the code, double win! Now, how do we 🌟 **change the value of a single element of this array/collection?** It's actually the same as *modifying a variable*:

```java
    int[] ages = {26, 21, 20, 19};
    
    ages[0] = 27;
    
    System.out.println("My age is now " + ages[0]); // My age is now 27
    
    System.out.println("The 2nd person's age is still" + ages[1]); // My 1st brother's  age is 21
    
    ages[1] = 22;
    
        System.out.println("Oop! Turns out the second person's age is actually" + ages[1]); // Oop! Turns out the second person's age is actually 22
        
    System.out.println("The 3rd person's age is still " + ages[2]); // Third Item
    
    System.out.println("The 4th person's age is still " + ages[3]); // Fourth Item

```

We could also find out how many people there are by utilizing ***nameOfArray.length***
```java
    int[] ages = {26, 21, 20, 19};
    System.out.println("There is " + ages.length + " people right now!);
```

*But what if I want to print out the ages all at once?* 
That's a question for m*uch later in the course ([[4 - Loops]])* but if you wanted to figure it out with what you already know...

```java
	System.out.println(ages[0]);
	System.out.println(ages[1]);
	System.out.println(ages[2]);
	System.out.println(ages[3]);
```

