FROM ubuntu:16.04

# install cowsay, and move the "default.cow" out of the way so we can overwrite it with "docker.cow"
RUN apt-get update

RUN apt-get install -y tree --no-install-recommends

CMD ["tree", "-f"]
