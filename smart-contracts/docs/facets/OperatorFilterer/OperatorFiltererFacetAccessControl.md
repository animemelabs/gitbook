# OperatorFiltererFacetAccessControl

## OperatorFiltererFacetAccessControl

### registerOperatorFilterer

```solidity
function registerOperatorFilterer(address subscriptionOrRegistrantToCopy, bool subscribe) external
```

Registers the contract with the registry.
This must be called from the proxy.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| subscriptionOrRegistrantToCopy | address | Provide a valid subscription address to copy the subscriptions from or the 0 address. |
| subscribe | bool | registers and subscribes |

### unregisterOperatorFilterer

```solidity
function unregisterOperatorFilterer() external
```

Unregisters the contract from the registry.

