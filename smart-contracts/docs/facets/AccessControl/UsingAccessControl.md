# UsingAccessControl

## IUsingAccessControl

### MissingRole

```solidity
error MissingRole(bytes32 role, address account)
```

_The caller is not authorized._

## UsingAccessControl

This contract provides modifiers for access control. Inherit from it and use the appropriate modifier.

### _msgSenderROJI

```solidity
function _msgSenderROJI() internal view virtual returns (address)
```

_Returns the sender. This can be overridden if necessary for meta transactions._

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | address | The sender. Defaults to `msg.sender`. |

### onlyAccessControlRole

```solidity
modifier onlyAccessControlRole(bytes32 role)
```

_Ensures that the current sender is in the ROJIVerse `role`._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| role | bytes32 | The role to check for. This checks against the ROJIVerse access control. The sender is retrieved through `_msgSenderROJI()`, which can be overridden in decendent contracts. |

### onlyAccessControlAdmin

```solidity
modifier onlyAccessControlAdmin()
```

_Ensures that the current sender is in the `ROLE_ACCESS_CONTROL_ADMIN` role.
This checks against the contracts access control control. The sender is retrieved through
`_msgSenderROJI()`, which can be overridden in decendent contracts._

### onlyAccessControlFinance

```solidity
modifier onlyAccessControlFinance()
```

_Ensures that the current sender is in the `ROLE_FINANCE` role.
This checks against the contracts access control control. The sender is retrieved through
`_msgSenderROJI()`, which can be overridden in decendent contracts._

### onlyAccessControlOperations

```solidity
modifier onlyAccessControlOperations()
```

_Ensures that the current sender is in the `ROLE_OPERATIONS` role.
This checks against the contracts access control control. The sender is retrieved through
`_msgSenderROJI()`, which can be overridden in decendent contracts._

### onlyAccessControlMetadataUpdate

```solidity
modifier onlyAccessControlMetadataUpdate()
```

_Ensures that the current sender is in the `ROLE_METADATA_UPDATE` role.
This checks against the contracts access control control. The sender is retrieved through
`_msgSenderROJI()`, which can be overridden in decendent contracts._

### onlyAccessControlAdminMinting

```solidity
modifier onlyAccessControlAdminMinting()
```

_Ensures that the current sender is in the `ROLE_ADMIN_MINTING` role.
This checks against the contracts access control control. The sender is retrieved through
`_msgSenderROJI()`, which can be overridden in decendent contracts._

### onlyAccessControlAdminBurning

```solidity
modifier onlyAccessControlAdminBurning()
```

_Ensures that the current sender is in the `ROLE_ADMIN_BURNING` role.
This checks against the contracts access control control. The sender is retrieved through
`_msgSenderROJI()`, which can be overridden in decendent contracts._

