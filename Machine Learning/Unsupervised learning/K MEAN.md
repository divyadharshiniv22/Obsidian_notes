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