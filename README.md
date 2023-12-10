# [Flask-Framework](https://flask.palletsprojects.com/en/3.0.x/) 

### About Flask Framework:
Flask is a lightweight and flexible web framework for Python. It's designed to be easy to use and build web applications quickly and efficiently. Some of its key features include:

+ **Lightweight**: Flask is simple and easy to get started with.
+ **Modularity**: It allows you to choose the components you need and easily integrate them.
+ **Built-in development server**: Flask comes with a built-in development server, making it convenient for testing your applications.
+ **Extensible**: It provides various extensions to add functionalities as needed.
+ **Jinja2 Templating**: Flask uses the Jinja2 templating engine to render HTML templates.

## Python | Introduction to Web development using Flask

**What is Flask?**
Flask is an API of Python that allows us to build up web-applications. It was developed by Armin Ronacher. Flask’s framework is more explicit than Django’s framework and is also easier to learn because it has less base code to implement a simple web-Application. A Web-Application Framework or Web Framework is the collection of modules and libraries that helps the developer to write applications without writing the low-level codes such as protocols, thread management, etc. Flask is based on WSGI(Web Server Gateway Interface) toolkit and Jinja2 template engine.

**Getting Started With Flask:**
Python 2.6 or higher is required for the installation of the Flask. You can start by import Flask from the flask package on any python IDE. For installation on any environment, you can click on the installation link given below.
To test that if the installation is working, check out this code given below.

### Installing Flask:
To install Flask, you'll need Python installed on your system. Then, you can use pip, Python's package manager, to install Flask. Here are the steps:
1. **Install Python**: If you haven't installed Python, download and install it from the official website: [Python Official Website](https://www.python.org/)
2. **Install Flask**:
Open your terminal or command prompt and enter the following command:

 ```python
 pip install Flask 
 ``` 
### Creating Your First Flask Project:
Once Flask is installed, you can create your first Flask project:
 
**Create a Folder for Your Project:**

Create a new directory for your project. Open your terminal or command prompt, navigate to the directory where you want to create the project, and create a folder, for example:
```bash
mkdir  my_flask_app
my_flask_app
```
**Create a Python File:**
Inside your project folder, create a Python file (e.g., ```app.py```) which will contain your Flask application:
```python
from flask  import Flask

app = Flask(__name__)

@app.route('/')
def hello():
    return 'Hello, Flask!'

if __name__ == '__main__':
    app.run(debug=>True)
```
3. **Run Your Flask Application:**
In the terminal, run your Flask application by executing the Python file you created: python app.py
4. **View Your Application:**
Open a web browser and go to http://127.0.0.1:5000/ or http://localhost:5000/. You should see 'Hello, Flask!' displayed, indicating your Flask app is running.

### Create working enviroment:

#### Install virtual enviroment and add virtual enviroment
```bash
pip install virtualenv
python -m virtualenv venv
source venv/bin/activate # for Linux/MacOS
venv\Scripts\activate 

pip install flask

set FLASK_APP=main.py
flask run
```


Example flask run code:
```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def hello_world():
    return "Good day and good coding, Flask Framework!"
```


‘/’ URL is bound with ```hello()``` function. When the home page of the webserver is opened in the browser, the output of this function will be rendered accordingly.

The Flask application is started by calling the```run()``` function. The method should be restarted manually for any change in the code. To overcome this, the debug support is enabled so as to track any error.

```python
app.debug = True
app.run()
app.run(debug=True) 
```

## Routing [¶](./)

Creating effective routes in web applications is crucial for user engagement. A well-crafted URL not only helps users remember and revisit a page but also enhances their overall experience. Flask simplifies this process by employing the ```route()``` decorator to link a function to a specific URL.
Routing is the process of mapping a URL to a function. 

```python
 from flask 
 import Flask

app = Flask(__name__)

@app.route('/')
def index():
    return 'Index Page'

@app.route('/hello')
def hello():
    return 'Hello, World'
```

### Basic Routing:
In Flask, routing is achieved using the ```@app.route()``` decorator. This decorator binds a URL to a Python function, defining what should be displayed or executed when that URL is accessed.

```python
from flask 
import Flask

app = Flask(__name__)

@app.route('/')
def index():
    return 'Index Page'

@app.route('/hello')
def hello():
    return 'Hello, World'
```
Here, accessing the root URL (```'/'```) will display 'Index Page', while visiting ```/hello``` will render 'Hello, World'.

### Dynamic Routing:
Flask supports dynamic URLs, allowing parts of the URL to be variable. You can specify variable sections in the route by using ```variable_name```. These variables can then be captured and utilized within the view function.

```python
from flask import Flask

@app.route('/user/<username>')
def show_user_profile(username):
    return f'User: {username}' 
```

