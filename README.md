<h1><a href="https://flask.palletsprojects.com/en/3.0.x/">Flask-Framework</a></h1> <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3c/Flask_logo.svg/1200px-Flask_logo.svg.png" jsaction="VQAsE" class="sFlh5c pT0Scc iPVvYb" style="max-width: 1200px; height: 332px; margin: 0px; width: 847px;" alt="Flask (web framework)" jsname="kn3ccd" aria-hidden="false">


<h3>About Flask Framework:</h3>
<p>Flask is a lightweight and flexible web framework for Python. It's designed to be easy to use and build web applications quickly and efficiently. Some of its key features include:</p>
<ul><li><strong>Lightweight</strong>: Flask is simple and easy to get started with.</li><li><strong>Modularity</strong>: It allows you to choose the components you need and easily integrate them.</li><li><strong>Built-in development server</strong>: Flask comes with a built-in development server, making it convenient for testing your applications.</li><li><strong>Extensible</strong>: It provides various extensions to add functionalities as needed.</li><li><strong>Jinja2 Templating</strong>: Flask uses the Jinja2 templating engine to render HTML templates.</li></ul>

# Python | Introduction to Web development using Flask

<p><b>What is Flask?</b><br>
Flask is an API of Python that allows us to build up web-applications. It was developed by Armin Ronacher. Flask’s framework is more explicit than Django’s framework and is also easier to learn because it has less base code to implement a simple web-Application. A Web-Application Framework or Web Framework is the collection of modules and libraries that helps the developer to write applications without writing the low-level codes such as protocols, thread management, etc. Flask is based on WSGI(Web Server Gateway Interface) toolkit and Jinja2 template engine.</p>

<p><b>Getting Started With Flask:</b><br>
Python 2.6 or higher is required for the installation of the Flask. You can start by import Flask from the flask package on any python IDE. For installation on any environment, you can click on the installation link given below.<br>
To test that if the installation is working, check out this code given below.</p>

<h3>Installing Flask:</h3>
<p>To install Flask, you'll need Python installed on your system. Then, you can use pip, Python's package manager, to install Flask. Here are the steps:</p>
<ol><li><p><strong>Install Python</strong>: If you haven't installed Python, download and install it from the official website: <a href="https://www.python.org/" target="_new">Python Official Website</a>.</p></li><li><p><strong>Install Flask</strong>:
Open your terminal or command prompt and enter the following command:</p><pre><div class="bg-black rounded-md"><div class="flex items-center relative text-gray-200 bg-gray-800 dark:bg-token-surface-primary px-4 py-2 text-xs font-sans justify-between rounded-t-md"></div><div class="p-4 overflow-y-auto"><code class="!whitespace-pre hljs">pip install Flask
</code></div></div></pre></li></ol>
<h3>Creating Your First Flask Project:</h3>
<p>Once Flask is installed, you can create your first Flask project:</p>
<ol><li><p><strong>Create a Folder for Your Project</strong>:
Create a new directory for your project. Open your terminal or command prompt, navigate to the directory where you want to create the project, and create a folder, for example:</p><pre><div class="bg-black rounded-md"><div class="flex items-center relative text-gray-200 bg-gray-800 dark:bg-token-surface-primary px-4 py-2 text-xs font-sans justify-between rounded-t-md"></div><div class="p-4 overflow-y-auto"><code class="!whitespace-pre hljs language-bash"><span class="hljs-built_in">mkdir</span> my_flask_app
<span class="hljs-built_in">cd</span> my_flask_app
</code></div></div></pre></li><li><p><strong>Create a Python File</strong>:
Inside your project folder, create a Python file (e.g., <code>app.py</code>) which will contain your Flask application:</p><pre><div class="bg-black rounded-md"><div class="flex items-center relative text-gray-200 bg-gray-800 dark:bg-token-surface-primary px-4 py-2 text-xs font-sans justify-between rounded-t-md"><span>python</span></div><div class="p-4 overflow-y-auto"><code class="!whitespace-pre hljs language-python"><span class="hljs-keyword">from</span> flask <span class="hljs-keyword">import</span> Flask

app = Flask(__name__)

<span class="hljs-meta">@app.route(<span class="hljs-params"><span class="hljs-string">'/'</span></span>)</span>
<span class="hljs-keyword">def</span> <span class="hljs-title function_">hello</span>():
    <span class="hljs-keyword">return</span> <span class="hljs-string">'Hello, Flask!'</span>

<span class="hljs-keyword">if</span> __name__ == <span class="hljs-string">'__main__'</span>:
    app.run(debug=<span class="hljs-literal">True</span>)
</code></div></div></pre></li><li><p><strong>Run Your Flask Application</strong>:
In the terminal, run your Flask application by executing the Python file you created:</p><pre><div class="bg-black rounded-md"><div class="flex items-center relative text-gray-200 bg-gray-800 dark:bg-token-surface-primary px-4 py-2 text-xs font-sans justify-between rounded-t-md"></div><div class="p-4 overflow-y-auto"><code class="!whitespace-pre hljs">python app.py
</code></div></div></pre></li><li><p><strong>View Your Application</strong>:
Open a web browser and go to <code>http://127.0.0.1:5000/</code> or <code>http://localhost:5000/</code>. You should see 'Hello, Flask!' displayed, indicating your Flask app is running.</p></li></ol>



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

<h2>Routing<a class="headerlink" href="#routing" title="Link to this heading">¶</a></h2>

<p>Creating effective routes in web applications is crucial for user engagement. A well-crafted URL not only helps users remember and revisit a page but also enhances their overall experience. Flask simplifies this process by employing the <code>route()</code> decorator to link a function to a specific URL.</p>

<div class="p-4 overflow-y-auto"><code class="!whitespace-pre hljs language-python"><span class="hljs-keyword">from</span> flask <span class="hljs-keyword">import</span> Flask

app = Flask(__name__)

<span class="hljs-meta">@app.route(<span class="hljs-params"><span class="hljs-string">'/'</span></span>)</span>
<span class="hljs-keyword">def</span> <span class="hljs-title function_">index</span>():
    <span class="hljs-keyword">return</span> <span class="hljs-string">'Index Page'</span>

<span class="hljs-meta">@app.route(<span class="hljs-params"><span class="hljs-string">'/hello'</span></span>)</span>
<span class="hljs-keyword">def</span> <span class="hljs-title function_">hello</span>():
    <span class="hljs-keyword">return</span> <span class="hljs-string">'Hello, World'</span>
</code></div>
<h3>Basic Routing:</h3>
<p>In Flask, routing is achieved using the <code>@app.route()</code> decorator. This decorator binds a URL to a Python function, defining what should be displayed or executed when that URL is accessed.</p>

<div class="p-4 overflow-y-auto"><code class="!whitespace-pre hljs language-python"><span class="hljs-keyword">from</span> flask <span class="hljs-keyword">import</span> Flask

app = Flask(__name__)

<span class="hljs-meta">@app.route(<span class="hljs-params"><span class="hljs-string">'/'</span></span>)</span>
<span class="hljs-keyword">def</span> <span class="hljs-title function_">index</span>():
    <span class="hljs-keyword">return</span> <span class="hljs-string">'Index Page'</span>

<span class="hljs-meta">@app.route(<span class="hljs-params"><span class="hljs-string">'/hello'</span></span>)</span>
<span class="hljs-keyword">def</span> <span class="hljs-title function_">hello</span>():
    <span class="hljs-keyword">return</span> <span class="hljs-string">'Hello, World'</span>
</code></div>
<p>Here, accessing the root URL (<code>'/'</code>) will display 'Index Page', while visiting <code>/hello</code> will render 'Hello, World'.</p>
<h3>Dynamic Routing:</h3>
<p>Flask supports dynamic URLs, allowing parts of the URL to be variable. You can specify variable sections in the route by using <code>&lt;variable_name&gt;</code>. These variables can then be captured and utilized within the view function.</p>
<textarea id="read-only-cursor-text-area" aria-label="file content" aria-readonly="true" inputmode="none" tabindex="0" aria-multiline="true" aria-haspopup="false" data-gramm="false" data-gramm_editor="false" data-enable-grammarly="false" spellcheck="false" autocorrect="off" autocapitalize="off" autocomplete="off" data-ms-editor="false" class="react-blob-print-hide" style="resize: none; margin-top: -2px; padding-left: 92px; width: 100%; background-color: unset; color: transparent; position: absolute; border: none; tab-size: 8; outline: none; overflow: auto hidden; height: 220px; font-size: 12px; line-height: 20px; overflow-wrap: normal; white-space: pre;">
from flask import Flask
@app.route('/user/<username>')
def show_user_profile(username):
    return f'User: {username}'
</textarea>
<div class="Box-sc-g0xbh4-0 eRkHwF"><textarea id="read-only-cursor-text-area" aria-label="file content" aria-readonly="true" inputmode="none" tabindex="0" aria-multiline="true" aria-haspopup="false" data-gramm="false" data-gramm_editor="false" data-enable-grammarly="false" spellcheck="false" autocorrect="off" autocapitalize="off" autocomplete="off" data-ms-editor="false" class="react-blob-print-hide" style="resize: none; margin-top: -2px; padding-left: 92px; width: 100%; background-color: unset; color: transparent; position: absolute; border: none; tab-size: 8; outline: none; overflow: auto hidden; height: 220px; font-size: 12px; line-height: 20px; overflow-wrap: normal; white-space: pre;">from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello_world():
    return '&lt;h1&gt;Hello World&lt;/h1&gt;'

@app.route('/about/&lt;username&gt;')
def about_page(username):
    return f'&lt;h1&gt;This is the about page of {username}'</textarea><button hidden="" data-testid="" data-hotkey="Alt+F1,Control+Alt+˙,Control+Alt+h" data-hotkey-scope="read-only-cursor-text-area"></button><div class="Box-sc-g0xbh4-0 cpgGLU"><div tabindex="0" class="Box-sc-g0xbh4-0 jIrvpW"><div class="Box-sc-g0xbh4-0 blTtWT react-code-file-contents" role="presentation" aria-hidden="true" data-tab-size="8" data-paste-markdown-skip="true" data-hpc="true" style="height: 200px;"><div class="react-line-numbers" style="pointer-events: auto; height: 200px;"><div data-line-number="1" class="react-line-number react-code-text" style="padding-right: 16px;">1</div><div data-line-number="2" class="react-line-number react-code-text virtual" style="padding-right: 16px; transform: translateY(20px);">2</div><div data-line-number="3" class="react-line-number react-code-text virtual" style="padding-right: 16px; transform: translateY(40px);">3</div><div data-line-number="4" class="react-line-number react-code-text virtual" style="padding-right: 16px; transform: translateY(60px);">4</div><div data-line-number="5" class="react-line-number react-code-text virtual" style="padding-right: 16px; transform: translateY(80px);">5</div><div data-line-number="6" class="react-line-number react-code-text virtual" style="padding-right: 16px; transform: translateY(100px);">6</div><div data-line-number="7" class="react-line-number react-code-text virtual" style="padding-right: 16px; transform: translateY(120px);">7</div><div data-line-number="8" class="react-line-number react-code-text virtual" style="padding-right: 16px; transform: translateY(140px);">8</div><div data-line-number="9" class="react-line-number react-code-text virtual" style="padding-right: 16px; transform: translateY(160px);">9</div><div data-line-number="10" class="react-line-number react-code-text virtual" style="padding-right: 16px; transform: translateY(180px);">10</div></div><div class="react-code-lines" style="height: 200px;"><div data-key="0" class="react-code-text react-code-line-contents" style="min-height: auto;"><div><div id="LC1" class="react-file-line html-div" data-testid="code-cell" data-line-number="1" style="position: relative;"><span class="pl-k" data-code-text="from"></span><span data-code-text=" "></span><span class="pl-s1" data-code-text="flask"></span><span data-code-text=" "></span><span class="pl-k" data-code-text="import"></span><span data-code-text=" "></span><span class="pl-v" data-code-text="Flask"></span></div></div></div><div data-key="1" class="react-code-text react-code-line-contents virtual" style="transform: translateY(20px); min-height: auto;"><div><div id="LC2" class="react-file-line html-div" data-testid="code-cell" data-line-number="2" style="position: relative;"><span class="pl-s1" data-code-text="app"></span><span data-code-text=" "></span><span class="pl-c1" data-code-text="="></span><span data-code-text=" "></span><span class="pl-v" data-code-text="Flask"></span><span data-code-text="("></span><span class="pl-s1" data-code-text="__name__"></span><span data-code-text=")"></span></div></div></div><div data-key="2" class="react-code-text react-code-line-contents virtual" style="transform: translateY(40px); min-height: auto;"><div><div id="LC3" class="react-file-line html-div" data-testid="code-cell" data-line-number="3" style="position: relative;"><span data-code-text="
"></span></div></div></div><div data-key="3" class="react-code-text react-code-line-contents virtual" style="transform: translateY(60px); min-height: auto;"><div><div id="LC4" class="react-file-line html-div" data-testid="code-cell" data-line-number="4" style="position: relative;"><span class="pl-en"><span data-code-text="@"></span><span class="pl-s1" data-code-text="app"></span><span data-code-text="."></span><span class="pl-en" data-code-text="route"></span><span data-code-text="("></span><span class="pl-s" data-code-text="'/'"></span><span data-code-text=")"></span></span></div></div></div><div data-key="4" class="react-code-text react-code-line-contents virtual" style="transform: translateY(80px); min-height: auto;"><div><div id="LC5" class="react-file-line html-div" data-testid="code-cell" data-line-number="5" style="position: relative;"><span class="pl-k" data-code-text="def"></span><span data-code-text=" "></span><span class="pl-en" data-code-text="hello_world"></span><span data-code-text="():"></span></div></div></div><div data-key="5" class="react-code-text react-code-line-contents virtual" style="transform: translateY(100px); min-height: auto;"><div><div id="LC6" class="react-file-line html-div" data-testid="code-cell" data-line-number="6" style="position: relative;"><span data-code-text="    "></span><span class="pl-k" data-code-text="return"></span><span data-code-text=" "></span><span class="pl-s" data-code-text="'<h1>Hello World</h1>'"></span></div></div></div><div data-key="6" class="react-code-text react-code-line-contents virtual" style="transform: translateY(120px); min-height: auto;"><div><div id="LC7" class="react-file-line html-div" data-testid="code-cell" data-line-number="7" style="position: relative;"><span data-code-text="
"></span></div></div></div><div data-key="7" class="react-code-text react-code-line-contents virtual" style="transform: translateY(140px); min-height: auto;"><div><div id="LC8" class="react-file-line html-div" data-testid="code-cell" data-line-number="8" style="position: relative;"><span class="pl-en"><span data-code-text="@"></span><span class="pl-s1" data-code-text="app"></span><span data-code-text="."></span><span class="pl-en" data-code-text="route"></span><span data-code-text="("></span><span class="pl-s" data-code-text="'/about/<username>'"></span><span data-code-text=")"></span></span></div></div></div><div data-key="8" class="react-code-text react-code-line-contents virtual" style="transform: translateY(160px); min-height: auto;"><div><div id="LC9" class="react-file-line html-div" data-testid="code-cell" data-line-number="9" style="position: relative;"><span class="pl-k" data-code-text="def"></span><span data-code-text=" "></span><span class="pl-en" data-code-text="about_page"></span><span data-code-text="("></span><span class="pl-s1" data-code-text="username"></span><span data-code-text="):"></span></div></div></div><div data-key="9" class="react-code-text react-code-line-contents virtual" style="transform: translateY(180px); min-height: auto;"><div><div id="LC10" class="react-file-line html-div" data-testid="code-cell" data-line-number="10" style="position: relative;"><span data-code-text="    "></span><span class="pl-k" data-code-text="return"></span><span data-code-text=" "></span><span class="pl-s"><span data-code-text="f'<h1>This is the about page of "></span><span class="pl-s1"><span class="pl-kos" data-code-text="{"></span><span class="pl-s1" data-code-text="username"></span><span class="pl-kos" data-code-text="}"></span></span><span data-code-text="'"></span></span></div></div></div></div><button hidden="" data-hotkey="Control+a"></button><div aria-hidden="true" data-testid="navigation-cursor" class="Box-sc-g0xbh4-0 code-navigation-cursor" style="top: 100px; left: 310px;"> </div><button hidden="" data-testid="NavigationCursorEnter" data-hotkey="Control+Enter" data-hotkey-scope="read-only-cursor-text-area"></button><button hidden="" data-testid="NavigationCursorSetHighlightedLine" data-hotkey="J" data-hotkey-scope="read-only-cursor-text-area"></button><button hidden="" data-testid="NavigationCursorSetHighlightAndExpandMenu" data-hotkey="Alt+C,Alt+Ç" data-hotkey-scope="read-only-cursor-text-area"></button><button hidden="" data-testid="NavigationCursorPageDown" data-hotkey="PageDown" data-hotkey-scope="read-only-cursor-text-area"></button><button hidden="" data-testid="NavigationCursorPageUp" data-hotkey="PageUp" data-hotkey-scope="read-only-cursor-text-area"></button><button hidden="" data-testid="" data-hotkey="/" data-hotkey-scope="read-only-cursor-text-area"></button></div></div></div></div>