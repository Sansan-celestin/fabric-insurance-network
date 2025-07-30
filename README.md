# Fabric Insurance Network

This project is a **Hyperledger Fabric test network** implementing an **insurance claim management system** using chaincode written in Go.

##  Features

- Smart contract for managing insurance claims
- Supports functions: `CreateClaim`, `ReadClaim`, `ClaimExists`
- Interacts with multiple peers from Org1 and Org2
- Secure TLS communication with orderer and peers
- Successfully tested with the Fabric CLI

##  Project Structure

- `chaincode/insurance/go/`: Smart contract source code
- `organizations/`: Peer and orderer crypto materials
- `test-network/`: Network scripts and Docker Compose files

##  How to Test

### 1. Start the network:
```bash
./network.sh up createChannel -ca

2. Deploy the chaincode:
./network.sh deployCC -ccn insurance -ccp ../chaincode/insurance/go -ccl go

3. Use CLI container:
docker exec -it cli bash

4. Invoke(S'inscrire soit inscrire les informations du sinistre) chaincode with the function below:
          - CreateClaim
 

5. Query(Faire une requête) the ledger with functions below:
        - CreateClaim
        - ReadClaim
        - ClaimExists

Author: Sansan Celestin Hien
University : Université Virtuelle de Côte D'Ivoire (UVCI)
Country : Ghana
