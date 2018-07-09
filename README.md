# wrestling

4 ways of developing and deploying our Smart Contracts:

- The first one is to use Truffle and Ganache. Since we copied the code from the last tutorial, I want to tell you that there are plugins available for the most popular text editors and IDEs. Some offer only syntax highlighting, while others help with other areas.
- The second one is to deploy code from Truffle to geth (and the GUI app Mist).
- The third, is to use Remix to write small, simple contract when you are just learning Solidity, and deploying the code in Mist like shown in the video previously linked.
- Or like a real cowboy, you could use a simple text editor to write and then deploy your untested contract using a nameless third party’s drag-and-drop deployment feature.

#### Test with ganache

- tells ganache-cli to start at the port 7545

```
ganache-cli -p 7545
```

- compile and deploy code to blockchain

```
truffle compile
truffle migrate --network development
```

- start Truffle’s console

```
truffle console --network development
```

#### Test with Mist
closer to a real environment, to be more familiar with it.

- create "genesis.json" file


- init our private network

```
geth --datadir=./chaindata/ init ./genesis.json
```

- start our private network

```
geth --datadir=./chaindata/ --rpc --ipcpath ./chaindata/geth.ip

```

- Connect to Mist (or Wallet)

```
/Applications/Mist.app/Contents/MacOS/Mist --rpc http://127.0.0.1:8545

```

or

```
/Applications/Ethereum\ Wallet.app/Contents/MacOS/Ethereum\ Wallet --rpc http://127.0.0.1:8545
```

-----

Source: 

- [Ethereum Development Walkthrough (Part 1: Smart contracts)](https://hackernoon.com/ethereum-development-walkthrough-part-1-smart-contracts-b3979e6e573e)
- [Ethereum Development Walkthrough (Part 2: Truffle, Ganache, Geth and Mist)](https://hackernoon.com/ethereum-development-walkthrough-part-2-truffle-ganache-geth-and-mist-8d6320e12269)

