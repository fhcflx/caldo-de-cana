FROM ubuntu:artful
ENTRYPOINT ["/bin/sh" "-c" "/bin/bash"]
MAINTAINER Francisco Felix <fhcflx@outlook.com> 
RUN echo "deb http://cran.rstudio.com/bin/linux/ubuntu artful/" | tee -a /etc/apt/sources.list
RUN apt-get update
RUN apt-get install r-base r-base-dev -y --allow-unauthenticated --fix-missing
RUN adduser --quiet --disabled-password --shell /bin/bash --home /home/somebody somebody
RUN chown somebody:somebody /home/somebody
WORKDIR /home/somebody
USER [somebody]
CMD ["/bin/bash"]
