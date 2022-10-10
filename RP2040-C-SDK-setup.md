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
At the end of installing, we need to click on all these boxes.
![image](https://user-images.githubusercontent.com/113710845/194961079-46ba7ee4-79a4-4741-a499-337aaf0a41b8.png)
