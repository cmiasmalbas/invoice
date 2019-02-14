# Hyperledger Fabric -  Invoice

### Development Environment
  + Operating System: Ubuntu 18.04 LTS – 64 bit
  + Go version: go1.11.5 linux/amd64
  
### Pre-Requisites:
  + Docker Engine: Version 17.03 or higher
  + Docker-Compose: Version 1.8 or higher
  + Node: 8.9 or higher (note version 9 and higher is not supported)
  + npm: v5.x
  + git: 2.9.x or higher
  + Python: 2.7.x
  + A code editor of your choice, we recommend VSCode
  
### GO Installation:
  + Open the browser, copy this link: https://golang.org/dl/ and download the latest version
  + Open the terminal and type the following commands:
    <pre> tar -C /usr/local -xzf go$VERSION.$OS-$ARCH.tar.gz </pre>
    <pre> export PATH=$PATH:/usr/local/go/bin </pre>
  + You can check if go is properly installed by running go version in your terminal.
    Check also if gopath is correct. Run **echo $GOPATH**
    
### Setting up the network:
   
  #### Step 1:
  + Clone the following links by typing the commands below:
    <pre> git clone https://github.com/bchinc/blockchain-training-labs </pre>
    <pre> git clone https://github.com/hyperledger/fabric-samples </pre>
    
  #### Step 2:
  + Open the terminal to create a folder **invoice** 


