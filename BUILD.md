BUILD INSTRUCTIONS
==================

Included below are instructions for building packages for UHD for the Spire
production stack.

Instructions assume starting from the user's home directory that the user is
in the docker group. Instructions have been tested on hosts that have the 
`testrig` ansible playbook applied.

# Building for Ubuntu 16.04

## Build Instructions
```
git clone git@github.com:nsat/uhd.git
docker run -v ~/uhd:/uhd -it --entrypoint bash ubuntu:16.04
apt-get update > /dev/null
apt-get install -y git python-cheetah cmake libboost-all-dev lsb-core > /dev/null
mkdir -p /uhd/host/build
cd /uhd/host/build
cmake ..
make -j8
cpack
```

# Building for Ubuntu 12.04:

## Build Instructions
```
git clone git@github.com:nsat/uhd.git
docker run -v ~/uhd:/uhd -it --entrypoint bash ubuntu:12.04
apt-get update > /dev/null
apt-get install -y git python-cheetah cmake libboost-all-dev lsb-core > /dev/null
mkdir -p /uhd/host/build
cd /uhd/host/build
cmake ..
make -j8
cpack
```
