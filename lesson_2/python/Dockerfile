FROM python:3.7

RUN pip install flask

RUN mkdir app

RUN mkdir app/python

ADD https://raw.githubusercontent.com/adterskov/geekbrains-conteinerization/master/homework/2.docker/python/requirements.txt  /app/python

ADD https://raw.githubusercontent.com/adterskov/geekbrains-conteinerization/master/homework/2.docker/python/app.py  /app/python

ENTRYPOINT python /app/python/app.py runserver 0.0.0.0:8080