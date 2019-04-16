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
2. Install windows build tools with admin rights (CMD or): `npm install --global --production windows-build-tools`
3. Set Path variable for python: 

```
    setx PYTHON "%USERPROFILE%\.windows-build-tools\python27\python.exe"
    set PYTHON
```

4. Install `npm i -g electron-rebuild`
5. `electron-rebuild -w <node-package>`, where <node-package> is f.ex.: bcrypt
6. Finished! Now you can install native node modules!


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



---> Stopped at 03/12
