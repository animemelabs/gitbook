# IPausableFacet

## IPausableFacet

This facet defines the pausable functionality.

### paused

```solidity
function paused() external view returns (bool status)
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
