FROM alpine:latest
LABEL maintainer="ppichier <ppichier@student.le-101.fr>"
LABEL description="Dockerfile with vim"

RUN apk update && \
	apk upgrade && \
	apk add vim

ENTRYPOINT ["vim"]
