FROM debian:bookworm

ENV RELEASE_STAMP=20230928
ENV RELEASE_VERSION=10.21.0

RUN apt-get -y update; apt-get -y install curl gnupg postgresql-client-15 azure-cli
RUN set -ex \
    && curl -L -o azcopy.tar.gz https://azcopyvnext.azureedge.net/release${RELEASE_STAMP}/azcopy_linux_amd64_${RELEASE_VERSION}.tar.gz \
    && tar -xzf azcopy.tar.gz && rm -f azcopy.tar.gz \
    && cp ./azcopy_linux_amd64_*/azcopy /usr/local/bin/. \
    && chmod +x /usr/local/bin/azcopy \
    && rm -rf azcopy_linux_amd64_*
RUN apt-get clean

ENTRYPOINT [ "/bin/sh" ]
