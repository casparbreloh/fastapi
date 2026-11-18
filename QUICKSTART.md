# FastAPI quickstart

This standalone example shows how to run a small FastAPI app locally and try a path parameter in the interactive docs.

Install FastAPI in a Python virtual environment:

```sh
python -m pip install "fastapi[standard]"
```

Save the following as `main.py` in your example directory:

```python
from fastapi import FastAPI

app = FastAPI()


@app.get("/hello/{name}")
def hello(name: str) -> dict[str, str]:
    return {"message": f"Hello, {name}!"}
```

Start the development server from the same directory:

```sh
fastapi dev main.py
```

Open <http://127.0.0.1:8000/hello/world> to see `{"message":"Hello, world!"}`. To try a different name in the browser, open <http://127.0.0.1:8000/docs>, expand `GET /hello/{name}`, and select **Try it out**.
