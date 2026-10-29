# DevOps Assignment 2 - Personal Portfolio

**Student:** Aima Perveen  
**Roll number:** FA23-BAI-066  
**Course:** DevOps for Cloud Computing (Lab)

A two-file HTML/CSS personal portfolio served by Nginx in Docker.
The `feature-endpoint` branch adds the mandatory Labs section.
GitHub Actions checks the files, builds the image for pull requests,
and publishes `latest` to Docker Hub only for pushes to `main`.

## Run locally
```bash
docker build -t devops-a2:local .
docker run -d -p 8080:80 --name devops-a2-page devops-a2:local
```
Visit http://localhost:8080.

## Required Docker Hub tags
- `YOUR_DOCKERHUB_USERNAME/devops-a2:manual`: local manual build/push
- `YOUR_DOCKERHUB_USERNAME/devops-a2:latest`: published by GitHub Actions

## Note
Configure `DOCKERHUB_USERNAME` and `DOCKERHUB_TOKEN` as repository Actions secrets.
See `../STEP_BY_STEP_INSTRUCTIONS.md` in the downloaded package.
