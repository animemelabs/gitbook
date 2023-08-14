# IERC712UpdateFacet

## IERC712UpdateFacet

Exports the EIP712 domain separator and eip712Domain (EIP-5267) methods.
This provides the foundation for ERC-712 support.

### updateERC712NameAndVersion

```solidity
function updateERC712NameAndVersion(string name, string version) external
```

Update the `name` and `symbol` of the NFT contract.
When run in a proxy -> diamond scenario this is restricted to the proxy only and will revert on the diamond.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| name | string | The new name used for the Domain Separator. |
| version | string | The new version used for the Domain Separator. |

