# 🎂 Cake E-commerce API

A RESTful API for a cake e-commerce platform built with **Python, Django, and Django REST Framework (DRF)**. This backend powers an online cake shop where customers can explore products, manage their shopping carts, and place orders.

The API is designed to work with a React-based frontend and provides backend functionality for product management, user authentication, shipping addresses, and order processing.

## ✨ Features

- **Product Management** — Retrieve and manage cake products and product information.
- **User Authentication** — User registration, authentication, and account management.
- **Shopping Cart** — Support for shopping cart operations.
- **Checkout System** — Process checkout requests and validate order information.
- **Shipping Addresses** — Manage customer shipping and delivery details.
- **Order Management** — Create and manage customer orders.
- **Cash on Delivery** — Support for cash-on-delivery orders.
- **Django Admin Panel** — Manage application data through Django's administration interface.
- **RESTful API** — Exchange data between the backend and frontend using HTTP requests.
- **Media Support** — Store and serve product images during development.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Backend programming language |
| Django | Web framework |
| Django REST Framework | REST API development |
| Djoser / JWT authentication | User authentication |
| SQLite or configured database | Data storage |
| React | Frontend integration |
| Git & GitHub | Version control |

*The actual database and authentication configuration depend on the project's settings.*

## 📂 Project Structure

```text
Ecommerce-Cake-API/
├── api/                  # API endpoints and related logic
├── ecommarce_app/        # E-commerce application
├── ecommarce_project/    # Django project configuration
├── user/                 # User-related functionality
├── media/                # Uploaded media files
├── staticfiles/          # Collected static files
├── templates/            # HTML templates
├── build.sh              # Build script
├── manage.py             # Django management utility
├── requirements.txt      # Python dependencies
└── README.md
```

## 🚀 Getting Started

Follow these steps to run the project locally.

### 1. Prerequisites

Make sure you have installed:

- Python 3.10 or a compatible version for the project's dependencies
- pip
- Git
- A terminal or command-line interface

### 2. Clone the repository

```bash
git clone https://github.com/md-saim850/Ecommerce-Cake-API.git
```

Navigate to the project directory:

```bash
cd Ecommerce-Cake-API
```

### 3. Create a virtual environment

```bash
python3 -m venv venv
```

Activate the environment on Linux or macOS:

```bash
source venv/bin/activate
```

On Windows:

```bash
venv\Scripts\activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

### 5. Configure environment variables

If the project requires environment variables, create a `.env` file in the project root and configure the values expected by the Django settings.

For example:

```env
SECRET_KEY=your-secret-key
DEBUG=True
```

Configure your database and any other required settings according to the project's configuration. Never commit real secrets or production credentials to GitHub.

### 6. Apply database migrations

```bash
python manage.py migrate
```

### 7. Create a superuser

```bash
python manage.py createsuperuser
```

Follow the prompts to create your administrator account.

### 8. Run the development server

```bash
python manage.py runserver
```

The API server should now be available at:

**http://127.0.0.1:8000/**

If API routes are configured under a prefix, use the corresponding route from the project's URL configuration.

### 9. Access Django Admin

Open the following URL in your browser:

http://127.0.0.1:8000/admin/

Log in with your superuser credentials to access the administration panel.

## 🔌 API Functionality

The backend supports the main operations needed by a cake e-commerce application.

| Module | Functionality |
|---|---|
| Products | Browse product listings and retrieve product details |
| Authentication | Register and authenticate users |
| Cart | Manage shopping cart items |
| Shipping | Manage delivery addresses |
| Checkout | Submit checkout information |
| Orders | Create and manage customer orders |

### Example API Request

Use `curl`, Postman, or another API client to test an endpoint.

```bash
curl http://127.0.0.1:8000/
```

The exact API routes, HTTP methods, required request fields, and authentication requirements are defined in the project's URL configuration and views.

## 🔗 Frontend Integration

This backend is intended to work with a React-based cake shopping website.

The frontend can communicate with the API using `fetch` or Axios.

Example using JavaScript:

```javascript
const response = await fetch(
  "http://127.0.0.1:8000/api/"
);

if (!response.ok) {
  throw new Error("Failed to fetch data");
}

const data = await response.json();
console.log(data);
```

Replace the example URL with the actual endpoint configured in the project.

For cross-origin requests, configure Django's CORS settings to allow requests from your frontend origin.

## 🔒 Security Considerations

- Keep secret keys and database credentials in environment variables.
- Set `DEBUG=False` in production.
- Configure `ALLOWED_HOSTS` for your deployed domain.
- Restrict CORS to trusted frontend origins.
- Use HTTPS in production.
- Protect private endpoints with the appropriate authentication and permissions.
- Do not commit `.env` files containing secrets.

## 🧪 Testing

Run the Django test suite with:

```bash
python manage.py test
```

You can also test API endpoints using Postman or the Django REST Framework browsable API, if enabled.

## 🚀 Deployment

The application can be deployed to a Python-compatible hosting platform.

Before deploying:

1. Configure production environment variables.
2. Set `DEBUG=False`.
3. Configure the production database and allowed hosts.
4. Install dependencies from `requirements.txt`.
5. Apply database migrations.
6. Configure static and media file handling.
7. Use a production WSGI server such as Gunicorn, if supported by the project configuration.

## 🎯 Project Purpose

This project demonstrates backend development skills, including REST API design, database operations, authentication, shopping cart functionality, checkout workflows, and order management for an e-commerce application.

## 👨‍💻 Author

**MD. Saim**

- GitHub: [@md-saim850](https://github.com/md-saim850)
- Repository: [Ecommerce-Cake-API](https://github.com/md-saim850/Ecommerce-Cake-API)

---

⭐ If you find this project useful, consider giving the repository a star!

