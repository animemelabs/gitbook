# OperatorFiltererLib

## OperatorFiltererLib

Contains functionality to implement operator filtering.

### OPERATOR_FILTER_REGISTRY

```solidity
contract IOperatorFilterRegistry OPERATOR_FILTER_REGISTRY
```

### CANONICAL_OPERATOR_FILTER_REGISTRY_ADDRESS

```solidity
address CANONICAL_OPERATOR_FILTER_REGISTRY_ADDRESS
```

### CANONICAL_CORI_SUBSCRIPTION

```solidity
address CANONICAL_CORI_SUBSCRIPTION
```

### _checkFilterOperator

```solidity
function _checkFilterOperator(address operator) internal view
```

_A helper function to check if the operator is allowed._

### _init

```solidity
function _init() internal
```

_Initializes with the default registry and subscribes._

### _register

```solidity
function _register(address subscriptionOrRegistrantToCopy, bool subscribe) internal
```

_Registers the contract with the registry.
This must be called from the proxy._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| subscriptionOrRegistrantToCopy | address | Provide a valid subscription address to copy the subscriptions from or the 0 address. |
| subscribe | bool | registers and subscribes |

### _unregister

```solidity
function _unregister() internal
```

_Unregisters the contract from the registry._

