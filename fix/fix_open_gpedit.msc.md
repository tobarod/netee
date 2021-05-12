# about how to open gpedit.msc

> ? cause: When your system is a home version of windows, it will be unable to open gpedit.msc.


## Solution method [中文入口](https://jingyan.baidu.com/article/454316abbbee56b6a7c03ae2.html)

**Copy the following code. Save it in an empty file with the suffix .cmd.**

```bash
@echo off

pushd "%~dp0"

dir /b C:\Windows\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientExtensions-Package~3*.mum >List.txt

dir /b C:\Windows\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientTools-Package~3*.mum >>List.txt

for /f %%i in ('findstr /i . List.txt 2^>nul') do dism /online /norestart /add-package:"C:\Windows\servicing\Packages\%%i"

pause
```
**Run this file with administrator privileges**

![Image text](https://gitee.com/nethowto/nethowto/raw/master/Img_folder/67.jpg)

**Usually after seeing the content shown in the image above, you have completed the repair.**