FROM rust:latest

WORKDIR /rust

# Make sure the container is up to date
RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
    
# Install any other required dependencies
# RUN rustup target add thumbv7em-none-eabi

CMD ["bash"]