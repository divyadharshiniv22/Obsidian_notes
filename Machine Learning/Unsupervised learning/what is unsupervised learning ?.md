# 🧠 What is Unsupervised Learning?

**Unsupervised learning is a type of Machine Learning where we give the model data without the correct answers (labels), and the model tries to discover patterns, structures, or groups in that data.**

### Simple formula

> **Unlabeled Data → ML Algorithm → Hidden Patterns / Groups**

# 1. What does "unlabeled data" mean?

This is the most important concept.

Suppose we have:

|Customer|Age|Monthly Spending|Purchases|
|---|---|---|---|
|A|22|₹2,000|3|
|B|25|₹2,500|4|
|C|45|₹30,000|20|
|D|42|₹28,000|18|
|E|30|₹10,000|10|

There is **no target column** saying:

|Customer|Type|
|---|---|
|A|Low-value|
|B|Low-value|
|C|High-value|

The model has to discover the structure itself.

That's why it is called **unsupervised**.

# 2. Best example: Customer Segmentation

Imagine an e-commerce company has **100,000 customers**.

They know:

- Age
- Income
- Amount spent
- Number of purchases
- Frequency of purchases

But they don't know what type of customer each person is.

They can use **K-Means clustering**.

The algorithm might discover:

### Cluster 1

Customers who:

- Spend ₹30,000+ per month
- Buy frequently
- Have many orders

The business might call them:

> **High-value customers**

### Cluster 2

Customers who:

- Spend ₹10,000–₹20,000
- Buy occasionally

Business might call them:

> **Medium-value customers**

### Cluster 3

Customers who:

- Spend very little
- Buy rarely

Business might call them:

> **Low-value customers**

Notice something important:

**The algorithm didn't know these names.**

It only found groups based on similarities.

Humans look at the resulting groups and give them meaningful names.


## ⭐ One interview-ready definition

If an interviewer asks:

**"What is unsupervised learning?"**

Say:

> **"Unsupervised learning is a type of machine learning where the model learns from unlabeled data and identifies hidden patterns, structures, or groups without a predefined target variable. For example, an e-commerce company can use K-Means clustering to group customers based on their purchasing behavior and spending, without previously labeling the customers into different categories."**