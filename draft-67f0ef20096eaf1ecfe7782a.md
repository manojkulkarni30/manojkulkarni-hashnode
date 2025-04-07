---
title: "🚀 How to Use SVG Images in Flutter? | Complete Guide 🖼️"
slug: how-to-use-svg-images-in-flutter-complete-guide
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1744026180074/5f58187a-636b-4cbd-9261-45bac3ff0f43.png

---

## Introduction:

In this article, we will explore the process of incorporating SVG (**Scalable Vector Graphics**) images into a Flutter application.

## Installation:

By utilizing, [**flutter\_svg**](https://pub.dev/packages/flutter_svg) package, developers can effortlessly integrate SVG images in Flutter application. To add flutter\_svg package to our Flutter application, open up `pubspec.yaml` file and add below code.

```yaml
dependencies:
  flutter_svg: ^2.0.17
```

Save the changes and execute below command in terminal to install the package in our Flutter application.

```bash
flutter pub get
```

## How To Use SVG Image From An Asset Folder?

* Now the package is installed, we can start using SVG images in our Flutter application.
    
* Create a folder called **asset** in project’s root directory and add SVG images to that folder.
    
* Now open up `pubspec.yaml` file, add the path of our SVG images under **assets** section as shown below.
    
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
    
* Open up **main.dart** file and use **SvgPicture.asset** widget to display the SVG image from asset folder as shown below.
    
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
              children: <Widget>[SvgPicture.asset('assets/<filename-with-extension>')],
            ),
          ),
        );
      }
    }
    ```
    
* Save the changes and let’s run the application.
    
* Image will get displayed as shown below.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1744024817634/064fc3b8-4622-445e-b190-bd3a601992a3.png align="center")

## How To Use SVG Image From Internet?

Displaying SVG image from internet is super easy. Instead of **SvgPicture.asset** widget, we use **SvgPicture.network** widget and instead of **image path**, we use **image URL** as shown below.

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
            SvgPicture.network('<image-url>')
          ],
        ),
      ),
    );
  }
}
```

Save the changes and run the application. While using SVG image from internet, just make sure your internet connection is active.

## How To Add Filtering Effect To SVG Image?

The **SvgPicture** widget has various properties that you can use to customize the look of SVG image. For instance, you can change the width and height of the image, as well as apply a filtering effect.

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
            SvgPicture.network(
              "<image-url>",
              width: 200,
              height: 200,
              colorFilter: ColorFilter.mode(Colors.amber, BlendMode.darken),
            )
          ],
        ),
      ),
    );
  }
}
```

Save the changes and let’s run the application. The image will look like this:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1744025358790/4d0f2a15-f2ae-4139-97a0-aaa98ba8c2bd.png align="center")

I have also created a YouTube video regarding this topic, so if you would like to watch a video tutorial, then please go to.

## Conclusion:

In conclusion, incorporating SVG images into a Flutter application is a straightforward process with the help of the [flutter\_svg](https://pub.dev/packages/flutter_svg) package. Whether you're using SVG images from an asset folder or directly from the internet, **SvgPicture** widget provides flexible options to display and customize SVG images. By following the steps outlined in this guide, you can enhance your application's visual appeal with scalable and high-quality graphics. I hope this article helped!

Happy coding!