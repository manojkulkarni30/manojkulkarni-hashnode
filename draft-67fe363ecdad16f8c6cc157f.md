---
title: "Mastering Custom Fonts in Flutter: A Step-by-Step Guide"
slug: mastering-custom-fonts-in-flutter-a-step-by-step-guide
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1744716243080/031e0127-493d-4285-9395-6570fa7242a2.png

---

## Introduction:

In this article, we will take a detailed look at how to incorporate custom fonts into a Flutter application, guiding you through the process step-by-step.

## Prerequisite:

Flutter support three font formats:

* OpenType font collections (`.ttc`)
    
* TrueType font (`.ttf`)
    
* OpenType font (`.otf`)
    

So make sure your font is in one of those formats. For this blog post, I will be using **Oswald** font from Google Fonts.

## Steps:

* Let’s create a Flutter project by executing below command in terminal.
    
    ```dart
      flutter create custom_font_app
    ```
    
* Navigate to the project folder by executing below command.
    
    ```dart
      cd custom_font_app
    ```
    
* Open the project in Visual Studio Code.
    
* Create a folder called **asset/font** in project’s root directory and add font files to that folder.
    
* Now open up `pubspec.yaml` file, add the below details under **fonts** section as shown below.
    
    ```yaml
    fonts:
        - family: Oswald
          fonts:
            - asset: assets/fonts/Oswald-Regular.ttf
            - asset: assets/fonts/Oswald-Bold.ttf
              weight: 700
    ```
    
    Using `family`, we can specify the name of the font (It should be unique). The `asset` property represent path of the font file from project’s root directory. The `weight` property specifies the weight of the font (An integer value between 100 to 900).
    
* We can now apply Oswald font to any text widget as shown below.
    

```dart
  Text
    (
      "Hello Flutter!",
      style: TextStyle(fontFamily: "Oswald", fontWeight: FontWeight.bold, fontSize: 24),
    ),
```

* Save the change and let’s run the application.
    
* Result is as shown below.
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1744715549680/7e25827e-9c24-48b2-855b-f959d6178552.png align="center")
    
    If you want to apply the font to whole application, then we can specify the font family under theme under section in **MaterialApp** widget as shown below.
    

```dart
    MaterialApp(
      title: 'Flutter Demo',
      theme: ThemeData(
        fontFamily: "Oswald",
        colorScheme: ColorScheme.fromSeed(seedColor: Colors.deepPurple),
        useMaterial3: true,
      ),
      home: CounterScreen(
        title: "Custom Font App",
      ), // Update this line
    );
```

* Save the change and run the application.
    
* Result is as shown below.
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1744715856096/510a3460-9a0b-4eba-b52a-05b11d271eab.png align="center")
    

I have also created a YouTube video regarding this topic, so if you would like to watch a video tutorial, then please go to.

## Conclusion:

In conclusion, incorporating custom fonts into a Flutter application is a straightforward process that enhances the visual appeal and branding of your app. By following the steps outlined in this article, you can easily add and apply custom fonts to individual text widgets or the entire application. This flexibility allows for a more personalized and cohesive user experience. Whether you prefer written instructions or a video tutorial, the resources provided will guide you through the process, ensuring your Flutter app stands out with its unique typography. I hope this article helped.

Happy Coding!