# pull official base image
FROM python:3.9.5-slim-buster

# set work directory
WORKDIR /usr/src/app

# set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# install dependencies
COPY ./requirements.txt /usr/src/app/requirements.txt
RUN apt-get update && \ 
  apt-get install gcc python3-dev libpq-dev netcat -y bash && \
  pip install --upgrade pip && \ 
  pip install -r requirements.txt

# copy project
COPY . /usr/src/app/

# run entrypoint.sh
ENTRYPOINT ["/usr/src/app/entrypoint.sh"]