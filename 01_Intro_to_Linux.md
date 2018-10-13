## Intro to Basic Commands

The purpose of this tutorial is to provide you with some basic commands that will allow you to: 

- 1. log onto a remote computer (e.g. "the cluster")
- 2. navigate to different locations on that computer
- 3. create new directory and files in that directory
- 4. edit files
- 5. execute files (scripts) from the command line

### 1. Logging on to a remote computer

First you need to open an application that will allow you to connect to a computer remotely. On a Mac, this is easy - find the **Terminal** application and launch it. You can do this just like you would any other application on your computer. If you are using a PC, you'll need to install an SSH client such as the program [PuTTY](https://www.putty.org/). The **Terminal** application on a Mac or software such as **PuTTY** on a PC will allow you to connect to a different computer remotely.

Now we need to log onto the remote computer where you will do your work.

First, open your Terminal or other SSH application/

Second, use the **SSH** command to log onto the computer. For example, to log onto the *Longleaf* cluster at UNC, we'll type:
```bash
ssh user@longleaf.unc.edu
```

You will then be prompted to enter your password. Once you've entered the password you should be logged onto the remote computer!

### 2. Navigating and 3. creating new directories and files on the remote computer

To view your location on the computer you have just logged into, use the "print working directory" command. Enter the following on the command line and hit return (or enter): 
```bash
pwd
```

The *path* to your current working directory should have printed to the screen. This is the location on the computer where other commands will be executed.

For example, lets run the command to make a new directory (can be thought of like creating a new folder on your desktop, for example):
```bash
mkdir my_tutorial
```

The **mkdir** command needs to be followed by a string. The string will be the name of the new directory we created. In the above example, a new directory will be created in your current working directory called "my_tutorial".

To view all the files and directories located in your current working directory type (followed by hitting return):
```bash
ls
```

**ls** has a number of optional arguments that can be used to modify it's output. For example, `ls -l` will return all the files and directories in the current working directory, but with each file or directory printed on a new line.

To view options associated with a built in linux command such as `ls` you can type `man <command>`. For example, `man ls`.

Let's now move into the **my_tutorial** directory and create a new file that we will then edit.
```bash
cd my_tutorial
```

You can use **cd** to **c**ange your working **d**irectory. Type `pwd` again. Note that you are now working within the **my_tutorial/** directory. 

Now that you are in your **my_tutorial** directory, lets create a file that we will use to write our first *bash* program.
```bash
touch my_first_program.sh
```

The above command should have created a new file in your current directory called ```my_first_program.sh```. Check that this file has been created.



