FROM python:3.14.4-alpine3.23

WORKDIR /app
COPY /Phase_I/app/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY /Phase_I/app /app

CMD ["flask","run","--host=0.0.0.0"]