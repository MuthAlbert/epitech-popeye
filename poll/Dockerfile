FROM python:lastest

WORKDIR /poll

COPY requirements.txt .

RUN pip3 install -r requirements.txt

COPY . .

EXPOSE 80

CMD flask run --host=0.0.0.0 --port=80