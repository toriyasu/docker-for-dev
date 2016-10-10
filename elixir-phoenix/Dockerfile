########## OS ##########
FROM toriyasu5032/ubuntu-deps:1.0

########## OS ##########


########## ENV ##########
# Set the locale(en_US.UTF-8)
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US:en
ENV LC_ALL en_US.UTF-8

# Set the locale(ja_JP.UTF-8)
#ENV LANG ja_JP.UTF-8
#ENV LANGUAGE ja_JP:ja
#ENV LC_ALL ja_JP.UTF-8

# Set app env
ENV HOME /root

########## ENV ##########


########## MIDDLEWARE ##########
RUN apt-get update && apt-get install -y --no-install-recommends \
		nodejs \
		npm \
		inotify-tools \
	&& rm -rf /var/lib/apt/lists/*
RUN apt-get clean
RUN ln -s /usr/bin/nodejs /usr/bin/node

########## MIDDLEWARE ##########


########## SETUP erlang ##########
RUN wget https://packages.erlang-solutions.com/erlang-solutions_1.0_all.deb && dpkg -i erlang-solutions_1.0_all.deb 
RUN apt-get update
RUN apt-get install -y --no-install-recommends esl-erlang
RUN apt-get clean

########## SETUP erlang ##########


########## SETUP elixir ##########
RUN apt-get install -y --no-install-recommends elixir
RUN apt-get clean

########## SETUP elixir ##########


########## SETUP phoenix ##########
RUN yes | mix local.hex 
RUN yes | mix local.rebar
RUN yes | mix archive.install https://github.com/phoenixframework/archives/raw/master/phoenix_new.ez

########## SETUP phoenix ##########


########## RUN phoenix ##########
ENV PHOENIX_APP_NAME hello_phoenix

RUN mkdir -p /usr/local/src/phoenix/app
WORKDIR /usr/local/src/phoenix/app
RUN mix phoenix.new ${PHOENIX_APP_NAME} --no-brunch --no-ecto
WORKDIR /usr/local/src/phoenix/app/${PHOENIX_APP_NAME}
RUN mix deps.get

########## RUN phoenix ##########

