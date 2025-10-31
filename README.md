# FastAPI Calculator CI Project

This is a project for Python for Web API Development to demonstrate a CI/CD pipeline for a simple FastAPI calculator application.
It includes:
* A FastAPI application with basic arithmetic operations.
* Logging for all endpoints.
* Unit, Integration, and End-to-End (Playwright) tests.
* A GitHub Actions workflow to automate testing.
* A Docker Compose setup to run the app with PostgreSQL and pgAdmin.

---

## 🐳 How to Run with Docker

This is the easiest way to run the full application stack, including the database.

1.  Make sure you have Docker Desktop running.
2.  Clone this repository.
3.  From the project's root directory, run:
    ```bash
    docker-compose up --build
    ```
4.  The application will be running at **`http://127.0.0.1:8000`**.
5.  pgAdmin (database manager) will be available at **`http://127.0.0.1:5050`**.

---

## 🐍 How to Run Locally (Original Setup)

This method runs the app directly on your machine using a Python virtual environment.

1.  Clone the repository:
    ```bash
    git clone <YOUR_REPO_URL_HERE>
    cd fastapi-calculator-ci
    ```
2.  Create and activate a virtual environment:
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```
3.  Install dependencies:
    ```bash
    pip install -r requirements.txt
    playwright install
    ```
4.  Run the application:
    ```bash
    uvicorn app.main:app --reload
    ```
5.  The application will be running at **`http://127.0.0.1:8000`**.

---

## 🧪 How to Run Tests

### Run Unit and Integration Tests

These tests do not require the application to be running.

```bash
pytest tests/test_unit.py tests/test_integration.py