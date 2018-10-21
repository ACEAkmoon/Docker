FROM shawn/ubuntu-precise-i386
MAINTAINER Alex Krushinsky <akrushin@student.unit.ua>

RUN apt-get -qqy update && apt-get -qqy install \
	build-essential \
	valgrind

WORKDIR /app
CMD /bin/sh

# docker build --tag=valgrind .
# docker run -it --rm valgrind

# install utilins for check leaks (valgrind)
# valgrind --leak-check=yes myprog argc1 argv2
