### What is `localhost`?

`localhost` is a special hostname that always refers to **your own computer**.

For example:

```
localhost:8000
```

means:

- **localhost** → your computer
- **8000** → the port number where your application is listening

So when you open:

```
http://localhost:8000
```

your browser is talking to the FastAPI server running **on your own machine**.

---

## What is Port 8000?

Think of your computer as a building.

- The **IP address** is the building's address.
- A **port** is like a room number.

Example:

```
Computer
 ├── Port 80   → Website
 ├── Port 443  → HTTPS Website
 ├── Port 3306 → MySQL
 ├── Port 5432 → PostgreSQL
 └── Port 8000 → FastAPI
```

Your FastAPI app is running in "room" 8000.

---

## Can other systems access `localhost:8000`?

**No.**

`localhost` is only accessible from the same computer where the server is running.

Example:

Your laptop:

```
localhost:8000
```

works.

Your friend's laptop:

```
localhost:8000
```

tries to connect to **their own** computer, not yours.

---

### Summary

| Address                                         | Who can access it?                                |
| ----------------------------------------------- | ------------------------------------------------- |
| `http://localhost:8000`                         | Only your computer                                |
| `http://127.0.0.1:8000`                         | Only your computer                                |
| `http://192.168.x.x:8000`                       | Other devices on the same network (if configured) |
| Public server (e.g., `https://api.example.com`) | Anyone on the internet (if exposed)               |