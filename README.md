# Project Title
Simple try of FastAPI and python.



## Description
integrating with snapchat to collect user data.



## Goal
to build application with zero knowldge about python & FastAPI



## Installing:

### Requirement:
just install docker for running the app and python to develope


#### Install virtualenv if it is not installed
````
pip install virtualenv
````
#### Create a virtual environment
````
virtualenv venv
````
#### Activate the virtual environment
On Windows
````
venv\Scripts\activate
````
#### On MacOS/Linux
````
source venv/bin/activate
````

#### Installing packages: 
````
pip install -r requirements.txt
````


### Executing program:

#### How to run the program
build the docker image
```
docker build -t pyroject .
```

* run the docker image
```
docker run -p 8000:80 pyroject
```



## File structure goal: 
```
/pyroject
|-- /app
|   |-- __init__.py
|   |-- main.py          # Entry point of the FastAPI application
|   |-- /api             # API specific files
|   |   |-- __init__.py
|   |   |-- dependencies.py  # Dependencies for routes (e.g., database sessions)
|   |   |-- security.py      # Security and authentication (OAuth2, JWT)
|   |   |-- /v1              # Version 1 of the API
|   |       |-- __init__.py
|   |       |-- routes.py    # API routes for this version
|   |       |-- /endpoints   # Individual endpoints
|   |           |-- __init__.py
|   |           |-- user_data.py   # Endpoints for user data interactions
|   |           |-- ads_data.py    # Endpoints for ads data interactions
|   |-- /models          # Database models
|   |   |-- __init__.py
|   |   |-- base.py      # Base class for all models
|   |   |-- user.py      # User model
|   |   |-- ad_data.py   # Ad data model
|   |-- /schemas         # Pydantic schemas for request and response data types
|   |   |-- __init__.py
|   |   |-- user_schema.py
|   |   |-- ad_data_schema.py
|   |-- /services        # Business logic and service layer
|   |   |-- __init__.py
|   |   |-- user_service.py
|   |   |-- ad_service.py
|   |-- /core            # Core application configurations and utilities
|   |   |-- __init__.py
|   |   |-- config.py    # Configuration settings and environment variables
|   |   |-- database.py  # Database session management and utilities
|   |-- /tests           # Test modules
|       |-- __init__.py
|       |-- test_main.py
|       |-- /api         # Tests for API endpoints
|           |-- __init__.py
|           |-- test_user_data.py
|           |-- test_ads_data.py
|-- /migrations         # Alembic migrations
|   |-- env.py
|   |-- script.py.mako
|   |-- versions
|-- docker-compose.yml  # Docker compose file for local development
|-- Dockerfile          # Dockerfile for building the FastAPI application
|-- requirements.txt    # Project dependencies
|-- README.md           # Project README file
```
