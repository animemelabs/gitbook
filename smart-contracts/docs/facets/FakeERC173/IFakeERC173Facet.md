# IFakeERC173Facet

## IFakeERC173Facet

Exposes an ERC173 ownership facet. The actual ownership is handled differently, this is only used for OpenSea and similar indexers

### OwnershipTransferred

```solidity
event OwnershipTransferred(address previousOwner, address newOwner)
```

_This emits when ownership of a contract changes._

### owner

```solidity
function owner() external view returns (address)
```

Get the address of the owner

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | address | The address of the owner. |

### transferOwnership

```solidity
function transferOwnership(address _newOwner) external
```

Set the address of the new owner of the contract

_Set _newOwner to address(0) to renounce any ownership._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| _newOwner | address | The address of the new owner of the contract |

