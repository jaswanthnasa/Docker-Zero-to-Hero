# Use an official Python runtime as a parent image
FROM python:3.11-slim

# Set the working directory in the container
WORKDIR /app

# Install dependencies
COPY requirements.txt /app/
COPY devops /app
RUN pip install --no-cache-dir -r requirements.txt && \
    cd devops

# Copy the rest of the application code
COPY . /app/


ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]

