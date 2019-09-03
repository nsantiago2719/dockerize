# Use ubuntu as base image
FROM ubuntu

# Install  python3, pip3 and create a default user
RUN apt update &&  \
    apt install python3 python3-pip git gcc g++ binutils musl-dev openssh-client wget -y &&\
    wget https://github.com/gohugoio/hugo/releases/download/v0.57.2/hugo_extended_0.57.2_Linux-64bit.tar.gz && \
    tar zxvf hugo_extended_0.57.2_Linux-64bit.tar.gz && \
    chmod +x hugo && \
    mv hugo /usr/local/bin/
    pip3 install awscli

# set workdir  to builder home
WORKDIR /tmp

#    echo "PATH=$PATH:/home/builder/.local/bin" > /home/builder/.bashrc && \
#    useradd -ms /bin/bash builder && \


