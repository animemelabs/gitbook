# AccessControlFacet

## AccessControlFacet

Implements the facet for access control. This version of access control is not tied to
the ROJIVerse access control.

### grantRole

```solidity
function grantRole(bytes32 role, address account) external
```

### hasRole

```solidity
function hasRole(bytes32 role, address account) external view returns (bool)
```

### getRoleAdmin

```solidity
function getRoleAdmin(bytes32 role) external view returns (bytes32)
```

### revokeRole

```solidity
function revokeRole(bytes32 role, address account) external
```

### renounceRole

```solidity
function renounceRole(bytes32 role) external
```

relinquish role

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| role | bytes32 | role to relinquish |

### getRoleMember

```solidity
function getRoleMember(bytes32 role, uint256 index) external view returns (address)
```

Returns one of the accounts that have `role`. `index` must be a
value between 0 and {getRoleMemberCount}, non-inclusive.

Role bearers are not sorted in any particular way, and their ordering may
change at any point.

WARNING: When using {getRoleMember} and {getRoleMemberCount}, make sure
you perform all queries on the same block. See the following
https://forum.openzeppelin.com/t/iterating-over-elements-on-enumerableset-in-openzeppelin-contracts/2296[forum post]
for more information.

### getRoleMemberCount

```solidity
function getRoleMemberCount(bytes32 role) external view returns (uint256)
```

Returns the number of accounts that have `role`. Can be used
together with {getRoleMember} to enumerate all bearers of a role.

