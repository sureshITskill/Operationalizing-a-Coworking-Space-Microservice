# Linux Image OS  with Python to host the application. 
FROM python:3.9-slim-buster

# Setting up the the working directory in the Docker container 
WORKDIR /src

# Install the latest OS packages

CMD apt update -y

# Copy the requirements.txt file  to install requried Python packages.
COPY requirements.txt .

# Install packages and upgrade the flask. 
RUN pip install --upgrade pip && pip install -r requirements.txt && pip install --upgrade Flask Werkzeug

# COPY application data in the working directory

COPY . .

# start the application

CMD python app.py 
