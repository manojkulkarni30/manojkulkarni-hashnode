---
title: "Const vs Readonly in C#"
seoTitle: "Const vs Readonly in C#"
seoDescription: "Learn about the difference between const and readonly keywords in C#"
datePublished: Wed Oct 04 2023 06:47:21 GMT+0000 (Coordinated Universal Time)
cuid: clnbdz4nu000309ladksqbe3d
slug: const-vs-readonly-in-csharp
tags: csharp, const, readonly, compile-time-constant, run-time-constant

---

In this article, we will talk about the two most commonly used keywords “**const**” and “**readonly**” and the difference between them. Let\`s get started.

## **const:**

* We can declare a variable as a constant using the **const** keyword in C#.
    
* We need to assign a value to a constant variable at the time of declaration by using a hard-coded value or an expression that can be fully evaluated at compile time. 
    
* Only built-in data types like int, string, boolean etc can be marked as constant variables.
    
* Once the value is assigned to a constant variable at the time of declaration, then we can\`t change its value. If we try to change the value, then we will get the compilation error “The left-hand side of an assignment must be a variable, property or indexer”. Because of this constant variables are most commonly called **Compile time constant.**
    
* The compiler compiles the constant value to every location that references it. For example, initially, we declare a constant variable with value X and we are using that variable in a method named foo(). After that we change the value to Y then we need to compile the code again so that the change will get reflected in method foo().
    
* **Constant variables are static**. So we can access constant variables using the class name.
    
* The best practice for naming the constant variable is to use Pascal casing.
    

### **readonly:**

* We can declare a variable as a readonly variable using the **readonly** keyword in C#.
    
* We can assign a value to a readonly variable at the time of declaration or in the constructor. Once the value is assigned, then we can\`t change it.
    
* As we can assign a value to readonly variable using a constructor, it can have a different value for a different constructor. Because of this readonly variables are most commonly called **Run time constants**.
    
* We can use any data type as a readonly variable.
    
* We can use static keyword with readonly variables.
    
* The best practice for naming the read-only variable is to use Pascal casing.
    

### **When to use constant and when to use readonly variable:**

So the main key points are:

* If we know that the value of the variable is not going to change in any part of our application, then we can declare that variable as a constant variable. For example, PI=3.14.
    
* If we are unsure about the value of a variable**,** but we don\`t want other classes to change the value after initialization then, we can declare that variable as readonly.
    

### **Conclusion:**

In this article, we talked about the difference between constant and readonly variables in C#. I hope you enjoyed reading the article.

Happy Coding!!!