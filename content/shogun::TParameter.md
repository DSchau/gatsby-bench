---
classname: "shogun::TParameter"
type: "struct"
---

# struct `shogun::TParameter` {#structshogun_1_1TParameter}

parameter struct

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public `[`TSGDataType`](#structshogun_1_1TSGDataType)` `[`m_datatype`](#structshogun_1_1TParameter_1a800195633729b3c03fb64a013ee2bb69) | type of parameter
`public void * `[`m_parameter`](#structshogun_1_1TParameter_1a6101b8335413f8d9153564a034da0a83) | pointer to parameter
`public char * `[`m_name`](#structshogun_1_1TParameter_1a21f02840f823e035f2e1d9e4272b9371) | name of parameter
`public char * `[`m_description`](#structshogun_1_1TParameter_1a2e1e12c3ddf5ce9ca5ac2e517d771c76) | description of parameter
`public  explicit `[`TParameter`](#structshogun_1_1TParameter_1ac943b7912bf9ec2d841affe179681407)`(const `[`TSGDataType`](#structshogun_1_1TSGDataType)` * datatype,void * parameter,const char * name,const char * description)` | explicit constructor 
`public  `[`~TParameter`](#structshogun_1_1TParameter_1aabf8715f8110f2e94d74e53ce0f39456)`()` | destructor
`public void `[`print`](#structshogun_1_1TParameter_1aa8d2cf54e816c6be1cf3a40ec5ee7ecb)`(const char * prefix)` | print with prefix 
`public bool `[`save`](#structshogun_1_1TParameter_1af5f394df0bf09bc2409808804f7e8c8b)`(`[`CSerializableFile`](#classshogun_1_1CSerializableFile)` * file,const char * prefix)` | save to serializable file 
`public bool `[`load`](#structshogun_1_1TParameter_1aec99d1d4b0e9cd1d10a61734a3d148db)`(`[`CSerializableFile`](#classshogun_1_1CSerializableFile)` * file,const char * prefix)` | load from serializable file 
`public bool `[`operator==`](#structshogun_1_1TParameter_1a16ea599d87078b6ebbed5cc81b8b4a25)`(const `[`TParameter`](#structshogun_1_1TParameter)` & other) const` | operator for comparison, (by string m_name)
`public bool `[`operator<`](#structshogun_1_1TParameter_1a1cf34ea866da0d5d51f0f9fd5e0db387)`(const `[`TParameter`](#structshogun_1_1TParameter)` & other) const` | operator for comparison (by string m_name)
`public bool `[`operator>`](#structshogun_1_1TParameter_1aaee8be544beb0f45128bc6cf4623142a)`(const `[`TParameter`](#structshogun_1_1TParameter)` & other) const` | operator for comparison (by string m_name)
`public void `[`get_incremental_hash`](#structshogun_1_1TParameter_1a0bfb3eadec9744df2aac3afc113e428f)`(uint32_t & hash,uint32_t & carry,uint32_t & total_length)` | Incrementally get a hash from parameter value
`public bool `[`is_valid`](#structshogun_1_1TParameter_1af4d2f059b86d0249fcab31063634aa57)`()` | test if parameter can be validly accessed, e.g., in case of a list/vector/matrix of objects the list/vector/matrix has non-zero length

## Members

#### `public `[`TSGDataType`](#structshogun_1_1TSGDataType)` `[`m_datatype`](#structshogun_1_1TParameter_1a800195633729b3c03fb64a013ee2bb69) {#structshogun_1_1TParameter_1a800195633729b3c03fb64a013ee2bb69}

type of parameter

#### `public void * `[`m_parameter`](#structshogun_1_1TParameter_1a6101b8335413f8d9153564a034da0a83) {#structshogun_1_1TParameter_1a6101b8335413f8d9153564a034da0a83}

pointer to parameter

#### `public char * `[`m_name`](#structshogun_1_1TParameter_1a21f02840f823e035f2e1d9e4272b9371) {#structshogun_1_1TParameter_1a21f02840f823e035f2e1d9e4272b9371}

name of parameter

#### `public char * `[`m_description`](#structshogun_1_1TParameter_1a2e1e12c3ddf5ce9ca5ac2e517d771c76) {#structshogun_1_1TParameter_1a2e1e12c3ddf5ce9ca5ac2e517d771c76}

description of parameter

#### `public  explicit `[`TParameter`](#structshogun_1_1TParameter_1ac943b7912bf9ec2d841affe179681407)`(const `[`TSGDataType`](#structshogun_1_1TSGDataType)` * datatype,void * parameter,const char * name,const char * description)` {#structshogun_1_1TParameter_1ac943b7912bf9ec2d841affe179681407}

explicit constructor 
#### Parameters
* `datatype` datatype 

* `parameter` pointer to parameter 

* `name` name of parameter 

* `description` description of parameter

#### `public  `[`~TParameter`](#structshogun_1_1TParameter_1aabf8715f8110f2e94d74e53ce0f39456)`()` {#structshogun_1_1TParameter_1aabf8715f8110f2e94d74e53ce0f39456}

destructor

#### `public void `[`print`](#structshogun_1_1TParameter_1aa8d2cf54e816c6be1cf3a40ec5ee7ecb)`(const char * prefix)` {#structshogun_1_1TParameter_1aa8d2cf54e816c6be1cf3a40ec5ee7ecb}

print with prefix 
#### Parameters
* `prefix` prefix to print

#### `public bool `[`save`](#structshogun_1_1TParameter_1af5f394df0bf09bc2409808804f7e8c8b)`(`[`CSerializableFile`](#classshogun_1_1CSerializableFile)` * file,const char * prefix)` {#structshogun_1_1TParameter_1af5f394df0bf09bc2409808804f7e8c8b}

save to serializable file 
#### Parameters
* `file` destination file 

* `prefix` prefix

#### `public bool `[`load`](#structshogun_1_1TParameter_1aec99d1d4b0e9cd1d10a61734a3d148db)`(`[`CSerializableFile`](#classshogun_1_1CSerializableFile)` * file,const char * prefix)` {#structshogun_1_1TParameter_1aec99d1d4b0e9cd1d10a61734a3d148db}

load from serializable file 
#### Parameters
* `file` source file 

* `prefix` prefix

#### `public bool `[`operator==`](#structshogun_1_1TParameter_1a16ea599d87078b6ebbed5cc81b8b4a25)`(const `[`TParameter`](#structshogun_1_1TParameter)` & other) const` {#structshogun_1_1TParameter_1a16ea599d87078b6ebbed5cc81b8b4a25}

operator for comparison, (by string m_name)

#### `public bool `[`operator<`](#structshogun_1_1TParameter_1a1cf34ea866da0d5d51f0f9fd5e0db387)`(const `[`TParameter`](#structshogun_1_1TParameter)` & other) const` {#structshogun_1_1TParameter_1a1cf34ea866da0d5d51f0f9fd5e0db387}

operator for comparison (by string m_name)

#### `public bool `[`operator>`](#structshogun_1_1TParameter_1aaee8be544beb0f45128bc6cf4623142a)`(const `[`TParameter`](#structshogun_1_1TParameter)` & other) const` {#structshogun_1_1TParameter_1aaee8be544beb0f45128bc6cf4623142a}

operator for comparison (by string m_name)

#### `public void `[`get_incremental_hash`](#structshogun_1_1TParameter_1a0bfb3eadec9744df2aac3afc113e428f)`(uint32_t & hash,uint32_t & carry,uint32_t & total_length)` {#structshogun_1_1TParameter_1a0bfb3eadec9744df2aac3afc113e428f}

Incrementally get a hash from parameter value

#### Parameters
* `hash` current hash value 

* `carry` value for incremental murmur hashing 

* `total_length` byte length of parameters. Function will add byte length to received value

#### `public bool `[`is_valid`](#structshogun_1_1TParameter_1af4d2f059b86d0249fcab31063634aa57)`()` {#structshogun_1_1TParameter_1af4d2f059b86d0249fcab31063634aa57}

test if parameter can be validly accessed, e.g., in case of a list/vector/matrix of objects the list/vector/matrix has non-zero length

