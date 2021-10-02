# Set a Python base image
FROM python:2.7

# Expose application port
EXPOSE 3111

# Copying files from the working directory to container filesystem
COPY ./techtrends /app

# Desired working directory within the container
WORKDIR /app

# Install packages defined in the requirements.txt file
RUN pip install -r requirements.txt

# Ensuring the database is initialized with the pre-defined posts in the init_db.py file
RUN python init_db.py

# Application should run on container start
CMD ["python", "app.py"]