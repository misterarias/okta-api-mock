# Really minimal Python 3 image
FROM frolvlad/alpine-python3

MAINTAINER juan.arias@schibsted.com

ADD requirements.txt .
RUN pip3 install -r requirements.txt

ADD app.py .

# If undefined, APP_PORT would be empty, and the app defaults to 5000 (and Debug mode)
CMD ["python3", "app.py", "$APP_PORT"]
