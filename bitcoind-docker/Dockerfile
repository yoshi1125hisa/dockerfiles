FROM debian

RUN sudo apt-add-repository ppa:bitcoin/bitcoin && \
    sudo apt-get update && \
    sudo apt-get install bitcoind && \
    bitcoind -daemon
