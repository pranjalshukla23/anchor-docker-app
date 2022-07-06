FROM ubuntu:20.04
RUN apt-get -y update
RUN apt-get -y upgrade
RUN apt-get -y install
RUN apt install -y npm nodejs
RUN curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
RUN sh -c "$(curl -sSfL https://release.solana.com/v1.10.29/install)"
RUN npm i -g corepack
RUN apt-get update
RUN apt -y install cargo
RUN apt-get install -y pkg-config build-essential libudev-dev
RUN curl https://sh.rustup.rs -sSf | sh
RUN cargo install --git https://github.com/project-serum/anchor avm --locked --force
RUN avm install -y latest
RUN avm use latest
RUN anchor --version
RUN anchor init anchor-workspace
EXPOSE 4000