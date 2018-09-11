---
classname: "shogun::SGStringList"
type: "class"
parents:
   - SGReferencedData
---

# class `shogun::SGStringList` {#classshogun_1_1SGStringList}

```
class shogun::SGStringList
  : public SGReferencedData
```

template class [SGStringList](#classshogun_1_1SGStringList)

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`num_strings`](#classshogun_1_1SGStringList_1ab50ca544cad9bc536168a01e751607c3) | number of strings
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`max_string_length`](#classshogun_1_1SGStringList_1a58f8097a717428dbdf3ea4491331f240) | length of longest string
`public `[`SGString`](#classshogun_1_1SGString)`< T > * `[`strings`](#classshogun_1_1SGStringList_1a70e433f0dc2915857978879b93d92710) | this contains the array of features
`public  `[`SGStringList`](#classshogun_1_1SGStringList_1a0a5c1c812faf4421edd282a98174d9ac)`()` | default constructor
`public  `[`SGStringList`](#classshogun_1_1SGStringList_1ae4652c5a93d58e5bfe2cd4a7aa7ab79b)`(`[`SGString`](#classshogun_1_1SGString)`< T > * s,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_s,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` max_length,bool ref_counting)` | constructor for setting params
`public  `[`SGStringList`](#classshogun_1_1SGStringList_1a0491d85babcf478d8e8d99e1e489e45b)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_s,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` max_length,bool ref_counting)` | constructor to create new string list in memory
`public  `[`SGStringList`](#classshogun_1_1SGStringList_1a3783d7cbe014f7f5569dc38da0973bc4)`(const `[`SGStringList`](#classshogun_1_1SGStringList)` & orig)` | copy constructor
`public virtual  `[`~SGStringList`](#classshogun_1_1SGStringList_1a4ac2b5b977686596ba78aaf6a2572cf6)`()` | destructor
`public inline `[`SGStringList`](#classshogun_1_1SGStringList)`< T > `[`get`](#classshogun_1_1SGStringList_1ab753c149f7f95e01439d237759884be4)`()` | get the string list (no copying is done here)
`public void `[`load`](#classshogun_1_1SGStringList_1a5d33ec59a4be25056cca1f3b6691ad00)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` | load strings from file
`public void `[`save`](#classshogun_1_1SGStringList_1aff4d5355fe0d9b68bc8c71cd331c082e)`(`[`CFile`](#classshogun_1_1CFile)` * saver)` | save strings to file
`public `[`SGStringList`](#classshogun_1_1SGStringList)`< T > `[`clone`](#classshogun_1_1SGStringList_1afe7e6c64e0b02cdf7cc6a47219d33e4c)`() const` | clone string list
`public int32_t `[`ref_count`](#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d)`()` | display reference counter
`protected virtual void `[`copy_data`](#classshogun_1_1SGStringList_1a6e8ddd37b0b245f7cca418642762e16b)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` | copy data
`protected virtual void `[`init_data`](#classshogun_1_1SGStringList_1a3b42d3bd68c5200393c1f0809ed1facf)`()` | init data
`protected virtual void `[`free_data`](#classshogun_1_1SGStringList_1ab340ce24b1c9d2b26ab2b46a7a64c346)`()` | free data
`protected void `[`copy_refcount`](#classshogun_1_1SGReferencedData_1a253175a13e8af17d4f2a2cfd9e14dd63)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` | copy refcount
`protected int32_t `[`ref`](#classshogun_1_1SGReferencedData_1ab8c24b912ee57d3f2c81ecccd083582a)`()` | increase reference counter
`protected int32_t `[`unref`](#classshogun_1_1SGReferencedData_1ad99bde1a142a1c07a963169123166e01)`()` | decrement reference counter and deallocate object if refcount is zero before or after decrementing it

## Members

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`num_strings`](#classshogun_1_1SGStringList_1ab50ca544cad9bc536168a01e751607c3) {#classshogun_1_1SGStringList_1ab50ca544cad9bc536168a01e751607c3}

number of strings

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`max_string_length`](#classshogun_1_1SGStringList_1a58f8097a717428dbdf3ea4491331f240) {#classshogun_1_1SGStringList_1a58f8097a717428dbdf3ea4491331f240}

length of longest string

#### `public `[`SGString`](#classshogun_1_1SGString)`< T > * `[`strings`](#classshogun_1_1SGStringList_1a70e433f0dc2915857978879b93d92710) {#classshogun_1_1SGStringList_1a70e433f0dc2915857978879b93d92710}

this contains the array of features

#### `public  `[`SGStringList`](#classshogun_1_1SGStringList_1a0a5c1c812faf4421edd282a98174d9ac)`()` {#classshogun_1_1SGStringList_1a0a5c1c812faf4421edd282a98174d9ac}

default constructor

#### `public  `[`SGStringList`](#classshogun_1_1SGStringList_1ae4652c5a93d58e5bfe2cd4a7aa7ab79b)`(`[`SGString`](#classshogun_1_1SGString)`< T > * s,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_s,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` max_length,bool ref_counting)` {#classshogun_1_1SGStringList_1ae4652c5a93d58e5bfe2cd4a7aa7ab79b}

constructor for setting params

#### `public  `[`SGStringList`](#classshogun_1_1SGStringList_1a0491d85babcf478d8e8d99e1e489e45b)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_s,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` max_length,bool ref_counting)` {#classshogun_1_1SGStringList_1a0491d85babcf478d8e8d99e1e489e45b}

constructor to create new string list in memory

#### `public  `[`SGStringList`](#classshogun_1_1SGStringList_1a3783d7cbe014f7f5569dc38da0973bc4)`(const `[`SGStringList`](#classshogun_1_1SGStringList)` & orig)` {#classshogun_1_1SGStringList_1a3783d7cbe014f7f5569dc38da0973bc4}

copy constructor

#### `public virtual  `[`~SGStringList`](#classshogun_1_1SGStringList_1a4ac2b5b977686596ba78aaf6a2572cf6)`()` {#classshogun_1_1SGStringList_1a4ac2b5b977686596ba78aaf6a2572cf6}

destructor

#### `public inline `[`SGStringList`](#classshogun_1_1SGStringList)`< T > `[`get`](#classshogun_1_1SGStringList_1ab753c149f7f95e01439d237759884be4)`()` {#classshogun_1_1SGStringList_1ab753c149f7f95e01439d237759884be4}

get the string list (no copying is done here)

#### Returns
the refcount increased string list

#### `public void `[`load`](#classshogun_1_1SGStringList_1a5d33ec59a4be25056cca1f3b6691ad00)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` {#classshogun_1_1SGStringList_1a5d33ec59a4be25056cca1f3b6691ad00}

load strings from file

#### Parameters
* `loader` File object via which to load data

#### `public void `[`save`](#classshogun_1_1SGStringList_1aff4d5355fe0d9b68bc8c71cd331c082e)`(`[`CFile`](#classshogun_1_1CFile)` * saver)` {#classshogun_1_1SGStringList_1aff4d5355fe0d9b68bc8c71cd331c082e}

save strings to file

#### Parameters
* `saver` File object via which to save data

#### `public `[`SGStringList`](#classshogun_1_1SGStringList)`< T > `[`clone`](#classshogun_1_1SGStringList_1afe7e6c64e0b02cdf7cc6a47219d33e4c)`() const` {#classshogun_1_1SGStringList_1afe7e6c64e0b02cdf7cc6a47219d33e4c}

clone string list

#### Returns
a deep copy of current string list

#### `public int32_t `[`ref_count`](#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d)`()` {#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d}

display reference counter

#### Returns
reference count

#### `protected virtual void `[`copy_data`](#classshogun_1_1SGStringList_1a6e8ddd37b0b245f7cca418642762e16b)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` {#classshogun_1_1SGStringList_1a6e8ddd37b0b245f7cca418642762e16b}

copy data

#### `protected virtual void `[`init_data`](#classshogun_1_1SGStringList_1a3b42d3bd68c5200393c1f0809ed1facf)`()` {#classshogun_1_1SGStringList_1a3b42d3bd68c5200393c1f0809ed1facf}

init data

#### `protected virtual void `[`free_data`](#classshogun_1_1SGStringList_1ab340ce24b1c9d2b26ab2b46a7a64c346)`()` {#classshogun_1_1SGStringList_1ab340ce24b1c9d2b26ab2b46a7a64c346}

free data

#### `protected void `[`copy_refcount`](#classshogun_1_1SGReferencedData_1a253175a13e8af17d4f2a2cfd9e14dd63)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` {#classshogun_1_1SGReferencedData_1a253175a13e8af17d4f2a2cfd9e14dd63}

copy refcount

#### `protected int32_t `[`ref`](#classshogun_1_1SGReferencedData_1ab8c24b912ee57d3f2c81ecccd083582a)`()` {#classshogun_1_1SGReferencedData_1ab8c24b912ee57d3f2c81ecccd083582a}

increase reference counter

#### Returns
reference count

#### `protected int32_t `[`unref`](#classshogun_1_1SGReferencedData_1ad99bde1a142a1c07a963169123166e01)`()` {#classshogun_1_1SGReferencedData_1ad99bde1a142a1c07a963169123166e01}

decrement reference counter and deallocate object if refcount is zero before or after decrementing it

#### Returns
reference count

