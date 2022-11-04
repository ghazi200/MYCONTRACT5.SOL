// SPDX - LINCENSE - Identifier: GPL-3.0 

pragma solidity ^0.8.4;

contract MyContract { 
    enum State {Waiting, Ready, Active}
    State public state;
    
    constructor() public {
      state = State.Waiting;

    }

    function activate() public {
        state = State.Active;
    }

    function isActive() public view returns(bool) {
        return state == State.Active;
    }
}
    
