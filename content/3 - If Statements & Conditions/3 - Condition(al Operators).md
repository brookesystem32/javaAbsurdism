---
creation date: 2026-06-20 15:06
modification date: Saturday 20th June 2026 15:06:25
date: << [[2026-06-19]] | [[2026-06-21]] >>
---
# Conditional Operators
Before you get to code [[3.1 - If Statement & Variations]], you'll need to know how to actually **determine if something is true or false** (ie: a **condition**). 

Fortunately for us, the **conditional operators** are actually rather self-explanatory! We really only have 🌟 **3 special operators** and the **rest stem from Mathematics.**

| 🌟 **Operator / Concept** | **Syntax** | **Description**                                                                                                                 | **Example**                                                                        |
| ------------------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| **Equal to**              | `==`       | Checks if two values are **equal**. **It's completely different from '='**                                                      | `if (x == 5)`<br>"is *x equal to 5?*"                                              |
| **Not equal to**          | `!=`       | Checks if two values are **not equal.**                                                                                         | `if (x != 5)`<br>"is *x NOT equal to 5?*"                                          |
| **Greater than**          | `>`        | Checks if the left value is strictly **greater** than the right.                                                                | `if (score > 90)`<br>"is the score greater than 90?"                               |
| **Less than**             | `<`        | Checks if the left value is strictly **less** than the right.                                                                   | `if (temperature < 0)`<br>"is the temperature less than 0?"                        |
| **Greater than or equal** | `>=`       | Checks if the left value is **greater** than or **equal** to the right.                                                         | `if (age >= 18)`<br>"is the age greater than OR equal to 18?"                      |
| **Less than or equal**    | `<=`       | Checks if the left value is **less** than or equal to **the** right.                                                            | `if (price <= 100)`<br>"is the price less than or equal to 100?"                   |
| **Logical AND**           | `&&`       | Returns **true** only if **both** conditions are true.                                                                          | `if (hasKey && isGuard)`<br>"do you BOTH have the key AND are the guard?"          |
| **Logical OR**            | `\|\|`     | Returns **true** if **at least one** condition is true.                                                                         | `if (isWeekend \|\| isHoliday)`<br>"do this if it's EITHER a weekend OR a holiday" |
| **Logical NOT**           | `!`        | Reverses the condition; think of it as "NO!" (Basically, if something is **true** **then** it becomes **false** and vice versa) | `if (!isLoggedIn)`<br>"do this if the user is NOT logged in"                       |


```java

System.out.println(2 == 2);              // true — 2 is equal to 2

System.out.println(5 != 7);              // true — 5 is not equal to 7

System.out.println(5 > 7);               // false — 5 is not greater than 7

System.out.println(3 < 10);              // true — 3 is less than 10

System.out.println(18 >= 18);            // true — 18 is greater than or equal to 18

System.out.println(25 <= 20);            // false — 25 is not less than or equal to 20

System.out.println(5 > 2 && 10 > 5);     // true — both conditions are true

System.out.println(5 > 10 || 10 > 5);    // true — at least one condition is true

System.out.println(!(5 > 10));           // true — 5 is not greater than 10, so NOT false becomes true
```

## Moving Forward: 