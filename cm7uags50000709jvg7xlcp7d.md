---
title: "Decoding Dart: Understanding the Difference Between Const and Final"
seoTitle: "Const vs Final in Dart Explained"
seoDescription: "Learn the key differences between const and final in Dart with real-world examples for more efficient coding in your Flutter apps"
datePublished: Tue Mar 04 2025 09:30:50 GMT+0000 (Coordinated Universal Time)
cuid: cm7uags50000709jvg7xlcp7d
slug: decoding-dart-understanding-the-difference-between-const-and-final
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1740976998751/2348f1e7-4924-4277-9761-e1f0d62403d6.png
tags: dart, dart-programming-tutorial, final-keyword-and-const-keyword

---

## Introduction:

In this article, we will explore what is the exact difference between **const** and **final** in Dart.

Whether you’re building a **Flutter app** or just learning **Dart**, you’ve probably seen **const** and **final** everywhere. But here’s the thing—**they aren’t the same!** Let’s understand the difference between them with real world examples.

## What is const?

Imagine const as a job **interview time**. You’ve applied for a job, your resume made it to the shortlist, and the company has set your interview for Friday at 10 AM. So, you know the interview time in advance and it’s set in stone.

In Dart, use the const keyword for values that you know won’t change and are known at compile time. For instance:

```dart
void main() {
  const pi = 3.1416;
  pi = 3.15; // ❌ Error! Can't change const values.
}
```

## What is final?

Imagine the final result as your interview outcome. After the interview, the company will make the decision whether you’re hired or not. Once the result is out, you can’t change it. In this case, the result wasn’t known before the interview. It was decided at runtime after the interview.

In Dart, use a final variable when the value is set only once but can be determined at runtime. For instance:

```dart
void main() {
  final interviewResult = getResult();  // Decided at runtime
  print(interviewResult);
}

String getResult() {
  return "Congratulations! You got the job!";
}
```

I have also created a YouTube video regarding this topic, so if you would like to watch a video tutorial, then please go to [https://youtu.be/Dv1YXhQZBQg](https://youtu.be/Dv1YXhQZBQg)

%[https://youtu.be/Dv1YXhQZBQg] 

## [Conclusion:](https://youtu.be/fHFgE51NZhk)

Understanding the difference between const and final in Dart is super important for writing efficient code. const is like a fixed interview time - you know it beforehand and it stays the same. On the other hand, final is like the result of an interview - you set it once and it’s set in stone. By using these keywords correctly, you can write code that’s easier to understand and maintain. I hope this article helped!

Happy coding!