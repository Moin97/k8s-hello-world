FROM python:3.7.3-alpine3.9 as base

RUN mkdir /work
WORKDIR /work/

COPY ./src/requirements.txt /work/requirements.txt
RUN pip install -r requirements.txt

COPY ./src/ /work/

ENV FLASK_APP=server.py


CMD flask run -h 0.0.0.0 -p 5000

