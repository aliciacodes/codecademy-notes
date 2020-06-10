# Len's Slice

You work at Len’s Slice, a new pizza joint in the neighborhood. You are going to use your knowledge of Python lists to organize some of your sales data.



**Make Some Pizzas**

1. To keep track of the kinds of pizzas you sell, create a list called `toppings` that holds the following:
   - `pepperoni`
   - `pineapple`
   - `cheese`
   - `sausage`
   - `olives`
   - `anchovies`
   - `mushrooms`

```
toppings = ['pepperoni', 'pineapple', 'cheese', 'sausage', 'olives', 'anchovies', 'mushrooms']
```

2. To keep track of how much each kind of pizza slice costs, create a list called `prices` that holds:
   - `2`
   - `6`
   - `1`
   - `3`
   - `2`
   - `7`
   - `2`

```
prices = [2, 6, 1, 3, 2, 7, 2]
```

3. Find the length of the `toppings` list and store it in a variable called `num_pizzas`.

```
num_pizzas = len(toppings)
```

4. Print the string `"We sell X different kinds of pizza!"`, with `num_pizzas` where the `X` is.

```
print("We sell "+ str(num_pizzas) + " different kinds of pizza!")
```

5. Use `zip` to combine the two lists into a list called `pizzas` that has the structure:

```
[(price_0, topping_0), (price_1, topping_1), (price_2, topping_2), ...]
```

In order to make the result of `zip` a list, do the following:

```
pizzas = list(zip(prices, toppings))
```

6. Print `pizzas`.

   Does it look the way you expect?

```
print(pizzas)
```

**Sorting and Slicing Pizzas**

7.  Sort `pizzas` so that the pizzas with the lowest prices are at the start of the list.

```
pizzas.sort()
```

8. Store the first element of `pizzas` in a variable called `cheapest_pizza`.

```
cheapest_pizza = pizzas[0]
```

9. A man in a business suit walks in and shouts “I will have your MOST EXPENSIVE pizza!”

   Get the last item of the `pizzas` list and store it in a variable called `priciest_pizza`.

```
priciest_pizza = pizzas[-1]
```

10. Three mice walk into the store. They don’t have much money (they’re mice), but they do each want different pizzas.

    Slice the `pizzas` list and store the 3 lowest cost pizzas in a list called `three_cheapest`.

```
three_cheapest = pizzas[:3]
```

11. Print the `three_cheapest` list.

```
print(three_cheapest)
```

12. Your boss wants you to do some research on $2 slices.

    Count the number of occurrences of `2` in the `prices` list, and store the result in a variable called `num_two_dollar_slices`. Print it out.

```
num_two_dollar_slices = prices.count(2)
print(num_two_dollar_slices)
```