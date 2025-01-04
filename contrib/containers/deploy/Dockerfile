FROM phusion/baseimage:focal-1.0.0
LABEL maintainer="EGamingCoin Developers <dev@egamingcoin.org>"
LABEL description="Dockerised EGamingCoin, built from Travis"

ARG USER_ID
ARG GROUP_ID

ENV HOME /home/egamingcoin

# add user with specified (or default) user/group ids
ENV USER_ID ${USER_ID:-1000}
ENV GROUP_ID ${GROUP_ID:-1000}
RUN groupadd -g ${GROUP_ID} egamingcoin && \
    useradd -u ${USER_ID} -g egamingcoin -s /bin/bash -m -d /home/egamingcoin egamingcoin && \
    mkdir /home/egamingcoin/.egamingcoin && \
    chown ${USER_ID}:${GROUP_ID} -R /home/egamingcoin

COPY bin/* /usr/local/bin/

RUN chmod a+x /usr/local/bin/*

USER egamingcoin

VOLUME ["/home/egamingcoin"]

EXPOSE 21371 9999 31371 31372

WORKDIR /home/egamingcoin
