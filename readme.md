# DriverInjectDll

## Introduction
 
Using Driver Global Injection dll, it can hide DLL modules. You need to determine the process name you want in DllMain

## Develop

#### DriverInjectDll
driver program

#### Input_dll
Tell the driver to inject DLL binary data

#### Loader
Shelcode for Memory Loaded DLL

#### MyDll
TODO: Judging Injected Process Name in DLLMain

# Build
vs2008-vs2017

wdk7-wdk10

# How Use
step1: install and start driver program

step2: run Input_dll.exe

# screen snapshot 
![avatar](./snapshot1.jpg)

## Support

Win7-Win10 x64

// 通过注册进程创建/退出回调函数把进程加入要注入list。
// 通过注册Image加载回调函数，在回调函数中创建系统线程，以线程函数中对进程进行DLL注入。
// 具体注入是hook了ZwContinue函数
