**Types of**  **Regression Model****:

* Regression modeling is a process of determining a relationship between dependent one or more independent variables and one dependent or output variable.

**example:**  

1. predicting the height of a person given the age of the person. ( height - dependent, age - independent )

2. Predicting the price of the car given the car model,year of manufacturing ,mileage,engine capacity etc...


![[Pasted image 20260820193658.png]]

**1 . simple linear regression :**


Simple Linear Regression is a supervised machine learning algorithm **used to predict a numerical value using one input feature.**

The word Simple means:

**Only ONE input feature (X) is used to predict the output (Y).**

For example:

**House size → House price**

Here:

X = house size (in technical term : x = feature /input , y =  target/ output )

Y = house price


# 2. A real example

Suppose we have historical house data:

|House Size (sq.ft)|Actual Price (₹ lakh)|
|---|---|
|500|25|
|800|40|
|1000|50|
|1200|60|
|1500|75|
|2000|100|

We want to answer:

> **If a new house is 1300 sq.ft, what could its price be?**

We don't know the actual price yet.

So we train a **Simple Linear Regression model** using the old data.


# 3. What are X and Y?

This is very important.

### X = Feature/Input

X = House Size

Example:

X = 1000 sq.ft

### Y = Target/Output

Y = House Price

Example:

Y = ₹50 lakh

So our training data looks like:

X             Y

500    →      25

800    →      40

1000   →      50

1200   →      60

1500   →      75

2000   →      100

# 4. What does the model actually do?

The model looks at all these old examples and tries to understand:

> **"As house size increases, how does house price change?"**


# 5. The formula

The Simple Linear Regression formula is:

**Y^=b0​+b1​X​**