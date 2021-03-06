# EthDemocracy
This project is an unfinished smart contract for Ethereum that is used in trainings.

[![CircleCI](https://circleci.com/gh/chrisdotn/ethdemocracy/tree/master.svg?style=svg)](https://circleci.com/gh/chrisdotn/ethdemocracy/tree/master)

## Use Case
The project provides a stub for a smart contract that implements a simple _liquid democracy_ on the blockchain. The projects supplies tests for the stub that all fail initially. During the training we want to actually implement the contract so that the tests all succeed.

## Installation
To use the project, clone the repository:
```Shell
$ git clone https://github.com/chrisdotn/ethdemocracy.git
```

Change into the directory and do a
```Shell
$ npm install
```


## Usage
To develop with the project make sure to have [testrpc](https://github.com/ethereumjs/testrpc) running.

After all packages have installed you can use the [truffle](http://truffleframework.com/) commands to interact with the project:
- `truffle compile` will compile smart contracts that have been changed since the last compile.
- `truffle compile --all` will compile all smart contracts.
- `truffle migrate` will compile smart contracts and deploy them to the default network.
- `truffle migrate --network staging` will compile and deploy to network staging.
- `truffle migrate --reset` will compile and deploy all smart contract even if they haven't changed.
- `truffle test` will run the tests in directory `$(PROJECT)/test`.
- `truffle test ./path/to/test/file.sol` will run the test in the specified file.
- `truffle console` will open a `web3`-enabled Javascript console for manual interaction with the contracts.

To interact with the frontend use:
- `npm run build` build the frontend using webpack
- `npm run dev` build the frontend using webpack and serve it to `localhost:8080`. This command will monitor changes to the frontend and redeploy if needed.
