ARG TOMCAT_VERSION
FROM tomcat:${TOMCAT_VERSION}

ARG TZ
ARG TOMCAT_JAVA_OPTS
ARG DEBIAN_REPOSITORIES_REPLACE

RUN cd /home

COPY source /var/local/source

#使用$(nproc)在mac下会出现错误，现在还找不到解决方法，下面的数值是你的cpu核数，linux环境可以直接用
ENV MC="-j2"
ENV TOMCAT_JAVA_OPTS=${TOMCAT_JAVA_OPTS}

WORKDIR /app/webapps
