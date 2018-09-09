# Vivaldi UserCSS

Just some CSS to give Vivaldi browser a bit of a facelift.

To use, first go the the Vivaldi resources directory, on Mac:

```
cd "$(find /Applications/Vivaldi.app/Contents/Versions -maxdepth 6 -type d -name "vivaldi" | head -1)"
```

...and on Windows:

```
cd %LOCALAPPDATA%\Vivaldi\Application\[Version]\resources\vivaldi\
```

Once there, open the file browser.html. In the head section, directly after the line that imports common.css, add the following:

```
<link rel="stylesheet" href="style/custom.css" />
```

Now copy the custom.css file from this project into the style folder under the Vivaldi resources directory. I've tried instead using a symbolic link, but at least on Mac, for whatever reason it doesn't pick up the CSS file when it's a symlink.

Make any edits that you wish to make to the custom.css file, and enjoy.

If you wish to debug the styles and work on your own, you can launch Vivaldi in dev mode with the following flags:

```
--args --debug-packed-apps --silent-debugger-extension-api
```

On Windows just pass those args to the exe file. On Mac, the following command will launch the browser in dev mode:

```
open /Applications/Vivaldi.app --args --debug-packed-apps --silent-debugger-extension-api
```

Once in dev mode, you can right click any element of the interface, and choose "Inspect" from the menu. The Chrome Dev Tools window will appear, allowing you to see and play with the CSS properties of that element.

Enjoy!