# Control Structure

## Introduction
-----------------------------
**Control statements** enable us to specify the flow of program control; ie, the order in which the instructions in a program must be executed. They make it possible to make decisions, to perform tasks repeatedly or to jump from one section of code to another.

## Types of Control Structure
-----------------------------
### **Decision making or branching statements:**
Conditional Statements or branching statements in C programming are used to make decisions based on the conditions. Conditional statements execute sequentially when there is no condition around the statements. If you put some condition for a block of statements, the execution flow may change based on the result evaluated by the condition. This process is called decision making in 'C.'

#### **if statement:**
_if statement is the most simple decision making statement. It is used to decide whether a certain statement or block of statements will be executed or not i.e if a certain condition is true then a block of statement is executed otherwise not._

The syntax for if statement is as follows:

```c
if (condition)
{ 
    Statement(s);
} 
```
_The condition evaluates to either true or false. True is always a non-zero value, and false is a value that contains zero. Instructions can be a single instruction or a code block enclosed by curly braces { }._

#### **if-else statement:**
_The if statement alone tells us that if a condition is true it will execute a block of statements and if the condition is false it won’t. But what if we want to do something else if the condition is false. Here comes the C else statement. We can use the else statement with if statement to execute a block of code when the condition is false._

The syntax for if else statement is as follows:
```c
if (condition)
{
    Statement(s);
}
else
{
    Statement(s);
}
```
_The block of code following the else statement is executed as the condition present in the if statement is false._

#### **if-else-if statement:**
_Here, a user can decide among multiple options. The C if statements are executed from the top down. As soon as one of the conditions controlling the if is true, the statement associated with that if is executed, and the rest of the C else-if ladder is bypassed. If none of the conditions are true, then the final else statement will be executed._

Syntax:
```c
if (condition)
{
    Statement(s);
}
else if (condition)
{
    Statement(s);
}
.
.
else
{
    Statement(s);
}
```
#### **Switch statement:**
_Switch statement in C tests the value of a variable and compares it with multiple cases. Once the case match is found, a block of statements associated with that particular case is executed._

_Each case in a block of a switch has a different name/number which is referred to as an identifier. The value provided by the user is compared with all the cases inside the switch block until the match is found._

_If a case match is NOT found, then the default statement is executed, and the control goes out of the switch block._

_The switch statement allows us to execute one code block among many alternatives._

_You can do the same thing with the ``if-else-if`` ladder. However, the syntax of the ``switch`` statement is much easier to read and write._

Syntax:

```c
switch (expression)
​{
    case (value-1):
    {
        Statement(s);
        break;
    }
    case (value-2):
    {
        Statement(s);
        break;
    }
    .
    .
    .
    default:
    {
        // default statements
        Statement(s);
    }
}
```
### **Looping statements:**
Loops in programming come into use when we need to repeatedly execute a block of statements.

A Loop executes the sequence of statements many times until the stated condition becomes false. A loop consists of two parts, a body of a loop and a control statement. The control statement is a combination of some conditions that direct the body of the loop to execute until the specified condition becomes false. The purpose of the loop is to repeat the same code a number of times.

Depending upon the position of a control statement in a program, looping in C is classified into two types:

* **Entry Controlled loops** : _In this type of loops the test condition is tested before entering the loop body. ``For Loop`` and ``While Loop`` are entry controlled loops._

* **Exit Controlled Loops** : _In this type of loops the test condition is tested or evaluated at the end of loop body. Therefore, the loop body will execute atleast once, irrespective of whether the test condition is true or false. ``do – while loop`` is exit controlled loop._

'C' programming language provides us with three types of loop constructs:

* For Loop
* While Loop
* Do-while Loop

#### **For Loop:**
_A for loop is a repetition control structure which allows us to write a loop that is executed a specific number of times. The loop enables us to perform n number of steps together in one line._

Syntax:
```c
for(Initialization Expression;Condition;Inc/Dec) 
{
    Statement(s);
}
```
_In for loop, a loop variable is used to control the loop. First initialize this loop variable to some value, then check whether this variable is less than or greater than counter value. If statement is true, then loop body is executed and loop variable gets updated . Steps are repeated till exit condition comes._

* **Initialization Expression** : _In this expression we have to initialize the loop counter to some value. for example: ``int i=1;``_
* **Condition** :_In this expression we have to test the condition. If the condition evaluates to true then we will execute the body of loop and go to Inc/Dec expression otherwise we will exit from the for loop. For example: ``i <= 10;``_
* **Inc/Dec** : _After executing loop body this expression increments/decrements the loop variable by some value. for example: ``i++;``_

#### **While Loop:**
_While studying for loop we have seen that the number of iterations is known beforehand, i.e. the number of times the loop body is needed to be executed is known to us. while loops are used in situations where we do not know the exact number of iterations of loop beforehand. The loop execution is terminated on the basis of test condition._

Syntax:
```c
Initialization Expression;
while (Condition)
{
    Statement(s);
    Inc/Dec;
}
```
#### **Do-while Loop:**
_In do while loops also the loop execution is terminated on the basis of test condition. The main difference between do while loop and while loop is in do while loop the condition is tested at the end of loop body, i.e do while loop is exit controlled whereas the other two loops are entry controlled loops._

>Note: In do while loop the loop body will execute at least once irrespective of test condition.

Syntax:
```c
Initialization Expression;
do
{
    Statement(s);
    Inc/Dec;
} while (Condition);
```
>Note: Notice the semi – colon ``;`` in the end of loop.

### **Jumping statements:**
Jumping statements are used to manipulate the flow of the program if some conditions are met. It is used to terminating or continues the loop inside a program or to stop the execution of a function.  In C there is four jump statement: continue, break, return, and goto.

#### **Goto:**
_This statement is used to jump directly to that part of the program to which it is being called.  Every ``goto`` statement is associated with the label which takes them to part of the program for which they are called. The label statements can be written anywhere in the program it is not necessary to use before or after goto statement. This statement makes it difficult to understand the flow of the program therefore it is avoided to use it in a program._

Syntax:

```c
goto label_name;
Statement(s);
.
.
.
label_name:
```
#### **Continue:**
_It is used to execute other parts of the loop while skipping some parts declared inside the condition, rather than terminating the loop, it continues to execute the next iteration of the same loop. It is used with a decision-making statement which must be present inside the loop. This statement can be used inside ``for`` loop or ``while`` or ``do-while`` loop._

Syntax:
```c
continue;
```

#### **Break:**
_It is used to terminate the whole loop if the condition is met. Unlike the continue statement after the condition is met, it breaks the loop and the remaining part of the loop is not executed. Break statement is used with decision-making statements such as ``if``, ``if-else``, or ``switch`` statement which is inside the for loop which can be ``for`` loop, ``while`` loop, or ``do-while`` loop. It forces the loop to stop the execution of the further iteration._

Syntax:
```c
break;
```

#### **Return:**
_It takes control out of the ``function`` itself. It is stronger than a break. It is used to terminate the entire function after the execution of the function or after some condition. Every function has a return statement with some returning value except the ``void()`` function. Although ``void()`` function can also have the return statement to end the execution of the function._

Syntax:
```c
return (expression);
```















