---
layout: post
title : Creating your first Smart Contract in Solidity
subtitle: A short guide to smart contracts, solidity and remix.
categories: Blockchain Development
tags: [Ethereum, Smart Contracts, Solidity Programming]
author: Advait Yadav
banner:
  image:  "/assets/images/banners/solidity-banner-1.jpg"
  heading_style: "font-size: 4.25em; font-weight: bold; text-decoration: underline"
  subheading_style: "color: gold"
---

# <span style="font-size: 4.25em; font-weight: bold; text-decoration: underline"> Creating Your First Smart Contract with Solidity </span>

## <span style="color: gold"> What are Smart Contracts? </span>

Smart contracts are self-executing contracts (programs) with the terms and conditions of an agreement directly written into code.
They run on blockchain technology such as Ethereum, ensuring that the terms of the contract are automatically enforced without the need for any intermediaries.
Smart contracts are programs that govern the behavior of accounts within the Ethereum state.
Smart contracts are a type of Ethereum account. This means they have a balance and can be the target of transactions.
However they're not controlled by a user, instead they are deployed to the network and run as programmed.
User accounts can then interact with a smart contract by submitting transactions that execute a function defined on the smart contract.
Smart contracts can define rules, like a regular contract, and automatically enforce them via the code.
Smart contracts cannot be deleted by default, and interactions with them are irreversible.

## <span style="color: gold"> What is Solidity? </span>

Solidity is an object-oriented, high-level language for implementing smart contracts.
Solidity is statically typed and supports inheritance, libraries, and complex user-defined types, among other features.
With Solidity, you can create contracts for uses such as voting, crowdfunding, blind auctions, and multi-signature wallets.
Smart contracts can be run on a local environment, for this guide we will be using and popular IDE Remix.

## <span style="color: gold"> REMIX IDE </span>

Remix is a popular web-based integrated development environment (IDE) specifically designed for Solidity smart contract development. It's an excellent choice for beginners, as it provides a user-friendly interface and a built-in Ethereum development environment. In this guide, we will walk you through creating your very first smart contract using Remix.

## <span style="color: gold"> Your first smart-contract ( SimpleStorage.sol ) </span>

1. Go to [Remix](https://remix.ethereum.org/)
2. You can check out the existing contracts in the contract folder.
3. In the Remix IDE, create a new file and name it SimpleStorage.sol
4. Write the Solidity code for the smart contract:

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract SimpleStorage {
    uint storedData;

    function set(uint x) public {
        storedData = x;
    }

    function get() public view returns (uint) {
        return storedData;
    }
}
```

The first line tells you that the source code is licensed under MIT. Machine-readable license specifiers are important in a setting where publishing the source code is the default.
The next line specifies that the source code is written for Solidity version 0.8.0, or a newer version of the language. This is to ensure that the contract is not compilable with a new (breaking) compiler version, where it could behave differently. Pragmas are common instructions for compilers about how to treat the source code (e.g. pragma once).
A contract in the sense of Solidity is a collection of code (its functions) and data (its state) that resides at a specific address on the Ethereum blockchain. The line uint storedData; declares a state variable called storedData of type uint (unsigned integer of 256 bits)
The contract defines the functions set and get that can be used to modify or retrieve the value of the variable storedData.

## <span style="color:gold"> Compiling and Deploying Your Smart Contract </span>

Now, let's compile and deploy your smart contract using Remix:

1. In the Remix IDE, go to the "Solidity Compiler" tab on the left.

2. Click the "Compile SimpleStorage.sol" button. Remix will compile your contract.
    ![Compile Contract](/assets/images/banners/compile-contract.png)

3. Head to the "Deploy & Run Transactions" tab. Click on the deploy button.
    ![Deploy Contract](/assets/images/banners/deploy-contract-1.png)

## <span style="color:gold"> Interacting with your smart contract </span>

From the "Deploy" section, select your contract "SimpleStorage". You can put in your value to be stored in storedData and click set to call the function set(). Further click on get to call get() and you will see the value stored in the variable storedData.
    ![Interacting with Contract](/assets/images/banners/deploy-contract-2.png)

## <span style="color: gold"> Conclusion </span>
Congratulations! You have successfully deployed your first ever smart contract!!
I hope this post has helped in building a basic understanding of smart contracts and has incited a fuel to learn more about smart contracts. To further continue your study, you can refer to the links mentioned in references.

## <span style="color:gold"> Further References </span>

### Documentations

- [Solidity Documentation](https://docs.soliditylang.org/en/v0.8.21/introduction-to-smart-contracts.html#simple-smart-contract)

- [Solidity by example](https://solidity-by-example.org/)

- [Satoshi Nakamoto(founder of Bitcoin) paper](https://bitcoin.org/bitcoin.pdf)

### Youtube and other courses

- [Learn Blockchain, Solidity, and Full Stack Web3 Development with JavaScript – 32-Hour Course](https://youtu.be/gyMwXuJrbJQ?si=-IwopmbznCS-rair)

- [Blockchain A-Z: Build a Blockchain, a Crypto + ChatGPT Bonus](https://www.udemy.com/course/build-your-blockchain-az/)
