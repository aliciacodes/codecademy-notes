# Carly's Clippers

You are the Data Analyst at Carly’s Clippers, the newest hair salon on the block. Your job is to go through the lists of data that have been collected in the past couple of weeks. You will be calculating some important metrics that Carly can use to plan out the operation of the business for the rest of the month.

You have been provided with three lists:

- `hairstyles`: the names of the cuts offered at Carly’s Clippers
- `prices`: the price of each hairstyle in the `hairstyles` list
- `last_week`: the number of each hairstyle in `hairstyles` that was purchased last week

<u>Steps</u>

1. Carly wants to be able to market her low prices. We want to find out what the average price of a cut is.

   First, let’s sum up all the prices of haircuts. Create a variable `total_price`, and set it to `0`.

   ```
   hairstyles = ["bouffant", "pixie", "dreadlocks", "crew", "bowl", "bob", "mohawk", "flattop"]
   
   prices = [30, 25, 40, 20, 20, 35, 50, 35]
   
   last_week = [2, 3, 5, 8, 4, 4, 6, 2]
   
   total_price = 0
   ```

2. Iterate through the `prices` list and add each price to the variable `total_price`.

   ```
   for i in prices:
   	total_price += i
   ```

3. After your loop, create a variable called `average_price` that is the `total_price` divided by the number of prices.

   You can get the number of prices by using the `len()` function.

   ```
   average_price = total_price/len(prices)
   ```

4. Print the value of `average_price` so the output looks like:

   ```
   Average Haircut Price: <average_price>
   ```

   ```
   print("Average Haircut Price: " + str(average_price))
   ```

   

5. That average price is more expensive than Carly thought it would be! She wants to cut all prices by 5 dollars.

   Use a list comprehension to make a list called `new_prices`, which has each element in `prices` minus `5`.

   ```
   new_prices = [price - 5 for price in prices]
   ```

   

6. Print `new_prices`.

   ```
   print(new_prices)
   ```

   

7. Carly really wants to make sure that Carly’s Clippers is a profitable endeavor. She first wants to know how much revenue was brought in last week.

   Create a variable called `total_revenue` and set it to `0`.

   ```
   total_revenue = 0
   ```

   

8. Use a `for` loop to create a variable `i` that goes from `0` to `len(hairstyles)`

   Hint: You can use `range()` to do this!

   ```
   for i in range(len(hairstyles)):
   ```

   

9. Add the product of `prices[i]` (the price of the haircut at position `i`) and `last_week[i]` (the number of people who got the haircut at position `i`) to `total_revenue` at each step. These two steps were confusing and should be combined into one.

   ```
   for i in range(len(hairstyles)):
   	total_revenue += prices[i] * last_week[i]
   ```

10. After your loop, print the value of `total_revenue`, so the output looks like:

    ```
    Total Revenue: <total_revenue>
    ```

    ```
    print(total_revenue)
    ```

    

11. Find the average daily revenue by dividing `total_revenue` by 7. Call this number `average_daily_revenue` and print it out.

    ```
    average_daily_revenue = total_revenue/7
    print(average_daily_revenue)
    ```

    

12. Carly thinks she can bring in more customers by advertising all of the haircuts she has that are under `30` dollars.

    Use a list comprehension to create a list called `cuts_under_30` that has the entry `hairstyles[i]` for each `i` for which `new_prices[i]` is less than `30`.

    You can use `range()` in your list comprehension to make `i` go from `0` to `len(new_prices) - 1`.

    ```
    cuts_under_30= [hairstyle for hairstyle in (len(new_prices) - 1) if price[i] < 30]
    ```

    

# Code Challenges: Loops

1. Create a function named `divisible_by_ten()` that takes a list of numbers named `nums` as a parameter.

   Return the count of how many numbers in the list are divisible by `10`.

```
#Write your function here
def divisible_by_ten(nums):
  count = 0
  for num in nums:
    if num % 10 == 0:
      count += 1
  return count

#Uncomment the line below when your function is done
#print(divisible_by_ten([20, 25, 30, 35, 40]))
```

```
def divisible_by_ten(nums):
  count = 0
  for number in nums:
    if (number % 10 == 0):
      count += 1
  return count

#Uncomment the line below when your function is done
print(divisible_by_ten([20, 25, 30, 35, 40]))
```



2. Create a function named `add_greetings()` which takes a list of strings named `names` as a parameter.

   In the function, create an empty list that will contain each greeting. Add the string `"Hello, "` in front of each name in `names` and `append` the greeting to the list.

   Return the new list containing the greetings.

```
def add_greetings(names):
	greeting = []
	for name in names:
		greeting.append('Hello, ' + name)
	return greeting
```

3. Write a function called `delete_starting_evens()` that has a parameter named `lst`.

   The function should remove elements from the front of `lst` until the front of the list is not even. The function should then return `lst`.

   For example if `lst` started as `[4, 8, 10, 11, 12, 15]`, then `delete_starting_evens(lst)` should return `[11, 12, 15]`.

   Make sure your function works even if every element in the list is even! This is definitely a trickier problem to solve. 

```
def delete_starting_evens(lst):
	for i in range(len(lst)):
		if lst[0] % 2 == 0:
			lst.pop(0)
	return lst
```

```
#Write your function here
def delete_starting_evens(lst):
  while (len(lst) > 0 and lst[0] % 2 == 0):
    lst = lst[1:]
  return lst

#Uncomment the lines below when your function is done
print(delete_starting_evens([4, 8, 10, 11, 12, 15]))
print(delete_starting_evens([4, 8, 10]))
```



4. Create a function named `odd_indices()` that has one parameter named `lst`.

   The function should create a new empty list and add every element from `lst` that has an odd index. The function should then return this new list.

   For example, `odd_indices([4, 3, 7, 10, 11, -2])` should return the list `[3, 10, -2]`.

   ```
   #Write your function here
   def odd_indices(lst):
     new_lst = []
     for i in range(len(lst)):
       if i % 2 != 0:
         new_lst.append(lst[i])
     return new_lst
   #Uncomment the line below when your function is done
   print(odd_indices([4, 3, 7, 10, 11, -2]))
   ```

   ```
   #Write your function here
   def odd_indices(lst):
     new_lst = []
     for index in range(1, len(lst), 2):
       new_lst.append(lst[index])
     return new_lst
   
   #Uncomment the line below when your function is done
   print(odd_indices([4, 3, 7, 10, 11, -2]))
   ```

   

5. Create a function named `exponents()` that takes two lists as parameters named `bases` and `powers`. Return a new list containing every number in bases `raised` to every number in `powers`.

   For example, consider the following code.

   ```
   exponents([2, 3, 4], [1, 2, 3])
   ```

   the result would be the list `[2, 4, 8, 3, 9, 27, 4, 16, 64]`. It would first add two to the first. Then two to the second. Then two to the third, and so on.

   ```
   #Write your function here
   def exponents(bases, powers):
     new_lst = []
     for base in bases:
       for power in powers:
           new_lst.append(base ** power)
     return new_lst
   
   #Uncomment the line below when your function is done
   print(exponents([2, 3, 4], [1, 2, 3]))
   ```

   

6. Create a function named `larger_sum()` that takes two lists of numbers as parameters named `lst1` and `lst2`.

   The function should return the list whose elements sum to the greater number. If the sum of the elements of each list are equal, return `lst1`.

   ```
   #Write your function here
   def larger_sum (lst1, lst2):
     sum1 = 0
     sum2 = 0
     for i in range(len(lst1)):
       sum1 += lst1[i]
       sum2 += lst2[i]
     if sum1 >= sum2:
       return lst1
     else:
       return lst2
   #Uncomment the line below when your function is done
   print(larger_sum([1, 9, 5], [2, 3, 7]))
   ```

   ```
   #Write your function here
   def larger_sum(lst1, lst2):
     sum1 = 0
     sum2 = 0
     for number in lst1:
       sum1 += number
     for number in lst2:
       sum2 += number
     if sum1 >= sum2:
       return lst1
     else: 
       return lst2
   
   #Uncomment the line below when your function is done
   print(larger_sum([1, 9, 5], [2, 3, 7]))
   ```

   

7. Create a function named `over_nine_thousand()` that takes a list of numbers named `lst` as a parameter.

   The function should sum the elements of the list until the sum is greater than `9000`. When this happens, the function should return the sum. If the sum of all of the elements is never greater than `9000`, the function should return total sum of all the elements. If the list is empty, the function should return `0`.

   For example, if `lst` was `[8000, 900, 120, 5000]`, then the function should return `9020`.

   ```
   #Write your function here
   def over_nine_thousand(lst):
    sum = 0
    for i in lst:
      if sum <= 9000:
        sum += i
      else:
        break
    return sum
   #Uncomment the line below when your function is done
   print(over_nine_thousand([8000, 900, 120, 5000]))
   ```

   ```
   #Write your function here
   def over_nine_thousand(lst):
     sum = 0
     for number in lst:
       sum += number
       if (sum > 9000):
         break
     return sum
   
   #Uncomment the line below when your function is done
   print(over_nine_thousand([8000, 900, 120, 5000]))
   ```

8. Create a function named `max_num()` that takes a list of numbers named `nums` as a parameter.

   The function should return the largest number in `nums`

   ```
   #Write your function here
   def max_num(nums):
     large_num = -100000000000
     for i in nums:
       if i > large_num:
         large_num = i
     return large_num
   #Uncomment the line below when your function is done
   print(max_num([50, -10, 0, 75, 20]))
   ```

   ```
   #Write your function here
   def max_num(nums):
     maximum = nums[0]
     for number in nums:
       if number > maximum:
         maximum = number
     return maximum
   
   #Uncomment the line below when your function is done
   print(max_num([50, -10, 0, 75, 20]))
   ```

9. Write a function named `same_values()` that takes two lists of numbers of equal size as parameters.

   The function should return a list of the indices where the values were equal in `lst1` and `lst2`.

   For example, the following code should return `[0, 2, 3]`

   ```
   same_values([5, 1, -10, 3, 3], [5, 10, -10, 3, 5])
   ```

   ```
   #Write your function here
   def same_values(lst1, lst2):
       lst =[]
       for i in range(len(lst1)):
         if lst1[i] == lst2[i]:
             lst.append(i)
       return lst
   
   #Uncomment the line below when your function is done
   print(same_values([5, 1, -10, 3, 3], [5, 10, -10, 3, 5]))
   ```

10. Create a function named `reversed_list()` that takes two lists of the same size as parameters named `lst1` and `lst2`.

    The function should return `True` if `lst1` is the same as `lst2` reversed. The function should return `False` otherwise.

    For example, `reversed_list([1, 2, 3], [3, 2, 1])` should return `True`.

    ```
    #Write your function here
    def reversed_list(lst1, lst2):
      for i in range(len(lst1)):
        if lst1[i] == lst2[len(lst1)- 1 - i]:
            continue
        else:
            return False
      return True
    
    #Uncomment the lines below when your function is done
    print(reversed_list([1, 2, 3], [3, 2, 1]))
    print(reversed_list([1, 5, 3], [3, 2, 1]))
    ```

    ```
    #Write your function here
    def reversed_list(lst1, lst2):
      for index in range(len(lst1)):
        if lst1[index] != lst2[len(lst2) - 1 - index]:
          return False
      return True
    #Uncomment the lines below when your function is done
    print(reversed_list([1, 2, 3], [3, 2, 1]))
    print(reversed_list([1, 5, 3], [3, 2, 1]))
    ```
