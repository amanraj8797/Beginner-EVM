# MyToken

This is a simple ERC-20 token contract implemented in Solidity. The contract allows for the creation and destruction of tokens, as well as storing information about the token.

## Requirements

1. The contract has public variables that store the details about the coin:
   - `tokenName`: A string representing the name of the token.
   - `tokenAbbrv`: A string representing the abbreviation of the token.
   - `totalSupply`: An unsigned integer representing the total supply of the token.

2. The contract has a mapping of addresses to balances:
   - `balanceOf`: A mapping that associates addresses with their corresponding token balances.

3. The contract has a `mint` function that increases the total supply and the balance of the "sender" address by a given value:
   - Parameters:
     - `_to`: The address to which the tokens will be minted.
     - `_amount`: The amount of tokens to be minted.
   - Actions:
     - Increase the `totalSupply` by `_amount`.
     - Increase the balance of the `_to` by `_amount`.

4. The contract has a `burn` function that decreases the total supply and the balance of the "sender" address by a given value:
   - Parameters:
     - `_from`: The address from which the tokens will be burned.
     - `_amount`: The amount of tokens to be burned.
   - Actions:
     - Check if the balance of the `_to` is greater than or equal to `_amount`.
     - If true, decrease the `totalSupply` by `_amount`.
     - Decrease the balance of the `_from` by `_amount`.

## Usage

1. Deploy the `MyToken` contract to a supported Ethereum network.

2. Once deployed, you can interact with the contract by calling the following functions:

   - `mint`: Creates new tokens and assigns them to a specified address.
     - Parameters:
       - `_to`: The address to which the tokens will be minted.
       - `_amount`: The amount of tokens to be minted.

   - `burn`: Destroys existing tokens by reducing the total supply and the balance of a specified address.
     - Parameters:
       - `_from`: The address from which the tokens will be burned.
       - `_amount`: The amount of tokens to be burned.

## Authors

Aman Raj  

## License

This contract is licensed under the MIT License. SPDX-License-Identifier: MIT.

