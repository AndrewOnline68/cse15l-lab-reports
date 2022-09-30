## Week 1 Lab Report

This lab report will be detailing on how to access a remote desktop thru your personal/work computer. This report will guide you with 6 easy steps that will allow you to understand how access a remote desktop and creating a private key to use to quickly access the remote desktop.

## **Step 1: Installing VSCode**
The first step to access a remote desktop is to install a coding program/terminal to actually input the code needed to access the remote desktop. One recommended program to use is called Visual Studio Code, or VSCode for short. You can download VSCode thru this link here: https://code.visualstudio.com/ and follow the steps displayed on the webpage.
![image](https://user-images.githubusercontent.com/114555448/193198553-1e4d4fd7-8435-444f-bdfa-92df42011e60.png)

Afterward following the website and opening up the program, your screen should look like this:
![image](https://user-images.githubusercontent.com/114555448/193198941-36a70bb3-bd09-4f0e-9888-4de631ce800d.png)
 
## **Step 2: Remotely Connecting**
 In order to connect remotely to the remote desktop, on the terminal type in the code:
`ssh cs15lfa22mf@ieng6.ucsd.edu`
 Afterwards, you should be prompted to input a password. This password should be the same one as the one your UCSD password
 
 *Note: This personally took a while due to waiting for the password to reset.*
 The terminal should look like this:
 ![image](https://user-images.githubusercontent.com/114555448/193199982-5b5bcbbd-a152-436d-94d0-feed5d92a6b3.png)
 
## **Step 3: Trying some Commands**
 Now that you are in the remote desktop, it is time to tryout some commands. Some recommended commands to use are listed below:
``` 
 * ls
 * ls -lat
 * ls -a
 * cd ~
 * cd
```

These Commands should allow you to experiment a bit to see how the remote desktop works on your local computer.

## **Step 4: Moving files with the scp command**
Now that you know how to access the remote desktop, this step will now teach you how to copy files from your local computer to the remote. To do this we will use the command:
`scp (className) cs15lfa22zz@ieng6.ucsd.edu:~/;`

The first step is to create a class file. Creating a class file will depend on what project you are currently working on. Afterwards, you are going to compile the class file using the command:
`javac (className).` Run the file using the command:`java (className).`

Here is an example from the local desktop:

![image](https://user-images.githubusercontent.com/114555448/193203122-53871a67-669a-41a0-bbac-e5075cfb5fc7.png)

Now use the command: `scp (className) cs15lfa22zz@ieng6.ucsd.edu:~/;` to copy the class file to the remote desktop. Once completed, use the ssh command to access the desktop again and run the javac (className) command to see if it copied over.

Here is an example from the remote desktop:

![image](https://user-images.githubusercontent.com/114555448/193203584-1d686de2-7344-4c07-a2c6-848e4d4fbcda.png)

Here's also the cluster of text that is shown when doing this process:

![image](https://user-images.githubusercontent.com/114555448/193203725-a1e137b6-6e83-44b6-9fd0-03c38451c5b7.png)

## **Step 5: Setting an SSH Key**
Logging into the remote is pretty fast and simple, right? Wrong, it is actually pretty tedious to type in and/or copy/paste your password everytime you want to access the remote desktop. What if I told you that you can input a private pin instead. To do this, run the following program on your client:
```
ssh key-gen;
```
Afterwards the terminal should display what is shown below:
![image](https://user-images.githubusercontent.com/114555448/193314777-7712745f-bf0d-4863-85c2-d1a603cdb263.png)

*Note: If your using windows, follow the extra `ssh-add` steps on the image below:*
![image](https://user-images.githubusercontent.com/114555448/193208171-7a9e0203-b030-4575-86f0-8ce2aa9ab700.png)

Now that we set up the ssh key, log back into the remote desktop and run the program `mkdir.ssh`. After that, copy the pin directory to the remote client.

Once finished, you should be able to use the `ssh` or the `scp` command with the use of the passcode.

## **Step 6: Optimizing Remote Running**
Now that we set up a pin to quickly log in to the remote client, We are now going to optimize running the remote client. The most common way to optimize the remote running is to use keystrokes, which is less keys used to run programs.
This part is honestly where I got stuck on. Tried using multiple keystrokes to optimized my remote progress, but wasn't able to do it

Example of what my attempts looks like:
![image](https://user-images.githubusercontent.com/114555448/193332039-539a1260-bee0-4c61-a482-00af77638ff1.png)


This will conclude the Lab Report on how to access the remote client and how to copy files to that remote client.
