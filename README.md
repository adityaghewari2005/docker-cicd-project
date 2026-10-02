Dockerized CI/CD Pipeline for Python REST API

description

Built a containerized Python Flask REST API with Docker and implemented a GitHub Actions CI/CD pipeline for automated testing, Docker image builds, and container health verification. Deployed and tested the application locally using Docker on Linux/WSL without relying on cloud infrastructure.



Understand your CI/CD pipeline

Your GitHub Actions pipeline now works like this:
             
             Git Push
                 │
                 ▼
        ┌─────────────────┐
        │ GitHub Actions  │
        └────────┬────────┘
                 │
                 ▼
          ┌─────────────┐
          │ Run pytest  │
          └──────┬──────┘
                 │
              PASS?
             /     \
           NO       YES
           │         │
           ▼         ▼
         STOP    Build Docker
                     │
                     ▼
               Run Container
                     │
                     ▼
               Health Check
                     │
                  PASS


