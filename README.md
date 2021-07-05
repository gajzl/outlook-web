# Electron Outlook Mac App
A custom version of Microsoft Outlook app for Mac using Electron

### Nativefier command
```zsh
nativefier --name 'Microsoft Outlook Web' 'outlook.live.com' 
           --internal-urls '.*?(outlook.live.com|outlook.office365.com).*?' 
           --file-download-options '{"saveAs": true}' 
           --title-bar-style 'hidden' 
           --browserwindow-options '{"webPreferences": { "webviewTag": true, "nodeIntegration": true, "nodeIntegrationInSubFrames": true, "nativeWindowOpen": true }, "trafficLightPosition": {"x": 12, "y": 35}}'
           --inject stylesheet.css --inject file.js --darwin-dark-mode-support --badge --counter
```
