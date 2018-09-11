---
classname: "shogun::CKNNHeap"
type: "class"
---

# class `shogun::CKNNHeap` {#classshogun_1_1CKNNHeap}

This class implements a specialized version of max heap structure. This heap specializes in storing the least k values seen so far along with the indices (or id) of the entities with which the values are associated. On calling the push method, it is automatically checked, if the new value supplied, is among the least k distances seen so far. Also, in case the heap is full already, the max among the stored values is automatically thrown out as the new value finds its proper place in the heap.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public  `[`CKNNHeap`](#classshogun_1_1CKNNHeap_1a9922b7b5ec540e4edfef79da06cbee66)`(int32_t k)` | constructor
`public inline  `[`~CKNNHeap`](#classshogun_1_1CKNNHeap_1a39c5ee42b397885d2e6d1bae416b1beb)`()` | destructor
`public void `[`push`](#classshogun_1_1CKNNHeap_1a9e13e4efd20594bb914623159e1915df)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` dist)` | push into heap
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_max_dist`](#classshogun_1_1CKNNHeap_1af2303228173e880d8ddebb2b314442b0)`()` | max distance
`public inline `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`get_max_index`](#classshogun_1_1CKNNHeap_1ab8ac64eeea8e7ef14450249490d40a3e)`()` | max index
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_dists`](#classshogun_1_1CKNNHeap_1ad8fd0946bdc845eb98af4424e0088da3)`()` | get distances
`public `[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > `[`get_indices`](#classshogun_1_1CKNNHeap_1a8338fbcf409d07c88dbfc9977d0f6a30)`()` | get indices

## Members

#### `public  `[`CKNNHeap`](#classshogun_1_1CKNNHeap_1a9922b7b5ec540e4edfef79da06cbee66)`(int32_t k)` {#classshogun_1_1CKNNHeap_1a9922b7b5ec540e4edfef79da06cbee66}

constructor

#### Parameters
* `k` heap capacity i.e. the number of least distance values to be stored

#### `public inline  `[`~CKNNHeap`](#classshogun_1_1CKNNHeap_1a39c5ee42b397885d2e6d1bae416b1beb)`()` {#classshogun_1_1CKNNHeap_1a39c5ee42b397885d2e6d1bae416b1beb}

destructor

#### `public void `[`push`](#classshogun_1_1CKNNHeap_1a9e13e4efd20594bb914623159e1915df)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` dist)` {#classshogun_1_1CKNNHeap_1a9e13e4efd20594bb914623159e1915df}

push into heap

#### Parameters
* `index` vector id whose distance value is pushed into the heap 

* `dist` distance value of the vector id index from the query point

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_max_dist`](#classshogun_1_1CKNNHeap_1af2303228173e880d8ddebb2b314442b0)`()` {#classshogun_1_1CKNNHeap_1af2303228173e880d8ddebb2b314442b0}

max distance

#### Returns
max distance value stored in the heap

#### `public inline `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`get_max_index`](#classshogun_1_1CKNNHeap_1ab8ac64eeea8e7ef14450249490d40a3e)`()` {#classshogun_1_1CKNNHeap_1ab8ac64eeea8e7ef14450249490d40a3e}

max index

#### Returns
vector id of the max distance stored

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_dists`](#classshogun_1_1CKNNHeap_1ad8fd0946bdc845eb98af4424e0088da3)`()` {#classshogun_1_1CKNNHeap_1ad8fd0946bdc845eb98af4424e0088da3}

get distances

#### Returns
distances stored in the heap

#### `public `[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > `[`get_indices`](#classshogun_1_1CKNNHeap_1a8338fbcf409d07c88dbfc9977d0f6a30)`()` {#classshogun_1_1CKNNHeap_1a8338fbcf409d07c88dbfc9977d0f6a30}

get indices

#### Returns
indices stored in the heap

