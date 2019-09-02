# Use ubuntu as base image
FROM ubuntu

# Install  python3, pip3 and create a default user
RUN apt update &&  \
    apt install python3 python3-pip git gcc g++ binutils musl-dev openssh-client wget -y &&\
    useradd -ms /bin/bash builder

# set workdir  to builder home
WORKDIR /tmp

# Install build dependencies
RUN pip3 install awscli --user &&\
    wget https://github.com/gohugoio/hugo/releases/download/v0.57.2/hugo_extended_0.57.2_Linux-64bit.tar.gz && \
    tar zxvf hugo_extended_0.57.2_Linux-64bit.tar.gz && \
    chmod +x hugo && \
    echo "PATH=$PATH:/home/builder/.local/bin" > /home/builder/.bashrc && \
    mv hugo /usr/local/bin/


