# basic-linux-commands
Sample repository to demonstrate usage of linux commands at a workshop

 \_______________\
< Linux is cool >
 \---------------\
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||

## Basic commands

First and foremost, in order to get this repository on your computer, we have to use git.
To clone a git repository locally, use `git clone`

`git clone https://github.com/0xkits/basic-linux-commands`

---

Great! Now lets enter the directory where we just cloned the repository

`cd basic-linux-commands`

---

Now, let's take a look at what's inside this repository. FOr this we use the ls command

`ls`

This should give us a list of files and folders inside our current directory
If you want to quickly find out where you are, you can use the `pwd` command

`pwd`

---

Okay, now lets go into the helloworld directory

`cd helloworld`

---

Let's see what is inside this directory

`ls`

---

There's a file called myname.txt. Let's open it and enter our name shall we?
For this, we shall use any text editor. For convenience, we will use Nano in this example

`nano myname.txt`

Go ahead and edit whatever you need to in the document. To save our changes, enter the following keystrokes

`CTRL + x` to exit
press `y` to save
and enter a name to save it as. Leave it blank if you do not want to change the name

---

Want to read your brand new file? We can `cat` it

`cat myname.txt`

---

Hmm... This file contains alot more than our name doesn't it. It would be more fitting to call it bio.txt
In Linux, to rename files, we simply 'move' them into themself. If it doesn't make sense, think of it as overwriting 
the same file with a different name. This can be done with the `mv` command

`mv myname.txt bio.txt`

Now, if we `cat` the new bio.txt file we should see it's contents are exactly identical as myname.txt

---

Let's say I want to make a backup of my bio.txt file. Let's make a new backup directory in our root directory
Go back to the `basic-linux-commands` directory by traversing backwords using `cd`

`cd ..`

`..` tells cd to go back one directory

Now check your current directory using `pwd` and it should be `basic-linux-commands`

---

Let's make a backup directory. To do this we shall use `mkdir`

`mkdir backup`

Now use `ls` to see the new directory, and `cd` into it

`ls`
`cd backup`

---

Since this is a backup, I want to copy over my bio.txt from helloworld to backup.
To copy files, we use `cp`. In Linux, we have to specify an output file for copy operations
We can copy our bio like this

`cp ../helloworld/bio.txt ./backup.txt`

Remember that `..` tells cd to go back one directory, then it goes into helloworld

Let's go back to the original directory using cd.

`cd ..`

---

Let's say we no longer need the backup bio.txt file. We can get rid of it by using the `rm` command

`rm -rf backup/bio.txt`

The `-rf` flag means that we are deleting a file

We can also delete the entire directory by using

`rm -rf backup`

---

## Some other cool stuff

We can use `grep` for pattern matching in files. For example, if I just want to find my name from
bio.txt I can do

`cat helloworld/bio.txt | grep Name`

Similar to task manager in windows, you can view all running processes in Linux by using `top`

`top`

You can see which user you are logged in as using `whoami`

`whoami`

You can create an empty file using `touch`

`touch test.txt`

Terminal feeling cluttered? You can clear it with `clear`

`clear`


