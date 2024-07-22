FROM mysql:5.7.44

RUN yum update -y --disablerepo mysql-tools-community &&\
    yum install -y --enablerepo ol7_optional_latest python3-pip python3-devel gcc wget &&\
    wget https://repo.mysql.com/yum/mysql-5.7-community/el/7/x86_64/mysql-community-devel-5.7.44-1.el7.x86_64.rpm &&\
    wget https://repo.mysql.com/yum/mysql-5.7-community/el/7/x86_64/mysql-community-libs-5.7.44-1.el7.x86_64.rpm &&\
    wget https://repo.mysql.com/yum/mysql-5.7-community/el/7/x86_64/mysql-community-common-5.7.44-1.el7.x86_64.rpm &&\
    cp /usr/bin/mysql_config /usr/bin/mysql_config.bak &&\
    rpm -i --replacefiles mysql-community-devel-5.7.44-1.el7.x86_64.rpm mysql-community-libs-5.7.44-1.el7.x86_64.rpm mysql-community-common-5.7.44-1.el7.x86_64.rpm &&\
    mv /usr/bin/mysql_config.bak /usr/bin/mysql_config &&\
    rm mysql-community-devel-5.7.44-1.el7.x86_64.rpm mysql-community-libs-5.7.44-1.el7.x86_64.rpm mysql-community-common-5.7.44-1.el7.x86_64.rpm &&\
    yum clean all &&\
    pip3 install mysqlclient PyMySQL
