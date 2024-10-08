
   ![run_app](https://github.com/user-attachments/assets/f00a276d-480e-4657-b370-8fdfae651814)
    


<h1>Flask Authentication System</h1>

<p>A basic user authentication system using Flask, SQLAlchemy, and Flask-Login. This system allows users to register, log in, and log out securely. It also includes password hashing for security using Flask-Bcrypt.</p>

<h2>Features</h2>
<ul>
    <li><strong>User Registration</strong>: Allows new users to register an account with a unique username and hashed password.</li>
    <li><strong>User Login</strong>: Users can log in with their username and password.</li>
    <li><strong>Authentication</strong>: Protects routes that require users to be logged in.</li>
    <li><strong>Flash Messages</strong>: Flash messages are displayed for user feedback (e.g., successful login, registration errors).</li>
    <li><strong>Password Hashing</strong>: Passwords are hashed for security using Flask-Bcrypt.</li>
    <li><strong>Session Management</strong>: Users can log in, stay authenticated during the session, and log out.</li>
</ul>

<h2>Technologies Used</h2>
<ul>
    <li><strong>Flask</strong>: A micro web framework for Python.</li>
    <li><strong>Flask-SQLAlchemy</strong>: ORM to handle the database.</li>
    <li><strong>Flask-Bcrypt</strong>: To hash passwords for security.</li>
    <li><strong>Flask-Login</strong>: User session management.</li>
    <li><strong>SQLite</strong>: Database used for storing user credentials.</li>
</ul>

<h2>Prerequisites</h2>
<ul>
    <li>Python 3.7+</li>
    <li>pip (Python package manager)</li>
</ul>

<h2>Installation</h2>
<ol>
    <li>Clone the repository:</li>
    <pre><code>git clone https://github.com/your-username/flask-authentication-system.git
cd flask-authentication-system</code></pre>

    <li>Create a virtual environment and activate it:</li>
    <pre><code>python -m venv venv
source venv/bin/activate  # For Windows use: venv\Scripts\activate</code></pre>

    <li>Install the required packages:</li>
    <pre><code>pip install -r requirements.txt</code></pre>

    <li>Initialize the database:</li>
    <pre><code>python
&gt;&gt;&gt; from backend import db
&gt;&gt;&gt; db.create_all()
&gt;&gt;&gt; exit()</code></pre>

    <li>Run the Flask application:</li>
    <pre><code>python backend.py</code></pre>

    <li>Visit <a href="http://127.0.0.1:5000/">http://127.0.0.1:5000/</a> in your browser to see the application in action.</li>
</ol>

<h2>Project Structure</h2>
<pre><code>flask-authentication-system/
│
├── backend.py          # Main Flask application
├── templates/          # HTML templates for rendering the pages
│   ├── login.html
│   ├── register.html
│   └── home.html
├── static/             # Static files (CSS, JS, images)
├── database.db         # SQLite database (created after running the app)
├── README.md           # Project documentation
└── requirements.txt    # Python dependencies
</code></pre>

<h2>Routes</h2>
<ul>
    <li><code>/register</code>: Register a new account.</li>
    <li><code>/</code>: Login to an existing account.</li>
    <li><code>/home</code>: User's homepage (requires login).</li>
    <li><code>/logout</code>: Logout from the current session.</li>
</ul>

<h2>Flash Messages</h2>
<p>Flash messages are used throughout the application to provide feedback to the user. They display messages like successful login, incorrect password, or registration errors.</p>

<h3>Example Flash Messages</h3>
<ul>
    <li><strong>Success</strong>: Green flash message for actions like successful registration or login.</li>
    <li><strong>Error</strong>: Red flash message for failed actions like login failure or duplicate registration.</li>
</ul>

<h2>License</h2>
<p>This project is licensed under the MIT License - see the <code>LICENSE</code> file for details.</p>

