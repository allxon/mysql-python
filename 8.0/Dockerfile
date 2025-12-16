FROM public.ecr.aws/docker/library/mysql:8.0.44-debian

ENV MYSQL_ALLOW_EMPTY_PASSWORD=yes
ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y python3-pip python3-dev gcc wget libmysqlclient-dev python3-pymysql python3-mysqldb && \
    apt-get clean && rm -rf /var/lib/apt/lists/*