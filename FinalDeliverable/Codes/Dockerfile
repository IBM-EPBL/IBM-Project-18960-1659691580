FROM python:3-alpine3.15
WORKDIR /app
RUN apk add gcc libc-dev
RUN pip install --upgrade setuptools
RUN pip install --upgrade pip
RUN pip install ibm-db
RUN pip install flask
RUN apk update
RUN apk add make automake gcc g++ subversion python3-dev
COPY . /app
RUN pip install -r requirements.txt
EXPOSE 3000
CMD python ./main.py