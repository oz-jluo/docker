# This dockerfile uses the centos7 image
# VERSION 1 - EDITION 1
# Author: Rojer
# Command format: Instruction [arguments / command] ..

FROM centos:7

MAINTAINER Rojer <rojer@ozstrategy.com>

ENV container docker

# Set environment variables.
ENV HOME /root

# Define working directory.
WORKDIR /root

RUN yum -y update; yum clean all;
# Install soft
RUN yum install -y ca-certificates net-tools wget tar unzip

CMD ["/usr/sbin/init"]