pragma solidity ^0.8.0; contract MyToken { string public tokenName = "META"; string public tokenAbbrv = "MTA"; uint public totalSupply = 0;

mapping(address => uint) public balances;

constructor() {
    // constructor code
}

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
}# step
