ALX Travel App
==============

ALX Travel App is a Django-based web application designed to manage and showcase travel listings. The project is equipped with a RESTful API, MySQL database integration, and comprehensive API documentation using Swagger.

---

Features
--------
- RESTful API for managing travel listings.
- MySQL database configuration using `django-environ` for secure credential management.
- API documentation with Swagger, accessible at `/swagger/`.
- CORS support for seamless integration with frontend applications.
- Configurable task queuing with Celery and RabbitMQ.

---

Requirements
------------
Ensure the following are installed on your system before running the project:
- Python 3.8+
- Django 4.0+
- MySQL 8.0+
- RabbitMQ (for Celery tasks)
- Virtualenv (optional but recommended)

---

Setup Instructions
------------------

1. Clone the repository:
   ```bash
   git clone https://github.com/shanzaog/alx_travel_app.git
   cd alx_travel_app
   ```
   
2. Create a Virtual Environment
    ```bash
   python -m venv venv source venv/bin/activate # Linux/Mac 
   python -m venv\Scripts\activate # Windows
   ```
3. Install Dependencies
    ```bash
   pip install -r requirements.txt
   ```
4. Set Up the Database
- Create a MySQL database for the project.
- Configure the database credentials in the `.env` file.

Example `.env` file:
    DB_NAME=your_database_name 
    DB_USER=your_database_user 
    DB_PASSWORD=your_database_password 
    DB_HOST=localhost 
    DB_PORT=3306

5. Apply Migrations
    ```bash
   python manage.py makemigrations python manage.py migrate
   ```
6. Run the Server
    ```bash
   python manage.py runserver
   ```
   

Access the application at `http://127.0.0.1:8000/`.

---

API Documentation
-----------------
API documentation is automatically generated using Swagger (via **drf-yasg**). Access it at:
- Swagger UI: `http://127.0.0.1:8000/swagger/`

---

Project Structure
-----------------
The project is organized as follows:
```
├── alx_travel_app/         # Root Django project folder
│   ├── __init__.py         # Package initialization
│   ├── asgi.py             # ASGI configuration
│   ├── settings.py         # Main project settings
│   ├── urls.py             # URL configurations
│   └── wsgi.py             # WSGI configuration
├── listings/               # App-specific folder
│   ├── migrations/         # Database migration files
│   ├── __init__.py         # Package initialization
│   ├── admin.py            # Admin panel configuration
│   ├── apps.py             # Application configuration
│   ├── models.py           # Data models
│   ├── serializers.py      # API serializers
│   ├── tests.py            # Test cases
│   └── views.py            # API views
├── seed.py                 # Core script for database and data management
├── main.py                 # Script to execute the workflow
├── user_data.csv           # Input data file
├── requirements.txt        # Project dependencies
├── .env                    # Environment variables (not included in the repo)
└── README.md               # Project documentation

```

Technologies Used
-----------------
- Backend: Django, Django REST Framework
- Database: MySQL
- Task Queue: Celery, RabbitMQ
- API Documentation: Swagger (drf-yasg)

---

Contributing
------------
Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature-name`).
5. Open a pull request.

---

License
-------
This project is licensed under the MIT License.

---

Author
------
Developed by Shanza Allan.  
Feel free to reach out at allanshanza@gmail.com.

