
# DegenToken Project

DegenToken is a decentralized token contract built on the Ethereum blockchain using the ERC-20 standard. It provides a platform for minting, transferring, redeeming tokens, checking token balances, and burning tokens.

## Features

### Minting New Tokens

Only the owner of the contract can mint new tokens. Minting allows the platform to create new tokens and distribute them to players as rewards.

```solidity
function mint(address to, uint256 amount) external onlyOwner {
    _mint(to, amount);
}
```

### Transferring Tokens

Players can transfer their tokens to others using the `transferTokens` function.

```solidity
function transferTokens(address recipient, uint256 amount) external {
    _transfer(msg.sender, recipient, amount);
}
```

### Redeeming Tokens

Players can redeem their tokens for items in the in-game store using the `redeemTokens` function.

```solidity
function redeemTokens(ItemType itemType, uint256 quantity) external {
    // Check if the player has sufficient balance and item quantity
    // Update account items and burn the required tokens
}
```


### Burning Tokens

Anyone can burn tokens they own that are no longer needed using the `burnTokens` function.

```solidity
function burnTokens(uint256 amount) external {
    _burn(msg.sender, amount);
}
```

### Viewing In-Store Items

The `viewInStoreItems` function allows users to see the items available in the in-game store along with their quantities.

```solidity
function viewInStoreItems() external view returns (string memory output) {
    // Retrieve and format item quantities
}
```

### Viewing Owned Items

The `viewOwnedItems` function enables users to view items they own along with their quantities.

```solidity
function viewOwnedItems(address account) external view returns (string memory output) {
    // Retrieve and format owned item quantities
}
```

