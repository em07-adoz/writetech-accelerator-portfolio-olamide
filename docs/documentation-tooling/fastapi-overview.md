---
title: Overview
---

# FastAPI Overview

FastAPI is a modern, high-performance web framework for building APIs with Python, designed for **speed**, **ease of use**, and **developer productivity**.  
It leverages Python's type hints, asynchronous programming, and the **Starlette** framework to deliver scalable APIs with minimal code.

---

## Key Features

- **High Performance**: Built on Starlette and Pydantic, using async/await to achieve performance comparable to Node.js and Go (via ASGI).  
- **Automatic Documentation**: Generates interactive API docs with **Swagger UI** and **ReDoc**, derived from type hints.   
- **Dependency Injection**: Flexible system for shared logic, authentication, or database connections.  
- **Built-in Security**: Supports OAuth2, JWT, and other authentication mechanisms.  
- **Extensibility**: Works with ORMs (SQLAlchemy, Tortoise) and integrates with many Python libraries.  

---

## Benefits

- **Speed**: Among the fastest Python frameworks, often outperforming Flask and Django for APIs.  
- **Developer Productivity**: Type hints + validation reduce errors, while auto-generated docs save time.  
- **Scalability**: Async support makes it ideal for high-concurrency applications.  
- **Community & Ecosystem**: Growing adoption with plugins for GraphQL, WebSockets, and testing.  
- **Standards-Based**: Adheres to **OpenAPI** and **JSON Schema** for tool compatibility.  

---

## Use Cases

- **RESTful APIs** → Microservices or monolithic APIs for web/mobile apps.  
- **Real-Time Applications** → WebSockets for chat, notifications, or streaming.  
- **Machine Learning APIs** → Serve ML models (e.g., TensorFlow, PyTorch).  
- **Prototyping & Production** → Great for rapid prototyping and production-ready systems.  

---

## Getting Started

### Installation
```bash
pip install fastapi uvicorn
```
(uvicorn is an ASGI server.)

### Example
```python
from fastapi import FastAPI
from pydantic import BaseModel

app = FastAPI()

class Item(BaseModel):
    name: str
    price: float

@app.post("/items/")
async def create_item(item: Item):
    return {"name": item.name, "price": item.price}
```
