# ChillAppManager
Download, launch and code cool apps in the simple Chill App Manager for Windows! (Is the Chill App Manager not loading? Maybe XAMPP isn't running.)
## Setting Up
### First, the hard stuff
This is probabally the longest part, however the process is pretty straightforward. You'll need a Windows OS (works on 10 and 11) and have access to admin stuff.
1. [Download NodeJS with NPM](https://nodejs.org/en/download/) and follow the prompts.
2. [Download XAMPP](https://www.apachefriends.org/download.html) and follow the prompts.
3. Open XAMPP with admin permissions. Click the X next to `Apache` then click `Yes` to install the service (this will run Chill App Manager at startup). If the service is n press `Start` on the Apache service.
5. In your file manager, navigate to `C:\xampp\htdocs` and make sure all files are deleted from here.
6. Copy all the files in the `web` folder of this repo to the `C:\xampp\htdocs` folder.
7. Press the Windows key and type `cmd`. Rightclick the first option and run it as an admininstrator.
8. Type `npm install -g nativefier` in the command prompt followed by the enter key.
9. Check if there's space for one folder on your desktop. This is where the app will be stored.
10. Type `cd C:\Users\%USERNAME%\Desktop` in the command prompt followed by the enter key.
11. Type `nativefier chillsocial.github.io/LocalhostRedirect/go.html` in the command prompt followed by the enter key.
12. Open `C:\Users\Donovan\Desktop\Webapp-win32-x64\resources\app\nativefier.json` in your text editor and add the string below directly after `"oldBuildWarningText":""`...
```
,"internalUrls": "(.*)"
```
Make sure you save it!


12. On your desktop, open the folder named `Webapp-win32-x64` and double-click `Webapp.exe`.

### Then, the easy stuff.
1. You'll need to enter your computers username. This will only be used to edit the `Webapp-win32-x64` for the sole purpose of providing you service updates.
2. That's it! :D

## Using
Chill App Manager is still in development :eyes:
