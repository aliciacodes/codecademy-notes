# Manhattan Zoo

Ready to try out some of your new Git knowledge?

In this project, you’ll use Git to keep track of meal guidelines for animals at the Manhattan Zoo.

`meal-regimens.txt`

```
Manhattan Zoo
Zookeeper Intern Onboarding:
Meal Guidelines

1. California Sea Lions
   Meal: 40 lbs. salmon, 40 lbs. herring, 20 lbs. Northern Anchovy, 20 lbs. Octupus
   Times: 6:00 am, 9:00 am, 12:00 pm, 3:00 pm, 6:00 pm, 9:00 pm
   Directions: Leave buckets for trainer at 12:00 pm and 3:00 pm, otherwise, follow standard protocol.
2. Ring-tailed Lemurs
   Meal: 10 bags Tamarind pods
   Times: 6:00 am, 3:00 pm, 8:00 pm
   Directions: Empty bags over meadow area during designated times
```

Steps

1. Initialize a new Git repository.

   $ git init

2. Check the status of the repository

​       $ git status

3. Add meal-regimens.txt to the staging area.

​       $ git add meal-regimens.txt

4. Make a commit

​       $ git commit -m "adding meal-regimens.txt to repo"

5. Include this new info in **meal-regimens.txt**.

   ```
   3. Long-Tailed Chinchillas
   Meal: 1 bag animal pellets, 1 bag dried fruit, 1/2 bag cashews, 5 carrots, 3 stalks kale
   Times: 8:00 am
   Directions: disperse contents throughout Chinchilla habitat
   ```

   Click Save.

6. Add **meal-regimens.txt** to the staging area.

   $ git add meal-regimens.txt

   

7. Check the status of the Git project.

   You should see **meal-regimens.txt** listed as “modified”.

   $ git status

   

8. Make a commit.

   $ git commit -m "Add long-tailed chinchillas to meal-regimens.txt"

   

9. View your Git commit history.

   If your cursor is stuck in Git log mode, press “q” on your keyboard to escape.

   $ git log

   

10. Here’s two more animal reports. Include each in **meal-regimens.txt**, making a new commit for each animal added.

    ```
    4. Poison Dart Frogs
    Meal: 1 bag small crickets
    Times: 6:00 am
    Directions: empty bag in frog habitat once daily. Do not touch frogs! Extremely poisonous.
    
    5. Western Lowland Gorilla
    Meal: (Morning) 20 lbs. kale, 10 lbs. celery, 10 lbs. green beans, 5 lbs. carrots, 1 bag sweet potatoes. (Evening) 10 Bananas, 10 apples, 5 oranges, 5 mango, 20 lbs. grapes, 10 lbs. turnips, 5 lbs. white potatoes
    Times: 6:30 am, 12:00 pm, 7:00 pm
    Directions: feed Gorillas in the morning as group, spread forage items during noon meal, and divide quantities for individual feeding in evening
    ```

    Add text and save the txt file.

    $ git add meal-regimens.txt

    $ git commit -m "Add poison dart frogs to meal-regimens.txt"

    Add text and save the txt file.

    $ git add meal-regimens.txt

    $ git commit -m "Add western lowland gorilla to meal-regimens.txt"
