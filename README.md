# Electron Outlook Mac App
A custom version of Microsoft Outlook app for Mac using Electron

### Nativefier command
```zsh
nativefier --name 'Microsoft Outlook Web' 'outlook.live.com' --internal-urls '.*?(outlook.live.com|outlook.office365.com).*?' --file-download-options '{"saveAs": true}' --title-bar-style 'hidden' --browserwindow-options '{"webPreferences": { "webviewTag": true, "nodeIntegration": true, "nodeIntegrationInSubFrames": true, "nativeWindowOpen": true }, "trafficLightPosition": {"x": 12, "y": 33}}' --inject stylesheet.css --inject stylesheet.js --darwin-dark-mode-support --icon icon.icns --badge --counter
```
### Move built app from home directory to the Applications folder
```zsh
mv Microsoft\ Outlook\ Web-darwin-x64 /Applications
```
