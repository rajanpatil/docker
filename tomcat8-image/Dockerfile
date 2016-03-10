# Author: Rajan Patil
# This is ubuntu image with tomcat8 web server
FROM ubuntu:14.04
MAINTAINER rajan patil <rajan.rb@gmail.com>
RUN apt-get update
RUN apt-get install -y wget
RUN wget http://mirrors.ibiblio.org/apache/tomcat/tomcat-8/v8.0.32/bin/apache-tomcat-8.0.32.tar.gz
RUN tar xvzf apache-tomcat-8.0.32.tar.gz
RUN mv apache-tomcat-8.0.32 /opt/tomcat
RUN apt-get -y install default-jdk
RUN touch ~/.bashrc
RUN echo "export JAVA_HOME=/usr/lib/jvm/default-java" >> ~/.bashrc
RUN echo "export CATALINA_HOME=/opt/tomcat" >> ~/.bashrc
CMD /opt/tomcat/bin/startup.sh && sleep 5 && tail -f /opt/tomcat/logs/*.log
EXPOSE 8080