# LSP9VaultCore

*Fabian Vogelsteller, Yamen Merhi, Jean Cavallera*

> Core Implementation of LSP9Vault built on top of ERC725, LSP1UniversalReceiver



*Could be owned by a UniversalProfile and able to register received asset with UniversalReceiverDelegateVault*

## Methods

### execute

```solidity
function execute(uint256 _operation, address _to, uint256 _value, bytes _data) external payable returns (bytes result)
```

Executes any other smart contract. Is only callable by the owner.



#### Parameters

| Name | Type | Description |
|---|---|---|
| _operation | uint256 | the operation to execute: CALL = 0; CREATE = 1; CREATE2 = 2; STATICCALL = 3; DELEGATECALL = 4;
| _to | address | the smart contract or address to interact with. `_to` will be unused if a contract is created (operation 1 and 2)
| _value | uint256 | the value of ETH to transfer
| _data | bytes | the call data, or the contract data to deploy

#### Returns

| Name | Type | Description |
|---|---|---|
| result | bytes | undefined

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



*Sets array of data at multiple given `key` SHOULD only be callable by the owner of the contract set via ERC173 and the UniversalReceiverDelegate Emits a {DataChanged} event.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _keys | bytes32[] | undefined
| _values | bytes[] | undefined

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



*Transfer the ownership and notify the vault sender and vault receiver*

#### Parameters

| Name | Type | Description |
|---|---|---|
| newOwner | address | undefined

### universalReceiver

```solidity
function universalReceiver(bytes32 _typeId, bytes _data) external nonpayable returns (bytes returnValue)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| _typeId | bytes32 | undefined
| _data | bytes | undefined

#### Returns

| Name | Type | Description |
|---|---|---|
| returnValue | bytes | undefined



## Events

### ContractCreated

```solidity
event ContractCreated(uint256 indexed _operation, address indexed _contractAddress, uint256 indexed _value)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| _operation `indexed` | uint256 | undefined |
| _contractAddress `indexed` | address | undefined |
| _value `indexed` | uint256 | undefined |

### DataChanged

```solidity
event DataChanged(bytes32 indexed key, bytes value)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| key `indexed` | bytes32 | undefined |
| value  | bytes | undefined |

### Executed

```solidity
event Executed(uint256 indexed _operation, address indexed _to, uint256 indexed _value, bytes _data)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| _operation `indexed` | uint256 | undefined |
| _to `indexed` | address | undefined |
| _value `indexed` | uint256 | undefined |
| _data  | bytes | undefined |

### OwnershipTransferred

```solidity
event OwnershipTransferred(address indexed previousOwner, address indexed newOwner)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| previousOwner `indexed` | address | undefined |
| newOwner `indexed` | address | undefined |

### UniversalReceiver

```solidity
event UniversalReceiver(address indexed from, bytes32 indexed typeId, bytes indexed returnedValue, bytes receivedData)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| from `indexed` | address | undefined |
| typeId `indexed` | bytes32 | undefined |
| returnedValue `indexed` | bytes | undefined |
| receivedData  | bytes | undefined |

### ValueReceived

```solidity
event ValueReceived(address indexed sender, uint256 indexed value)
```

Emitted when a native token is received



#### Parameters

| Name | Type | Description |
|---|---|---|
| sender `indexed` | address | The address of the sender |
| value `indexed` | uint256 | The amount of value sent |



