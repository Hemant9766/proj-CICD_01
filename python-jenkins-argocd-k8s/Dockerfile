FROM python:3

# Install dependencies
RUN apt-get update && apt-get install -y python3-distutils

# Install Python dependencies from requirements.txt
COPY requirements.txt .
RUN pip install -r requirements.txt

# Copy the application files
COPY . .

# Run migrations
RUN python manage.py migrate
