

# DegenToken

DegenToken is a decentralized token contract built on the Ethereum blockchain using the ERC-20 standard. This contract allows users to mint, transfer, redeem, and burn tokens, while also managing in-store and owned items. The project demonstrates key Solidity concepts and serves as a foundation for more complex blockchain applications.

## Description

DegenToken provides an interface for interacting with tokenized items, where users can redeem tokens for physical items like laptops, smartphones, and tablets. The contract is built with security and ownership in mind, utilizing OpenZeppelin's ERC20 and Ownable standards.

## Getting Started

### Prerequisites

- **Solidity**: Version 0.8.18
- **OpenZeppelin Contracts**: For ERC20 and Ownable implementation

### Executing Program

To interact with the DegenToken contract:

1. **Set up the environment**:
   - Use Remix IDE or any Solidity-compatible development environment.
   - Install OpenZeppelin contracts via Remix or npm if using a local environment.

2. **Compile the Contract**:
   - Ensure the Solidity compiler is set to version 0.8.18.
   - Compile the contract with no errors.

3. **Deploy the Contract**:
   - Deploy the contract to an Ethereum test network (e.g., Ropsten, Rinkeby) or a local blockchain like Ganache.
   - Specify the initial owner during deployment.

4. **Interact with the Contract**:
   - **Mint Tokens**: The owner can mint new tokens to a specified address.
   - **Transfer Tokens**: Users can transfer tokens to other addresses.
   - **Redeem Tokens**: Users can redeem tokens for items, provided they have sufficient balance and item quantity is available.
   - **Burn Tokens**: Users can burn their tokens, reducing the total supply.
   - **View Items**: Users can view in-store item quantities and items they own.

### Example

```solidity
// Example to mint tokens
DegenToken.mint("0xYourAddress", 1000);

// Example to redeem a laptop
DegenToken.redeemTokens(ItemType.Laptop, 1);
```

## Authors

- **Metacrafter Chris** - [@metacraftersio](https://github.com/metacraftersio)

## License

This project is licensed under the MIT License - see the LICENSE.md file for details.

---
**code with ahsan**
