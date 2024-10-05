# My entry for the IntroETH Assessment in Metacrafters
My creation of 'Quanta', a token made with Solidity.

# Description
In this assessment we were tasked to create a Token using Solidity via Remix IDE.

# Code Details
*for the purpose of ease, the code was set to public.*
- In order to create Quanta, we first have to declare it as a variable which contains its name, name abbreviation and token amount:

      string public tokenName = "QUANTA";
      string public tokenAbbrv = "QTA";
      uint public totalSupply = 0;

- next, we need to make a map for the variable:

       mapping(address => uint) public balances;

- then, we have to implement a minting function for it to record on the blockchain:

      function mint (address _address, uint _value) public {
          totalSupply += _value;
          balances[_address] += _value;
      }

- and lastly, we implemented a burning function for the token for it to have a function to be reduced or destroyed:

       function burn (address _address, uint _value) public {
          if (balances[_address] >= _value) {
              totalSupply -= _value;
              balances[_address] -= _value;
          }
      }

# Author
Lars James Manansala (larsjamesmanansala@gmail.com)
