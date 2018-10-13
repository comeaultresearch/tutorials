## Intro to Basic Commands

The purpose of this tutorial is to provide you with some basic commands that will allow you to: 

- 1 log onto a remote computer (e.g. "the cluster")
- 2 navigate to different locations on that computer
- 3 create new directory and files in that directory
- 4 edit files
- 5 execute files (scripts) from the command line


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

You can use **cd** to **c**hange your working **d**irectory. Type `pwd` again. Note that you are now working within the **my_tutorial/** directory. 

Now that you are in your **my_tutorial** directory, lets create a file that we will use to write our first *bash* program.
```bash
touch my_first_program.sh
```

The above command should have created a new file in your current directory called `my_first_program.sh`. Check that this file has been created.


### 4. Editing text files

There are a number of different text editors that will be available on a linux system that we can take advantage of to edit the scripts that we will be creating. We will use a common and powerful text editor called **vim**. To open a file with **vim** we type:
```bash
vi <file_name>
```
Open the file we just created using **vi**.

Once we open the file in the **vi** editor, we need to first ask the program to let us edit the file. We can do this by typing `i`. This tells **vim** to change to **insert** mode. Now you can add text to your file.

The first line of our new program needs to read `#!/bin/bash`. Enter this into your script and press **return**. This line tells the computer that when it executes our scripts, we want it to interpret the commands with the *bash* scripting language. 

Press **return** again to move to a new line. Let's now tell our program that whenever it sees a certain string in the script below to print a different output to the screen. What we first need to do is assign a *value* to a *variable* that we can then call upon whenever we need it below in our script. To define variable:value pairs in bash we use an `=` symbol. So lets assign some text to a variable called `my_output`.
```bash
my_output="Hello Word!"
```

Press return two more times. You should now be on the fifth line of your program. Now lets tell our program to print the value associated with the `my_output` variable to the screen. To do this we can use bash's **echo** command. 
```bash
echo $my_output
```

Note that to access the value associated with a variable in bash, we need to add a *$* in front of the variable name.

Okay, lets save our new program and exit the **vim** editor. First hit the **esc** button. This takes us out of the *--insert* mode. Now type `:wq` and then hit **return**. This tells **vim** to write the changes we've made to the file and quit the editor.
 
