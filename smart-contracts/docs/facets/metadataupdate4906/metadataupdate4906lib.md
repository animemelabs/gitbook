# MetadataUpdate4906Lib

## MetadataUpdate4906Lib

### MetadataUpdate

```solidity
event MetadataUpdate(uint256 tokenId)
```

_This event emits when the metadata of a token is changed. So that the third-party platforms such as NFT market could timely update the images and related attributes of the NFT._

### BatchMetadataUpdate

```solidity
event BatchMetadataUpdate(uint256 fromTokenId, uint256 toTokenId)
```

_This event emits when the metadata of a range of tokens is changed. So that the third-party platforms such as NFT market could timely update the images and related attributes of the NFTs._

### \_notifyMetadataUpdated

```solidity
function _notifyMetadataUpdated(uint256 tokenId) internal
```

_Notifies that the metadata for a token has been updated._

#### Parameters

| Name    | Type    | Description                           |
| ------- | ------- | ------------------------------------- |
| tokenId | uint256 | The id of the token that was updated. |

### \_notifyBatchMetadataUpdated

```solidity
function _notifyBatchMetadataUpdated(uint256 fromTokenId, uint256 toTokenId) internal
```

_Notifies that the metadata for a range of tokens has been updated._

#### Parameters

| Name        | Type    | Description                                            |
| ----------- | ------- | ------------------------------------------------------ |
| fromTokenId | uint256 | The first id of the range of tokens that were updated. |
| toTokenId   | uint256 | The last id of the range of tokens that were updated.  |
