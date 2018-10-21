FROM node
MAINTAINER Alex Krushinsky <akrushin@student.unit.ua>

RUN apt-get -qqy update && \
	apt-get -qqy install \
	nodejs \
	build-essential \
	curl

RUN curl -o- -L https://yarnpkg.com/install.sh | \
	bash && \
	apt-get -qqy purge curl

WORKDIR /project
EXPOSE 8080

CMD ["bash"]

# docker build --tag=yarn-env .
# docker run -it --rm yarn-env

# yarn-env -> analog is apt-get
# https://yarnpkg.com/lang/en/docs/install/#mac-stable
# yarn --version
