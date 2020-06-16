# Introduction

With strings, there are lots that can be done.

- Parse a giant string for information
- Sanitize a user input to work in a function
- Generate outputs with variable values.

You can do all this with built-in string methods that Python provides. The string methods allow you to change the case of a string, split the string into many smaller strings, join many small strings together in a larger string. and neatly combine changing variables with string outputs. 

In previous materials, `len()` was a *function* that determined the number of characters in a string. These string methods all have the same syntax:

```
py string_name.string_method(arguments)
```

This is not like `len()`, typically a string method is not called at the end of a string, the string is typically in front of the method.

A string method is called at the end of a string and each one has its own method specific arguments

```
>>> 'Hello'.upper()
HELLO
>>> 'Hello'.lower()
hello
>>> 'Hello man'.title()
Hello Man
>>> 'Hello man'.split()
['Hello', 'man']
>>> ' '.join(['Hello', 'man'])
Hello man
>>> 'Hello man'.replace('H', 'J')
Jello man
>>> '       Hello      man   '.strip()
Hello man
>>> "{} {} ".format("Hello", "man")
Hello man
```



# Formatting Methods

Three string methods that change casing of a string: `.lower()`, `.upper()`, and `.title()`.

- `.lower()` - returns string with all lowercase characters.

- `.upper()` - returns string with all uppercase characters.
- `.title()` - returns string with first letter of each word capitalized. 

Here they are in action:

```
>>> favorite_tv_show = "Community"
>>> favorite_tv_show.lower()
community
>>> favorite_tv_show.upper()
COMMUNITY
>>> tv_show_title = favorite_tv_show.title()
Community
```

All these methods can only **create new strings** and do not change the original string. 

<u>Activity</u>

1. You’re a programmer working for an organization that is trying to digitize and store poetry called *Preserve the Verse*. 

   You’ve been given two strings, the  title of a poem and it’s author, and have been asked to reformat them  slightly to fit the conventions of the organization’s database.

   Make `poem_title` have title case and save it to `poem_title_fixed`.

```
poem_title = "spring storm"
poem_author = "William Carlos Williams"
poem_title_fixed = poem_title.title()
```

2. Print `poem_title` and `poem_title_fixed`.

   How did the string change?

```
>>> print(poem_title)
spring storm
```

```
>>> print(poem_title_fixed)
Spring Storm
```

3. The organization’s database also needs the author’s name to be uppercase only.

   Make `poem_author` uppercase and save it to `poem_author_fixed`.

```
poem_author_fixed = poem_author.upper()
```

4. Print `poem_author` and `poem_author_fixed`. 

   Again, how did the string change?

```
>>> print(poem_author)
William Carlos Williams
>>> print(poem_author_fixed)
WILLIAM CARLOS WILLIAMS
```



# Splitting Strings

`.split()` is performed on a string, takes one argument, and returns list of substrings. 

This is the syntax:

```
string_name.split(delimiter)
```

If there is no argument, it will default to splitting at spaces.

```
its_raining_today = "Today, it will rain"
its_raining_today.split()
['Today', ',', 'it', 'will', 'rain']
```

`.split()` returned a list with each word in a string. If we run`.split()` with no spaces, we get the same string.

<u>Activity</u>

1. In the code editor is a string of the first line of the poem *Spring Storm* by William Carlos Williams.

   Use `.split()` to create a list called `line_one_words` that contains each word in this line of poetry.

   ```
   line_one = "The sky has given over"
   line_one_words = line_one.split()
   ```

# Splitting Strings II

Providing an argument for `split()` can dictate the character we want the string to be split on.

```
>>> greatest_fruit = "banana"
>>> greatest_fruit.split('n')
['ba', 'a', 'a']
```

We provided `'a'` as an argument for `.split()` so the string "banana" got split at each `'n'` character into a list of three strings.

What if we split this at a?

```
>>> greatest_fruit.split('a')
['b', 'n', 'n', '']
```

There is an extra space (`' ' `) string in this list. When you split a string on a character that it ends with, you end up with an empty string.

You can use *any* string as argument for `.split()`

<u>Activity</u>

1. Your boss at the Poetry organization sent over a bunch of author names that  he wants you to prepare for importing into the database. Annoyingly, he  sent them over as a long string with the names separated by commas.

   Using `.split()` and the provided string, create a list called `author_names` containing each individual author name as it’s own string.

   ```
   authors = "Audre Lorde, William Carlos Williams, Gabriela Mistral, Jean Toomer, An Qi, Walt Whitman, Shel Silverstein, Carmen Boullosa, Kamala Suraiyya, Langston Hughes, Adrienne Rich, Nikki Giovanni"
   
   author_names = authors.split(',')
   
   print(author_names)
   ```

2. Great work, but now it turns out they didn’t want poet’s first names (why didn’t they just say that the first time!?)

   Create another list called `author_last_names` that only contains the last names of the poets in the provided string.

   ```
   author_last_names = []
   for name in author_names:
     author_last_names.append(name.split()[-1])
     
   print(author_last_names)
   ```

   

# Splitting Strings III

We can split strings using escape sequences. These are used to indicate that we want to split something in a string that's not necessarily a character. Two escape sequence:

- `\n` Newline: Allows us to split multi-line string by line breaks.
- `\t` Horizontal Tab: Useful for data points separated by tabs.

```
book_quote = \
"""
Books, books, books. 
It was not that I read so much. 
I read and re-read the same ones. 
But all of them were necessary to me. 
Their presence, their smell, the letters of their titles, and the texture of their leather bindings.
"""
book_lines = book_quote.split('\n')
print(book_lines)
```

The code is splitting the multi-line string at the newlines (`\n`) that exist at the end of every line and saving it to a new list.

```
['Books, books, books.', It was not that I read so much.', 'I read and re-read the same ones.', 'But all of them were necessary to me.', 'Their presence, their smell, the letters of their titles, and the texture of their leather bindings.']
```

This new list contains smaller strings. Also, Python automatically adds the escaped character (`'`) when creating a new list.

<u>Activity</u> 

1. The organization has sent you over the full text for William Carlos Williams poem *Spring Storm*. They want you to break the poem up into its individual lines.

   Create a list called `spring_storm_lines` that contains a string for each line of *Spring Storm*.

   ```
   spring_storm_lines = spring_storm_text.split('\n')
   ```



# Joining Strings

`.split()` breaks strings apart, `.join()` brings the strings together with a given delimiter. The syntax of `.join()` is:

```
'the_delimeter'.join(list_to_join)
```

This is weird, with `.join()` the arguments seem to be flipped. *Join* is a string method, meaning acting on a string. The string `join()` acts on the delimiter you want to join with so the list you want to join has to be the argument.

```
>>> tonight = ['Tonight', 'tonight', 'The', 'world', 'is', 'full', 'of', 'light']
>>> ' '.join(tonight)
'Tonight tonight The world is full of light'
```

This code takes a list of strings `tonight` and join it together with a space (`' ' ` ):

```
>>> ''.join(tonight)
'TonighttonightTheworldisfulloflight'
```

<u>Activity</u>

1. You’ve been provided with a list of words from the first line of Jean Toomer’s poem [*Reapers*](https://www.poetryfoundation.org/poems/46405/reapers).

   Use `.join()` to combine these words into a sentence and save that sentence as the string `reapers_line_one`.

```
reapers_line_one_words = ["Black", "reapers", "with", "the", "sound", "of", "steel", "on", "stones"]
reapers_line_one = ' '.join(reapers_line_one_words)
```



# Joining Strings II

You can use any string as a delimiter to join together a list of strings.

```
>>> west_side_story_songs = ['America', 'One Hand, One Heart', 'Something's Coming', 'Maria', 'Tonight', 'I Feel Pretty']
```

Join this list together using ANY string. Often used string is a comma (`,`) then we can create a string of *comma separated variables* or CSV.

```
>>> west_side_story_songs_csv = ','.join(west_side_story_songs)
>>> west_side_story_songs_csv
'America,One Hand, One Heart,Something's Coming,Maria,Tonight,I Feel Pretty'
```

You can use *escape sequences* as the delimiter. 

```
america_lyrics = ['Life can be bright in America.', 'If you can fight in America.', 'Life is all right in America.', 'If you're all-white in America.']

america_song_lyrics = '/n'.join(america_lyrics)

print(america_song_lyrics)
```

The code takes the list of strings and joins them using a newline (`\n`) as the delimiter. It then takes the result and prints it:

```
Life can be bright in America.
If you can fight in America.
Life is all right in America.
If you're all-white in America.
```

<u>Activity</u>

1. You’ve been given a list, `winter_trees_lines`, that contains all the lines to William Carlos Williams poem, *Winter Trees*. You’ve been asked to join together the strings in the list together  into a single string that can be used to display the full poem. Name  this string `winter_trees_full`.

   Print your result to the terminal. Make sure that each line of the poem appears on a new line in your string.

```
winter_trees_lines = ['All the complicated details', 'of the attiring and', 'the disattiring are completed!', 'A liquid moon', 'moves gently among', 'the long branches.', 'Thus having prepared their buds', 'against a sure winter', 'the wise trees', 'stand sleeping in the cold.']
winter_trees_full = '\n'.join(winter_trees_lines)
```

# strip()

Strings often aren't super clean, you have unnecessary line breaks, and tabs everywhere.

Python provides a great method for cleaning strings: `strip()`.  Stripping a string removes whitespace characters from the beginning to the end.

```
>>> maria = "                 Maria     "
>>> maria.strip()
# This works with special characters too
maria
>>> maria = "  !!!!          Maria !!!!! "
>>> maria.strip('!')
maria
```

By including `'!'` we can strip all `'!'` characters in the entire string.  It also removes the whitespace

<u>Activity</u>

1. They sent over another list containing all the lines to the Audre Lorde poem, *Love, Maybe*. They want you to join together all of the lines into a single string  that can be used to display the poem again, but this time, you’ve  noticed that the list contains a ton of unnecessary whitespace that  doesn’t appear in the actual poem.

   First, use `.strip()` on each line in the list to remove the unnecessary whitespace and save it as a new list `love_maybe_lines_stripped`.

```
love_maybe_lines = ['Always    ', '     in the middle of our bloodiest battles  ', 'you lay down your arms', '           like flowering mines    ','\n' ,'   to conquer me home.    ']

love_maybe_lines_stripped = []
for line in love_maybe_lines:
    love_maybe_lines_stripped.append(line.strip())
```

2. `.join()` the lines in `love_maybe_lines_stripped` together into one large multi-line string, `love_maybe_full`, that can be printed to display the poem.

   Each line of the poem should show up on its own line.

```
love_maybe_full = '\n'.join(love_maybe_lines_stripped)
```

3. Print `love_maybe_full`.

```
print(love_maybe_full)
```



# Replace

`.replace()` takes two arguments and replaces all instances of the first argument in a string with the second given argument. The syntax looks like this.

```
string_name.replace(character_being_replaced, new_character)
```

Here's an example: 

```
wrong_variable_name = "a variable"
right_variable_name = wrong_variable_name.replace(' ', '_')
>>> right_variable_name
a_variable
```

Every instance of space is changed with an underscore 

<u>Activity</u>

1. The poetry organization has sent over the bio for Jean Toomer as it  currently exists on their site. Notice that there was a mistake with his last name and all instances of *Toomer* are lacking one `o`.  

   Use `.replace()` to change all instances of `Tomer` in the bio to `Toomer`. Save the updated bio to the string `toomer_bio_fixed`.

   ```
   toomer_bio_fixed = toomer_bio.replace("Tomer", "Toomer")
   ```

   

# .find()

`.find()` takes one string argument and searches the string it was run on for that string. It then returns the first *index value* where the string is located. 

An example:

```
>>> 'community'.find('m')
'2'
>>> 'community'.find('mm')
'2'
```

We searched the string `'community'` for the `'m'` string and found the first `'m' `string in the second index spot, so this method returns 2. 

<u>Activity</u>

1. In the code editor is the first line of Gabriela Mistral’s poem [*God Wills It*](https://www.poetryfoundation.org/poetrymagazine/browse?contentId=23104).

   At what index place does the word “disown” appear? Save that index place to the variable `disown_placement`.

```
god_wills_it_line_one = "The very earth will disown you"
disown_placement = god_wills_it_line_one.find("disown")
```



# .format() 

You can include variables in strings too by using `.format()`. This takes on a variable argument and includes them in the string it is run on. You can use `{}` marks as placeholders for variables to be imported. 

```
def my_favorites(type, name):
	return "My favorite {} is {}.".format(type, name)
```

This function takes two arguments and returns a string that includes both the arguments and prints it in a sentence. `.format()` can take many arguments as there are `{}` in the string to support it.

```
>>> my_favorites("TV show", "Community")
"My favorite TV show is Community."
```

Why couldn't you have written this using string concatenation instead of `.format()`, why is this method better? Legibility and reusability. You can reuse the method above to show all of your favorite things!

<u>Activity</u>

1. Write a function called `poem_title_card` that takes two inputs: the first input should be `poet` and the second `title`. The function should use `.format()` to return the following string:

   ```
    The poem "[TITLE]" is written by [POET].
   ```

   For example, if the function is given the inputs

   ```
   poem_title_card("Walt Whitman", "I Hear America Singing")
   ```

   It should return the string

   ```
   The poem "I Hear America Singing" is written by Walt Whitman.		
   ```



```
def poem_title_card(poet, title):
  poem_desc = "The poem \"{}\" is written by {}.".format(title, poet)
  return poem_desc
```



# .format() II

With `.format()` , you have to make sure arguments are in the same order as how you want them to appear in the code. 

You can add keywords in the string to remove this ambiguity. 

```
def my_favorites(type, name):
	return "My favorite {type} is {name}.".format(type = type, name = name)
```

Now, it no longer matters if the arguments are in the wrong order and the reader has a clear understanding of what is going on. 

<u>Activity</u>

1. The function `poem_description` is supposed to use `.format()` to print out some quick information about a poem, but it seems to be causing some errors currently.

   Fix the function by using keywords in the `.format()` method.

```
def poem_description(publishing_date, author, title, original_work):
  poem_desc = "The poem {title} by {author} was originally published in {original_work} in {publishing_date}.".format(publishing_date=publishing_date, author=author, title=title, original_work=original_work)
  return poem_desc
```

2. Run `poem_description` with the following arguments and save the results to the variable `my_beard_description`:

   ```
   author = "Shel Silverstein"
   title = "My Beard"
   original_work = "Where the Sidewalk Ends"
   publishing_date = "1974"
   ```

```
my_beard_description = poem_description("1974", "Shel Silverstein", "My Beard", "Where the Sidewalk Ends")
```

# Review

Excellent work! This lesson has shown you the vast variety of string methods and  their power. Whatever the problem you are trying to solve, if you are  working with strings then string methods are likely going to be part of  the solution.

Over this lesson you’ve learned:

- `.upper()`, `.title()`, and `.lower()` adjust the casing of your string.
- `.split()` takes a string and creates a list of substrings.
- `.join()` takes a list of strings and creates a string.
- `.strip()` cleans off whitespace, or other noise from the beginning and end of a string.
- `.replace()` replaces all instances of a character/string in a string with another character/string.
- `.find()` searches a string for a character/string and returns the index value that character/string is found at.
- `.format()` and f-strings allow you to interpolate a string with variables.

Well I’ve been stringing you along for long enough, let’s get some more practice in!

<u>Activity</u>

1.  *Preserve the Verse* has one final task for you. They have delivered you a string that contains a list of poems, titled `highlighted_poems`, they want to highlight on the site, but they need your help to parse  the string into something that can display the name, title, and  publication date of the highlighted poems on the site.

   First, start by printing `highlighted_poems` to the terminal and see how it displays.

```
highlighted_poems = "Afterimages:Audre Lorde:1997,  The Shadow:William Carlos Williams:1915, Ecstasy:Gabriela Mistral:1925,   Georgia Dusk:Jean Toomer:1923,   Parting Before Daybreak:An Qi:2014, The Untold Want:Walt Whitman:1871, Mr. Grumpledump's Song:Shel Silverstein:2004, Angel Sound Mexico City:Carmen Boullosa:2013, In Love:Kamala Suraiyya:1965, Dream Variations:Langston Hughes:1994, Dreamwood:Adrienne Rich:1987"
print(highlighted_poems)
```

2. The information for each poem is separated by commas, and within this  information is the title of the poem, the author, and the date of  publication.

   Start by splitting `highlighted_poems` at the commas and saving it to `highlighted_poems_list`.

```
highlighted_poems_list = highlighted_poems.split(',')
```

3. Print `highlighted_poems_list`, how does the structure of the data look now?

```
print(highlighted_poems_list)
```

4. Notice that there is inconsistent whitespace in `highlighted_poems_list`. Let’s clean that up.

   Start by creating a new empty list, `highlighted_poems_stripped`. 

   Then, iterate through `highlighted_poems_list` using a for loop and for each poem strip away the whitespace and append it to your new list, `highlighted_poems_stripped`.

```
highlighted_poems_stripped = []
for poems in highlighted_poems_list:
  highlighted_poems_stripped.append(poems.strip())
```

5. Print `highlighted_poems_stripped`.

   Looks good! All the whitespace is cleaned up.

```
print(highlighted_poems_stripped)
```

6. Next we want to break up all the information for each poem into it’s own list, so we end up with a list of lists.

   Create a new empty list called `highlighted_poems_details`.

```
highlighted_poems_details = []
```

7. Iterate through `highlighted_poems_stripped` and split each string around the `:` characters and append the new lists into `highlighted_poems_details`.

```
for poems in highlighted_poems_stripped:
  highlighted_poems_details.append(poems.split(':'))
```

8. Great! Now we want to separate out all of the titles, the poets, and the publication dates into their own lists.

   Create three new empty lists, `titles`, `poets`, and `dates`.

```
titles = []
poets = []
dates = []
```

9. Iterate through `highlighted_poems_details` and for each list in the list append the appropriate elements into the lists `titles`, `poets`, and `dates`.

   For example, for the poem *The Shadow* (1915) by William Carlos Williams your code should be adding `"The Shadow"` to `titles`, `"William Carlos Williams"` to `poets`, and `"1915"` to `dates`.

```
for poem in highlighted_poems_details:
    titles.append(poem[0])
    poets.append(poem[1])
    dates.append(poem[2])
```

10. Finally, write a for loop that uses either f-strings or `.format()` to prints out the following string for each poem:

    ```
    The poem TITLE was published by POET in DATE.
    ```

```
for i in range(len(titles)):
  print("The poem {} was published by {} in {}".format(title[i], poets[i], dates[i]))
```



# Quiz

1. Given the list `greeting = ["Hello", "my", "name", "is", "Earl"]` what line of code would produce a string that contains `”Hello_my_name_is_Earl”.

```
'_'.join(greeting)
```

2. Given the following block of code, what is stored in the string `split_hairs`?

   ```
   dirty_harry = "Go ahead, make my day."
   split_hairs = dirty_harry.split("a")
   ```

```
["Go", "he", "d, m", "ke my d", "y."]
```

3. Consider the string `user_name = "::::::::Eloise        :::::::::::"`. What line of code would clean this string and produce the string `user_name_fixed = "Eloise"`?

```
user_name_fixed = user_name.strip(':').strip()
```

4. Which of the following is a benefit of using `.format()` to include variables in your strings?

It makes your code more legible.

5. Which of the following answer choices best describes the function of the string method `.find()`?

Find searches a string for its argument returns the index location of that argument.

6. Given the poem (*When You Are Old*, by W. B. Yeats) saved as multiline string as shown in the code block,  what code could we use to create a list that contains a string of each  line in the poem?

   ```
   when_you_are_old = \ """When you are old and grey and full of sleep, And nodding by the fire, take down this book, And slowly read, and dream of the soft look Your eyes had once, and of their shadows deep; How many loved your moments of glad grace, And loved your beauty with love false or true, But one man loved the pilgrim soul in you, And loved the sorrows of your changing face; And bending down beside the glowing bars, Murmur, a little sadly, how Love fled And paced upon the mountains overhead And hid his face amid a crowd of stars."""
   ```

```
list_of_lines = when_you_are_old.split("\n")
```



7. Given the string `hello_jerry = "Hi, my name is Jerry"`, which of the following lines of code will produce the string `"Hi, My Name Is Jerry"`?

```
hello_jerry = "Hi, my name is Jerry"
hello_jerry.title()
```

# Project

Link is <a href ="https://www.youtube.com/watch?time_continue=1&v=x1AxPYJwHCw&feature=emb_title">here</a>. You’ve recently been hired as a cashier at the local sewing hobby shop, ***Thread Shed\***.  Some of your daily responsibilities involve tallying the number of  sales during the day, calculating the total amount of money made, and  keeping track of the names of the customers.

Unfortunately, the ***Thread Shed\*** has an extremely out-dating register system and stores all of the transaction information in one huge unwieldy string called `daily_sales`. 

All day, for each transaction, the  name of the customer, amount spent, types of thread purchased, and the  date of sale is all recorded in this same string.  Your task is to use  your Python skills to iterate through this string and clean up each  transaction and store all the information in easier to access lists.

### Break up `daily_sales` in easy to understand lists `customers`, `sales`, and `threads_sold`.

1. First, take a minute to inspect the string `daily_sales` in the code editor. 

   How is each transaction stored? How is each piece of data within the transaction stored?

   Start thinking about how we can split up this string into its individual pieces of data.

2. It looks like each transaction is separated from the next transaction by a `,`, and then each piece of data within a transaction is separated by the artifact `;,;`.

   If we want to split up `daily_sales` into a list of individual transactions, we are going to want to split by `,`, but first, we need to replace the artifact `;,;` to something *without* a comma, so we don’t split any transactions themselves.

   Replace all the instances of `;,;` in `daily_sales` with some other character and save the result to `daily_sales_replaced`.

```
daily_sales_replaced = daily_sales.replace(';,;', '+')
```

3. Now we can split the string into a list of each individual transaction.

   Split `daily_sales_replaced` around commas and save it to a new list `daily_transactions`.

```
daily_transactions = daily_sales_replaced.split(",")
```

4. Print `daily_transactions`.

   How does it look?

```
print(daily_transactions)
```

5. Our next step is to split each individual transaction into a list of its data points.  

   First, define an empty list `daily_transactions_split`

```
daily_transactions_split = []
```

6. Now, iterate through `daily_transactions` (remember, this is a list of strings currently), and for each  transaction, split the string around whatever character you replaced the `;,;` artifacts with in **Step 2**.

   Append each of these split strings (which are lists now) to our new list `daily_transactions_split`.

```
for trans in daily_transactions:
  daily_transactions_split.append(trans.split('+'))
```

7. Print `daily_transactions_split`.

   How’s it looking?

```
print(daily_transactions_split)
```

8. It looks like each data item has inconsistent whitespace around it. First, define an empty list `transactions_clean`.

   Now, Iterate through `daily_transactions_split` and for each transaction iterate through the different data points and strip off any whitespace.

   Add each of these cleaned up transactions to the new list `transactions_clean`.

```
transactions_clean = []
for daily in daily_transactions_split:
  transaction_clean = []
  for data in daily:
  	transaction_clean.append(data.replace("\n", "").strip(" "))
  transactions_cleans.append(transaction_clean)
```

9. Print `transactions_clean`.

   If you performed the last step correctly, you shouldn’t see any unnecessary whitespace.

```
print(transactions_clean)
```

10. Create three empty lists. `customers`, `sales`, and `thread_sold`. We are going to collect the individual data points for each transaction in these lists.

```
customers = []
sales = []
thread_sold = []
```

11. Now, iterate through `transactions_clean` and for each transaction:
    1. Append the customers name to `customers`.
    2. Append the amount of the sale to `sales`.
    3. Append the threads sold to `thread_sold`.

```
for tran in transactions_clean:
  customers.append(tran[0])
  sales.append(tran[1])
  thread_sold.append(tran[2])
```

12. Print `customers`, `sales`, and `thread_sold` to make sure each list is what you are expected.

```
print(customers, sales, thread_sold)
```

13. Now we want to know how much *Thread Shed* made in a day.

    First, define a variable called `total_sales` and set it equal to `0`.

```
total_sales = 0
```

14. Now, consider the list `sales`. It is a list of *strings* that we want to sum. In order for us to sum these values, we will have to remove the `$`, and set them equal to floats.

    Iterate through `sales` and for each item, strip off the `$`, set it equal to a float, and add it to `total_sales`

```
for sale in sales:
  total_sales += float(sale.strip('$'))
```

15. Print `total sales`.

    How much did we make today?

```
print(round(total_sales,2))
```



### How much thread of any specific color was sold?

16. Finally, we want to determine how many of each color thread we sold today. Let’s start with a single color, and then we’ll generalize it.

    First, print out `thread_sold` and inspect it.

```
print(thread_sold)
```

17. We see that `thread_sold` is a list of strings, some are single colors and some are multiple colors separated by the `&` character.

    The end product we want here is a  list that contains an item for each color thread sold, so no strings  that have multiple colors in them.

    First, define an empty list `thread_sold_split`.

```
thread_sold_split = []
```

18. Next, iterate through thread_sold. For each item, check if it is a single  color or multiple colors. If it is a single color, append that color to `thread_sold_split`.

    If it is multiple colors, first split the string around the `&` character and then add each color individually (this was a typo) to `thread_sold_split`.

```
for item in thread_sold:
  for color in item.split("&"):
    thread_sold_split.append(color)
```

19. Great, now we have a list `thread_sold_split` that contains an entry with the color of every thread sold today.

    Define a function called `color_count` that takes one argument, `color`.  The function should iterate through `thread_sold_split` and count the number of times the item is equal to argument, `color`. Then, it should return this count.

```
def color_count(color):
  count = 0
  for thread_color in thread_sold_split:
    if color == thread_color:
      color_total += 1
  return color_total
```

20. Test your new function by running `color_count('white')`.

    Your function should return `28`.

```
print(color_count('white'))
```

21. Define a list called `colors` that stores all of the colored threads that *Thread Shed* offers:

    ```
    colors = ['red','yellow','green','white','black','blue','purple']
    ```

```
colors = ['red','yellow','green','white','black','blue','purple']
```

22. Now, using the list `colors`, the string method `.format()`, and the function `color_count`, iterate through `thread_sold_split` and print a sentence that says how many threads of each color were sold today.

```
for color in colors:
  print("Thread Shed sold {number} threads of {colors} today.".format(number = color_count(color), colors = color)
```
