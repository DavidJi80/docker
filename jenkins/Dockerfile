FROM davidji80/tomcat:v1

MAINTAINER jz_1106@163.com

#Maven 安装配置
ADD apache-maven-3.5.4-bin.tar.gz /usr/local/
ADD settings.xml /usr/local/apache-maven-3.5.4/conf/
ENV M2_HOME /usr/local/apache-maven-3.5.4
ENV PATH $PATH:$M2_HOME/bin

#war安装jenkins
ADD jenkins.war /usr/local/apache-tomcat-8.5.32/webapps/

EXPOSE 8080
#启动Tomcat
CMD catalina.sh run