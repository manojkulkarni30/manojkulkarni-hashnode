---
title: "🚀 How to Use Images in Flutter? | Complete Guide 🖼️"
seoTitle: "Flutter Images: A Complete Guide"
seoDescription: "Learn to incorporate images in Flutter apps using assets or internet links with Image.asset and Image.network widgets for enhanced visual appeal"
datePublished: Tue Apr 15 2025 10:33:35 GMT+0000 (Coordinated Universal Time)
cuid: cm9id792j001e09ladopohbdr
slug: how-to-use-images-in-flutter-complete-guide
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1743842943187/1de14237-67ab-46a9-ab4d-09afd8e9c428.png
tags: flutter, flutter-image-widget, image-asset, image-network

---

## Introduction:

In this article, we will explore the process of incorporating images into a Flutter application, enhancing its visual appeal and user experience.

## How To Use Image From Asset Folder?

* Let’s create a Flutter project by executing below command in terminal.
    
    ```bash
    flutter create my_image_app
    ```
    
* Navigate to the project folder by executing below command.
    
    ```bash
    cd my_image_app
    ```
    
* Open the project in Visual Studio Code.
    
* Create a folder called **asset** in project’s root directory and add images to that folder.
    
* Now open up `pubspec.yaml` file, add the path of our images under **assets** section as shown below.
    
    ```yaml
    flutter:
      assets:
        - assets/<filename-with-extension>
    ```
    
* If you have multiple images, then just specify the directory name as shown below and save the changes.
    
    ```yaml
    flutter:
      assets:
        - assets/
    ```
    
* Open up **main.dart** file and use **Image.asset** widget to display the image from asset folder as shown below.
    
    ```dart
    class MyHomePage extends StatelessWidget {
      const MyHomePage({super.key, required this.title});
    
      final String title;
    
      @override
      Widget build(BuildContext context) {
        return Scaffold(
          appBar: AppBar(
            backgroundColor: Theme.of(context).colorScheme.inversePrimary,
            title: Text(title),
          ),
          body: Center(
            child: Column(
              mainAxisAlignment: MainAxisAlignment.center,
              children: <Widget>[Image.asset('assets/<filename-with-extension>')],
            ),
          ),
        );
      }
    }
    ```
    
* Save the changes and let’s run the application.
    
* Image will get displayed as shown below.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1743840546491/63f30f62-c495-4eb1-aaf2-3ef78905a876.png align="center")

## How To Use Image From Internet?

* Displaying an image from internet is super easy. Instead of **Image.asset** widget, we use **Image.network** widget and instead of **image path**, we use **image URL** as shown below.
    
    ```dart
    class MyHomePage extends StatelessWidget {
      const MyHomePage({super.key, required this.title});
    
      final String title;
    
      @override
      Widget build(BuildContext context) {
        return Scaffold(
          appBar: AppBar(
            backgroundColor: Theme.of(context).colorScheme.inversePrimary,
            title: Text(title),
          ),
          body: Center(
            child: Column(
              mainAxisAlignment: MainAxisAlignment.center,
              children: <Widget>[Image.network('<image-url>')],
            ),
          ),
        );
      }
    }
    ```
    
* Save the changes and run the application.
    

## How To Add Filtering Effect To An Image?

The Image widget has various properties that you can use to customize the look of an image. For instance, you can change the width and height of the image, as well as apply a filtering effect.

```dart
class MyHomePage extends StatelessWidget {
  const MyHomePage({super.key, required this.title});

  final String title;

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        backgroundColor: Theme.of(context).colorScheme.inversePrimary,
        title: Text(title),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            Image.asset(
              'assets/<filename-with-extension>',
              width: 400,
              height: 400,
              color: Colors.amber,
              colorBlendMode: BlendMode.darken,
            )
          ],
        ),
      ),
    );
  }
}
```

Save the changes and let’s run the application. The image will look like this:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1743842474800/c93e1322-6f74-4a35-9541-ae42493b8400.png align="center")

I have also created a YouTube video regarding this topic, so if you would like to watch a video tutorial, then please go to [https://youtu.be/kTa6cPppI-4](https://youtu.be/kTa6cPppI-4).

%[https://youtu.be/kTa6cPppI-4] 

## Conclusion:

In conclusion, using images in a Flutter application is a straightforward process that enhances the visual appeal and user experience. Whether you're using images from the asset folder or fetching them from the internet, Flutter provides flexible widgets like `Image.asset` and `Image.network` to make the process seamless. Additionally, Flutter offers various properties to customize images, such as adjusting size and applying filtering effects, allowing developers to create visually engaging applications. By following the steps outlined in this guide, you can effectively incorporate images into your Flutter projects and elevate your app's design. I hope this article helped!

Happy coding!