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
    Check also if gopath is correct. 
    Run **echo $GOPATH**
    
### Setting up the network:
   
  #### Step 1:
  + Clone the following links/materials by typing the commands below:
    <pre> git clone https://github.com/bchinc/blockchain-training-labs </pre>
    <pre> git clone https://github.com/hyperledger/fabric-samples </pre>
    <pre> git clone https://github.com/cmiasmalbas/invoice </pre>
    
  #### Step 2:
  + From this repository, open the **invoice** folder and go to **invoice** folder 
  + Copy the following files from **invoice** folder:
  <pre> invoice/
  | ---- invoice/
              | ---- app.js
              | ---- enrollAdmin.js
              | ---- package.json
              | ---- registerUser.js
              | ---- startFabric.sh
  </pre>
   
  
  #### Step 3:
  + Open the terminal, go to the directory of **fabric-samples** and create a **invoice** folder by typing the commands below:
  <pre> cd fabric-samples </pre>
  <pre> mkdir invoice </pre>
  
  + Paste the files from **Step 2** in the **invoice** folder:
  <pre>fabric-samples/
  | ---- invoice/
              | ---- app.js
              | ---- enrollAdmin.js
              | ---- package.json
              | ---- registerUser.js
              | ---- startFabric.sh
  </pre>
  
  #### Step 4:
   + Create a folder **invoice** under **fabric-samples/chaincode/**
   + Then copy the **go/** folder in this repository or simply create a new folder named **go/** inside **fabric-samples/chaincode/invoice/** then paste it to the directory:
   <pre>fabric-samples/
  | ---- chaincode/
              | ---- invoice/
                          | ---- go/
                                      | ---- invoice.go
  </pre>
  
  #### Step 5:
    + Open terminal then change directory to **/fabric-samples/invoice/**
    + Then run **./startFabric.sh**

