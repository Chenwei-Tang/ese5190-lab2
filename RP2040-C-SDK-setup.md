University of Pennsylvania, ESE 5190: Intro to Embedded Systems, Lab 2A
```
Chenwei Tang
  email:tchenwei@seas.upenn.edu
  Linkedin:https://www.linkedin.com/in/chenwei-tang-3328a224b/
 Tested on: Legion Y7000, Windows 10 21H2
```
# Introduction
This is the RP2040-C-SDK-setup guide of Lab2A. There is a little differnce between this guide and the official guide "getting-started-with-pico". 
I don't use Visual Studio+CMake to build, instead I choose CMake+MinGW. 
The reason is that there are a lot of compatibility issues in my computer leading to failure in "nmake" and it's much easier!

# Configuring Environment
## Arm GNU Toolchain 
