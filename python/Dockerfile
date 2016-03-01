FROM python:2.7.10-slim

WORKDIR /app
COPY . /app/
RUN pip install -r packages_requirements.txt

EXPOSE 8080

CMD ["script/server"]
