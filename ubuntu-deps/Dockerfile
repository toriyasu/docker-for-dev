########## OS ##########
FROM ubuntu:latest

########## OS ##########


########## MIDDLEWARE ##########
RUN apt-get update && apt-get install -y --no-install-recommends \
		language-pack-en-base \
		language-pack-en \
		language-pack-ja-base \
		language-pack-ja \
		ca-certificates \
		curl \
		wget \
		bzr \
		git \
		mercurial \
		openssh-client \
		autoconf \
		automake \
		bzip2 \
		file \
		g++ \
		gcc \
		imagemagick \
		libbz2-dev \
		libc6-dev \
		libcurl4-openssl-dev \
		libdb-dev \
		libevent-dev \
		libffi-dev \
		libgeoip-dev \
		libglib2.0-dev \
		libjpeg-dev \
		libkrb5-dev \
		liblzma-dev \
		libmagickcore-dev \
		libmagickwand-dev \
		libmysqlclient-dev \
		libncurses-dev \
		libpng-dev \
		libpq-dev \
		libreadline-dev \
		libsqlite3-dev \
		libssl-dev \
		libtool \
		libwebp-dev \
		libxml2-dev \
		libxslt-dev \
		libyaml-dev \
		make \
		patch \
		xz-utils \
		zlib1g-dev \
	&& rm -rf /var/lib/apt/lists/*
RUN apt-get clean
RUN locale-gen en_US en_US.UTF-8
RUN dpkg-reconfigure locales 

########## MIDDLEWARE ##########

