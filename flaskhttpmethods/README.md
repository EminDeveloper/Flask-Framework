# Flask HTTP methods, handle GET & POST requests

So, this article is about how we deal with GET and POST requests in Flask using Python.

Think of the internet like a big web (like Spider-Man’s world but with more cat videos). When you’re on a website, your computer talks to the server using different methods. These methods are like ways of asking for things or telling the server to do stuff. In Flask, we have a bunch of these methods, like GET, POST, PUT, DELETE, and HEAD. Each one helps us do different things like getting info, sending data, or deleting stuff from the server. Cool, right?

# Understanding HTTP Methods with Flask

This repository aims to provide a comprehensive breakdown of commonly used HTTP methods and demonstrate their implementation within a simple Flask project, specifically focusing on handling user logins using GET and POST.

## HTTP Methods Explained

### **GET**
GET is akin to requesting information from the server. Imagine shopping online and searching for an item. When you hit search, the search term appears in the website link. It's for acquiring information and isn't considered sensitive as it's visible in the URL.

### **POST**
POST involves sending data to the server. For instance, when signing up or logging in on a website, the details entered are submitted to the server. Unlike GET, this data isn't visible in the website link, maintaining a level of privacy.

### **PUT**
PUT is primarily for updating server data. However, in many cases, developers prefer using POST for these updates.

### **DELETE**
As the name suggests, DELETE is used to remove specific data from the server.

### **HEAD**
Similar to GET, HEAD fetches only the headers of the information, omitting the complete content.

### **CONNECT**
CONNECT establishes a connection to a designated server.

### **OPTIONS**
OPTIONS informs about the available communication methods for a resource.

### **TRACE**
TRACE resembles testing the pathway to a resource.

### **PATCH**
PATCH is for making minor alterations to a resource without modifying the entire content.

Now, let's build a simple project in Flask to show how we use GET and POST for handling user logins!

### What's the best way to manage GET and POST requests using Flask in Python?
When working with requests in Flask, we utilize a construct known as a route decorator. Within this decorator, there exists an attribute called `methods`. This attribute instructs our code about the type of requests a particular function can manage. If left unspecified, it defaults to accepting a GET request. However, we have the option to explicitly define the types of requests it can handle using the following syntax:

`Syntax: @app.routes(‘/example’, methods=[‘GET’, ‘POST])`


### Code Example for Handling GET & POST Requests
In this illustrative code snippet, users access a login form to submit their credentials. On the backend, we retrieve the provided username. To extract the value of a specific input, we utilize its designated `name` attribute. Implementing this functionality requires setting up the Flask application accordingly.

### Step-by-Step Implementation:
**Step 1:** Begin by establishing a new project folder. Inside this folder, create a `templates` directory to house HTML files. Outside the `templates` directory, store your Python file. As part of this process, generate both a `login.html` file and an `app.py` file.

![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.](https://media.geeksforgeeks.org/wp-content/uploads/20221219184612/Screenshot-2022-12-19-184502.png)

## Step 2: Crafting a Login Form

In this step, we've developed a straightforward login form using HTML. Within this form, we've created two login instances to showcase the functionality of GET and POST requests.

- The first form utilizes a GET request for logging in.
- The second form employs a POST request for authentication.

It's crucial to highlight that this HTML page is securely stored in the templates folder, as described in the initial step.


```html
<!-- templates/login.html-->

<html>

<head>
	<title>Handling of http get and post request</title>
	<style>
		div {
			width: 400px;
			border: 1px solid green;
			padding: 10px;
			margin-bottom: 5px;
		}
	</style>
</head>

<body>

	<div>
<!-- url_for will route the forms request to 
appropriate function that user made to handle it.-->
<!--we will Retrieve submitted values of inputs 
on the backend side using 'name' field of form.-->
		<h1>Handle GET Request</h1>
		<form method="GET"
			action="{{ url_for('handle_get') }}">
			<input type="text"
				name="username"
				placeholder="Username">
			<input type="password"
				name="password"
				placeholder="Password">
			<button type="submit">submit</button>
		</form>
	</div>
	<div>
		<h1>Handle POST Request</h1>
		<form method="POST"
			action="{{ url_for('handle_post') }}">
			<input type="text"
				name="username"
				placeholder="Username">
			<input type="password"
				name="password"
				placeholder="Password">
			<button type="submit">submit</button>
		</form>
	</div>
</body>

</html>
```