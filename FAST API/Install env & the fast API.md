
```fastapi
first create the virutal env.
so open the vs code , run next we have ... three dots click it. open the new terimal. 
```
**install the virutal environment**
```fastapi
sudo apt update 
sudo apt install python3-venv
```
**Then create the virtual environment again:**
```fastapi
python3 -m venv tutorial-env
```

### step 2: Activate the virtual environment

**On Ubuntu:**
```fastapi
source tutorial-env/bin/activate
```
**You should then see:**
```fastapi
(tutorial-env) dharshini@gautam-desktop:~/fastapi$
```
**Check Python version**
```fastapi
python3 --version
```
**Example output:**
```fastapi
Python 3.12.3
```
**Step 3: Upgrade pip**
```fastapi
pip install --upgrade pip
```
## Step 4: Install FastAPI and Uvicorn
```fastapi
pip install fastapi uvicorn
```
**Check that they were installed:**
```fastapi
pip list
```
You should see packages like:
```fastapi
fastapi 
uvicorn 
starlette 
pydantic
```
### Create `main.py`
```fastapi
from fastapi import FastAPI 
app = FastAPI() 
@app.get("/") 
def home(): 
    return {"message": "Hello, FastAPI!"}
```
**Run the application**
```fastapi
uvicorn main:app --reload
```


You should see:
```fastapi
INFO:Uvicorn running on http://127.0.0.1:8000
```

http://localhost:8000 . go to the chrome paste it

output will come.


**Jinja2 install**

CREATE A  ENV

```PYTHON
(tutorial-env)
```
```python
pip install jinja2
```
```python
python -m pip install jinja2
```
```python
pip show jinja2
```

Output
```fastapi
Name: Jinja2 Version: 3.x.x ...
```
```fastapi
uvicorn main:app --reload
```