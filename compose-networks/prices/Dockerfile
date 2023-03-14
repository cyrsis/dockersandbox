FROM python:latest@sha256:1db68f83ca0d2735aeb804708cbc2b7be573ff4c236b2bbfa220bbac81512bb8
WORKDIR app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY . .
EXPOSE 80
CMD ["python", "app.py"]
