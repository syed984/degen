# DegenToken

DegenToken is a basic ERC-20 token contract written in Solidity. It provides functionalities for minting, transferring, burning tokens, and redeeming bonus products.

## Overview

This token contract includes the following features:

- **Minting:** The owner can mint new tokens and distribute them to specific addresses.

- **Transferring:** Token holders can transfer their tokens to other addresses.

- **Burning:** Token holders can burn their tokens, reducing the total supply.

- **Redeeming Bonus Products:** Users can redeem bonus products (Early Access, VIP Membership, Smartphone) in exchange for a specified amount of tokens.

## Bonus Products

The contract defines the following bonus products:

- **Early Access**
  - Cost: 250 tokens

- **VIP Membership**
  - Cost: 300 tokens

- **Smartphone**
  - Cost: 200 tokens

## Usage

### Deployment

1. Deploy the contract to the Ethereum blockchain.
2. The contract owner initially receives 100 tokens.

### Minting Tokens

- Use the `mintTokens` function to mint tokens and distribute them to a specified address.

### Transferring Tokens

- Use the `transferTokens` function to transfer tokens from one address to another.

### Burning Tokens

- Use the `burnTokens` function to burn a specific amount of tokens, reducing the total supply.

### Redeeming Bonus Products

- Use the `redeemBonusProduct` function to redeem a bonus product by burning the required number of tokens.

### Checking Player Balance

- Use the `checkPlayerBalance` function to check the token balance of a specific address.

### Getting Reward Cost

- Use the `getRewardCost` function to retrieve the cost in tokens for a specific bonus product.

## Example

Here's a simple example of using the contract in a JavaScript environment:

```javascript
// Deploy the contract and get the contract instance

// Mint tokens to a specific address

// Transfer tokens to another address

// Burn a specific amount of tokens

// Redeem a bonus product by burning tokens
```
## Author

Syed owaiz

owaiz9866@gmail.com
