# Minimal Django + Pytest + Jenkins example

This minimal example shows you how you can runs pytest on your Django app on every commit using GitHub WebHook.

## Installation

Follow these instructions to setup this demo out locally.
This requires Python 3 and the pip package manager.

```bash
# Create virtual environment
python -m venv env

# Activate virtual environment (Bash for Linux or Mac)
. env/bin/activate

# Activate virtual environment (cmd / PowerShell for Windows)
./env/Scripts/activate

# Install requirements
pip install -r requirements.txt
```

## Running tests

```bash
# Activate virtual environment (Bash for Linux or Mac)
. env/bin/activate

# Go into the Django application folder
cd app

# Run pytest
pytest -vv
```

## Running the server

```bash
# Activate virtual environment (Bash for Linux or Mac)
. env/bin/activate


# Go into the Django application folder
cd app

# Setup database.
./manage.py migrate

# Run the development server.
./manage.py runserver

# Now you can view the project at http://localhost:8000
```
## Adding Webhook in Github
Go to repository -> settings -> Webhook
