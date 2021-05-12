# about windows Digital signature is not trusted

> ? cause: Due to the influence of the software and system version, sometimes the drivers created by the software cannot be digitally certified by the system.

## Solution method

**Disable Driver Signature Verification on Windows 64-Bit** 

### Change the Startup settings

```txt
This is the simplest way to disable driver signature enforcement on Windows 10 but bear in mind that this method will only disable driver signature temporarily.

After you restart your computer driver signature enforcement will automatically turn itself on.

To disable driver signature enforcement do the following:

1.  Press and hold the Shift key on your keyboard and click the Restart button.
```

![Image text](https://gitee.com/nethowto/nethowto/raw/master/Img_folder/65.jpg)

```txt
2.  Choose Troubleshoot > Advanced options > Startup Settings and click the Restart button.
3.  When your computer restarts you’ll see a list of options. Press F7 on your keyboard to select Disable driver signature enforcement.
4.  Your computer will now restart and you’ll be able to install unsigned drivers.

Bear in mind that this method only temporarily disables driver signature enforcement, so be sure to install all the unsigned drivers as soon as you can.
```

### [Recommend] Disable driver signing code 

```txt
Another solution is to use the Local Group Policy Editor. Keep in mind that you have to be careful while messing with the Policy Editor, and don’t modify anything else.

To disable the driver signing code, follow the steps:

1.  On your PC open Local Group Policy Editor: press the Win+R hotkeys and in the Run box enter gpedit.msc. 
```
[Click when you can't open gpedit.msc](https://gitee.com/nethowto/nethowto/blob/master/fix/fix_open_gpedit.msc.md)

![Image text](https://gitee.com/nethowto/nethowto/raw/master/Img_folder/66.png)

```txt
2.  In Local Group Policy Editor, from the left panel, click on User Configuration.
3.  Then, from the main window double-click on Administrative Templates.
4.  From the menu that will open double-click on System and then go to Driver Installation.
5.  Select the Code signing for device drivers entry.
6.  Select Enabled and from the dropdown located beneath, change to Ignore.
7.  Click Ok and apply your changes.
8.  Restart your Windows 10 system in the end.
```