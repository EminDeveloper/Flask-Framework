# Flask-Framework


<p style="text-align:justify;">This <strong>Flask Tutorial</strong> is the latest and comprehensive guide designed for beginners and professionals to learn <strong>Python Flask</strong> framework, which is one of the most popular Python-based web frameworks. Whether you are a beginner or an experienced developer, this tutorial is specially designed to help you learn and master Flask and build your own real-world web applications. This Flask Tutorial covers a wide range of topics from basic concepts such as setup and installation to advanced concepts like user authentication, database integration, and deployment. In addition to this, we also provide you with a list of Flask projects, FAQs, and interview questions for your future Interview.</p>

# Python | Introduction to Web development using Flask

<p><b>What is Flask?</b><br>
Flask is an API of Python that allows us to build up web-applications. It was developed by Armin Ronacher. Flask’s framework is more explicit than Django’s framework and is also easier to learn because it has less base code to implement a simple web-Application. A Web-Application Framework or Web Framework is the collection of modules and libraries that helps the developer to write applications without writing the low-level codes such as protocols, thread management, etc. Flask is based on WSGI(Web Server Gateway Interface) toolkit and Jinja2 template engine.</p>

<p><b>Getting Started With Flask:</b><br>
Python 2.6 or higher is required for the installation of the Flask. You can start by import Flask from the flask package on any python IDE. For installation on any environment, you can click on the installation link given below.<br>
To test that if the installation is working, check out this code given below.</p>

<p>Create working enviroment:

--  Install virtual enviroment and add virtual enviroment
<pre>
pip install virtualenv
python -m virtualenv venv
source venv/bin/activate # for Linux/MacOS
venv\Scripts\activate 

pip install flask

set FLASK_APP=main.py
flask run
</pre>

</p>

<p>
Example flask run code:
</p>
<pre>
from flask import Flask

app = Flask(__name__)

@app.route("/")
def hello_world():
    return "<p>Good day and good coding, Flask Framework!</p>"
</pre>


