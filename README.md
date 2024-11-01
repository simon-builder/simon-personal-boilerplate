This README.md is a journaling of noteworthy stuff i came across that i want to use in the future

```
docker-compose up --build
```

# Step-by-step when cloning project

clone repo

```
clone https://github/[REPO URL]
```

git separate branch (optional but recommended)

```
git checkout -b your-branch-name
````

make changes and add

```
git add .
```

commit changes

```
git commit -m "Your commit message here
```

pull latest changes

```
git pull origin main
```

push branch

```
git push origin your-branch-name
```

create pull request on github (web) and merge

create .env file (if needed)

create venv

```Windows
py -3 -m venv .venv
```

```MacOS
python3 -m venv .venv
```

start venv

```
.\.venv\Scripts\Activate.ps1
```

```
source .venv/bin/activate
```

install dependencies

```
pip install -r requirements.txt
```

## MongoDB connection




# Generate secret key:

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
