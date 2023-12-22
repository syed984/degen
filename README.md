# Token

## Overview

The `CustomTokenV4` contract is a Solidity smart contract based on the Ethereum blockchain that implements a custom ERC-20 token named "Degen" (symbol: DGN). This token includes additional functionality such as minting, burning, and bonus redemption.

## Features

1. **ERC-20 Token Standard**: The contract follows the ERC-20 standard, providing basic functionalities such as transferring tokens and checking balances.

2. **Ownable Contract**: The contract inherits from the OpenZeppelin `Ownable` contract, ensuring that certain functions can only be executed by the owner of the contract.

3. **Burnable Token**: The contract includes burn functionality, allowing token holders to destroy a specific amount of their tokens, reducing the total supply.

4. **Bonus Redemption System**: Users can redeem special bonuses (Early Access, VIP Membership, and Discount Coupon) by burning a specified amount of tokens associated with each bonus.

## Bonus System

The contract introduces a bonus system with the following features:

- **Bonus Enumeration**: Bonuses are identified using an enumeration named `Bonus`, including options such as Early Access, VIP Membership, and Discount Coupon.

- **Bonus Costs and Names**: Each bonus has an associated cost in terms of tokens and a human-readable name. These values are set during contract deployment.

- **Bonus Redemption**: Users can redeem bonuses by calling the `redeemBonus` function, burning the required tokens, and emitting an event to signal the bonus redemption.

## Functions

1. **Constructor**: Initializes the contract, mints an initial supply of tokens to the contract owner, and sets up bonus costs and names.

2. **mintTokens**: Allows the owner to mint additional tokens and assign them to a specified address.

3. **transferTokens**: Enables users to transfer tokens to another address.

4. **burn**: Overrides the OpenZeppelin `ERC20Burnable` function to allow users to burn a specified amount of their tokens.

5. **redeemBonus**: Allows users to redeem bonuses by burning the required tokens.

6. **getPlayerBalance**: Retrieves the token balance of a specified player.

## Events

- **PlayerRewarded**: Signals the reward of tokens to a specific player.
- **BonusRedeemed**: Indicates the redemption of a bonus by a player, including the bonus name and cost.
- **PlayerBalanceChecked**: Logs the checking of the balance for a specific player.

## Usage

1. **Deployment**: Deploy the contract to the Ethereum blockchain.
2. **Token Minting**: Mint additional tokens using the `mintTokens` function if needed.
3. **Transfer Tokens**: Use the `transferTokens` function to transfer tokens between addresses.
4. **Burn Tokens**: Burn tokens using the `burn` function if desired.
5. **Redeem Bonuses**: Users can redeem bonuses by calling the `redeemBonus` function.

## Example

```solidity
// Deploy the contract
CustomTokenV4 token = new CustomTokenV4();

// Mint 50 tokens to a specific address
token.mintTokens(addressToMint, 50);

// Transfer 10 tokens to another address
token.transferTokens(anotherAddress, 10);

// Burn 5 tokens
token.burn(5);

// Redeem VIP Membership bonus
token.redeemBonus(CustomTokenV4.Bonus.VIPMembership);

// Check the balance of a player
uint256 playerBalance = token.getPlayerBalance(playerAddress);
```
