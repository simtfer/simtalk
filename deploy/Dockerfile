FROM python:3.7

ENV PYTHONUNBUFFERED 1
ENV SIMTALK_PROFILE product

COPY ./config/sources.list /etc/apt/
RUN apt-get update
RUN apt-get install python3-dev default-libmysqlclient-dev -y

RUN mkdir /code
WORKDIR /code

COPY ./config/requirements.txt ./deploy/config/
RUN pip install -i https://mirrors.aliyun.com/pypi/simple/ -r ./deploy/config/requirements.txt

EXPOSE 8080
