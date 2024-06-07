# HALCON_MODULE_4_ASSESSMENT

# Building on Avalanche - Module 4
This Solidity program is a simple smart contract program that demonstrates the transaction of ERC20 tokens in Avalanche network for Degen Gaming.

# Description
This program is a smart contract written in Solidity, which will have the function to mint, burn, transfer, redeem DGN Tokens to and from the addresses of the ERC20 tokens in Avalanche Fuji Network.

// SPDX-License-Identifier: MIT

pragma solidity ^0.8.20;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

contract DGNT is ERC20, Ownable {
    uint256[] internal upliftIds;
    mapping(uint256 => Uplift) public uplifts;

    struct Uplift { 
        string upliftName;
        uint256 amount;
    }

    constructor(uint256 initialSupply) ERC20("MyDegenToken", "DT") Ownable(msg.sender) {
        _mint(msg.sender, initialSupply);

        uplifts[1] = Uplift("Scholar Allowance Batch 1", 500);
        uplifts[2] = Uplift("Scholar Allowance Batch 2", 800);
        uplifts[3] = Uplift("Scholar Allowance Batch 3", 1000);

        upliftIds.push(1);
        upliftIds.push(2);
        upliftIds.push(3);
    
    }

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.20" (or another compatible version), and then click on the "Compile DGNToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "DGNToken" contract from the dropdown menu, and then click on the "Deploy" button.


### Authors

Halcon, Divine Louielyn. 
8216021@ntc.edu.ph


Once the contract is deployed, you can interact with it by calling the functions. Finally, click on the "transact" button to execute the function and interact with the contract.
