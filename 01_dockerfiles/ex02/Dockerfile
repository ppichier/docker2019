FROM ruby:2.5.1
LABEL maintainer="ppichier@student.le-101.fr"
LABEL description="Dockerfile ruby container"

ONBUILD RUN apt-get -y update && apt-get -y upgrade
ONBUILD RUN apt-get install -y nodejs && \
			apt-get install -y sqlite3
ONBUILD COPY ./blog opt/app/
ONBUILD WORKDIR opt/app/
ONBUILD RUN gem install rails && \
			bundle install
ONBUILD RUN rake db:create && \
			rake db:migrate && \
			rake db:seed

EXPOSE 3000

