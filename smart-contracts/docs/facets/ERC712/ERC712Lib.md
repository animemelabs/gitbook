# ERC712Lib

## ERC712Lib

Contains utility functions for the ERC712 implementation.

### _TYPE_HASH

```solidity
bytes32 _TYPE_HASH
```

### init

```solidity
function init(string name, string version) internal
```

_Initializes the storage with app name and version_

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| name | string | The name of the app as used for the EIP712 domain separator. |
| version | string | The version of the app as used for the EIP712 domain separator. |

### _domainSeparatorV4

```solidity
function _domainSeparatorV4() internal view returns (bytes32)
```

_Returns the domain separator for the current chain._

### _hashTypedDataV4

```solidity
function _hashTypedDataV4(bytes32 structHash) internal view returns (bytes32)
```

_Given an already https://eips.ethereum.org/EIPS/eip-712#definition-of-hashstruct[hashed struct], this
function returns the hash of the fully encoded EIP712 message for this domain.

This hash can be used together with {ECDSA-recover} to obtain the signer of a message. For example:

```solidity
bytes32 digest = _hashTypedDataV4(keccak256(abi.encode(
    keccak256("Mail(address to,string contents)"),
    mailTo,
    keccak256(bytes(mailContents))
)));
address signer = ECDSA.recover(digest, signature);
```_

### _EIP712Name

```solidity
function _EIP712Name() internal view returns (string)
```

_The name parameter for the EIP712 domain.

NOTE: This function reads from storage by default, but can be redefined to return a constant value if gas costs
are a concern._

### _EIP712Version

```solidity
function _EIP712Version() internal view returns (string)
```

_The version parameter for the EIP712 domain.

NOTE: This function reads from storage by default, but can be redefined to return a constant value if gas costs
are a concern._

### _EIP712NameHash

```solidity
function _EIP712NameHash() internal view returns (bytes32)
```

_The hash of the name parameter for the EIP712 domain.

NOTE: In previous versions this function was virtual. In this version you should override `_EIP712Name` instead._

### _EIP712VersionHash

```solidity
function _EIP712VersionHash() internal view returns (bytes32)
```

_The hash of the version parameter for the EIP712 domain.

NOTE: In previous versions this function was virtual. In this version you should override `_EIP712Version` instead._

