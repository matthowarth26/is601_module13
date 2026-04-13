
# FastAPI Calculator Application

This project includes a calculator API where users can perform operations such as add, subtract, multiply, and divide.

## Key Features
- Docker containerization
- PostgreSQL database integration
- Factory method for creating and instatiating calculcations
- User authentication with JWT
- Secure user model using SQLAlchemy ORM models and Pydantic schemas
- CI/CD pipeline with GitHub Actions and Docker Hub
- Security scanning with Trivy

---

## Docker Image

Docker Hub Repository

https://hub.docker.com/r/msh0626/601_module11
https://hub.docker.com/r/msh0626/601_module11/tags

---

## Project Installation

Clone the repository
```
git clone git@github.com:matthowarth26/is601_assignment11.git
cd is601_assignment10
```

git@github.com:matthowarth26/is601_assignment11.git
```
python3 -m venv venv
source venv/bin/activate
```

Install required packages
```
pip install -r requirements.txt
playwright install
```

Running the project locally
```
python main.py
```

Run with docker
```
docker compose up --build
```

Application URLs:
FastAPI:
```
http://localhost:8000
```

pgAdmin 
```
http://localhost:5050
```

## Running Tests Locally
Run all tests
```
pytest 
```

Run end-to-end tests
```
pytest tests/e2e/test_e2e.py -v
```

Run integration tests
```
pytest tests/integration/test_calculation_schema.py -v
pytest tests/integration/test_calculation.py -v
pytest tests/integration/test_fastapi_calculator.py -v
```

Run unit tests
```
pytest tests/unit/test_calculator.py -v
```

Run coverage report
```
pytest --cov=app
```

---

## CI/CD Information

GitHub Actions automatically runs tests and builds the Docker image.

GitHub Actions Workflow:
 - Checkout code using `actions/checkout`
 - Set up Python environment using `actions/setup-python`
 - Install dependencies from `requirements.txt`
 - Run unit tests
 - Run integration tests
 - Run end-to-end tests
 - Build Docker image 
 - Run security scan with Trivy
 - Push Docker Image to Docker Hub

Configuration File:
```
.github/workflows/test.yml
```
