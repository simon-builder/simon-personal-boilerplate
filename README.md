Generate secret key:

``openssl rand -base64 32``

# How to start a new FARM Stack Project

## Create project structure

```
/<root project folder>
    /backend
    /frontend
```

## Create virtual environment in backend

- Navigate to backend folder
- Create a virtual env

``py -3 -m venv .venv`` (Windows)
``python3 -m venv .venv`` (Mac)

## Install FASTAPI and other packages

- Install any packages you need for your project with

``pip install FastAPI[Standard] <other packages>``

Run venv
``.\venv\Scripts\Activate.ps1`` (Win)
``source venv/bin/activate`` (Mac)
