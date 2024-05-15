# MyToken Solidity Contract

Welcome to the MyToken contract, a simple token implementation written in Solidity. This contract allows for minting and burning of tokens, providing a basic framework for a cryptocurrency.

## Description

This program is a basic implementation of a custom cryptocurrency token using the Solidity programming language. This contract provides the fundamental features required to mint and burn tokens, allowing for a simple management of token supply. It is designed to be easy to understand and interact with, making it a great starting point for anyone looking to create their own token on an Ethereum-compatible blockchain.

## Getting Started

### Installing

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

### Executing program

1. Access Remix
Go to Remix IDE.

2. Create a New File
In the File Explorer, click on the "+" button to create a new file.
Name the file MyToken.sol.

4. Add the Smart Contract Code
Copy and paste the following Solidity code into the newly created MyToken.sol file:

solidity
     
    // SPDX-License-Identifier: MIT
    pragma solidity 0.8.18;

    contract MyToken {
  
    // public variables here
    string public tokenName = "byte";
    string public tokenAbbrv = "BYT";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;
    
    // mint function
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn(address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
      }
    }

4. Compile the Contract
Navigate to the "Solidity Compiler" tab on the left sidebar.
Ensure the compiler version is set to 0.8.18.
Click the "Compile MyToken.sol" button.
5. Deploy the Contract
Navigate to the "Deploy & Run Transactions" tab on the left sidebar.
Click the "Deploy" button next to MyToken.
6. Interact with the Contract
Once deployed, you can interact with the contract directly from Remix:

In the "Deployed Contracts" section, expand the MyToken contract.
You will see various functions you can call:

* tokenName: View the token name.

* tokenAbbrv: View the token abbreviation.

* totalSupply: View the total supply of tokens.

* balances: Check the balance of a specific address.

* mint: Mint new tokens to an address.

* burn: Burn tokens from an address.

# Example Interactions
### Minting Tokens:
* Enter the address to mint tokens to and the amount of tokens to mint in the mint function fields.
* Click the transact button.

### Burning Tokens:
* Enter the address to burn tokens from and the amount of tokens to burn in the burn function fields.
* Click the transact button.

### Checking Balances:
* Enter the address to check the balance in the balances function field.
* Click the call button.

## Authors

Angela Marie B. Silva

BSIT 2.1


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
