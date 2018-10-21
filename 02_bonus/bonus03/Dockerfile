FROM ubuntu:latest
MAINTAINER Alex Krushinsky <akrushin@student.unit.ua>

RUN apt-get update -y && \
    apt-get upgrade -y && \
    apt-get install -y curl
ENV MY_URL https://www.kyivpost.com/
WORKDIR /data
VOLUME /data
CMD sh -c "curl  -Lk $MY_URL > /data/results"

# docker build --tag=bonus03 .
# docker run --rm -e MY_URL=MY_URL -v $(pwd)/vol:/data/:rw bonus03

# -c flag means execute the following command as interpreted by this program.
# curl -k  This option explicitly allows curl to  perform  "insecure" SSL connections and transfers.
# https://askubuntu.com/questions/230476/