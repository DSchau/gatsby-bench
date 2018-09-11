---
classname: "shogun::internal::DataManager"
type: "class"
---

# class `shogun::internal::DataManager` {#classshogun_1_1internal_1_1DataManager}

Class [DataManager](#classshogun_1_1internal_1_1DataManager) for fetching/streaming test data block-wise. It can handle data coming from multiple sources. The number of data sources is represented by the num_distributions parameter in the constructor of the data manager. It can handle heterogenous data sources, and it can stream multiple blocks per burst, as the computation would require. The size of the blocks and the number of blocks to be fetched per burst can be set externally.

This class is designed to be used on a stack. An instance of [DataManager](#classshogun_1_1internal_1_1DataManager) should not be serialzied or copied or moved around. In [Shogun](#classShogun), it is helpful when used inside just the implementation inside a PIMPL.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public  `[`DataManager`](#classshogun_1_1internal_1_1DataManager_1a2a1dd74b90d12d4c899620d54202cca9)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_distributions)` | Default constructor.
`public  `[`DataManager`](#classshogun_1_1internal_1_1DataManager_1a2244766f95ae7ba574e4eedd3f865b4c)`(const `[`DataManager`](#classshogun_1_1internal_1_1DataManager)` & other) = delete` | Disabled copy constructor 
`public `[`DataManager`](#classshogun_1_1internal_1_1DataManager)` & `[`operator=`](#classshogun_1_1internal_1_1DataManager_1a38cabfdd3fbad3d47c044cd7ae2416cb)`(const `[`DataManager`](#classshogun_1_1internal_1_1DataManager)` & other) = delete` | Disabled assignment operator 
`public  `[`~DataManager`](#classshogun_1_1internal_1_1DataManager_1a6fbfb5f67ba6ffa1f6feed3679bf827d)`()` | Destructor
`public void `[`set_blocksize`](#classshogun_1_1internal_1_1DataManager_1abbbbfd812ee8b3e9bbda4c58d393c6e8)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` blocksize)` | Sets the blocksize for block-wise data fetching. It divides the block-size per data source according to the total number of feature vectors available from that source. More formally, if there are $K$ data sources, $X_k$, $k=\[1,K]$, with number of feature vectors $n_{X_k}$ from each, then setting a block-size of $B$ would mean that in each next() call of the data manager instance, it will fetch $rho_{X_k} B$ samples from each $X_k$, where $rho_{X_k}=n_{X_k}/n$, $n=sum_k n_{X_k}$.
`public void `[`set_num_blocks_per_burst`](#classshogun_1_1internal_1_1DataManager_1a963c6bf10894b160cfb17e0e57ca53cc)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_blocks_per_burst)` | In order to speed up the computation, usually a number of blocks are fetched at once per next() call. This method sets that number.
`public InitPerFeature `[`samples_at`](#classshogun_1_1internal_1_1DataManager_1a6b56ddc9d65a6389af098b40e25fcc73)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i)` | Setter for feature object as a data source. Since multiple data sources are supported, this method takes an index in which the feature object is set. Internally, it initializes a data fetcher object for the provided feature object.
`public `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`samples_at`](#classshogun_1_1internal_1_1DataManager_1a1502d76318b406a82824888024d535e6)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i) const` | Getter for feature object at a give data source index.
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` & `[`num_samples_at`](#classshogun_1_1internal_1_1DataManager_1a1a7ee11ed90f3bb95be7dedf1ea7b61b)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i)` | Setter for the number of samples. Setting this number is mandatory for streaming features. For other type of feature objects, this number equals the number of vectors, and is set internally.
`public const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`num_samples_at`](#classshogun_1_1internal_1_1DataManager_1a0e3a1256201855c82fe06e2cc07b40cb)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i) const` | Getter for the number of samples.
`public const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`blocksize_at`](#classshogun_1_1internal_1_1DataManager_1ac45d74f98c5dbee568bfe2fbdc45f06e)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i) const` | Getter for the number of samples from a specified data source in a block.
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`get_num_samples`](#classshogun_1_1internal_1_1DataManager_1a57cf35d53e6f71ea046aed9f6e573630)`() const` | #### Returns
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`get_min_blocksize`](#classshogun_1_1internal_1_1DataManager_1aefc324a9750e0d636fdfbf2bd202aa38)`() const` | #### Returns

## Members

#### `public  `[`DataManager`](#classshogun_1_1internal_1_1DataManager_1a2a1dd74b90d12d4c899620d54202cca9)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_distributions)` {#classshogun_1_1internal_1_1DataManager_1a2a1dd74b90d12d4c899620d54202cca9}

Default constructor.

#### Parameters
* `num_distributions` number of data sources (i.e. CFeature objects)

#### `public  `[`DataManager`](#classshogun_1_1internal_1_1DataManager_1a2244766f95ae7ba574e4eedd3f865b4c)`(const `[`DataManager`](#classshogun_1_1internal_1_1DataManager)` & other) = delete` {#classshogun_1_1internal_1_1DataManager_1a2244766f95ae7ba574e4eedd3f865b4c}

Disabled copy constructor 
#### Parameters
* `other` other instance

#### `public `[`DataManager`](#classshogun_1_1internal_1_1DataManager)` & `[`operator=`](#classshogun_1_1internal_1_1DataManager_1a38cabfdd3fbad3d47c044cd7ae2416cb)`(const `[`DataManager`](#classshogun_1_1internal_1_1DataManager)` & other) = delete` {#classshogun_1_1internal_1_1DataManager_1a38cabfdd3fbad3d47c044cd7ae2416cb}

Disabled assignment operator 
#### Parameters
* `other` other instance

#### `public  `[`~DataManager`](#classshogun_1_1internal_1_1DataManager_1a6fbfb5f67ba6ffa1f6feed3679bf827d)`()` {#classshogun_1_1internal_1_1DataManager_1a6fbfb5f67ba6ffa1f6feed3679bf827d}

Destructor

#### `public void `[`set_blocksize`](#classshogun_1_1internal_1_1DataManager_1abbbbfd812ee8b3e9bbda4c58d393c6e8)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` blocksize)` {#classshogun_1_1internal_1_1DataManager_1abbbbfd812ee8b3e9bbda4c58d393c6e8}

Sets the blocksize for block-wise data fetching. It divides the block-size per data source according to the total number of feature vectors available from that source. More formally, if there are $K$ data sources, $X_k$, $k=\[1,K]$, with number of feature vectors $n_{X_k}$ from each, then setting a block-size of $B$ would mean that in each next() call of the data manager instance, it will fetch $rho_{X_k} B$ samples from each $X_k$, where $rho_{X_k}=n_{X_k}/n$, $n=sum_k n_{X_k}$.

#### Parameters
* `blocksize` The size of the block consisting of data from all the sources.

#### `public void `[`set_num_blocks_per_burst`](#classshogun_1_1internal_1_1DataManager_1a963c6bf10894b160cfb17e0e57ca53cc)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_blocks_per_burst)` {#classshogun_1_1internal_1_1DataManager_1a963c6bf10894b160cfb17e0e57ca53cc}

In order to speed up the computation, usually a number of blocks are fetched at once per next() call. This method sets that number.

#### Parameters
* `num_blocks_per_burst` The number of blocks to be fetched in a burst.

#### `public InitPerFeature `[`samples_at`](#classshogun_1_1internal_1_1DataManager_1a6b56ddc9d65a6389af098b40e25fcc73)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i)` {#classshogun_1_1internal_1_1DataManager_1a6b56ddc9d65a6389af098b40e25fcc73}

Setter for feature object as a data source. Since multiple data sources are supported, this method takes an index in which the feature object is set. Internally, it initializes a data fetcher object for the provided feature object.

[Example](#classshogun_1_1Example) usage: 
```cpp
DataManager data_mgr;
// feats_0 = some CFeatures instance
// feats_1 = some CFeatures instance
data_mgr.sample_at(0) = feats_0;
data_mgr.sample_at(1) = feats_1;
```

#### Parameters
* `i` The data source index, at which the feature object is to be set as a data source. 

#### Returns
An initializer for the specified data source (that sets up a fetcher for this feature), to be used as lvalue.

#### `public `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`samples_at`](#classshogun_1_1internal_1_1DataManager_1a1502d76318b406a82824888024d535e6)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i) const` {#classshogun_1_1internal_1_1DataManager_1a1502d76318b406a82824888024d535e6}

Getter for feature object at a give data source index.

#### Parameters
* `i` The data source index, from which the feature object is to be obtained 

#### Returns
The underlying [CFeatures](#classshogun_1_1CFeatures) object at the specified data source.

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` & `[`num_samples_at`](#classshogun_1_1internal_1_1DataManager_1a1a7ee11ed90f3bb95be7dedf1ea7b61b)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i)` {#classshogun_1_1internal_1_1DataManager_1a1a7ee11ed90f3bb95be7dedf1ea7b61b}

Setter for the number of samples. Setting this number is mandatory for streaming features. For other type of feature objects, this number equals the number of vectors, and is set internally.

[Example](#classshogun_1_1Example) usage: 
```cpp
DataManager data_mgr;
data_mgr.num_sample_at(0) = 10;
data_mgr.num_sample_at(1) = 15;
```

#### Parameters
* `i` The data source index, at which the number of samples is to be set. 

#### Returns
A reference for the number of samples for the specified data source to be used as lvalue.

#### `public const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`num_samples_at`](#classshogun_1_1internal_1_1DataManager_1a0e3a1256201855c82fe06e2cc07b40cb)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i) const` {#classshogun_1_1internal_1_1DataManager_1a0e3a1256201855c82fe06e2cc07b40cb}

Getter for the number of samples.

#### Parameters
* `i` The data source index, from which the number of samples is to be obtained. 

#### Returns
The number of samples for the specified data source.

#### `public const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`blocksize_at`](#classshogun_1_1internal_1_1DataManager_1ac45d74f98c5dbee568bfe2fbdc45f06e)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i) const` {#classshogun_1_1internal_1_1DataManager_1ac45d74f98c5dbee568bfe2fbdc45f06e}

Getter for the number of samples from a specified data source in a block.

#### Parameters
* `i` The data source index. 

#### Returns
The number of samples from i-th data source in a block.

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`get_num_samples`](#classshogun_1_1internal_1_1DataManager_1a57cf35d53e6f71ea046aed9f6e573630)`() const` {#classshogun_1_1internal_1_1DataManager_1a57cf35d53e6f71ea046aed9f6e573630}

#### Returns
Total number of samples that can be fetched from all the data sources.

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`get_min_blocksize`](#classshogun_1_1internal_1_1DataManager_1aefc324a9750e0d636fdfbf2bd202aa38)`() const` {#classshogun_1_1internal_1_1DataManager_1aefc324a9750e0d636fdfbf2bd202aa38}

#### Returns
The minimum block-size that can be fetched from the specified data sources. For example, if there are two data sources, with samples 20 and 30, respectively, then minimum blocksize can be 5 (2 from 1st data source, 3 from the 2nd), and there can be then 10 such blocks.

