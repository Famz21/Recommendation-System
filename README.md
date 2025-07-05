# Anime Recommendation System - MLOps Project

A machine learning-based recommendation system for anime, implemented with MLOps best practices for continuous integration, deployment, and monitoring.

## Project Overview

This project implements a hybrid recommendation system that combines user-based collaborative filtering and content-based filtering to suggest anime titles to users. The system is built with a focus on MLOps practices, including:

- Containerization with Docker
- CI/CD pipeline with Jenkins
- Data version control with DVC
- Model training and serving pipelines
- Web interface for recommendations

## Project Structure

```
├── ALL_Project_2/               # Additional project files and resources
├── artifacts/                  # Model artifacts and outputs
├── config/                     # Configuration files
├── custom_jenkins/             # Custom Jenkins configuration
├── logs/                       # Application logs
├── notebook/                   # Jupyter notebooks for exploration
├── pipeline/                   # ML pipelines
│   ├── prediction_pipeline.py  # Prediction pipeline for recommendations
│   └── training_pipeline.py    # Training pipeline for model development
├── src/                        # Source code
├── static/                     # Static web assets
├── templates/                  # HTML templates
├── utils/                      # Utility functions
├── application.py              # Flask web application
├── Dockerfile                  # Docker configuration
├── Jenkinsfile                 # Jenkins pipeline definition
├── requirements.txt            # Python dependencies
├── setup.py                    # Package setup configuration
└── tester.py                   # Testing script
```

## Features

- Hybrid recommendation system combining:
  - User-based collaborative filtering
  - Content-based filtering
- Web interface for entering user ID and receiving recommendations
- Containerized deployment with Docker
- Automated CI/CD pipeline with Jenkins

## Technologies Used

- **Python**: Core programming language
- **Flask**: Web framework
- **TensorFlow**: Machine learning framework
- **Pandas & NumPy**: Data processing
- **DVC**: Data version control
- **Docker**: Containerization
- **Jenkins**: CI/CD automation
- **Google Cloud Storage**: Cloud storage integration

## Getting Started

### Prerequisites

- Python 3.8+
- Docker
- Jenkins (optional, for CI/CD)

### Installation

1. Clone the repository
   ```bash
   git clone https://github.com/Famz21/Recommendation-System.git
   cd Recommendation-System
   ```

2. Create and activate a virtual environment
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies
   ```bash
   pip install -e .
   ```

### Running the Application

#### Using Python directly

```bash
python application.py
```

The application will be available at http://localhost:5000

#### Using Docker

```bash
docker build -t anime-recommendation-system .
docker run -p 5000:5000 anime-recommendation-system
```

## MLOps Pipeline

### Data Processing

The data processing pipeline handles:
- Loading anime and user data
- Preprocessing and feature engineering
- Preparing data for model training

### Model Training

The training pipeline:
- Builds and trains recommendation models
- Evaluates model performance
- Saves model artifacts

### Prediction

The prediction pipeline:
- Loads trained models
- Combines user-based and content-based recommendations
- Returns top anime recommendations for a given user

### CI/CD with Jenkins

The project includes a Jenkinsfile that defines the CI/CD pipeline:
- Clones the repository
- Sets up a virtual environment
- Installs dependencies
- Runs tests
- Builds and deploys the Docker container

## Usage

1. Open the web interface at http://localhost:5000
2. Enter a user ID in the form
3. Submit to receive personalized anime recommendations

## License

[Include license information here]

## Contributors

[Include contributor information here]
