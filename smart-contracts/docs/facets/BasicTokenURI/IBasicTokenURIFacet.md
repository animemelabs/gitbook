# IBasicTokenURIFacet

## IBasicTokenURIFacet

Defines the facet for a basic token URI storage implementation. See `setBaseTokenURI` for details.

### tokenURI

```solidity
function tokenURI(uint256 tokenId) external view returns (string)
```

_Returns the Uniform Resource Identifier (URI) for `tokenId` token.
Throws `URIQueryForNonexistentToken` if `tokenId` does not exist._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| tokenId | uint256 | uint256 ID of the token to query. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | string | string URI of given token. |

### baseTokenURI

```solidity
function baseTokenURI() external view returns (string)
```

_Returns the baseTokenURI which is used to construct the tokenURI. See `setBaseTokenURI` for details._

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | string | string The baseTokenURI. |

### setBaseTokenURI

```solidity
function setBaseTokenURI(string baseTokenURI_) external
```

_Sets the baseTokenURI.
The {tokenURI}, by default, is composed of baseTokenURI + tokenId + .json.
Requires `ROLE_ACCESS_CONTROL_ADMIN` membership._

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| baseTokenURI_ | string | The new baseTokenURI, which must end with a forward slash. Example: https://myserver.com/metadata/ |

