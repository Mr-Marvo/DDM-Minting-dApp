# NFT Minting dApp using ERC721
This is a Testnet Minting dApp using Ethereum ERC721 Smart Contract.

## Installation

You can use **the default smart contract** and play with it or you can also put **your own smart contract** and make changes as needed. Remember to change `.env` file with your own variables.

Use the default **Smart Contract:**

```bash

  # Clone the repository and change directory into it
  git clone https://github.com/Mr-Marvo/DDM-Minting-dApp
  cd minting-dapp

  npm install            # Download packages
  npm run dev            # Run the dev server
```

## Making Changes

First of all change .env variables with yours. And update the `dapp.config.js` file according to your needs.

If you want to make changes on DidemRaffe smart contract, you can find DidemRaffe.sol inside `/contracts`folder. After making changes you need to recompile your smart contract using `npx hardhat compile` command. It will recompile the smart contract and create & update `/artifacts` folder. Smart contract ABI is also in this folder.

After making changes you need to update the `scripts/whitelist.js` with your whitelisted users accounts and deploy & verify your smart contract on ethereum blockchain. Use the scripts I created for you
to do that. You can find the _deploy_ & _verify_ scripts inside `/scripts`folder.

```bash
  # This command will deploy your smart contract on rinkeby test network
  npx hardhat run scripts/deployContract.js --network rinkeby

  # This command will verify your smart contract on rinkeby etherscan
  npx hardhat run scripts/verifyContract.js --network rinkeby
```

\*\* If you want to use a different network you need to pass its name instead of rinkeby. Also make sure you configured it
in `hardhat.config.js` file as a network option.

Finally update the `/utils/interact.js` file so that it uses the related functions from your updated contract. Also change the contract address and the imported ABI in this file with your newly deployed contract.

## Deploying on mainnet

When you are done with making changes and your minting dapp is just as you wanted it is time to deploy on ethereum mainnet.
To do that;

- Make sure you changed all env variables with yours. And also for the network you need to chose ethereum mainnet.
- Update `hardhat.config.js` so that as network option you use _mainnet_ not _rinkeby_. [hardhat tutorial](https://hardhat.org/tutorial/deploying-to-a-live-network.html)
- While deploying your contract with hardhat you need to use mainnet as network-name

```bash
  # This command will deploy your smart contract on ethereum mainnet
  npx hardhat run scripts/deployContract.js --network mainnet

  # This command will verify your smart contract on mainnet etherscan
  npx hardhat run scripts/verifyContract.js --network mainnet
```

## Learn More

You can learn more about Blockchain Development and web3 from my github. So please hit [Follow](https://github.com/login?return_to=https%3A%2F%2Fgithub.com%2FMr-Marvo) button.

### Contact Me

If you want any support or If you have any project for me please feel free to contact me.\
View [Github Profile](https://github.com/Mr-Marvo) for contact details.

If you like my project please hit the [star] button
## ⭐ Give a Star
## 💪 [Follow Me](https://github.com/login?return_to=https%3A%2F%2Fgithub.com%2FMr-Marvo) 
## ⚡ [Github](https://github.com/Mr-Marvo)


## Happy Coding ♨
devNishan