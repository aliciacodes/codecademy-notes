# SnapFit Robots, Inc.

Now that you’ve had more practice with the Git workflow, let’s solidify your new skills even more.

In this project, you will be working on assembly instructions for Snap-Fit Robots Inc., a build-it-yourself robot company.

Steps:

`disclaimer.txt`

```
SNAPFIT ROBOTS PRODUCT DISCLAIMER

Your Snapfit Robot Model i075 is provided with guarantee of limited 1-year warranty only. Outside of maintenance and malfunction descriptions covered in the warranty, customer shall make no claims of any kind, either express or implied, including but not limited to warranties of sellability, fitness for specific usage, of title, or of noninfringement of third and fourth party rights, and/or rights to attend robot parties. Use of the product by uninformed user is at the user’s risk.
```



1. Initialize a new Git project.

   ```
   $ git init
   ```

2. Check the status of the Git project.

   You will see multiple files listed in the output as “Untracked”.

```
$ git status
```

3. Add each file to the Git staging area.

```
$ git add disclaimer.txt
$ git add instruction.txt
$ git add warranty.txt
```

or

```
$ git add .
```

4. Check the status of the Git project again.

```
git status
```

5. Make a commit

```
git commit -m "Adding multiple files"
```

6. View your commit log.

   ```
   git log
   ```

7. Include this line in disclaimer.txt

```
Warning: For best battery life, do not leave robot battery charging overnight
```

Save this file



8. Add the file to the staging area

```
git add disclaimer.txt
```

9. Now make a commit

```
git commit -m "Modifying the disclaimer"
```

10. View your Git commit log again to identify your commit.

```
git log
```

11. Revise each file in whatever ways you’d like. Then add your changes to the staging area and make another commit.

```
git add .
git commit -m "Modifying the disclaimer"
```

