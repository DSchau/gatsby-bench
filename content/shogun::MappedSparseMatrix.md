---
classname: "shogun::MappedSparseMatrix"
type: "class"
---

# class `shogun::MappedSparseMatrix` {#classshogun_1_1MappedSparseMatrix}

mapped sparse matrix for representing graph relations of tasks

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public std::vector< std::map< `[`index_t](#common_8h_1a6da8132ec1234c0d616142e3a246f858), [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > > `[`data`](#classshogun_1_1MappedSparseMatrix_1a701f05ea95da23f7c601883b6f9ce484) | under-the-hood data structure
`public inline const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`operator()`](#classshogun_1_1MappedSparseMatrix_1aa6799d1e27785386d0a1d2e80487b2ab)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i_row,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i_col) const` | operator overload for matrix read only access 
`public inline void `[`set_from_sparse`](#classshogun_1_1MappedSparseMatrix_1ab91019aa13ae17a5a582653b49109fd3)`(const `[`SGSparseMatrix](#classshogun_1_1SGSparseMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > & sgm)` | set matrix from [SGSparseMatrix](#classshogun_1_1SGSparseMatrix)

## Members

#### `public std::vector< std::map< `[`index_t](#common_8h_1a6da8132ec1234c0d616142e3a246f858), [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > > `[`data`](#classshogun_1_1MappedSparseMatrix_1a701f05ea95da23f7c601883b6f9ce484) {#classshogun_1_1MappedSparseMatrix_1a701f05ea95da23f7c601883b6f9ce484}

under-the-hood data structure

#### `public inline const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`operator()`](#classshogun_1_1MappedSparseMatrix_1aa6799d1e27785386d0a1d2e80487b2ab)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i_row,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i_col) const` {#classshogun_1_1MappedSparseMatrix_1aa6799d1e27785386d0a1d2e80487b2ab}

operator overload for matrix read only access 
#### Parameters
* `i_row` 

* `i_col`

#### `public inline void `[`set_from_sparse`](#classshogun_1_1MappedSparseMatrix_1ab91019aa13ae17a5a582653b49109fd3)`(const `[`SGSparseMatrix](#classshogun_1_1SGSparseMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > & sgm)` {#classshogun_1_1MappedSparseMatrix_1ab91019aa13ae17a5a582653b49109fd3}

set matrix from [SGSparseMatrix](#classshogun_1_1SGSparseMatrix)
#### Parameters
* `sgm`

