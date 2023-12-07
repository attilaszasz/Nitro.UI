FROM ubuntu:20.04

# Install curl and sudo
RUN apt-get update -y && \
    apt-get install -y --no-install-recommends sudo curl jq numactl && \
    curl -sfL https://raw.githubusercontent.com/janhq/nitro/main/install.sh | sudo /bin/bash - && \
    mkdir /models && \
    apt-get remove --purge -y curl jq && \
    apt-get autoremove -y --purge && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

EXPOSE 3928

ENTRYPOINT ["numactl", "--physcpubind=0-7", "nitro"]

CMD ["1", "0.0.0.0", "3928"]