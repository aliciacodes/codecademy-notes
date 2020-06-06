# Your First Command

**Command Line**: A text-based program for the computer.  It takes commands and gives it to the computer operating system to run.

From this program, you can navigate your computer's files and folders like you do in Finder and Windows Explorer. The difference is there are no visual assets and it is simply text.

Why should you use the command line? Well, you can run programs, write scripts to automate tasks, and combine commands to handle difficult tasks so command line knowledge is extremely important to know.

This course is for unix-based systems like Linux and Mac OS X. 



<u>Activity</u>

1. To access the command line, we use an application called the **terminal**

   In the terminal, after the `$` , type:

   ```
   $ ls
   ```

   and press **enter**.

# ls

In the terminal, you will see `$` sign. This is called a *shell prompt* and appears when the terminal can take a command

The `ls` command looks at the current folder you are in and "lists" the files and folders (directories) inside it.

`ls` is an example of a command which is a prompt to the computer to perform a task.



<u>Activity</u>

In the command line, folders are referred to as directories. Files and directories in the computer are organized in a hierarchal *filesystem*.



# Filesystem

The job of a filesystem is to organize a computer's files and directories into a **tree structure**. 

1. The first directory in the filesystem is the *root* directory. This is the parent for all directories and files in the system.
2. Each parent directory can contain multiple files and directories. 
3. The parent-child relationship continues as long as directories and files are nested. 

<u>Activity</u>

1. Start navigating the filesystem from the command line. Type the `pwd` command and press enter.

```
$ pwd
```



# pwd

`pwd` = "printing working directory"

It outputs the directory you're currently in which is called the *working directory*.

Combined with the `ls` command, you can learn where you are in the filesystem. 



<u>Activity</u>

1. In the terminal, print the working directory

```
$ pwd
```

2. List all files and directories in the working directory.

```
$ ls
```

3. Now, type `cd` and the name of a directory that was listed in the previous command. 

```
$ cd child_directory
```

4. List all the files and directories in the new working directory you are in. 

```
$ pwd
```

# cd I

cd = "change directory"

1. `cd` switches into a directory you specify much like clicking on a folder in Finder on Windows Explorer. `cd ` changes the working directory.
2. When a file, directory, or program is given with a command it's called an *argument*.

<u>Activity</u>

1. Use the `pwd` command to see what directory you are in.

```
$ pwd
```

2. Use the `cd` command to go to another working directory

```
$ cd directory1/directory2
```

3. Type `cd ..` to see the new location and print the working directory you're in.

```
$ cd ..
$ pwd
```



# cd II

```
$ cd diretory1/directory2
```

To go directly to a directory, use `cd` with the directory path as an argument. `cd directory1/directory2` navigates to directory2 and makes that the working directory.

```
$ cd ..
```

To move up one directory, use `cd ..` .

<u>Activity</u>

1. Change the directory using:

   ```
   $ cd ../neightbour_directory
   ```

   This command goes up to the nearest parent directory then it can go to a neighboring directory. Now, list all the files and directories in the working directory.

   ```
   $ pwd
   ```

   

2. Type `mkdir`

```
$ mkdir directory1
```

​	   List all the files and directories in the working directory. Now you see a new directory name`directory1` .

```
$ pwd
```



# mkdir

```
$ mkdir directory1
```

`mkdir` = "make directory"

The mkdir needs the new directory name as an argument and creates the new directory in current working directory.

<u>Activity</u>

1. Navigate to a parent directory using `cd`. 

   ```
   cd ..
   ```

   

2. Then type

   ```
   touch keyboard.txt
   ```

   Use the `pwd` directory to see what has changed.

   ```
   pwd
   ```



# touch

```
touch keyboard.txt
```

The `touch` command creates a new file inside the working directory. 

`Touch` takes the filename as an argument and creates an empty file in working directory.



# Review

What is the command line?

It is a text interface for the computer's operating system. Use terminal to access.

What is a filesystem?

A filesystem organizes the computer's files and directories into a tree structure. It starts with a root directory and each directory can contain multiple child directories and files. 

The five commands learned:

- `pwd ` = name of current working directory
- `ls` = lists all files and directories in the working directory
- `cd` = moves you into specified directory
- `mkdir` = creates a new directory in the working directory
- `touch` = creates a new file in working directory