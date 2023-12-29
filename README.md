# Redeem Token 

This repository contains a Solidity smart contract named `redeemToken` that serves as an ERC20 token with additional features for minting, transferring, burning, pausing, and redeeming vouchers. The contract is implemented using OpenZeppelin libraries for ERC20, Ownable, ERC20Burnable, and Pausable functionalities.

## Overview

### ERC20 Token
The `redeemToken` contract is an ERC20-compliant token with the name "DEGEN" and symbol "DGN." It includes features such as minting, transferring, and burning tokens.

### Vouchers
The contract introduces a voucher system, allowing users to redeem specific vouchers in exchange for tokens. Each voucher has a unique name and a corresponding token cost.

### Owner Control
The contract is initially owned by the deployer (owner), providing exclusive access to certain functions such as minting tokens, modifying vouchers, and emergency pausing of the contract.

### Pausing Mechanism
The contract includes a pausing mechanism using OpenZeppelin's `Pausable` module, allowing the owner to pause and unpause certain functions in emergency situations.

## Functionality

### 1. Mint Tokens
The owner can mint additional tokens to a specified address using the `mint` function.

### 2. Transfer Tokens
Token holders can transfer tokens to another address using the standard ERC20 `transfer` function.

### 3. Burn Tokens
Token holders can burn their own tokens using the `burn` function, provided they have sufficient funds.

### 4. Redeem Voucher
Users can redeem vouchers using the `redeemVoucher` function. The cost of the voucher in tokens is deducted from the user's balance, and the voucher is recorded as redeemed.

### 5. Modify Voucher Name
The owner can modify the name of a voucher using the `modifyVoucherName` function. This is useful for updating voucher names while preserving their associated costs.

### 6. Emergency Pause Contract
The owner can pause and unpause the contract using the `emergencyPauseContract` function, provided by the `Pausable` module. This feature is designed for emergency situations to temporarily halt specific contract functions.

## Events

The contract emits one custom event:
1. `LogMessage`: Logs generic messages for various operations.

## Initialization

The contract initializes with four predefined vouchers: "Discount50," "FreeBurger," "ComboDeal," and "FreeDrink," each with a unique token cost.

## License

This smart contract is licensed under the MIT License. See the provided `LICENSE` file for details.
