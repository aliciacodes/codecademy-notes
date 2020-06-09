# ython Gradebook

**Create Some Lists:**

1. Create a list called `subjects` and fill it with the classes you are taking:
   - `"physics"`
   - `"calculus"`
   - `"poetry"`
   - `"history"`

```
subjects = ["physics", "calculus", "poetry", "history"]
```

2. Create a list called `grades` and fill it with your scores:

- `98`
- `97`
- `85`
- `88`

```
grades = [98, 97, 85, 88]
```

3. Use the `zip()` function to combine `subjects` and `grades`.

   Save this zip object as a `list` into a variable called `gradebook`.

```
gradebook = zip(subjects, grades)
```

4. Print `gradebook`.

   Does it look how you expected it would? Yes it does.

```
print(list(gradebook))
```

**Add More Subjects**

5. Your grade for Computer Science class just came in! You got a perfect score, 100!

After your definitions of `subjects` and `grades` but *before* you create `gradebook`, use `append` to add `"computer science"` to `subjects` and `100` to `grades`.

```
subjects = ["physics", "calculus", "poetry", "history"]

grades = [98, 97, 85, 88]

subjects.append("computer science")
grades.append(100)

gradebook = list(zip(subjects, grades))
print(list(gradebook))
```

6. Your grade for visual arts just came in! You got a 93!

   After the creation of `gradebook` (but before you `print` it out), use `append` to add `("visual arts", 93)` to `gradebook`.

```
gradebook.append(("visual arts", 93))
```

**One Big Gradebook!**

7. You also have your grades from last semester, stored in `last_semester_gradebook`. Create a new variable `full_gradebook` with the items from both `gradebook` and `last_semester_gradebook`.

```
full_gradebook = gradebook + last_semester_gradebook
```

