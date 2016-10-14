FROM ubuntu:16.04

# install tools and dependencies
RUN apt-get update && \
    apt-get install -y ca-certificates wget && \
    rm -rf /var/lib/apt/lists/*

RUN wget https://github.com/ethcore/parity/releases/download/v1.3.7/parity_1.3.7-0_amd64.deb && \
    dpkg -i parity_1.3.7-0_amd64.deb  
    
VOLUME /root/.parity
WORKDIR /root

#ENTRYPOINT ["parity","--tracing","on","--rpcaddr","0.0.0.0","--jsonrpc-interface","all","--jsonrpc-hosts","all"]
ENTRYPOINT parity
