# MetadataNameSymbolUpdateFacetERC721AAccessControl

## MetadataNameSymbolUpdateFacetERC721AAccessControl

Allows updating the name and symbol of the contract.

### updateNameAndSymbol

```solidity
function updateNameAndSymbol(string name, string symbol) external
```

Update the `name` and `symbol` of the NFT contract. When run in a proxy -> diamond scenario this is restricted to the proxy only and will revert on the diamond.

#### Parameters

| Name   | Type   | Description                                                                                              |
| ------ | ------ | -------------------------------------------------------------------------------------------------------- |
| name   | string | The new name of the contract.                                                                            |
| symbol | string | The new symbol of the contract. It is recommended to keep the length at 11 characters or less, all caps. |
