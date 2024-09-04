# Spotify Recommender with FastAPI Integration

This project features a recommendation algorithm designed to suggest Spotify music and artists. The algorithm leverages an unsupervised K-Nearest Neighbors (KNN) approach, predicting the nearest neighbors of each song to provide similar recommendations upon request.

## Project Overview

### Objective
The aim is to develop a proof-of-concept (PoC) that integrates machine learning with FastAPI, offering real-time music recommendations through an API.

### Key Features
- **Recommendation Algorithm**: Utilizes KNN for predicting and suggesting similar songs and artists.
- **API Integration**: FastAPI framework is used to build and deploy endpoints for interacting with the recommendation model.
- **Deployment**: Uvicorn is used for deploying the FastAPI application.

## Team
**Argnauts without JSON**

## Tools & Technologies
- **Machine Learning**: K-Nearest Neighbors (KNN)
- **Framework**: FastAPI
- **Deployment**: Uvicorn

## Model Overview

This project showcases a complete machine learning pipeline, demonstrating how to automate end-to-end ML/AI workflows. The pipeline includes tasks such as data sanity checks, unit testing, model training on various compute targets, model version management, evaluation and selection, and deployment as a real-time web service. Staged deployment to QA/Prod environments, as well as integration and functional testing, are also included.

## Project Structure

```bash
├── LICENSE
├── MANIFEST
├── README.md
├── docs
│   ├── DOCS.md
│   ├── authorize.png
│   ├── sample_payload.json     # Sample payload for frontend testing
│   └── sample_payload.png
├── fastapi_skeleton            # FastAPI skeleton module
│   ├── __init__.py             
│   ├── api                     # API related code
│   │   ├── __init__.py
│   │   └── routes              # API routes
│   │       ├── __init__.py
│   │       ├── heartbeat.py    # Route for server heartbeat
│   │       ├── playlist.py     # Route for playlist recommendation
│   │       └── router.py       # Main router serving all routes
│   ├── core
│   │   ├── __init__.py
│   │   ├── config.py           # Server configuration
│   │   ├── event_handlers.py   # Server start/stop handlers
│   │   ├── messages.py         # Shared messages/resources
│   │   └── security.py         # Security helpers
│   ├── main.py                 # App entry point
│   ├── models
│   │   ├── __init__.py
│   │   ├── heartbeat.py        # Data model for heartbeat response
│   │   ├── payload.py          # Data model for ML model payload
│   │   └── playlist.py         # Data model for playlist recommendations
│   └── services
│       ├── __init__.py      
│       └── models.py           # Service layer for ML model
├── requirements.txt            # Project dependencies
├── sample_model                # Sample ML model folder
│   ├── Models                  # Model binaries
│   └── Utils                   # Utilities for data processing
│       ├── scaler.py           # Data manipulation and scaling
│       └── split_data.py       # Data splitting utilities
│   ├── interference.py         # Inference scripts
│   ├── poc.py                  # Proof of concept (to be removed)
│   └── train.py                # Model training scripts
├── setup.py                    # Python setup script
├── tests                       # Testing framework
│   ├── __init__.py
│   ├── conftest.py             # Test configuration/bootstrap
│   ├── test_api                # API test cases
│   │   ├── __init__.py 
│   │   ├── test_api_auth.py    # API authentication tests
│   │   ├── test_heartbeat.py   # Heartbeat endpoint tests
│   │   └── test_playlist.py    # Playlist recommendation tests
│   └── test_service
│       ├── __init__.py       
│       └── test_models.py      # ML model tests
└── tox.ini                     # Tox configuration for testing

FastAPI Integration

	•	Authentication: The app uses token-based authentication, with tokens stored in a .env file.
	•	Endpoints:
	•	GET /heartbeat: Check if the server is running.
	•	POST /playlist: Get playlist recommendations based on input data.