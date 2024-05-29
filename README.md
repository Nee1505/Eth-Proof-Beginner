# Create a token

In this Solidity program  we create a token by creating a smart contract. In the contract, we use public variables to store the details of the token like the token_name,token_abbreviation and total supply etc.

## Description

This program is a written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract have two functions-the mint function and the burn function. The mint function takes two parameters: an address and a value. This function increases the total supply by that number and increases the balance of the address by that amount.
The burn function works the opposite of the mint function, as it destroy tokens. It takes an address and value just like the mint functions. It deducts the value from the total supply and from the balance of the address.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Create_token.sol). Copy and paste the following code into the file:

```// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public token_name="HUSKY";
    uint public token_Abbrv=132;
    uint public total_supply= 300;

    // mapping variable here
    mapping(address => uint) public balances;


    // mint function
    function mint(address _x, uint _y) public {
        total_supply += _y;
        balances[_x] += _y;
    }

    // burn function
    function burn(address _x,uint _y) public {
        total_supply -= _y;
        if(balances[_x]>=_y){
        balances[_x] -= _y;
        }
    }

}


```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile Create_token.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mint and burn function. Now, provide the input for the mint and burn functions and then click on transact to get the output.

## Authors

Neelam Rani
