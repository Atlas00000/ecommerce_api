# 📂 ecommerce_api

A simple E-commerce Product API built with Django and Django REST Framework, allowing CRUD operations for products and users, with search functionality by name or category.

---

## 🚀 Features

- Full CRUD operations for **Products**
- Search products by **name** or **category**
- Custom user model for flexibility
- Django admin for easy backend management
- RESTful API with pagination and filtering
- Ready for deployment on **Heroku** or **PythonAnywhere**

---

## 🛠 Tech Stack

- **Python 3.10+**
- **Django 5.2**
- **Django REST Framework**
- **SQLite** (Development database)
- **Gunicorn** (for production WSGI)
- **Heroku** / **PythonAnywhere** (Deployment)

---

## 📦 Requirements & Dependencies

Install dependencies with:

```bash
pip install -r requirements.txt
```

Example `requirements.txt` (partial):

```
Django==5.2
djangorestframework==3.15.1
gunicorn==21.2.0
```

---

## 📁 Folder Structure

```
ecommerce_api/
│
├── ecommerce_api/         # Django project settings
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
│
├── products/              # Product app
│   ├── models.py
│   ├── serializers.py
│   ├── views.py
│   └── admin.py
│
├── users/                 # Custom user app
│   ├── models.py
│   ├── admin.py
│   └── ...
│
├── db.sqlite3             # Local database (for development)
├── manage.py              # Django CLI
├── requirements.txt       # Python package dependencies
└── README.md              # This file
```

---

## 🔧 API Endpoints

| Method | Endpoint              | Description                    |
|--------|-----------------------|--------------------------------|
| GET    | `/api/products/`      | List all products              |
| POST   | `/api/products/`      | Create a new product           |
| GET    | `/api/products/:id/`  | Retrieve a specific product    |
| PUT    | `/api/products/:id/`  | Update a product               |
| DELETE | `/api/products/:id/`  | Delete a product               |
| GET    | `/api/products/?search=phone` | Search by name/category |

---

## 🧪 Running Locally

```bash
# Start the development server
python manage.py runserver

# Access the admin interface
http://127.0.0.1:8000/admin/
```

---

## 🔐 Superuser Login

```bash
python manage.py createsuperuser
# Follow prompts to create username, email, and password
```

---

## ☁️ Deployment (Heroku or PythonAnywhere)

1. Freeze requirements:
    ```bash
    pip freeze > requirements.txt
    ```

2. Add `Procfile` (Heroku only):
    ```
    web: gunicorn ecommerce_api.wsgi
    ```

3. Add `runtime.txt` (Heroku):
    ```
    python-3.10.13
    ```

4. Set `ALLOWED_HOSTS`, collect static files, and push to cloud.

---

## 🧑‍💼 Author

Built by [Celestine Emili](mailto:emilicelestine@gmail.com) — feel free to reach out!

---

## 📜 License

MIT License - feel free to use and modify for learning or production with credit.

