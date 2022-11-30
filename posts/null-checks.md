---
title: Null checks
description: Avoiding the NullPointerException nightmare
date: 2022-11-30
tags:
  - null values
layout: layouts/post.njk
---

You can check if a variable is null by using the equality operator `==`, since your **really** want to compare the references in this case.

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

You can return a value which indicate that the parameters are invalid

