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


