FROM phusion/baseimage:focal-1.0.0
LABEL maintainer="Halfy Developers <dev@halfy.org>"
LABEL description="Dockerised Halfy, built from Travis"

ARG USER_ID
ARG GROUP_ID

ENV HOME /home/halfy

# add user with specified (or default) user/group ids
ENV USER_ID ${USER_ID:-1000}
ENV GROUP_ID ${GROUP_ID:-1000}
RUN groupadd -g ${GROUP_ID} halfy && \
    useradd -u ${USER_ID} -g halfy -s /bin/bash -m -d /home/halfy halfy && \
    mkdir /home/halfy/.halfy && \
    chown ${USER_ID}:${GROUP_ID} -R /home/halfy

COPY bin/* /usr/local/bin/

RUN chmod a+x /usr/local/bin/*

USER halfy

VOLUME ["/home/halfy"]

EXPOSE 8547 9999 25693 25694

WORKDIR /home/halfy
