# learning_electron

## Install electron

```
npm init -f

npm install --save-dev electron
```

or try:

Download `https://github.com/electron/electron-quick-start` and run `npm install`

## Run app

1. Install electron globally `npm install electron -g`
2. Run `electron .` to start the app

## Useful Packages

* `electron-reload`: Reloads the app automatically when developing

## Install native node modules 

### Windows

1. Install electron locally: `npm install electron`
2. Install windows build tools with admin rights (CMD or): 

    `npm install --global --production windows-build-tools`
    `npm install --global --production windows-build-tools@4.0.0`
    
3. Set Path variable for python: 

```
    setx PYTHON "%USERPROFILE%\.windows-build-tools\python27\python.exe"
    set PYTHON
```

4. Install `npm i -g electron-rebuild`
5. `electron-rebuild -w <node-package>`, where <node-package> is f.ex.: bcrypt
6. Finished! Now you can install native node modules!

If error try:
1. `npm install --msvs_version=2017`

## Install devtron

```
# Install Devtron
$ npm install --save-dev devtron

// Run the following from the Console tab of your app's DevTools
    require('devtron').install()
// You should now see a Devtron tab added to the DevTools
```

## Save window state in electron

Use the package `electron-window-state`

## Electron API

### API: Main Process

`electron.app` controls the event's lifecycle

`electron.BrowserWindow` Frameless Window

`electron.BrowserWindow.webContents`

`sessions` is used to store cookies, local data

`sessions.cookies` we can store data within cookies, useful for user data or app state

`sessions.downloadItem` starts a file download

`dialog`, presents the user a specific dialog option

`Accelerator & global shortcuts` are basically keyboard shortcuts for the user

`Menu` allows to create main menues and context menues

`Context Menu` create a context menu

`Tray` electron allows us to have our app part of the tray

`powerMonitor` allows us to react to changes in the power state

## IPC Process

* Inter Process Communication
* Used to talk from the cipc lient with the server side

# Renderer Process API

* `remote` electron module
* `BrowserWindowProxy` is a way to access a newly created browser window
* `Webview` is a browser window in a page

# API:Shared

* `Process`, exists for any node process
* `Screen`, allows us to get specific info about user screen sizes and layouts
* `Shell` allows us to open/close/delete files
* `nativeImage` allows us to manipulate images
* `clipboard` allows us to copy/paste text via selection
* Offscreen Rendering: Allows us render f.ex.: link off the screen
* Network Detection: Uses HTML5 APIs to detect if a user is offline/online
* Battery Status: Getting deeper information about the battery status of the device 

# Distribution

* Use `electron-builder` to build the app -> Can create a workflow for building
* `electron-builder build -m zip` --> build for MAC
* Code Signing is used to check that the app was created by you
* Publish Releases via github
    * Use "Release"-Tab on Github
    * Create GH token and publish via `electron-builder`




---> Stopped at 09/05