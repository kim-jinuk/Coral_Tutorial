# What is it?

This project makes it easy to use libedgetpu and tensorflowlite using CMake. 
So for quick use, we use prebuilt tensorflow, edgetpu, and flatbuffers.
In particular, ARM64 (aarch64) has been documented separately for this purpose because of its weak support.

# Requirements

1. Ninja
2. CMake
3. gcc, g++
4. aarch64(ARM64) Board

# How to build?

1. lstpu (Displays a list of TPU equipment currently connected.)
```sh
# 우분투 기준으로 필수 프로그램
# 현재 보드에 연결된, TPU 장비를 검색하는 소프트웨어 
$ sudo apt install ninja-build cmake gcc g++ make
$ git clone --recursive https://github.com/kim-jinuk/coral_tutorial.git
$ cd coral_tutorial
$ make lstpu && cd build
$ ./lstpu

# Model 빌드 
$ make build && cd build
$ ./model test.tflite label.txt 0.5
```

2. lstpu (Displays a list of TPU equipment currently connected.)
```sh
$ git clone --recursive https://github.com/kim-jinuk/coral_tutorial.git
$ cd coral_tutorial
$ make lstpu
$ ./build/chacha
```

3. your software build
```sh
$ git clone --recursive https://github.com/kim-jinuk/coral_tutorial.git
$ cd coral_tutorial
$ make build # make
$ ./build/chacha
```
