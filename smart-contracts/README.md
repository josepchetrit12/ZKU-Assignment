# Question
## How are smart contracts deployed? List the necessary steps.

Main Steps:
1. Compile the smart contract to get the creation bytecode.
2. Add ethers in your Etheurem account to pay for the gas of the contract deployment transaction
3. Create a deployment script or plugin.
4. Connect to the ethereum node in order to make the contract deployment transaction.

## Is the new design better than having separate confirmReceived and refundSeller? Why or why not?

In terms of gas optimization, yes, because we only have one call to make. But there is a small security problem, if the buyer is a contract, and this contract is programmed in a malicious way, it could have programmed a revert in the transfer call, this would block the ethers of the buyer but also of the seller. By doing it separately you avoid this type of attack, but in terms of gas it is more expensive.


