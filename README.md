# Flask Blog Application

This project is a blog application built with Flask. It allows users to register, log in, create blog posts, and comment on posts. It also includes administrative functionalities for managing posts and comments.

## Features

- User registration and login
- Blog post creation, editing, and deletion (admin only)
- Commenting on blog posts
- Gravatar integration for user avatars
- CKEditor integration for rich text editing
- Responsive design with Flask-Bootstrap

## Requirements

- Python 3.x
- Flask
- Flask-Bootstrap
- Flask-CKEditor
- Flask-SQLAlchemy
- Flask-Login
- Flask-WTF
- Flask-Gravatar

## Installation



1. Set up your secret key and database URI in the configuration:

   ```python
   app.config['SECRET_KEY'] = 'your_secret_key'
   app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///blog.db'
   ```

2. Run the application:

   ```bash
   python main.py
   ```

## Usage

1. Register a new user.
2. Log in with the registered user.
3. Create new blog posts (admin only).
4. Comment on blog posts.

## Project Structure

- `main.py`: The main Flask application file.
- `templates/`: Contains the HTML templates for the application.
- `static/`: Contains static files such as CSS and JavaScript.
- `forms.py`: Contains the WTForms used in the application.
- `requirements.txt`: Lists the required Python packages.

## Application Routes

- `/`: Home page displaying all blog posts.
- `/register/`: User registration page.
- `/login/`: User login page.
- `/logout/`: User logout.
- `/post/<int:post_id>`: Page displaying a single blog post and its comments.
- `/about`: About page.
- `/contact`: Contact page.
- `/new-post/`: Page for creating a new blog post (admin only).
- `/edit-post/<int:post_id>`: Page for editing an existing blog post (admin only).
- `/delete/<int:post_id>`: Route for deleting a blog post (admin only).

## Admin User

To designate an admin user, ensure the user has an ID of 1 in the database. The `admin_only` decorator restricts certain actions to admin users.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
