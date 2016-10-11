FROM python:2.7
ENV PYTHONUNBUFFERED 1
RUN apt-get install libmysqlclient-dev
RUN mkdir /app
WORKDIR /app
ADD requirements.txt /app/
RUN pip install -r requirements.txt
ADD . /app/