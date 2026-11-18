# FastAPI quickstart

Install with `python -m pip install "fastapi[standard]"`. Save as `main.py`:

```python
from fastapi import FastAPI

app = FastAPI()


@app.get("/hello/{name}")
def hello(name: str):
    return {"message": f"Hello, {name}!"}
```

Run `fastapi dev main.py` and try the endpoint at <http://127.0.0.1:8000/docs>.
