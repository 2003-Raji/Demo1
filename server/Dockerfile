FROM python:3-alpine3.15


COPY . .
RUN pip install -r requirements.txt
EXPOSE 5000

CMD gunicorn -w 4 -b 0.0.0.0:5000 app:app