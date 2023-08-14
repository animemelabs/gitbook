# AdminMinterERC721AFacetAccessControl

## AdminMinterERC721AFacetAccessControl

Minting facet implementation for 1155 NFTs for admins.

### adminMint

```solidity
function adminMint(address to, uint256 quanity) external
```

Mints an 1155 NFT with the specified quantity.

#### Parameters

| Name    | Type    | Description                                                                                                            |
| ------- | ------- | ---------------------------------------------------------------------------------------------------------------------- |
| to      | address | The address that should receive the NFT. If this is a contract, then the contract must be ERC1155 receiver conforming. |
| quanity | uint256 | The quanity of the tokens to mint.                                                                                     |
