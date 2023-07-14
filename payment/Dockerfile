FROM python:3.9

EXPOSE 8080
USER root

ENV CART_HOST=cart \
    USER_HOST=user

WORKDIR /app

COPY requirements.txt /app/

RUN pip install -r requirements.txt

COPY *.py /app/
COPY payment.ini /app/

#CMD ["python", "payment.py"]
CMD ["uwsgi", "--ini", "payment.ini"]

