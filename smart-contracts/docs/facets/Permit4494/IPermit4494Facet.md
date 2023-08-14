# IPermit4494Facet

## IPermit4494Facet

### permit

```solidity
function permit(address spender, uint256 tokenId, uint256 deadline, bytes signature) external
```

Function to approve by way of owner signature

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| spender | address | the address to approve |
| tokenId | uint256 | the index of the NFT to approve the spender on |
| deadline | uint256 | a timestamp expiry for the permit |
| signature | bytes | a traditional or EIP-2098 signature |

### nonces

```solidity
function nonces(uint256 tokenId) external view returns (uint256)
```

Returns the nonce of an NFT - useful for creating permits

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| tokenId | uint256 | the index of the NFT to get the nonce of |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | uint256 | the uint256 representation of the nonce |

