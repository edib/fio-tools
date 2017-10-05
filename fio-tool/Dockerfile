FROM ubuntu:16.04
MAINTAINER <Ryan Wallner ryan.wallner@clusterhq.com>

#RUN sed -i -e 's/archive.ubuntu.com/old-releases.ubuntu.com/g' /etc/apt/sources.list
RUN apt-get -y update && apt-get -y install fio wget

VOLUME /tmp/fio-data
ADD run.sh /opt/run.sh
RUN chmod +x /opt/run.sh
WORKDIR /tmp/fio-data
CMD ["/opt/run.sh"] 
