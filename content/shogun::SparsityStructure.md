---
classname: "shogun::SparsityStructure"
type: "struct"
---

# struct `shogun::SparsityStructure` {#structshogun_1_1SparsityStructure}

Struct that represents the sparsity structure of the Sparse Matrix in CRS. Implementation has been adapted from Krylstat ([https://github.com/](https://github.com/) Froskekongen/KRYLSTAT) library (c) Erlend Aune [erlenda@math.ntnu.no](mailto:erlenda@math.ntnu.no) under GPL2+.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`m_num_rows`](#structshogun_1_1SparsityStructure_1af864656eef91e8db3ed2943d3b635813) | number of rows
`public int32_t ** `[`m_ptr`](#structshogun_1_1SparsityStructure_1a9c1dab1dd01e08f7536e76bc3bef7aa9) | the pointer that stores the nnz entries
`public inline  `[`SparsityStructure`](#structshogun_1_1SparsityStructure_1a71ef776947d1a3778c7720c429cd5b60)`()` | default constructor
`public inline  `[`SparsityStructure`](#structshogun_1_1SparsityStructure_1a0438c1401019fff1bed863231a8cee5e)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * row_offsets,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * column_indices,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_rows)` | constructor
`public inline  `[`~SparsityStructure`](#structshogun_1_1SparsityStructure_1a408c66c114adc74a535544b83b80f881)`()` | destructor
`public inline void `[`display_sparsity_structure`](#structshogun_1_1SparsityStructure_1ac8b0bd77f04be850d83f8eb5f0c72470)`()` | display sparsity structure

## Members

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`m_num_rows`](#structshogun_1_1SparsityStructure_1af864656eef91e8db3ed2943d3b635813) {#structshogun_1_1SparsityStructure_1af864656eef91e8db3ed2943d3b635813}

number of rows

#### `public int32_t ** `[`m_ptr`](#structshogun_1_1SparsityStructure_1a9c1dab1dd01e08f7536e76bc3bef7aa9) {#structshogun_1_1SparsityStructure_1a9c1dab1dd01e08f7536e76bc3bef7aa9}

the pointer that stores the nnz entries

#### `public inline  `[`SparsityStructure`](#structshogun_1_1SparsityStructure_1a71ef776947d1a3778c7720c429cd5b60)`()` {#structshogun_1_1SparsityStructure_1a71ef776947d1a3778c7720c429cd5b60}

default constructor

#### `public inline  `[`SparsityStructure`](#structshogun_1_1SparsityStructure_1a0438c1401019fff1bed863231a8cee5e)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * row_offsets,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * column_indices,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_rows)` {#structshogun_1_1SparsityStructure_1a0438c1401019fff1bed863231a8cee5e}

constructor

#### Parameters
* `row_offsets` outer index ptr in CRS 

* `column_indices` inner index ptr in CRS 

* `num_rows` number of rows

#### `public inline  `[`~SparsityStructure`](#structshogun_1_1SparsityStructure_1a408c66c114adc74a535544b83b80f881)`()` {#structshogun_1_1SparsityStructure_1a408c66c114adc74a535544b83b80f881}

destructor

#### `public inline void `[`display_sparsity_structure`](#structshogun_1_1SparsityStructure_1ac8b0bd77f04be850d83f8eb5f0c72470)`()` {#structshogun_1_1SparsityStructure_1ac8b0bd77f04be850d83f8eb5f0c72470}

display sparsity structure

