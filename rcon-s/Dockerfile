FROM ubuntu:artful
ENTRYPOINT ["/bin/sh" "-c" "/bin/bash"]
MAINTAINER Francisco Felix <fhcflx@outlook.com>
RUN apt-get update &&\
    apt-get install -y --no-install-recommends ca-certificates dirmngr
RUN echo "deb https://cran.rstudio.com/bin/linux/ubuntu artful/" | tee -a /etc/apt/sources.list
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E298A3A825C0D65DFD57CBB651716619E084DAB9
RUN apt-get update &&\
    apt-get install r-base r-base-dev -y --allow-unauthenticated --fix-missing
RUN adduser --quiet --disabled-password --shell /bin/bash --home /home/somebody somebody
RUN chown somebody:somebody /home/somebody
WORKDIR /home/somebody
USER [somebody]
CMD ["/bin/bash"]
