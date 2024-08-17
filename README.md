# ML Pipeline Implementation and Deployment

## Project Overview
This project focuses on building and deploying a machine learning pipeline to predict travel time. The project involves comprehensive data preprocessing, exploratory data analysis (EDA), and training an XGBoost model that achieved an R2 score of 0.92. The pipeline was managed using CI/CD practices with Git and DVC, and the application was containerized with Docker. Finally, the container was deployed on AWS EC2 using ECR, AWS CLI, and the workflow was automated with GitHub Actions.

## Features
- **Data Preprocessing and EDA**: Performed thorough data preprocessing and exploratory data analysis to prepare the dataset.
- **Model Training**: Trained an XGBoost model to predict travel time, achieving an R2 score of 0.92.
- **CI/CD Pipeline**: Built and managed a CI/CD pipeline using Git, DVC, and Docker.
- **Containerization**: Containerized the application using Docker, making it portable and scalable.
- **Deployment**: Deployed the Docker container on AWS EC2 using ECR and AWS CLI, and automated the workflow using GitHub Actions.

## Files in the Repository
- **.dockerignore**: Specifies files and directories to be ignored when building the Docker image.
- **.dvcignore**: Specifies files and directories to be ignored by DVC (Data Version Control).
- **.gitignore**: Specifies files and directories to be ignored by Git.
- **Dockerfile**: Defines the Docker image, including the base image and dependencies required for the application.
- **LICENSE**: The license file for the project.
- **Makefile**: Automates tasks such as building the Docker image, running tests, and deploying the application.
- **README.md**: Documentation file describing the project.
- **app.py**: The main application script that runs the ML model and serves predictions.
- **ci_cd_demo.py**: Demonstrates the CI/CD process, including steps for integration and deployment.
- **compose.yaml**: Defines services, networks, and volumes used in the Docker Compose setup.
- **data_models.py**: Contains data models and schema definitions used in the application.
- **dvc.lock**: Auto-generated file by DVC to lock the pipeline stages and dependencies.
- **dvc.yaml**: Defines the data pipeline stages and dependencies managed by DVC.
- **params.yaml**: Configuration file that stores hyperparameters and other parameters used in the pipeline.
- **requirements-actions.txt**: Lists Python dependencies required for GitHub Actions.
- **requirements-dev.txt**: Lists Python dependencies required for development.
- **requirements.txt**: Lists Python dependencies required to run the application.
- **setup.py**: Script for setting up the Python package, including metadata and dependencies.
- **test_environment.py**: Script for testing the environment setup, ensuring all dependencies are correctly installed.
- **tox.ini**: Configuration file for Tox, used for testing in different environments.

## Getting Started
### Prerequisites
- **Python 3.x**: Required to run the scripts.
- **Docker**: Required to build and run the containerized application.
- **AWS CLI**: Required for deploying the container to AWS EC2.
- **DVC**: Required for managing the data version control pipeline.

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/ml-pipeline-deployment.git
pip install -r requirements.txt

docker build -t travel-time-predictor .

docker run -p 5000:5000 travel-time-predictor

Deploying to AWS EC2
Push the Docker image to Amazon ECR
aws ecr create-repository --repository-name travel-time-predictor
docker tag travel-time-predictor:latest <aws-account-id>.dkr.ecr.<region>.amazonaws.com/travel-time-predictor:latest
docker push <aws-account-id>.dkr.ecr.<region>.amazonaws.com/travel-time-predictor:latest
Automating with GitHub Actions

The CI/CD pipeline is automated using GitHub Actions, ensuring that every commit triggers tests, builds the Docker image, and deploys it to AWS EC2.

#Project Timeline
Duration: July 2024 - August 2024
