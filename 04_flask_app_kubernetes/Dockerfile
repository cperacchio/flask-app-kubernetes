# python runtime
FROM python:stretch

# copy current directory into the container
COPY . /app

# working directory
WORKDIR /app

# install requirements
RUN pip install --upgrade pip
RUN pip3 install -r requirements.txt

# make port 8000 available to the world outside
# EXPOSE 8000

ENTRYPOINT ["gunicorn", "-b", ":8080", "main:APP"]