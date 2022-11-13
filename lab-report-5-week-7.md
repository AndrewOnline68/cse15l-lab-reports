# Week 7 Lab Report

## Part 1

VIM is one of the more common ways to edit files. To use `VIM`, all you need to do is to input the command `VIM` into the command line with the name of the file that is needed to be edited. In this lab report, we'll use `VIM` to add a line into the `DocSearchServer.java` file. The line we'll be adding will print out whether or not the given input is a string or not. Below is the shortest process I could think of that will add the line to the code using `VIM`.

```
vim DocSearchServer.java
/File[] <enter>
i
<enter>
<up arrow>
System.out.println(f.toString + " This is a directory!!!"
<escape>
:wq
```
Here are some screenshots that displays the changes of the program:

![image](https://user-images.githubusercontent.com/114555448/201511993-e6f1712f-7382-4b0f-a6ab-815e9bed0893.png)

*The image above displays the code changes after searching for the /File[] and before adding the new line.*

![image](https://user-images.githubusercontent.com/114555448/201512251-0d70cc88-a29c-4369-b5db-9ff931a0362e.png)

*The image above displays the code after the new line has been added.*


![image](https://user-images.githubusercontent.com/114555448/201512262-76a9d5c8-dba4-43f5-a814-05f5c2191482.png)

*The image above displays the code when the user is about to save the code and quit `VIM`.*


## Part 2

This part of the lab report will detail whether using `VIM` is faster than using the `scp` command.

Time for `scp`: 14:06*

Time for `VIM`: 1:22

*Note: Time includes time to copy files to remote*

Questions:

1. Which of these two styles would you prefer using if you had to work on a program that you were running remotely, and why?

My preferred method to use when working on a program that is running remotely is `VIM`. This editing style is easy to use on remote and I don't have to deal with recopying the program back and forth from local to remote.

2. What about the project or task might factor into your decision one way or another? (If nothing would affect your decision, say so and why!) 

The project or task that would influence my decision would be whether or not I need to copy multiple files to the remote client or if it's only a single file to edit.
