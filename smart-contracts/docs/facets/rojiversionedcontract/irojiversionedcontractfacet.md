# IROJIVersionedContractFacet

## IROJIVersionedContractFacet

Returns the contract version, starting with 1, of the implementing contract. When inheriting from this contract you need to support EIP-165 as well. The interface id is bytes4 private constant \_INTERFACE\_ID\_ROJI\_VERSIONED\_CONTRACT = bytes4(0xa0a8e460);

### contractVersion

```solidity
function contractVersion() external pure returns (uint32)
```

_Returns the version of the underlying contract._
