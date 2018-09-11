---
classname: "shogun::TSGDataType"
type: "struct"
---

# struct `shogun::TSGDataType` {#structshogun_1_1TSGDataType}

Datatypes that shogun supports.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public EContainerType `[`m_ctype`](#structshogun_1_1TSGDataType_1a8544edd6954039ceb557a8df0c3380d1) | container type
`public EStructType `[`m_stype`](#structshogun_1_1TSGDataType_1a6f3884edd4fdd1cc697d0a272979e0e1) | struct type
`public EPrimitiveType `[`m_ptype`](#structshogun_1_1TSGDataType_1a72142052adcac8b346352c6b58ea3fc9) | primitive type
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * `[`m_length_y`](#structshogun_1_1TSGDataType_1a3ac945b0aa53b18d3b7f321da4200141) | length y
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * `[`m_length_x`](#structshogun_1_1TSGDataType_1a964f7a46b5dbba6c4ff5cbf6d6233ef8) | length x
`public  explicit `[`TSGDataType`](#structshogun_1_1TSGDataType_1a543cfd301c7184f762938038ab96be31)`(EContainerType ctype,EStructType stype,EPrimitiveType ptype)` | constructor 
`public  explicit `[`TSGDataType`](#structshogun_1_1TSGDataType_1a61cfa22c28aaafff9938b4b6991b70e4)`(EContainerType ctype,EStructType stype,EPrimitiveType ptype,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length)` | constructor 
`public  explicit `[`TSGDataType`](#structshogun_1_1TSGDataType_1ad98a56e93608115288db43580050b7ed)`(EContainerType ctype,EStructType stype,EPrimitiveType ptype,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x)` | constructor 
`public bool `[`operator==`](#structshogun_1_1TSGDataType_1a1ae9d5814258046b47df5a900f8708a8)`(const `[`TSGDataType`](#structshogun_1_1TSGDataType)` & a)` | equality
`public inline bool `[`operator!=`](#structshogun_1_1TSGDataType_1ae0c29775ba65acce32e6a77e6699336e)`(const `[`TSGDataType`](#structshogun_1_1TSGDataType)` & a)` | inequality 
`public void `[`to_string`](#structshogun_1_1TSGDataType_1a5a6fb7c40e3820229463bd4a149805e6)`(char * dest,size_t n) const` | to string 
`public size_t `[`sizeof_stype`](#structshogun_1_1TSGDataType_1ac3f5c46267ead3236f526f0bfdc37a97)`() const` | size of stype
`public size_t `[`sizeof_ptype`](#structshogun_1_1TSGDataType_1a9522956e823bbb500a51a0078e82693c)`() const` | size of ptype
`public size_t `[`get_size`](#structshogun_1_1TSGDataType_1adf55ed6a1edf8e1aa4f3f5f97936ad1e)`()` | get size 
`public int64_t `[`get_num_elements`](#structshogun_1_1TSGDataType_1a91222c3c4c8b8c6324ca791ce40e753f)`()` | get num of elements 

## Members

#### `public EContainerType `[`m_ctype`](#structshogun_1_1TSGDataType_1a8544edd6954039ceb557a8df0c3380d1) {#structshogun_1_1TSGDataType_1a8544edd6954039ceb557a8df0c3380d1}

container type

#### `public EStructType `[`m_stype`](#structshogun_1_1TSGDataType_1a6f3884edd4fdd1cc697d0a272979e0e1) {#structshogun_1_1TSGDataType_1a6f3884edd4fdd1cc697d0a272979e0e1}

struct type

#### `public EPrimitiveType `[`m_ptype`](#structshogun_1_1TSGDataType_1a72142052adcac8b346352c6b58ea3fc9) {#structshogun_1_1TSGDataType_1a72142052adcac8b346352c6b58ea3fc9}

primitive type

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * `[`m_length_y`](#structshogun_1_1TSGDataType_1a3ac945b0aa53b18d3b7f321da4200141) {#structshogun_1_1TSGDataType_1a3ac945b0aa53b18d3b7f321da4200141}

length y

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * `[`m_length_x`](#structshogun_1_1TSGDataType_1a964f7a46b5dbba6c4ff5cbf6d6233ef8) {#structshogun_1_1TSGDataType_1a964f7a46b5dbba6c4ff5cbf6d6233ef8}

length x

#### `public  explicit `[`TSGDataType`](#structshogun_1_1TSGDataType_1a543cfd301c7184f762938038ab96be31)`(EContainerType ctype,EStructType stype,EPrimitiveType ptype)` {#structshogun_1_1TSGDataType_1a543cfd301c7184f762938038ab96be31}

constructor 
#### Parameters
* `ctype` 

* `stype` 

* `ptype`

#### `public  explicit `[`TSGDataType`](#structshogun_1_1TSGDataType_1a61cfa22c28aaafff9938b4b6991b70e4)`(EContainerType ctype,EStructType stype,EPrimitiveType ptype,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length)` {#structshogun_1_1TSGDataType_1a61cfa22c28aaafff9938b4b6991b70e4}

constructor 
#### Parameters
* `ctype` 

* `stype` 

* `ptype` 

* `length`

#### `public  explicit `[`TSGDataType`](#structshogun_1_1TSGDataType_1ad98a56e93608115288db43580050b7ed)`(EContainerType ctype,EStructType stype,EPrimitiveType ptype,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x)` {#structshogun_1_1TSGDataType_1ad98a56e93608115288db43580050b7ed}

constructor 
#### Parameters
* `ctype` 

* `stype` 

* `ptype` 

* `length_y` 

* `length_x`

#### `public bool `[`operator==`](#structshogun_1_1TSGDataType_1a1ae9d5814258046b47df5a900f8708a8)`(const `[`TSGDataType`](#structshogun_1_1TSGDataType)` & a)` {#structshogun_1_1TSGDataType_1a1ae9d5814258046b47df5a900f8708a8}

equality

#### `public inline bool `[`operator!=`](#structshogun_1_1TSGDataType_1ae0c29775ba65acce32e6a77e6699336e)`(const `[`TSGDataType`](#structshogun_1_1TSGDataType)` & a)` {#structshogun_1_1TSGDataType_1ae0c29775ba65acce32e6a77e6699336e}

inequality 
#### Parameters
* `a`

#### `public void `[`to_string`](#structshogun_1_1TSGDataType_1a5a6fb7c40e3820229463bd4a149805e6)`(char * dest,size_t n) const` {#structshogun_1_1TSGDataType_1a5a6fb7c40e3820229463bd4a149805e6}

to string 
#### Parameters
* `dest` 

* `n`

#### `public size_t `[`sizeof_stype`](#structshogun_1_1TSGDataType_1ac3f5c46267ead3236f526f0bfdc37a97)`() const` {#structshogun_1_1TSGDataType_1ac3f5c46267ead3236f526f0bfdc37a97}

size of stype

#### `public size_t `[`sizeof_ptype`](#structshogun_1_1TSGDataType_1a9522956e823bbb500a51a0078e82693c)`() const` {#structshogun_1_1TSGDataType_1a9522956e823bbb500a51a0078e82693c}

size of ptype

#### `public size_t `[`get_size`](#structshogun_1_1TSGDataType_1adf55ed6a1edf8e1aa4f3f5f97936ad1e)`()` {#structshogun_1_1TSGDataType_1adf55ed6a1edf8e1aa4f3f5f97936ad1e}

get size 
#### Returns
size of type in bytes

#### `public int64_t `[`get_num_elements`](#structshogun_1_1TSGDataType_1a91222c3c4c8b8c6324ca791ce40e753f)`()` {#structshogun_1_1TSGDataType_1a91222c3c4c8b8c6324ca791ce40e753f}

get num of elements 
#### Returns
number of (matrix, vector, scalar) elements of type

