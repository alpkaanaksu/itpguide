---
title: Exceptions
description: Catch exceptions and create new custom ones.
date: 2022-12-05
tags:
  - Try/Catch
  - Exceptions
layout: layouts/post.njk
---

Using exceptions is a way of communicating errors between methods.

## Creating custom exceptions
You can create your own exceptions by extending the Java RuntimeException class. Let's create a new exception called UpperCaseNotFoundException.

We can start by creating a class called `UpperCaseNotFoundException`.

If you want your new exception to be checked (i.e. the calling code **must** handle the exception), extend the `Exception` class.

```java
public class UpperCaseNotFoundException extends Exception {
    // ...
}
```

If you want your new exception to be unchecked (i.e. you are allowed to use the code without handling the exception), extend the `RuntimeException` class. All runtime exceptions are unchecked.

```java
public class UpperCaseNotFoundException extends RuntimeException {
    // ...
}
```

You can then create the constructor(s) for your new exception.

```java
public class UpperCaseNotFoundException extends Exception/RuntimeException {
    public UpperCaseNotFoundException() {
        super();
    }
}
```

You can also create a constructor with a message if you want your new custom exception to have a message.

```java
public class UpperCaseNotFoundException extends Exception/RuntimeException {
    public UpperCaseNotFoundException(String message) {
        super(message);
    }
}
```

## Exception Handling
When you want to run a line of code, which might throw an exception, you should write it in a try/catch block. You write your code in the `try` block and handle the exception in the `catch` block, for example:

```java
try {
    maybeThrowException();
} catch(Exception e) {
    System.out.println("An exception was thrown!");
}
```