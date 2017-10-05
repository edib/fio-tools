FROM ubuntu:16.04
MAINTAINER <Ryan Wallner ryan.wallner@clusterhq.com>

#RUN sed -i -e 's/archive.ubuntu.com/old-releases.ubuntu.com/g' /etc/apt/sources.list
RUN apt-get -y update && apt-get -y install fio gnuplot

# Add modified script to y axis is set accurately
ADD fio2gnuplot /usr/bin/fio2gnuplot
RUN chmod +x /usr/bin/fio2gnuplot

WORKDIR /tmp/fio-data
ENTRYPOINT ["/usr/bin/fio2gnuplot"]
