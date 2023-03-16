FROM python:3@sha256:0d753a7365274cef746b34dde9b4aaa27644f64e1567ed8f40ccd191ac4bd530
WORKDIR /usr/src/app
COPY requirements.txt ./
RUN pip install -r requirements.txt
COPY . .
EXPOSE 80
CMD ["python", "./app.py"]
