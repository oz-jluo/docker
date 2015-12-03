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

# install jdk then remove the rpm
RUN wget --no-check-certificate --no-cookies --header 'Cookie: oraclelicense=accept-securebackup-cookie' http://download.oracle.com/otn-pub/java/jdk/${JAVA_BUILD_VERSION}/jdk-${JAVA_MAJOR_VERSION}u${JAVA_MINOR_VERSION}-linux-x64.rpm

RUN rpm -ivh jdk-${JAVA_MAJOR_VERSION}u${JAVA_MINOR_VERSION}-linux-x64.rpm && rm jdk-${JAVA_MAJOR_VERSION}u${JAVA_MINOR_VERSION}-linux-x64.rpm

# set JAVA_HOME
ENV JAVA_HOME /usr/java/jdk1.${JAVA_MAJOR_VERSION}.0_${JAVA_MINOR_VERSION}

ENV PATH $PATH:$JAVA_HOME/bin

# Define default command.
CMD ["bash"]