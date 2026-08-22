**A Pydantic model is like a form/template that tells FastAPI what data is allowed, checks that data, and helps keep API responses in the correct format.**

**Pydantic validation** means **checking whether the data coming into your Python/FastAPI application is in the correct format and follows the rules you defined.**

story: real time example

THINK OF IT LIKE…

A model is like a paper form with printed fields

A government form tells you exactly what to fill in — name, date of birth, amount — and rejects the submission if a field is missing or in the wrong format.

Pydantic models work the same way: you declare the fields once, and every piece of incoming data must pass through that form before your code ever sees it.

![[Pasted image 20260821195136.png]]
## What is a Pydantic Model?

A **Pydantic model** is a Python class that tells your application **what data should look like**.

### 1. A model is a class

class User(BaseModel):

This means we create a `User` model using Pydantic's `BaseModel`.

Think of it as a **form/template** for user data.

---

### 2. Fields tell us what data we need

class User(BaseModel):

    name: str

    age: int

Here:

- `name` → must be text (`str`)
- `age` → must be a number (`int`)

So we are telling Pydantic:

> "I want a name and an age, and they must have these types."

---

### 3. FastAPI uses these rules

When someone sends data to your FastAPI application, FastAPI uses the Pydantic model to **check the data**.

For example:

{

    "name": "Divya",

    "age": 22

}

✅ This is valid.

But:

{

    "name": "Divya",

    "age": "hello"

}

❌ This is invalid because `age` should be an integer.

---

### 4. Invalid data is rejected

If someone sends incorrect data, FastAPI automatically returns a **422 validation error**.

You don't have to manually write code to check every field.

---

### 5. It also helps create the response

Pydantic can also control the data that your API **sends back**.

For example, you can say:

class UserResponse(BaseModel):

    name: str

    age: int

Then your API response follows this structure.

---

![[Pasted image 20260821200314.png]]
### The 5 points to remember

**1. Type hint** → tells FastAPI which model to use.

**2. Parse + validate** → Pydantic checks the incoming data.

**3. ValidationError** → bad data is rejected.

**4. Model instance** → your function receives a validated Pydantic object.

**5. `response_model`** → controls the structure of the response.


## What FastAPI does from Request → Response

Let's understand each point in **very simple words**.

### 1. FastAPI reads the type hints

Suppose you write:

def create_product(product: Product):

FastAPI sees:

product: Product

        ↑

   Pydantic model

It understands:

> "The incoming data should follow the `Product` model."

FastAPI also uses this information to create the **JSON Schema** used in its API documentation, such as Swagger UI.

---

### 2. FastAPI receives the JSON

The client sends:

{

    "name": "Laptop",

    "price": 50000

}

FastAPI takes this incoming data and gives it to Pydantic.

Pydantic checks the fields and their types.

For example:

class Product(BaseModel):

    name: str

    price: float

It checks:

name  → Is it text?       ✓

price → Is it a number?   ✓

---

### 3. What does "coerced" mean?

**Coerced** simply means:

> Pydantic may convert a value into the expected type when the conversion is valid.

For example, depending on the field/type and Pydantic's rules, a value such as:

"50000"

may be converted to:

50000.0

But if the value cannot be converted appropriately, validation fails.

---

### 4. What happens with bad data?

Suppose your model says:

class Product(BaseModel):

    name: str

    price: float

But the client sends:

{

    "name": "Laptop",

    "price": "hello"

}

Pydantic checks:

price should be float

        ↓

"hello" cannot be converted to float

        ↓

ValidationError

        ↓

FastAPI returns 422

You don't have to manually write all these checks.

---

### 5. Your function gets validated data

If validation succeeds:

def create_product(product: Product):

your function receives a **Product object**, not just raw JSON.

For example:

product

 ├── name = "Laptop"

 └── price = 50000.0

So inside your function you can do:

product.name

product.price

This is one of the main benefits of using Pydantic.

---

### 6. What does `response_model` do?

Suppose you have:

@app.post("/products", response_model=Product)

def create_product(product: Product):

    return product

Here:

response_model=Product

means:

> "The data I send back to the client should follow the `Product` model."