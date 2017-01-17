FROM debian:jessie
MAINTAINER Michael Heuer <heuermh@acm.org>

#
# Derived from:
#
# Mark Cerqueira <mark.cerqueira@gmail.com>
# https://github.com/markcerqueira/chuck-renderer/
# Licensed GPL version 3
#

# ChucK dependencies
RUN apt-get update && apt-get install -y \
    build-essential \
    git \
    bison \
    flex \
    libsndfile1-dev \
    libpulse-dev \
    libasound2-dev
		
# Clone ChucK, build it, copy it to /bin/
RUN git clone --depth 1 https://github.com/ccrma/chuck.git \
    && cd chuck/ \
    && cd src/ \
    && make linux-alsa \
    && mv ./chuck /bin/
