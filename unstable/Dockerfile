FROM ubuntu:bionic
MAINTAINER Francisco Felix <fhcflx@outlook.com>
RUN groupadd -r somebody && useradd --no-log-init -r -g somebody somebody
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
            dirmngr \
            tzdata
RUN apt-get update \
    && apt-get install -t unstable r-base r-base-dev -y --allow-unauthenticated
WORKDIR /home/somebody
CMD ["/bin/bash"]
