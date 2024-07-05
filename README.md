# MyToken


## Description

MyToken is a simple Ethereum smart contract for a basic ERC20-like token. It allows minting and burning of tokens and keeps track of balances associated with addresses. The token is named "Eclipse" and has the abbreviation "Ecl".

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

```javascript
pragma solidity ^0.8.4;

contract MyToken {
    string public tokenName = "Eclipse";
    string public tokenAbbrv = "Ecl";
    uint public totalSupply = 0;

    mapping(address => uint) public balances;

    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    function burn(address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}


```

To compile the code, Click on the "Solidity Compiler" tab in the left-hand sidebar.
Make sure the "Compiler" option is set to "0.8.4" (or another compatible version).
Click on the "Compile MyToken.sol" button.


Click on the "Deploy & Run Transactions" tab in the left-hand sidebar.
Select the "MyToken" contract from the dropdown menu.
Click on the "Deploy" button.


Click on the "MyToken" contract in the left-hand sidebar.
Use the available functions (mint and burn) to interact with the contract.
## Authors

Yuvraj Singh  
[@uvcodes69](https://github.com/uvcodes69)


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
