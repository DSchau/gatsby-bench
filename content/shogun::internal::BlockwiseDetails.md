---
classname: "shogun::internal::BlockwiseDetails"
type: "class"
---

# class `shogun::internal::BlockwiseDetails` {#classshogun_1_1internal_1_1BlockwiseDetails}

Class that holds block-details for the data-fetchers. There are one instance of this class per fetcher.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public  `[`BlockwiseDetails`](#classshogun_1_1internal_1_1BlockwiseDetails_1a9f8b979b32ec3b123ca46f2cea1ed451)`()` | Default constructor.
`public `[`BlockwiseDetails`](#classshogun_1_1internal_1_1BlockwiseDetails)` & `[`with_blocksize`](#classshogun_1_1internal_1_1BlockwiseDetails_1a8aaa41195f7e139f2dc0e637ac082f9f)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` blocksize)` | Method that sets the blocksize for current fetcher. 
`public `[`BlockwiseDetails`](#classshogun_1_1internal_1_1BlockwiseDetails)` & `[`with_num_blocks_per_burst`](#classshogun_1_1internal_1_1BlockwiseDetails_1ac8d57eff131aad697c7ad52e008ae9a7)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_blocks_per_burst)` | Method that sets the number of blocks to be fetched per burst for current fetcher. 

## Members

#### `public  `[`BlockwiseDetails`](#classshogun_1_1internal_1_1BlockwiseDetails_1a9f8b979b32ec3b123ca46f2cea1ed451)`()` {#classshogun_1_1internal_1_1BlockwiseDetails_1a9f8b979b32ec3b123ca46f2cea1ed451}

Default constructor.

#### `public `[`BlockwiseDetails`](#classshogun_1_1internal_1_1BlockwiseDetails)` & `[`with_blocksize`](#classshogun_1_1internal_1_1BlockwiseDetails_1a8aaa41195f7e139f2dc0e637ac082f9f)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` blocksize)` {#classshogun_1_1internal_1_1BlockwiseDetails_1a8aaa41195f7e139f2dc0e637ac082f9f}

Method that sets the blocksize for current fetcher. 
#### Parameters
* `blocksize` the size of the block 

#### Returns
an instance of the current object

#### `public `[`BlockwiseDetails`](#classshogun_1_1internal_1_1BlockwiseDetails)` & `[`with_num_blocks_per_burst`](#classshogun_1_1internal_1_1BlockwiseDetails_1ac8d57eff131aad697c7ad52e008ae9a7)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_blocks_per_burst)` {#classshogun_1_1internal_1_1BlockwiseDetails_1ac8d57eff131aad697c7ad52e008ae9a7}

Method that sets the number of blocks to be fetched per burst for current fetcher. 
#### Parameters
* `num_blocks_per_burst` the number of blocks to be fetched per burst 

#### Returns
an instance of the current object

