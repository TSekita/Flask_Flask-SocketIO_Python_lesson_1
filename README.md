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

#### Q3. flask run コマンドでサーバーを起動するには何が必要か。

A. Flask_APP環境変数でFlaskアプリを指定し、Flaskがインストールされていること。

#### Q4. Flaskの@app.route()デコレータの役割を説明せよ。

A. Flaskで「URLパス」と「処理関数」を結びつけるための仕組みです。

#### Q5. Flaskのデフォルトポート番号は何番か。

A. Flaskのデフォルトポート番号は5000番。

#### Q6. debug=Trueにすると何が起きるか。

A. debug=Trueにすると、Flaskがデバッグモードで動作する。

    具体的には次の３つの効果がある。

    １．コードの自動ロード

        Pythonファイルを変更すると、Flaskサーバーが自動的に再起動する。

    ２．デバッグコンソールの有効化

        エラーが発生した際に、ブラウザ上でインタラクティブな

        Pythonシェル(Werkzeug debugger)が開く。

    ３．詳細なトレースバック出力

        エラー内容とスタックとレースがターミナルに詳細表示される。

#### Q7. Flaskアプリを0.0.0.0で起動すると何が変わるか。

A. Flaskアプリを0.0.0.0で起動すると、ローカルホスト以外

    （同一LAN上のほかの端末など）からもアクセスできるようになる。

#### Q8. HTMLを返すエンドポイントを作る方法を示せ。

A. Flaskでは、render_template()関数を使ってHTMLファイルを返す。

```python
from flask import Flask, render_template

app = Flask(__name__)

@app.route('/')
def index():
    return render_template('index.html')  # templates/index.html を返す

if __name__ == '__main__':
    app.run()

```
<pre>
project/
├── app.py
└── templates/
    └── index.html
</pre>
