
# 🔴 What is Anomaly Detection?

**Anomaly Detection means finding something that is unusual or different from the normal pattern.**

Very simple:

> **Normal = things that usually happen**  
> **Anomaly = something unusual that doesn't look normal**

### Example

Suppose your bank transactions are normally:

```
₹500
₹800
₹1,200
₹700
₹1,000
```

Suddenly:

```
₹5,00,000
```

That transaction is very unusual.

👉 **Anomaly Detection can flag it.**

---

# 🎯 Why do we use Anomaly Detection?

The main purpose is:

> **To find unusual data points that may indicate a problem, fraud, error, attack, or abnormal behavior.**

It can help answer:

> **"Which data point doesn't look normal?"**

---

# 🏦 Example 1 — Bank Fraud

Imagine a person's normal transactions:

```
₹500
₹1,000
₹2,000
₹800
₹1,500
```

Then suddenly:

```
₹4,00,000
```

The system can say:

```
⚠️ UNUSUAL TRANSACTION
```

It doesn't automatically mean fraud.

It means:

> **"This is significantly different from the person's normal pattern. Check it."**

---

# 🖥️ Example 2 — Website / Server

Suppose your server normally receives:

```
100 requests/minute
120 requests/minute
150 requests/minute
110 requests/minute
```

Suddenly:

```
50,000 requests/minute
```

🚨 That's abnormal.

It could indicate:

- DDoS attack
- unusual traffic
- system problem

Anomaly detection can identify this unusual behavior.

---

# 🏭 Example 3 — Machine Failure

Imagine a factory machine normally operates at:

```
Temperature = 60°C
```

Suddenly:

```
Temperature = 110°C
```

That's abnormal.

Anomaly detection can alert:

> ⚠️ Possible machine failure.

This allows engineers to investigate before the machine breaks.

---

# 🛒 Example 4 — Customer behavior

Suppose a customer normally:

```
Visits website → 2 times/day
Purchases → ₹1,000/month
```

Suddenly:

```
500 login attempts
50 purchases in 2 minutes
```

That's unusual behavior.

It could indicate a compromised account or bot activity.

---

# 🧠 How does Anomaly Detection find something unusual?

This is the important part.

The algorithm first tries to understand:

> **"What does normal data look like?"**

Then it looks for points that are **far away from the normal pattern**.

Imagine:

```
Normal data:

       ● ● ●
     ● ● ● ●
       ● ● ●

                          ❌
                       Anomaly
```

The majority of points are together.

One point is far away.

👉 That point is suspicious/anomalous.

---

# 🔵 How does ML find anomalies?

There are different methods.

### 1. Isolation Forest ⭐

Very important for your ML foundation.

It tries to **isolate unusual points**.

Simple idea:

> Normal points are usually packed together.  
> Anomalies are easier to separate.

Example:

```
● ● ● ● ●
● ● ● ●
● ● ●

                    ❌
```

The isolated point can be detected quickly.

---

### 2. DBSCAN

You just learned this.

DBSCAN looks for **dense areas**.

```
● ● ●
● ● ●
 ● ●

                ❌
```

Dense area → cluster

Isolated point → noise

So DBSCAN can also help identify anomalies.

---

### 3. Autoencoder

This is more important later when you learn Deep Learning.

The model learns to reconstruct **normal data**.

If it reconstructs something badly:

```
Normal → reconstruction error small ✅
Anomaly → reconstruction error large ❌
```

Then it can flag the data as an anomaly.

---

# 🟣 How do we actually find an anomaly?

Imagine you have transaction amounts:

```
500
700
800
1000
1200
900
1100
500000
```

Most values are around:

```
500–1200
```

But:

```
500000
```

is extremely different.

An algorithm calculates some kind of **anomaly score**.

For example:

```
Transaction   Anomaly Score
₹500           0.02
₹700           0.03
₹1,000         0.01
₹1,200         0.04
₹5,00,000      0.98  ← suspicious
```

Higher score → more anomalous.

The exact meaning of the score depends on the algorithm.

---

# 📍 Where do we use Anomaly Detection?

Very commonly in:

|Area|What we detect|
|---|---|
|🏦 Banking|Fraudulent transactions|
|🛡️ Cybersecurity|Unusual network activity|
|🏭 Manufacturing|Machine failures|
|🖥️ IT systems|Server/system problems|
|🛒 E-commerce|Unusual customer behavior|
|🚗 Vehicles|Abnormal sensor behavior|
|📊 Business|Unusual sales patterns|
|🏥 Healthcare|Unusual measurements|

---

# 🔥 Normal ML vs Anomaly Detection

Suppose you have bank transactions.

### Supervised Learning

You have labels:

```
₹500 → Normal
₹1000 → Normal
₹500000 → Fraud
```

The model learns:

> "Given this transaction, is it fraud?"

That's **classification**.

---

### Anomaly Detection

You may **not have fraud labels**.

You mostly have normal transactions:

```
₹500
₹700
₹1000
₹1200
...
```

The algorithm learns the normal pattern and finds unusual transactions.

```
Normal pattern
      ↓
Learn
      ↓
Find unusual points
      ↓
Anomaly
```

---

# 🧠 Very easy difference

### Classification

> **"Which category does this belong to?"**

### Anomaly Detection

> **"Does this look unusual?"**

---

# ⭐ Important: Anomaly doesn't always mean bad

This is very important.

Anomaly means:

> **Unusual**

It does **not automatically mean:

> "This is fraud."**

For example, you normally spend ₹1,000.

One day you spend ₹50,000 because you bought a laptop.

That's unusual, but it's not fraud.

So anomaly detection usually means:

```
Unusual
   ↓
Flag it
   ↓
Investigate
```

---

# 🎯 For your AI Engineer roadmap

You mainly need to understand:

### ⭐ Must know

- What is anomaly detection?
- Why do we use it?
- Normal vs anomaly
- Outlier vs anomaly
- Isolation Forest
- DBSCAN can identify noise
- Basic idea of Autoencoder for anomaly detection

You **do not need deep mathematical details** right now.

---

# 🎤 Interview answer

If they ask:

**"What is Anomaly Detection?"**

Say:

> **"Anomaly detection is a technique used to identify data points or patterns that significantly differ from normal behavior. It is commonly used for fraud detection, cybersecurity, machine monitoring, and unusual behavior detection."**

### 🧠 One-line memory:

> **Anomaly Detection = Learn what is normal → find what looks unusual.**