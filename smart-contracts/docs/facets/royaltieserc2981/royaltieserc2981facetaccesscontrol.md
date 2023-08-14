# RoyaltiesERC2981FacetAccessControl

## RoyaltiesERC2981FacetAccessControl

_Inherits storage layout of ERC2981Storage. This facet uses access control._

### royaltyInfo

```solidity
function royaltyInfo(uint256 tokenId, uint256 salePrice) public view returns (address, uint256)
```

#### Parameters

| Name      | Type    | Description |
| --------- | ------- | ----------- |
| tokenId   | uint256 |             |
| salePrice | uint256 |             |

#### Return Values

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \[0] | address |             |
| \[1] | uint256 |             |

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
