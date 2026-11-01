
## 1. What are Path Parameters?

Path parameters are values that we pass directly inside a URL to identify a particular resource.

Imagine you are building an AI chatbot application. Each chatbot has a unique ID.

For example, imagine you have a website containing 100 posts.

You want to open post number 5.

You visit:

```
http://127.0.0.1:8000/posts/5
```

Here:

- `/posts` = Route
    
- `5` = Path parameter
    

Another example:

```
/posts/1
/posts/2
/posts/3
/posts/10
```

The number changes depending on which post you want.

![[Pasted image 20261027185834.png]]

## 2. How to create a path parameter

Let's write your first example.

```python

#put how many json is there is not there error will cause

@app.get("/api/posts/{post_id}")

def get_posts(post_id: int):

for post in posts:

if post.get ("id") == post_id:

return post

# error cause details = "post not found"

raise HTTPException(status_code=status.HTTP_404_NOT_FOUND, detail= "post not found")
```

![[Pasted image 20261027190021.png]]

### Understand each line

| Code              | Meaning                                          |
| ----------------- | ------------------------------------------------ |
| `app = FastAPI()` | Creates your FastAPI application.                |
| `@app.get(...)`   | Defines a GET endpoint.                          |
| `{product_id}`    | A variable part of the URL.                      |
| `product_id: int` | Tells FastAPI that the value must be an integer. |
| `return`          | Sends a response to the user.                    |
![[Pasted image 20261027190309.png]]

**THIS ONE MINE**

![[Pasted image 20261027190359.png]]

![[Pasted image 20261027190450.png]]
![[Pasted image 20261027190522.png]]

```PYTHON
# put how many json is.. there is not there error will cause

  

@app.get("/posts/{post_id}",include_in_schema= False)

def get_posts(request:Request,post_id: int):

for post in posts:

if post.get ("id") == post_id:

title = post["title"][:50]

return templates.TemplateResponse(

request,

"post.html",

{"posts":post, "title": title},

)

# error cause details = "post not found"

raise HTTPException(status_code=status.HTTP_404_NOT_FOUND, detail= "post not found")

# Starlette is a lightweight Python web framework.

# FastAPI uses Starlette's features for handling HTTP requests, responses, and exceptions.

  

@app.exception_handler(StarletteHTTPException)

def general_http_exception_handler(request:Request,exception:StarletteHTTPException):

message = (

exception.detail

if exception.detail

else "An error occurred. Please check your request and try again."

)

  

if request.url.path.startswith("/api"): # URL START WITH API...LIKE THIS (/api/posts/10)

return JSONResponse(

status_code=exception.status_code,

content={"detail":message},

)

return templates.TemplateResponse(

request,

"error.html",

{

"status_code": exception.status_code, # 404

"title": exception.status_code, # 404

"message":message, # post not found

  

},

status_code=exception.status_code

)
```

**OUTPUT** :

![[Pasted image 20261031193120.png]]