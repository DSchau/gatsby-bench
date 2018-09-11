---
classname: "shogun::SGSparseVectorEntry"
type: "struct"
---

# struct `shogun::SGSparseVectorEntry` {#structshogun_1_1SGSparseVectorEntry}

template class [SGSparseVectorEntry](#structshogun_1_1SGSparseVectorEntry)

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`feat_index`](#structshogun_1_1SGSparseVectorEntry_1a0a6fba3a4847624bddb747a393bd7e2c) | feature index
`public T `[`entry`](#structshogun_1_1SGSparseVectorEntry_1ae365e5c1b1f93157c401cda2c01b6913) | entry ...
`public inline bool `[`operator==`](#structshogun_1_1SGSparseVectorEntry_1a0eee5ecc390b55ad073d432c288f0983)`(const `[`SGSparseVectorEntry`](#structshogun_1_1SGSparseVectorEntry)`< T > & other) const` | Comparson of entry 
`public template<>`  <br/>`bool `[`operator==`](#structshogun_1_1SGSparseVectorEntry_1aa3dcc244d916f16a5d98b5427aa2dd07)`(const `[`SGSparseVectorEntry](#structshogun_1_1SGSparseVectorEntry)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > & other) const` | 

## Members

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`feat_index`](#structshogun_1_1SGSparseVectorEntry_1a0a6fba3a4847624bddb747a393bd7e2c) {#structshogun_1_1SGSparseVectorEntry_1a0a6fba3a4847624bddb747a393bd7e2c}

feature index

#### `public T `[`entry`](#structshogun_1_1SGSparseVectorEntry_1ae365e5c1b1f93157c401cda2c01b6913) {#structshogun_1_1SGSparseVectorEntry_1ae365e5c1b1f93157c401cda2c01b6913}

entry ...

#### `public inline bool `[`operator==`](#structshogun_1_1SGSparseVectorEntry_1a0eee5ecc390b55ad073d432c288f0983)`(const `[`SGSparseVectorEntry`](#structshogun_1_1SGSparseVectorEntry)`< T > & other) const` {#structshogun_1_1SGSparseVectorEntry_1a0eee5ecc390b55ad073d432c288f0983}

Comparson of entry 
#### Returns
true iff index and value (numerically for floats) are equal

#### `public template<>`  <br/>`bool `[`operator==`](#structshogun_1_1SGSparseVectorEntry_1aa3dcc244d916f16a5d98b5427aa2dd07)`(const `[`SGSparseVectorEntry](#structshogun_1_1SGSparseVectorEntry)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > & other) const` {#structshogun_1_1SGSparseVectorEntry_1aa3dcc244d916f16a5d98b5427aa2dd07}

