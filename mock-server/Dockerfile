# Really minimal Python 3 image
FROM frolvlad/alpine-python3

MAINTAINER juan.arias@schibsted.com

ADD requirements.txt .
RUN pip3 install -r requirements.txt

ADD app.py .

EXPOSE 5000

ENV FLASK_PORT=5000
ENV FLASK_APP=app.py
CMD ["flask", "run", "--host=0.0.0.0"]
