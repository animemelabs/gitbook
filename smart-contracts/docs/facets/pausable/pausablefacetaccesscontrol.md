# PausableFacetAccessControl

## PausableFacetAccessControl

This facet implements the pausable functionality. This implementation of the facet requires access control (`AccessControlFacet`).

### paused

```solidity
function paused() public view virtual returns (bool status)
```

query whether contract is paused

#### Return Values

| Name   | Type | Description                |
| ------ | ---- | -------------------------- |
| status | bool | whether contract is paused |

### pause

```solidity
function pause() external
```

pauses the contract

_requires that the contract is not paused_

### unpause

```solidity
function unpause() external
```

unpauses the contract

_requires that the contract is paused_
