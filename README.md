# Blockchain-Class-Notes

Contains my notes from Blockchain Lectures.

## Lecture 1 - 5th August
Blockchain is chain of blocks, each block has set of transactions, based on these transactions it creates a hash code.\
These set of blocks have a unique hashcode associated to details of transactions. Combining these blocks make a node.\
All cryptos are one possible application of blockchain.\
Zero block is called the Genesis Block. (Zero Block: The first block of Blockchain)\


#### Features of Blockchain
- System of recording information
- Difficult/Impossible to change, hack or cheat
- Fully decentralized p2p data storage spread across all particiapnts that are reffered as nodes.

#### Features of Distributed Ledger (DLT)
- Programmable i.e Smart Contracts
- Secure
- Anonymous
- Unanimous
- Distributed
- Immutable
- TimeStamped



## Lecture 2 - 6th August
Blockchain - Distributed ledger for maintaining a permanent and secure ledger managed by p2p network.\

#### Blockchain Internals
Miner Node
- Extremely powerful hardware
- Can take multiple transactions, create a hash that meets blockchain's difficulty level
- somebody takes group of transactions and create a valid hash for it.
- Once such block is accepted in blockchain, Miner gets his fees.


#### Types of Blockchain
Public Blockchain
- Anyone can be a node in a public network and submit transactions
- Example: $BTC, $ETH

Private Blockchain
- use blockchain according to your business logic
- private in scope and limited to defined users.
- Example: Ethereum, Polygon

Permissionless Blockchain
- Anyone can process transactions

Permissioned Blockchain
- Only approved nodes(also referred as users) can process the transaction


## Lecture 3 - 12th August
#### Ethereum
- Blockchain-based computing platform

This includes three things
- Gas: Price per operation
- Nonce: Random number a mining algorithm uses to affect outcome of hashing algorithm
- Difficulty

#### Accounts in Ethereum
- User accounts
- Contracts

#### Nodes
- Computers that are part of blockchain network
- Miners are nodes that are willing to participate in transactions and creating a hash for it.

#### Ether
- Digital currency used by Ethereum
- 10^8 wei = 1 ether

#### Smart Contracts
- Programmatic definition of business rules for 2 or more entities to transact with each other
- Written and deployed on blockchain framework.

#### DApps
- Code running on decentralized p2p network.
- DApps = UI + Smart Contracts



## Lecture 4 - 13th August
- Create directory called Ethereum - mkdir ethereum
- Create an environment var called ethereum_home
export VARIABLE_NAME=Path of folder
{export ETHEREUM_HOME=/path}
export ETHEREUM_HOME=/Users/abhinav/ethereum
- check environment variables
printenv
- Create a file genesis.json in your ethereum_home directory


- To init your first ethereum node:

```geth --datadir “$ethereum_home/NUclass” init “<ethereumdir>/genesis.json” [**run once only**]```\
```geth --datadir ”$ethereum_home/NUclass” console 2>console.log```\
```admin. [tab key] to view all options possible with the admin command```\
```admin.nodeInfo - observe the default port and the enode id```\
```personal. [tab key]```\
```personal.newAccount() to create a new account```

- Operations


```personal.listAccounts() to list accounts```\
```eth. [tab key]```\
```eth.blockNumber should return 0 since we are yet to create our first block```\

Create a 2nd node:
```geth --datadir “$ethereum_home/Nuclass-node2” init “<ethereumdir>/genesis.json” [**run once only**]```\

```geth --datadir ”$ethereum_home/Nuclass-node2” --port 30304 --nodiscover -- networkid 1234 console 2>console.log```
[**different port number – also, need to restart first node with same networkid**]

(**On Windows, add --ipcdisable, if you get access denied**)

