# Online Store Web Application (Fullstack & CI/CD Pipeline)

A complex e-commerce web application built with Python (Django) and fully automated using Docker and GitHub Actions for continuous integration and deployment (CI/CD).

## 🛠 Tech Stack & Tools
- **Backend:** Python 3.11, Django 5.2, Gunicorn
- **Database:** PostgreSQL (`psycopg2-binary`)
- **Containerization:** Docker, Docker Compose
- **CI/CD Pipeline:** GitHub Actions
- **Deployment:** Heroku (`akhileshns/heroku-deploy`), Procfile
- **Testing:** Django Unit Tests (`unittest`)

## Key Features & Implementation
- **Fullstack E-commerce Architecture:** Catalog, shopping cart, checkout flow, user authentication, and a custom Admin Panel (`admin_panel`) for inventory management.
- **Docker Containerization:** Optimized lightweight multi-stage image (`python:3.11-slim`) and `docker-compose.yml` setup for local development and service orchestration.
- **Automated CI/CD Pipeline (`.github/workflows/deploy.yml`):**
  - **`build-and-test`:** Builds the Docker image and executes isolated unit tests (`python manage.py test`) inside the container on every `push` and `pull_request`.
  - **`automerge`:** Automatically merges Pull Requests to `main`/`master` upon successful test execution.
  - **`deploy`:** Automatically deploys the tested build to Heroku using GitHub Secrets for security.
