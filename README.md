# Electron Outlook Mac App
A custom version of Microsoft Outlook app for Mac using Electron

Download [stylesheet.css](https://github.com/ghzliahlam/outlook-web/blob/main/stylesheet.css), [stylesheet.js](https://github.com/ghzliahlam/outlook-web/blob/main/stylesheet.js) (intentionally left empty for future customisation), and [icon.icns](https://github.com/ghzliahlam/outlook-web/blob/main/icon.icns) and put the files in the home directory.

### Nativefier command
Enter the command below in the command line:
```zsh
nativefier --name 'Microsoft Outlook Web' 'outlook.live.com' --internal-urls '.*?(outlook.live.com|outlook.office365.com).*?' --file-download-options '{"saveAs": true}' --title-bar-style 'hidden' --browserwindow-options '{"webPreferences": { "webviewTag": true, "nodeIntegration": true, "nodeIntegrationInSubFrames": true, "nativeWindowOpen": true }, "trafficLightPosition": {"x": 12, "y": 33}}' --inject stylesheet.css --inject stylesheet.js --darwin-dark-mode-support --icon icon.icns --badge --counter
```
### Move app to the Applications folder
Move the built app from the home directory to the `/Applications` folder.
```zsh
mv Microsoft\ Outlook\ Web-darwin-x64 /Applications
```
