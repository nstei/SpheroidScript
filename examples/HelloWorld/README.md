# Hello world

This tutorial will take you through the steps to create and launch on your mobile phone 
a simple app powered by the Spheroid Universe Platform. This app will 

Before you start, you need to [create an app](../../docs/app-create.md).

## Download the source code

We have already prepared for you the source code you'll need to create a demo app. Download a zip archive from [our repo](https://github.com/SpheroidUniverse/SpheroidScript).

[TODO: image]

Then extract contents of the 'SpheroidScript-master\examples\HelloWorld\src' folder from the zip archive. You're now all set to upload the source code to your app!

## Upload the source code to Spheroid Demiurge IDE

Now, what you need to do is to upload the extracted files with source code to the IDE keeping the tree structure unchanged. So in the root of your app you need to have "app.json" and "Client.spheroid" files".

```
(Your app name)
|--- app.json
\--- Client.spheroid
```

Currently, you can't upload a whole zip or a folder to the IDE but you can upload multiple files at once by a single drag-n-drop.

Open the "IDE" tab and select your app in the dropdown list.

![](../../docs/images/05---create-app-complete.png)

![](../../docs/images/06---ide-select-app.png)

Left-click the root folder (with the same name as your app) to expand it and drag-n-drop the "app.json" and "Client.spheroid" files.

![](../../docs/images/hello-world-files.png)

You're done! Now you can proceed to publishing the app.

## Publish your app

Publish your app. Click the "Publish" button in the top menu and, when the dialog comes up, keep the default settings, and click the "Publish" button at the right bottom of the dialog.

![](../../docs/images/13---publish-1.png)

If the publication has been successful, you will see four info messages in the "Build" tab in the bottom pane. Congratulations, you have published your app!

![](../../docs/images/14---publish-2.png)

If you don't see the four info messages, or you see error messages instead, check you've followed the previous steps accurately and, if so, [write us an issue](https://github.com/SpheroidUniverse/SpheroidScript/issues/new), and we will help you solve the problem.

## Launch your app on your mobile phone

Now as you have your app built and published, it's time to run it on your mobile phone.

[Log in to XRHub](../../docs/xrhub-login.md). Swipe right through the list of worlds to find the world your app has been published into (world is called "layer" in IDE). Note that if you're not logged in, you won't see the world, because the worlds created by developers are private. In the later tutorials you will learn how to add testers to your layer aka world.

| ![](../../docs/images/26---xrhub-user-app.png) | ![](../../docs/images/mobile-placeholder.png) | ![](../../docs/images/mobile-placeholder.png) | ![](../../docs/images/mobile-placeholder.png) |
| --- | --- | --- | --- |
| ![](../../docs/images/pixel.png) | ![](../../docs/images/pixel.png) | ![](../../docs/images/pixel.png) | ![](../../docs/images/pixel.png) |

When you've found your world, tap the "Launch" button, and your app will run. 
Congratulations, you have successfully run your app in the XRHub! 
See the logs from the app appearing in real time in the IDE in the "Client" tab 
in the bottom pane to find a "Hello world!" log.

## Troubleshooting

If you have encountered any problems, please let us know by [submitting an issue](https://github.com/SpheroidUniverse/SpheroidScript/issues/new), we will make sure to help you find the solution. Please don't hesitate to contact us, as your issues and our replies will help to make our platform better and will be valuable to other developers.

See more on how to submit an issue [here](../../docs/issues.md).

## What next?

In the next tutorials, we will take a closer look at what we've done by exploring the source code of the app.
We'll get familiar with the Spheroid Script – the Platform language.
We'll talk about the project structure and discuss some key concepts e.g. dividing code into a client-side part, and a server-side part.
Finally, we'll learn the basics of persisting data in a cloud database using the Spheroid SQL.

Until the next tutorial, you can already start exploring Spheroid Script by yourself using the [documentation](https://spheroiduniverse.github.io/SpheroidScript/).