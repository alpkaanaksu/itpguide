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

## Avoiding the ConcurrentModificationException
If you change a list while iterating over it (for example if you remove a value), the `ConcurrentModificationException` is thrown. To avoid that, you can use a normal for loop instead of an enhanced for loop and decrease the index after removing the item.

```java
for (int i = 0; i < list.size(); i++) {
  if (list.get(i).equals(itemToRemove)) {
    list.remove(i);
    i--;
  }

  // do something else
}
```
