# DekohDiamondStorage

## DekohDiamondStorage

Storage for the diamond. This storage should only be used for admin level data like intialization status. Put all other data into facets and their storage.

### Layout

```solidity
struct Layout {
  bool initializedV1;
}
```

### STORAGE\_SLOT

```solidity
bytes32 STORAGE_SLOT
```

### layout

```solidity
function layout() internal pure returns (struct DekohDiamondStorage.Layout l)
```
