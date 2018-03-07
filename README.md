## caldo-de-cana

### Automated build of a safer R docker

- OS: Ubuntu 16.04.3 LTS Xenial Xerus (latest) or 18.04 alpha Bionic Beaver (unstable)
- R version: 3.4.3 (2017-11-30) -- "Kite-Eating Tree"
- No RStudio
- non-root user: somebody
- pull: ```docker pull fhcflx/caldo-de-cana:latest``` or ```docker pull fhcflx/caldo-de-cana:unstable```
- run:  ```docker run -it -u somebody --rm fhcflx/caldo-de-cana```
- example of prompt: ```somebody@<container id>:~$```
- transfer databases and scripts to container (or output from it):
   ```docker cp /path/to/somebodys/file.rda <container id>:/home/somebody/```
- can install new packages and save history

LICENSE: no one for my pieces of code (public domain); Ubuntu, R and third party stuff all have their own licenses.
