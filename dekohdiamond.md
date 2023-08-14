# DekohDiamond

## DekohDiamond

### constructor

```solidity
constructor(address _contractOwner, struct IDiamondCut.FacetCut[] _diamondCut, struct Diamond.Initialization[] _initializations) public payable
```

This construct a diamond contract

#### Parameters

| Name              | Type                             | Description                                                                                                                   |
| ----------------- | -------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| \_contractOwner   | address                          | the owner of the contract. With default DiamondCutFacet, this is the sole address allowed to make further cuts.               |
| \_diamondCut      | struct IDiamondCut.FacetCut\[]   | the list of facet to add                                                                                                      |
| \_initializations | struct Diamond.Initialization\[] | the list of initialization pair to execute. This allow to setup a contract with multiple level of independent initialization. |
