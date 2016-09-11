FROM python:2.7
MAINTAINER Aidan Smith
ENV REFRESHED_AT 2016-08-30

ADD . /flask

WORKDIR /flask

RUN pip install -r requirements.txt

RUN uwsgi --build-plugin https://github.com/unbit/uwsgi-consul

ENTRYPOINT [ "uwsgi", "--ini", "uwsgi-consul.ini", "--ini", "uwsgi-consul.ini:server1"]
CMD []
