---
title: "What is Dart? Everything You Need to Know About Google’s Programming Language"
seoTitle: "What is Dart? A Beginner-Friendly Guide to Google’s Programming Langua"
seoDescription: "Learn what Dart is, why it’s popular among developers, and how it powers Flutter apps with its fast performance, simple syntax, and seamless integration"
datePublished: Wed Jan 08 2025 06:09:48 GMT+0000 (Coordinated Universal Time)
cuid: cm5ni2e2t001s09kz6eswbd52
slug: what-is-dart-everything-you-need-to-know-about-googles-programming-language
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1736316575812/04814d12-b680-4f4b-95e8-aee491670bde.png
tags: programming-blogs, flutter, mobile-app-development, mobile-development, cross-platform-development, dart-programming-tutorial, google-dart, dart-and-flutter

---

## Introduction:

In this article, we will explore Dart, its key features, and its basic syntax to help you become familiar with this versatile programming language.

## What Is Dart?

Dart is an open-source programming language developed by Google for building mobile, web and desktop applications. It is widely used to develop Flutter applications, which allows developers to create cross-platform applications with a single code base.

## Key Features:

* **Object-Oriented**: Dart is an object oriented programming language, means it is based on the concepts of classes and objects. This makes it easy to model real-world problems. If you are familiar with any other object oriented programming language like Java or C#, then you will not feel much difference.
    
* **Type-safe**: Dart is a strongly typed language, means every variable must have a defined type. However it supports both static typing (explicit type declarations) and type inference (types deduced automatically). One of the benefit of static type checking is the ability to find bugs at compile time using Dart’s static analyzer.
    
* **Cross-Platform Development**: With Dart, we can write code once and run on multiple platforms like android, iOS, web etc. This saves time and effort since we don’t have to write separate code for each platform.
    
* **Ease Of Use**: Dart’s syntax is very clean and simple, similar to other popular languages. This helps beginners to pick up quickly and experienced developers to switch to it with ease.
    
* **Fast Performance**: Dart is compiled to:
    
    * Native machine code for mobile and desktop platforms
        
    * Javascript or web assembly for web platform
        
    
    This makes the apps run very quickly.
    
* **Asynchronous Programming**: Dart has built-in support for handling tasks that take time with **async** and **await** keywords.
    
* **Rich Built-In Libraries**: Dart has rich set of core libraries which can help developers in everyday programming tasks. For example:
    
    * dart:math: For mathematical operations
        
    * dart:async: For asynchronous programming
        
    * dart:io: For I/O related operations
        
* **Null Safety**: Dart helps prevent command programming bugs by ensuring variables can’t have a “**null**” value unless explicitly allowed. This makes our app more stable and reliable.
    

## Write First Dart Program:

To create our first Dart program, follow the steps below:

* Launch Visual Studio Code.
    
* Click on New File or select the New File option from the File menu as shown below.
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1732686823544/075ea3fb-48c3-4ff8-a825-f9a0ec6d2ee8.png align="center")
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1732686828483/a3498313-b6e2-491d-845a-350680f6785b.png align="center")
    
    Give it a name as `hello_world.dart` and select location to save the file on your machine.
    
* Paste the below code in `hello_world.dart` file.
    
    ```dart
    void main() {
      print('Hello, World!');
    }
    ```
    
* To run the program, open up terminal in Visual Studio Code and go to the location where `hello_world.dart` file is stored on your machine. Execute below command in terminal to run the program.
    
    ```bash
    dart run hello_world.dart
    ```
    
* After running the program, you will see "Hello, World!" printed to the console. Great! We have successfully created and executed our first Dart program.
    

Let's understand the code we added to our `hello_world.dart` file. The `main()` function in the code above is the **top-level function in Dart**. This is where the program execution begins. This function does not return any value, so its return type is `void`. We use the built-in `print()` function to display the text on the console.

## Basics Of Dart:

As with any other object oriented language, Dart language support the following:

* **Built-in Types**: Dart supports following built-in types.
    
    * Numbers (int, double)
        
        * ```dart
                int a = 10; 
                double pi= 3.142; 
                
                num x = 1; // x can have both int and double values
            ```
            
    * Strings (String): We can create string variables either using single or double quotes.
        
        * ```dart
                var s1 = "This is a string"; // type inference
                String s2 = "Dart is very easy to learn";
                String s3 = 'Dart is very easy to learn';
            ```
            
    * Booleans (bool)
        
        * ```dart
                bool isTrue = false;
                bool isVisible = true;
            ```
            
    * Lists (List): Dart list is denoted by a comma separated list of expressions or values, enclosed in a square brackets.
        
        * ```dart
                var list = [1, 2, 3]; // List of integers
                var colors = ['Red', 'Blue', 'Green'];// List of strings
            ```
            
    * Maps (Map - Holds key value pair similar to Dictionary in C#): The Map object is a key-value pair. Both keys and values can be of any type of object. Each key occurs only once, but we can use same value multiple times. Map is a dynamic collection which can grow or shrink at runtime.
        
        * ```dart
                var todoItem = {
                    'task':'Learn Dart',
                    'isCompleted':false
                };
                
                // We can create a map object where key and value can
                // only be of type string
                var todoList = Map<String, String>();
                todoList['firstTask'] = 'Read a book';
                todoList['secondTask'] = 'Learn Dart';
            ```
            
    * Function: Function is also a return type in dart, means we can assign function to variables or also pass function as an argument to other functions.
        
    * ```dart
            // Below function has a positional arguement text which is required
            void displayString1(String text){
                print(text);
            }
            
            // Calling above displayString1 function
            displayString1('Hello World');
            
            // Below function has an optional positional argument text
            // While calling this function we don't have to pass parameter
            void displayString2([String? text]){
                print(text == null ? 'Hello World' : text);
            }
            
            // Calling above displayString2 function
            displayString2();
            
            // Below function has named parameters with default values
            void displayString3({bool isBold = false, bool isItalic = false}){
                // Code here
            }
            
            // Calling above displayString3 function
            displayString3(isBold: true, isItalic: false);
        ```
        
* **Control Flow**: We can control the flow of our Dart code using loops and supporting statements.
    
    * `for` loop.
        
        * ```dart
                var list = ['Red', 'Blue','Green'];
                for (var i = 0; i < list.length; i++) {
                    print(list[i]);
                }
            ```
            
    * `while` loop.
        
        * ```dart
                while(condition) {
                   doSomeThing();
                }
            ```
            
    * `do-while` loop.
        
        * ```dart
                do {
                  doSomeThing();
                } while (condition);
            ```
            
    * `if-else` statements.
        
        * ```dart
                if(condition1){
                    doThis1();
                }
                else if(condition2){
                    doThis2();
                }
                else{
                    doThis();
                }
            ```
            
    * `switch` statements.
        
        * ```dart
                var status = 'TODO';
                switch (command) {
                  case 'TODO':
                    // Code Here
                  case 'INPROGRESS':
                    // Code Here
                  case 'BLOCKED':
                    // Code Here
                  case 'COMPLETED':
                    // Code Here
                  default:
                    // Unknown status
                    // Code here
                }
            ```
            
* **Classes:** Dart is an object-oriented programming language with classes. We can define classes in Dart as below.
    
    * ```dart
            class Person{
                String id;
                String name;
            
                Person(this.id, this.name);
            }
            
            // We can create an object 
            var person = Person('1', 'Manoj Kulkarni');
        ```
        

## Naming Convention:

* To declare classes or enums we use PascalCase.
    
    * ```dart
            class Person{
                String id;
                String name;    
            }
        ```
        
* To declare variables and functions we use camelCase.
    
    * ```dart
            String name = 'Manoj';
            
            bool isValid(){
                // Code here
            }
        ```
        
* For file name, use lowercase\_with\_underscores. For example `hello_world.dart`
    

These are just some of the basic concepts related to Dart. To learn more about Dart programming language, goto [https://dart.dev/language](https://dart.dev/language)

## Quick-Tip:

[DartPad](https://dartpad.dev/) is an online editor which we can use to learn more about Dart syntax and to experiment the Dart language features.

## Conclusion:

In conclusion, Dart is a powerful and versatile programming language developed by Google, designed for building mobile, web, and desktop applications. Its object-oriented nature, type safety, and cross-platform capabilities make it an excellent choice for developers, especially those working with Flutter. With its familiar syntax and ease of use, Dart provides a smooth learning curve for those already acquainted with other object-oriented languages. By exploring its basic syntax and features, developers can effectively leverage Dart to create robust and efficient applications. I hope you found this article informative and enjoyable.

Happy Coding!