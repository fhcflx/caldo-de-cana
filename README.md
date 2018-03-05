# Automated build of a safer R docker

## caldo-de-cana

- OS: Ubuntu 16.04 Xenial
- R version: 3.4.3 (2017-11-30) -- "Kite-Eating Tree"
- No RStudio
- non-root user: somebody, UID = 1000
- run:  ```docker run -it -u somebody --rm fhcflx/caldo-de-cana```
- example of prompt: ```somebody@<container id>:~$```
- transfer databases and scripts to container (or output from it):
   ```docker cp /path/to/somebodys/file.rda <container id>:/home/somebody/```
- can install new packages and save history

LICENSE: no one for my pieces of code (public domain); Ubuntu, R and third party stuff all have their own licenses.
