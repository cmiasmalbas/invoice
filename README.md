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
    Check also if gopath is correct. <br> Run **echo $GOPATH**
    
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
   + Then run **npm install**
   + Then run **node enrollAdmin.js**
   + Then run **node registerUser.js**
   + Then run **node app.js**
   
  #### Step 6: Postman or Insomnia Installation:
   #### Postman
   + Go to this link https://www.getpostman.com/downloads/ 
   + Select the applicable platform for your OS type
   + Then click Download and Install the application
   #### Insomnia
   + Go to this link https://insomnia.rest/download/
   + Select the applicable platform for your OS type
   + Then click Download and Install the application
   
  #### Step 7: Test the endpoints using **POSTMAN** or **INSOMNIA REST Client**
    
  #### Testing Endpoints

  #### Display All Invoices
  ##### http://localhost:3000/
  ##### Use the GET http request in this function as we are getting data
  <br />
  <br />
  <br />

  #### Raise Invoice
  ##### http://localhost:3000/invoice
  ##### Use the POST http request in this function as we are pushing data
  Select **Form URL Encoded** as a structure
  ##### Parameters
  + invoiceId
  + invoiceNumber
  + billedTo
  + invoiceDate
  + invoiceAmount
  + itemDescription
  + gr
  + isPaid
  + paidamount
  + isRepaid
  + repaymentAmount

  ##### NOTE: gr , ispaid , paidamount , repaid , repaymentamount default values are as follows false , false , 0 , false , 0
  **gr = false**
  <br />
  **isPaid = false**
  <br />
  **paidAmount = 0**
  <br />
  **isRepaid = false**
  <br />
  **repaymentamount = 0**
  <br />
  <br />
  <br />

  #### Goods Received
  ##### http://localhost:3000/invoice
  ##### Use the PUT http request in this function as we are modifying a data
  Select **Form URL Encoded** as a structure

  ##### Parameters
  + invoiceId
  + gr
  <br />
  <br />
  <br />

  #### Bank Payment to Supplier
  ##### http://localhost:3000/invoice
  ##### Use the PUT http request in this function as we are modifying a data
  Select **Form URL Encoded** as a structure

  ##### Parameters
  + invoiceId
  + isPaid
  <br />
  <br />
  <br />

  #### OEM Repays to Bank
  ##### http://localhost:3000/invoice
  ##### Use the PUT http request in this function as we are modifying a data
  Select **Form URL Encoded** as a structure

  ##### Parameters
  + invoiceId
  + isRepaid
  <br />
  <br />
  <br />
  
    
    

