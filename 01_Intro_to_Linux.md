## Intro to Basic Commands

The purpose of this tutorial is to provide you with some basic commands that will allow you to: 

- 1) log onto an external computer (e.g. "the cluster")
- 2) navigate to different locations on that computer
- 3) create new directory and files in that directory
- 4) edit files
- 5) execute files (scripts) from the command line

### Logging on to a remote computer

First you need to open an application that will allow you to connect to a computer remotely. On a Mac, this is easy - find the **Terminal** application and launch it. You can do this just like you would any other application on your computer. If you are using a PC, you'll need to install an SSH client such as the program [PuTTY](https://www.putty.org/). The **Terminal** application on a Mac or software such as **PuTTY** on a PC will allow you to connect to a different computer remotely.

### Getting started

Print the directory that you are currently working in: 
```bash
pwd
```

The above command will give you the *path* to your current directory. This is the location on the computer where other commands will be executed.

For example, lets run the command to make a new directory (can be thought of like creating a a folder on your desktop, for example):
```bash
mkdir my_tutorial
```

The **mkdir** command needs to be followed by a string. In the above example, a new directory will be created in your current working directory called "my_tutorial".
