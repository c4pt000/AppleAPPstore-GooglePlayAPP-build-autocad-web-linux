
# apple app store + google play store cordova (requires nodejs + npm)


# android requires android sdk + ndk on linux (on macos just Xcode)
```
npm -g install cordova 
npm -g install nativefier

cd Desktop
cordova create myApp org.apache.cordova.myApp myApp
cd myApp
cordova platform add android
cd platforms/android/www       #<--html+js here
cd ../
open myApp.xcodeproj

```


# iOS requires Xcode + $99 developer fee + working iphone
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"


npm -g install cordova 
npm -g install nativefier

cd Desktop
cordova create myApp org.apache.cordova.myApp myApp
cd myApp
cordova platform add ios
cd platforms/ios/www       #<--html+js here
cd ../
open myApp.xcodeproj
```

# setup signing

![s1](https://raw.githubusercontent.com/c4pt000/AppleAPPstore-GooglePlayAPP-build-autocad-web-linux/master/signing.png)


# nativefier example Desktop app (electron)

# AutoCAD Web for Linux
AutoCAD Web desktop app for Linux

<img src="https://raw.githubusercontent.com/giovannicaligaris/autocad-web-linux/master/Screenshot%20from%202018-11-01%2017.44.34.png">

<b>You will need an AutoCAD or AutoCAD LT subscription, otherwise it will only work as a CAD viewer. </b>


<b>INSTALLATION</b>

In order to build this, you will need Nativefier first.

https://github.com/jiahaog/nativefier/

```
optional:
ImageMagick , ImageMagick-devel, wine 
```

Once Nativefier is installed, run the following command:

```bash
$ sudo npm -g install nativefier

$ cd /opt

$ nativefier --name "autocadweb" "https://web.autocad.com" --user-agent "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/88.0.4324.150 Safari/537.36" --platform "linux" --internal-urls ".*?\autodesk\.*?"

$ sudo cp -rf autocadweb-linux-x64 /usr/bin/autocadweb

$ sudo chmod +x /usr/bin/autocadweb/autocadweb

$ autocadweb
```
