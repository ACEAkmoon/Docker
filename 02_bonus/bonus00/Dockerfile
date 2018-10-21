FROM alpine
MAINTAINER Alex Krushinsky <akrushin@student.unit.ua>

RUN apk add --no-cache emacs
CMD ["sh", "-c", "emacs ."]

# docker build --tag=emacs .
# docker run -it --rm emacs