FROM alpine:3.9

LABEL maintainer="adani.rotem@gmail.com"

RUN apk update && apk add python3 py3-pip

COPY requirements.txt /tmp/
RUN pip3 install -r /tmp/requirements.txt

COPY app.py /opt
WORKDIR /opt

EXPOSE 5000
ENTRYPOINT [ "python3" ]
CMD [ "app.py" ]