# REST API Collection Documentation

### 1. GET /api/v1/restaurants
* **Description:** Retrieve operational restaurants list.
* **Expected Response:** `200 OK` | **Status:** Not Executed

### 2. POST /api/v1/auth/login
* **Description:** Authenticate user and issue JWT token.
* **Request Body:**
  ```json
  {
    "email": "standard.user@foodore.test",
    "password": "P@ssword2026!"
  }
