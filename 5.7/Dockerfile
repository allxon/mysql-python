FROM mysql:5.7.42-debian

RUN apt-get update || true &&\
    apt-get install -y python3-pip python3-dev default-libmysqlclient-dev build-essential &&\
    pip3 install mysqlclient PyMySQL
