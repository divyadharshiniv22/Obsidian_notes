## . What is FastAPI?

FastAPI is a Python framework used to build APIs.

Let's understand this with a simple example.

Imagine you build an AI model that predicts whether an email is spam or not spam.

Your Python model can make predictions, but how can another application, a website, or a mobile app use your model?

You can use FastAPI to connect your model to those applications.


![[Pasted image 20261021065551.png]]

```python
  

from fastapi import FastAPI

  

app = FastAPI()

  

@app.get("/") 

def home():

return {"message": "Hello World!"}
```

see : http://localhost:8000/docs
![[Pasted image 20261021081428.png]]

http://localhost:8000/redoc

![[Pasted image 20261021081414.png]]

```python

from fastapi import FastAPI


app = FastAPI()

@app.get("/") # you can see in local host:8000

def home():

return {"message": "Hello World!"} # localhost return the msg like this

posts: list[dict] = [

{   # json file

"id":1,

"author":"Divya Dharshini",

"title":"Fastapi is awesome",

"content":"This framework is really easy to use and superfast",

"datepost":"feb 22 ,2003",

},

{

"id":2,

"author": "Gautam Kumar",

"title": "python is great for web development",

"content":"python is a great language for web development , and Fastapi makes it even.",

"datepost":"sep 03,1994",

},

]

@app.get("/",response_class = HTMLResponse,include_in_schema=True)# responseclass means true means present in local host 

@app.get("/posts",response_class = HTMLResponse,include_in_schema=False) #not in local host

def get_posts():

return f"<h1>{posts[0]['title']}</h1>" # 


  

@app.get("/api/posts") # now you can see in localhost:8000/api/posts

def get_posts():

return posts   # it will return the json file

  

```
