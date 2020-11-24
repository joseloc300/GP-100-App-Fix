# GP-100-App-Fix
Fix for the Valeton GP-100 Desktop App.

# What is it?
This repository provides a modified configuration file that aims at solving the crashing problems caused by the Valeton GP-100 desktop app.

# What is causing the problem?
From what the pedal itself printed on error, and what the testing confirmed, is that the desktop app's interface is allowing users to input values outside the range authorized by the pedal's firmware and thus, causing an error.

# How was it fixed?
Changing the configuration file allows us to change the range of values for the knobs. By matching this with the values present on the pedal itself we can ensure that the authorized range isn't crossed anymore. For this we'll assume that the pedal's firmware has the correct values for everything.

# Does this require any kind of installation?
No. This only requires the configuration file to be replaced by the one provided here. It is advised to keep a backup of the original just for safety, but a backup of the original is provided as well.

# Is this safe?
The answer is probably yes. Since we're not changing any code, the app should work just like it should with the simple benefit of preventing the previously mentioned crashes. With that said it is a "use at your own risk" warning nevertheless. For the people concerned with security, once again, no code is modified, only the configuration file. If any of you still don't like the idea of downloading a file from the internet you can open your own and change the values manually.

# What platform was this tested on?
This was only tested on Windows 10. If you are using a Mac, I can't verify if it works. If the same file is present, open it, and see if the contents are similar to the file in the repository. If so, backup your file, and if you wish, try this fix as well.

# What versions of the app and firmware were used?
As of the time of creating this repository and writing this, the desktop app is v1.2.0 and the firmware is v1.5.0. Hopefully, an official update will fix these problems in the future. If the new updates bring more errors of similar nature it is likely that repository will be updated as well.

# How to apply the fix?
Windows 10 - Just navigate to the installation folder of the app. Default folder should be something similar to "C:\Program Files\Valeton\GP-100". After finding this folder, navigate to the folder ".\Resource\GP-100\File" inside it. There you will find a file named "algorithm.xml". Remember to ALWAYS make a backup of the original file. Replace this file by the updated one. The name must be "algorithm.xml" for the app to recognize it.
