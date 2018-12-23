---
layout: default
title: Bash and Python with Jupyter Notebooks
comments: true
permalink:
---
<figure class="center">
<a href="/images/jupyter/jupyterlogo.png"><img alt="Jupyter logo" src="/images/jupyter/jupyterlogo.png" style="width:500px;height:150px;"></a>
<figcaption><a href="/images/jupyter/jupyterlogo.png"><strong>Jupyter Notebooks</strong></a></figcaption>
</figure>
What's interesting about **[Jupyter Notebooks][1]** is that this web-based tool combines the convenience of having a markdown text editor and a bash/python command interpreter. Don't believe me...? Check out the following two commands that output *Hello World*

##### Python Code Snippet
![Jupyter Python Print code](/images/jupyter/print_python.png)

##### Bash Command 
![Jupyter Bash Echo function](/images/jupyter/echo_bash.png)

As you can tell, the first input command is a python built-in function that displays any text between the double quotation marks (" "). Similarly, the following command is another function called *echo*, which also displays any input that is contained within the double quotation marks (" ") to a standard output display. Notice that this command is prepended with an exlamation mark (!) to inform the kernel that the subsequent command is a bash command.

Let me preface the following explanations by saying that a unix/linux operating system treats all files and directories as files. Technically, a user's current directory (```.```) or parent directory (```..```) can be considered as files since they are located relative to a parent directory. This will hopefully make sense a bit further in this explanation when we reach the **File System Navigation** section below

Ok, let's try a few more commands that are fairly similar to each other; but first let me import a python module called ```os``` to gain access to the host's operating system dependent functionality.

## Current Filesystem Location
##### Python Code Snippet
![Jupyter Python Current Directory code](/images/jupyter/currentdir_python.png)

In a few lines of code, the python command, beginning with the import of the ```os``` module, accomplishes the goal of printing the filepath of the current working directory. Next we'll see how a simple bash command can show the samein even fewer typed text characters.

##### Bash Command 
![Jupyter Bash Current Directory command](/images/jupyter/pwd_bash.png)

As you'll notice, the exact same result is achieved using the ```pwd``` command, which stands for ***P***rint ***W***orking ***D***irectory. In the next section, we'll review basic filesystem navigation commands. Used in conjunction, beginner users can quickly make sense of where they are in a filesystem by utilizing the ```pwd``` command.

## Basic Filesystem Navigation
##### Python Code Snippet
![Jupyter Python Change Directory code](/images/jupyter/changedir_python.png)

As you can see above in the lines of python code, we first begin by defining a new filepath in which we seek to move to. In this case, we want to move into a directory labeled "*testfile_pydir*". Relative to our current working directory, which is "/home/mrmachine/Desktop/PROJECTS/jupyter_work/pynb", our destination directory is a sub-folder of the current directory. When we move into the sub-folder and list it's contents, the current directory and parent directory, denoted by a ```.``` and a ```..```, respectively, are considered files, or rather anchor points for which to move into other files or directories.

Ok, let's move on to additional explanation of this code block beginning on line 1. Notice that I've have prepended this text with a "/" and enclosed it within double quotations (" "). This is done so intentionally so that the python kernal interprets the input as a raw string of text, much like how users would type in a file path like */home/user/Desktop/*.

The second line of code is defining the variable called *new_dir* by utilizing the function called ```os.chdir```, which essentially takes in the arguement , or parameter, previously defined in the *new_path* variable. The python kernel subsequently interprets this command, in its literal sense, as the following:

![Jupyter Change Directory example](/images/jupyter/os.chdir_python.png)

The next two lines of code essentially defines and prints a new variable called the *current_dir*, which should indicate a new filepath since the ```os.chdir``` function was utilized to change the current working directory.

![Jupyter Python Reset Current Directory code](/images/jupyter/resetdir_python.png)

The block of code above, simply reverts the changes made to the current location of the user within the filepath. To briefly explain this block of code, we utilize another function of the ```os``` module called ```.path.dirname```, which essentially gets interpreted to the full filepath of the current directory, **except** the last name of the directory, in this case (*/testfile_pydir*). The ```python parent_dir = os.chdir(parent)``` command ends up evaluating to the following:

![Jupyter New Directory example](/images/jupyter/parentdir_python.png)

Doing so, brings us back to the base directory where we began this tutorial and the subsequent ```print``` command simply displays the output of the current directory.

##### Bash Commands
![Jupyter Bash Change Directory command](/images/jupyter/cd_bash.png)

Similar to what has been explained above, the concept of the commands being run in this code block is simply to change to a new directory called *testfile_bashdir*. Note rather than prepending an exclamation mark (!) before each bash command, I have added ***%%bash*** to the beginning of the code block to instruct the python kernel to interpret the subsequent commands as bash commands.

Each ```echo``` statement simply outputs standard text to display the curent directory, as well as the parent directory, after the ```cd``` (change directory) bash command is executed.

## Filesystem Directory List
So, now that we understand where amongst our file system we are, wouldn't it be nice to see what files or directories are in our current working directory?

Well of course! How else can we access our filesystem programmatically?!?

Let's take a look at commands that list the files in the current directory. Before I do, I'd like to make note of the import of the ***glob*** module. This module is used by python to find all the pathnames matching a specified pattern according to the rules used by the host's operating system shell.

##### Python Code Snippet
![Jupyter Python List Directory code](/images/jupyter/listdir_python.png)

As previously mentioned, searching a directory for file names that match a specific pattern can be accomplished with the module called ```glob```. In the block of code noted above, the current directory variable is being set to the value of the new_path from the code block above. If you were to print the variable named ```current_dir``` you would get an output that reads as the following:

![Jupyter Python Print Directory code](/images/jupyter/printdir_python.png)

Line 3 begins to define a new directory by appending the file type patter that will be searched by the glob function in line 4. Notice that forward slash (/) and a wildcard character (\*) are entered before defining the file type extension. This is intentional for two reasons
1. The ```glob``` function returns results listing the full filepath from the ```new_dir``` location
2. All files within the current directory that end with a *.txt* are matched by the ```glob``` function being called

Line 4 of the code snippet begins with a ```for``` loop, which is intended to execute the ```glob``` function over all files contained within the ```new_dir``` directory. Each resulting filename, including the full filepath, is printed recursively until the ```for``` loop ends when all files have been matched to the *.txt* text string.

##### Bash Commands

![Jupyter Bash List & Grep Directory Files command](/images/jupyter/ls_grep_bash.png)

The bash commands indicated above build on one step further from what has previously been explained. 
In this code block you notice that ```pwd``` is shown to indicate the current working directory, as well as a ```cd``` command to move to a new directory. The final command in the list is a compound command, which utilizes a special character called a pipe "|". This pipe character in simple terms, creates a figurative pipe to funnel the output from the previous command as an input into the next command.

So, lets break this compound command into two parts:
1. ``` ls``` 
> ``` ls -al``` -  This command simply lists the content of the current directory, although with special modifiers (denoted by the flag (-) and the letters \[a, l\]) to specify additional information. The ***-a*** is interpreted by the python kernel to list ***all*** files, including possible hidden files within a directory, such as the current directory (denoted by a ```.```), a parent directory (denoted by a ```..```) or a configuration file (more on configuration files in a later post). The ***-l*** is simply utilized by the kernel to display the results in a vertical arrangement with additional file level permission detail, denoted by the ```-rw-r--r-``` file information. These are file level permissions, which I will explain more of in a later post.
2. ``` grep``` 
> ```grep /*.txt``` - This command is a utility for searching plain-text data sets for lines that match a particularly defined patter, in this case any file that ends with *.txt*. 

As mentioned previously, a pipe ```|``` takes the output from the ```ls -al``` command and directs results as inputs into the ```grep /*.txt``` command. If we were to exclude the ```grep /*.txt``` command, we would see the current directory (denoted by a ```.```) and the parent directory (denoted by a ```..```).

## Conclusion 
To wrap up this tutorial, I hope you now have a grasp of some very basic commands utilized in both python as well as in bash. These explanations are intended to give you a glimpse into the very simple, practical use cases. As you may notice, perhaps it is easier to combine some bash commands within your python notebooks, especially for purpose of navigating throughout your project directories. In a later post, I will review a bash script in greater detail to explain how the script is able to consolidate similarly formatted data files into one master data set.

[1]: https://jupyter.org/ "Jupyter Notebooks"
