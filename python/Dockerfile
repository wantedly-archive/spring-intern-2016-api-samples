FROM python:2.7.10-slim

WORKDIR /app
COPY . /app/
RUN pip install tornado
RUN pip install requests

EXPOSE 8080

CMD ["script/server"]
