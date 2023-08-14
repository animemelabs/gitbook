# AccessControlLib

## AccessControlLib

Functionality for access control outside of ROJIVerse.

### RoleAdminChanged

```solidity
event RoleAdminChanged(bytes32 role, bytes32 previousAdminRole, bytes32 newAdminRole)
```

### RoleGranted

```solidity
event RoleGranted(bytes32 role, address account, address sender)
```

### RoleRevoked

```solidity
event RoleRevoked(bytes32 role, address account, address sender)
```

### hasRole

```solidity
function hasRole(bytes32 role, address account) internal view returns (bool)
```

### checkRole

```solidity
function checkRole(bytes32 role, address account) internal view
```

revert if given account does not have given role

#### Parameters

| Name    | Type    | Description   |
| ------- | ------- | ------------- |
| role    | bytes32 | role to query |
| account | address | to query      |

### getRoleAdmin

```solidity
function getRoleAdmin(bytes32 role) internal view returns (bytes32)
```

### setRoleAdmin

```solidity
function setRoleAdmin(bytes32 role, bytes32 adminRole) internal
```

set role as admin role

#### Parameters

| Name      | Type    | Description       |
| --------- | ------- | ----------------- |
| role      | bytes32 | role to set       |
| adminRole | bytes32 | admin role to set |

### grantRole

```solidity
function grantRole(bytes32 role, address account) internal
```

### revokeRole

```solidity
function revokeRole(bytes32 role, address account) internal
```

### renounceRole

```solidity
function renounceRole(bytes32 role) internal
```

relinquish role

#### Parameters

| Name | Type    | Description        |
| ---- | ------- | ------------------ |
| role | bytes32 | role to relinquish |

### getRoleMember

```solidity
function getRoleMember(bytes32 role, uint256 index) internal view returns (address)
```

query role for member at given index

#### Parameters

| Name  | Type    | Description    |
| ----- | ------- | -------------- |
| role  | bytes32 | role to query  |
| index | uint256 | index to query |

### getRoleMemberCount

```solidity
function getRoleMemberCount(bytes32 role) internal view returns (uint256)
```

query role for member count

#### Parameters

| Name | Type    | Description   |
| ---- | ------- | ------------- |
| role | bytes32 | role to query |
