---
creation date: 2026-06-20 15:06
modification date: Saturday 20th June 2026 15:06:25
date: << [[2026-06-19]] | [[2026-06-21]] >>
---
## IF Only There Was A Solution
### Syntax
```java
if(condition){
	System.out.println("This condition is true!);
}

// Or if you want something to happen if the condition is false

if(condition){
	System.out.println("This condition is true!);
} else {
	System.out.println("This condition is false!);
}

// OR if you want something *specific* to happen if the condition is false

if(condition){
	System.out.println("This condition is true!);
	
} else if (secondCondition) {
	System.out.println("The second condition is true if the first condition is false!);
	
} else {
	System.out.println("Both conditions are false!");
}
```

The programming concept that everyone (*yes, including your boss*) is totally familiar with is **If Statements**, and it's for a good reason: **it's actually as simple as it seems.** 

In a majority of programming languages (including Java), we have 3 main types of *If Statements*:
1. [[3.2 - The Normal If]] - If true, then execute; If false, then skip.
2. [[3.3 - If & Else]] - If true, then execute; If false, then execute something else
3. [[3.4 - If & Else If]] - If true, then execute; If false BUT something else is true, then execute something else.


Now lets get back to our scenario:
*Sick! but what **if** I wanted to make **someone** automatically **age by 1** after **1 year** without having to **manually changing the value myself** because **I am kinda lazy to do that**.
```java
    int[] siblingAges = {26, 21, 20, 19};
    System.out.println("My age is " + siblingAges[0]); // First item
```

You can solve this issue as such:
```java
   int yearSinceCodeExecution = 0;
   int[] siblingAges = {26, 21, 20, 19};
   
   	if(yearSinceCodeExecution > 0){
		siblingAges[0]++; // a simple way to say x + 1
	}
	
  System.out.println("My age is " + siblingAges[0]); // 26
  
  yearSinceCodeExecution++; // This is a simple way to say x + 1
  
  System.out.println("My age after a year is " + siblingAges[0]); // 27
```

 **Wait!** but what if the year is less than 0? Do we age back one year? Sure, we can do that!
```java
   int yearSinceCodeExecution = 0;
   int[] siblingAges = {26, 21, 20, 19};
   	if(yearSinceCodeExecution > 0){
		siblingAges[0]++;
	} else { 
		siblingAges[0]--; // a simple way to say x - 1
	}
  System.out.println("My age is " + siblingAges[0]); // 26
  yearSinceCodeExecution--; // This is a simple way to say x - 1
  System.out.println("My age after a year is " + siblingAges[0]); // 27
```

**Wait again!** but what if by year is -90 and we want to age 100 years? *Erm... sure?*
```java
   int yearSinceCodeExecution = 0;
   int[] siblingAges = {26, 21, 20, 19};
   	if(yearSinceCodeExecution > 0){
		siblingAges[0]++;
	} else if (yearSinceCodeExecution == -90){ 
		siblingAges[0] += 100; // simple way to say x + 100
	} else {
		siblingAges[0]--; // this will run if the years is LESS than zero and NOT equal to 60. Or in layman's terms: This is the fail-safe
	}
  System.out.println("My age is " + siblingAges[0]); // 26
  yearSinceCodeExecution == -90 // This is a simple way to say x + 1
  System.out.println("My age after a year is " + siblingAges[0]); // 27
```
**Wai-** I'll have to stop you right there, you're going to make this more complicated than it needs to be. *Understand the syntax and the table, and you can figure out the rest*.

**No but seriously, there's a bug!** The code will *only always age by 1 year*, even if the *yearSinceCodeExecution* variable is set to 900! 

The issue is that what we actually need is to make this code **iterate** and therefore needs to be **looped**. Alas, *Java cannot handle such a concept...* I suppose we're forever stuck with this broken piece of co-