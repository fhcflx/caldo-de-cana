FROM ubuntu:xenial
MAINTAINER Francisco Felix <fhcflx@outlook.com>
RUN groupadd -r somebody && useradd --no-log-init -r -g somebody somebody
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
            ca-certificates \
            dirmngr \
            apt-transport-https
RUN echo "deb https://cran.rstudio.com/bin/linux/ubuntu xenial/" | tee -a /etc/apt/sources.list
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E298A3A825C0D65DFD57CBB651716619E084DAB9
RUN apt-get update \
    && apt-get install r-base r-base-dev -y --allow-unauthenticated
WORKDIR /home/somebody
CMD ["/bin/bash"]
