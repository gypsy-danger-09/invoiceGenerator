# Invoice Generator App

## How to Run

### Prerequisites

- Docker
- Docker Compose

### Steps

1. Clone the repository:

```bash
git clone https://github.com/gypsy-danger-09/invoice-generator-app.git
cd invoice-generator-app
```

2. Start the services:

```bash

docker-compose up --build
```

# Access the application:

Backend: http://localhost:3001

API Endpoints
User Login

    URL: /login
    Method: POST
    Body: { "email": "user@example.com", "password": "password" }
    Response: { "user": { ... }, "token": "..." }

User Registration

    URL: /register
    Method: POST
    Body: { "name": "User", "email": "user@example.com", "password": "password" }
    Response: { "user": { ... }, "token": "..." }

Add Products

    URL: /addProducts
    Method: POST
    Headers: { "Authorization": "Bearer <token>" }
    Body: { "products": [{ "name": "Product1", "qty": 2, "rate": 100 }] }
    Response: { "message": "Products added successfully", "pdfPath": "/path/to/pdf" }

View Quotations

    URL: /viewQuotations
    Method: GET
    Headers: { "Authorization": "Bearer <token>" }
    Response: [{ "_id": "...", "products": [...], "date": "...", "totalAmount": 200, "pdfPath": "/path/to/pdf" }]
