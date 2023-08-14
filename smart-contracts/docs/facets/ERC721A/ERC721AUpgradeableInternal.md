# ERC721AUpgradeableInternal

## ERC721A__IERC721ReceiverUpgradeable

### onERC721Received

```solidity
function onERC721Received(address operator, address from, uint256 tokenId, bytes data) external returns (bytes4)
```

## ERC721AUpgradeableInternal

_Implementation of the [ERC721](https://eips.ethereum.org/EIPS/eip-721)
Non-Fungible Token Standard, including the Metadata extension.
Optimized for lower gas during batch mints.

Token IDs are minted in sequential order (e.g. 0, 1, 2, 3, ...)
starting from `_startTokenId()`.

Assumptions:

- An owner cannot have more than 2**64 - 1 (max value of uint64) of supply.
- The maximum token ID cannot exceed 2**256 - 1 (max value of uint256)._

### _BITMASK_ADDRESS_DATA_ENTRY

```solidity
uint256 _BITMASK_ADDRESS_DATA_ENTRY
```

### _BITPOS_NUMBER_MINTED

```solidity
uint256 _BITPOS_NUMBER_MINTED
```

### _BITPOS_NUMBER_BURNED

```solidity
uint256 _BITPOS_NUMBER_BURNED
```

### _BITPOS_AUX

```solidity
uint256 _BITPOS_AUX
```

### _BITMASK_AUX_COMPLEMENT

```solidity
uint256 _BITMASK_AUX_COMPLEMENT
```

### _BITPOS_START_TIMESTAMP

```solidity
uint256 _BITPOS_START_TIMESTAMP
```

### _BITMASK_BURNED

```solidity
uint256 _BITMASK_BURNED
```

### _BITPOS_NEXT_INITIALIZED

```solidity
uint256 _BITPOS_NEXT_INITIALIZED
```

### _BITMASK_NEXT_INITIALIZED

```solidity
uint256 _BITMASK_NEXT_INITIALIZED
```

### _BITPOS_EXTRA_DATA

```solidity
uint256 _BITPOS_EXTRA_DATA
```

### _BITMASK_EXTRA_DATA_COMPLEMENT

```solidity
uint256 _BITMASK_EXTRA_DATA_COMPLEMENT
```

### _BITMASK_ADDRESS

```solidity
uint256 _BITMASK_ADDRESS
```

### _MAX_MINT_ERC2309_QUANTITY_LIMIT

```solidity
uint256 _MAX_MINT_ERC2309_QUANTITY_LIMIT
```

### _TRANSFER_EVENT_SIGNATURE

```solidity
bytes32 _TRANSFER_EVENT_SIGNATURE
```

### _startTokenId

```solidity
function _startTokenId() internal view virtual returns (uint256)
```

_Returns the starting token ID.
To change the starting token ID, please override this function._

### _nextTokenId

```solidity
function _nextTokenId() internal view virtual returns (uint256)
```

_Returns the next token ID to be minted._

### _totalMinted

```solidity
function _totalMinted() internal view virtual returns (uint256)
```

_Returns the total amount of tokens minted in the contract._

### _totalBurned

```solidity
function _totalBurned() internal view virtual returns (uint256)
```

_Returns the total number of tokens burned._

### _numberMinted

```solidity
function _numberMinted(address owner) internal view returns (uint256)
```

Returns the number of tokens minted by `owner`.

### _numberBurned

```solidity
function _numberBurned(address owner) internal view returns (uint256)
```

Returns the number of tokens burned by or on behalf of `owner`.

### _getAux

```solidity
function _getAux(address owner) internal view returns (uint64)
```

Returns the auxiliary data for `owner`. (e.g. number of whitelist mint slots used).

### _setAux

```solidity
function _setAux(address owner, uint64 aux) internal virtual
```

Sets the auxiliary data for `owner`. (e.g. number of whitelist mint slots used).
If there are multiple variables, please pack them into a uint64.

### _baseURI

```solidity
function _baseURI() internal view virtual returns (string)
```

_Base URI for computing {tokenURI}. If set, the resulting URI for each
token will be the concatenation of the `baseURI` and the `tokenId`. Empty
by default, it can be overridden in child contracts._

### _ownershipOf

```solidity
function _ownershipOf(uint256 tokenId) internal view virtual returns (struct IERC721AUpgradeable.TokenOwnership)
```

_Gas spent here starts off proportional to the maximum mint batch size.
It gradually moves to O(1) as tokens get transferred around over time._

### _ownershipAt

```solidity
function _ownershipAt(uint256 index) internal view virtual returns (struct IERC721AUpgradeable.TokenOwnership)
```

_Returns the unpacked `TokenOwnership` struct at `index`._

### _ownershipIsInitialized

```solidity
function _ownershipIsInitialized(uint256 index) internal view virtual returns (bool)
```

_Returns whether the ownership slot at `index` is initialized.
An uninitialized slot does not necessarily mean that the slot has no owner._

### _initializeOwnershipAt

```solidity
function _initializeOwnershipAt(uint256 index) internal virtual
```

_Initializes the ownership slot minted at `index` for efficiency purposes._

### _packedOwnershipOf

```solidity
function _packedOwnershipOf(uint256 tokenId) internal view returns (uint256 packed)
```

Returns the packed ownership data of `tokenId`.

### _unpackedOwnership

```solidity
function _unpackedOwnership(uint256 packed) internal pure returns (struct IERC721AUpgradeable.TokenOwnership ownership)
```

_Returns the unpacked `TokenOwnership` struct from `packed`._

### _packOwnershipData

```solidity
function _packOwnershipData(address owner, uint256 flags) internal view returns (uint256 result)
```

_Packs ownership data into a single uint256._

### _nextInitializedFlag

```solidity
function _nextInitializedFlag(uint256 quantity) internal pure returns (uint256 result)
```

_Returns the `nextInitialized` flag set if `quantity` equals 1._

### _exists

```solidity
function _exists(uint256 tokenId) internal view virtual returns (bool result)
```

_Returns whether `tokenId` exists.

Tokens can be managed by their owner or approved accounts via {approve} or {setApprovalForAll}.

Tokens start existing when they are minted. See {_mint}._

### _isSenderApprovedOrOwner

```solidity
function _isSenderApprovedOrOwner(address approvedAddress, address owner, address msgSender) internal pure returns (bool result)
```

_Returns whether `msgSender` is equal to `approvedAddress` or `owner`._

### _getApprovedSlotAndAddress

```solidity
function _getApprovedSlotAndAddress(uint256 tokenId) internal view returns (uint256 approvedAddressSlot, address approvedAddress)
```

_Returns the storage slot and value for the approved address of `tokenId`._

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

### _checkContractOnERC721Received

```solidity
function _checkContractOnERC721Received(address from, address to, uint256 tokenId, bytes _data) internal returns (bool)
```

_internal function to invoke {IERC721Receiver-onERC721Received} on a target contract.

`from` - Previous owner of the given token ID.
`to` - Target address that will receive the token.
`tokenId` - Token ID to be transferred.
`_data` - Optional data to send along with the call.

Returns whether the call correctly returned the expected magic value._

### _mint

```solidity
function _mint(address to, uint256 quantity) internal virtual
```

_Mints `quantity` tokens and transfers them to `to`.

Requirements:

- `to` cannot be the zero address.
- `quantity` must be greater than 0.

Emits a {Transfer} event for each mint._

### _mintERC2309

```solidity
function _mintERC2309(address to, uint256 quantity) internal virtual
```

_Mints `quantity` tokens and transfers them to `to`.

This function is intended for efficient minting only during contract creation.

It emits only one {ConsecutiveTransfer} as defined in
[ERC2309](https://eips.ethereum.org/EIPS/eip-2309),
instead of a sequence of {Transfer} event(s).

Calling this function outside of contract creation WILL make your contract
non-compliant with the ERC721 standard.
For full ERC721 compliance, substituting ERC721 {Transfer} event(s) with the ERC2309
{ConsecutiveTransfer} event is only permissible during contract creation.

Requirements:

- `to` cannot be the zero address.
- `quantity` must be greater than 0.

Emits a {ConsecutiveTransfer} event._

### _safeMint

```solidity
function _safeMint(address to, uint256 quantity, bytes _data) internal virtual
```

_Safely mints `quantity` tokens and transfers them to `to`.

Requirements:

- If `to` refers to a smart contract, it must implement
{IERC721Receiver-onERC721Received}, which is called for each safe transfer.
- `quantity` must be greater than 0.

See {_mint}.

Emits a {Transfer} event for each mint._

### _safeMint

```solidity
function _safeMint(address to, uint256 quantity) internal virtual
```

_Equivalent to `_safeMint(to, quantity, '')`._

### _approve

```solidity
function _approve(address to, uint256 tokenId) internal virtual
```

_Equivalent to `_approve(to, tokenId, false)`._

### _ownerOf

```solidity
function _ownerOf(uint256 tokenId) internal view returns (address)
```

### _approve

```solidity
function _approve(address to, uint256 tokenId, bool approvalCheck) internal virtual
```

_Gives permission to `to` to transfer `tokenId` token to another account.
The approval is cleared when the token is transferred.

Only a single account can be approved at a time, so approving the
zero address clears previous approvals.

Requirements:

- `tokenId` must exist.

Emits an {Approval} event._

### _burn

```solidity
function _burn(uint256 tokenId) internal virtual
```

_Equivalent to `_burn(tokenId, false)`._

### _isApprovedForAll

```solidity
function _isApprovedForAll(address owner, address operator) internal view returns (bool)
```

### _burn

```solidity
function _burn(uint256 tokenId, bool approvalCheck) internal virtual
```

_Destroys `tokenId`.
The approval is cleared when the token is burned.

Requirements:

- `tokenId` must exist.

Emits a {Transfer} event._

### _setExtraDataAt

```solidity
function _setExtraDataAt(uint256 index, uint24 extraData) internal virtual
```

_Directly sets the extra data for the ownership data `index`._

### _extraData

```solidity
function _extraData(address from, address to, uint24 previousExtraData) internal view virtual returns (uint24)
```

_Called during each token transfer to set the 24bit `extraData` field.
Intended to be overridden by the cosumer contract.

`previousExtraData` - the value of `extraData` before transfer.

Calling conditions:

- When `from` and `to` are both non-zero, `from`'s `tokenId` will be
transferred to `to`.
- When `from` is zero, `tokenId` will be minted for `to`.
- When `to` is zero, `tokenId` will be burned by `from`.
- `from` and `to` are never both zero._

### _nextExtraData

```solidity
function _nextExtraData(address from, address to, uint256 prevOwnershipPacked) internal view returns (uint256)
```

_Returns the next extra data for the packed ownership data.
The returned result is shifted into position._

### _msgSenderERC721A

```solidity
function _msgSenderERC721A() internal view virtual returns (address)
```

_Returns the message sender (defaults to `msg.sender`).

If you are writing GSN compatible contracts, you need to override this function._

### _toString

```solidity
function _toString(uint256 value) internal pure virtual returns (string str)
```

_Converts a uint256 to its ASCII string decimal representation._

### _revert

```solidity
function _revert(bytes4 errorSelector) internal pure
```

_For more efficient reverts._

