# RolesLib

## RolesLib

A collection of roles used within Animeme Labs contracts.

### ROLE_FINANCE

```solidity
bytes32 ROLE_FINANCE
```

_Role used for anything touching finance (withdrawals, changing royalties etc)_

### ROLE_OPERATIONS

```solidity
bytes32 ROLE_OPERATIONS
```

_Role used for anything touching operations (pause etc) but not the access control admin, which is reserved for ROLE_ACCESS_CONTROL_ADMIN_

### ROLE_METADATA_UPDATE

```solidity
bytes32 ROLE_METADATA_UPDATE
```

_Role used to trigger the metadata update._

### ROLE_ADMIN_MINTING

```solidity
bytes32 ROLE_ADMIN_MINTING
```

_Role used for anything touching manual minting._

### ROLE_ADMIN_BURNING

```solidity
bytes32 ROLE_ADMIN_BURNING
```

_Role used for anything touching manual burning._

### ROLE_ACCESS_CONTROL_ADMIN

```solidity
bytes32 ROLE_ACCESS_CONTROL_ADMIN
```

_Core role for managing access control. Holders of this role cam obtain full access to all
aspects of the contract._

