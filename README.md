# Proof / Submission Checklist

Before submitting the GitHub link:

1. Run the API with `uvicorn app.main:app --reload`.
2. Open `http://127.0.0.1:8000/docs`.
3. Take a screenshot showing the Swagger/OpenAPI endpoints.
4. Register and login to receive a JWT token.
5. Click **Authorize** and enter `Bearer YOUR_TOKEN`.
6. Create and read an item to show authenticated CRUD access.
7. Take a screenshot of the authenticated Swagger request/response.
8. Import `postman/FastAPI-JWT-Microservice.postman_collection.json` into Postman and test the endpoints.
9. If required by the platform, take a screenshot of the Postman collection/request.
