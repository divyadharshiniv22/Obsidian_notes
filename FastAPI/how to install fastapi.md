## Step 1: Generate `pyproject.toml`

Run this command:

```
uv init
```
It will generate automatically 
 * gitignore
 * python-version
 * pyproject.toml
 * README.md
 * uv.lock

### Step 2: Install FastAPI

Open the terminal and run:

```
uv add "fastapi[standard]"
```
install fastapi

### Step 4: Run your application

```
uv run fastapi dev main.py
```