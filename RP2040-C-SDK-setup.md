University of Pennsylvania, ESE 5190: Intro to Embedded Systems, Lab 2A
```
Chenwei Tang
  email:tchenwei@seas.upenn.edu
  Linkedin:https://www.linkedin.com/in/chenwei-tang-3328a224b/
 Tested on: Legion Y7000, Windows 10 21H2
```
# Introduction
This is the RP2040-C-SDK-setup guide of Lab2A based on Windows10. There is a little differnce between this guide and the official guide "getting-started-with-pico". 
I don't use Visual Studio+CMake to build, instead I choose CMake+MinGW. 
The reason is that there are a lot of compatibility issues in my computer leading to failure in "nmake" and it's much easier!

# Configuring Environment
It's better for us to download installer(.exe/.msi) instead of .zip/.tar files because we can avoid some configurations we need to complete manually.
## Arm GNU Toolchain 
[Downloading Here](https://developer.arm.com/downloads/-/arm-gnu-toolchain-downloads)<br>
At the end of installation, we need to click on all these boxes.<br>
![image](https://user-images.githubusercontent.com/113710845/194961079-46ba7ee4-79a4-4741-a499-337aaf0a41b8.png)<br>

## CMake
[Downloading Here](https://cmake.org/download/)<br>
We need to click on this box.<br>
![image](https://user-images.githubusercontent.com/113710845/194962583-a59a4545-2919-4b1e-8a31-2c9cf50686e0.png)

## MinGW
[Downloading Here](https://www.mingw-w64.org/)<br>
After finishing, we need to copy "mingw32-make" and paste in the same folder then rename "make"<br>
![image](https://user-images.githubusercontent.com/113710845/194963491-52d62b0d-e15c-448b-a1ec-2552fed498b3.png)

## Python
[Downloading Here](https://www.python.org/downloads/windows/)<br>
We need to click on these options.<br>
![image](https://user-images.githubusercontent.com/113710845/194964104-de46d7d6-239d-4ebc-8796-d11c24500782.png)<br>
![image](https://user-images.githubusercontent.com/113710845/194964157-2a4dd7a9-c1ae-4da7-ae1c-a8db2c017fb8.png)<br>


## Git
[Downloading Here](https://git-scm.com/download/win)<br>
Here we can use nano editor as the default editor.<br>
![image](https://user-images.githubusercontent.com/113710845/194964438-8425137c-5364-482d-925a-f0052b38ea6e.png)<br>
And in the following options, we can follow "getting-started-with-pico" or choose the default options, there is no difference and both can work well.

## VS code
[Downloading Here](https://code.visualstudio.com/)<br>
We need to click on these options.<br>
![image](https://user-images.githubusercontent.com/113710845/194965130-985a885c-61af-4d2c-bb87-b4a0a74cd38f.png)<br>

## Environment Varibles
We need to add the User and System Environment Varibles like below. Remember, both User and System!<br>
![image](https://user-images.githubusercontent.com/113710845/194970465-d5f80f0f-ce4b-495e-a71e-2f86c11b63ba.png)<br>
This is very important!

# Starting to build
At first, we need to create a folder. Then we enter the terminal(we can download in Mircosoft Store) in this folder. Then we enter the code below
```
git clone -b master https://github.com/raspberrypi/pico-sdk.git
cd pico-sdk
git submodule update --init
cd ..
git clone -b master https://github.com/raspberrypi/pico-examples.git
```
Then we open VS code in folder "pico-examples" in your folder created before<br>
We need to download these in VS code extension.<br>
![image](https://user-images.githubusercontent.com/113710845/194968004-fcc4f13e-f284-468d-a79b-d9891f900e52.png)<br>
Then we need to configue CMake tools in extension settings.<br>
We need to change following options.<br>
![image](https://user-images.githubusercontent.com/113710845/194968253-26260bd8-3bc4-4e5f-83d0-47f3e9b8d3b6.png)<br>
![image](https://user-images.githubusercontent.com/113710845/194968299-591a8716-bdf2-4762-bf5d-e666168b7ff1.png)<br>
![image](https://user-images.githubusercontent.com/113710845/194968331-18fb1367-30f9-4a73-91a6-6589d413eb2e.png)<br>
Then we click on configure this folder by using Arm GNU Toolchain<br> 
![image](https://user-images.githubusercontent.com/113710845/194967561-ed155641-98f0-4b4d-8991-4add0943215d.png)<br>
Now it's the final step. We build hello_usb.elf and we can get a uf2 file. We need to reboot our Raspberry Pi by holding down the BOOTSEL button to force it into USB Mass Storage Mode at first. Then we can now drag-and-drop the UF2 binary onto the external drive.<br>
We open the putty and enter the REPL, and we can find it keep outputting "Hello world", we success!!!<br>
![image](https://user-images.githubusercontent.com/113710845/194969489-92e797e0-1a15-490a-9442-5a8c3705a55c.png)


