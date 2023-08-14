# IWithdrawFacet

## IWithdrawFacet

Provides the ability to withdraw funds from the contract. This is used as 'Black Hole Protection' to be able to refund users who inadvertently send funds or tokens to the contract.

### CantWithdrawTokenOfContractItself

```solidity
error CantWithdrawTokenOfContractItself()
```

### withdraw

```solidity
function withdraw() external
```

Withdraws ETH from the contract.

_This is to be used to withdraw the ETH that was sent to the contract as payment for the NFTs._

### withdrawERC20

```solidity
function withdrawERC20(address tokenAddress) external
```

Withdraws ERC20 tokens from the contract.

_This is to be used to withdraw the ERC20 tokens (USDC, etc) that were sent to the contract as payment for the NFTs._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| tokenAddress | address | The address of the ERC20 token contract. |

### withdrawERC721

```solidity
function withdrawERC721(address tokenAddress, uint256 tokenId) external
```

Blackhole protection against accidentally transferred NFTs.

_This is a fallback in case the contract receives 721 NFTs directly._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| tokenAddress | address | The address of the NFT contract. |
| tokenId | uint256 | The ID of the NFT to withdraw. |

### withdrawERC1155

```solidity
function withdrawERC1155(address tokenAddress, uint256 tokenId) external
```

Blackhole protection against accidentally transferred NFTs.

_This is a fallback in case the contract receives 1155 NFTs directly._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| tokenAddress | address | The address of the NFT contract. |
| tokenId | uint256 | The ID of the NFT to withdraw. |

