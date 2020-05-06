# Deploy EIP 1820

Ethereum [EIP 1820](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-1820.md) is a standard for pseudo-introspection of smart contracts on Ethereum.

This library ensures that the EIP 1820 registry smart contract exists on any given chain.  Particularly useful for test environments.

Uses [ethers.js](https://docs.ethers.io/ethers.js/html/index.html).

# Setup

Install `deploy-eip-1820` via yarn:

```sh
$ yarn add deploy-eip-1820
```

or npm:

```sh
$ npm i deploy-eip-1820
```

# Usage

To ensure that the EIP 1820 Registry contract exists on the network you are using, use the `setup1820` function:

```javascript
const { deploy1820 } = require('deploy-eip-1820')

async function deploy() {
    const wallet = ethers.Wallet.fromMnemonic("...your mnemonic...")
    // The wallet must have at least 0.08 Ether
    await deploy1820(wallet)
}

```