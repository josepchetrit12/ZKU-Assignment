# Questions
## What is a hash? Why do people use hashing to hide information?

A hash is a cryptographic function, this function takes an input of any length, and with that input it makes the hash, after making the hash you get an output with a fixed size (normally 256 bits). 

People use it to hide information, because if you only have the output it is "impossible" to find the input. But if you hash the same input again you always get the same output.

## What is a smart contract?

In ethereum, smart contracts are a type of account in Etheurem (called a contract account), it is simply a program that runs on the Ethereum blockchain, this program has functions and storage variables that give the state of this contract , this program has a specific address on the blockchain.  

The smart contract does not execute itself, we always need an EOA account to pay gas fees to call functions of that contract.

## What are gas fees? Why is gas optimization a big focus when building smart contracts?

On ethereum, if you want to call a contract or make a transaction, this is not free, it requires computational resources to execute, the gas is the amount of computational effort required to execute this call in EVM.

The gas fee is what you have to pay in ethers for this call, The following formula describes how to calculate this gas fee:
```math
gas fee = gas units * gas price per unit}
```

Optimization in smart contracts is very important, because today the gas fees in ethereum are very high, and you need to optimize as much as possible to pay less fees for calls in a smart contract.