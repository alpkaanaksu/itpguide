---
title: Null checks
description: Avoiding the NullPointerException nightmare
date: 2022-11-30
tags:
  - Null Values
  - Conditionals
layout: layouts/post.njk
---

### Simple checks
You can check if a variable is null by using the equality operator `==`, since you **really** want to compare the references in this case.

```java
if (variable == null) {
  // do something
}
```

### Combining null checks and method calls
```java
if (list != null && !list.isEmpty()) {
  // do something
}
```

### Returning if a value is null
You can return a value which indicates that the parameters are invalid, for example:
```java
if (order == null) {
  return -1; // return -1, which (int this case) means that the method does not succeed.
}
```

If you are in a `void` method, you can use the `return` keyword to *exit* the method:
```java
if (order == null) {
  return; // leave the method
}
```