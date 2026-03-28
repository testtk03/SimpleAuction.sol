# SimpleAuction.sol
Base - Smart Contract Deployed by Remix SimpleAuction.sol
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract SimpleAuction {
    address public highestBidder;
    uint public highestBid;

    function bid() public payable {
        require(msg.value > highestBid, "Bid too low");

        highestBidder = msg.sender;
        highestBid = msg.value;
    }
}
