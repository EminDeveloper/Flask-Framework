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
    return "Good day and good coding, Flask Framework!"
</pre>


<p>‘/’ URL is bound with <code>hello()</code> function. When the home page of the webserver is opened in the browser, the output of this function will be rendered accordingly.</p>
<p>The Flask application is started by calling the <code>run()</code> function. The method should be restarted manually for any change in the code. To overcome this, the debug support is enabled so as to track any error.</p>

<table border="0" cellpadding="0" cellspacing="0">
<tbody>
<tr>
<td class="code">
<div class="container">
<div class="line number1 index0 alt2"><code class="plain">app.debug </code><code class="keyword">=</code> <code class="color1">True</code></div>
<div class="line number2 index1 alt1"><code class="plain">app.run() </code></div>
<div class="line number3 index2 alt2"><code class="plain">app.run(debug </code><code class="keyword">=</code> <code class="color1">True</code><code class="plain">) </code></div>
</div>
</td>
</tr>
</tbody>
</table>


<p>&nbsp;<br>
<b>Routing:</b><br>
Nowadays, the web frameworks provide routing technique so that user can remember the URLs. It is useful to access the web page directly without navigating from the Home page. It is done through the following <code>route()</code> decorator, to bind the URL to a function.</p>


<table border="0" cellpadding="0" cellspacing="0">
<tbody>
<tr>
<td class="code">
<div class="container">
<div class="line number1 index0 alt2"><code class="comments"># decorator to route URL </code></div>
<div class="line number2 index1 alt1"><code class="decorator">@app</code><code class="plain">.route(‘</code><code class="keyword">/</code><code class="plain">hello’)&nbsp;&nbsp; </code></div>
<div class="line number3 index2 alt2"><code class="undefined spaces">&nbsp;</code>&nbsp;</div>
<div class="line number4 index3 alt1"><code class="comments"># binding to the function of route&nbsp; </code></div>
<div class="line number5 index4 alt2"><code class="keyword">def</code> <code class="plain">hello_world():&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </code></div>
<div class="line number6 index5 alt1"><code class="undefined spaces">&nbsp;&nbsp;&nbsp;</code><code class="keyword">return</code> <code class="plain">‘hello world’ </code></div>
</div>
</td>
</tr>
</tbody>
</table>

<p>If a user visits http://localhost:5000/hello URL, the output of the hello_world() function will be rendered in the browser. The <code>add_url_rule()</code> function of an application object can also be used to bind URL with the function as in above example.</p>

<table border="0" cellpadding="0" cellspacing="0">
<tbody>
<tr>
<td class="code">
<div class="container">
<div class="line number1 index0 alt2"><code class="keyword">def</code> <code class="plain">hello_world(): </code></div>
<div class="line number2 index1 alt1"><code class="undefined spaces">&nbsp;&nbsp;&nbsp;</code><code class="keyword">return</code> <code class="plain">‘hello world’ </code></div>
<div class="line number3 index2 alt2"><code class="plain">app.add_url_rule(‘</code><code class="keyword">/</code><code class="plain">’, ‘hello’, hello_world) </code></div>
</div>
</td>
</tr>
</tbody>
</table>


<p>&nbsp;<br>
<b>Using Variables in Flask:</b><br>
The Variables in the flask is used to build a URL dynamically by adding the variable parts to the rule parameter. This variable part is marked as. It is passed as keyword argument. See the example below</p>


<table border="0" cellpadding="0" cellspacing="0">
<tbody>
<tr>
<td class="code">
<div class="container">
<div class="line number1 index0 alt2"><code class="keyword">from</code> <code class="plain">flask </code><code class="keyword">import</code> <code class="plain">Flask </code></div>
<div class="line number2 index1 alt1"><code class="plain">app </code><code class="keyword">=</code> <code class="plain">Flask(__name__) </code></div>
<div class="line number3 index2 alt2"><code class="undefined spaces">&nbsp;</code>&nbsp;</div>
<div class="line number4 index3 alt1"><code class="comments"># routing the decorator function hello_name </code></div>
<div class="line number5 index4 alt2"><code class="decorator">@app</code><code class="plain">.route(</code><code class="string">'/hello/&lt;name&gt;'</code><code class="plain">)&nbsp;&nbsp; </code></div>
<div class="line number6 index5 alt1"><code class="keyword">def</code> <code class="plain">hello_name(name): </code></div>
<div class="line number7 index6 alt2"><code class="undefined spaces">&nbsp;&nbsp;&nbsp;</code><code class="keyword">return</code> <code class="string">'Hello %s!'</code> <code class="keyword">%</code> <code class="plain">name </code></div>
<div class="line number8 index7 alt1"><code class="undefined spaces">&nbsp;</code>&nbsp;</div>
<div class="line number9 index8 alt2"><code class="keyword">if</code> <code class="plain">__name__ </code><code class="keyword">=</code><code class="keyword">=</code> <code class="string">'__main__'</code><code class="plain">: </code></div>
<div class="line number10 index9 alt1"><code class="undefined spaces">&nbsp;&nbsp;&nbsp;</code><code class="plain">app.run(debug </code><code class="keyword">=</code> <code class="color1">True</code><code class="plain">) </code></div>
</div>
</td>
</tr>
</tbody>
</table>


<p>Save the above example as hello.py and run from power shell. Next, open the browser and enter the URL http://localhost:5000/hello/GeeksforGeeks.</p>


<p>In the above example, the parameter of route() decorator contains the variable part attached to the URL ‘/hello’ as an argument. Hence, if URL like http://localhost:5000/hello/GeeksforGeeks is entered then ‘GeeksforGeeks’ will be passed to the hello() function as an argument.</p>

<p>In addition to the default string variable part, other data types like int, float, and path(for directory separator channel which can take slash) are also used. The URL rules of Flask are based on Werkzeug’s routing module. This ensures that the URLs formed are unique and based on precedents laid down by Apache. </p>

<p><strong>Examples:</strong></p>

<div class="noIdeBtnDiv">
<div class="code-block">
<div class="code-gutter">
<div class="editor-buttons-container">
<div class="editor-buttons">
<div class="editor-buttons-div" title="Run and Edit">
                                    <i id="copy-code-button" title="Copy Code" class="gfg-icon gfg-icon_copy code-sidebar-button padding-2px copy-code-button"></i><p></p>
<div id="run-and-edit-loader" class="ring-load"></div>
<p>                                    <i id="run-and-edit-button" title="Edit Code" lang="python3" class="gfg-icon gfg-icon_edit_1 padding-2px code-sidebar-button"></i><br>
                                    <i id="close-code-editor-button" title="Close Editor" class="gfg-icon gfg-icon_close-editor padding-2px code-sidebar-button close-code-editor-button"></i></p>
<div id="run-code-loader" class="ring-load"></div>
<p>                                    <i id="run-code-button" lang="python3" title="Run Code and See Output" class="gfg-icon gfg-icon_play padding-2px code-sidebar-button"></i></p>
<div id="generate-url-loader" class="ring-load"></div>
<p>                                    <i id="generate-url-and-run-button" title="Run Code and Generate IDE URL" lang="python3" class="gfg-icon gfg-icon_link padding-2px code-sidebar-button generate-url-and-run-button"></i><br>
                                    <i title="Light Mode" class="gfg-icon padding-2px code-sidebar-button light-editor-button gfg-icon_light-toggle"></i><br>
                                    <i id="edit-on-ide-button" title="Edit on IDE" lang="python3" class="gfg-icon gfg-icon_code padding-2px code-sidebar-button edit-on-ide-button"></i>
                                </p></div>
<p></p></div>
<p></p></div>
<p></p></div>
<div class="code-container">
<div id="highlighter_389901" class="syntaxhighlighter nogutter night">
<table border="0" cellpadding="0" cellspacing="0">
<tbody>
<tr>
<td class="code">
<div class="container">
<div class="line number1 index0 alt2"><code class="keyword">from</code> <code class="plain">flask </code><code class="keyword">import</code> <code class="plain">Flask </code></div>
<div class="line number2 index1 alt1"><code class="plain">app </code><code class="keyword">=</code> <code class="plain">Flask(__name__) </code></div>
<div class="line number3 index2 alt2"><code class="undefined spaces">&nbsp;</code>&nbsp;</div>
<div class="line number4 index3 alt1"><code class="decorator">@app</code><code class="plain">.route(</code><code class="string">'/blog/&lt;postID&gt;'</code><code class="plain">) </code></div>
<div class="line number5 index4 alt2"><code class="keyword">def</code> <code class="plain">show_blog(postID): </code></div>
<div class="line number6 index5 alt1"><code class="undefined spaces">&nbsp;&nbsp;&nbsp;</code><code class="keyword">return</code> <code class="string">'Blog Number %d'</code> <code class="keyword">%</code> <code class="plain">postID </code></div>
<div class="line number7 index6 alt2"><code class="undefined spaces">&nbsp;</code>&nbsp;</div>
<div class="line number8 index7 alt1"><code class="decorator">@app</code><code class="plain">.route(</code><code class="string">'/rev/&lt;revNo&gt;'</code><code class="plain">) </code></div>
<div class="line number9 index8 alt2"><code class="keyword">def</code> <code class="plain">revision(revNo): </code></div>
<div class="line number10 index9 alt1"><code class="undefined spaces">&nbsp;&nbsp;&nbsp;</code><code class="keyword">return</code> <code class="string">'Revision Number %f'</code> <code class="keyword">%</code> <code class="plain">revNo </code></div>
<div class="line number11 index10 alt2"><code class="undefined spaces">&nbsp;</code>&nbsp;</div>
<div class="line number12 index11 alt1"><code class="keyword">if</code> <code class="plain">__name__ </code><code class="keyword">=</code><code class="keyword">=</code> <code class="string">'__main__'</code><code class="plain">: </code></div>
<div class="line number13 index12 alt2"><code class="undefined spaces">&nbsp;&nbsp;&nbsp;</code><code class="plain">app.run() </code></div>
<div class="line number14 index13 alt1"><code class="undefined spaces">&nbsp;</code>&nbsp;</div>
<div class="line number15 index14 alt2"><code class="comments"># say the URL is <a href="http://localhost:5000/blog/555">http://localhost:5000/blog/555</a> </code></div>
</div>
</td>
</tr>
</tbody>
</table>
</div></div>
<div class="code-editor-container"></div>
<p></p></div>
<div class="code-output-container">
<div class="output-block">
                        <i id="output-icon" title="Output" class="gfg-icon gfg-icon_arrow-right-editor padding-2px code-sidebar-button output-icon"></i><p></p>
<pre class="output-pre"></pre>
<p></p></div>
<div class="ide-link-div">
                        <i id="copy-url-button" title="Copy Generated Ide URL" class="gfg-icon gfg-icon_copy padding-2px code-sidebar-button copy-url-button"></i><p></p>
<pre id="ide-url"></pre>
<p></p></div>
<p></p></div>
<p></p></div>




NEW

NEw

NEw