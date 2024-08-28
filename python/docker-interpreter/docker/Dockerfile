ARG PYTHON_VERSION=3.9

FROM python:${PYTHON_VERSION}-slim-buster

COPY ../requirements.txt ./

LABEL maintainer=loustler<dev.loustler@gmail.com>

RUN apt-get update -y

RUN pip install -r ./requirements.txt \
  && rm -f ./requirements.txt