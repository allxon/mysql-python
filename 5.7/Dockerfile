FROM mysql:5.7.44

RUN apt-get update &&\
    apt-get install -y python3-pip python3-dev default-libmysqlclient-dev build-essential &&\
    pip3 install mysqlclient PyMySQL
