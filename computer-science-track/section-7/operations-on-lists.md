# Operations on Lists

Now, we'll work on existing lists of data. In this lesson, you'll learn how to:

- Get the length of a list
- Select subsets of a list (called *subsets*)
- Count number of times certain elements appear in a list
- Sort a list of items

# Length of a List

The number of items in a list is called its *length*.

In Python, there is a function called `len()` to do this. You can save this to a variable.

```
a_list = [1, 2, 3, 4]
print(len(my_list))
# returns 4
```

<u>Activity</u>

1. Calculate the length of `list1` and save it to the variable `list1_len`.

```
list1_len = len(list1)
```

2. Use `print` to examine `list1_len`.

```
print(list1_len)
```

3. Change the `range` command that generates `list1` so that it skips `3` instead of `2` between items.

   How does this change `list1_len`?

```
list1 = range(2, 20, 3)
```



# Selecting List Elements I

Asia is trying to fill a position at a large tech company. She has several candidates, represented by this list:

```
interviews = ['Erin', 'Joe', 'Fred', 'Rose', 'Kenny']
```

First, `Erin `will be called then `Joe`.  The position (order) these items are in the list is called an `index`. 

These lists are *zero-induced* which means the first element has an index of 0 not 1. 

Here are examples of that:

| Element   | Index |
| --------- | ----- |
| `'Erin'`  | `0`   |
| `'Joe'`   | `1`   |
| `'Fred'`  | `2`   |
| `'Rose'`  | `3`   |
| `'Kenny'` | `4`   |

Even though `'Fred'` is the third element, the index of the list is `2`. 

To select a single item from the list, you can use square brackets (`[]`) and the index of the list item.

To call the fourth element in the list, we can use `interviews[3]`. 

```
print(interviews[3])
```

<u>Activity</u>

```
employees = ['Michael', 'Dwight', 'Jim', 'Pam', 'Ryan', 'Andy', 'Robert']
```

1. Use square brackets (`[` and `]`) to select the element with index `4` from the list `employees`. Save it to the variable `index4`.

```
index4 = employees[4]
```

2. Use `print` and `len` to display how many items are in `employees`.

```
print(len(employees))
```

3. Paste the following code into **script.py**:

```
print(employees[8])
```

What happens? Why?

There is an IndexError since this index doesn't exist in our code.

4. Selecting an element that does not exist produces an `IndexError`.

   In the line of code that you pasted, change `8` to a different number so that you don’t get an `IndexError`.

```
print(employees[6])
```



# Selecting List Elements II

What if we want the last element of the list?

We can use index `-1` here to select the last item of the list no matter the size of the list.

Consider a list with 5 elements.

```
a_list = [1, 2, 3, 4, 5]
```

If we select the `-1` element, we get the ending element, `5`. 

```
>>> print(a_list[-1])
5
```

This is the same as selecting an element with index `4`.

```
>>> print(a_list[4])
5
```



<u>Activity</u>

1. Use `print` and `len` to display the length of `shopping_list`.

```
shopping_list = ['eggs', 'butter', 'milk', 'cucumbers', 'juice', 'cereal']
print(len(shopping_list))
```

2. Get the last element of `shopping_list` using the `-1` index. Save this element to the variable `last_element`.

```
last_element = shopping_list[-1]
```

3. Now select the element with index `5` and save it to the variable `element5`.

```
element5 = shopping_list[5]
```

4. Use `print` to display both `element5` and `last_element`.

```
print(element5, last_element)
```



# Slicing Lists

Now we have a list of numbers

```
a_list = [0, 1, 2, 3, 4, 5, 6]
```

We want to select elements `1` to `5`. 

We use this using the following syntax: `a_list = [start_index:end_index]`. The `start_index` is the element we want to include in the selection, so we put `1`. The `end_index` is the index of one more than the last index, so we use `6`. 

```
shorter_list = [1:6
print(shorter_list)
# would return [1, 2, 3, 4, 5]
```

<u>Activity</u>

1. Use `print` to examine the variable `beginning`.

   How many elements does it contain?

```
suitcase = ['shirt', 'shirt', 'pants', 'pants', 'pajamas', 'books']

beginning = suitcase[0:2]

print(beginning)
```

2. Modify `beginning`, so that it selects the first 4 elements of `suitcase`.

```
beginning = suitcase[0:4]
```

3. Create a new list called `middle` that contains the middle two items from `suitcase`.

```
middle = suitcase[2:4]
```



# Slicing Lists II

Select first 3 elements, we can use this snippet of code:

```
>>> pokemon = ['Bulbasaur', 'Squirtle', 'Charmander', 'Pikachu']
>>> print(pokemon[0:3])
```

If starting at the beginning of the list, you can omit the `0`. 

```
>>> print(pokemon[:3])
['Bulbasaur', 'Squirtle', 'Charmander']
```

The syntax is similar to doing this to the end of the list

```
print(pokemon[3:])
```

We can also use *negative* indexes to go backward from last element. 

```
>>> print(pokemon[-3:])
['Squirtle', 'Charmander', 'Pikachu']
```

<u>Activity</u>

1. Create a new list called `start` containing the first 3 elements of `suitcase`.

```
start = suitcase[:3]
```

2. Create a new list called `end` containing the final two elements of `suitcase`.

```
end = suitcase[4:]
```



# Counting elements in a list

We have a list called `word` that contains the letters in `Massachusetts`

```
letters = ['m', 'a', 's', 's', 'a', 'c', 'h', 'u', 's', 'e', 't', 't', 's']
```

We would like to know how many times `s` appears in the word, so we use count. 

```
s_count = letters.count('s')
print(s_count)
# prints out 4
```

<u>Activity</u>

```
votes = ['Jake', 'Jake', 'Laurie', 'Laurie', 'Laurie', 'Jake', 'Jake', 'Jake', 'Laurie', 'Cassie', 'Cassie', 'Jake', 'Jake', 'Cassie', 'Laurie', 'Cassie', 'Jake', 'Jake', 'Cassie', 'Laurie']
```

1. Mrs. WIlson’s class is voting for class president. She has saved each student’s vote into the list `votes`.

   Use `count` to determine how many students voted for `'Jake'`. Save your answer as `jake_votes`.

   ```
   jake_votes = votes.count('Jake')
   ```

2. Use `print` to examine `jake_votes`.

```
print(jake_votes)
```



# Sorting List I

There are times when we need to sort a list in numerical or alphabetical order.

To, do this we use `.sort()`. We have a list of names:

```
names = ['Elsa', 'Anna', 'Mateo', 'Jane', 'Raphael', 'Pietra']
print(names)
```

This would print:

```
['Elsa', 'Anna', 'Mateo', 'Jane', 'Raphael', 'Pietra']
```

Now, we should apply `.sort()`:

```
names.sort()
print(names)
# returns ['Anna', 'Elsa', 'Jane', 'Pietra', 'Raphael']
```

NOTE: `sort()` like `zip()` needs the name of the list in front of it. Else, it will result to a `NameError`. 

`sort` doesn't return anything so assigning it to another variable will return `None`.

```
sorted_names = names.sort()
print(sorted_names)
#prints None, but still edited the list
>>> print(names)
['Anna', 'Elsa', 'Jane', 'Pietra', 'Raphael']
```



<u>Activity</u>

1. Use `sort` to sort `addresses`.

```
### Exercise 1 & 2 ###
addresses = ['221 B Baker St.', '42 Wallaby Way', '12 Grimmauld Place', '742 Evergreen Terrace', '1600 Pennsylvania Ave', '10 Downing St.']

# Sort addresses here:
addresses.sort()

### Exercise 3 ###
names = ['Ron', 'Hermione', 'Harry', 'Albus', 'Sirius']
# sort(names)

### Exercise 4 ###
cities = ['London', 'Paris', 'Rome', 'Los Angeles', 'New York']

sorted_cities = cities.sort()
```



2. Use `print` to see how `addresses` changed.

```
# Sort addresses here:
addresses.sort()
print(addresses)
```

3. Remove the `#` in front of the line `sort(names)`. Edit this line so that it runs without producing a `NameError`.

```
names = ['Ron', 'Hermione', 'Harry', 'Albus', 'Sirius']
names.sort()
```

4. Use `print` to examine `sorted_cities`. Why is it not the sorted version of `cities`?

```
cities = ['London', 'Paris', 'Rome', 'Los Angeles', 'New York']

sorted_cities = cities.sort()
print(sorted_cities)
```



# Sorting Lists II

Second way to sort a list is to use `sorted`. The only differences in function are that it generates a new list based off the given list argument and that it is written like `print()`.

```
names = ['Elsa', 'Anna', 'Mateo', 'Jane', 'Raphael', 'Pietra']
sorted_names = sorted(names)
print(sorted_names)
['Anna', 'Elsa', 'Jane', 'Pietra', 'Raphael']
```

`sorted` doesn't change the original array.

```
>>> print(names)
['Elsa', 'Anna', 'Mateo', 'Jane', 'Raphael', 'Pietra']
```

<u>Activity</u>

1. Use `sorted` to order `games` and create a new list called `games_sorted`.

```
games = ['Portal', 'Minecraft', 'Pacman', 'Tetris', 'The Sims', 'Pokemon']
games_sorted = sorted(games)
```

2. Use `print` to inspect `games` and `games_sorted`. How are they different?

```
print(games)
print(games_sorted)
```



# Review

In this lesson, we learned how to:

- Get the length of a list
- Select subsets of a list (called *slicing*)
- Count the number of times that an element appears in a list
- Sort a list of items

<u>Activity</u>

1. `inventory` is a list of items that are in the warehouse for Bob’s Furniture. How many items are in the warehouse?

   Save your answer to `inventory_len`.

   ```
   inventory = ['twin bed', 'twin bed', 'headboard', 'queen bed', 'king bed', 'dresser', 'dresser', 'table', 'table', 'nightstand', 'nightstand', 'king bed', 'king bed', 'twin bed', 'twin bed', 'sheets', 'sheets', 'pillow', 'pillow']
   
   inventory_len = len(inventory)
   ```

   

2. Select the first element in `inventory`. Save it to the variable `first`.

```
first = inventory[0]
```

3. Select the last item from `inventory` and save it to the variable `last`.

```
last = inventory[-1]
```

4. Select items from the `inventory` starting at index `2` and up to, but not including, index `6`.

   Save your answer to `inventory_2_6`.

```
inventory_2_6 = inventory[2:6]
```

5. Select the first 3 items of `inventory` and save it to the variable `first_3`.

```
first_3 = inventory[:3]
```

6. How many `'twin bed'`s are in `inventory`? Save your answer to `twin_beds`.

```
twin_beds = inventory.count('twin bed')
```

7. Sort `inventory` using `.sort()`.

```
inventory.sort()
```



# The Quiz

Which of the following code selects the last three elements of `mylist`?

```
mylist[-3:]
```

Which of the following lines of code will tell us how many time `win` appears in the list `game_schedule`?

```
game_schedule.count("win")
```

Which of the following lines of code would select the letter `e` from `mylist`:

```
mylist = ['a', 'b', 'c', 'd', 'e']
```

```
mylist[-1]
```

Which of the following lines of code would select the list `['b', 'c']` from `mylist`:

```
mylist = ['a', 'b', 'c', 'd', 'e']
```

```
mylist[1:3]
```

Which of the following lines of code would select the letter `d` from `mylist`:

```
mylist = ['a', 'b', 'c', 'd', 'e']
```

```
mylist[3]
```

Which of the following lines of code will correctly sort `mylist`?

```
mylist.sort()
```

Which of the following commands will return the length of the list `mylist`?

```
len(mylist)
```



Which of the following would be generated by the code snippet?

```
mylist = ['a', 'b', 'c', 'd', 'e', 'f'] 
print(mylist[2:5])
```

```
['c', 'd', 'e']
```



# Challenge Part 1

In the first challenge, you create a function that has one parameter `lst`. The function adds the last two elements of `lst` three times and append all the results. This was hard for me!

```
#Write your function here
def append_sum(lst):
  first_num = lst[len(lst) - 1] + lst[len(lst) - 2]
  lst.append(first_num)
  second_num = lst[len(lst) - 1] + lst[len(lst) - 2]
  lst.append(second_num)
  third_num = lst[len(lst) - 1] + lst[len(lst) - 2]
  lst.append(third_num)
  return lst
#Uncomment the line below when your function is done
print(append_sum([1, 1, 2]))
#returns [1, 1, 2, 3, 5, 8]
```

```
#Write your function here
def append_sum(lst):
  lst.append(lst[-1] + lst[-2])
  lst.append(lst[-1] + lst[-2])
  lst.append(lst[-1] + lst[-2])
  return lst

#Uncomment the line below when your function is done
print(append_sum([1, 1, 2]))
```



In the second challenge, the function takes two parameters named `lst1` and `lst2`.

The function compares two lists and if one list contains more elements, then it returns the last element of the list. If they are the same size, then automatically default for the first argument.

```
#Write your function here
def larger_list(lst1,lst2):
  if(len(lst1) > len(lst2)):
    return lst1[len(lst1) - 1]
  elif (len(lst1) < len(lst2)):
    return lst2[len(lst2) - 1]
  else:
    return lst1[len(lst1) - 1]
#Uncomment the line below when your function is done
print(larger_list([4, 10, 2, 5], [-10, 2, 5, 10]))
```

```
#Write your function here
def larger_list(lst1, lst2):
  if len(lst1) >= len(lst2):
    return lst1[-1]
  else:
    return lst2[-1]

#Uncomment the line below when your function is done
print(larger_list([4, 10, 2, 5], [-10, 2, 5, 10]))
```



The third function, has three parameters: a list, an item (could be string or integer), and integer. The function returns `True` if the item appears more than the given integer amount of time. Should return false otherwise. 

```
#Write your function here
def more_than_n(lst, item, n):
  if lst.count(item) > n:
    return True
  else:
    return False

#Uncomment the line below when your function is done
print(more_than_n([2, 4, 6, 2, 3, 2, 1, 2], 2, 3))
```



The fourth function as one parameter that is a list. The function appends the size of the list to the end of the list. This will return a new list. 

```
#Write your function here
def append_size(lst):
  new_lst = lst + [len(lst)]
  return new_lst

#Uncomment the line below when your function is done
print(append_size([23, 42, 108]))
```

```
#Write your function here
def append_size(lst):
  lst.append(len(lst))
  return lst

#Uncomment the line below when your function is done
print(append_size([23, 42, 108]))
```

 

The final function takes two lists and combines the two lists into one new list, sorts the result, and return new sorted list.

```
#Write your function here
def combine_sort(lst1,lst2):
  lst1 = lst1 + lst2
  lst1.sort()
  return lst1
#Uncomment the line below when your function is done
print(combine_sort([4, 10, 2, 5], [-10, 2, 5, 10]))
```

```
#Write your function here
def combine_sort(lst1, lst2):
  unsorted = lst1 + lst2
  sortedList = sorted(unsorted)
  return sortedList

#Uncomment the line below when your function is done
print(combine_sort([4, 10, 2, 5], [-10, 2, 5, 10]))
```



# Advanced Python Code Challenges: Lists

Function one has one integer function. This function returns a list of every third number between the integer and 100 (inclusive).

```
#Write your function here
def every_three_nums(start):
  return list(range(start,101,3))

#Uncomment the line below when your function is done
print(every_three_nums(91))
```

In the second function, there are three parameters: a list, a start integer, and end integer. This returns a list where all elements within an index between start and end (inclusive) is removed. This too was pretty hard and required me to think some. 

```
#Write your function here
def remove_middle(lst, start, end):
  lst = lst[:start] + lst[end+1:]
  return lst

#Uncomment the line below when your function is done
print(remove_middle([4, 8, 15, 16, 23, 42], 1, 3))
```

In the third function, it takes a list, an `item1`, and `item2`.  Whichever item appears more, you should return that. Return the first item if they are tied.

```
#Write your function here
def more_frequent_item(lst,item1,item2):
  if lst.count(item1) > lst.count(item2):
    return item1
  elif lst.count(item1) < lst.count(item2):
    return item2
  else:
    return item1
#Uncomment the line below when your function is done
print(more_frequent_item([2, 3, 3, 2, 3, 2, 3, 2, 3], 2, 3))
```

```
#Write your function here
def more_frequent_item(lst, item1, item2):
  if lst.count(item1) >= lst.count(item2):
    return item1
  else:
    return item2

#Uncomment the line below when your function is done
print(more_frequent_item([2, 3, 3, 2, 3, 2, 3, 2, 3], 2, 3))
```

The fourth function takes in two parameters: one that is list and one that is an integer named `index`. The function returns a new list where all values are the same, except the location of the `index` value should be doubled. Function should return the original list if it's not a valid index.

```
#Write your function here
def double_index(lst, index):
  if index > (len(lst)-1):
    return lst
  else:
    num = (lst[index] * 2)
    lst = lst[:index] + [num] + lst[index+1:]
    return lst
#Uncomment the line below when your function is done
print(double_index([3, 8, -10, 12], 2))
```

```
#Write your function here
def double_index(lst, index):
  # Checks to see if index is too big
  if index >= len(lst):
    return lst
  else:
    # Gets the original list up to index
    new_lst = lst[0:index]
 # Adds double the value at index to the new list 
  new_lst.append(lst[index]*2)
  #  Adds the rest of the original list
  new_lst = new_lst + lst[index+1:]
  return new_lst

#Uncomment the line below when your function is done
print(double_index([3, 8, -10, 12], 2))
```



The final function for today takes only a list. If there is an odd number, return the middle element. If there are an even number of elements, then the function should return average of middle two elements. This was hard too! I wasn't able to figure it out completely given the time constraints, but I did get very close. 

```
#Write your function here
def middle_element(lst):
  if len(lst) % 2 == 0:
    sum = lst[int(len(lst)/2)] + lst[int(len(lst)/2) - 1]
    return sum / 2
  else:
    return lst[int(len(lst)/2)]

#Uncomment the line below when your function is done
print(middle_element([5, 2, -10, -4, 4, 5]))
```

# Tuple Video

https://www.youtube.com/watch?time_continue=6&v=yDvRR8nWMNI&feature=emb_titlehttps://www.youtube.com/watch?time_continue=6&v=yDvRR8nWMNI&feature=emb_title

