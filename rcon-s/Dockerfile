FROM ubuntu:xenial
ENTRYPOINT ["/bin/sh" "-c" "/bin/bash"]
MAINTAINER Francisco Felix <fhcflx@outlook.com>
RUN adduser --home /home/somebody --shell /bin/bash somebody \
    && chown somebody:somebody /home/somebody
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
USER [somebody]
CMD ["/bin/bash"]
