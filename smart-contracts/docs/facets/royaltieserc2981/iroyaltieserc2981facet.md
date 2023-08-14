# IRoyaltiesERC2981Facet

## IRoyaltiesERC2981Facet

_Interface for the NFT Royalty Standard https://eips.ethereum.org/EIPS/eip-2981_

### DefaultRoyaltyReceiverIsNull

```solidity
error DefaultRoyaltyReceiverIsNull()
```

_Emitted when the defaultRoyaltyReceiver parameter is set to null._

### RoyaltyBPSExceedsMax

```solidity
error RoyaltyBPSExceedsMax()
```

_Emitted when the defaultRoyaltyBPS parameter is above 10000._

### DefaultRoyaltyChanged

```solidity
event DefaultRoyaltyChanged(address oldDefaultRoyaltyReceiver, address newDefaultRoyaltyReceiver, uint16 oldDefaultRoyaltyBPS, uint16 newDefaultRoyaltyBPS)
```

Emitted when the royalties tier has changed.

#### Parameters

| Name                      | Type    | Description            |
| ------------------------- | ------- | ---------------------- |
| oldDefaultRoyaltyReceiver | address | The previous receiver. |
| newDefaultRoyaltyReceiver | address | The new receiver.      |
| oldDefaultRoyaltyBPS      | uint16  | The previous BPS.      |
| newDefaultRoyaltyBPS      | uint16  | The new BPS.           |

### royaltyInfo

```solidity
function royaltyInfo(uint256 _tokenId, uint256 _salePrice) external view returns (address receiver, uint256 royaltyAmount)
```

#### Parameters

| Name        | Type    | Description                                              |
| ----------- | ------- | -------------------------------------------------------- |
| \_tokenId   | uint256 | - the NFT asset queried for royalty information          |
| \_salePrice | uint256 | - the sale price of the NFT asset specified by \_tokenId |

#### Return Values

| Name          | Type    | Description                                         |
| ------------- | ------- | --------------------------------------------------- |
| receiver      | address | - address of who should be sent the royalty payment |
| royaltyAmount | uint256 | - the royalty payment amount for \_salePrice        |

### setDefaultRoyalty

```solidity
function setDefaultRoyalty(address defaultRoyaltyReceiver, uint16 defaultRoyaltyBPS) external
```

Sets the default royalty receiver and default royalty base points (1/100 of a percent).

#### Parameters

| Name                   | Type    | Description                                                  |
| ---------------------- | ------- | ------------------------------------------------------------ |
| defaultRoyaltyReceiver | address | The account that receives the royalties.                     |
| defaultRoyaltyBPS      | uint16  | The base points (1/100 of a percent) of the default royalty. |
