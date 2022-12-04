---
title: Using conditional statements
description: Deciding on how the program should continue based on conditions
date: 2022-11-30
tags:
  - If-statments
  - Switches
layout: layouts/post.njk
---

We can determine which the program should follow based on coditions. In case the condition for your if statement resolves to true, the statement will be accessed and the regarding code will be executed. If not, it will be ignored and not executed.
## If statment
```java
boolean conditiion = true;

if (condition) {
  //do something
} 
```

You can actually check for different conditions. So in case the first one doesn't resolve to true, your program will go on and check the succeeding ones. You can actually add as many of those as you want to. Depending on the use case you might also consider using a switch which is explained down below.
## Else if statment
```java
int num = 1;

if (num == 2) {
  //do something
} else if (num == 1) {
  //do something
}
```
The else statement is your default of some kind. So if neither your if statement nor one of your possible else if statements gets executed, the else statement will in any case.
## Else statment
```java
boolean condition = false;

if (condition) {
  //do something
} else {
  //do something
}
```

There is different ways on how to use conditions. As of the exmaples below, you usally prefer the first two since it is not redundant. However the last two are not incorrect and in case you feel more comfortable with the later ones, you can still go with it.
## Ways to use conditions
```java
boolean condition;

if (condition) //this will resolve to true in case the value stored in condition is true and enter the statement otherwise it will resolve to false
if (!condition) //this will resolve to true in case the value stored in condition is false and enter the statement otherwise it will resolve to false
if (condition == true) //this does the same as the first but is a little longer and redundant
if (condition == false) //this does the same as 
```
Switch statements are based on the expression of your conditional variable. So you will predefine certain possible expressions of your variable and depending on that the behavior of your program. 
Important note: always make sure to add the "break;" statement at the end of your codeblock inside the case. Otherwise you will go through all of the further statements below and the code there will also be executed.
## Switch statements
```java
int expression = 1;

switch(expression) {
  case 1:
    //do something
    break;
  case 2:
    //do something
    break;
  default:
    //do something
}
```

<a href="{{ 'https://www.oracle.com/java/technologies/javase/codeconventions-namingconventions.html' | url }}">Oracle Docs</a> 
