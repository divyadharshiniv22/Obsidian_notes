uv run fastapi dev main.py  -  page will come like this![[Pasted image 20261022182849.png]]
![[Pasted image 20261022183031.png]]


**NEXT** **IMPORT JINJA2**

![[Pasted image 20261022183900.png]]

```python
# This line is used in FastAPI to display HTML pages using Jinja2 templates.

templates = Jinja2Templates(directory="templates")

#- FastAPI = the waiter who receives a request.

# Jinja2 = the person who prepares the webpage.

# HTML template = the webpage design.

# templates folder = the place where your HTML files are stored.

posts: list[dict] = [

{

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

  

@app.get("/") #handles an HTTP GET request. / - represents your application's root URL.

def home(request: Request):

return templates.TemplateResponse(

request=request,

name="home.html",

context={"posts": posts, "title": "Home"},

)

  

@app.get("/api/posts")

def get_posts():

return posts
```

**template folder - la home.html** 

output

DOCTYPE html - html format la write panrom


```python
## Home template

<!DOCTYPE html>

<html>

<head>

refresh see in localhost:8000 
<title>FastAPI Blog - Home</title> # see your tab page name it will change 

</head>

<body>

<h1>Home Page</h1>

  

{% for post in posts %}

	<h2>{{ post.title }}</h2> # post la title nu panrom(json)

<p>{{ post.content }}</p> # post  la content varom (json)

{% endfor %}

  

</body>

</html>


refresh see in localhost:8000 

```

**OUTPUT**:
![[Pasted image 20261024113809.png]]      

**VIEW PAGE SOURCE** :

![[Pasted image 20261024114013.png]] 
**LAYOUT.HTML**

![[Pasted image 20261024115256.png]]

**NOW HOME.HTML**

![[Pasted image 20261024115334.png]]

**LAYOUT_FINISHED .HTML**
```PYTHON
<!DOCTYPE html> #html format la writing
<html lang = "en"> # html la english laguage writing
     <head>
          <meta charset = "utf-8">
	          <meta name="viewport" content="width=device-width,initial-scale=1">
```