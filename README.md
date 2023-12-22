# Degen Token

## Overview

The `degen token` contract is a Solidity smart contract based on the Ethereum blockchain that implements a custom ERC-20 token named "Degen" (symbol: DGN). This token includes additional functionality such as minting, burning, and bonus redemption for various products.

## Features

1. **ERC-20 Token Standard**: The contract follows the ERC-20 standard, providing basic functionalities such as transferring tokens and checking balances.

2. **Ownable Contract**: The contract inherits from the OpenZeppelin `Ownable` contract, ensuring that certain functions can only be executed by the owner of the contract.

3. **Burnable Token**: The contract includes burn functionality, allowing token holders to destroy a specific amount of their tokens, reducing the total supply.

4. **Bonus Redemption System**: Users can redeem bonuses for products (Speaker, Alexa, Laptop) by burning a specified amount of tokens associated with each product.

## Bonus Redemption

The contract introduces a bonus redemption system with the following features:

- **Bonus Enumeration**: Bonus products are identified using an enumeration named `BonusProduct`, including options such as Speaker, Alexa, and Laptop.

- **Bonus Costs and Names**: Each bonus product has an associated cost in terms of tokens and a human-readable name. These values are set during contract deployment.

## Functions

1. **Constructor**: Initializes the contract, mints an initial supply of tokens to the contract owner, and sets up bonus product costs and names.

2. **mint_FN**: Allows the owner to mint additional tokens and assign them to a specified address.

3. **Transfer_FN**: Enables users to transfer tokens to another address.

4. **burn_FN**: Allows users to burn a specified amount of their tokens.

5. **redeemBonusProduct**: Allows users to redeem bonus products by burning the required tokens.

6. **checkPlayerBalance**: Retrieves the token balance of a specified player.

7. **getRewardCost**: Retrieves the cost of a specific bonus product without performing any transactions.

## Example

```solidity
// Deploy the contract
CustomTokenV4 token = new CustomTokenV4();

// Mint 50 tokens to a specific address
token.mint_FN(addressToMint, 50);

// Transfer 10 tokens to another address
token.Transfer_FN(anotherAddress, 10);

// Burn 5 tokens
token.burn_FN(5);

// Redeem Alexa bonus product
token.redeemBonusProduct(CustomTokenV4.BonusProduct.Alexa);

// Check the balance of a player
uint256 playerBalance = token.checkPlayerBalance(playerAddress);
```

## Author

Syed Owaiz

owaiz9866@gmail.com
