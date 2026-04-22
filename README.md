
# FastAPI Calculator Application

This project includes a calculator API and web interface where users can perform arithemtic operations such as add, subtract, multiply, and divide. The application includes user authentication and persists data using PostgreSQL. 

## Key Features
- Docker containerization
- PostgreSQL database integration
- Redis integration for JWT token blacklist 
- User authentication with JWT
- Secure user model using SQLAlchemy ORM models and Pydantic schemas  
- BREAD operations for calculations 
- Web UI using Jinja2 templates and static CSS
- CI/CD pipeline with GitHub Actions and Docker Hub
- Security scanning with Trivy 

## Web Page Interfaces
- Home: home page 
- Login: user login 
- Register: acount creation 
- Dashboard: perform calculations 

---

## Docker Image

Docker Hub Repository

https://hub.docker.com/r/msh0626/601_module13/tags

---

## Project Installation

Clone the repository
```
git clone git@github.com:matthowarth26/is601_assignment13.git
cd is601_assignment13
```

Initialize virtual environment
```
python3 -m venv venv
source venv/bin/activate
```

Install required packages
```
pip install -r requirements.txt
playwright install
```

Run the project locally with docker
```
docker compose up --build
```

Application URLs:
FastAPI:
```
http://localhost:8000
```

pgAdmin: 
```
http://localhost:5050
```

## Running Tests Locally
Start database container
```
docker compose up -d
```

Run all tests
```
pytest 
```

Run end-to-end tests
```
pytest tests/e2e -v
```

Run integration tests
```
pytest tests/integration -v
```

Run unit tests
```
pytest tests/unit -v
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
 - Generate coverage report 
 - Build Docker image 
 - Run security scan with Trivy
 - Push Docker Image to Docker Hub

Configuration File:
```
.github/workflows/test.yml
```
