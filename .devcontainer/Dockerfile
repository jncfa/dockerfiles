FROM ubuntu:latest

# install dependencies
RUN apt-get update && apt-get install -y \
    curl python3 python3-pip python3-venv \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# install direnv and hook into bash
ENV bin_path /usr/local/bin
RUN curl -sfL https://direnv.net/install.sh | bash
RUN echo 'eval "$(direnv hook bash)"' >> ~/.bashrc
RUN echo 'direnv allow $WORKSPACE' >> ~/.bashrc
