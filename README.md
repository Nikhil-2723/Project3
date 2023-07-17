# Smart Contract Project
This cricket match contract program tells about the scheduliung and injuries of matches using require(), assert() and revert() statements techniques.
## Description
    This program is a simple contract for cricket matches, providing the details of match scheduling and injuries during the match. It contains three functions that is "Match" 
## Getting Started
### Executing program
       
```javascript
 // SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract Errorhandling {
    bool public Matchtoday = true;
    bool public Medical = false;
    uint finalCall = 0;

    function Match () public {
        require(Matchtoday,"Today is no match!!!");
        finalCall += 3;
    
        assert (finalCall != 0);
    }
    function CancelledMatch() public{
        Matchtoday = !Matchtoday;
    }
    function getCal() public view returns(uint) {
        return finalCall;
    }
    function InjuryHappened () public {
        if(Matchtoday){
            Medical = true;
        }else{
            revert("No medical needed");
        }
    }
}
```
## Authors
Metacrafter Chris  
[@metacraftersio](https://twitter.com/metacraftersio)

## License
This project is licensed under the MIT License
