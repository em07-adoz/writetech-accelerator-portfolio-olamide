---
id: getting-started
title: Getting Started
---

# 🚀 Getting Started with FastAPI

**FastAPI** is a modern Python web framework for building APIs quickly, with automatic docs and high performance.  

## Installation
```bash
pip install fastapi uvicorn
```
## Create a simple app (main.py)
```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def read_root():
    return {"message": "Hello, FastAPI!"}
```
## Run the app
```bash
uvicorn main:app --reload
```

## Access the app:
[Open in browser:](http://127.0.0.1:8000)

## API Documentation:
- [Swagger UI:](http://127.0.0.1:8000/docs)
- [ReDoc:](http://127.0.0.1:8000/redoc)
