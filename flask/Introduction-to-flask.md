- Flask Notes by Praveen Kumar
# Introduction to Flask

- What is Flask?
    
    Flask is a web framework written in Python that allows developers to build web applications quickly and easily. It is lightweight, flexible, and ideal for building small to medium-sized web applications.
    
    Flask was created by Armin Ronacher and released in 2010. Its design philosophy is based on simplicity and minimalism, which makes it easy to learn and use. Flask has a modular design, which means that you can add or remove features as needed, making it very customizable.
    
    One of the key strengths of Flask is its built-in support for templating, which allows developers to create dynamic HTML pages using Python code. This makes it easy to create complex web applications without having to write a lot of boilerplate code.
    
    Flask also supports extensions, which are pre-built packages that provide additional functionality such as database integration, user authentication, and more. These extensions allow developers to quickly add advanced features to their applications without having to write a lot of custom code.
    
    Overall, Flask is a great choice for developers who want to build web applications quickly and easily, without sacrificing flexibility or scalability.
    
    To use Flask for web development, you first need to install it on your system using pip, the package installer for Python. Once installed, you can create a new Flask application by defining a Python file that will serve as the entry point for your application.
    
    Here's a simple example of a Flask app:
    
    ```
    from flask import Flask
    
    app = Flask(__name__)
    
    @app.route('/')
    def hello_world():
        return 'Hello, World!'
    
    if __name__ == '__main__':
        app.run()
    
    ```
    
    In this example, we import the Flask module and create an instance of the `Flask` class, which we name `app`. We then define a route for the root URL (`'/'`) and a function that returns the string `'Hello, World!'`. Finally, we run the app using the `run()` method.
    
    Once you've defined your Flask app, you can start adding more routes and functionality to it using Flask's built-in features or third-party extensions. Flask supports a wide range of web development tasks, including handling requests and responses, authentication and authorization, database integration, and more.
    
- Why Flask ?
    
    Flask is a popular Python web framework that is used for developing web applications. Flask is lightweight, flexible, and easy to use, making it a great choice for building both small and large-scale web applications.
    
    One of the main advantages of Flask is its simplicity. Flask provides a minimalistic approach to web development, allowing developers to focus on building their application without being bogged down by unnecessary complexity. Flask also has a small codebase, which makes it easier to understand and maintain.
    
    Flask is also highly customizable, allowing developers to add or remove functionality as needed. This flexibility makes Flask a great choice for building a wide range of web applications, from simple blog sites to complex e-commerce platforms.
    
    In addition, Flask has a vibrant community of developers who contribute to its ongoing development and provide support through online forums and documentation. Overall, Flask is a powerful and versatile web framework that has become a popular choice for building web applications in Python.
    
- Hello World APP
    
    Let's see how Flask works:
    
    Let's say you want to build a simple web application that displays a "Hello, World!" message on a webpage. Here are the steps you would take using Flask:
    
    1. First, you need to install Flask. You can do this using pip, the package installer for Python:
    
    ```
    Copy Code
    pip install Flask
    
    ```
    
    1. Once Flask is installed, create a new file called `app.py` in your project directory. This will be the main file for your application.
    2. In `app.py`, import the Flask module and create a new instance of the Flask class:
    
    ```
    pythonCopy Code
    from flask import Flask
    
    app = Flask(__name__)
    
    ```
    
    1. Next, define a route for your application using the `@app.route()` decorator:
    
    ```
    pythonCopy Code
    @app.route('/')
    def hello():
        return 'Hello, World!'
    
    ```
    
    This code defines a route for the root URL (`/`) of your application. When a user visits this URL, the `hello()` function will be called, which simply returns the string "Hello, World!".
    
    1. Finally, start the Flask development server by adding the following lines to `app.py`:
    
    ```
    pythonCopy Code
    if __name__ == '__main__':
        app.run()
    
    ```
    
    1. Run the `app.py` file from the command line using:
    
    ```
    Copy Code
    python app.py
    
    ```
    
    1. Open a web browser and type in `http://localhost:5000` in the address bar. You should see the "Hello, World!" message displayed on the page.
    
    That's it! You've just created a simple Flask web application. Of course, this is just the beginning—Flask has many more features and capabilities for building more complex web applications.
    
- Working principle of a Flask Application
    
    The working principle of Flask can be summarized in a few key points:
    
    1. Routing: Flask uses a decorator-based system for routing, which allows you to map URLs to specific functions in your application. For example, you can use the @app.route decorator to specify what function should be called when a user visits a particular URL.
    2. Templates: Flask uses a Jinja2 template engine to render HTML templates. You can use templates to separate your application logic from your presentation layer, making it easier to maintain and update your code.
    3. Views: In Flask, a view is simply a function that returns an HTTP response. Views can be decorated with additional functionality, such as authentication or caching.
    4. Request handling: Flask provides a request object that contains all the information about the current HTTP request. This makes it easy to access data submitted by the user or to set cookies or other HTTP headers.
    5. Extensions: Flask has a modular architecture that allows you to add functionality through extensions. There are many third-party Flask extensions available that provide additional features, such as database integration, authentication, and caching.
    
    Overall, Flask's working principle is designed to allow developers to build web applications quickly and efficiently, while still providing enough flexibility and functionality to meet their needs.
    
- Understanding the  routes in Flask
    
    In Flask, routes define the logic that determines how the application responds to client requests. A route is a decorator that binds a function to a URL endpoint so that when a client sends a request to that endpoint, the Flask application invokes the corresponding function.
    
    Here's an example of a basic Flask application with a single route:
    
    ```
    Copy Code
    from flask import Flask
    
    app = Flask(__name__)
    
    @app.route('/')
    def hello_world():
        return 'Hello, World!'
    
    ```
    
    In this example, the `@app.route('/')` decorator binds the `hello_world()` function to the root URL endpoint (`/`). When a client sends a GET request to the root URL, the Flask application invokes the `hello_world()` function and returns the string "Hello, World!" as the response.
    
    Routes can also accept dynamic parameters in the URL by including variable parts in the endpoint pattern. For example:
    
    ```
    Copy Code
    @app.route('/users/<username>')
    def show_user_profile(username):
        return f'User {username}'
    
    ```
    
    In this example, the `show_user_profile()` function is bound to the `/users/<username>` endpoint. Any value provided for `<username>` in the URL will be passed to the function as the `username` parameter.
    
    Flask also provides support for HTTP methods such as GET, POST, PUT, DELETE, etc. You can specify the allowed methods for a route using the `methods` argument:
    
    ```
    Copy Code
    @app.route('/login', methods=['GET', 'POST'])
    def login():
        if request.method == 'POST':
    # process login form dataelse:
    # display login form
    ```
    
    In this example, the `login()` function is bound to the `/login` endpoint and allows both GET and POST requests. If a POST request is received, the function processes the submitted data. Otherwise, it displays the login form.
    
- Working with templates
    
    In Flask, templates are used to separate the presentation logic from the application logic. Templates are written in HTML and can contain placeholders for dynamic content, which are filled in by the application before being sent to the client.
    
    Here's an example of how templates work in Flask:
    
    Let's say you have a Flask application that displays a list of products. In your application code, you would define a route that handles requests to the URL "/products":
    
    ```python
    pythonCopy Code
    from flask import Flask, render_template
    
    app = Flask(__name__)
    
    @app.route('/products')
    def show_products():
        products = ['Product A', 'Product B', 'Product C']
        return render_template('products.html', products=products)
    
    ```
    
    Inside the `show_products` function, we define a list of products and pass it to the `render_template` method. The first argument to `render_template` is the name of the template file (in this case, "products.html"). The second argument is a dictionary containing the data we want to pass to the template. In this case, we're passing the list of products as a variable named `products`.
    
    Now let's create the "products.html" template file:
    
    ```
    htmlCopy Code
    <!DOCTYPE html>
    <html>
    <head>
    	<title>Products</title>
    </head>
    <body>
    	<h1>Products</h1>
    	<ul>
    	{% for product in products %}
    		<li>{{ product }}</li>
    	{% endfor %}
    	</ul>
    </body>
    </html>
    
    ```
    
    This template will display a header tag containing the text "Products", followed by an unordered list of the products passed from the application. The `{% %}` syntax is used to denote template control statements, while the `{{ }}` syntax is used to output values.
    
    When the user navigates to the "/products" URL in their browser, Flask will execute the `show_products` function and pass the resulting HTML to the client. The template engine will replace the placeholders in the template with the actual values passed from the application, and the final HTML output will be displayed to the user.
    
- CRUD Application using in-memory data
    
    Flask is a Python web framework that allows you to build web applications quickly and easily. CRUD stands for Create, Read, Update, and Delete, which are the four basic functions needed for most database operations.
    
    Here's an example of a simple Flask app that performs CRUD operations on a list of books:
    
    ```
    Copy Code
    from flask import Flask, request, jsonify
    
    app = Flask(__name__)
    
    # Define a global variable to store the books
    books = []
    
    # Create a book@app.route('/books', methods=['POST'])
    def create_book():
        title = request.json['title']
        author = request.json['author']
        new_book = {'title': title, 'author': author}
        books.append(new_book)
        return jsonify(new_book)
    
    # Read all books@app.route('/books', methods=['GET'])
    def get_books():
        return jsonify(books)
    
    # Read a single book@app.route('/books/<int:book_id>', methods=['GET'])
    def get_book(book_id):
        for book in books:
            if book['id'] == book_id:
                return jsonify(book)
        return jsonify({'message': 'Book not found'})
    
    # Update a book@app.route('/books/<int:book_id>', methods=['PUT'])
    def update_book(book_id):
        for book in books:
            if book['id'] == book_id:
                book['title'] = request.json['title']
                book['author'] = request.json['author']
                return jsonify(book)
        return jsonify({'message': 'Book not found'})
    
    # Delete a book@app.route('/books/<int:book_id>', methods=['DELETE'])
    def delete_book(book_id):
        for book in books:
            if book['id'] == book_id:
                books.remove(book)
                return jsonify({'message': 'Book deleted'})
        return jsonify({'message': 'Book not found'})
    
    if __name__ == '__main__':
        app.run(debug=True)
    
    ```
    
    In this example, we define a global variable called `books` to store the list of books. Then we define five routes for performing CRUD operations on the books.
    
    The `create_book()` function handles the creation of a new book. It reads the book information from the request body in JSON format, creates a new book dictionary and appends it to the `books` list. It then returns the new book as a JSON response.
    
    The `get_books()` function retrieves all books from the `books` list and returns them as a JSON response.
    
    The `get_book()` function retrieves a single book by its ID from the `books` list and returns it as a JSON response. If the book is not found, it returns an error message.
    
    The `update_book()` function updates a book's information by its ID. It reads the updated book information from the request body and updates the corresponding book in the `books` list. It then returns the updated book as a JSON response. If the book is not found, it returns an error message.
    
    The `delete_book()` function deletes a book by its ID from the `books` list. If the book is found and deleted, it returns a success message. If the book is not found, it returns an error message.
    
    Finally, if the script is run directly (not imported as a module), the Flask app runs in debug mode on port 5000.
    
    Note that this example uses a simple list to store the books. In a real-world application, you would likely use a database instead. However, the basic structure of the Flask app and CRUD operations would remain the same.
    
- Persisting data in flask [CRUD application using postgresql db].
    
    here's a step-by-step guide to data persistence in Flask without using any ORM:
    
    Flask CRUD application using psycopg2 to connect to a PostgreSQL database.
    
    First, make sure you have installed Flask and psycopg2 libraries. You can install them via pip:
    
    ```
    
    pip install Flask psycopg2
    
    ```
    
    Next, create a new Python file named [app.py](http://app.py/) and import the necessary libraries:
    
    ```
    
    from flask import Flask, request, jsonify
    import psycopg2
    
    ```
    
    Then, create an instance of Flask and set up the database connection:
    
    ```
    
    app = Flask(__name__)
    conn = psycopg2.connect(database="mydatabase", user="myuser", password="mypassword", host="localhost", port="5432")
    
    ```
    
    Replace "mydatabase", "myuser", "mypassword", "localhost", and "5432" with your own PostgreSQL database information.
    
    After that, define the CRUD endpoints for your application. Here's an example of an endpoint to retrieve all records from a table:
    
    ```
    
    @app.route('/records', methods=['GET'])
    def get_records():
        cur = conn.cursor()
        cur.execute("SELECT * FROM mytable")
        rows = cur.fetchall()
        cur.close()
        return jsonify(rows)
    
    ```
    
    This endpoint executes a SELECT query on a table named "mytable" and returns all rows as a JSON response.
    
    Here's an example of an endpoint to create a new record:
    
    ```
    
    @app.route('/record', methods=['POST'])
    def create_record():
        data = request.get_json(force=True)
        cur = conn.cursor()
        cur.execute("INSERT INTO mytable (field1, field2, field3) VALUES (%s, %s, %s)", (data['field1'], data['field2'], data['field3']))
        conn.commit()
        cur.close()
        return jsonify({'message': 'Record created successfully'})
    
    ```
    
    This endpoint receives a JSON payload with data for the new record, inserts it into the "mytable" table, and returns a success message.
    
    Here's an example of an endpoint to update a record:
    
    ```
    
    @app.route('/record/<id>', methods=['PUT'])
    def update_record(id):
        data = request.get_json(force=True)
        cur = conn.cursor()
        cur.execute("UPDATE mytable SET field1 = %s, field2 = %s, field3 = %s WHERE id = %s", (data['field1'], data['field2'], data['field3'], id))
        conn.commit()
        cur.close()
        return jsonify({'message': 'Record updated successfully'})
    
    ```
    
    This endpoint receives an ID parameter in the URL, updates the corresponding record in the "mytable" table with the new data from the JSON payload, and returns a success message.
    
    Finally, here's an example of an endpoint to delete a record:
    
    ```
    
    @app.route('/record/<id>', methods=['DELETE'])
    def delete_record(id):
        cur = conn.cursor()
        cur.execute("DELETE FROM mytable WHERE id = %s", (id,))
        conn.commit()
        cur.close()
        return jsonify({'message': 'Record deleted successfully'})
    
    ```
    
    This endpoint receives an ID parameter in the URL, deletes the corresponding record from the "mytable" table, and returns a success message.
    
    That's it! You can run your Flask application by calling `app.run()` at the end of your file.
    
    <aside>
    💡 Using an ORM like SQLAlchemy can provide a more convenient and cleaner way to interact with databases in Flask applications.
    
    </aside>
    
- Persisting data with ORM
    
    ORM stands for Object-Relational Mapping, which is a technique used to map objects in an application to rows in a database table. This technique can simplify database operations by allowing developers to work with objects and classes rather than raw SQL queries.
    
    In Flask, one popular ORM is SQLAlchemy, which provides a high-level API for interacting with databases using Python code. Here's an example of how to use SQLAlchemy in a Flask app:
    
    First, you need to install the `flask_sqlalchemy` library using pip:
    
    ```
    
    pip install flask_sqlalchemy
    
    ```
    
    Next, you can create a new Flask app and configure the database connection using SQLAlchemy:
    
    ```
    
    from flask import Flask
    from flask_sqlalchemy import SQLAlchemy
    
    app = Flask(__name__)
    app.config['SQLALCHEMY_DATABASE_URI'] = 'postgresql://user:password@localhost/mydatabase'
    db = SQLAlchemy(app)
    
    ```
    
    In this example, we're using a PostgreSQL database with credentials "user" and "password", hosted on the local machine. Replace these values with your own database connection details.
    
    Next, you can define a class that represents a table in your database using SQLAlchemy's declarative syntax:
    
    ```
    
    class Book(db.Model):
        id = db.Column(db.Integer, primary_key=True)
        title = db.Column(db.String(80), unique=True, nullable=False)
        author = db.Column(db.String(120), nullable=False)
        year = db.Column(db.Integer, nullable=False)
    
    ```
    
    In this example, we're defining a `Book` class with three attributes: `title`, `author`, and `year`, which correspond to columns in a table in our database. The `id` attribute is a primary key column, which is automatically generated by SQLAlchemy.
    
    With the `Book` class defined, we can now use it to interact with the database. Here's an example of how to use SQLAlchemy to perform CRUD (Create, Read, Update, Delete) operations:
    
    ```
    
    # Create a new book
    book = Book(title='FullStack Development', author='Praveen Kumar', year=2023)
    db.session.add(book)
    db.session.commit()
    
    # Retrieve all books
    books = Book.query.all()
    
    # Retrieve a single book by ID
    book = Book.query.get(1)
    
    # Update a book
    book.title = 'FullStack Development with Flask'
    db.session.commit()
    
    # Delete a book
    db.session.delete(book)
    db.session.commit()
    
    ```
    
    In this example, we first create a new `Book` object and add it to the database using `db.session.add()` and `db.session.commit()`. We then retrieve all books using `Book.query.all()`, retrieve a single book by ID using `Book.query.get(1)`, update a book's title using normal Python attribute assignment and then commit using `db.session.commit()`, and finally delete a book using `db.session.delete()` and `db.session.commit()`.
    
    That's how you can use SQLAlchemy ORM in a Flask app!
    
- Project-1Small bookstore application
    
    I can provide an example implementation of the Flask application for the online bookstore, but please keep in mind that this is not a complete or functional implementation. It's just meant to give you an idea of how the different components fit together.
    
    Here's what `__init__.py` might look like:
    
    ```
    
    from flask import Flask
    from flask_sqlalchemy import SQLAlchemy
    from flask_migrate import Migrate
    from flask_login import LoginManager
    
    app = Flask(__name__)
    app.config.from_object('config')
    db = SQLAlchemy(app)
    migrate = Migrate(app, db)
    
    login_manager = LoginManager()
    login_manager.init_app(app)
    login_manager.login_view = 'login'
    
    from . import views, models
    
    ```
    
    In this file, we create the Flask application object and configure it using the settings in `config.py`. We also create a `SQLAlchemy` object to handle database interactions, as well as a `Migrate` object to handle database migrations. Finally, we create a `LoginManager` object to handle user authentication.
    
    Next, here's an example implementation of `models.py`:
    
    ```
    
    from . import db
    from flask_login import UserMixin
    
    class Book(db.Model):
        id = db.Column(db.Integer, primary_key=True)
        title = db.Column(db.String(255))
        author = db.Column(db.String(255))
        price = db.Column(db.Float)
    
    class User(UserMixin, db.Model):
        id = db.Column(db.Integer, primary_key=True)
        email = db.Column(db.String(255), unique=True)
        password = db.Column(db.String(255))
    
    ```
    
    In this file, we define two models: `Book` and `User`. The `Book` model represents a book in the online store, with columns for the title, author, and price. The `User` model represents a registered user of the website, with columns for the email and hashed password.
    
    Next, here's an example implementation of `views.py`:
    
    ```
    
    from flask import render_template, redirect, url_for
    from flask_login import login_required, login_user, logout_user
    from . import app, db
    from .models import Book, User
    
    @app.route('/')
    def home():
        books = Book.query.all()
        return render_template('home.html', books=books)
    
    @app.route('/login', methods=['GET', 'POST'])
    def login():
        if request.method == 'POST':
            email = request.form['email']
            password = request.form['password']
            user = User.query.filter_by(email=email).first()
            if user is not None and user.check_password(password):
                login_user(user)
                return redirect(url_for('home'))
            flash('Invalid email or password.')
        return render_template('login.html')
    
    @app.route('/logout')
    @login_required
    def logout():
        logout_user()
        return redirect(url_for('home'))
    
    @app.route('/register', methods=['GET', 'POST'])
    def register():
        if request.method == 'POST':
            email = request.form['email']
            password = request.form['password']
            confirm_password = request.form['confirm_password']
            if password != confirm_password:
                flash('Passwords do not match.')
                return redirect(url_for('register'))
            user = User(email=email, password=User.hash_password(password))
            db.session.add(user)
            db.session.commit()
            login_user(user)
            return redirect(url_for('home'))
        return render_template('register.html')
    
    ```
    
    In this file, we define several Flask routes that handle incoming requests. The `home` route displays a list of all the books in the online store. The `login`, `logout`, and `register` routes handle user authentication and registration.
    
    Finally, here's an example `config.py` file:
    
    ```
    
    import os
    
    basedir = os.path.abspath(os.path.dirname(__file__))
    
    SQLALCHEMY_DATABASE_URI = 'sqlite:///' + os.path.join(basedir, 'app.db')
    SECRET_KEY = 'replace_this_with_a_random_string'
    
    ```
    
    In this file, we define the database URI and a secret key for the Flask application.
    
    <aside>
    💡 Again, please keep in mind that this is just an example implementation of a Flask application for an online bookstore. You would need to implement additional functionality, security measures, and error handling to make it production-ready
    
    </aside>
    
- Assignment-1
    
    Make the previous bookstore application production ready by following the given steps below:
    
    Let's say you are building a web application for an online bookstore that allows users to browse and purchase books. Here are some important considerations for making the Flask application production-ready:
    
    1. Scalability: The application should be designed in a way that it can handle a large number of requests and traffic. You can use tools like Gunicorn or uWSGI to run multiple worker processes in parallel.
    2. Security: The application should be secure against common web application attacks such as SQL injection and cross-site scripting. You can use Flask-Security to handle user authentication and authorization, and Flask-WTF to protect against CSRF attacks.
    3. Database: You need a database to store book information and user data. Flask supports a wide range of databases through SQLAlchemy, including PostgreSQL, MySQL, and SQLite.
    4. Testing: It's important to test the application thoroughly before deploying it to production. You can use Python's built-in unittest module or a third-party testing framework like pytest.
    5. Deployment: Once the application is ready to be deployed, you need to choose a hosting provider that supports Flask applications. Some popular options include Heroku, Amazon Web Services, and Google Cloud Platform.
    
    Here's an example of how you might structure your Flask application:
    
    ```
    Copy Code
    bookstore/
       __init__.py
       models.py
       views.py
       templates/
          base.html
          home.html
          login.html
          register.html
          ...
       static/
          css/
             main.css
          js/
             main.js
       config.py
       requirements.txt
    
    ```
    
    In this example, `__init__.py` initializes the Flask application and sets up the database. `models.py` defines the database schema using SQLAlchemy. `views.py` contains the Flask routes that handle incoming requests. The `templates` folder contains Jinja2 templates that render the HTML pages, and the `static` folder contains static assets like CSS and JavaScript.
    
    The `config.py` file contains configuration options for the Flask application, such as the database URL and secret key. The `requirements.txt` file lists all the Python packages required by the application, so they can be installed with a single command.
    
    With these components in place, you can create a production-ready Flask application for your online bookstore.
    
- Project-2: URL shortening application using flask
    
    Follow the below steps to develop a mini url shortening application 
    
    1. Install Flask:
    You can install Flask using pip, which is a package manager for Python. Open your terminal and run the following command:
        
        ```
        Copy Code
        pip install Flask
        
        ```
        
    2. Create a new Flask application:
    Create a new Python file, and import the Flask module. Then, create a new instance of the Flask class:
        
        ```
        Copy Code
        from flask import Flask
        
        app = Flask(__name__)
        
        ```
        
    3. Define a route for the homepage:
    In Flask, routes are mapped to specific functions that handle requests. Define a route for the homepage by using the `@app.route()` decorator:
        
        ```
        Copy Code
        @app.route('/')
        def home():
            return 'Welcome to my URL shortener!'
        
        ```
        
    4. Define a route for creating short URLs:
    In order to create short URLs, you'll need to define a route that accepts a long URL and returns a shortened version of it. You can use the `@app.route()` decorator again to define this route:
        
        ```
        Copy Code
        @app.route('/shorten/<url>')
        def shorten(url):
        # Code for generating a short URL goes herereturn 'Shortened URL will be displayed here'
        
        ```
        
    5. Implement a function for generating short URLs:
    There are different ways to generate short URLs, but one common approach is to use a hash function to convert the long URL into a unique short code. Here's an example implementation using the built-in hashlib module:
        
        ```
        Copy Code
        import hashlib
        
        def generate_short_code(url):
            md5 = hashlib.md5()
            md5.update(url.encode('utf-8'))
            return md5.hexdigest()[:6]
        
        ```
        
    6. Store the short URL in a database:
    When a user requests a short URL, you'll need to store the mapping between the short code and the long URL in a database. You can use SQLite or another lightweight database for this purpose:
        
        ```
        Copy Code
        import sqlite3
        
        conn = sqlite3.connect('urls.db')
        cursor = conn.cursor()
        
        cursor.execute('''CREATE TABLE IF NOT EXISTS urls
                          (short_code TEXT PRIMARY KEY, long_url TEXT)''')
        conn.commit()
        
        def save_url(short_code, long_url):
            cursor.execute('''INSERT INTO urls (short_code, long_url)
                              VALUES (?, ?)''', (short_code, long_url))
            conn.commit()
        
        ```
        
    7. Update the `shorten()` function to generate and store short URLs:
    Now that you have the necessary components, you can update the `shorten()` function to generate a short URL and store it in the database:
        
        ```
        Copy Code
        @app.route('/shorten/<url>')
        def shorten(url):
            short_code = generate_short_code(url)
            save_url(short_code, url)
            short_url = f'http://localhost:5000/{short_code}'
            return f'Shortened URL: {short_url}'
        
        ```
        
    8. Define a route for redirecting short URLs:
    Finally, you need to define a route that redirects users from the short URL to the corresponding long URL. You can use the `@app.route()` decorator again to define this route:
        
        ```
        Copy Code
        @app.route('/<short_code>')
        def redirect(short_code):
            cursor.execute('''SELECT long_url FROM urls WHERE short_code = ?''', (short_code,))
            row = cursor.fetchone()
            if row is None:
                return 'Short URL not found'
            else:
                long_url = row[0]
                return redirect(long_url, code=302)
        
        ```
        
    
    That's it! With these steps, you should have a working URL shortener application using Flask.
    
- Assignment-2
    
    Here is a step-by-step process to develop a portfolio application using Flask and Bootstrap and deploy it on DigitalOcean:
    
    1. Set up a development environment:
        - Install Python and pip
        - Install Flask and required packages using pip
        - Install a code editor like Visual Studio Code or PyCharm
    2. Create a new Flask project:
        - Create a new directory for the project
        - Create a virtual environment for the project
        - Initialize a new Flask application
    3. Design the website:
        - Choose a design for the website
        - Create HTML templates for each page of the website
        - Use Bootstrap to style the website
    4. Implement the views:
        - Create functions for each page of the website in the Flask application
        - Render the HTML templates in each function
    5. Add dynamic content:
        - Connect to a database (e.g. SQLite) to store data for the website
        - Create models to represent the data
        - Implement CRUD operations to manipulate the data
    6. Test the website:
        - Run the Flask application to test the website locally
        - Make sure all pages are working correctly
        - Check if the database is behaving as expected
    7. Deploy the website:
        - Create an account on DigitalOcean
        - Create a new Droplet (server) on DigitalOcean
        - Log in to the server using SSH
        - Install necessary packages (e.g. Python, pip, Git)
        - Clone the project from GitHub onto the server
        - Install required packages using pip
        - Configure the server to run the Flask application using Gunicorn and Nginx
    8. Test the deployed website:
        - Visit the IP address of the server in a web browser
        - Make sure the website is running correctly
        - Test all functionality of the website
    
    With these steps, you can develop a portfolio application using Flask and Bootstrap and deploy it on DigitalOcean.

- [Contact us for real time software development trainings, in-house internships, corporate trainings & team building 
Email: kumarpraveen3299@gmail.com  | mobile: +916261501868
]