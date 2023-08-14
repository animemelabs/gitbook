# IERC712Facet

## IERC712Facet

Exports the EIP712 domain separator and eip712Domain (EIP-5267) methods. This provides the foundation for ERC-712 support.

### DOMAIN\_SEPARATOR

```solidity
function DOMAIN_SEPARATOR() external view returns (bytes32)
```

Returns the domain separator used in the encoding of the signature for permits, as defined by EIP-712

#### Return Values

| Name | Type    | Description                  |
| ---- | ------- | ---------------------------- |
| \[0] | bytes32 | the bytes32 domain separator |

### eip712Domain

```solidity
function eip712Domain() external view returns (bytes1 fields, string name, string version, uint256 chainId, address verifyingContract, bytes32 salt, uint256[] extensions)
```

_See {EIP-5267}._
