# Karlsen Network and Karlsen Miner Installation Guide

This guide provides detailed instructions for setting up the Karlsen Network node and the Karlsen Miner.

## Setting Up Karlsen Network Node

### Cloning the Repository
Clone the Karlsen Network repository:

git clone https://github.com/karlsen-network/karlsend/
cd karlsend

### Installing Go

Download and install Go:
wget https://golang.org/dl/go1.18.linux-amd64.tar.gz

sudo tar -C /usr/local -xzf go1.18.linux-amd64.tar.gz

echo 'export PATH=$PATH:/usr/local/go/bin' >> $HOME/.profile
source $HOME/.profile

Verify the Go installation:
go version

### Building and Running the Node
Build and run the Karlsen Network node:

go build -o karlsend_exec

./karlsend_exec --utxoindex

## Setting Up Karlsen Miner

### Cloning the Miner Repository
Clone the Karlsen Miner repository:

git clone https://github.com/karlsen-network/karlsen-miner
cd karlsen-miner

### Installing Rust
Install Rust programming language:

curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env

rustc --version
cargo --version

### Installing Dependencies
Install necessary dependencies:

sudo apt-get install protobuf-compiler
protoc --version

sudo apt-get install ocl-icd-opencl-dev

### Building the Miner

Build the Karlsen Miner:

cargo build --release
cd target/release

### Running the Miner

Run the Karlsen Miner with your mining address:

./karlsen-miner --mining-address karlsen:qz74XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
