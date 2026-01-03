---
title: "Arithmetic Promotions in Java"
seoTitle: "Arithmetic Promotions in Java"
seoDescription: "This short article is about Arithmetic Promotions in Java language programming."
datePublished: Sat Jan 03 2026 05:05:34 GMT+0000 (Coordinated Universal Time)
cuid: cmjxuaggg000c02l5fwm6exsr
slug: arithmetic-promotions-in-java
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1767416587095/ebf55eeb-ea69-4623-ba1e-8cb8c7343b00.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1767416538959/ac437a75-8bdb-4929-956a-bdaf10acc945.png

---

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1765956103709/c630d247-7739-45c0-b4bf-fbf80b9846b0.png align="center")

Java is familiar with data types and attempts to adapt both types of rational or equality expressions. There are situations where you tend to assign two variables with different data types, and the JVM attempts to mitigate this.

`short a = 100;`  
`int b = a;`

Here, the compiler knows about the fact that we can put every `short` number in integer variables, so the JVM do arithmetic promotion to the `a` variable and promotes it temporarily from `short` to `int`, without changing the original variable. But in contrast, we have a more complicated situation. Assume we want to put the `int` value in `short` variable.

`int a = 100;`  
`short b = a`

This time, the compiler knows the fact that the `int` size is bigger than `short` and we can’t put a bigger variable in a smaller one, although the `a` variable is in the range of the short variables; Although the current value of `a` fits within the range of `short`, the compiler cannot allow the assignment because the value of `a` might change in the future. Therefore, the code will not compile unless you guarantee that `a` is constant by declaring it as `final`

`final int a = 100;`  
`short b = a`

Notes:  
It is not a good idea to assign or compare different data types with each other. Try to avoid it.