---
classname: "shogun::SGSparseMatrix"
type: "class"
parents:
   - SGReferencedData
---

# class `shogun::SGSparseMatrix` {#classshogun_1_1SGSparseMatrix}

```
class shogun::SGSparseMatrix
  : public SGReferencedData
```

template class [SGSparseMatrix](#classshogun_1_1SGSparseMatrix)

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`num_vectors`](#classshogun_1_1SGSparseMatrix_1a6fac06dc9c6ad5d50478babfa4740090) | total number of vectors
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`num_features`](#classshogun_1_1SGSparseMatrix_1af1bf25fd28f743fadb40a71d608280b6) | total number of features
`public `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< T > * `[`sparse_matrix`](#classshogun_1_1SGSparseMatrix_1a2b610cb0a3ac7745f184f07141f89427) | array of sparse vectors of size num_vectors
`public  `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix_1aa56f7a843902874baf6d8fd9ac500c7d)`()` | default constructor
`public  `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix_1abcc7b6657b471faa86a151856db55e3b)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< T > * vecs,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_feat,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_vec,bool ref_counting)` | constructor for setting params
`public  `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix_1a343c33a3b9467cc4437095073a8a993f)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_feat,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_vec,bool ref_counting)` | constructor to create new matrix in memory
`public  `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix_1ac29f507bfa5ef5b34d798075708bfd00)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > dense)` | constructor to create new sparse matrix from a dense one
`public  `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix_1a36a094fc0e613fbc742e8566aa899ac8)`(const `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)` & orig)` | copy constructor
`public virtual  `[`~SGSparseMatrix`](#classshogun_1_1SGSparseMatrix_1a2ee7c75b54c2d66a52ecbf327c25a457)`()` | destructor
`public inline const `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< T > & `[`operator[]`](#classshogun_1_1SGSparseMatrix_1ae5e86af461dec319fffd592d144c2ae3)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index) const` | index access operator
`public inline `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< T > & `[`operator[]`](#classshogun_1_1SGSparseMatrix_1a1b081b4e94e59abc23d3c1dc8861fe75)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index)` | index access operator
`public inline `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< T > `[`get`](#classshogun_1_1SGSparseMatrix_1a20120349cb92703ef712993330e7cdf4)`()` | get the sparse matrix (no copying is done here)
`public inline const `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`operator*`](#classshogun_1_1SGSparseMatrix_1a0ffee4e8139cc077d3220ad72bcda29f)`(`[`SGVector`](#classshogun_1_1SGVector)`< T > v) const` | compute sparse-matrix dense-vector multiplication 
`public template<>`  <br/>`const `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`operator*`](#classshogun_1_1SGSparseMatrix_1ad23550adfd56b7c98d0986edcb6484d7)`(`[`SGVector`](#classshogun_1_1SGVector)`< ST > v) const` | compute sparse-matrix dense-vector multiplication 
`public inline const T `[`operator()`](#classshogun_1_1SGSparseMatrix_1abb0e4f39231a82d8eb03d668101729a4)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i_row,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i_col) const` | operator overload for sparse-matrix read only access 
`public inline T & `[`operator()`](#classshogun_1_1SGSparseMatrix_1ad04272397d8648956c81226c93f4468b)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i_row,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i_col)` | operator overload for sparse-matrix r/w access 
`public void `[`load`](#classshogun_1_1SGSparseMatrix_1a5d33ec59a4be25056cca1f3b6691ad00)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` | load sparse matrix from file
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`load_with_labels`](#classshogun_1_1SGSparseMatrix_1a5362eace54b0e867768d22bf557275f4)`(`[`CLibSVMFile`](#classshogun_1_1CLibSVMFile)` * libsvm_file,bool do_sort_features)` | load sparse matrix from libsvm file together with labels
`public void `[`save`](#classshogun_1_1SGSparseMatrix_1aff4d5355fe0d9b68bc8c71cd331c082e)`(`[`CFile`](#classshogun_1_1CFile)` * saver)` | save sparse matrix to file
`public void `[`save_with_labels`](#classshogun_1_1SGSparseMatrix_1a970a028f4cbb242c4bd6e285eaa1b3a8)`(`[`CLibSVMFile`](#classshogun_1_1CLibSVMFile)` * saver,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > labels)` | save sparse matrix together with labels to file
`public `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< T > `[`get_transposed`](#classshogun_1_1SGSparseMatrix_1a10e6b2fcf9c8f18f48c6f691f146d643)`()` | return the transposed of the sparse matrix
`public void `[`from_dense`](#classshogun_1_1SGSparseMatrix_1a72ee1dc4773eb2eeba95744cc2f45912)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > full)` | create a sparse matrix from a dense one
`public void `[`sort_features`](#classshogun_1_1SGSparseMatrix_1aa0010ddb91f3132cf24e5266551b7215)`()` | sort the indices of the sparse matrix such that they are in ascending order
`public bool `[`operator==`](#classshogun_1_1SGSparseMatrix_1a3fa4546152dfd953a56f08401c6608fd)`(const `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< T > & other) const` | Pointer identify comparison. 
`public bool `[`equals`](#classshogun_1_1SGSparseMatrix_1a1031dc7bc70ea0a7b20f716dff5b4623)`(const `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< T > & other) const` | Equals method up to precision for matrix (element-wise) 
`public template<>`  <br/>`const `[`SGVector](#classshogun_1_1SGVector)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > `[`operator*`](#classshogun_1_1SGSparseMatrix_1adbdfde34cb308bdb3863cdf3dd6c4988)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > v) const` | 
`public template<>`  <br/>`const `[`SGVector](#classshogun_1_1SGVector)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > `[`operator*`](#classshogun_1_1SGSparseMatrix_1a649eba978ffb426bf12c6006ecb9b14c)`(`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > v) const` | 
`public template<>`  <br/>`const `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`operator*`](#classshogun_1_1SGSparseMatrix_1a9f7f20e22659bad1d94b21c05a00dd3b)`(`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > v) const` | 
`public template<>`  <br/>`void `[`load`](#classshogun_1_1SGSparseMatrix_1a17763c63f0719b10922bc4ed6f392ec4)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` | 
`public template<>`  <br/>[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`load_with_labels`](#classshogun_1_1SGSparseMatrix_1ae88bd50309fbd2ed69009078f8231320)`(`[`CLibSVMFile`](#classshogun_1_1CLibSVMFile)` * file,bool do_sort_features)` | 
`public template<>`  <br/>`void `[`save`](#classshogun_1_1SGSparseMatrix_1aa61bf55fa90bee7cd7e92beaebe38774)`(`[`CFile`](#classshogun_1_1CFile)` * saver)` | 
`public template<>`  <br/>`void `[`save_with_labels`](#classshogun_1_1SGSparseMatrix_1a71f311497245d8f12b3315472dc0c165)`(`[`CLibSVMFile`](#classshogun_1_1CLibSVMFile)` * saver,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > labels)` | 
`public int32_t `[`ref_count`](#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d)`()` | display reference counter
`protected virtual void `[`copy_data`](#classshogun_1_1SGSparseMatrix_1a6e8ddd37b0b245f7cca418642762e16b)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` | copy data
`protected virtual void `[`init_data`](#classshogun_1_1SGSparseMatrix_1a3b42d3bd68c5200393c1f0809ed1facf)`()` | init data
`protected virtual void `[`free_data`](#classshogun_1_1SGSparseMatrix_1ab340ce24b1c9d2b26ab2b46a7a64c346)`()` | free data
`protected void `[`copy_refcount`](#classshogun_1_1SGReferencedData_1a253175a13e8af17d4f2a2cfd9e14dd63)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` | copy refcount
`protected int32_t `[`ref`](#classshogun_1_1SGReferencedData_1ab8c24b912ee57d3f2c81ecccd083582a)`()` | increase reference counter
`protected int32_t `[`unref`](#classshogun_1_1SGReferencedData_1ad99bde1a142a1c07a963169123166e01)`()` | decrement reference counter and deallocate object if refcount is zero before or after decrementing it

## Members

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`num_vectors`](#classshogun_1_1SGSparseMatrix_1a6fac06dc9c6ad5d50478babfa4740090) {#classshogun_1_1SGSparseMatrix_1a6fac06dc9c6ad5d50478babfa4740090}

total number of vectors

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`num_features`](#classshogun_1_1SGSparseMatrix_1af1bf25fd28f743fadb40a71d608280b6) {#classshogun_1_1SGSparseMatrix_1af1bf25fd28f743fadb40a71d608280b6}

total number of features

#### `public `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< T > * `[`sparse_matrix`](#classshogun_1_1SGSparseMatrix_1a2b610cb0a3ac7745f184f07141f89427) {#classshogun_1_1SGSparseMatrix_1a2b610cb0a3ac7745f184f07141f89427}

array of sparse vectors of size num_vectors

#### `public  `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix_1aa56f7a843902874baf6d8fd9ac500c7d)`()` {#classshogun_1_1SGSparseMatrix_1aa56f7a843902874baf6d8fd9ac500c7d}

default constructor

#### `public  `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix_1abcc7b6657b471faa86a151856db55e3b)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< T > * vecs,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_feat,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_vec,bool ref_counting)` {#classshogun_1_1SGSparseMatrix_1abcc7b6657b471faa86a151856db55e3b}

constructor for setting params

#### `public  `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix_1a343c33a3b9467cc4437095073a8a993f)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_feat,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_vec,bool ref_counting)` {#classshogun_1_1SGSparseMatrix_1a343c33a3b9467cc4437095073a8a993f}

constructor to create new matrix in memory

#### `public  `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix_1ac29f507bfa5ef5b34d798075708bfd00)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > dense)` {#classshogun_1_1SGSparseMatrix_1ac29f507bfa5ef5b34d798075708bfd00}

constructor to create new sparse matrix from a dense one

#### Parameters
* `dense` dense matrix to be converted

#### `public  `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix_1a36a094fc0e613fbc742e8566aa899ac8)`(const `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)` & orig)` {#classshogun_1_1SGSparseMatrix_1a36a094fc0e613fbc742e8566aa899ac8}

copy constructor

#### `public virtual  `[`~SGSparseMatrix`](#classshogun_1_1SGSparseMatrix_1a2ee7c75b54c2d66a52ecbf327c25a457)`()` {#classshogun_1_1SGSparseMatrix_1a2ee7c75b54c2d66a52ecbf327c25a457}

destructor

#### `public inline const `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< T > & `[`operator[]`](#classshogun_1_1SGSparseMatrix_1ae5e86af461dec319fffd592d144c2ae3)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index) const` {#classshogun_1_1SGSparseMatrix_1ae5e86af461dec319fffd592d144c2ae3}

index access operator

#### `public inline `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< T > & `[`operator[]`](#classshogun_1_1SGSparseMatrix_1a1b081b4e94e59abc23d3c1dc8861fe75)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index)` {#classshogun_1_1SGSparseMatrix_1a1b081b4e94e59abc23d3c1dc8861fe75}

index access operator

#### `public inline `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< T > `[`get`](#classshogun_1_1SGSparseMatrix_1a20120349cb92703ef712993330e7cdf4)`()` {#classshogun_1_1SGSparseMatrix_1a20120349cb92703ef712993330e7cdf4}

get the sparse matrix (no copying is done here)

#### Returns
the refcount increased matrix

#### `public inline const `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`operator*`](#classshogun_1_1SGSparseMatrix_1a0ffee4e8139cc077d3220ad72bcda29f)`(`[`SGVector`](#classshogun_1_1SGVector)`< T > v) const` {#classshogun_1_1SGSparseMatrix_1a0ffee4e8139cc077d3220ad72bcda29f}

compute sparse-matrix dense-vector multiplication 
#### Parameters
* `v` the dense-vector to be multiplied with 

#### Returns
the result vector $Q*v$, Q being this sparse matrix

#### `public template<>`  <br/>`const `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`operator*`](#classshogun_1_1SGSparseMatrix_1ad23550adfd56b7c98d0986edcb6484d7)`(`[`SGVector`](#classshogun_1_1SGVector)`< ST > v) const` {#classshogun_1_1SGSparseMatrix_1ad23550adfd56b7c98d0986edcb6484d7}

compute sparse-matrix dense-vector multiplication 
#### Parameters
* `v` the dense-vector to be multiplied with 

#### Returns
the result vector $Q*v$, Q being this sparse matrix

#### `public inline const T `[`operator()`](#classshogun_1_1SGSparseMatrix_1abb0e4f39231a82d8eb03d668101729a4)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i_row,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i_col) const` {#classshogun_1_1SGSparseMatrix_1abb0e4f39231a82d8eb03d668101729a4}

operator overload for sparse-matrix read only access 
#### Parameters
* `i_row` 

* `i_col`

#### `public inline T & `[`operator()`](#classshogun_1_1SGSparseMatrix_1ad04272397d8648956c81226c93f4468b)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i_row,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i_col)` {#classshogun_1_1SGSparseMatrix_1ad04272397d8648956c81226c93f4468b}

operator overload for sparse-matrix r/w access 
#### Parameters
* `i_row` 

* `i_col`

#### `public void `[`load`](#classshogun_1_1SGSparseMatrix_1a5d33ec59a4be25056cca1f3b6691ad00)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` {#classshogun_1_1SGSparseMatrix_1a5d33ec59a4be25056cca1f3b6691ad00}

load sparse matrix from file

#### Parameters
* `loader` File object via which to load data

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`load_with_labels`](#classshogun_1_1SGSparseMatrix_1a5362eace54b0e867768d22bf557275f4)`(`[`CLibSVMFile`](#classshogun_1_1CLibSVMFile)` * libsvm_file,bool do_sort_features)` {#classshogun_1_1SGSparseMatrix_1a5362eace54b0e867768d22bf557275f4}

load sparse matrix from libsvm file together with labels

#### Parameters
* `libsvm_file` the libsvm file 

* `do_sort_features` whether to sort the vector indices (such that they are in ascending order) after loading 

#### Returns
label vector

#### `public void `[`save`](#classshogun_1_1SGSparseMatrix_1aff4d5355fe0d9b68bc8c71cd331c082e)`(`[`CFile`](#classshogun_1_1CFile)` * saver)` {#classshogun_1_1SGSparseMatrix_1aff4d5355fe0d9b68bc8c71cd331c082e}

save sparse matrix to file

#### Parameters
* `saver` File object via which to save data

#### `public void `[`save_with_labels`](#classshogun_1_1SGSparseMatrix_1a970a028f4cbb242c4bd6e285eaa1b3a8)`(`[`CLibSVMFile`](#classshogun_1_1CLibSVMFile)` * saver,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > labels)` {#classshogun_1_1SGSparseMatrix_1a970a028f4cbb242c4bd6e285eaa1b3a8}

save sparse matrix together with labels to file

#### Parameters
* `saver` File object via which to save data 

* `labels` label vector

#### `public `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< T > `[`get_transposed`](#classshogun_1_1SGSparseMatrix_1a10e6b2fcf9c8f18f48c6f691f146d643)`()` {#classshogun_1_1SGSparseMatrix_1a10e6b2fcf9c8f18f48c6f691f146d643}

return the transposed of the sparse matrix

#### `public void `[`from_dense`](#classshogun_1_1SGSparseMatrix_1a72ee1dc4773eb2eeba95744cc2f45912)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > full)` {#classshogun_1_1SGSparseMatrix_1a72ee1dc4773eb2eeba95744cc2f45912}

create a sparse matrix from a dense one

#### Parameters
* `full` the dense matrix to create the sparse one from

#### `public void `[`sort_features`](#classshogun_1_1SGSparseMatrix_1aa0010ddb91f3132cf24e5266551b7215)`()` {#classshogun_1_1SGSparseMatrix_1aa0010ddb91f3132cf24e5266551b7215}

sort the indices of the sparse matrix such that they are in ascending order

#### `public bool `[`operator==`](#classshogun_1_1SGSparseMatrix_1a3fa4546152dfd953a56f08401c6608fd)`(const `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< T > & other) const` {#classshogun_1_1SGSparseMatrix_1a3fa4546152dfd953a56f08401c6608fd}

Pointer identify comparison. 
#### Returns
true iff number of vectors and features and pointer are equal

#### `public bool `[`equals`](#classshogun_1_1SGSparseMatrix_1a1031dc7bc70ea0a7b20f716dff5b4623)`(const `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< T > & other) const` {#classshogun_1_1SGSparseMatrix_1a1031dc7bc70ea0a7b20f716dff5b4623}

Equals method up to precision for matrix (element-wise) 
#### Parameters
* `other` matrix to compare with 

#### Returns
false if any element differs or if shapes are different, true otherwise

#### `public template<>`  <br/>`const `[`SGVector](#classshogun_1_1SGVector)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > `[`operator*`](#classshogun_1_1SGSparseMatrix_1adbdfde34cb308bdb3863cdf3dd6c4988)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > v) const` {#classshogun_1_1SGSparseMatrix_1adbdfde34cb308bdb3863cdf3dd6c4988}

#### `public template<>`  <br/>`const `[`SGVector](#classshogun_1_1SGVector)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > `[`operator*`](#classshogun_1_1SGSparseMatrix_1a649eba978ffb426bf12c6006ecb9b14c)`(`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > v) const` {#classshogun_1_1SGSparseMatrix_1a649eba978ffb426bf12c6006ecb9b14c}

#### `public template<>`  <br/>`const `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`operator*`](#classshogun_1_1SGSparseMatrix_1a9f7f20e22659bad1d94b21c05a00dd3b)`(`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > v) const` {#classshogun_1_1SGSparseMatrix_1a9f7f20e22659bad1d94b21c05a00dd3b}

#### `public template<>`  <br/>`void `[`load`](#classshogun_1_1SGSparseMatrix_1a17763c63f0719b10922bc4ed6f392ec4)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` {#classshogun_1_1SGSparseMatrix_1a17763c63f0719b10922bc4ed6f392ec4}

#### `public template<>`  <br/>[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`load_with_labels`](#classshogun_1_1SGSparseMatrix_1ae88bd50309fbd2ed69009078f8231320)`(`[`CLibSVMFile`](#classshogun_1_1CLibSVMFile)` * file,bool do_sort_features)` {#classshogun_1_1SGSparseMatrix_1ae88bd50309fbd2ed69009078f8231320}

#### `public template<>`  <br/>`void `[`save`](#classshogun_1_1SGSparseMatrix_1aa61bf55fa90bee7cd7e92beaebe38774)`(`[`CFile`](#classshogun_1_1CFile)` * saver)` {#classshogun_1_1SGSparseMatrix_1aa61bf55fa90bee7cd7e92beaebe38774}

#### `public template<>`  <br/>`void `[`save_with_labels`](#classshogun_1_1SGSparseMatrix_1a71f311497245d8f12b3315472dc0c165)`(`[`CLibSVMFile`](#classshogun_1_1CLibSVMFile)` * saver,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > labels)` {#classshogun_1_1SGSparseMatrix_1a71f311497245d8f12b3315472dc0c165}

#### `public int32_t `[`ref_count`](#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d)`()` {#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d}

display reference counter

#### Returns
reference count

#### `protected virtual void `[`copy_data`](#classshogun_1_1SGSparseMatrix_1a6e8ddd37b0b245f7cca418642762e16b)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` {#classshogun_1_1SGSparseMatrix_1a6e8ddd37b0b245f7cca418642762e16b}

copy data

#### `protected virtual void `[`init_data`](#classshogun_1_1SGSparseMatrix_1a3b42d3bd68c5200393c1f0809ed1facf)`()` {#classshogun_1_1SGSparseMatrix_1a3b42d3bd68c5200393c1f0809ed1facf}

init data

#### `protected virtual void `[`free_data`](#classshogun_1_1SGSparseMatrix_1ab340ce24b1c9d2b26ab2b46a7a64c346)`()` {#classshogun_1_1SGSparseMatrix_1ab340ce24b1c9d2b26ab2b46a7a64c346}

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

