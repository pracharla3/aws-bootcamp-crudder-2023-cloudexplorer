FROM python:3.10-slim-buster

#make a new folder inside the container and set the curent working directory
WORKDIR /backend-flask

# this contains the libraries want to install to run the app
COPY requirements.txt requirements.txt

# Install py libraries used for the app
RUN pip3 install -r requirements.txt

# . means everything in the current directory
# first period everything outside the container
# second period is everything inside the container
COPY . .

#set env var these set the inside the container and will remain set when the container is running
ENV FLASK_ENV=development

EXPOSE ${PORT}

# Commnad to run flask
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]