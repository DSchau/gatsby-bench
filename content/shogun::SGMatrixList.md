---
classname: "shogun::SGMatrixList"
type: "class"
parents:
   - SGReferencedData
---

# class `shogun::SGMatrixList` {#classshogun_1_1SGMatrixList}

```
class shogun::SGMatrixList
  : public SGReferencedData
```

shogun matrix list

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > * `[`matrix_list`](#classshogun_1_1SGMatrixList_1abba92d16ac07bc480b7592447c786552) | matrix list
`public int32_t `[`num_matrices`](#classshogun_1_1SGMatrixList_1abbf09fb5e6b0a87992558f5b9648ed55) | number of matrices of matrix list
`public  `[`SGMatrixList`](#classshogun_1_1SGMatrixList_1ab6ea84a62c71d42734ddfc9c4ac66162)`()` | default constructor
`public  `[`SGMatrixList`](#classshogun_1_1SGMatrixList_1a677bd751ae7f31695588e5f5e90ba46d)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > * ml,int32_t nmats,bool ref_counting)` | constructor for setting parameters
`public  `[`SGMatrixList`](#classshogun_1_1SGMatrixList_1a2c0165133cccf281a0ddaf1380caf982)`(int32_t nmats,bool ref_counting)` | constructor to create a new matrix list in memory
`public  `[`SGMatrixList`](#classshogun_1_1SGMatrixList_1abd3b46ee5ada85fa633ae2b8efeee265)`(`[`SGMatrixList`](#classshogun_1_1SGMatrixList)` const & orig)` | copy constructor
`public virtual  `[`~SGMatrixList`](#classshogun_1_1SGMatrixList_1a72b1919347e4633115f3bf5c8ef41e9d)`()` | destructor
`public `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`get_matrix`](#classshogun_1_1SGMatrixList_1a09f87efd18c281bb2d0378d937d34eeb)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index) const` | get a matrix of the list
`public `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`operator[]`](#classshogun_1_1SGMatrixList_1a8ba2cb22a361b3b9f4c41ec7e8bec4ac)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index) const` | operator overload to get a matrix for read & write access
`public void `[`set_matrix`](#classshogun_1_1SGMatrixList_1a03d3dc1c4940e6e39a3c27e80cc2742d)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index,const `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > matrix)` | set a matrix of the list
`public int32_t `[`ref_count`](#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d)`()` | display reference counter
`protected virtual void `[`copy_data`](#classshogun_1_1SGMatrixList_1a6e8ddd37b0b245f7cca418642762e16b)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` | copy data
`protected virtual void `[`init_data`](#classshogun_1_1SGMatrixList_1a3b42d3bd68c5200393c1f0809ed1facf)`()` | initialize empty data
`protected virtual void `[`free_data`](#classshogun_1_1SGMatrixList_1ab340ce24b1c9d2b26ab2b46a7a64c346)`()` | free data
`protected void `[`copy_refcount`](#classshogun_1_1SGReferencedData_1a253175a13e8af17d4f2a2cfd9e14dd63)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` | copy refcount
`protected int32_t `[`ref`](#classshogun_1_1SGReferencedData_1ab8c24b912ee57d3f2c81ecccd083582a)`()` | increase reference counter
`protected int32_t `[`unref`](#classshogun_1_1SGReferencedData_1ad99bde1a142a1c07a963169123166e01)`()` | decrement reference counter and deallocate object if refcount is zero before or after decrementing it

## Members

#### `public `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > * `[`matrix_list`](#classshogun_1_1SGMatrixList_1abba92d16ac07bc480b7592447c786552) {#classshogun_1_1SGMatrixList_1abba92d16ac07bc480b7592447c786552}

matrix list

#### `public int32_t `[`num_matrices`](#classshogun_1_1SGMatrixList_1abbf09fb5e6b0a87992558f5b9648ed55) {#classshogun_1_1SGMatrixList_1abbf09fb5e6b0a87992558f5b9648ed55}

number of matrices of matrix list

#### `public  `[`SGMatrixList`](#classshogun_1_1SGMatrixList_1ab6ea84a62c71d42734ddfc9c4ac66162)`()` {#classshogun_1_1SGMatrixList_1ab6ea84a62c71d42734ddfc9c4ac66162}

default constructor

#### `public  `[`SGMatrixList`](#classshogun_1_1SGMatrixList_1a677bd751ae7f31695588e5f5e90ba46d)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > * ml,int32_t nmats,bool ref_counting)` {#classshogun_1_1SGMatrixList_1a677bd751ae7f31695588e5f5e90ba46d}

constructor for setting parameters

#### `public  `[`SGMatrixList`](#classshogun_1_1SGMatrixList_1a2c0165133cccf281a0ddaf1380caf982)`(int32_t nmats,bool ref_counting)` {#classshogun_1_1SGMatrixList_1a2c0165133cccf281a0ddaf1380caf982}

constructor to create a new matrix list in memory

#### `public  `[`SGMatrixList`](#classshogun_1_1SGMatrixList_1abd3b46ee5ada85fa633ae2b8efeee265)`(`[`SGMatrixList`](#classshogun_1_1SGMatrixList)` const & orig)` {#classshogun_1_1SGMatrixList_1abd3b46ee5ada85fa633ae2b8efeee265}

copy constructor

#### `public virtual  `[`~SGMatrixList`](#classshogun_1_1SGMatrixList_1a72b1919347e4633115f3bf5c8ef41e9d)`()` {#classshogun_1_1SGMatrixList_1a72b1919347e4633115f3bf5c8ef41e9d}

destructor

#### `public `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`get_matrix`](#classshogun_1_1SGMatrixList_1a09f87efd18c281bb2d0378d937d34eeb)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index) const` {#classshogun_1_1SGMatrixList_1a09f87efd18c281bb2d0378d937d34eeb}

get a matrix of the list

#### Parameters
* `index` matrix index, index must be less than num_matrices although no check is performed in the method

#### Returns
the matrix at position index of the list

#### `public `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`operator[]`](#classshogun_1_1SGMatrixList_1a8ba2cb22a361b3b9f4c41ec7e8bec4ac)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index) const` {#classshogun_1_1SGMatrixList_1a8ba2cb22a361b3b9f4c41ec7e8bec4ac}

operator overload to get a matrix for read & write access

#### Parameters
* `index` matrix index, index must be less than num_matrices although no check is performed in the method

#### Returns
the matrix at position index of the list

#### `public void `[`set_matrix`](#classshogun_1_1SGMatrixList_1a03d3dc1c4940e6e39a3c27e80cc2742d)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index,const `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > matrix)` {#classshogun_1_1SGMatrixList_1a03d3dc1c4940e6e39a3c27e80cc2742d}

set a matrix of the list

#### Parameters
* `index` matrix index, index must be less than num_matrices although no check is performed in the method 

* `matrix` matrix to set at index

#### `public int32_t `[`ref_count`](#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d)`()` {#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d}

display reference counter

#### Returns
reference count

#### `protected virtual void `[`copy_data`](#classshogun_1_1SGMatrixList_1a6e8ddd37b0b245f7cca418642762e16b)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` {#classshogun_1_1SGMatrixList_1a6e8ddd37b0b245f7cca418642762e16b}

copy data

#### `protected virtual void `[`init_data`](#classshogun_1_1SGMatrixList_1a3b42d3bd68c5200393c1f0809ed1facf)`()` {#classshogun_1_1SGMatrixList_1a3b42d3bd68c5200393c1f0809ed1facf}

initialize empty data

#### `protected virtual void `[`free_data`](#classshogun_1_1SGMatrixList_1ab340ce24b1c9d2b26ab2b46a7a64c346)`()` {#classshogun_1_1SGMatrixList_1ab340ce24b1c9d2b26ab2b46a7a64c346}

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

