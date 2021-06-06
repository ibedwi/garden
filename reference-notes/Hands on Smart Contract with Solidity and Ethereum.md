---
title: Ref - Hands on Smart Contract with Solidity and Ethereum
tags: blockchain solidity
---

## Notes
### Chapter 2 - Decentralized App
- `Tokens`: representasi kepemilikan (proof of ownership)
- With ownership being something that can change often, tracking these changes on a cryptographically secured platform makes a lot of sense.
- Melalui Ethereum Improvement Standard, komunitas Ethereum membuat standar development Ethereum:
	- **ERC-20**
		- The ERC-20 standard is used when creating a fungible, or mutually interchangeable token. These tokens would be ideal replacements for things like rewards points from retailers, miles from airlines, or a currency.
		- Because all the tokens are considered identical, the primary responsibility of an ERC-20 contract is tracking balances.
		- Implementations:
			1. `totalSupply`: jumlah token yang beredar
			2. `balanceOf(addressOwner)`: jumlah balance dari sebuah address
			3. `transfer(address to, uint value)`:  Mengembalikan nilai `true` atau `false` dari status berhasil atau gagalnya sebuah transfer
			4. `transferFrom(address from, address to, uint value)`: sama seperti transfer, tapi pada kasus ini yang melakukan pengecekan bukan pemilik address
			5. `approve`
			6. `allowance`
		- If you ever find yourself working on an application that requires an ERC-20 implementation, you can create an ERC-20 token by defining these functions; however, we recommend using the [OpenZeppelin contracts](https://oreil.ly/ElzWd) as a basis to get started. These contracts have all been thoroughly audited and well documented, making them a great starting place for crafting your own token.
 
	- ERC-721


### Chapter 3 - Before We Get Started
1. Node.js -> provides JS environtment for Truffle
2. Truffle & Ganache (Truffle Suite) -> Provides utilites for testing and deploying contracts. Ganace gives local blockchain development'

#### Install
1. Install parity
2. Install truffle
3. Install ganache


## Part II - Developing Smart Contract

```solidity
pragma solidity >=0.4.0 <0.7.0;

contract Greeter {
    // external => part of our contract's interface and
    // can be called from other contracts, from transactions,
    // but cannot be called from within contract or at least
    // without an explicit reference to the object it is being called on
    function greet() external pure returns (string memory) {
        return "Hello, World";
    }
}
```
1. Function's identifier:
	1.  `external`
	2.  `public`
	3.  `internal`
	4.  `private`

- `address` type
	- `address payable` -> bisa akses method transfer dan send