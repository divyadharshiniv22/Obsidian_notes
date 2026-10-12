![[Pasted image 20261006070125.png]]

### What does the ML model do?

We give the data to an **unsupervised learning algorithm**, such as **K-Means clustering**.

The algorithm looks at similarities and automatically creates groups:

**Group 1 → High-value customers**

- Spend a lot
- Purchase frequently

**Group 2 → Medium-value customers**

- Moderate spending
- Moderate purchases

**Group 3 → Low-value customers**

- Spend little
- Purchase rarely

The important point is:

> **We didn't tell the model which customers belong to which group. The model discovered the groups itself.**


### Interview answer

> **“Unsupervised learning is a type of machine learning where the model learns patterns from data without labeled outputs. For example, an e-commerce company can use K-Means clustering to group customers based on their spending and purchasing behavior. The model automatically discovers groups such as high-value, medium-value, and low-value customers without being given those labels.”**
> ![[Pasted image 20261007190106.png]]
![[Pasted image 20261007190259.png]]

k - means 1 ,2,3,4.......n . in this image we have 3 cluster.


![[Pasted image 20261007192540.png]]
### ⭐ Remember this

**Supervised:**  
`Data + Correct Answer → Learn to predict`

**Unsupervised:**  
`Data → Find hidden patterns/groups`

**Best beginner example:**  
👉 **Customer segmentation using K-Means clustering**.


# 13. The easiest way to remember

Think about **three situations**:

### 🟢 Supervised

**"I know the answer."**

```
Tumor → Malignant/Benign
```

The model learns to predict the answer.

---

### 🔵 Unsupervised

**"I don't know the groups."**

```
Customers → ? ? ?
             ↓
          Clustering
             ↓
        Group 1, 2, 3
```

The model discovers groups.

---

### 🟠 Reinforcement Learning

**"Learn through rewards and penalties."**

```
Action
  ↓
Reward / Penalty
  ↓
Learn better action
```

Example: a game-playing AI learning which moves produce higher rewards.