# Chill App Manager
Download, launch and code cool apps in the simple Chill App Manager for Windows! 

With a UI similar yet different from the classic Nintendo Wii, I developed the Chill App Manager to give a sense of nostaliga for the abandoned console. For the best experience, connect your bluetooth mouse and keyboard to your laptop and plug your laptop into your TV. If you can somehow set up your Nintendo Wiimote as a mouse, that will be cool (and let me know how you did that so I can set up a guide!).

(Is the Chill App Manager not loading? The most common fix is that XAMPP Apache isn't running.)
## Setting Up
### First, the hard stuff
This is probabally the longest part, however the process is pretty straightforward. You'll need a Windows OS (works on 10 and 11) and have access to admin stuff.
1. [Download NodeJS with NPM](https://nodejs.org/en/download/) and follow the prompts.
2. [Download XAMPP](https://www.apachefriends.org/download.html) and follow the prompts.
3. Open XAMPP with admin permissions. Click the X next to `Apache` then click `Yes` to install the service (this will run Chill App Manager at startup). If the service is n press `Start` on the Apache service.
5. In your file manager, navigate to `C:\xampp\htdocs` and make sure all files are deleted from here.
6. [Extract the service pack contents](https://github.com/chillsocial/ChillAppManager/raw/main/servicepack.zip) to the `C:\xampp\htdocs` folder.
7. Press the Windows key and type `cmd`. Rightclick the first option and run it as an admininstrator.
8. Type `npm install -g nativefier` in the command prompt followed by the enter key.
9. Check if there's space for one folder on your desktop. This is where the app will be stored.
10. Type `cd C:\Users\%USERNAME%\Desktop` in the command prompt followed by the enter key.
11. Type `nativefier chillsocial.github.io/LocalhostRedirect/go.html` in the command prompt followed by the enter key.
12. Open `C:\Users\Donovan\Desktop\Webapp-win32-x64\resources\app\nativefier.json` in your text editor and add the string below directly after `"oldBuildWarningText":""`...
```
,"internalUrls": "(.*)"
```
Make sure you save it, otherwise most Chill apps will not work!


12. On your desktop, open the folder named `Webapp-win32-x64` and double-click `Webapp.exe`.

### Then, the easy stuff.
1. You'll need to enter your computers username. This will only be used to edit the `Webapp-win32-x64` for the sole purpose of providing you service updates.
2. Once you're on the main menu, restart the app. This is nessecary for some apps and features to work.

## Using
### Apps
#### Developing Apps
[Read this.](https://github.com/chillsocial/ChillApps/blob/main/README.md)
#### Pre-Installed Apps
Chill Browser, Chill TV, Discord, Store and YouTube will be pre-installed. You can uninstall any app by clicking it then clicking `Uninstall App`.
#### Downloading Apps (through the Store)
Open and start the Store channel to see channels you can get. You can enter a Github repository or use the official Chill one. Then, click a channel to install it. (Do not spam click, it may take awhile to install apps depending on the files contents).
#### Downloading Apps (manually)
You'll need to find an app source folder. Move this folder to `C:\xampp\htdocs\apps`.
## Common Error Fixes
### YouTube channel saying `You are being directed to youtube.com` and redirects to youtube.com instead of loading in TV Mode
The user agent is out of date and I will try to update this ASAP. Basically, I have to change the [user agent](https://github.com/chillsocial/ChillAppManager/blob/main/latestUserAgent.txt) to appear as a Smart TV and as YouTube discontinues some user agents I have to switch it over to a new one.
### White Screen
Although this error is extremely uncommon, there is a fix for this! Run `CTRL + Shift + I`, click the `Console` tab and enter the following...
```
location = 'http://localhost';
```
