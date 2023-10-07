# Decentralized Identity Package

Easily create and verify decentralized identities using Ethereum wallets. This package allows users to connect their Ethereum wallet, generate an API key based on their address, and create a decentralized identity stored on IPFS.

## Features

- Wallet connectivity
- API key generation
- UI for identity creation
- Data pinning on IPFS
- Smart contract interactions for storing and verifying identities

## Installation

```bash
npm install decentralized-identity-package
```

## Usage

### Connecting a Wallet and Generating API Key

```javascript
const { connectWallet } = require('decentralized-identity-package');

async function initiate() {
    const apiKey = await connectWallet();
    console.log(apiKey);
}
```

### Creating a Decentralized Identity

```javascript
const { createIdentity } = require('decentralized-identity-package');

const userData = {
    name: "John Doe",
    jobRole: "Developer",
    experience: "5 years",
    stack: "JavaScript, React, Ethereum"
};

async function initiateIdentity() {
    const ipfsPath = await createIdentity(userData);
    console.log(ipfsPath);
}
```

### Verifying a User's Identity

```javascript
const { verifyIdentity } = require('decentralized-identity-package');

async function checkIdentity(address) {
    const identityData = await verifyIdentity(address);
    console.log(identityData);
}
```

## Requirements

- Web3-enabled browser or provider
- IPFS (if self-hosting)
- Ethereum smart contract setup for storing user identities

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

[MIT](https://choosealicense.com/licenses/mit/)

---
