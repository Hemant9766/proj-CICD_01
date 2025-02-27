FROM python:3

# Install dependencies including distutils and python3-dev
RUN apt-get update && apt-get install -y python3-distutils python3-dev

# Install Django
RUN pip install django==3.2

# Copy the application files
COPY . .

# Run migrations
RUN python manage.py migrate
