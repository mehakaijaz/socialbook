# SocialBook README

## Overview
SocialBook is a social interaction website designed to facilitate connections and interactions among users. The application leverages Django for backend functionality, including authentication, CRUD operations, and database interactions, using PostgreSQL as the database system.

## Features
- User authentication and authorization 
- CRUD operations for user posts and profiles
- Efficient database queries with Django ORM
- Responsive design for optimal user experience

## Technologies Used
### Backend
- **Django**: A high-level Python web framework that encourages rapid development and clean, pragmatic design.
- **PostgreSQL**: A powerful, open-source object-relational database system.

### Frontend
- **Bootstrap**: A popular CSS framework for developing responsive and mobile-first websites.
- **HTML**: The standard markup language for creating web pages.
- **CSS**: A stylesheet language used for describing the presentation of a document written in HTML.
- **JavaScript**: A programming language that enables interactive web pages.

## Installation and Setup

### Prerequisites
- Python 
- Django
- PostgreSQL

### Backend Setup
1. **Clone the repository:**
   ```sh
   git clone https://github.com/yourusername/socialbook.git
   cd socialbook
   ```


2. **Install the required Python packages:**
   ```sh
   pip install -r requirements.txt
   ```

3. **Set up PostgreSQL database:**
   Create a PostgreSQL database and configure it in the `settings.py` file.
   ```python
   DATABASES = {
       'default': {
           'ENGINE': 'django.db.backends.postgresql',
           'NAME': 'your_db_name',
           'USER': 'your_db_user',
           'PASSWORD': 'your_db_password',
           'HOST': 'localhost',
           'PORT': '5432',
       }
   }
   ```

4. **Apply database migrations:**
   ```sh
   python manage.py migrate
   ```

5. **Create a superuser to access the admin interface:**
   ```sh
   python manage.py createsuperuser
   ```

6. **Run the development server:**
   ```sh
   python manage.py runserver
   ```

### Frontend Setup
The frontend uses static files managed by Django. Ensure that the static files are correctly configured and collected.

1. **Collect static files:**
   ```sh
   python manage.py collectstatic
   ```

2. **Access the application:**
   Open your web browser and navigate to `http://localhost:8000` to start using SocialBook.

## Usage

### Authentication
- **Register**: Create a new account to start interacting with other users.
- **Login**: Access your account by logging in with your credentials.

### Social Interaction
- **Posts**: Create, read, update, and delete posts.
- **Profiles**: View and edit user profiles.

## Project Structure
- `socialbook/`: Main project directory.
  - `settings.py`: Configuration for the Django project.
  - `urls.py`: URL routing for the project.
  - `wsgi.py`: WSGI entry point for the application.
- `social/`: App directory containing the social interaction functionality.
  - `models.py`: Database models for the social application.
  - `urls.py`: URL routing for the social application.
  - `views.py`: Views for handling HTTP requests.
- `manage.py`: Command-line utility for administrative tasks.
- `templates`: HTML templates for rendering the frontend.
- `static/`: Static files (CSS, JavaScript, images).
- `media`: Uploaded files(images,vedioes)
