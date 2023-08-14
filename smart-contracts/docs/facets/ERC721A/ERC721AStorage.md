# ERC721AStorage

## ERC721AStorage

### TokenApprovalRef

```solidity
struct TokenApprovalRef {
  address value;
}
```

### Layout

```solidity
struct Layout {
  uint256 _currentIndex;
  uint256 _burnCounter;
  string _name;
  string _symbol;
  mapping(uint256 => uint256) _packedOwnerships;
  mapping(address => uint256) _packedAddressData;
  mapping(uint256 => struct ERC721AStorage.TokenApprovalRef) _tokenApprovals;
  mapping(address => mapping(address => bool)) _operatorApprovals;
}
```

### STORAGE_SLOT

```solidity
bytes32 STORAGE_SLOT
```

### layout

```solidity
function layout() internal pure returns (struct ERC721AStorage.Layout l)
```

