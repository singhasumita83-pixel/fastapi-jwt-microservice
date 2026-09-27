# FastAPI / Flask Microservice with JWT Authentication

A beginner-friendly REST API built with **FastAPI**, **SQLite**, **SQLAlchemy**, **Pydantic**, **bcrypt**, and **JWT authentication**.

## Features

- User registration
- User login
- Password hashing with bcrypt
- JWT Bearer token authentication
- Pydantic request validation
- Secure CRUD operations for items
- SQLite database persistence
- Interactive Swagger/OpenAPI documentation at `/docs`

## Project Structure

```text
fastapi-jwt-microservice/
├── app/
│   ├── __init__.py
│   └── main.py
├── postman/
│   └── FastAPI-JWT-Microservice.postman_collection.json
├── requirements.txt
├── .gitignore
└── README.md
```

## Run Locally

### 1. Open the project folder

```bash
cd fastapi-jwt-microservice
```

### 2. Create a virtual environment

Windows:

```bash
python -m venv venv
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Start the API

```bash
uvicorn app.main:app --reload
```

### 5. Open Swagger

Open:

```text
http://127.0.0.1:8000/docs
```

## API Flow

1. Use `POST /register` to create a user.
2. Use `POST /login` to get a JWT token.
3. Click **Authorize** in Swagger.
4. Enter:

```text
Bearer YOUR_TOKEN
```

5. Test the protected `/items` CRUD endpoints.

## Main Endpoints

| Method | Endpoint | Authentication |
|---|---|---|
| GET | `/` | No |
| POST | `/register` | No |
| POST | `/login` | No |
| GET | `/items` | JWT |
| POST | `/items` | JWT |
| GET | `/items/{item_id}` | JWT |
| PUT | `/items/{item_id}` | JWT |
| DELETE | `/items/{item_id}` | JWT |

## Expected Proof

For submission, include:

- Public GitHub repository containing the source code
- Screenshot of Swagger `/docs`
- Screenshot showing an authenticated CRUD request
- Postman collection file in the repository

## Important

This project is suitable for a learning/demo submission. For production use, store the JWT secret in an environment variable and use a production database such as PostgreSQL.
