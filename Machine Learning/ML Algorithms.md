
Machine Learning Algorithms
│
├── Supervised Learning
│   │
│   ├── Regression
│   │   └── Linear Regression
│   │
│   └── Classification
│       ├── Logistic Regression
│       ├── Decision Tree
│       ├── Random Forest
│       ├── KNN
│       └── SVM
│
├── Unsupervised Learning
│   │
│   └── Clustering
│       └── K-Means
│
└── Deep Learning
    │
    └── Neural Networks



1.supervised learning
2.unsupervised learning
3.semi-supervised learning
4.reinforcement learning.



**Supervised

### Interview answer

If they ask **"What is supervised learning?"**, you can say:

> **"Supervised learning is a type of machine learning where we train a model using data that has inputs and known correct outputs. The model learns the relationship between them and uses that knowledge to make predictions on new data."**

type of supervised learning:
### 1. Regression 📈

Regression is used when the answer you want to predict is a **number**.

Examples:

- Predict house price → ₹50 lakh
- Predict salary → ₹6 LPA
- Predict temperature → 32°C
- Predict sales → ₹2,50,000

Example:

House size → Price

  

1000 sq.ft → ₹50 lakh

1500 sq.ft → ₹75 lakh

2000 sq.ft → ₹100 lakh

The model learns the relationship and predicts a **continuous numerical value**.

**Common algorithms:**

- Linear Regression
- Decision Tree Regression
- Random Forest Regression

---

### 2. Classification

Classification is used when the answer belongs to a **category/class**.

Examples:

- Email → Spam / Not Spam
- Customer → Churn / Not Churn
- Image → Cat / Dog
- Transaction → Fraud / Not Fraud

Example:

Customer data

      ↓

Classification model

      ↓

Churn = YES

The output is a **class/category**, rather than a continuous number.

So the structure is:

Supervised Learning

       │

       ├── Regression → Predict a number

       │

       └── Classification → Predict a category

* Supervised machine learning ,or more commonly,supervised learning ,refers to algorithms that learn x to y , or input-to-output mappings.

 * The key characteristic of supervised learning is that  you give your learning algorithm example to learn from that include the right answer.


IF THE INPUT **X** IS AN EMAIL AND THE OUTPUT **Y** IS THIS EMAIL SPAM OR NOT SPAM

![[Pasted image 20260816002817.png]]

Say you want to predict housing prices based on the size of the house.

You've collected data,and say you plot the data,and it looks like this.
Here on the Horizontal axis is the size of the house in square feet.
![[Pasted image 20260816003318.png]]
	And yes,I live in the United States where we still use square feet.I know most  of the world uses square meters.
 
	And here on the vertical axis is the price of the house in ,say,thousands of dollars.

 so with this data,let's say a friend wants to know what's the price for their 750 square foot house.


### In an interview

If they ask:

> **"What are some applications of Machine Learning?"**

You can answer simply:

> **"Machine Learning is used in many real-world applications such as recommendation systems, spam detection, fraud detection, face recognition, medical diagnosis, customer churn prediction, voice assistants, and self-driving cars. In general, whenever we have data and want to find patterns or make predictions from that data, Machine Learning can be useful."**


## 1. Supervised Learning 👨‍🏫

**Supervised = We give the computer examples along with the correct answers.**

Imagine you are teaching a child to identify cats and dogs.

You show:

🐱 → Cat

🐶 → Dog

🐱 → Cat

🐶 → Dog



**supervised Learning** **Example:**


**Classification:**


**Breast Cancer detection:**

Take breast cancer dectection as an example of a  classification problem.

Say you're building a machine learning system so that doctors can have a diagnostic tool. to dected breast cancer .

This is important because early detection cloud potenially save a patient's life.

Using a patient's medical records,your machine learning system tries to figure out if a tumor, that is , a lump is malignant,meaning cancerous or dangerous,or if  that tumor,that lump. is benign , meaning that it's just a lump that isn't cancerous and isn't that dangerous.

so maybe your dataset has tumors of various size,and these tumors are labeled as either





![[Pasted image 20260817071807.png]]![[Pasted image 20260817072734.png]]

Benign       → Non-cancerous
Malignant    → Cancerous

**My own words:** 

**Supervised learning example:**

Breast cancer

### Your understanding

You are thinking:

> Historical patient data + diagnosis information (tumor size, shape, texture, radius, etc.) → ML learns → predicts whether a new patient has cancer or not.

### During training

Suppose we have historical patients:

| Patient | Tumor size | Shape | Texture | Radius | Known diagnosis |
| ------- | ---------- | ----- | ------- | ------ | --------------- |
| A       | 10         | ...   | ...     | 12     | Benign          |
| B       | 20         | ...   | ...     | 22     | Malignant       |
| C       | 8          | ...   | ...     | 10     | Benign          |
| D       | 25         | ...   | ...     | 27     | Malignant       |
And yes, this is a **Supervised Learning → Classification** problem.

> **Supervised** because we have the correct answers for historical training data.

> **Classification** because the prediction is a category: **Benign or Malignant**.




## What is Unsupervised Learning?

**Unsupervised Learning is when we give data to a machine learning model, but we don't give it the correct answers.**

The model looks at the data and **tries to find patterns or similarities by itself**.

1. **Clustering**

**Goal:** Group similar data together (example it will see the similar names)

Example:

Patient data

     ↓

Clustering

     ↓

Group 1 → Similar patients

Group 2 → Similar patients

Group 3 → Similar patients


2. **Dimensionality Reduction**

**Goal:** Reduce the number of features while keeping important information.


### Original data

Suppose we have 4 features:

|Patient|Radius|Texture|Area|Smoothness|
|---|---|---|---|---|
|A|12|15|500|0.10|
|B|13|16|520|0.11|
|C|25|30|900|0.18|
|D|24|29|880|0.17|

Here:

Radius       → number

Texture      → number

Area         → number

Smoothness   → number

So we have **4 numerical dimensions**.

IMPORTANCE:

**100 + dimensions we don't want all the dimension ,so we reduce the dimension. give 10 dimension.**
**so it will work machine learning model working effectively.**
-------------------------------------------------------------------------------------------------------------------------------------------
**PCA stands for Principal Component Analysis.**

PCA is a technique used for **dimensionality reduction**.

In very simple words:

> **PCA takes many features and creates fewer new features called Principal Components, while trying to keep as much important information as possible.**


## Why PC1?

**PC1 = Principal Component 1**

PC1 is the direction that captures the **largest amount of variation** in the data.

For example:

PC1 → 60% of variation

PC2 → 25% of variation

PC3 → 8%

PC4 → 4%

PC5 → 3%

If we keep PC1 + PC2:

60% + 25% = 85%

So we're keeping a representation that captures about **85% of the variance** while reducing 5 dimensions to 2.


### 1. Anomaly Detection → Find unusual things

Anomaly means **something that doesn't look normal**.

Example: Banking transactions:

₹500

₹700

₹1,000

₹800

₹900

₹5,00,000  ← unusual

The model can identify:

> "This transaction is very different from the others."

**Purpose:** Find unusual/suspicious data.

Common uses:

- Fraud detection
- Network intrusion detection
- Machine failure detection
- Unusual customer behavior


**Remember:**

> 🟢 Clustering → **Who is similar?**  
> 🔵 PCA → **Can I simplify the data?**  
> 🔴 Anomaly → **What is unusual?**  
> 🟡 Association → **What goes together?**

**Easy memory:**



3. **Semi-Supervised Learning**


# 3. Very simple analogy

Imagine a teacher has **100 questions**.

The teacher gives you the answers to only **10 questions**.

10 questions → Question + Answer

90 questions → Question only

You learn from the 10 answered questions and also look for patterns in the 90 unanswered questions.

That's similar to **Semi-Supervised Learning**.


4. **Reinforcement Learning**

### Interview answer

If the interviewer asks:

> **"What is Reinforcement Learning?"**

You can say:

> **"Reinforcement Learning is a type of machine learning where an agent learns by interacting with an environment. It takes actions and receives rewards or penalties based on the results. Through repeated trial and error, the agent learns which actions lead to better outcomes."**


# 5. Example: Robot

Imagine a robot needs to reach a destination.

Initially, it doesn't know the best path.

Robot

 ↓

Moves forward

 ↓

Gets closer to destination

 ↓

+10 reward

Another time:

Robot

 ↓

Moves into a wall

 ↓

-10 reward

After many attempts, the robot learns:

> "Moving in this direction is bad."

and:

> "Moving in this direction is better."


![[Pasted image 20260819071449.png]]