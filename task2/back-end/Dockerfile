FROM ubuntu:latest

RUN apt-get update
RUN apt-get upgrade -y

# Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# Fix externally managed error (if needed)
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask using pip
RUN pip3 install flask

# Set working directory
WORKDIR /app

# Copy the Python file into the container
COPY ./api.py /app/api.py

# Command to run when container starts
CMD ["python3", "api.py"]