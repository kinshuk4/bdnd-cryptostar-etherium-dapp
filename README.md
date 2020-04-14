# cryptostar-etherium-dapp
CryptoStar Dapp running on Rinkeby Ethereum Testnet

### Token Info
* ERC-721 Token Name: Star Notary Token
* ERC-721 Token Symbol: SNT
* Token Address: [0xBdb81AC5D9D73248e98af1434D35043bdD8d2d81](https://rinkeby.etherscan.io/address/0xBdb81AC5D9D73248e98af1434D35043bdD8d2d81)



## Dependencies

* Truffle version: v5.1.13
* OpenZeppelin version: 2.5.0
* truffle-hdwallet-provider

### Installation

```bash
npm install --save truffle-hdwallet-provider
```
```bash
npm install --save openzeppelin-solidity
```

## Configuration to deploy the contract on Rinkeby Ethereum Testnet.
When you deploy the contract on Rinkeby Ethereum Testnet, you need to add and modify `truffle-config.js` file on the root folder by using your Metamask’s seed and Infura setup.

The code of `truffle-config.js` should look something as follows:
```javascript
const HDWalletProvider = require('truffle-hdwallet-provider');
const infuraKey = "<Infura Project Id>";
//
const fs = require('fs');
const mnemonic = fs.readFileSync(".secret").toString().trim();
```

For metamask we create a .secret file and put the secret there.
For infurakey, just set your project id api key from Infura.

## Develop the project

- For starting the development console, run:

  `truffle develop`

- For compiling the contract, inside the development console, run:

  `compile`

- For migrating the contract to the locally running Ethereum network, inside the development console, run:

  `migrate --reset`

- For running unit tests the contract, inside the development console, run:

  `test`

- For running the Front End of the DAPP, open another terminal window and go inside the project directory, and run:

  `cd app`

  `npm run dev`



## Deploy on Rinkeby

```bash
truffle migrate --reset --network rinkeby
```