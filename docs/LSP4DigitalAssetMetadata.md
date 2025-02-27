# LSP4DigitalAssetMetadata

*Matthew Stevens*

> LSP4DigitalAssetMetadata



*Implementation of a LSP8 compliant contract.*

## Methods

### getData

```solidity
function getData(bytes32[] _keys) external view returns (bytes[] values)
```

Gets array of data at multiple given `key`



#### Parameters

| Name | Type | Description |
|---|---|---|
| _keys | bytes32[] | the keys which values to retrieve

#### Returns

| Name | Type | Description |
|---|---|---|
| values | bytes[] | The array of data stored at multiple keys

### owner

```solidity
function owner() external view returns (address)
```



*Returns the address of the current owner.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined

### renounceOwnership

```solidity
function renounceOwnership() external nonpayable
```



*Leaves the contract without owner. It will not be possible to call `onlyOwner` functions anymore. Can only be called by the current owner. NOTE: Renouncing ownership will leave the contract without an owner, thereby removing any functionality that is only available to the owner.*


### setData

```solidity
function setData(bytes32[] _keys, bytes[] _values) external nonpayable
```

Sets array of data at multiple given `key`



#### Parameters

| Name | Type | Description |
|---|---|---|
| _keys | bytes32[] | the keys which values to retrieve
| _values | bytes[] | the array of bytes to set.

### supportsInterface

```solidity
function supportsInterface(bytes4 interfaceId) external view returns (bool)
```



*See {IERC165-supportsInterface}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| interfaceId | bytes4 | undefined

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined

### transferOwnership

```solidity
function transferOwnership(address newOwner) external nonpayable
```



*Transfers ownership of the contract to a new account (`newOwner`). Can only be called by the current owner.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| newOwner | address | undefined



## Events

### DataChanged

```solidity
event DataChanged(bytes32 indexed key, bytes value)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| key `indexed` | bytes32 | undefined |
| value  | bytes | undefined |

### OwnershipTransferred

```solidity
event OwnershipTransferred(address indexed previousOwner, address indexed newOwner)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| previousOwner `indexed` | address | undefined |
| newOwner `indexed` | address | undefined |



