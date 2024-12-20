This README.md is a journaling of noteworthy stuff i came across that i want to use in the future

Create venv anaconda
```
conda create -n my-venv-name python=3.10 -y
```

# How to contribute to a repo

## Fork repo, clone repo to machine, create a separate branch and update files and push branch to your repo

1. fork repo
2. clone repo
```
git clone https://github.com/your-username/repo-name.git
```
3. create a new branch
```
git checkout -b update-readme
```
4. update files and commit files
```
git add .
git commit -m "message"
```
5. push to my fork
```
git push origin update-readme
```
6. open a pull request on the original repo and add desc

## Link fork to original repo
```
git remote add upstream https://github.com/original-owner/original-repo.git
git fetch upstream
git checkout main
git merge upstream/main
git push origin main
```

# general flow of ci cd pipeline with docker

cicd
1. setup triggers for ci
2. set env var if needed
3. two jobs (a) build (b) deploy
4. build
    a. build docker image of frontend and backend (use actions from github marketplace if avail)
    b. use a hub (docker hub, github registry/pkg) for private images
5. deploy
    a. call hooks on platform (or inftrastructure?)


# best practice for setting up docker in a full stack app

- Create Dockerfile in each backend and frontend folder
- Dockerfile general config flow
    - 1 install deps
    - 2 build the app (e.g. npm run dev or npm run build)
    - 3 copy files for the image (from prev step)
        - optionally, add and use a different user for more security
    - 4 expose port, ip and cmd


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
