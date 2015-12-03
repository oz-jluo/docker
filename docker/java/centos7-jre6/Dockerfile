# This dockerfile uses the centos7 image
# VERSION 1 - EDITION 1
# Author: Rojer
# Command format: Instruction [arguments / command] ..

FROM cmcagile/centos7

MAINTAINER Rojer <rojer@ozstrategy.com>

# Define the JAVA Version
ENV JAVA_MAJOR_VERSION 6
ENV JAVA_BUILD_VERSION 6u45-b06
ENV JAVA_MINOR_VERSION 45

# install jre then remove the rpm
RUN wget --no-check-certificate --no-cookies --header 'Cookie: oraclelicense=accept-securebackup-cookie' http://download.oracle.com/otn-pub/java/jdk/${JAVA_BUILD_VERSION}/jre-${JAVA_MAJOR_VERSION}u${JAVA_MINOR_VERSION}-linux-x64-rpm.bin

RUN chmod +x jre-${JAVA_MAJOR_VERSION}u${JAVA_MINOR_VERSION}-linux-x64-rpm.bin
RUN ./jre-${JAVA_MAJOR_VERSION}u${JAVA_MINOR_VERSION}-linux-x64-rpm.bin && rm jre-${JAVA_MAJOR_VERSION}u${JAVA_MINOR_VERSION}-linux-x64-rpm.bin

# set JAVA_HOME
ENV JAVA_HOME /usr/java/jre1.${JAVA_MAJOR_VERSION}.0_${JAVA_MINOR_VERSION}

ENV PATH $PATH:$JAVA_HOME/bin

# Define default command.
CMD ["bash"]
