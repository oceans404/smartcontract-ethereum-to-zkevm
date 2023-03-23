# Deploy a smart contract that exists on Ethereum to Polygon zkEVM

This project was bootstrapped with the default [Hardhat javascript starter](https://hardhat.org/hardhat-runner/docs/getting-started#quick-start) Lock.sol contract deployed to Ethereum (Goerli). The deploy script sets a lock amount (.001 ETH) and a lock time (60 seconds). After the lock time, you will be able to withdraw() your lock amount from the contract.

Here's how to deploy the exact same smart contract code to Polygon zkEVM in less than a minute.


## Pre-req: Deploy a contract to Goerli (or any other EVM network)

Here's how I originally deployed the contract to Goerli:

Run this command to create a .env file. 

```shell
cp .env.sample .env;
```

Replace the variables values with your ACCOUNT_PRIVATE_KEY and GOERLI_API_KEY_ALCHEMY.

```shell
npm i
npx hardhat compile
npx hardhat run scripts/deploy.js --network goerli
```

> Lock with 0.001ETH and unlock timestamp 1679613983 deployed to 0x1370f5c43DaAF6E2c8e66A22EdB16aECF3adB067

View the Goerli contract on Etherscan: https://goerli.etherscan.io/address/0x1370f5c43DaAF6E2c8e66A22EdB16aECF3adB067 You should be able to withdraw your Goerli ETH from the contract within 1 minute of deployment.

## Add Polygon zkEVM to your Hardhat config file and deploy to zkEVM