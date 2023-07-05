# Create a Token

This Solidity program is a simple "Create a Token" program that demonstrates will create a contract together to fulfill the following requirements:

1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
2. Your contract will have a mapping of addresses to balances (address => uint)
3. You will have a mint function that takes two parameters: an address and a value. The function then increases the total supply by that number and increases the balance of the address by that amount.
4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. It will take an address and value just like the mint functions. It will then deduct the value from the total supply and from the balance of the address.
5. Lastly, your burn function should have conditionals to make sure the balance of account is greater than or equal to the amount that is supposed to be burned.
## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a multiple functions which will help in creating token.

## Getting Started
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18; // virsion of solidity language has been used


### Executing program


To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., token.sol). Copy and paste the following code into the file:

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;
contract MyToken {

    // public variables here
    string public Token_Name ="crpto";
    string public Token_Abb ="CR";
    uint Total_Supply = 0;


    // mapping variable here

    mapping (address => uint) public balance;

    // mint function

    function mint (address _add, uint _value) public {
        Total_Supply += _value;
        balance [_add] += _value;
    }

    // burn function
    
    function burn(address _add, uint _value) public {
        if (balance[_add]>=_value){
        Total_Supply -= _value;
        balance [_add] -= _value;
    }

}
}



To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile token.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "token" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the public variable with token name= "crpto", token abbr = "CR", and total_supply=0. after that mapping of balance variable with adress will be done. Then copy one adress and Click on the "mint fuction" contract in the left-hand sidebar to add number of token, and then click on the "burn" function to burn the number of token you have burnt on the same adress Finally, click on the "balance" button to the balance available at the smae adress.




