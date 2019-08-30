# flask-mega-tutorial

Practice for flask framework.

## 参考

The Flask Mega-Tutorial
https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-i-hello-world

## Flask run

``` bash
# windows user: make sure your bash is execused on winpty
python -m venv venv
# on windows git bash
source venv/Script/activate
# on windows powershell
# venv/Script/Activate.ps1
python -m pip install pip --upgrade
python -m pip install -r requirements.txt
python -m flask run
```

## Emulate Email Server

``` bash
python -m smtpd -n -c DebuggingServer localhost:8025
```

## .vscode/settins.json

vscodeでjinja, jinja2 Snippet Kit, Better Jinjaを入れると.htmlがHTMLとして認識されなくなる。
flake8の一部のエラーを抑制する。

``` json
{
    "files.associations": {
        "*.html": "html"
    },
    "python.pythonPath": "venv\\Scripts\\python.exe",
    "python.linting.pylintEnabled": false,
    "python.linting.flake8Enabled": true,
    "python.linting.flake8Args": [
        "--max-line-length=120",
        "--ignore=E402"
    ]
}
```
