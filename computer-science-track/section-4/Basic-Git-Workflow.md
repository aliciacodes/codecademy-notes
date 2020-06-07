# Hello Git

Git - Allows you to keep track of changes made to project over time. Records the changes you make to a project, stores the change, then reference them as needed. 

<u>Activity</u>

We’ll get started by taking a look at the screenplay project.

In **scene-1.txt**, add this text:

```
Harry Programmer and the Sorcerer’s Code: Scene 1
```

Then press `enter` to create a new empty line. Once you’ve created the new line, click Run.



# git init

`git init` = Turns the current directory you are in into a Git project and tracks changes. 

`init` means initialize. 

<u>Activity</u>

1. In the terminal, initialize a new Git project.

   Notice the output:

   ```
   Initalized empty Git repository in /home/ccuser/workspace/sorcerers-code/.git/
   ```

   The Git project was created. Click Next to continue.

   ```
   git init
   ```

# Git Workflow

A Git project has three parts:

1. A *Working Directory*:  where all the work is done: creating, editing, deleting, and organizing files. 
2. A *Staging Directory*:  where you'll list changes made to the working directory.
3. A *Repository*: Git permanently stores changes as different versions (revisions) of project.

When working on a Git project:

1. Start by editing a file in the working directory
2. Adding files to staging area
3. Saving changes to Git repository through *commits*.



# git status

As you edit a file, you change the contents of the working directory. Check changes with

```
git status
```

<u>Activity</u>

1. From the terminal, check the status of the **sorcerers-code** project.

   In the output, notice the file in red under `untracked files`. Untracked means that Git sees the file but has not started tracking changes yet.

# git add

For Git to track a file, the file needs to be added to the staging area.

```
git add filename
```

`filename` is the name of the file you are editing and want to add to git.

<u>Activity</u>

1. Add **scene-1.txt** to the staging area in Git. Recall that you will need to identify the file by its name.

   ```
   git add scene-1.txt
   ```

   

2. Check the status of the project in Git.

   In the output, notice that Git indicates the changes to be committed with “new file: scene-1.txt” in green text. Here Git tells us the file was added to the staging area.

   ```
   git status
   ```

   

# git diff

```
git diff filename
```

Now that the file is tracked and in the staging area, we can check the differences between the working directory and staging area. 

<u>Activity</u>

1. In the code editor, add this text to **scene-1.txt**:

   ```
   Dumblediff: I should've known you would be here, Professor McGonagit.
   ```

   Click Run.

   ```
   Harry Programmer and the Sorcerer’s Code: Scene 1
   Dumblediff: I should've known you would be here, Professor McGonagit.
   ```

   

2. From the terminal, use the new command to check the difference between the working directory and the staging area.

   Notice the output:

   - “Harry Programmer and the Sorcerer’s Code: Scene 1” is in the staging area, as indicated in white.

   - Changes to the file are marked with a `+` and are indicated in green.

     ```
     git add scene-1.txt
     ```

3. Add the changes to the staging area in Git. Recall that you will need to identify the file by its name.

```
git add scene-1.txt
```



# git commit

A *commit* is the last step in the workflow. A commit permanently stores changes from the staging area to a repository. 

`git commit-m "any message you want"` 

How to write commit messages:

- Must be in quotation marks
- Written in the present tense
- Should be brief (50 characters or less) when using -m

<u>Activity</u>

1. Make your first commit! From the terminal, type the command along with a commit message. The message should describe the point of the commit.

   If you’re having trouble thinking of a good commit message, reflect on how the project has changed since it began

   ```
   git commit -m "Complete commit!"
   ```



# git log

If you want to refer to an earlier version of the project.

Commits can be viewed with:

```
git log
```

In the logs, you can see a list of your commits. 

In the output, notice:

- A 40-character code, called a *SHA*, that identifies the commit which appears in orange text

- The commit author.

- The date and time of the commit

- The commit message

  

  # Review

- Git is the industry-standard version control system
- Use commands to track changes in your project
  - `git init` creates a new Git repository
  - `git status` gives status on whether repository is committed or not in the working and staging directory
  - `git add` adds files to staging area from working directory
  - `git diff` difference between working and staging area
  - `git commit` stores file changes from staging area in repository
  - `git log` lists all previous changes