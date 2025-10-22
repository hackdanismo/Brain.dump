# Flask
`Flask` is a popular and lightweight web framework for `Python`. 

+ [Setup](#setup)
+ [Create a Simple Flask App](#create-a-simple-flask-app)

## Setup
Begin by checking `Python` is installed, setting up a directory/folder for the project and a `Virtual Machine`. Once the setup is complete, install `Flask` using the `Pip` package manager.

```shell
# Check that Python and Pip are installed and what versions are installed
$ python3 --version
$ pip3 --version

$ mkdir project-name
$ cd project-name

# Setup a Virtual Environment within the project folder
$ python3 -m venv venv
# Activate the Virtual Environment (macOS)
$ source venv/bin/activate
# Activate the Virtual Environment (Windows)
$ venv\Scripts\activate

# Install Flask
$ pip3 install flask
# Check the installation
$ pip3 show flask
```

A good option is to save the dependencies that have been installed:

```shell
$ pip3 freeze > requirements.txt
```

When opening a project, run the following command to install and setup the dependencies:

```shell
$ pip3 install -r requirements.txt
```

## Create a Simple Flask App
Create a file named `app.py` in the project folder:

```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def home():
    return "Hello, Flask!"

if __name__ == "__main__":
    app.run(debug=True)
```

+ Flask(__name__) creates your web app.
+ @app.route("/") defines the URL route for your homepage.
+ debug=True restarts the server automatically when you change code.

To run the App:

```shell
$ python3 app.py

# Output that should be displayed in the terminal:
* Running on http://127.0.0.1:5000/
```
