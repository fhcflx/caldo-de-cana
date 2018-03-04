FROM ubuntu:zesty
ENTRYPOINT ["/bin/sh" "-c" "/bin/bash"]
MAINTAINER Francisco Felix <fhcflx@outlook.com>
RUN adduser --quiet --home /home/somebody --shell /bin/bash --disabled-password  \
    --uid 1000 --gecos "" somebody \
    && chown somebody:somebody /home/somebody
RUN rm /etc/apt/sources.list \
    && echo "deb http://old-releases.ubuntu.com/ubuntu zesty main \
          multiverse restricted universe" | tee -a /etc/apt/sources.list \
    && echo "deb http://old-releases.ubuntu.com/ubuntu zesty-updates main \
          multiverse restricted universe" | tee -a /etc/apt/sources.list \
    && echo "deb http://old-releases.ubuntu.com/ubuntu zesty-backports main \
          multiverse restricted universe" | tee -a /etc/apt/sources.list \
    && echo "deb http://old-releases.ubuntu.com/ubuntu zesty-security main \
          multiverse restricted universe" | tee -a /etc/apt/sources.list
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
            ca-certificates \
            dirmngr \
            apt-transport-https
RUN echo "deb https://cran.rstudio.com/bin/linux/ubuntu zesty/" | tee -a /etc/apt/sources.list
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E298A3A825C0D65DFD57CBB651716619E084DAB9
RUN apt-get update \
    && apt-get install r-base r-base-dev -y --allow-unauthenticated --fix-missing
WORKDIR /home/somebody
USER [somebody]
CMD ["/bin/bash"]
