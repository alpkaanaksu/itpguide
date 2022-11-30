---
title: Iterating over Lists and Arrays
description: Visiting each element of an iterable
date: 2022-11-30
tags:
  - Iterating
  - List
  - Array
layout: layouts/post.njk
---

We can find the sum of the numbers in a list by iterating over the list/array once.
## For loop
```java
int sum = 0;

for (int i = 0; i < numbers.size(); i++) {
  sum += numbers.get(i);
}
```

## Enhanced for loop
```java
int sum = 0;

for (int number : numbers) {
  sum += number;
}
```

<a href="{{ 'https://www.oracle.com/java/technologies/javase/codeconventions-namingconventions.html' | url }}">Oracle Docs</a> 
