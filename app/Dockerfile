FROM --platform=linux/x86_64 python:3.7-slim AS build

WORKDIR /app
RUN groupadd -r webservice && useradd --no-log-init -r -g webservice webservice
COPY . .
RUN pip install -r requirements.txt

USER webservice:webservice

EXPOSE 8050
CMD ["python", "hello.py"]
