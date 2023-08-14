# OpenSeaContractFacetAccessControl

## OpenSeaContractFacetAccessControl

Exposes a contractURI property that is used by opensea to retrieve collection metadata.

### setContractURI

```solidity
function setContractURI(string contractURI_) external
```

Sets the contract URI that is used by opensea to retrieve contract info.

#### Parameters

| Name          | Type   | Description                        |
| ------------- | ------ | ---------------------------------- |
| contractURI\_ | string | The new contract URI. Can be null. |

### contractURI

```solidity
function contractURI() public view returns (string)
```

Returns the contract URI as used by OpenSea.
