# ARM Cross-compilation

*sudo apt-get update*

*sudo apt list --upgradable*

*sudo apt-get upgrade*

*sudo apt-get install git*

*sudo apt-get install gcc make gcc-arm-linux-gnueabi binutils-arm-linux-gnueabi*

*sudo apt-get install gcc-arm-linux-gnueabihf g++-arm-linux-gnueabihf*

*sudo apt-get install gcc-arm-linux-gnueabi g++-arm-linux-gnueabi*

Then, you have to compile you program with one of these compiler:
- For C files -> _arm-linux-gnueabi-gcc prog.c -o prog -static_
- For C++ files -> _arm-linux-gnueabi-g++ prog.c -o prog -static_

You can chek if the file is good for ARM: _file prog_ and the answer has to be the same as:

**_prog: ELF 32-bit LSB executable, ARM, EABI5 version 1 (SYSV), statically linked, for GNU/Linux 3.2.0, BuildID[sha1]=1aec53a65fdd71ec68e761b5ef4cd2fae6e4e75c, not stripped_**

And finally you can send the program on the embedded device and type these command lines on the terminal of the embedded device when the trasnfert is done:
- *sudo chmod +x prog*
- *./prog*
