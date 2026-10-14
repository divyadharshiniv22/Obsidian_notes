# K-Means Clustering

**K-Means is an unsupervised machine learning algorithm used to divide data into `K` groups (clusters) based on similarity.**

### Simple example — Customer Segmentation

Suppose an e-commerce company has:

- Customer age
- Amount spent
- Number of purchases

But there is **no label** saying "premium customer" or "low-value customer."

We choose:

```
K = 3
```

K-Means might discover:

```
        Customer Data
              ↓
           K-Means
              ↓
     ┌────────┼────────┐
     ↓        ↓        ↓
 Cluster 1  Cluster 2  Cluster 3
     ↓        ↓        ↓
   Low      Medium     High
  spending  spending  spending
```

The algorithm **discovers the groups itself**.

---

## How K-Means works

There are **5 main steps**:

### 1. Choose K

Decide how many clusters you want.

```
K = 3
```

means we want **3 clusters**.

### 2. Initialize centroids

Choose 3 initial **centroids**.

A centroid is basically the **center point of a cluster**.

```
        ● ●
       ● X       ← Centroid 1

                    ● ●
                   X ●     ← Centroid 2

  ● ●
   X ●                     ← Centroid 3
```

### 3. Assign data points

Each data point is assigned to the **nearest centroid**.

```
Data point → nearest centroid → cluster
```

Usually, K-Means uses **Euclidean distance** to determine which centroid is closest.

### 4. Recalculate centroids

After assigning the points, calculate the new center of each cluster.

```
Old centroid
     ↓
Average position of points
     ↓
New centroid
```

### 5. Repeat

The algorithm repeatedly:

```
Assign points
      ↓
Recalculate centroids
      ↓
Assign points again
      ↓
Recalculate centroids
      ↓
      ...
```

It stops when the clusters/centroids **no longer change significantly**.

This is called **convergence**.

---

# Important terms

|Term|Meaning|
|---|---|
|**K**|Number of clusters|
|**Cluster**|Group of similar data points|
|**Centroid**|Center of a cluster|
|**Distance**|How far a point is from a centroid|
|**Convergence**|When the clusters become stable|
|**K-Means++**|Smarter method for choosing initial centroids|

---

## Where is K-Means used?

**1. Customer segmentation**

Group customers based on behavior.

**2. Image compression**

Group similar pixel colors.

**3. Document clustering**

Group similar documents.

**4. Anomaly detection**

Identify points that don't fit well with the clusters.

---

## ⭐ Interview answer

If they ask **"What is K-Means?"**, you can say:

> **"K-Means is an unsupervised machine learning algorithm used for clustering. It divides data into K clusters by assigning each data point to the nearest centroid and repeatedly recalculating the centroids until the clusters converge."**

For your **AI Engineer preparation**, this level of K-Means understanding is good. You should next learn **PCA**, then **DBSCAN and basic anomaly detection**, before moving to deep learning.

# 1. First: Why do we use K-Means?

Suppose an online shopping company has **10,000 customers**.

They have data like:

|Customer|Annual Income|Spending|
|---|---|---|
|A|₹2L|₹10K|
|B|₹2.5L|₹12K|
|C|₹15L|₹1L|
|D|₹18L|₹1.2L|
|E|₹8L|₹50K|

The company wants to know:

> **"What different types of customers do we have?"**

But they don't have labels.

They don't know beforehand:

```
Customer A → Low-value
Customer B → Low-value
Customer C → Premium
...
```

This is an **unsupervised learning problem**.

So we can use **K-Means**.

---

# 2. What does K-Means actually do?

K-Means tries to **group similar data points together**.

Imagine putting the customers on a graph:

```
Spending
   ↑
   |
   |                         ● ● ●
   |                        ● ● ●
   |
   |              ● ●
   |             ● ●
   |
   |   ● ●
   |  ● ●
   +--------------------------------→ Income
```

We can see that there seem to be different groups.

K-Means tries to automatically discover those groups.

For example:

```
Cluster 1 → Low spending customers

Cluster 2 → Medium spending customers

Cluster 3 → High spending customers
```

### So why use K-Means?

Because:

> **We have unlabeled data and want to discover natural groups within it.**

---

# 3. What does the "K" mean?

**K = number of clusters.**

Suppose we want 3 groups:

```
K = 3
```

Then K-Means tries to create:

```
Cluster 1
Cluster 2
Cluster 3
```

If:

```
K = 5
```

we get 5 clusters.

---

# 4. What is a centroid?

This is the most important K-Means concept.

A **centroid is the center of a cluster**.

Imagine:

```
        ● ●
      ● ● ●
       ● X
      ● ●
```

`X` is approximately the **center**.

That is the centroid.

K-Means basically asks:

> "Which data points are closest to this center?"

and groups them together.

---

# 5. How does K-Means work?

Let's say:

```
K = 3
```

### Step 1 — Choose 3 initial centroids

The algorithm needs 3 starting centers.

```
        X₁


                   X₂


    X₃
```

### Step 2 — Assign points to the nearest centroid

Each customer is assigned to the closest centroid.

```
Customer → nearest centroid → cluster
```

### Step 3 — Recalculate the centroid

Once customers are grouped, K-Means calculates a new center for each group.

### Step 4 — Repeat

```
Assign points
      ↓
Calculate new centers
      ↓
Assign points again
      ↓
Calculate new centers
      ↓
Repeat
```

Eventually the groups become stable.

---

# 6. Now comes the problem with K-Means

This is where **K-Means++** becomes important.

The question is:

> **Where should we initially place the centroids?**

Suppose we have:

```
        ● ● ●
        ● ● ●


                    ● ● ●
                    ● ● ●


   ● ● ●
   ● ● ●
```

We want:

```
K = 3
```

Ideally, the starting centroids should be:

```
        X₁ ● ● ●


                    X₂ ● ● ●


   X₃ ● ● ●
```

One centroid near each group.

But if we randomly initialize them, we might get:

```
        X₁ ● ● ●
        X₂ ● ● ●


                    ● ● ●
                    ● ● ●


   X₃ ● ● ●
```

Notice:

**X₁ and X₂ are very close together.**

There is no initial centroid near the right-side group.

This is a **bad initialization**.

It can cause K-Means to:

- take more iterations,
- produce a poorer clustering,
- converge to a less useful solution.