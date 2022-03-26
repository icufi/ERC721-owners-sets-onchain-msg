# Overview

This is an ERC-721 contract with on-chain metadata set by the contract owner.

The mint function is controlled by both a pause variable and a call to a seperate ERC-721 contract. In order to mint, the user must own a specified number of tokens from this seperate contract to mint on this contract. During mint on this contract, the mint function initializes a struct with empty strings. This is also a mintForAddress function that allows the user to mint an NFT to a seperate address.

After minting is complete, only the contract owner can then set the struct data for a specified NFT. The struct data includes both metadata, user message and other data. Struct data is accessible by public functions and a tokenURI function which accepts the token ID number and returns metadata encoded Base64.