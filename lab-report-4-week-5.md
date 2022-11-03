# Week 5 Lab Report

## Find Command Research Task

The **find** command is a command that goes through directories and sub-directories and list all files within those directories/sub-directories. Usually, the **find** command is just used by itself to display all the files and directories with in the current directory.

Example:

![image](https://user-images.githubusercontent.com/114555448/199079721-d82c980a-fa15-463b-a0a4-8950a86ca335.png)

One alternate way to use the find command is to use the -name option of the **find** command. The -name command option searches through the given directory and any sub-directories for any files that match the string given in the command line. We use the command like this:
`find <directory> -name (name)`
This command option is useful because it'll search through the directory and sub-directories for any files that use the inputed string.

Below are some examples of the -name option in place.

![image](https://user-images.githubusercontent.com/114555448/199079466-3b9b78bc-f7f3-4cc1-8c05-cdebdef8d167.png)

![image](https://user-images.githubusercontent.com/114555448/199653243-d8958ae5-f15b-45b0-bfdc-40e80c5a0e41.png)

![image](https://user-images.githubusercontent.com/114555448/199653505-3b0e4d10-56aa-4c8c-9cc0-914e571df98d.png)


*NOTE: The ".txt" at the end of the command displays all .txt files within the current directory.*


Another alternate way to use the find command is the -empty command option. This option allows you to find specific directories or files that contain no files or text within the directory or file. The -empty command searches the directory and any sub-directories for any sub-directories and files that haav no text or files within itself. This command is helpful because it allows the user to locate any file directories and files that have no text or text files. We use the -empty option command like this:
`find <directory> -empty`

Here are some examples of -empty option:

![image](https://user-images.githubusercontent.com/114555448/199650841-56ce9e27-0d79-4952-b9b7-3b9ccee725c6.png)

![image](https://user-images.githubusercontent.com/114555448/199654049-de8b3ab9-3226-4ba8-8824-257dfc1c0177.png)

![image](https://user-images.githubusercontent.com/114555448/199654098-3e24024a-2ae4-48ce-93de-d9ef87b2c617.png)


*NOTE: The files and directories listed for the -empty command were added to demostrate the command*


The final alternate way to use the find command is thru the -exec command option. Through the use of the -exec command, the client searches the directory and any sub-directories for any file that the user wants to delete and prompts them if they do want to delete the specific file. This command is useful because it allows the user to delete any file without going through and searching for the directory for the specific file to delete. This command option allows you to delete a file from a directory. Below is the template of the -exec command:
`find <directory> -name -exec rm -i {} \;`

Here are some examples of -exec option:

![image](https://user-images.githubusercontent.com/114555448/199652270-72a98b36-8875-4465-9719-34840ca612fb.png)

![image](https://user-images.githubusercontent.com/114555448/199654438-e91547c0-4357-4777-89c0-53e5791a4b3d.png)

![image](https://user-images.githubusercontent.com/114555448/199654590-00aee7a0-a058-42a3-b317-051b044723a9.png)
