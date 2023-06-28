FROM python:3.7.17-alpine

RUN apk update 
RUN pip install --upgrade pip
COPY requirements.txt /home/requirements.txt
COPY getData.py /home/getData.py
COPY config.py /home/config.py
COPY kafkaHelper.py /home/kafkaHelper.py
RUN pip install -r /home/requirements.txt
CMD ["/home/getData.py"]
ENTRYPOINT [ "python" ]