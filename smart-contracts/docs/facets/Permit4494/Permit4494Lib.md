# Permit4494Lib

## Permit4494Lib

Contains utility functions for the permit implementation.

### PERMIT_4494_TYPEHASH

```solidity
bytes32 PERMIT_4494_TYPEHASH
```

### _handleAfterTokenTransfers

```solidity
function _handleAfterTokenTransfers(uint256 startTokenId, uint256 quantity) internal
```

Must be called after the token transfer in the ERC721A implementation
but BEFORE the base code.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| startTokenId | uint256 | The first token id of the transfer |
| quantity | uint256 | The number of tokens transferred. |

### _isValidContractERC1271Signature

```solidity
function _isValidContractERC1271Signature(address signer, bytes32 hash, bytes signature) internal view returns (bool)
```

