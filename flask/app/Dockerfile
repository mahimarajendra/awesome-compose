FROM python:3.11 AS builder
MAINTAINER mahima
WORKDIR /app
COPY requirements.txt /app
RUN pip3 install -r requirements.txt
COPY . /app/

FROM python:3.11-slim
COPY --from=builder /app /app
ENTRYPOINT ['python']
CMD ['app.py']
