# URL Shortener

## Install the Project

1. Create a Python virtual environment

```sh
$ python -m venv venv
$ source venv/bin/activate
(venv) $
```

2. Install the requirements

```
(venv) $ python -m pip install -r requirements.txt
```

## Run the Project

You can run the project with this command in your terminal:

```sh
(venv) $ uvicorn shortener_app.main:app --reload
```


## Verify Your Environment Variables

The project provides default environment settings in [`shortener_app/config.py`](shortener_app/config.py).
While you can use the default settings, it's recommended to create a `.env` file to store your settings outside of your production code. E.g.:

```config
# .env
ENV_NAME="Development"
BASE_URL="http://url.shortener"
DB_URL="sqlite:///./test_database.db"
```
## Using Docker
Build the image using the docker command:
```sh
docker build -t image_name .
```
Run the image using the docker command:
```sh
docker run --network host image_name
```
(The add --network host is to share the same local host between the host and container is optional but recommended for ease of use).  

## The Documentation

When the project is running you can visit the documentation in your browser:

- http://127.0.0.1:8000/docs
- http://127.0.0.1:8000/redoc
