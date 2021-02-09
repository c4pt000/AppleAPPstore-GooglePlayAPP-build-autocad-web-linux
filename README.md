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
