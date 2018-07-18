FROM centos:latest

MAINTAINER jz_1106@163.com

ADD jdk-8u181-linux-x64.tar.gz /usr/local/ 
ADD apache-tomcat-8.5.32.tar.gz /usr/local/ 
#ADD tomcat-users.xml /usr/local/apache-tomcat-8.5.32/conf/tomcat-users.xml
# configuration of java and tomcat ENV 
ENV JAVA_HOME /usr/local/jdk1.8.0_181 
ENV CLASSPATH $JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
ENV CATALINA_HOME /usr/local/apache-tomcat-8.5.32
ENV CATALINA_BASE /usr/local/apache-tomcat-8.5.32
ENV PATH $PATH:$JAVA_HOME/bin:$CATALINA_HOME/lib:$CATALINA_HOME/bin
# container listener port
EXPOSE 8080
# startup web application services by self 
CMD /usr/local/apache-tomcat-8.5.32/bin/catalina.sh run