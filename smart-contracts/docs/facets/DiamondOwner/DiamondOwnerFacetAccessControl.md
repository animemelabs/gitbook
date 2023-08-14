# DiamondOwnerFacetAccessControl

## DiamondOwnerFacetAccessControl

Implements the facet for a basic token URI storage implementation. See `setBaseTokenURI` for details.
Requires the `DiamondOrProxyFacet` to be present.

### diamondOwner

```solidity
function diamondOwner() external view returns (address)
```

Get the address of the owner

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | address | The address of the owner. |

### nomineeDiamondOwner

```solidity
function nomineeDiamondOwner() external view returns (address)
```

Get the nominated owner who has permission to call acceptOwnership

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | address | The address of the nominated owner. |

### acceptDiamondOwnership

```solidity
function acceptDiamondOwnership() external
```

Accept transfer of contract ownership

### transferDiamondOwnership

```solidity
function transferDiamondOwnership(address account) external
```

Grants permission to `account` to accept the diamond ownership.
This can only be called on the diamond, never on the proxy.
Requires the caller to be the current owner.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| account | address | The proposed new owner of the diamond. Can be 0 address. |

