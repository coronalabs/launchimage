##Setup a Storyboard based LaunchScreen for iOS 8 based devices.
- Download the project to a folder, remember where you put it. Unpack as necessary.
- Navigate to that folder in Finder
- Click on the <strong>LaunchImage.xcodeproj</strong> file to launch Xcode.
- Click on the Asset.xcassets entry.
- Click on the <strong>Launch</strong> entry.
- Drag the image you want for your 1x splash image to the 1x slot, your 2x splash image to the 2x slot and your 3x image to the 3x slot. The images should be named "launch.png", "launch@2x.png" and "launch@3x.png"
- Click on the <strong>LaunchScreen.storyboard</strong> file.
- Save your project.
- From the menu, click File->Export. Then choose: "Interface Builder Storyboard <strong>Package</strong>" and select the main folder of your project. Leave the name "LaunchScreen".
- Edit your build.settings and add a key <strong>UILaunchStoryboardName</strong> with a value of <strong>"LaunchScreen"</strong> to the <code>plist</strong>.
- Remove any UILaunchImage table you might be using.
- Make sure the images you included above are in the folder with your main.lua.
- Build your app for iOS.

An example build.settings might be:

    settings = {
        iphone = {
    	    plist = {
                UILaunchStoryboardName = "LaunchScreen"
    	    }
    	}
     }
