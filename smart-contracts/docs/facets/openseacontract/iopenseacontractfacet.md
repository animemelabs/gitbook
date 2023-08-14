# IOpenSeaContractFacet

## IOpenSeaContractFacet

### ContractURIUpdated

```solidity
event ContractURIUpdated(string contractURI)
```

Emitted when the receiver has been updated for an NFT contract

#### Parameters

| Name        | Type   | Description                                                                      |
| ----------- | ------ | -------------------------------------------------------------------------------- |
| contractURI | string | The new contract URI. This should point to some file, preferably stored on ipfs. |

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
function contractURI() external view returns (string)
```

Returns the contract URI as used by OpenSea.
