# ERC712UpdateFacetAccessControl

## ERC712UpdateFacet

Implements a means to update the ERC712 name and version. This is restricted to members of ROLE\_ACCESS\_CONTROL\_ADMIN.

### updateERC712NameAndVersion

```solidity
function updateERC712NameAndVersion(string name, string version) external
```

Update the `name` and `symbol` of the NFT contract. When run in a proxy -> diamond scenario this is restricted to the proxy only and will revert on the diamond.

#### Parameters

| Name    | Type   | Description                                    |
| ------- | ------ | ---------------------------------------------- |
| name    | string | The new name used for the Domain Separator.    |
| version | string | The new version used for the Domain Separator. |
