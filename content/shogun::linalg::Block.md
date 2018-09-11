---
classname: "shogun::linalg::Block"
type: "struct"
---

# struct `shogun::linalg::Block` {#structshogun_1_1linalg_1_1Block}

Generic class [Block](#structshogun_1_1linalg_1_1Block) which wraps a matrix class and contains block specific information, providing a uniform way to deal with matrix blocks for all supported backend matrices.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public Matrix `[`m_matrix`](#structshogun_1_1linalg_1_1Block_1aa460d14c52aaec500bc9180b51846328) | the matrix on which the block is defined
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`m_row_begin`](#structshogun_1_1linalg_1_1Block_1aa8d4eae3745f31b6ed19acab6ab2b4f6) | the row index at which the block starts
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`m_col_begin`](#structshogun_1_1linalg_1_1Block_1a1094f655d1be40f2a913a895a29ff493) | the col index at which the block starts
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`m_row_size`](#structshogun_1_1linalg_1_1Block_1a1f53cdb7c23da5b145191471da8dea0c) | the number of rows in the block
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`m_col_size`](#structshogun_1_1linalg_1_1Block_1a575ecbd7be0d3ca542930ae43a239c9e) | the number of cols in the block
`public inline  `[`Block`](#structshogun_1_1linalg_1_1Block_1a099287e2ff6fd3cff3c4517e074b8a00)`(Matrix matrix,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` row_begin,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` col_begin,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` row_size,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` col_size)` | constructor
`typedef `[`Scalar`](#structshogun_1_1linalg_1_1Block_1a432df1c9fe58bff5a8855264b9039fec) | scalar type

## Members

#### `public Matrix `[`m_matrix`](#structshogun_1_1linalg_1_1Block_1aa460d14c52aaec500bc9180b51846328) {#structshogun_1_1linalg_1_1Block_1aa460d14c52aaec500bc9180b51846328}

the matrix on which the block is defined

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`m_row_begin`](#structshogun_1_1linalg_1_1Block_1aa8d4eae3745f31b6ed19acab6ab2b4f6) {#structshogun_1_1linalg_1_1Block_1aa8d4eae3745f31b6ed19acab6ab2b4f6}

the row index at which the block starts

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`m_col_begin`](#structshogun_1_1linalg_1_1Block_1a1094f655d1be40f2a913a895a29ff493) {#structshogun_1_1linalg_1_1Block_1a1094f655d1be40f2a913a895a29ff493}

the col index at which the block starts

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`m_row_size`](#structshogun_1_1linalg_1_1Block_1a1f53cdb7c23da5b145191471da8dea0c) {#structshogun_1_1linalg_1_1Block_1a1f53cdb7c23da5b145191471da8dea0c}

the number of rows in the block

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`m_col_size`](#structshogun_1_1linalg_1_1Block_1a575ecbd7be0d3ca542930ae43a239c9e) {#structshogun_1_1linalg_1_1Block_1a575ecbd7be0d3ca542930ae43a239c9e}

the number of cols in the block

#### `public inline  `[`Block`](#structshogun_1_1linalg_1_1Block_1a099287e2ff6fd3cff3c4517e074b8a00)`(Matrix matrix,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` row_begin,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` col_begin,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` row_size,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` col_size)` {#structshogun_1_1linalg_1_1Block_1a099287e2ff6fd3cff3c4517e074b8a00}

constructor

#### Parameters
* `matrix` the matrix on which the block is defined 

* `row_begin` the row index at which the block starts 

* `col_begin` the col index at which the block starts 

* `row_size` the number of rows in the block 

* `col_size` the number of cols in the block

For example, row_begin 0, col_begin 4 and row_size 5, col_size 6 represents the block that starts at index (0,4) in the matrix and goes upto (0+5-1,4+6-1) i.e. (4,9) both inclusive

#### `typedef `[`Scalar`](#structshogun_1_1linalg_1_1Block_1a432df1c9fe58bff5a8855264b9039fec) {#structshogun_1_1linalg_1_1Block_1a432df1c9fe58bff5a8855264b9039fec}

scalar type

