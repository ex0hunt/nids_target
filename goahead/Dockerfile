FROM debian:9
RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y build-essential
RUN apt-get install -y git-core
RUN cd /
RUN git clone https://github.com/embedthis/goahead.git
WORKDIR /goahead
RUN make && make install
RUN cp /goahead/src/self.key /etc/goahead
RUN cp /goahead/src/self.crt /etc/goahead
CMD goahead -v --home /etc/goahead /var/www/