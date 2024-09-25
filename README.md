# Django Authentication App

This is a Django-based web application for user authentication, including features like user signup, login, logout, password reset, and profile management. The app is built using Django's authentication framework, along with additional integrations like `bootstrap4` and `crispy-forms` for enhanced UI.

## Features

- User Signup and Login
- Password Change and Password Reset
- Profile Management with Date Joined and Last Active Display
- Logout and Redirection to Login
- Bootstrap-styled forms using `crispy-forms`

## Prerequisites

Make sure you have the following installed:

- Python 3.x
- pip (Python package installer)
- Virtual environment (optional, but recommended)

## Setup Instructions

### Step 1: Clone the Repository

```bash
git clone https://github.com/yourusername/yourrepository.git
cd yourrepository

Step 2: Set Up Virtual Environment (Optional, but recommended)

Create a virtual environment to keep your project dependencies isolated.
python3 -m venv env
source env/bin/activate  # On Windows use `env\Scripts\activate`

Step 3: Install Dependencies
pip install django
pip install django-crispy-forms
pip install django-bootstrap4

Step 4: Add Bootstrap4 and Crispy Forms

You need to add the following to your Django settings:
# For Bootstrap4 integration
INSTALLED_APPS = [
    ...
    'bootstrap4',
    'crispy_forms',
    ...
]

# Crispy Forms Template Pack
CRISPY_TEMPLATE_PACK = 'bootstrap4'


Step 5: Apply Migrations
To set up the database and necessary tables, run the following commands:

python manage.py makemigrations
python manage.py migrate

Step 6: Create a Superuser (Optional)

To access the Django admin panel, you can create a superuser by running:
python manage.py createsuperuser

Follow the prompts to set up the username and password.
Step 7: Run the Development Server

To start the development server, run:
python manage.py runserver

Additional Configuration
{% load bootstrap4 %}
{% load crispy_forms_tags %}

URLs

    /signup/ - User signup page
    / - Login page
    /logout/ - Logout (redirects to login)
    /profile/ - User profile page (requires login)
    /password-reset/ - Password reset page
    /password-reset-success/ - Password reset success page (after successful reset)

yourrepository/
│
├── manage.py
├── auth_app/
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   ├── templates/
│   │   ├── base.html
│   │   ├── home.html
│   │   ├── login.html
│   │   ├── profile.html
│   │   ├── signup.html
│   │   ├── password_reset.html
│   │   ├── password_reset_complete.html
│   └── views.py
└── users/
    ├── forms.py
    ├── models.py
    └── views.py


Required Django Packages

Below is a list of all the required packages for this project:

    Django: The main web framework.
        Install using pip install django
    Django Crispy Forms: To style forms using Bootstrap.
        Install using pip install django-crispy-forms
    Django Bootstrap 4: For Bootstrap 4 support.
        Install using pip install django-bootstrap4

Notes

    This app requires bootstrap4 and crispy-forms for styling. Make sure these are installed and configured in settings.py.
    You can extend the project with additional features like email verification, two-factor authentication, etc.
