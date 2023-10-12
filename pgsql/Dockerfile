FROM debian:bookworm

RUN apt-get -y update; apt-get -y install curl gnupg postgresql-client-15 azure-cli
RUN apt-get clean

ENTRYPOINT [ "/bin/sh" ]
