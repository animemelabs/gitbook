# ERC721AUpgradeableFacet

## ERC721A__IERC721ReceiverUpgradeable

_Interface of ERC721 token receiver._

### onERC721Received

```solidity
function onERC721Received(address operator, address from, uint256 tokenId, bytes data) external returns (bytes4)
```

## ERC721AUpgradeableFacet

_Implementation of the [ERC721](https://eips.ethereum.org/EIPS/eip-721)
Non-Fungible Token Standard, including the Metadata extension.
Optimized for lower gas during batch mints.

Token IDs are minted in sequential order (e.g. 0, 1, 2, 3, ...)
starting from `_startTokenId()`.

Assumptions:

- An owner cannot have more than 2**64 - 1 (max value of uint64) of supply.
- The maximum token ID cannot exceed 2**256 - 1 (max value of uint256)._

### totalSupply

```solidity
function totalSupply() public view virtual returns (uint256)
```

_Returns the total number of tokens in existence.
Burned tokens will reduce the count.
To get the total number of tokens minted, please see {_totalMinted}._

### balanceOf

```solidity
function balanceOf(address owner) public view virtual returns (uint256)
```

_Returns the number of tokens in `owner`'s account._

### name

```solidity
function name() public view virtual returns (string)
```

_Returns the token collection name._

### symbol

```solidity
function symbol() public view virtual returns (string)
```

_Returns the token collection symbol._

### ownerOf

```solidity
function ownerOf(uint256 tokenId) public view virtual returns (address)
```

_Returns the owner of the `tokenId` token.

Requirements:

- `tokenId` must exist._

### approve

```solidity
function approve(address to, uint256 tokenId) public payable virtual
```

_Gives permission to `to` to transfer `tokenId` token to another account. See {ERC721A-_approve}.

Requirements:

- The caller must own the token or be an approved operator._

### getApproved

```solidity
function getApproved(uint256 tokenId) public view virtual returns (address)
```

_Returns the account approved for `tokenId` token.

Requirements:

- `tokenId` must exist._

### setApprovalForAll

```solidity
function setApprovalForAll(address operator, bool approved) public virtual
```

_Approve or remove `operator` as an operator for the caller.
Operators can call {transferFrom} or {safeTransferFrom}
for any token owned by the caller.

Requirements:

- The `operator` cannot be the caller.

Emits an {ApprovalForAll} event._

### isApprovedForAll

```solidity
function isApprovedForAll(address owner, address operator) public view virtual returns (bool)
```

_Returns if the `operator` is allowed to manage all of the assets of `owner`.

See {setApprovalForAll}._

### transferFrom

```solidity
function transferFrom(address from, address to, uint256 tokenId) public payable virtual
```

_Transfers `tokenId` from `from` to `to`.

Requirements:

- `from` cannot be the zero address.
- `to` cannot be the zero address.
- `tokenId` token must be owned by `from`.
- If the caller is not `from`, it must be approved to move this token
by either {approve} or {setApprovalForAll}.

Emits a {Transfer} event._

### safeTransferFrom

```solidity
function safeTransferFrom(address from, address to, uint256 tokenId) public payable virtual
```

_Equivalent to `safeTransferFrom(from, to, tokenId, '')`._

### safeTransferFrom

```solidity
function safeTransferFrom(address from, address to, uint256 tokenId, bytes _data) public payable virtual
```

_Safely transfers `tokenId` token from `from` to `to`.

Requirements:

- `from` cannot be the zero address.
- `to` cannot be the zero address.
- `tokenId` token must exist and be owned by `from`.
- If the caller is not `from`, it must be approved to move this token
by either {approve} or {setApprovalForAll}.
- If `to` refers to a smart contract, it must implement
{IERC721Receiver-onERC721Received}, which is called upon a safe transfer.

Emits a {Transfer} event._

### _afterTokenTransfers

```solidity
function _afterTokenTransfers(address from, address to, uint256 startTokenId, uint256 quantity) internal virtual
```

_Hook that is called after a set of serially-ordered token IDs
have been transferred. This includes minting.
And also called after one token has been burned.

`startTokenId` - the first token ID to be transferred.
`quantity` - the amount to be transferred.

Calling conditions:

- When `from` and `to` are both non-zero, `from`'s `tokenId` has been
transferred to `to`.
- When `from` is zero, `tokenId` has been minted for `to`.
- When `to` is zero, `tokenId` has been burned by `from`.
- `from` and `to` are never both zero._

### _beforeTokenTransfers

```solidity
function _beforeTokenTransfers(address from, address to, uint256 startTokenId, uint256 quantity) internal virtual
```

_Hook that is called before a set of serially-ordered token IDs
are about to be transferred. This includes minting.
And also called before burning one token.

`startTokenId` - the first token ID to be transferred.
`quantity` - the amount to be transferred.

Calling conditions:

- When `from` and `to` are both non-zero, `from`'s `tokenId` will be
transferred to `to`.
- When `from` is zero, `tokenId` will be minted for `to`.
- When `to` is zero, `tokenId` will be burned by `from`.
- `from` and `to` are never both zero._

