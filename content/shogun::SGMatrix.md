---
classname: "shogun::SGMatrix"
type: "class"
parents:
   - SGReferencedData
---

# class `shogun::SGMatrix` {#classshogun_1_1SGMatrix}

```
class shogun::SGMatrix
  : public SGReferencedData
```

shogun matrix

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public T * `[`matrix`](#classshogun_1_1SGMatrix_1ade725ef52c38276385e43df41d4bb119) | matrix
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`num_rows`](#classshogun_1_1SGMatrix_1a8310beaef69971cfb365f1e55c2adc35) | number of rows of matrix
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`num_cols`](#classshogun_1_1SGMatrix_1aacd86c9864c23facdd96d44fe8958e5b) | number of columns of matrix
`public std::shared_ptr< `[`GPUMemoryBase`](#structshogun_1_1GPUMemoryBase)`< T > > `[`gpu_ptr`](#classshogun_1_1SGMatrix_1af119f089106467dfd9eb1ecf6c50d36e) | GPU Matrix structure. Stores pointer to the data on GPU.
`public  `[`SGMatrix`](#classshogun_1_1SGMatrix_1ac28d48186d8bc1971402905f684e02e8)`()` | Default constructor
`public  `[`SGMatrix`](#classshogun_1_1SGMatrix_1a2be56da1613418d45a45ebffc76d1d9f)`(bool ref_counting)` | Constructor for setting reference counting while not creating the matrix in memory (use this for static [SGMatrix](#classshogun_1_1SGMatrix) instances)
`public  `[`SGMatrix`](#classshogun_1_1SGMatrix_1aac48d49445996406acd796cfd5179346)`(T * m,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` nrows,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` ncols,bool ref_counting)` | Constructor for setting params
`public  `[`SGMatrix`](#classshogun_1_1SGMatrix_1a5e17470eb128fd1a905e11b9b83c0881)`(T * m,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` nrows,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` ncols,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` offset)` | Wraps a matrix around an existing memory segment with an offset
`public  `[`SGMatrix`](#classshogun_1_1SGMatrix_1a4e6fe001cbebf6c8528d4a6e8c05aaf1)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` nrows,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` ncols,bool ref_counting)` | Constructor to create new matrix in memory
`public  `[`SGMatrix`](#classshogun_1_1SGMatrix_1af7f279b5f793f685701b7dc242e978b5)`(`[`GPUMemoryBase`](#structshogun_1_1GPUMemoryBase)`< T > * matrix,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` nrows,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` ncols)` | Construct [SGMatrix](#classshogun_1_1SGMatrix) from GPU memory.
`public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` bool `[`on_gpu`](#classshogun_1_1SGMatrix_1a544d60c4a40021806165381020ea7d49)`() const` | Check whether data is stored on GPU
`public  `[`SGMatrix`](#classshogun_1_1SGMatrix_1a1755221047575e24215c63e851f149c0)`(`[`SGVector`](#classshogun_1_1SGVector)`< T > vec)` | Constructor for creating a [SGMatrix](#classshogun_1_1SGMatrix) from a [SGVector](#classshogun_1_1SGVector) with refcounting. We do not copy the data here, just the pointer to data and the ref- count object of the [SGVector](#classshogun_1_1SGVector) (i.e. vec and this share same data and ref-count object).
`public  `[`SGMatrix`](#classshogun_1_1SGMatrix_1a337c83f31e7a00df12b1c6ade331d5d3)`(`[`SGVector`](#classshogun_1_1SGVector)`< T > vec,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` nrows,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` ncols)` | Constructor for creating a [SGMatrix](#classshogun_1_1SGMatrix) from a [SGVector](#classshogun_1_1SGVector) with refcounting. We do not copy the data here, just the pointer to data and the ref- count object of the [SGVector](#classshogun_1_1SGVector) (i.e. vec and this share same data and ref-count object).
`public  `[`SGMatrix`](#classshogun_1_1SGMatrix_1a1f9f0290d7077e7b3d57b0be3a70b098)`(`[`EigenMatrixXt`](#classshogun_1_1SGMatrix_1a17526020a293e2cfc41c7524ef8ebb89)` & mat)` | Wraps a matrix around the data of an Eigen3 matrix
`public  `[`operator EigenMatrixXtMap`](#classshogun_1_1SGMatrix_1aa3d92248b22c8cae83307f97a7ccbde2)`() const` | Wraps an Eigen3 matrix around the data of this matrix
`public `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > & `[`operator=`](#classshogun_1_1SGMatrix_1af87daf8019e89e92278f03abd73eafcb)`(const `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > &)` | Copy assign operator
`public  `[`SGMatrix`](#classshogun_1_1SGMatrix_1a829ed0f1d35bd1552294e8fa476020bd)`(const `[`SGMatrix`](#classshogun_1_1SGMatrix)` & orig)` | Copy constructor
`public virtual  `[`~SGMatrix`](#classshogun_1_1SGMatrix_1aa15f265cf2a289d45acce6d2f6285d60)`()` | [Empty](#structshogun_1_1Empty) destructor
`public inline T * `[`get_column_vector`](#classshogun_1_1SGMatrix_1a266af60a386717077a9d58c2a57cd2a8)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` col) const` | Get a column vector 
`public `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`submatrix`](#classshogun_1_1SGMatrix_1a19d0cd4f730be82f036702f3cec8e587)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` col_start,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` col_end) const` | Given a range of columns (start, end), return a view of the matrix from column start to end excluded. The returned [SGMatrix](#classshogun_1_1SGMatrix) is non-owning! 
`public `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`get_column`](#classshogun_1_1SGMatrix_1a766d9fdb72e643da7076c9fc14073fd8)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` col) const` | Map a column to a [SGVector](#classshogun_1_1SGVector)The returned [SGVector](#classshogun_1_1SGVector) is non-owning! 
`public void `[`set_column`](#classshogun_1_1SGMatrix_1a40cf26eedaf88b3f1c0c6a7c8d471b56)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` col,const `[`SGVector`](#classshogun_1_1SGVector)`< T > vec)` | Copy the content of a vector into a column 
`public `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`get_row_vector`](#classshogun_1_1SGMatrix_1a530176fe9f1bdb2dc67c3fb0c1e98ad4)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` row) const` | Get a row vector
`public `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`get_diagonal_vector`](#classshogun_1_1SGMatrix_1ae8f1cbe5f1f1a541e2fb74f7607e0185)`() const` | Get a main diagonal vector. Matrix is not required to be square.
`public inline const T & `[`operator()`](#classshogun_1_1SGMatrix_1a216ad792113019b9dee240ededb4972a)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i_row,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i_col) const` | Operator overload for matrix read only access 
`public inline const T & `[`operator[]`](#classshogun_1_1SGMatrix_1a1ba5350612032058f4c1e531b6f155a5)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index) const` | Operator overload for matrix read only access 
`public inline T & `[`operator()`](#classshogun_1_1SGMatrix_1ad04272397d8648956c81226c93f4468b)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i_row,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i_col)` | Operator overload for matrix r/w access 
`public inline T & `[`operator[]`](#classshogun_1_1SGMatrix_1abe0aa2d215384e9de7b5bf3163d15d9e)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index)` | Operator overload for matrix r/w access 
`public inline `[`iterator`](#classshogun_1_1SGMatrix_1a88be8e03f7fa96234ccab7620a598fc0)` `[`begin`](#classshogun_1_1SGMatrix_1a979556eb331ec35eb33472a90a160f99)`() noexcept` | Returns an iterator to the first element of the container.
`public inline `[`iterator`](#classshogun_1_1SGMatrix_1a88be8e03f7fa96234ccab7620a598fc0)` `[`end`](#classshogun_1_1SGMatrix_1afc5380afa64b233d0df01a147616974b)`() noexcept` | Returns an iterator to the element following the last element of the container.
`public inline const T & `[`get_element`](#classshogun_1_1SGMatrix_1a69a04d759f41dcd548484489e2f2c54d)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` row,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` col)` | Get element at index
`public inline void `[`set_element`](#classshogun_1_1SGMatrix_1ac6e2f3535c2220708536453dd4de0bc3)`(const T & el,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` row,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` col)` | Set element at index
`public inline `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`get`](#classshogun_1_1SGMatrix_1a566319b53624273511f8b9dd5bd1bb30)`()` | Get the matrix (no copying is done here)
`public inline T * `[`data`](#classshogun_1_1SGMatrix_1a2a1c4b452e7e2523397112c12e53554d)`() const` | The data
`public inline int64_t `[`size`](#classshogun_1_1SGMatrix_1aa326d81dcac346461f3b8528bf0b49de)`() const` | The size
`public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` bool `[`operator==`](#classshogun_1_1SGMatrix_1aad30b5507d745dbbb3fb85a935de3179)`(const `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > & other) const` | Check for pointer identity
`public bool `[`equals`](#classshogun_1_1SGMatrix_1a6a94ae418e110e32022c3987781207ee)`(const `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > & other) const` | Operator overload for element-wise matrix comparison. Note that only numerical data is compared. Works for floating point numbers (along with complex128_t) as well.
`public void `[`set_const`](#classshogun_1_1SGMatrix_1a8bce01a1fc41a734d9b5cf1533fd7a2a)`(T const_elem)` | Set matrix to a constant
`public void `[`zero`](#classshogun_1_1SGMatrix_1a0c4493a5d4723940d60164428f11adc3)`()` | fill matrix with zeros
`public bool `[`is_symmetric`](#classshogun_1_1SGMatrix_1a9ec74ce38de6639353080b12e79a3f28)`() const` | Checks whether the matrix is symmetric or not. The equality check is performed using '==' operators for discrete types (int, char, bool) and using [CMath::fequals](#classshogun_1_1CMath_1a7d233f472ad7fcac6bfd1dfff5c4be32) method for floating types (float, double, long double, std::complex<double>) with default espilon values from std::numeric_limits
`public T `[`max_single`](#classshogun_1_1SGMatrix_1a7be43eb4a301961899c647d81d73df9e)`() const` | #### Returns
`public `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`clone`](#classshogun_1_1SGMatrix_1aa20b7dd504defa15aab4c37507ffbbe2)`() const` | Clone matrix
`public void `[`compute_few_eigenvectors`](#classshogun_1_1SGMatrix_1a2228c78be8e8092a21dc83b8cda045b3)`(double * matrix_,double *& eigenvalues,double *& eigenvectors,int n,int il,int iu)` | Compute few eigenpairs of a symmetric matrix using LAPACK DSYEVR method (Relatively Robust Representations). Has at least O(n^3/3) complexity 
`public void `[`center`](#classshogun_1_1SGMatrix_1a5013a22e5b1f902226b7394353f884ff)`()` | Centers the matrix, i.e. removes column/row mean from columns/rows
`public void `[`remove_column_mean`](#classshogun_1_1SGMatrix_1a6d96748216ba81a76bd664c9a8f728b8)`()` | Remove column mean
`public void `[`display_matrix`](#classshogun_1_1SGMatrix_1a2b6bd83acf89e8e9c7b0a21613620ef4)`(const char * name) const` | Display matrix
`public void `[`load`](#classshogun_1_1SGMatrix_1a5d33ec59a4be25056cca1f3b6691ad00)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` | Load matrix from file
`public void `[`save`](#classshogun_1_1SGMatrix_1aff4d5355fe0d9b68bc8c71cd331c082e)`(`[`CFile`](#classshogun_1_1CFile)` * saver)` | Save matrix to file
`public template<>`  <br/>`bool `[`equals`](#classshogun_1_1SGMatrix_1a449c820e7378a70660f21ba0d9d66e49)`(const `[`SGMatrix](#classshogun_1_1SGMatrix)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > & other) const` | 
`public template<>`  <br/>`bool `[`is_symmetric`](#classshogun_1_1SGMatrix_1aa014e6826f17c8813cc9b4a183af78ca)`() const` | 
`public template<>`  <br/>[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` `[`max_single`](#classshogun_1_1SGMatrix_1a0a53902eef4b431922d80553f18ff62a)`() const` | 
`public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1a9c4fbe4f61d28785b3cdd351813b0f37)`(const bool * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1aab3405fe3cb37295a8d571db063c60ee)`(const char * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1aee926d9888d39690b53163742b5a4479)`(const int8_t * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1ac8e2639b8057c1cc298b256ae39a5eb3)`(const uint8_t * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1a25c2df79f9f96c5d5f20c251dddf72f5)`(const int16_t * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1a9f4a3bbae57066e997166d359c883b55)`(const uint16_t * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1a1e11b137492687a1e4d13643531fde90)`(const int32_t * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1ad2b27db9bc30f53bf7cdaccc0a1e7013)`(const uint32_t * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1ab02713ea1cd2cdf514ab9073e21a6b1c)`(const int64_t * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1a693b936ef55ebc48cd88a5c14e96ae98)`(const uint64_t * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1a24c1432a1f92ee2284d04688592738eb)`(const `[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1a05cd8641d4bdd788f7117d6a7bb7c22a)`(const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1a5c098e54fe2db0bc62b105a7e14719f2)`(const `[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1ad9836dcff7235055c65d6c24f0a7d2a7)`(const `[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` | 
`public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< char > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1a58f38ef0c2b6444e7fa29bf2db1887db)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,char scale)` | 
`public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< int8_t > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1a7e25a38a237d8d8ff57a6605b548b381)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,int8_t scale)` | 
`public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< uint8_t > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1abbd4f9eb1c4d62dfef430e4625aa4963)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,uint8_t scale)` | 
`public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< bool > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1a9bcd23ba4edcc6cc949d97c2812d7f55)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,bool scale)` | 
`public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< int16_t > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1a8f5f603c840edd96107263ae8399311e)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,int16_t scale)` | 
`public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< uint16_t > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1a61bbec163dd6a066721fb7597ea74028)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,uint16_t scale)` | 
`public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< int32_t > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1abb4346eee73c90b0426d830283a70f34)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,int32_t scale)` | 
`public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< uint32_t > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1a74aded9dd9905e8bcf0fac2a902ca10a)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,uint32_t scale)` | 
`public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< int64_t > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1aeeff18718382ba49c7c1308235fd5a50)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,int64_t scale)` | 
`public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< uint64_t > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1a4c09d26bd754c5bd8ed152ce732f09b2)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,uint64_t scale)` | 
`public template<>`  <br/>[`SGMatrix](#classshogun_1_1SGMatrix)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1a0941dd62599ac7af4f69ac89e5ee66f0)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` scale)` | 
`public template<>`  <br/>[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1a42fcb9d0c1a07fd67d3e8601140f9af0)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` scale)` | 
`public template<>`  <br/>[`SGMatrix](#classshogun_1_1SGMatrix)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1aabdbfd43edd248aacc21ec0931a9eb12)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,`[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` scale)` | 
`public template<>`  <br/>[`SGMatrix](#classshogun_1_1SGMatrix)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1aff19869ba1353764084f5456f85b1fa9)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` scale)` | 
`public template<>`  <br/>`void `[`load`](#classshogun_1_1SGMatrix_1a17763c63f0719b10922bc4ed6f392ec4)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` | 
`public template<>`  <br/>`void `[`save`](#classshogun_1_1SGMatrix_1aa61bf55fa90bee7cd7e92beaebe38774)`(`[`CFile`](#classshogun_1_1CFile)` * saver)` | 
`public int32_t `[`ref_count`](#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d)`()` | display reference counter
`protected virtual void `[`copy_data`](#classshogun_1_1SGMatrix_1a6e8ddd37b0b245f7cca418642762e16b)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` | overridden to copy data
`protected virtual void `[`init_data`](#classshogun_1_1SGMatrix_1a3b42d3bd68c5200393c1f0809ed1facf)`()` | overridden to initialize empty data
`protected virtual void `[`free_data`](#classshogun_1_1SGMatrix_1ab340ce24b1c9d2b26ab2b46a7a64c346)`()` | overridden to free data
`protected void `[`copy_refcount`](#classshogun_1_1SGReferencedData_1a253175a13e8af17d4f2a2cfd9e14dd63)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` | copy refcount
`protected int32_t `[`ref`](#classshogun_1_1SGReferencedData_1ab8c24b912ee57d3f2c81ecccd083582a)`()` | increase reference counter
`protected int32_t `[`unref`](#classshogun_1_1SGReferencedData_1ad99bde1a142a1c07a963169123166e01)`()` | decrement reference counter and deallocate object if refcount is zero before or after decrementing it
`typedef `[`iterator`](#classshogun_1_1SGMatrix_1a88be8e03f7fa96234ccab7620a598fc0) | 
`typedef `[`EigenMatrixXt`](#classshogun_1_1SGMatrix_1a17526020a293e2cfc41c7524ef8ebb89) | 
`typedef `[`EigenMatrixXtMap`](#classshogun_1_1SGMatrix_1a0ce4417ac4f98ef2d70956b81d92d081) | 
`typedef `[`Scalar`](#classshogun_1_1SGMatrix_1a47fdf58368a1d22e91e658ab30bfcda8) | The scalar type of the matrix
`typedef `[`container_type`](#classshogun_1_1SGMatrix_1af69bd97ebadfda8ecd5312634e3610e2) | The container type for a given template argument

## Members

#### `public T * `[`matrix`](#classshogun_1_1SGMatrix_1ade725ef52c38276385e43df41d4bb119) {#classshogun_1_1SGMatrix_1ade725ef52c38276385e43df41d4bb119}

matrix

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`num_rows`](#classshogun_1_1SGMatrix_1a8310beaef69971cfb365f1e55c2adc35) {#classshogun_1_1SGMatrix_1a8310beaef69971cfb365f1e55c2adc35}

number of rows of matrix

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`num_cols`](#classshogun_1_1SGMatrix_1aacd86c9864c23facdd96d44fe8958e5b) {#classshogun_1_1SGMatrix_1aacd86c9864c23facdd96d44fe8958e5b}

number of columns of matrix

#### `public std::shared_ptr< `[`GPUMemoryBase`](#structshogun_1_1GPUMemoryBase)`< T > > `[`gpu_ptr`](#classshogun_1_1SGMatrix_1af119f089106467dfd9eb1ecf6c50d36e) {#classshogun_1_1SGMatrix_1af119f089106467dfd9eb1ecf6c50d36e}

GPU Matrix structure. Stores pointer to the data on GPU.

#### `public  `[`SGMatrix`](#classshogun_1_1SGMatrix_1ac28d48186d8bc1971402905f684e02e8)`()` {#classshogun_1_1SGMatrix_1ac28d48186d8bc1971402905f684e02e8}

Default constructor

#### `public  `[`SGMatrix`](#classshogun_1_1SGMatrix_1a2be56da1613418d45a45ebffc76d1d9f)`(bool ref_counting)` {#classshogun_1_1SGMatrix_1a2be56da1613418d45a45ebffc76d1d9f}

Constructor for setting reference counting while not creating the matrix in memory (use this for static [SGMatrix](#classshogun_1_1SGMatrix) instances)

#### `public  `[`SGMatrix`](#classshogun_1_1SGMatrix_1aac48d49445996406acd796cfd5179346)`(T * m,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` nrows,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` ncols,bool ref_counting)` {#classshogun_1_1SGMatrix_1aac48d49445996406acd796cfd5179346}

Constructor for setting params

#### `public  `[`SGMatrix`](#classshogun_1_1SGMatrix_1a5e17470eb128fd1a905e11b9b83c0881)`(T * m,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` nrows,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` ncols,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` offset)` {#classshogun_1_1SGMatrix_1a5e17470eb128fd1a905e11b9b83c0881}

Wraps a matrix around an existing memory segment with an offset

#### `public  `[`SGMatrix`](#classshogun_1_1SGMatrix_1a4e6fe001cbebf6c8528d4a6e8c05aaf1)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` nrows,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` ncols,bool ref_counting)` {#classshogun_1_1SGMatrix_1a4e6fe001cbebf6c8528d4a6e8c05aaf1}

Constructor to create new matrix in memory

#### `public  `[`SGMatrix`](#classshogun_1_1SGMatrix_1af7f279b5f793f685701b7dc242e978b5)`(`[`GPUMemoryBase`](#structshogun_1_1GPUMemoryBase)`< T > * matrix,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` nrows,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` ncols)` {#classshogun_1_1SGMatrix_1af7f279b5f793f685701b7dc242e978b5}

Construct [SGMatrix](#classshogun_1_1SGMatrix) from GPU memory.

#### Parameters
* `vector` [GPUMemoryBase](#structshogun_1_1GPUMemoryBase) pointer 

* `nrows` row number of the matrix 

* `ncols` column number of the matrix 

**See also**: [GPUMemoryBase](#structshogun_1_1GPUMemoryBase)

#### `public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` bool `[`on_gpu`](#classshogun_1_1SGMatrix_1a544d60c4a40021806165381020ea7d49)`() const` {#classshogun_1_1SGMatrix_1a544d60c4a40021806165381020ea7d49}

Check whether data is stored on GPU

#### Returns
true if matrix is on GPU

#### `public  `[`SGMatrix`](#classshogun_1_1SGMatrix_1a1755221047575e24215c63e851f149c0)`(`[`SGVector`](#classshogun_1_1SGVector)`< T > vec)` {#classshogun_1_1SGMatrix_1a1755221047575e24215c63e851f149c0}

Constructor for creating a [SGMatrix](#classshogun_1_1SGMatrix) from a [SGVector](#classshogun_1_1SGVector) with refcounting. We do not copy the data here, just the pointer to data and the ref- count object of the [SGVector](#classshogun_1_1SGVector) (i.e. vec and this share same data and ref-count object).

This constructor assumes that the vector is the column 0 in the matrix.

#### Parameters
* `vec` The [SGVector](#classshogun_1_1SGVector)

#### `public  `[`SGMatrix`](#classshogun_1_1SGMatrix_1a337c83f31e7a00df12b1c6ade331d5d3)`(`[`SGVector`](#classshogun_1_1SGVector)`< T > vec,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` nrows,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` ncols)` {#classshogun_1_1SGMatrix_1a337c83f31e7a00df12b1c6ade331d5d3}

Constructor for creating a [SGMatrix](#classshogun_1_1SGMatrix) from a [SGVector](#classshogun_1_1SGVector) with refcounting. We do not copy the data here, just the pointer to data and the ref- count object of the [SGVector](#classshogun_1_1SGVector) (i.e. vec and this share same data and ref-count object).

The number of elements in the matrix *MUST* be same as the number of elements in the vector

#### Parameters
* `vec` The [SGVector](#classshogun_1_1SGVector)

* `nrows` number of rows in the matrix 

* `ncols` number of columns in the matrix

#### `public  `[`SGMatrix`](#classshogun_1_1SGMatrix_1a1f9f0290d7077e7b3d57b0be3a70b098)`(`[`EigenMatrixXt`](#classshogun_1_1SGMatrix_1a17526020a293e2cfc41c7524ef8ebb89)` & mat)` {#classshogun_1_1SGMatrix_1a1f9f0290d7077e7b3d57b0be3a70b098}

Wraps a matrix around the data of an Eigen3 matrix

#### `public  `[`operator EigenMatrixXtMap`](#classshogun_1_1SGMatrix_1aa3d92248b22c8cae83307f97a7ccbde2)`() const` {#classshogun_1_1SGMatrix_1aa3d92248b22c8cae83307f97a7ccbde2}

Wraps an Eigen3 matrix around the data of this matrix

#### `public `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > & `[`operator=`](#classshogun_1_1SGMatrix_1af87daf8019e89e92278f03abd73eafcb)`(const `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > &)` {#classshogun_1_1SGMatrix_1af87daf8019e89e92278f03abd73eafcb}

Copy assign operator

#### `public  `[`SGMatrix`](#classshogun_1_1SGMatrix_1a829ed0f1d35bd1552294e8fa476020bd)`(const `[`SGMatrix`](#classshogun_1_1SGMatrix)` & orig)` {#classshogun_1_1SGMatrix_1a829ed0f1d35bd1552294e8fa476020bd}

Copy constructor

#### `public virtual  `[`~SGMatrix`](#classshogun_1_1SGMatrix_1aa15f265cf2a289d45acce6d2f6285d60)`()` {#classshogun_1_1SGMatrix_1aa15f265cf2a289d45acce6d2f6285d60}

[Empty](#structshogun_1_1Empty) destructor

#### `public inline T * `[`get_column_vector`](#classshogun_1_1SGMatrix_1a266af60a386717077a9d58c2a57cd2a8)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` col) const` {#classshogun_1_1SGMatrix_1a266af60a386717077a9d58c2a57cd2a8}

Get a column vector 
#### Parameters
* `col` column index 

#### Returns
the column vector for index col

#### `public `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`submatrix`](#classshogun_1_1SGMatrix_1a19d0cd4f730be82f036702f3cec8e587)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` col_start,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` col_end) const` {#classshogun_1_1SGMatrix_1a19d0cd4f730be82f036702f3cec8e587}

Given a range of columns (start, end), return a view of the matrix from column start to end excluded. The returned [SGMatrix](#classshogun_1_1SGMatrix) is non-owning! 

#### Parameters
* `col_start` column index (inclusive) 

* `col_end` column index (excluded) 

#### Returns
the submatrix

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`get_column`](#classshogun_1_1SGMatrix_1a766d9fdb72e643da7076c9fc14073fd8)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` col) const` {#classshogun_1_1SGMatrix_1a766d9fdb72e643da7076c9fc14073fd8}

Map a column to a [SGVector](#classshogun_1_1SGVector)The returned [SGVector](#classshogun_1_1SGVector) is non-owning! 

#### Parameters
* `col` column index 

#### Returns
the column vector for index col

#### `public void `[`set_column`](#classshogun_1_1SGMatrix_1a40cf26eedaf88b3f1c0c6a7c8d471b56)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` col,const `[`SGVector`](#classshogun_1_1SGVector)`< T > vec)` {#classshogun_1_1SGMatrix_1a40cf26eedaf88b3f1c0c6a7c8d471b56}

Copy the content of a vector into a column 
#### Parameters
* `col` column index 

* `vec` vector

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`get_row_vector`](#classshogun_1_1SGMatrix_1a530176fe9f1bdb2dc67c3fb0c1e98ad4)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` row) const` {#classshogun_1_1SGMatrix_1a530176fe9f1bdb2dc67c3fb0c1e98ad4}

Get a row vector

#### Parameters
* `row` row index 

#### Returns
row vector

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`get_diagonal_vector`](#classshogun_1_1SGMatrix_1ae8f1cbe5f1f1a541e2fb74f7607e0185)`() const` {#classshogun_1_1SGMatrix_1ae8f1cbe5f1f1a541e2fb74f7607e0185}

Get a main diagonal vector. Matrix is not required to be square.

#### Returns
main diagonal vector

#### `public inline const T & `[`operator()`](#classshogun_1_1SGMatrix_1a216ad792113019b9dee240ededb4972a)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i_row,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i_col) const` {#classshogun_1_1SGMatrix_1a216ad792113019b9dee240ededb4972a}

Operator overload for matrix read only access 
#### Parameters
* `i_row` 

* `i_col`

#### `public inline const T & `[`operator[]`](#classshogun_1_1SGMatrix_1a1ba5350612032058f4c1e531b6f155a5)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index) const` {#classshogun_1_1SGMatrix_1a1ba5350612032058f4c1e531b6f155a5}

Operator overload for matrix read only access 
#### Parameters
* `index` to access

#### `public inline T & `[`operator()`](#classshogun_1_1SGMatrix_1ad04272397d8648956c81226c93f4468b)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i_row,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` i_col)` {#classshogun_1_1SGMatrix_1ad04272397d8648956c81226c93f4468b}

Operator overload for matrix r/w access 
#### Parameters
* `i_row` 

* `i_col`

#### `public inline T & `[`operator[]`](#classshogun_1_1SGMatrix_1abe0aa2d215384e9de7b5bf3163d15d9e)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index)` {#classshogun_1_1SGMatrix_1abe0aa2d215384e9de7b5bf3163d15d9e}

Operator overload for matrix r/w access 
#### Parameters
* `index` to access

#### `public inline `[`iterator`](#classshogun_1_1SGMatrix_1a88be8e03f7fa96234ccab7620a598fc0)` `[`begin`](#classshogun_1_1SGMatrix_1a979556eb331ec35eb33472a90a160f99)`() noexcept` {#classshogun_1_1SGMatrix_1a979556eb331ec35eb33472a90a160f99}

Returns an iterator to the first element of the container.

#### `public inline `[`iterator`](#classshogun_1_1SGMatrix_1a88be8e03f7fa96234ccab7620a598fc0)` `[`end`](#classshogun_1_1SGMatrix_1afc5380afa64b233d0df01a147616974b)`() noexcept` {#classshogun_1_1SGMatrix_1afc5380afa64b233d0df01a147616974b}

Returns an iterator to the element following the last element of the container.

#### `public inline const T & `[`get_element`](#classshogun_1_1SGMatrix_1a69a04d759f41dcd548484489e2f2c54d)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` row,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` col)` {#classshogun_1_1SGMatrix_1a69a04d759f41dcd548484489e2f2c54d}

Get element at index

#### Parameters
* `row` row index 

* `col` column index 

#### Returns
element at index

#### `public inline void `[`set_element`](#classshogun_1_1SGMatrix_1ac6e2f3535c2220708536453dd4de0bc3)`(const T & el,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` row,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` col)` {#classshogun_1_1SGMatrix_1ac6e2f3535c2220708536453dd4de0bc3}

Set element at index

#### Parameters
* `el` element to set 

* `row` row index 

* `col` column index

#### `public inline `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`get`](#classshogun_1_1SGMatrix_1a566319b53624273511f8b9dd5bd1bb30)`()` {#classshogun_1_1SGMatrix_1a566319b53624273511f8b9dd5bd1bb30}

Get the matrix (no copying is done here)

#### Returns
the refcount increased matrix

#### `public inline T * `[`data`](#classshogun_1_1SGMatrix_1a2a1c4b452e7e2523397112c12e53554d)`() const` {#classshogun_1_1SGMatrix_1a2a1c4b452e7e2523397112c12e53554d}

The data

#### `public inline int64_t `[`size`](#classshogun_1_1SGMatrix_1aa326d81dcac346461f3b8528bf0b49de)`() const` {#classshogun_1_1SGMatrix_1aa326d81dcac346461f3b8528bf0b49de}

The size

#### `public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` bool `[`operator==`](#classshogun_1_1SGMatrix_1aad30b5507d745dbbb3fb85a935de3179)`(const `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > & other) const` {#classshogun_1_1SGMatrix_1aad30b5507d745dbbb3fb85a935de3179}

Check for pointer identity

#### `public bool `[`equals`](#classshogun_1_1SGMatrix_1a6a94ae418e110e32022c3987781207ee)`(const `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > & other) const` {#classshogun_1_1SGMatrix_1a6a94ae418e110e32022c3987781207ee}

Operator overload for element-wise matrix comparison. Note that only numerical data is compared. Works for floating point numbers (along with complex128_t) as well.

#### Parameters
* `other` matrix to compare with 

#### Returns
true iff all elements are equal

#### `public void `[`set_const`](#classshogun_1_1SGMatrix_1a8bce01a1fc41a734d9b5cf1533fd7a2a)`(T const_elem)` {#classshogun_1_1SGMatrix_1a8bce01a1fc41a734d9b5cf1533fd7a2a}

Set matrix to a constant

#### `public void `[`zero`](#classshogun_1_1SGMatrix_1a0c4493a5d4723940d60164428f11adc3)`()` {#classshogun_1_1SGMatrix_1a0c4493a5d4723940d60164428f11adc3}

fill matrix with zeros

#### `public bool `[`is_symmetric`](#classshogun_1_1SGMatrix_1a9ec74ce38de6639353080b12e79a3f28)`() const` {#classshogun_1_1SGMatrix_1a9ec74ce38de6639353080b12e79a3f28}

Checks whether the matrix is symmetric or not. The equality check is performed using '==' operators for discrete types (int, char, bool) and using [CMath::fequals](#classshogun_1_1CMath_1a7d233f472ad7fcac6bfd1dfff5c4be32) method for floating types (float, double, long double, std::complex<double>) with default espilon values from std::numeric_limits

#### Returns
whether the matrix is symmetric

#### `public T `[`max_single`](#classshogun_1_1SGMatrix_1a7be43eb4a301961899c647d81d73df9e)`() const` {#classshogun_1_1SGMatrix_1a7be43eb4a301961899c647d81d73df9e}

#### Returns
the maximum single element of the matrix

#### `public `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`clone`](#classshogun_1_1SGMatrix_1aa20b7dd504defa15aab4c37507ffbbe2)`() const` {#classshogun_1_1SGMatrix_1aa20b7dd504defa15aab4c37507ffbbe2}

Clone matrix

#### `public void `[`compute_few_eigenvectors`](#classshogun_1_1SGMatrix_1a2228c78be8e8092a21dc83b8cda045b3)`(double * matrix_,double *& eigenvalues,double *& eigenvectors,int n,int il,int iu)` {#classshogun_1_1SGMatrix_1a2228c78be8e8092a21dc83b8cda045b3}

Compute few eigenpairs of a symmetric matrix using LAPACK DSYEVR method (Relatively Robust Representations). Has at least O(n^3/3) complexity 
#### Parameters
* `matrix_` symmetric matrix 

* `eigenvalues` contains iu-il+1 eigenvalues in ascending order (to be free'd) 

* `eigenvectors` contains iu-il+1 orthonormal eigenvectors of given matrix column-wise (to be free'd) 

* `n` dimension of matrix 

* `il` low index of requested eigenpairs (1<=il<=n) 

* `iu` high index of requested eigenpairs (1<=il<=iu<=n)

#### `public void `[`center`](#classshogun_1_1SGMatrix_1a5013a22e5b1f902226b7394353f884ff)`()` {#classshogun_1_1SGMatrix_1a5013a22e5b1f902226b7394353f884ff}

Centers the matrix, i.e. removes column/row mean from columns/rows

#### `public void `[`remove_column_mean`](#classshogun_1_1SGMatrix_1a6d96748216ba81a76bd664c9a8f728b8)`()` {#classshogun_1_1SGMatrix_1a6d96748216ba81a76bd664c9a8f728b8}

Remove column mean

#### `public void `[`display_matrix`](#classshogun_1_1SGMatrix_1a2b6bd83acf89e8e9c7b0a21613620ef4)`(const char * name) const` {#classshogun_1_1SGMatrix_1a2b6bd83acf89e8e9c7b0a21613620ef4}

Display matrix

#### `public void `[`load`](#classshogun_1_1SGMatrix_1a5d33ec59a4be25056cca1f3b6691ad00)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` {#classshogun_1_1SGMatrix_1a5d33ec59a4be25056cca1f3b6691ad00}

Load matrix from file

#### Parameters
* `loader` File object via which to load data

#### `public void `[`save`](#classshogun_1_1SGMatrix_1aff4d5355fe0d9b68bc8c71cd331c082e)`(`[`CFile`](#classshogun_1_1CFile)` * saver)` {#classshogun_1_1SGMatrix_1aff4d5355fe0d9b68bc8c71cd331c082e}

Save matrix to file

#### Parameters
* `saver` File object via which to save data

#### `public template<>`  <br/>`bool `[`equals`](#classshogun_1_1SGMatrix_1a449c820e7378a70660f21ba0d9d66e49)`(const `[`SGMatrix](#classshogun_1_1SGMatrix)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > & other) const` {#classshogun_1_1SGMatrix_1a449c820e7378a70660f21ba0d9d66e49}

#### `public template<>`  <br/>`bool `[`is_symmetric`](#classshogun_1_1SGMatrix_1aa014e6826f17c8813cc9b4a183af78ca)`() const` {#classshogun_1_1SGMatrix_1aa014e6826f17c8813cc9b4a183af78ca}

#### `public template<>`  <br/>[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` `[`max_single`](#classshogun_1_1SGMatrix_1a0a53902eef4b431922d80553f18ff62a)`() const` {#classshogun_1_1SGMatrix_1a0a53902eef4b431922d80553f18ff62a}

#### `public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1a9c4fbe4f61d28785b3cdd351813b0f37)`(const bool * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` {#classshogun_1_1SGMatrix_1a9c4fbe4f61d28785b3cdd351813b0f37}

#### `public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1aab3405fe3cb37295a8d571db063c60ee)`(const char * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` {#classshogun_1_1SGMatrix_1aab3405fe3cb37295a8d571db063c60ee}

#### `public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1aee926d9888d39690b53163742b5a4479)`(const int8_t * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` {#classshogun_1_1SGMatrix_1aee926d9888d39690b53163742b5a4479}

#### `public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1ac8e2639b8057c1cc298b256ae39a5eb3)`(const uint8_t * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` {#classshogun_1_1SGMatrix_1ac8e2639b8057c1cc298b256ae39a5eb3}

#### `public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1a25c2df79f9f96c5d5f20c251dddf72f5)`(const int16_t * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` {#classshogun_1_1SGMatrix_1a25c2df79f9f96c5d5f20c251dddf72f5}

#### `public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1a9f4a3bbae57066e997166d359c883b55)`(const uint16_t * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` {#classshogun_1_1SGMatrix_1a9f4a3bbae57066e997166d359c883b55}

#### `public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1a1e11b137492687a1e4d13643531fde90)`(const int32_t * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` {#classshogun_1_1SGMatrix_1a1e11b137492687a1e4d13643531fde90}

#### `public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1ad2b27db9bc30f53bf7cdaccc0a1e7013)`(const uint32_t * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` {#classshogun_1_1SGMatrix_1ad2b27db9bc30f53bf7cdaccc0a1e7013}

#### `public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1ab02713ea1cd2cdf514ab9073e21a6b1c)`(const int64_t * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` {#classshogun_1_1SGMatrix_1ab02713ea1cd2cdf514ab9073e21a6b1c}

#### `public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1a693b936ef55ebc48cd88a5c14e96ae98)`(const uint64_t * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` {#classshogun_1_1SGMatrix_1a693b936ef55ebc48cd88a5c14e96ae98}

#### `public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1a24c1432a1f92ee2284d04688592738eb)`(const `[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` {#classshogun_1_1SGMatrix_1a24c1432a1f92ee2284d04688592738eb}

#### `public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1a05cd8641d4bdd788f7117d6a7bb7c22a)`(const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` {#classshogun_1_1SGMatrix_1a05cd8641d4bdd788f7117d6a7bb7c22a}

#### `public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1a5c098e54fe2db0bc62b105a7e14719f2)`(const `[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` {#classshogun_1_1SGMatrix_1a5c098e54fe2db0bc62b105a7e14719f2}

#### `public template<>`  <br/>`void `[`display_matrix`](#classshogun_1_1SGMatrix_1ad9836dcff7235055c65d6c24f0a7d2a7)`(const `[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` * matrix,int32_t rows,int32_t cols,const char * name,const char * prefix)` {#classshogun_1_1SGMatrix_1ad9836dcff7235055c65d6c24f0a7d2a7}

#### `public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< char > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1a58f38ef0c2b6444e7fa29bf2db1887db)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,char scale)` {#classshogun_1_1SGMatrix_1a58f38ef0c2b6444e7fa29bf2db1887db}

#### `public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< int8_t > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1a7e25a38a237d8d8ff57a6605b548b381)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,int8_t scale)` {#classshogun_1_1SGMatrix_1a7e25a38a237d8d8ff57a6605b548b381}

#### `public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< uint8_t > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1abbd4f9eb1c4d62dfef430e4625aa4963)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,uint8_t scale)` {#classshogun_1_1SGMatrix_1abbd4f9eb1c4d62dfef430e4625aa4963}

#### `public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< bool > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1a9bcd23ba4edcc6cc949d97c2812d7f55)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,bool scale)` {#classshogun_1_1SGMatrix_1a9bcd23ba4edcc6cc949d97c2812d7f55}

#### `public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< int16_t > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1a8f5f603c840edd96107263ae8399311e)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,int16_t scale)` {#classshogun_1_1SGMatrix_1a8f5f603c840edd96107263ae8399311e}

#### `public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< uint16_t > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1a61bbec163dd6a066721fb7597ea74028)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,uint16_t scale)` {#classshogun_1_1SGMatrix_1a61bbec163dd6a066721fb7597ea74028}

#### `public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< int32_t > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1abb4346eee73c90b0426d830283a70f34)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,int32_t scale)` {#classshogun_1_1SGMatrix_1abb4346eee73c90b0426d830283a70f34}

#### `public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< uint32_t > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1a74aded9dd9905e8bcf0fac2a902ca10a)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,uint32_t scale)` {#classshogun_1_1SGMatrix_1a74aded9dd9905e8bcf0fac2a902ca10a}

#### `public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< int64_t > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1aeeff18718382ba49c7c1308235fd5a50)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,int64_t scale)` {#classshogun_1_1SGMatrix_1aeeff18718382ba49c7c1308235fd5a50}

#### `public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< uint64_t > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1a4c09d26bd754c5bd8ed152ce732f09b2)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,uint64_t scale)` {#classshogun_1_1SGMatrix_1a4c09d26bd754c5bd8ed152ce732f09b2}

#### `public template<>`  <br/>[`SGMatrix](#classshogun_1_1SGMatrix)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1a0941dd62599ac7af4f69ac89e5ee66f0)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` scale)` {#classshogun_1_1SGMatrix_1a0941dd62599ac7af4f69ac89e5ee66f0}

#### `public template<>`  <br/>[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1a42fcb9d0c1a07fd67d3e8601140f9af0)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` scale)` {#classshogun_1_1SGMatrix_1a42fcb9d0c1a07fd67d3e8601140f9af0}

#### `public template<>`  <br/>[`SGMatrix](#classshogun_1_1SGMatrix)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1aabdbfd43edd248aacc21ec0931a9eb12)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,`[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` scale)` {#classshogun_1_1SGMatrix_1aabdbfd43edd248aacc21ec0931a9eb12}

#### `public template<>`  <br/>[`SGMatrix](#classshogun_1_1SGMatrix)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > `[`create_identity_matrix`](#classshogun_1_1SGMatrix_1aff19869ba1353764084f5456f85b1fa9)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` size,`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` scale)` {#classshogun_1_1SGMatrix_1aff19869ba1353764084f5456f85b1fa9}

#### `public template<>`  <br/>`void `[`load`](#classshogun_1_1SGMatrix_1a17763c63f0719b10922bc4ed6f392ec4)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` {#classshogun_1_1SGMatrix_1a17763c63f0719b10922bc4ed6f392ec4}

#### `public template<>`  <br/>`void `[`save`](#classshogun_1_1SGMatrix_1aa61bf55fa90bee7cd7e92beaebe38774)`(`[`CFile`](#classshogun_1_1CFile)` * saver)` {#classshogun_1_1SGMatrix_1aa61bf55fa90bee7cd7e92beaebe38774}

#### `public int32_t `[`ref_count`](#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d)`()` {#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d}

display reference counter

#### Returns
reference count

#### `protected virtual void `[`copy_data`](#classshogun_1_1SGMatrix_1a6e8ddd37b0b245f7cca418642762e16b)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` {#classshogun_1_1SGMatrix_1a6e8ddd37b0b245f7cca418642762e16b}

overridden to copy data

#### `protected virtual void `[`init_data`](#classshogun_1_1SGMatrix_1a3b42d3bd68c5200393c1f0809ed1facf)`()` {#classshogun_1_1SGMatrix_1a3b42d3bd68c5200393c1f0809ed1facf}

overridden to initialize empty data

#### `protected virtual void `[`free_data`](#classshogun_1_1SGMatrix_1ab340ce24b1c9d2b26ab2b46a7a64c346)`()` {#classshogun_1_1SGMatrix_1ab340ce24b1c9d2b26ab2b46a7a64c346}

overridden to free data

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

#### `typedef `[`iterator`](#classshogun_1_1SGMatrix_1a88be8e03f7fa96234ccab7620a598fc0) {#classshogun_1_1SGMatrix_1a88be8e03f7fa96234ccab7620a598fc0}

#### `typedef `[`EigenMatrixXt`](#classshogun_1_1SGMatrix_1a17526020a293e2cfc41c7524ef8ebb89) {#classshogun_1_1SGMatrix_1a17526020a293e2cfc41c7524ef8ebb89}

#### `typedef `[`EigenMatrixXtMap`](#classshogun_1_1SGMatrix_1a0ce4417ac4f98ef2d70956b81d92d081) {#classshogun_1_1SGMatrix_1a0ce4417ac4f98ef2d70956b81d92d081}

#### `typedef `[`Scalar`](#classshogun_1_1SGMatrix_1a47fdf58368a1d22e91e658ab30bfcda8) {#classshogun_1_1SGMatrix_1a47fdf58368a1d22e91e658ab30bfcda8}

The scalar type of the matrix

#### `typedef `[`container_type`](#classshogun_1_1SGMatrix_1af69bd97ebadfda8ecd5312634e3610e2) {#classshogun_1_1SGMatrix_1af69bd97ebadfda8ecd5312634e3610e2}

The container type for a given template argument

