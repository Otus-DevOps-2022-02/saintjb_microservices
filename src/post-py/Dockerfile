FROM python:3.6.0-alpine

WORKDIR /app
ADD . /app

RUN pip install --upgrade pip
RUN apk --no-cache --update add build-base gcc musl-dev && \
    pip install -r /app/requirements.txt && \
    apk del build-base

ENV POST_DATABASE_HOST post_db
ENV POST_DATABASE posts
CMD ["python3", "post_app.py"]
