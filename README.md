# Electron Outlook Mac App
A custom version of Microsoft Outlook app ([© Microsoft 2021](https://www.microsoft.com/en-us/legal)) for Mac using Electron. Built with [Nativefier](https://github.com/nativefier/nativefier).

The official Outlook Mac app from Microsoft lacks a number of features that its [web version](https://outlook.live.com) has—at least for now, such as [rules](https://support.microsoft.com/en-us/office/how-to-set-up-rules-in-outlook-75ab719a-2ce8-49a7-a214-6d62b67cbd41) and [calendar icons](https://answers.microsoft.com/en-us/outlook_com/forum/all/microsoft-outlook-calendar-icons/938cefea-906e-45c5-bbfd-69f00dc0bf92).

***Note: I initially created this due to the macOS Outlook App (with the new interface) not supporting [rules](https://support.microsoft.com/en-us/office/how-to-set-up-rules-in-outlook-75ab719a-2ce8-49a7-a214-6d62b67cbd41). I'm archiving this repository because an update adding this particular feature was released.***

## Building Instructions

### (1) Install Nativefier
Install [Nativefier](https://github.com/nativefier/nativefier) using the [instructions](https://github.com/nativefier/nativefier#installation) in the official repository.

### (2) Download files
Download [stylesheet.css](https://github.com/gajzl/outlook-web/blob/main/stylesheet.css), [stylesheet.js](https://github.com/gajzl/outlook-web/blob/main/stylesheet.js) (intentionally left empty for future customisation), and [icon.icns](https://github.com/gajzl/outlook-web/blob/main/icon.icns) (icon belongs to [© Microsoft 2021](https://www.microsoft.com/en-us/legal)) and put the files in the home directory.

### (3) Use Nativefier to build the app
Enter the command below in the terminal:
```zsh
nativefier --name 'Microsoft Outlook Web' 'outlook.live.com' --internal-urls '.*?(outlook.live.com|outlook.office365.com).*?' --file-download-options '{"saveAs": true}' --title-bar-style 'hidden' --browserwindow-options '{"webPreferences": { "webviewTag": true, "nodeIntegration": true, "nodeIntegrationInSubFrames": true, "nativeWindowOpen": true }, "trafficLightPosition": {"x": 12, "y": 33}}' --inject stylesheet.css --inject stylesheet.js --darwin-dark-mode-support --icon icon.icns --badge --counter
```
### (4) Move app to the 'Applications' folder
Move the built app from the home directory to the `/Applications` folder.
```zsh
mv Microsoft\ Outlook\ Web-darwin-x64 /Applications
```
