FROM ubuntu:latest

WORKDIR /app

COPY requirements.txt /app
COPY devops /app

RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    pip install -r requirements.txt && \
    cd devops

#ENTRYPOINT and CMD can be used as execute as your start command
#But ENTRYPOINT is cannot be changed, so they cannot override this inside docker image
#But CMD is configurable field, you can pass values.
ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]




