FROM python:3.9

COPY requirements.txt .
COPY devops .

RUN apt-get update && apt-get install -y python3 python3-pip python3-venv tzdata

SHELL ["/bin/bash", "-c"]

RUN python3 -m venv venv1 && \
source venv1/bin/activate && \
pip install --no-cache-dir -r requirements.txt

EXPOSE 8000

CMD source venv1/bin/activate && python3 manage.py runserver 0.0.0.0:8000




