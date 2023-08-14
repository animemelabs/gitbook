# ERC712Storage

## ERC712Storage

Storage for the ERC712 implementation.
Based upon OpenZeppelin's ERC712 implementation.

### Layout

```solidity
struct Layout {
  bytes32 _hashedName;
  bytes32 _hashedVersion;
  string _name;
  string _version;
}
```

### STORAGE_SLOT

```solidity
bytes32 STORAGE_SLOT
```

### layout

```solidity
function layout() internal pure returns (struct ERC712Storage.Layout l)
```

