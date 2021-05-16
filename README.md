# CRYPTOSTAR DAPP
**PROJECT: Decentralized Star Notary Service Project** - For this project, you will create a DApp by adding functionality with your smart contract and deploy it on the public testnet.

### Dependencies
For this project, you will need to have:
1. **Node and NPM** installed - NPM is distributed with [Node.js](https://www.npmjs.com/get-npm)
```bash
# Check Node version, Project tested with version v14.17.0. you can use "nvm" to switch between node versions
node -v
# Check NPM version, Project tested with v6.14.13
npm -v
```


2. **Truffle v5.X.X** - A development framework for Ethereum. 
```bash
# Unsinstall any previous version
npm uninstall -g truffle
# Install
npm install -g truffle
# Specify a particular version. Project tested with v5.3.6
npm install -g truffle@5.3.6
# Verify the version
truffle version
```


3. **Metamask: 9.5.2** - If you need to update Metamask just delete your Metamask extension and install it again.


4. Ganache not needed. We run a local test node using the command "truffle develop". Port is 8585


5. **Mandatory packages for contracts and truffle**:
```bash

# install packages
npm install --save  openzeppelin-solidity@4.1.0
npm install --save  dotenv@9.0.2
npm install --save  @truffle/hdwallet-provider@1.4.0
```

6. **Mandatory packages for the frontend**:
```bash
cd app
# install packages
npm install webpack-dev-server -g
npm install web3
```

6. **Configure truffle compiler** in `truffle-config.js`:
```js
// Configure your compilers  
compilers: {    
  solc: {      
    version: "0.8.4", // <- Use this        
    // docker: true,
    // ...
```

7. **Load Infura key and your account private key in ** in `.env` file (please created in the root of your project):
```
PRIVATE_KEYS="<your-private-key>"
INFURA_API_KEY=<infura-rinkeby-api-key>
```


### Run the application
1. Clean the frontend 
```bash
cd app
# Remove the node_modules  
# remove packages
rm -rf node_modules
# clean cache
npm cache clean
rm package-lock.json
# initialize npm (you can accept defaults)
npm init
# install all modules listed as dependencies in package.json
npm install
```


2. Start Truffle by running
```bash
# For starting the development console
truffle develop
# truffle console

# For compiling the contract, inside the development console, run:
compile

# For migrating the contract to the locally running Ethereum network, inside the development console
migrate --reset

# For running unit tests the contract, inside the development console, run:
test
```

3. Frontend - Once you are ready to start your frontend, run the following from the app folder:
```bash
cd app
npm run dev
```

---
## Compare with my tests on Rinkeby

- ERC-721 Token Name & ERC-721 Token Symbol are setup in the file `StarNotary.sol`. They are respectively "StarNotary" and "STR".
- compile your project `trumple compile`
- Deploy contract to rinkeby. Execute `truffle migrate --reset --network rinkeby`
- Please fetch contract address from truffle output. Mine is "0x784F73b81f207B79768103b568d16c33433f4504"
- Check on [Rinkeby etherscan](https://rinkeby.etherscan.io/address/0x784f73b81f207b79768103b568d16c33433f4504)

