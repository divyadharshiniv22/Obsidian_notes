Real-world datasets are highly influenced by negative factors such as the presence of noise, missing values, redundancy, outliers, and inconsistencies. 

A low-quality dataset will leads to poor performance or failure of machine learning or deep learning project.


story:

Now a day’s, a large number of Machine Learning, Deep Learning, and transfer learning algorithms were designed. But the success or failure of these models largely depends on the quality of the data set used and the features selected.

Hence, Data Preprocessing also known as Feature Engineering & Feature Selection plays a very important stage in building a useable machine learning or deep learning project.



**There are mainly two steps in data preprocessing:**

1. Data Preparation
2. Data Reduction
![[Pasted image 20260821075342.png]]


### 1. 🧹 Data Cleaning

**Simple meaning:** Fix or remove incorrect, duplicate, or unnecessary data.

**Example:**

Age: 25

Age: -5     ❌

Age: 30

`-5` is incorrect, so we fix or remove it.

👉 **Cleaning = Fix bad data**

---

### 2. 🔄 Data Transformation

**Simple meaning:** Change data into a format that is easier for the model to use.

**Example:**

Salary: ₹50,000

We might convert it to:

Salary: 50000

Or convert:

Male → 0

Female → 1

👉 **Transformation = Change the format of data**

---

### 3. 🔗 Data Integration

**Simple meaning:** Combine data from different sources into one dataset.

**Example:**

**Customer database:**

Customer ID | Name

101         | Ravi

**Purchase database:**

Customer ID | Purchase

101         | ₹5,000

Combine them:

Customer ID | Name | Purchase

101         | Ravi | ₹5,000

👉 **Integration = Combine data**

---

### 4. 📏 Data Normalization

**Simple meaning:** Put numerical values into a similar scale/range.

Suppose we have:

Age       = 25

Salary    = 50,000

Experience = 3

Salary is much larger than the other values. A machine learning algorithm may be affected by this difference.

So we can scale them to something like:

Age        → 0.25

Salary     → 0.50

Experience → 0.30

👉 **Normalization = Put numbers on a similar scale**

**Important:** Normalization is usually a type of **feature scaling**, not simply making units the same.

---

### 5. 🩹 Missing Data Imputation

**Simple meaning:** Fill in missing values.

Example:

Name | Age

Ravi | 25

John | ?

Anu  | 30

We can replace `?` with the average age:

Name | Age

Ravi | 25

John | 27.5

Anu  | 30

👉 **Imputation = Fill missing values**

Common methods:

- Mean
- Median
- Mode
- Forward fill / backward fill
- ML-based imputation

---

### 6. 🔊 Noise Identification

**Simple meaning:** Find data values that are unusual because of errors or random variation.

Example:

Student marks:

78

82

75

80

999  ❌

79

`999` is probably an error.

Another example:

Temperature:

30°C

31°C

29°C

30°C

500°C ❌

`500°C` is suspicious and needs investigation.

👉 **Noise identification = Find suspicious/random/error data**


### 1. 🎯 Feature Selection

**Simple meaning:** Choose only the **important columns** and remove unnecessary columns.

Example:

Age | Salary | City | Height | Customer_ID | Churn

Suppose `Height` and `Customer_ID` are not useful for predicting Churn.

We keep:

Age | Salary | City | Churn

👉 **Feature Selection = Keep useful columns, remove useless columns.**

**Why?**

- Less data to process
- Faster training
- Can reduce overfitting
- Makes the model simpler

---

### 2. 👥 Instance Selection

**Simple meaning:** Choose only **some rows** from the dataset instead of using every row.

Suppose you have **1 million customer records**.

Customer 1

Customer 2

Customer 3

...

Customer 1,000,000

You might select 100,000 representative records for training.

👉 **Instance Selection = Choose useful rows from the dataset.**

**Remember:**

- **Feature selection → columns**
- **Instance selection → rows**

---

### 3. 📊 Discretization

**Simple meaning:** Convert continuous numerical values into **categories/ranges**.

Suppose you have:

Age

18

23

35

47

62

75

Instead of using exact ages, create groups:

18–25  → Young

26–40  → Adult

41–60  → Middle-aged

61+    → Senior

So:

23 → Young

35 → Adult

47 → Middle-aged

75 → Senior

👉 **Discretization = Convert numbers into categories/ranges.**

---

### 4. 🔧 Feature Extraction

**Simple meaning:** Create **new useful features from existing data**.

Example:

You have:

Date of Birth

Instead of directly using the date, calculate:

Age

Another example:

Height = 170 cm

Weight = 70 kg

Create a new feature:

BMI = Weight / Height²

So you're creating a **new representation** from existing data.

👉 **Feature Extraction = Create useful new features from existing data.**

---

### 5. 🧩 Instance Generation

**Simple meaning:** Create **new data examples/instances** from existing data.

For example, in image ML:

Original image:

🚗 Car image

You might create slightly modified versions:

Original image

Rotated image

Flipped image

Cropped image

Brightness-changed image

These become additional training examples.

👉 **Instance Generation = Create new rows/examples from existing data.**

This is commonly related to **data augmentation**.