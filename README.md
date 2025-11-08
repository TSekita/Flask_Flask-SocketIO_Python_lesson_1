#### Q1. Flaskとは何かを説明せよ。

A. Flaskとは軽量なWebアプリケーションフレームワークです。

#### Q2. Flaskアプリを最小構成で起動するコードを書け。

A.
```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def hello_world():
    return "<p>Hello, World!</p>"

```
