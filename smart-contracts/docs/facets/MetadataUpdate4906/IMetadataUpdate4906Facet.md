# IMetadataUpdate4906Facet

## IMetadataUpdate4906Facet

### notifyMetadataUpdated

```solidity
function notifyMetadataUpdated(uint256 tokenId) external
```

Notifies that the metadata for a token has been updated.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| tokenId | uint256 | The id of the token that was updated. |

### notifyBatchMetadataUpdated

```solidity
function notifyBatchMetadataUpdated(uint256 fromTokenId, uint256 toTokenId) external
```

Notifies that the metadata for a range of tokens has been updated.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| fromTokenId | uint256 | The first id of the range of tokens that were updated. |
| toTokenId | uint256 | The last id of the range of tokens that were updated. |

