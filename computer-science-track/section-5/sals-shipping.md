# Sal's Shipping

Video is <a href = "https://www.youtube.com/watch?time_continue=496&v=46_cL0O6xyQ&feature=emb_title">Here</a>

Sal runs the biggest shipping company in the tri-county area, Sal’s Shippers. Sal wants to make sure that every single one of his customers has the best, and most affordable experience shipping their packages. In this project, you’ll build a program that will take the weight of a package and determine the cheapest way to ship that package using Sal’s Shippers.

Sal’s Shippers has several different options for a customer to ship their package. They have ground shipping, which is a small flat charge plus a rate based on the weight of your package. Premium ground shipping, which is a much higher flat charge, but you aren’t charged for weight. They recently also implemented drone shipping, which has no flat charge, but the rate based on weight is triple the rate of ground shipping.

Here are the prices:

**Ground Shipping**

| Weight of Package                         | Price per Pound | Flat Charge |
| ----------------------------------------- | --------------- | ----------- |
| 2 lb or less                              | $1.50           | $20.00      |
| Over 2 lb but less than or equal to 6 lb  | $3.00           | $20.00      |
| Over 6 lb but less than or equal to 10 lb | $4.00           | $20.00      |
| Over 10 lb                                | $4.75           | $20.00      |

**Drone Shipping**

| Weight of Package                         | Price per Pound | Flat Charge |
| ----------------------------------------- | --------------- | ----------- |
| 2 lb or less                              | $4.50           | $0.00       |
| Over 2 lb but less than or equal to 6 lb  | $9.00           | $0.00       |
| Over 6 lb but less than or equal to 10 lb | $12.00          | $0.00       |
| Over 10 lb                                | $14.25          | $0.00       |

**Premium Ground Shipping**

Flat charge: $125.00



## Finding the Cheapest Shipping Method

Step 1: 
First off, we need to know how much it costs to ship a package of given weight by normal ground shipping.

Write a function for the cost of ground shipping. This function should take one parameter, `weight`, and return the `cost` of shipping a package of that weight.

```
def cost_ground_shipping(weight):
  if weight < 2:
    cost = 1.50
  elif weight <= 6 and weight > 2:
    cost = 3.00
  elif weight > 6 and weight <= 10:
    cost = 4.00
  else:
    cost = 4.75
  return (cost * weight) + 20

```

Step 2: A package that weighs 8.4 pounds should cost $53.60 to ship with normal ground shipping:

```
8.4\ lb \times \$4.00 + \$20.00 = \$53.608.4 lb×$4.00+$20.00=$53.60
```

Test that your ground shipping function gets the same value.

```
print(cost_ground_shipping(8.4))
```

Step 3: We’ll also need to make sure we include the price of premium ground shipping in our code.

Create a variable for the cost of premium ground shipping.

Note: this does not need to be a function because the price of premium ground shipping does not change with the weight of the package.

```
premium_ground_shipping = 125.00
```

Step 4: Write a function for the cost of drone shipping. This function should take one parameter, `weight`, and return the `cost` of shipping a package of that weight.

```
def drone_shipping(weight):
  if weight < 2:
    price = 4.50
  elif weight > 2 and weight <= 6:
    price = 9.00
  elif weight > 6 and weight <= 10:
    price = 12.00
  else:
    price = 14.25
  return price * weight
```



Step 5: A package that weighs 1.5 pounds should cost $6.75 to ship by drone:

```
1.5\ lb \times \$4.50 + \$0.00 = \$6.751.5 lb×$4.50+$0.00=$6.75
```

Test that your drone shipping function gets the same value.

```
drone_shipping(1.5)
```

Step 6: 

Using those two functions for ground shipping cost and drone shipping cost, as well as the cost of premium ground shipping, write a function that takes one parameter, `weight` and prints a statement that tells the user

- The shipping method that is cheapest.
- How much it would cost to ship a package of said weight using this method.

```
def cheapest_method(weight):
  ground = cost_ground_shipping(weight)
  pre_ground = premium_ground_shipping
  drone = drone_shipping(weight)
  if ground < pre_ground and ground < drone:
    cheapest = ground
    string = "Ground shipping"
  elif pre_ground < ground and pre_ground < drone:
    cheapest = pre_ground
    string = "Premium Ground shipping"
  elif drone < ground and drone < pre_ground:
    cheapest = drone
    string = "Drone"
  print(string + " is the cheapest method. The cost will be $"+ str(cheapest))
```



How they did it:

```
def cheapest_method(weight):
	ground = cost_shipping_ground(weight)
	premium = premium_ground_shipping
	drone = drone_shipping(weight)
	
	if ground < premium and ground < drone:
		method = "standard ground"
		cost = "ground"
	elif premium < ground and premium < drone:
		method = "premium ground"
		cost = premium
	else:
		method = "drone"
		cost = drone
		
	print(
	"The cheapest option available is $%.2f with %s shipping."
	% (cost, method)
	)
```



Step 7: Great job! Now, test your function!

What is the cheapest method of shipping a 4.8 pound package and how much would it cost?

What is the cheapest method of shipping a 41.5 pound package and how much would it cost?

(See hint for answers)

```
cheapest_method(4.8)
cheapest_method(41.5)
```
