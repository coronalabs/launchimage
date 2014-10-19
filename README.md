##Setup a Storyboard based LaunchScreen for iOS 8 based devices.
- Download the project to a folder, remember where you put it.  Unpack as necessary.
- Navigate to that folder in Finder
- Click on the <strong>LaunchImage.xcodeproj</strong> file to launch Xcode.
- Click on the Images.xcassets entry.
- Under the <strong>AppIcon</strong> entry, right-click (CMD-click) and choose New Image Set.
- Drag the image you want for your 1x splash image to the 1x slot, your 2x splash image to the 2x slot and your 3x image to the 3x slot.
- Click on the <strong>LaunchScreen.xib</strong> file.
- Change the text of the label as desired, or delete the label if you do not want it.
- Click on the UIImageView and then click on <strong>Image</strong> field in the Attributes Inspector and choose <strong>Image</strong> from the pull down.
- Make any other design changes that you want.  This example does a simple image and label.
- Save your project.
- Open the <strong>Terminal</strong> app and change directory to where your <strong>LaunchScreen.xib file exists. It's inside the LaunchImage/Base.lproj folder.
- Type in this command:  <code>ibtool --compile LaunchScreen.nib LaunchScreen.xib</code>
- Copy the LaunchScreen.nib file to your project folder where your main.lua lives.
- Add a key <strong>UILaunchStoryboardName</strong> with a value of <strong>"LaunchScreen"</strong> to the <code>plist</strong>.
- Remove any UILaunchImage key you might be using.
- Make sure the iamges you included above are in the folder with your main.lua.
- Build your app for iOS.

An example build.settings might be:

    settings = {
        iphone = {
    	    plist = {
                UILaunchStoryboardName = "LaunchScreen"
    	    }
    	}
     }

  

