## assignment1 - Add god mode to an ERC20 token

God mode on an ERC20 token allows a special address to steal other people’s funds, create tokens, and destroy tokens. Implement the following functions:

`mintTokensToAddress(address recipient)`

`reduceTokensAtAddress(address target)`

`authoritativeTransferFrom(address from, address to)`

<br>

## assignment2 - ERC20 with sanctions

Congratulations! The government wants to use your smart contract ERC20 tokens now for transferring economic value!

However, they require the ability to prevent transfers to blacklisted addresses from occurring, and they want addresses on a blacklist to not be able to transfer their funds until they are removed from the blacklist.

Hint: what is the appropriate data structure to store this blacklist?

Hint: make sure only the government can control this list!

Hint: if you chose to use the OpenZeppelin implementation, study the function here: https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/ERC20.sol#L358

<br>

## assignment3: Token sale with ethereum

Add a function where users can mint 1000 tokens if they pay 1 ether.

IMPORTANT: your token should have 18 decimal places as is standard in ERC20 tokens

IMPORTANT: your total supply should not exceed 1 million tokens. The sale should close after 1 million tokens have been minted

IMPORTANT: you must have a function to withdraw the ethereum from the contract to your address

<br>

## assignment4

WARNING! THIS ASSIGNMENT IS TRICKIER THAN THE EARLIER ONES.

Take what you did in assignment 4 and give the users the ability to transfer their tokens to the contract and receive 0.5 ether for every 1000 tokens they transfer.

ERC20 tokens don’t have the ability to trigger functions on smart contracts. Users need to give the smart contract approval to withdraw their ERC20 tokens from their balance.

See here: https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/ERC20.sol#L136

The smart contract should block the transaction if the smart contract does not have enough ether to pay the user.

If another user wants to buy tokens from the contract, and the supply has already been used up, and the contract is holding tokens that other people sent in, it must sell them those tokens at the original price of 1 ether per 1000 tokens.
