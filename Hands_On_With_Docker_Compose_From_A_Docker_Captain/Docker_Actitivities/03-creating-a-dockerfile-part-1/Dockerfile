FROM python:2.7-alpine

RUN mkdir /app
WORKDIR /app

COPY requirement.txt /app/requirement.txt
RUN pip install -r requirements.txt 

COPY . .

LABEL maintener="John Carl Sanico <john.johncarlsanico1998@gmail.com>"\
          version="1.0";

CMD flask run --host=0.0.0.0 --port=5000
