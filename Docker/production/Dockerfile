# Use a specific version of the Python image
FROM python:3.7-slim-buster

# Set the working directory
WORKDIR /app

# Add the Odoo source code into the container
ADD . /app

# Install build dependencies and Odoo requirements
RUN apt-get update && apt-get install -y python3-pip libldap2-dev libpq-dev libsasl2-dev python3-cffi
RUN pip install --no-cache-dir -r requirements.txt

# Run odoo.py when the container launches
CMD ["python", "odoo-bin", "-c", "run.conf"]
