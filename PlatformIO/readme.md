Open the "Example Button" folder in vscode.

Make sure you have the platformio extension installed.

Note: Build will fail the first time it is run. The lvgl library requries a bit of config. Read on for details.

Click the "Build" icon (check mark) on the bar at the bottom of vscode to compile. Platformio will install the required libraries. The first build will fail. Open the .pio/libdeps/lvlg folder and copy and paste lv_conf_template.h to the same directory. Remane the copied file to lv_conf.h, then edit the file and change `#if 0 /*Set it to "1" to enable content*/` to `#if 1 /*Set it to "1" to enable content*/` to enable the content (as per the comment in the file).

For some reason, the lvgl library doesn't seem to compile outside of the `~user/Documents/PlatformIO/Projects` folder. I don't know why yet...

Now run the build again and it should compile and upload.
