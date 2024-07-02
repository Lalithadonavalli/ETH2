CustomToken Solidity Contract

Overview
CustomToken is a simple ERC20-like smart contract implemented in Solidity that allows minting and burning of tokens. The contract maintains the total supply of tokens and the balances of individual addresses.

Features

Token Details: The contract stores the name and abbreviation of the token.
Minting: Increase the total supply and balance of a specified address.
Burning: Decrease the total supply and balance of a specified address, ensuring that the address has enough balance to burn.
Token Details
Token Name: Custom Coin
Token Abbreviation: CC
Functions
mint(address _address, uint _value)
Increases the total supply of tokens and the balance of the specified address.

Parameters:

_address: The address to which the tokens will be minted.
_value: The amount of tokens to mint.
Behavior:

Increases the totalSupply by _value.
Increases the balance of _address by _value.
burn(address _address, uint _value)
Decreases the total supply of tokens and the balance of the specified address.

Parameters:

_address: The address from which the tokens will be burned.
_value: The amount of tokens to burn.
Behavior:

Requires that the balance of _address is greater than or equal to _value.
Decreases the totalSupply by _value.
Decreases the balance of _address by _value.
Error:

Reverts the transaction with the message "Insufficient balance to burn" if _address does not have enough tokens.
Public Variables
string public tokenName: The name of the token.
string public tokenAbbrv: The abbreviation of the token.
uint public totalSupply: The total supply of the token.
mapping(address => uint) public balances: A mapping that stores the balances of each address.
