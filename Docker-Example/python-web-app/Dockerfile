FROM ubuntu
WORKDIR /app
COPY requirements.txt /app/
COPY devops /app/

RUN apt-get update && apt-get install -y python3 python3-pip python3-venv

SHELL["/bin/bash", "-c"]

RUN python3 -m venv ven1 && \
source ven1/bin/activate && \
pip install --no-cache-dir -r requirements.txt 
EXPOSE 8000
CMD source ven1/bin/activate && python3 manage.py runserver 0.0.0.0:8000