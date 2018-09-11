---
classname: "shogun::SGSparseVector"
type: "class"
parents:
   - SGReferencedData
---

# class `shogun::SGSparseVector` {#classshogun_1_1SGSparseVector}

```
class shogun::SGSparseVector
  : public SGReferencedData
```

template class [SGSparseVector](#classshogun_1_1SGSparseVector) The assumtion is that the stored SGSparseVectorEntry<T>* vector is ordered by [SGSparseVectorEntry.feat_index](#structshogun_1_1SGSparseVectorEntry_1a0a6fba3a4847624bddb747a393bd7e2c) in non-decreasing order. This has to be assured by the user of the class.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`num_feat_entries`](#classshogun_1_1SGSparseVector_1a6cf2fe4392c31c6af4ba8fdd490eaf14) | number of feature entries
`public `[`SGSparseVectorEntry`](#structshogun_1_1SGSparseVectorEntry)`< T > * `[`features`](#classshogun_1_1SGSparseVector_1a8da1d3461097a812935b4b987ba339fe) | features
`public  `[`SGSparseVector`](#classshogun_1_1SGSparseVector_1a9cc6c62fe4f811a0dab1c85f45a84818)`()` | default constructor
`public  `[`SGSparseVector`](#classshogun_1_1SGSparseVector_1a83ad18e52981dd288d28c5ba065e290b)`(`[`SGSparseVectorEntry`](#structshogun_1_1SGSparseVectorEntry)`< T > * feats,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_entries,bool ref_counting)` | constructor for setting params
`public  `[`SGSparseVector`](#classshogun_1_1SGSparseVector_1a1d871f895593c28760b064e2232f9b36)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_entries,bool ref_counting)` | constructor to create new vector in memory
`public  `[`SGSparseVector`](#classshogun_1_1SGSparseVector_1ade701bfbb22be3581e26d72349a25640)`(const `[`SGSparseVector`](#classshogun_1_1SGSparseVector)` & orig)` | copy constructor
`public virtual  `[`~SGSparseVector`](#classshogun_1_1SGSparseVector_1ab3be82c004a3f0a5d620c19661fbcc1f)`()` | 
`public T `[`dense_dot`](#classshogun_1_1SGSparseVector_1ab58916351a4d76adc458739145612516)`(T alpha,T * vec,int32_t dim,T b)` | compute the dot product between dense weights and a sparse feature vector alpha * sparse^T * w + b
`public template<>`  <br/>`T `[`dense_dot`](#classshogun_1_1SGSparseVector_1a01cc19f3d2292b49790c3274110738b5)`(`[`SGVector`](#classshogun_1_1SGVector)`< ST > vec)` | compute the dot product between dense weights and a sparse feature vector sparse^T * w
`public T `[`sparse_dot`](#classshogun_1_1SGSparseVector_1ad8cc44044786b6c5aaef947095477112)`(const `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< T > & v)` | compute the dot product between current sparse vector and a given sparse vector. sparse_a^T * sparse_b
`public inline `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< T > `[`get`](#classshogun_1_1SGSparseVector_1a0783eb336c74ea031fe24be60f7a8820)`()` | get the sparse vector (no copying is done here)
`public int32_t `[`get_num_dimensions`](#classshogun_1_1SGSparseVector_1a84b9667dbfc0be8f47cf8721e46d59d2)`()` | get number of dimensions
`public void `[`sort_features`](#classshogun_1_1SGSparseVector_1ac773053877b5ea4fcf90a84a2658778f)`(bool stable_pointer)` | sort features by indices (Setting stable_pointer=true to guarantee that pointer features does not change. On the other hand, stable_pointer=false can shrink the vector if possible.)
`public bool `[`is_sorted`](#classshogun_1_1SGSparseVector_1a343961e93957293edc0602052f9d9abf)`() const` | Utility function to tell if feature indices are sorted
`public T `[`get_feature`](#classshogun_1_1SGSparseVector_1ae7b81e68af898b6d2660576fab103478)`(int32_t index)` | get feature value for index
`public `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`get_dense`](#classshogun_1_1SGSparseVector_1a6dae91dfa9cbfb21f7b8580f0658f934)`(int32_t dimension)` | get dense representation of given size
`public `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`get_dense`](#classshogun_1_1SGSparseVector_1a2ce36c386a1e904d806b97bc5befc3d7)`()` | get shortet dense representation for sparse vector
`public `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< T > `[`clone`](#classshogun_1_1SGSparseVector_1ac55177478fee490a629f23a56d97851f)`() const` | clone vector
`public void `[`load`](#classshogun_1_1SGSparseVector_1a5d33ec59a4be25056cca1f3b6691ad00)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` | load vector from file
`public void `[`save`](#classshogun_1_1SGSparseVector_1aff4d5355fe0d9b68bc8c71cd331c082e)`(`[`CFile`](#classshogun_1_1CFile)` * saver)` | save vector to file
`public void `[`add_to_dense`](#classshogun_1_1SGSparseVector_1af4354b5c1ee9ae5eb8283da4b0731343)`(T alpha,T * vec,int32_t dim,bool abs_val)` | add a sparse feature vector onto a dense one dense += alpha*sparse
`public void `[`display_vector`](#classshogun_1_1SGSparseVector_1a63cdd03367ce03c52466124cef9415c7)`(const char * name,const char * prefix)` | display vector
`public inline bool `[`operator==`](#classshogun_1_1SGSparseVector_1a7763bf96ef47e8ed5559b3982f48a05d)`(const `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< T > & other) const` | Pointer identify comparison. 
`public bool `[`equals`](#classshogun_1_1SGSparseVector_1a10e0252b81b68ebe4136e81fc29992bc)`(const `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< T > & other) const` | 
`public template<>`  <br/>`void `[`load`](#classshogun_1_1SGSparseVector_1a17763c63f0719b10922bc4ed6f392ec4)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` | 
`public template<>`  <br/>`void `[`save`](#classshogun_1_1SGSparseVector_1aa61bf55fa90bee7cd7e92beaebe38774)`(`[`CFile`](#classshogun_1_1CFile)` * saver)` | 
`public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGSparseVector_1a7b2121f1f19fd05e8dcb2930711242bf)`(const char * name,const char * prefix)` | 
`public int32_t `[`ref_count`](#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d)`()` | display reference counter
`protected virtual void `[`copy_data`](#classshogun_1_1SGSparseVector_1a6e8ddd37b0b245f7cca418642762e16b)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` | needs to be overridden to copy data
`protected virtual void `[`init_data`](#classshogun_1_1SGSparseVector_1a3b42d3bd68c5200393c1f0809ed1facf)`()` | needs to be overridden to initialize empty data
`protected virtual void `[`free_data`](#classshogun_1_1SGSparseVector_1ab340ce24b1c9d2b26ab2b46a7a64c346)`()` | needs to be overridden to free data
`protected void `[`copy_refcount`](#classshogun_1_1SGReferencedData_1a253175a13e8af17d4f2a2cfd9e14dd63)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` | copy refcount
`protected int32_t `[`ref`](#classshogun_1_1SGReferencedData_1ab8c24b912ee57d3f2c81ecccd083582a)`()` | increase reference counter
`protected int32_t `[`unref`](#classshogun_1_1SGReferencedData_1ad99bde1a142a1c07a963169123166e01)`()` | decrement reference counter and deallocate object if refcount is zero before or after decrementing it

## Members

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`num_feat_entries`](#classshogun_1_1SGSparseVector_1a6cf2fe4392c31c6af4ba8fdd490eaf14) {#classshogun_1_1SGSparseVector_1a6cf2fe4392c31c6af4ba8fdd490eaf14}

number of feature entries

#### `public `[`SGSparseVectorEntry`](#structshogun_1_1SGSparseVectorEntry)`< T > * `[`features`](#classshogun_1_1SGSparseVector_1a8da1d3461097a812935b4b987ba339fe) {#classshogun_1_1SGSparseVector_1a8da1d3461097a812935b4b987ba339fe}

features

#### `public  `[`SGSparseVector`](#classshogun_1_1SGSparseVector_1a9cc6c62fe4f811a0dab1c85f45a84818)`()` {#classshogun_1_1SGSparseVector_1a9cc6c62fe4f811a0dab1c85f45a84818}

default constructor

#### `public  `[`SGSparseVector`](#classshogun_1_1SGSparseVector_1a83ad18e52981dd288d28c5ba065e290b)`(`[`SGSparseVectorEntry`](#structshogun_1_1SGSparseVectorEntry)`< T > * feats,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_entries,bool ref_counting)` {#classshogun_1_1SGSparseVector_1a83ad18e52981dd288d28c5ba065e290b}

constructor for setting params

#### Parameters
* `feats` vector of [SGSparseVectorEntry](#structshogun_1_1SGSparseVectorEntry) ordered by [SGSparseVectorEntry.feat_index](#structshogun_1_1SGSparseVectorEntry_1a0a6fba3a4847624bddb747a393bd7e2c) in non-decreasing order 

* `num_entries` number of elements in feats vector 

* `ref_counting` use reference counting

#### `public  `[`SGSparseVector`](#classshogun_1_1SGSparseVector_1a1d871f895593c28760b064e2232f9b36)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_entries,bool ref_counting)` {#classshogun_1_1SGSparseVector_1a1d871f895593c28760b064e2232f9b36}

constructor to create new vector in memory

#### `public  `[`SGSparseVector`](#classshogun_1_1SGSparseVector_1ade701bfbb22be3581e26d72349a25640)`(const `[`SGSparseVector`](#classshogun_1_1SGSparseVector)` & orig)` {#classshogun_1_1SGSparseVector_1ade701bfbb22be3581e26d72349a25640}

copy constructor

#### `public virtual  `[`~SGSparseVector`](#classshogun_1_1SGSparseVector_1ab3be82c004a3f0a5d620c19661fbcc1f)`()` {#classshogun_1_1SGSparseVector_1ab3be82c004a3f0a5d620c19661fbcc1f}

#### `public T `[`dense_dot`](#classshogun_1_1SGSparseVector_1ab58916351a4d76adc458739145612516)`(T alpha,T * vec,int32_t dim,T b)` {#classshogun_1_1SGSparseVector_1ab58916351a4d76adc458739145612516}

compute the dot product between dense weights and a sparse feature vector alpha * sparse^T * w + b

possible with subset

#### Parameters
* `alpha` scalar to multiply with 

* `vec` dense vector to compute dot product with 

* `dim` length of the dense vector 

* `b` bias 

#### Returns
dot product between dense weights and a sparse feature vector

#### `public template<>`  <br/>`T `[`dense_dot`](#classshogun_1_1SGSparseVector_1a01cc19f3d2292b49790c3274110738b5)`(`[`SGVector`](#classshogun_1_1SGVector)`< ST > vec)` {#classshogun_1_1SGSparseVector_1a01cc19f3d2292b49790c3274110738b5}

compute the dot product between dense weights and a sparse feature vector sparse^T * w

#### Parameters
* `vec` dense vector to compute dot product with 

#### Returns
dot product between dense weights and a sparse feature vector

#### `public T `[`sparse_dot`](#classshogun_1_1SGSparseVector_1ad8cc44044786b6c5aaef947095477112)`(const `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< T > & v)` {#classshogun_1_1SGSparseVector_1ad8cc44044786b6c5aaef947095477112}

compute the dot product between current sparse vector and a given sparse vector. sparse_a^T * sparse_b

#### Parameters
* `v` sparse vector 

#### Returns
dot product between the current sparse vector and v sparse vector

#### `public inline `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< T > `[`get`](#classshogun_1_1SGSparseVector_1a0783eb336c74ea031fe24be60f7a8820)`()` {#classshogun_1_1SGSparseVector_1a0783eb336c74ea031fe24be60f7a8820}

get the sparse vector (no copying is done here)

#### Returns
the refcount increased vector

#### `public int32_t `[`get_num_dimensions`](#classshogun_1_1SGSparseVector_1a84b9667dbfc0be8f47cf8721e46d59d2)`()` {#classshogun_1_1SGSparseVector_1a84b9667dbfc0be8f47cf8721e46d59d2}

get number of dimensions

#### Returns
largest feature index

#### `public void `[`sort_features`](#classshogun_1_1SGSparseVector_1ac773053877b5ea4fcf90a84a2658778f)`(bool stable_pointer)` {#classshogun_1_1SGSparseVector_1ac773053877b5ea4fcf90a84a2658778f}

sort features by indices (Setting stable_pointer=true to guarantee that pointer features does not change. On the other hand, stable_pointer=false can shrink the vector if possible.)

#### Parameters
* `stable_pointer` (default false) enforce stable pointer

#### `public bool `[`is_sorted`](#classshogun_1_1SGSparseVector_1a343961e93957293edc0602052f9d9abf)`() const` {#classshogun_1_1SGSparseVector_1a343961e93957293edc0602052f9d9abf}

Utility function to tell if feature indices are sorted

#### Returns
bool (true if sorted, else false)

#### `public T `[`get_feature`](#classshogun_1_1SGSparseVector_1ae7b81e68af898b6d2660576fab103478)`(int32_t index)` {#classshogun_1_1SGSparseVector_1ae7b81e68af898b6d2660576fab103478}

get feature value for index

#### Parameters
* `index` 

#### Returns
value

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`get_dense`](#classshogun_1_1SGSparseVector_1a6dae91dfa9cbfb21f7b8580f0658f934)`(int32_t dimension)` {#classshogun_1_1SGSparseVector_1a6dae91dfa9cbfb21f7b8580f0658f934}

get dense representation of given size

#### Parameters
* `dimension` of requested dense vector 

#### Returns
SGVector<T>

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`get_dense`](#classshogun_1_1SGSparseVector_1a2ce36c386a1e904d806b97bc5befc3d7)`()` {#classshogun_1_1SGSparseVector_1a2ce36c386a1e904d806b97bc5befc3d7}

get shortet dense representation for sparse vector

#### Returns
SGVector<T>

#### `public `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< T > `[`clone`](#classshogun_1_1SGSparseVector_1ac55177478fee490a629f23a56d97851f)`() const` {#classshogun_1_1SGSparseVector_1ac55177478fee490a629f23a56d97851f}

clone vector

#### `public void `[`load`](#classshogun_1_1SGSparseVector_1a5d33ec59a4be25056cca1f3b6691ad00)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` {#classshogun_1_1SGSparseVector_1a5d33ec59a4be25056cca1f3b6691ad00}

load vector from file

#### Parameters
* `loader` File object via which to load data

#### `public void `[`save`](#classshogun_1_1SGSparseVector_1aff4d5355fe0d9b68bc8c71cd331c082e)`(`[`CFile`](#classshogun_1_1CFile)` * saver)` {#classshogun_1_1SGSparseVector_1aff4d5355fe0d9b68bc8c71cd331c082e}

save vector to file

#### Parameters
* `saver` File object via which to save data

#### `public void `[`add_to_dense`](#classshogun_1_1SGSparseVector_1af4354b5c1ee9ae5eb8283da4b0731343)`(T alpha,T * vec,int32_t dim,bool abs_val)` {#classshogun_1_1SGSparseVector_1af4354b5c1ee9ae5eb8283da4b0731343}

add a sparse feature vector onto a dense one dense += alpha*sparse

#### Parameters
* `alpha` scalar to multiply with 

* `vec` dense vector 

* `dim` length of the dense vector 

* `abs_val` if true, do dense+=alpha*abs(sparse)

#### `public void `[`display_vector`](#classshogun_1_1SGSparseVector_1a63cdd03367ce03c52466124cef9415c7)`(const char * name,const char * prefix)` {#classshogun_1_1SGSparseVector_1a63cdd03367ce03c52466124cef9415c7}

display vector

#### Parameters
* `name` vector name in output 

* `prefix` prepend on every entry

#### `public inline bool `[`operator==`](#classshogun_1_1SGSparseVector_1a7763bf96ef47e8ed5559b3982f48a05d)`(const `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< T > & other) const` {#classshogun_1_1SGSparseVector_1a7763bf96ef47e8ed5559b3982f48a05d}

Pointer identify comparison. 
#### Returns
true iff length and pointer are equal

#### `public bool `[`equals`](#classshogun_1_1SGSparseVector_1a10e0252b81b68ebe4136e81fc29992bc)`(const `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< T > & other) const` {#classshogun_1_1SGSparseVector_1a10e0252b81b68ebe4136e81fc29992bc}

#### `public template<>`  <br/>`void `[`load`](#classshogun_1_1SGSparseVector_1a17763c63f0719b10922bc4ed6f392ec4)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` {#classshogun_1_1SGSparseVector_1a17763c63f0719b10922bc4ed6f392ec4}

#### `public template<>`  <br/>`void `[`save`](#classshogun_1_1SGSparseVector_1aa61bf55fa90bee7cd7e92beaebe38774)`(`[`CFile`](#classshogun_1_1CFile)` * saver)` {#classshogun_1_1SGSparseVector_1aa61bf55fa90bee7cd7e92beaebe38774}

#### `public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGSparseVector_1a7b2121f1f19fd05e8dcb2930711242bf)`(const char * name,const char * prefix)` {#classshogun_1_1SGSparseVector_1a7b2121f1f19fd05e8dcb2930711242bf}

#### `public int32_t `[`ref_count`](#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d)`()` {#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d}

display reference counter

#### Returns
reference count

#### `protected virtual void `[`copy_data`](#classshogun_1_1SGSparseVector_1a6e8ddd37b0b245f7cca418642762e16b)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` {#classshogun_1_1SGSparseVector_1a6e8ddd37b0b245f7cca418642762e16b}

needs to be overridden to copy data

#### `protected virtual void `[`init_data`](#classshogun_1_1SGSparseVector_1a3b42d3bd68c5200393c1f0809ed1facf)`()` {#classshogun_1_1SGSparseVector_1a3b42d3bd68c5200393c1f0809ed1facf}

needs to be overridden to initialize empty data

#### `protected virtual void `[`free_data`](#classshogun_1_1SGSparseVector_1ab340ce24b1c9d2b26ab2b46a7a64c346)`()` {#classshogun_1_1SGSparseVector_1ab340ce24b1c9d2b26ab2b46a7a64c346}

needs to be overridden to free data

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

