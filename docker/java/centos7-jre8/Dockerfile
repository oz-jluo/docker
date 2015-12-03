# This dockerfile uses the centos7 image
# VERSION 1 - EDITION 1
# Author: Rojer
# Command format: Instruction [arguments / command] ..

FROM cmcagile/centos7

MAINTAINER Rojer <rojer@ozstrategy.com>

# Define the JAVA Version
ENV JAVA_MAJOR_VERSION 8
ENV JAVA_BUILD_VERSION 8u66-b17
ENV JAVA_MINOR_VERSION 66

# install jre then remove the rpm
RUN wget --no-check-certificate --no-cookies --header 'Cookie: oraclelicense=accept-securebackup-cookie'\
 http://download.oracle.com/otn-pub/java/jdk/${JAVA_BUILD_VERSION}/server-jre-${JAVA_MAJOR_VERSION}u${JAVA_MINOR_VERSION}-linux-x64.tar.gz

RUN tar zxf server-jre-${JAVA_MAJOR_VERSION}u${JAVA_MINOR_VERSION}-linux-x64.tar.gz\
    && mkdir -p /usr/java/\
    && mv jdk1.${JAVA_MAJOR_VERSION}.0_${JAVA_MINOR_VERSION}/ /usr/java/\
    && rm server-jre-${JAVA_MAJOR_VERSION}u${JAVA_MINOR_VERSION}-linux-x64.tar.gz

# set JAVA_HOME
ENV JAVA_HOME /usr/java/jdk1.${JAVA_MAJOR_VERSION}.0_${JAVA_MINOR_VERSION}

ENV PATH $PATH:$JAVA_HOME/bin

# Define default command.
CMD ["bash"]