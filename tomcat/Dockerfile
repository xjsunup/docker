# Pull base image
FROM  java:8

MAINTAINER xjsun "sxjjio@163.com"

VOLUME /tmp

# 添加
ADD target/tomcat-0.0.1-SNAPSHOT.jar app.jar

RUN bash -c 'touch /app.jar'

# Define default command.
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]

#设置时区
RUN /bin/cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo 'Asia/Shanghai' >/etc/timezone