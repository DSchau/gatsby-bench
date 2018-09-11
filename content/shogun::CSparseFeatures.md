---
classname: "shogun::CSparseFeatures"
type: "class"
parents:
   - CDotFeatures
---

# class `shogun::CSparseFeatures` {#classshogun_1_1CSparseFeatures}

```
class shogun::CSparseFeatures
  : public CDotFeatures
```

Template class SparseFeatures implements sparse matrices.

Features are an array of [SGSparseVector](#classshogun_1_1SGSparseVector). Within each vector feat_index are sorted (increasing).

Sparse feature vectors can be accessed via [get_sparse_feature_vector()](#classshogun_1_1CSparseFeatures_1aef6eae81a9bc8c951de5493fe53adcdf) and should be freed (this operation is a NOP in most cases) via [free_sparse_feature_vector()](#classshogun_1_1CSparseFeatures_1abb38feee4815fd4b0ca1a5d581003bb7).

As this is a template class it can directly be used for different data types like sparse matrices of real valued, integer, byte etc type.

(Partly) subset access is supported for this feature type. Simple use the (inherited) [add_subset()](#classshogun_1_1CFeatures_1acb58d8008e2ef9bb83e6b5fc5fb42f71), [remove_subset()](#classshogun_1_1CFeatures_1a5c8a113b96b3d3a2d565ed9fffeed172) functions. If done, all calls that work with features are translated to the subset. See comments to find out whether it is supported for that method. See also [CFeatures](#classshogun_1_1CFeatures) class documentation

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public `[`SGIO`](#classshogun_1_1SGIO)` * `[`io`](#classshogun_1_1CSGObject_1ab3ff22f724961ace985100941ba0364d) | io
`public `[`Parallel`](#classshogun_1_1Parallel)` * `[`parallel`](#classshogun_1_1CSGObject_1a1401044636b5c2353226b974526302e9) | parallel
`public `[`Version`](#classshogun_1_1Version)` * `[`version`](#classshogun_1_1CSGObject_1afc25f30ab1a6d04798c360a2ce70b87d) | version
`public `[`Parameter`](#classshogun_1_1Parameter)` * `[`m_parameters`](#classshogun_1_1CSGObject_1a70e59038292e669701bad2af7715aa1e) | parameters
`public `[`Parameter`](#classshogun_1_1Parameter)` * `[`m_model_selection_parameters`](#classshogun_1_1CSGObject_1a113f5ae82840ac3f354f94456c10f59b) | model selection parameters
`public `[`Parameter`](#classshogun_1_1Parameter)` * `[`m_gradient_parameters`](#classshogun_1_1CSGObject_1ac3f51364b93830b9c9d991cb2d5801f4) | parameters wrt which we can compute gradients
`public uint32_t `[`m_hash`](#classshogun_1_1CSGObject_1a170f14be9561242f924939c56b372a41) | Hash of parameter values
`public  `[`CSparseFeatures`](#classshogun_1_1CSparseFeatures_1afb99d45e29457cbe4b2551bb5b9b996c)`(int32_t size)` | constructor
`public  `[`CSparseFeatures`](#classshogun_1_1CSparseFeatures_1a6add6550063e649c9daada7853361a94)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< ST > sparse)` | convenience constructor that creates sparse features from sparse features
`public  `[`CSparseFeatures`](#classshogun_1_1CSparseFeatures_1a9d81cc71f02cbf7f57d5bc9752f7ddff)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< ST > dense)` | convenience constructor that creates sparse features from dense features
`public  `[`CSparseFeatures`](#classshogun_1_1CSparseFeatures_1a337640d02feb5d1894d125977ccc53bb)`(const `[`CSparseFeatures`](#classshogun_1_1CSparseFeatures)` & orig)` | copy constructor
`public  `[`CSparseFeatures`](#classshogun_1_1CSparseFeatures_1a9aa5e9d7914378ff802909a6cb4ea4df)`(`[`CDenseFeatures`](#classshogun_1_1CDenseFeatures)`< ST > * dense)` | copy constructor from DenseFeatures
`public  `[`CSparseFeatures`](#classshogun_1_1CSparseFeatures_1a0a4554f19043005bd2530c8c8414a1be)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` | constructor loading features from file
`public virtual  `[`~CSparseFeatures`](#classshogun_1_1CSparseFeatures_1a9a588e07feac3260d3e9ea05c86e6d0f)`()` | default destructor
`public void `[`free_sparse_feature_matrix`](#classshogun_1_1CSparseFeatures_1a7d1791c8d5684f8508e478eaa95a0a7c)`()` | free sparse feature matrix
`public void `[`free_sparse_features`](#classshogun_1_1CSparseFeatures_1a51881f6fcd5a266ebaef20a5e382199c)`()` | free sparse feature matrix and cache
`public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`duplicate`](#classshogun_1_1CSparseFeatures_1a451c5fd7954842d7a19f1b0faa710e0c)`() const` | duplicate feature object
`public ST `[`get_feature`](#classshogun_1_1CSparseFeatures_1a457ca9c3e75d88b33364c4dff73db372)`(int32_t num,int32_t index)` | get a single feature
`public `[`SGVector`](#classshogun_1_1SGVector)`< ST > `[`get_full_feature_vector`](#classshogun_1_1CSparseFeatures_1ab1fe225ab22e1a370aa7015260a95370)`(int32_t num)` | get the fully expanded dense feature vector num
`public virtual int32_t `[`get_nnz_features_for_vector`](#classshogun_1_1CSparseFeatures_1ab7b680a2262f123880faae88061830cb)`(int32_t num)` | get number of non-zero features in vector
`public `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< ST > `[`get_sparse_feature_vector`](#classshogun_1_1CSparseFeatures_1aef6eae81a9bc8c951de5493fe53adcdf)`(int32_t num)` | get sparse feature vector for sample num from the matrix as it is if matrix is initialized, else return preprocessed compute_feature_vector
`public ST `[`dense_dot`](#classshogun_1_1CSparseFeatures_1a2d0e500f551684261674d709859e7fb1)`(ST alpha,int32_t num,ST * vec,int32_t dim,ST b)` | compute the dot product between dense weights and a sparse feature vector alpha * sparse^T * w + b
`public virtual void `[`add_to_dense_vec`](#classshogun_1_1CSparseFeatures_1a05ee86f75779fe7b29638f131d843868)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` alpha,int32_t num,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * vec,int32_t dim,bool abs_val)` | add a sparse feature vector onto a dense one dense+=alpha*sparse
`public void `[`free_sparse_feature_vector`](#classshogun_1_1CSparseFeatures_1abb38feee4815fd4b0ca1a5d581003bb7)`(int32_t num)` | free sparse feature vector
`public `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< ST > * `[`get_sparse_feature_matrix`](#classshogun_1_1CSparseFeatures_1a2941f8e93a187097b8b2dd90955049eb)`(int32_t & num_feat,int32_t & num_vec)` | get the pointer to the sparse feature matrix num_feat,num_vectors are returned by reference
`public `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< ST > `[`get_sparse_feature_matrix`](#classshogun_1_1CSparseFeatures_1a1f76335e82bcc10155dddc9ba53fe8c9)`()` | get the sparse feature matrix
`public `[`CSparseFeatures`](#classshogun_1_1CSparseFeatures)`< ST > * `[`get_transposed`](#classshogun_1_1CSparseFeatures_1a6fb4c681fc001c28e452a3254f410fd7)`()` | get a transposed copy of the features
`public `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< ST > * `[`get_transposed`](#classshogun_1_1CSparseFeatures_1a32ba325366b4457400edc86f6137b7ab)`(int32_t & num_feat,int32_t & num_vec)` | compute and return the transpose of the sparse feature matrix which will be prepocessed. num_feat, num_vectors are returned by reference caller has to clean up
`public void `[`set_sparse_feature_matrix`](#classshogun_1_1CSparseFeatures_1a9925b7247d1ec2f61d3eb0458b1c7f83)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< ST > sm)` | set sparse feature matrix
`public `[`SGMatrix`](#classshogun_1_1SGMatrix)`< ST > `[`get_full_feature_matrix`](#classshogun_1_1CSparseFeatures_1a9c3af84f8076ce6bccc8c9b20bc23be3)`()` | gets a copy of a full feature matrix
`public virtual void `[`set_full_feature_matrix`](#classshogun_1_1CSparseFeatures_1a70f397556c4ace1ac9b569c130f3c29e)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< ST > full)` | creates a sparse feature matrix from a full dense feature matrix necessary to set feature_matrix, num_features and num_vectors where num_features is the column offset, and columns are linear in memory see above for definition of sparse_feature_matrix
`public virtual int32_t `[`get_num_vectors`](#classshogun_1_1CSparseFeatures_1a25a45bd4c25c9d7d72826dd195a7c696)`() const` | get number of feature vectors, possibly of subset
`public int32_t `[`get_num_features`](#classshogun_1_1CSparseFeatures_1ac8a43465974b1625cd461d1e19d290ff)`() const` | get number of features
`public int32_t `[`set_num_features`](#classshogun_1_1CSparseFeatures_1ac09e081001f3f6c602c5e1b4642ed3f3)`(int32_t num)` | set number of features
`public virtual `[`EFeatureClass`](#namespaceshogun_1a9e2a4d8b86b9e061779c3fdbcda57c3b)` `[`get_feature_class`](#classshogun_1_1CSparseFeatures_1ae83dd54e69a4e8f1c7a571545fa1c8c1)`() const` | get feature class
`public virtual `[`EFeatureType`](#namespaceshogun_1a064eec90e91f56435546d77f38c0b618)` `[`get_feature_type`](#classshogun_1_1CSparseFeatures_1a48ec5bbd5022e2ffa67a31613fd257f9)`() const` | get feature type
`public void `[`free_feature_vector`](#classshogun_1_1CSparseFeatures_1a1f7aaef030fc753b2622779af19ca3ae)`(int32_t num)` | free feature vector
`public int64_t `[`get_num_nonzero_entries`](#classshogun_1_1CSparseFeatures_1af10874a583f1aecd35e0374535a8411d)`()` | get number of non-zero entries in sparse feature matrix
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`compute_squared`](#classshogun_1_1CSparseFeatures_1af16c85d52cd4baece591def958c2de16)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * sq)` | compute a^2 on all feature vectors
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_squared_norm`](#classshogun_1_1CSparseFeatures_1a36853f4e7ff0735cc39befea4222f30c)`(`[`CSparseFeatures](#classshogun_1_1CSparseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * lhs,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * sq_lhs,int32_t idx_a,`[`CSparseFeatures](#classshogun_1_1CSparseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * rhs,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * sq_rhs,int32_t idx_b)` | compute (a-b)^2 (== a^2+b^2-2ab) usually called by kernels'/distances' compute functions works on two feature vectors, although it is a member of a single feature: can either be called by lhs or rhs.
`public virtual void `[`load`](#classshogun_1_1CSparseFeatures_1a5d33ec59a4be25056cca1f3b6691ad00)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` | load features from file
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`load_with_labels`](#classshogun_1_1CSparseFeatures_1a280b249dd4ccf9556944c8a91c8c00e1)`(`[`CLibSVMFile`](#classshogun_1_1CLibSVMFile)` * loader)` | load features from file
`public virtual void `[`save`](#classshogun_1_1CSparseFeatures_1a2ec11d78c7f60dfbc77bc2f56d211033)`(`[`CFile`](#classshogun_1_1CFile)` * writer)` | save features to file
`public void `[`save_with_labels`](#classshogun_1_1CSparseFeatures_1a4f9660cee348dfcedd859fd1170c5750)`(`[`CLibSVMFile`](#classshogun_1_1CLibSVMFile)` * writer,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > labels)` | save features to file
`public void `[`sort_features`](#classshogun_1_1CSparseFeatures_1aa0010ddb91f3132cf24e5266551b7215)`()` | ensure that features occur in ascending order, only call when no preprocessors are attached
`public virtual int32_t `[`get_dim_feature_space`](#classshogun_1_1CSparseFeatures_1a13fbd248e2925b0a24f49889c542e74c)`() const` | obtain the dimensionality of the feature space
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`dot`](#classshogun_1_1CSparseFeatures_1a1f97967a070acb388927a27a449b9bae)`(int32_t vec_idx1,`[`CDotFeatures`](#classshogun_1_1CDotFeatures)` * df,int32_t vec_idx2)` | compute dot product between vector1 and vector2, appointed by their indices
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`dense_dot`](#classshogun_1_1CSparseFeatures_1a403b986eccb3fb295a77f2e699f02105)`(int32_t vec_idx1,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * vec2,int32_t vec2_len)` | compute dot product between vector1 and a dense vector
`public virtual void * `[`get_feature_iterator`](#classshogun_1_1CSparseFeatures_1a05368260e526dd61037bf36049f7a458)`(int32_t vector_index)` | iterate over the non-zero features
`public virtual bool `[`get_next_feature`](#classshogun_1_1CSparseFeatures_1a55dc88fdfa05cbcb8ffee8d191481123)`(int32_t & index,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` & value,void * iterator)` | iterate over the non-zero features
`public virtual void `[`free_feature_iterator`](#classshogun_1_1CSparseFeatures_1a3e93f36c6ec2624036a0f8d961c15d9f)`(void * iterator)` | clean up iterator call this function with the iterator returned by get_first_feature
`public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`copy_subset`](#classshogun_1_1CSparseFeatures_1adf4a1baaff0c06456ceca3b217c46338)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | Creates a new [CFeatures](#classshogun_1_1CFeatures) instance containing copies of the elements which are specified by the provided indices.
`public inline virtual const char * `[`get_name`](#classshogun_1_1CSparseFeatures_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` | #### Returns
`public template<>`  <br/>` `[`CSparseFeatures`](#classshogun_1_1CSparseFeatures_1ae1057a99dcf60605ef972ffa8c1ac389)`(`[`CDenseFeatures](#classshogun_1_1CDenseFeatures)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > * dense)` | 
`public template<>`  <br/>`virtual void `[`add_to_dense_vec`](#classshogun_1_1CSparseFeatures_1aad4da1ab509c3a70a9c74d1f374d6195)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` alpha,int32_t vec_idx1,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * vec2,int32_t vec2_len,bool abs_val)` | add vector 1 multiplied with alpha to dense vector2
`public template<>`  <br/>[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`compute_squared`](#classshogun_1_1CSparseFeatures_1a91df3d94e7f3aceaa561287d3c323a19)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * sq)` | 
`public template<>`  <br/>`virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`dot`](#classshogun_1_1CSparseFeatures_1a58a7125f3ee6d08bec5bfef985a0eac1)`(int32_t vec_idx1,`[`CDotFeatures`](#classshogun_1_1CDotFeatures)` * df,int32_t vec_idx2)` | compute dot product between vector1 and vector2, appointed by their indices
`public template<>`  <br/>`virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`dense_dot`](#classshogun_1_1CSparseFeatures_1aa8f01741b4e4abf9428a3441d5e01572)`(int32_t vec_idx1,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * vec2,int32_t vec2_len)` | compute dot product between vector1 and a dense vector
`public template<>`  <br/>`virtual bool `[`get_next_feature`](#classshogun_1_1CSparseFeatures_1aaa606c5e0c9dae930acdab018ee1f462)`(int32_t & index,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` & value,void * iterator)` | iterate over the non-zero features
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`dense_dot_sgvec`](#classshogun_1_1CDotFeatures_1ab7d8fd6dbd49dd8bf718c52f48739270)`(int32_t vec_idx1,const `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > vec2)` | compute dot product between vector1 and a dense vector
`public virtual void `[`dense_dot_range`](#classshogun_1_1CDotFeatures_1aa42ca5ff67f737f667b744f3aaaa2c09)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * output,int32_t start,int32_t stop,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * alphas,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * vec,int32_t dim,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` b)` | Compute the dot product for a range of vectors. This function makes use of dense_dot alphas[i] * sparse[i]^T * w + b
`public virtual void `[`dense_dot_range_subset`](#classshogun_1_1CDotFeatures_1ad60b812407a0f68110ce5b2e968b05da)`(int32_t * sub_index,int32_t num,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * output,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * alphas,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * vec,int32_t dim,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` b)` | Compute the dot product for a subset of vectors. This function makes use of dense_dot alphas[i] * sparse[i]^T * w + b
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_combined_feature_weight`](#classshogun_1_1CDotFeatures_1aded91b11393d1add2d2bc112bd3eb5f7)`()` | get combined feature weight
`public inline void `[`set_combined_feature_weight`](#classshogun_1_1CDotFeatures_1acdef16d18b5739e57eb089c0acbb843b)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` nw)` | set combined kernel weight
`public `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_computed_dot_feature_matrix`](#classshogun_1_1CDotFeatures_1a5c737a3c973bf08b30f9e43c56a6efa4)`()` | compute the feature matrix in feature space
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_computed_dot_feature_vector`](#classshogun_1_1CDotFeatures_1a28c4e362056c07a3a47bfcd5aa8f90f9)`(int32_t num)` | compute the feature vector in feature space
`public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_mean`](#classshogun_1_1CDotFeatures_1a92d96916c774173e59d8a960648ebd78)`()` | get mean
`public virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_cov`](#classshogun_1_1CDotFeatures_1a5796ce37031e0fd989686840e26b276e)`(bool copy_data_for_speed)` | get covariance
`public inline virtual `[`Range`](#classshogun_1_1Range)`< int32_t > `[`index_iterator`](#classshogun_1_1CFeatures_1a71bb6f4167a24d55e8e12fca77baabcd)`() const` | returns an iterator of indices from 0 to [CFeatures::get_num_vectors](#classshogun_1_1CFeatures_1a91f8bf82dad4bb05accdc606d85a0da3)
`public virtual void `[`add_preprocessor`](#classshogun_1_1CFeatures_1a53d5b6b17d8e4b44117d404b119faca6)`(`[`CPreprocessor`](#classshogun_1_1CPreprocessor)` * p)` | add preprocessor
`public virtual void `[`del_preprocessor`](#classshogun_1_1CFeatures_1af2ad4fb4c64ea892dc73a288f1be27a2)`(int32_t num)` | delete preprocessor from list
`public `[`CPreprocessor`](#classshogun_1_1CPreprocessor)` * `[`get_preprocessor`](#classshogun_1_1CFeatures_1a16a2c185a1d7059892ef6ffb2d09f19b)`(int32_t num) const` | get specified preprocessor
`public int32_t `[`get_num_preprocessors`](#classshogun_1_1CFeatures_1aa1b9b05b4535ba2c8c888aa107321c54)`() const` | get number of preprocessors
`public void `[`clean_preprocessors`](#classshogun_1_1CFeatures_1aa6b20826d18617fc3bc0482c73908fb2)`()` | clears all preprocs
`public void `[`list_preprocessors`](#classshogun_1_1CFeatures_1a476493a28014c60a6006106f3d846147)`()` | print preprocessors
`public int32_t `[`get_cache_size`](#classshogun_1_1CFeatures_1a6b599085eff3dab5a66cce6f133ae47e)`() const` | get cache size
`public virtual bool `[`reshape`](#classshogun_1_1CFeatures_1ad2a12e099e61e61e3872253a13cc0287)`(int32_t num_features,int32_t num_vectors)` | in case there is a feature matrix allow for reshaping
`public void `[`list_feature_obj`](#classshogun_1_1CFeatures_1aff469383824e5b8736c191cd4e4476b7)`() const` | list feature object
`public bool `[`check_feature_compatibility`](#classshogun_1_1CFeatures_1a7fe9c8b9c4e4474b1893f837ea29fa21)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * f) const` | check feature compatibility
`public bool `[`has_property`](#classshogun_1_1CFeatures_1af181de39b142f32c3bb00a19bea32bcc)`(`[`EFeatureProperty`](#namespaceshogun_1add4a728b32cf3898a63b2ef4564c1925)` p) const` | check if features have given property
`public void `[`set_property`](#classshogun_1_1CFeatures_1a732ec5df91b2d7d80ae25a79fe068055)`(`[`EFeatureProperty`](#namespaceshogun_1add4a728b32cf3898a63b2ef4564c1925)` p)` | set property
`public void `[`unset_property`](#classshogun_1_1CFeatures_1affaad72e745ecc61e93d676d78705b1e)`(`[`EFeatureProperty`](#namespaceshogun_1add4a728b32cf3898a63b2ef4564c1925)` p)` | unset property
`public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`create_merged_copy`](#classshogun_1_1CFeatures_1abba142f59793094f4f324787d43e0b4e)`(`[`CList`](#classshogun_1_1CList)` * others) const` | Takes a list of feature instances and returns a new instance being a concatenation of a copy of this instace's data and the given instancess data. Note that the feature types have to be equal.
`public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`create_merged_copy`](#classshogun_1_1CFeatures_1aef378f04b4eb3b6a21752a5400260769)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * other) const` | Convenience method for method with same name and list as parameter.
`public virtual void `[`add_subset`](#classshogun_1_1CFeatures_1acb58d8008e2ef9bb83e6b5fc5fb42f71)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > subset)` | Adds a subset of indices on top of the current subsets (possibly subset of subset). Every call causes a new active index vector to be stored. Added subsets can be removed one-by-one. If this is not needed, [add_subset_in_place()](#classshogun_1_1CFeatures_1a6dabbf53b34ca64a7645191b8ea04e31) should be used (does not store intermediate index vectors)
`public virtual void `[`add_subset_in_place`](#classshogun_1_1CFeatures_1a6dabbf53b34ca64a7645191b8ea04e31)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > subset)` | Sets/changes latest added subset. This allows to add multiple subsets with in-place memory requirements. They cannot be removed one-by-one afterwards, only the latest active can. If this is needed, use [add_subset()](#classshogun_1_1CFeatures_1acb58d8008e2ef9bb83e6b5fc5fb42f71). If no subset is active, this just adds.
`public virtual void `[`remove_subset`](#classshogun_1_1CFeatures_1a5c8a113b96b3d3a2d565ed9fffeed172)`()` | removes that last added subset from subset stack, if existing Calls [subset_changed_post()](#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7) afterwards
`public virtual void `[`remove_all_subsets`](#classshogun_1_1CFeatures_1a434b4feb76767ed0adc9ccdd55a3ef61)`()` | removes all subsets Calls [subset_changed_post()](#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7) afterwards
`public virtual `[`CSubsetStack`](#classshogun_1_1CSubsetStack)` * `[`get_subset_stack`](#classshogun_1_1CFeatures_1a47944f23a63a0eed56ff3d0bba40d253)`()` | returns subset stack
`public inline virtual void `[`subset_changed_post`](#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7)`()` | method may be overwritten to update things that depend on subset
`public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`copy_dimension_subset`](#classshogun_1_1CFeatures_1ab5e4da6272e74503f9ac4405d8ac92b5)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > dims)` | Creates a new [CFeatures](#classshogun_1_1CFeatures) instance containing only the dimensions of the feature vector which are specified by the provided indices.
`public inline virtual bool `[`support_compatible_class`](#classshogun_1_1CFeatures_1a0e8af4cc2f64bde8fe2b3dd4557e9a4f)`() const` | does this class support compatible computation bewteen difference classes? for example, this->dot(rhs_prt), can rhs_prt be an instance of a difference class?
`public virtual bool `[`get_feature_class_compatibility`](#classshogun_1_1CFeatures_1a3f98caf024a0a4713f5201f44b71dcd6)`(`[`EFeatureClass`](#namespaceshogun_1a9e2a4d8b86b9e061779c3fdbcda57c3b)` rhs) const` | Given a class in right hand side, does this class support compatible computation?
`public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CFeatures_1ad3711d9770e4b96ae8e89a99c9f530f7)`(const `[`Tag`](#classshogun_1_1Tag)`< T > & _tag,const T & value)` | Throws an error, as features are immutable
`public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CSGObject_1ade486add69a3fb33395968d9ad8fc4be)`(const std::string & name,T * value)` | Typed setter for an object class parameter of a [Shogun](#classShogun) base class type, identified by a name.
`public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CSGObject_1a7c9acb98546f6fab79715f3c151b0de4)`(const std::string & name,`[`Some`](#classshogun_1_1Some)`< T > value)` | Typed setter for an object class parameter of a [Shogun](#classShogun) base class type, identified by a name.
`public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CSGObject_1a21240124c06dd6296b254555e15cbf2d)`(const std::string & name,T value)` | Typed setter for a non-object class parameter, identified by a name.
`public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`shallow_subset_copy`](#classshogun_1_1CFeatures_1a896eb199c1413950bbf9a89226817fb4)`()` | 
`public int32_t `[`ref`](#classshogun_1_1CSGObject_1ab8c24b912ee57d3f2c81ecccd083582a)`()` | increase reference counter
`public int32_t `[`ref_count`](#classshogun_1_1CSGObject_1a6401d138f63be4c245f1f556f197689d)`()` | display reference counter
`public int32_t `[`unref`](#classshogun_1_1CSGObject_1ad99bde1a142a1c07a963169123166e01)`()` | decrement reference counter and deallocate object if refcount is zero before or after decrementing it
`public virtual `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`shallow_copy`](#classshogun_1_1CSGObject_1a3a25f61e5062adfce5df46be45e7e8c4)`() const` | A shallow copy. All the SGObject instance variables will be simply assigned and SG_REF-ed.
`public virtual `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`deep_copy`](#classshogun_1_1CSGObject_1afa9949a366159a39ab8118918b57f578)`() const` | A deep copy. All the instance variables will also be copied.
`public virtual bool `[`is_generic`](#classshogun_1_1CSGObject_1a6801eb416eadc35f5499a48436e1cf43)`(EPrimitiveType * generic) const` | If the SGSerializable is a class template then TRUE will be returned and GENERIC is set to the type of the generic.
`public template<>`  <br/>`void `[`set_generic`](#classshogun_1_1CSGObject_1ad3463e866082d6707af04276ae8aa477)`()` | set generic type to T
`public template<>`  <br/>`void `[`set_generic`](#classshogun_1_1CSGObject_1a9fca24ed1095acc6c52f3c5353156d74)`()` | 
`public inline EPrimitiveType `[`get_generic`](#classshogun_1_1CSGObject_1a3329cfa1654e757472c9098770635530)`() const` | Returns generic type. 
`public void `[`unset_generic`](#classshogun_1_1CSGObject_1aa15afe4277334593139dae884cc951e1)`()` | unset generic type
`public virtual void `[`print_serializable`](#classshogun_1_1CSGObject_1ade3b14c2f62ba4d8f2f6422e08567ae9)`(const char * prefix)` | prints registered parameters out
`public virtual bool `[`save_serializable`](#classshogun_1_1CSGObject_1aa9787e341533c4970885ce6d3022a935)`(`[`CSerializableFile`](#classshogun_1_1CSerializableFile)` * file,const char * prefix)` | Save this object to file.
`public virtual bool `[`load_serializable`](#classshogun_1_1CSGObject_1ad67e38ad80d4152151081f838c0a13e1)`(`[`CSerializableFile`](#classshogun_1_1CSerializableFile)` * file,const char * prefix)` | Load this object from file. If it will fail (returning FALSE) then this object will contain inconsistent data and should not be used!
`public void `[`set_global_io`](#classshogun_1_1CSGObject_1a36d256e2d05357b57e83f31f7e358f69)`(`[`SGIO`](#classshogun_1_1SGIO)` * io)` | set the io object
`public `[`SGIO`](#classshogun_1_1SGIO)` * `[`get_global_io`](#classshogun_1_1CSGObject_1ac6c994717cb550f81c70129e839ea98b)`()` | get the io object
`public void `[`set_global_parallel`](#classshogun_1_1CSGObject_1a9543b75e320e477d12553f2aa8593e8a)`(`[`Parallel`](#classshogun_1_1Parallel)` * parallel)` | set the parallel object
`public `[`Parallel`](#classshogun_1_1Parallel)` * `[`get_global_parallel`](#classshogun_1_1CSGObject_1a2cd3ba36c7e0ef6e5234393cc7e22bb0)`()` | get the parallel object
`public void `[`set_global_version`](#classshogun_1_1CSGObject_1a1ba2ee8842e30d8ceaaf5d44c567efe1)`(`[`Version`](#classshogun_1_1Version)` * version)` | set the version object
`public `[`Version`](#classshogun_1_1Version)` * `[`get_global_version`](#classshogun_1_1CSGObject_1a03ce854ec4f745dbe219533dc36c9e20)`()` | get the version object
`public `[`SGStringList`](#classshogun_1_1SGStringList)`< char > `[`get_modelsel_names`](#classshogun_1_1CSGObject_1a730ecbf7f326b93350f00cc937e59ac0)`()` | #### Returns
`public void `[`print_modsel_params`](#classshogun_1_1CSGObject_1a8dcb739fd760f227b3fa1dc0684f762d)`()` | prints all parameter registered for model selection and their type
`public char * `[`get_modsel_param_descr`](#classshogun_1_1CSGObject_1ac26fd2403c6a5c334f4a2d8094be9833)`(const char * param_name)` | Returns description of a given parameter string, if it exists. SG_ERROR otherwise
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`get_modsel_param_index`](#classshogun_1_1CSGObject_1aeb1f5a55b8170409ff2a94e3a3664c05)`(const char * param_name)` | Returns index of model selection parameter with provided index
`public void `[`build_gradient_parameter_dictionary`](#classshogun_1_1CSGObject_1a17f448c257ccf4083987c4670c86a967)`(`[`CMap](#classshogun_1_1CMap)< [TParameter](#structshogun_1_1TParameter) *, [CSGObject`](#classshogun_1_1CSGObject)` *> * dict)` | Builds a dictionary of all parameters in SGObject as well of those of SGObjects that are parameters of this object. Dictionary maps parameters to the objects that own them.
`public bool `[`has`](#classshogun_1_1CSGObject_1aa911ba3ef90e0b3179e0a8dc10586424)`(const std::string & name) const` | Checks if object has a class parameter identified by a name.
`public template<>`  <br/>`inline bool `[`has`](#classshogun_1_1CSGObject_1a0ba98fe70db33bb2036e76fd4ec28e04)`(const `[`Tag`](#classshogun_1_1Tag)`< T > & tag) const` | Checks if object has a class parameter identified by a [Tag](#classshogun_1_1Tag).
`public template<>`  <br/>`inline bool `[`has`](#classshogun_1_1CSGObject_1ac947804131f9937507db2da99f36e933)`(const std::string & name) const` | Checks if a type exists for a class parameter identified by a name.
`public template<>`  <br/>`inline void `[`add`](#classshogun_1_1CSGObject_1a3b1dff76eb6397801f84101060c5956c)`(const std::string & name,T * value)` | Typed appender for an object class parameter of a [Shogun](#classShogun) base class type, identified by a name.
`public template<>`  <br/>`inline void `[`add`](#classshogun_1_1CSGObject_1a98738b2423f4eb9cee078924311a9e04)`(const std::string & name,`[`Some`](#classshogun_1_1Some)`< T > value)` | Typed appender for an object class parameter of a [Shogun](#classShogun) base class type, identified by a name.
`public `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`get`](#classshogun_1_1CSGObject_1a4de6e15966500093d2c04db29bbf4ac7)`(const std::string & name)` | Untyped getter for an object class parameter, identified by a name. Will attempt to get specified object of appropriate internal type.
`public template<>`  <br/>`inline T `[`get`](#classshogun_1_1CSGObject_1a081b48e5b14e9ff75e7e56c941870ed5)`(const `[`Tag`](#classshogun_1_1Tag)`< T > & _tag) const` | Getter for a class parameter, identified by a [Tag](#classshogun_1_1Tag). Throws an exception if the class does not have such a parameter.
`public template<>`  <br/>`inline T `[`get`](#classshogun_1_1CSGObject_1adeb49b89495067e83e4208d1d60bea60)`(const std::string & name) const` | Getter for a class parameter, identified by a name. Throws an exception if the class does not have such a parameter.
`public virtual std::string `[`to_string`](#classshogun_1_1CSGObject_1aac993ecccd3d88aafefb6b8e3caa1dee)`() const` | Returns string representation of the object that contains its name and parameters.
`public std::vector< std::string > `[`parameter_names`](#classshogun_1_1CSGObject_1a924f620b4718c3367cf5403c52a30074)`() const` | Returns set of all parameter names of the object.
`public template<>`  <br/>`inline T * `[`as`](#classshogun_1_1CSGObject_1aa4cdefb81ca8c583f1c2ef0d20d8feeb)`()` | Specializes the object to the specified type. Throws exception if the object cannot be specialized.
`public inline `[`SGObservable`](#classshogun_1_1CSGObject_1a3f344a622ab6c3e0dd73b5dd3f7aa556)` * `[`get_parameters_observable`](#classshogun_1_1CSGObject_1a539800ba1bbe5a4260df8c5641305afc)`()` | Get parameters observable 
`public void `[`subscribe_to_parameters`](#classshogun_1_1CSGObject_1aeb13a31ffeb912767b6f16f1bc1d3e61)`(`[`ParameterObserverInterface`](#classshogun_1_1ParameterObserverInterface)` * obs)` | Subscribe a parameter observer to watch over params
`public void `[`list_observable_parameters`](#classshogun_1_1CSGObject_1aac0c9d125edd61f235eeba5efed47142)`()` | Print to stdout a list of observable parameters
`public virtual void `[`update_parameter_hash`](#classshogun_1_1CSGObject_1afd6d5beea40c6d1222d361fb706d4651)`()` | Updates the hash of current parameter combination
`public virtual bool `[`parameter_hash_changed`](#classshogun_1_1CSGObject_1aeb270031640bb2f00ec9452c637bfbc2)`()` | #### Returns
`public virtual bool `[`equals`](#classshogun_1_1CSGObject_1afe6a79f0c2c3db09f98ebdbe23a8a5d9)`(const `[`CSGObject`](#classshogun_1_1CSGObject)` * other) const` | Deep comparison of two objects.
`public virtual `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`clone`](#classshogun_1_1CSGObject_1a4ae46a8c294896b69fc21384f6d86fad)`()` | Creates a clone of the current object. This is done via recursively traversing all parameters, which corresponds to a deep copy. Calling equals on the cloned object always returns true although none of the memory of both objects overlaps.
`protected `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< ST > `[`sparse_feature_matrix`](#classshogun_1_1CSparseFeatures_1a7e0b7c3ad27442fa4fb39c86c8d53346) | array of sparse vectors of size num_vectors
`protected `[`CCache](#classshogun_1_1CCache)< [SGSparseVectorEntry`](#structshogun_1_1SGSparseVectorEntry)`< ST > > * `[`feature_cache`](#classshogun_1_1CSparseFeatures_1a3b6d9e774ba060c3ee9a063db7c1547e) | feature cache
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`combined_weight`](#classshogun_1_1CDotFeatures_1a900f01e3d31c1ed4470c2972433f958d) | feature weighting in combined dot features
`protected `[`CSubsetStack`](#classshogun_1_1CSubsetStack)` * `[`m_subset_stack`](#classshogun_1_1CFeatures_1ac406fc1620ad5a8714a1c34c935ae328) | subset used for index transformations
`protected virtual `[`SGSparseVectorEntry`](#structshogun_1_1SGSparseVectorEntry)`< ST > * `[`compute_sparse_feature_vector`](#classshogun_1_1CSparseFeatures_1a25afcb83ea08a98851a3232854f1c7f0)`(int32_t num,int32_t & len,`[`SGSparseVectorEntry`](#structshogun_1_1SGSparseVectorEntry)`< ST > * target)` | compute feature vector for sample num if target is set the vector is written to target len is returned by reference
`protected template<>`  <br/>`inline `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`get_sgobject_type_dispatcher`](#classshogun_1_1CSGObject_1a7de7c1e11c3d4322d74a9a8cf5cc13f1)`(const std::string & name)` | 
`protected virtual void `[`load_serializable_pre`](#classshogun_1_1CSGObject_1a7361535fc1a8b13beb9dd0b4ac2dd790)`()` | Can (optionally) be overridden to pre-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::LOAD_SERIALIZABLE_PRE is called.
`protected virtual void `[`load_serializable_post`](#classshogun_1_1CSGObject_1a4c8da771d1ddf319cabc6b9e896326f2)`()` | Can (optionally) be overridden to post-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::LOAD_SERIALIZABLE_POST is called.
`protected virtual void `[`save_serializable_pre`](#classshogun_1_1CSGObject_1a44300a33d16909f1bf7a129d19d4ca41)`()` | Can (optionally) be overridden to pre-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::SAVE_SERIALIZABLE_PRE is called.
`protected virtual void `[`save_serializable_post`](#classshogun_1_1CSGObject_1ab63af4bfbc71bb737703e48425db1aa2)`()` | Can (optionally) be overridden to post-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::SAVE_SERIALIZABLE_POST is called.
`protected template<>`  <br/>`inline void `[`register_param`](#classshogun_1_1CSGObject_1ac0fdc76cf24d242d99d8d862475131a6)`(`[`Tag`](#classshogun_1_1Tag)`< T > & _tag,const T & value)` | Registers a class parameter which is identified by a tag. This enables the parameter to be modified by [put()](#classshogun_1_1CSGObject_1ad3711d9770e4b96ae8e89a99c9f530f7) and retrieved by [get()](#classshogun_1_1CSGObject_1a4de6e15966500093d2c04db29bbf4ac7). Parameters can be registered in the constructor of the class.
`protected template<>`  <br/>`inline void `[`register_param`](#classshogun_1_1CSGObject_1ad06fb7206a6d3cecfb21fb270cdefbc5)`(const std::string & name,const T & value)` | Registers a class parameter which is identified by a name. This enables the parameter to be modified by [put()](#classshogun_1_1CSGObject_1ad3711d9770e4b96ae8e89a99c9f530f7) and retrieved by [get()](#classshogun_1_1CSGObject_1a4de6e15966500093d2c04db29bbf4ac7). Parameters can be registered in the constructor of the class.
`protected template<>`  <br/>`inline void `[`watch_param`](#classshogun_1_1CSGObject_1a430010070f8439a0b49b647fa6f60296)`(const std::string & name,T * value,`[`AnyParameterProperties`](#classshogun_1_1AnyParameterProperties)` properties)` | Puts a pointer to some parameter into the parameter map.
`protected template<>`  <br/>`inline void `[`watch_param`](#classshogun_1_1CSGObject_1ad0e74133e14d5cba696532db034671ec)`(const std::string & name,T ** value,S * len,`[`AnyParameterProperties`](#classshogun_1_1AnyParameterProperties)` properties)` | Puts a pointer to some parameter array into the parameter map.
`protected template<>`  <br/>`inline void `[`watch_param`](#classshogun_1_1CSGObject_1a7e9db200a31d2d1faaca5a83828aeee5)`(const std::string & name,T ** value,S * rows,S * cols,`[`AnyParameterProperties`](#classshogun_1_1AnyParameterProperties)` properties)` | Puts a pointer to some 2d parameter array (i.e. a matrix) into the parameter map.
`protected template<>`  <br/>`inline void `[`watch_method`](#classshogun_1_1CSGObject_1ad4c5a49c32b7640f955bd3c2ca844b8f)`(const std::string & name,T(S::*)() const method)` | Puts a pointer to a (lazily evaluated) function into the parameter map.
`protected virtual `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`create_empty`](#classshogun_1_1CSGObject_1adf79c57eee99ece954548a61ca38cd80)`() const` | Returns an empty instance of own type.
`protected void `[`observe`](#classshogun_1_1CSGObject_1ab7f66a33081e42252d9c0bb971bbb019)`(const `[`ObservedValue`](#classshogun_1_1ObservedValue)` value)` | Observe a parameter value and emit them to observer. 
`protected void `[`register_observable_param`](#classshogun_1_1CSGObject_1a0fe3525aebc1dd5896191740320e20cd)`(const std::string & name,const `[`SG_OBS_VALUE_TYPE`](#namespaceshogun_1adcef34436f03207dcc3b97db8b4794d9)` type,const std::string & description)` | Register which params this object can emit. 
`typedef `[`SGSubject`](#classshogun_1_1CSGObject_1a52509313192ce488ae91f9d7e2b16267) | Definition of observed subject
`typedef `[`SGObservable`](#classshogun_1_1CSGObject_1a3f344a622ab6c3e0dd73b5dd3f7aa556) | Definition of observable
`typedef `[`SGSubscriber`](#classshogun_1_1CSGObject_1a658eb47ba606529e8ffc5090d36e34e8) | Definition of subscriber

## Members

#### `public `[`SGIO`](#classshogun_1_1SGIO)` * `[`io`](#classshogun_1_1CSGObject_1ab3ff22f724961ace985100941ba0364d) {#classshogun_1_1CSGObject_1ab3ff22f724961ace985100941ba0364d}

io

#### `public `[`Parallel`](#classshogun_1_1Parallel)` * `[`parallel`](#classshogun_1_1CSGObject_1a1401044636b5c2353226b974526302e9) {#classshogun_1_1CSGObject_1a1401044636b5c2353226b974526302e9}

parallel

#### `public `[`Version`](#classshogun_1_1Version)` * `[`version`](#classshogun_1_1CSGObject_1afc25f30ab1a6d04798c360a2ce70b87d) {#classshogun_1_1CSGObject_1afc25f30ab1a6d04798c360a2ce70b87d}

version

#### `public `[`Parameter`](#classshogun_1_1Parameter)` * `[`m_parameters`](#classshogun_1_1CSGObject_1a70e59038292e669701bad2af7715aa1e) {#classshogun_1_1CSGObject_1a70e59038292e669701bad2af7715aa1e}

parameters

#### `public `[`Parameter`](#classshogun_1_1Parameter)` * `[`m_model_selection_parameters`](#classshogun_1_1CSGObject_1a113f5ae82840ac3f354f94456c10f59b) {#classshogun_1_1CSGObject_1a113f5ae82840ac3f354f94456c10f59b}

model selection parameters

#### `public `[`Parameter`](#classshogun_1_1Parameter)` * `[`m_gradient_parameters`](#classshogun_1_1CSGObject_1ac3f51364b93830b9c9d991cb2d5801f4) {#classshogun_1_1CSGObject_1ac3f51364b93830b9c9d991cb2d5801f4}

parameters wrt which we can compute gradients

#### `public uint32_t `[`m_hash`](#classshogun_1_1CSGObject_1a170f14be9561242f924939c56b372a41) {#classshogun_1_1CSGObject_1a170f14be9561242f924939c56b372a41}

Hash of parameter values

#### `public  `[`CSparseFeatures`](#classshogun_1_1CSparseFeatures_1afb99d45e29457cbe4b2551bb5b9b996c)`(int32_t size)` {#classshogun_1_1CSparseFeatures_1afb99d45e29457cbe4b2551bb5b9b996c}

constructor

#### Parameters
* `size` cache size

#### `public  `[`CSparseFeatures`](#classshogun_1_1CSparseFeatures_1a6add6550063e649c9daada7853361a94)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< ST > sparse)` {#classshogun_1_1CSparseFeatures_1a6add6550063e649c9daada7853361a94}

convenience constructor that creates sparse features from sparse features

#### Parameters
* `sparse` sparse matrix

#### `public  `[`CSparseFeatures`](#classshogun_1_1CSparseFeatures_1a9d81cc71f02cbf7f57d5bc9752f7ddff)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< ST > dense)` {#classshogun_1_1CSparseFeatures_1a9d81cc71f02cbf7f57d5bc9752f7ddff}

convenience constructor that creates sparse features from dense features

#### Parameters
* `dense` dense feature matrix

#### `public  `[`CSparseFeatures`](#classshogun_1_1CSparseFeatures_1a337640d02feb5d1894d125977ccc53bb)`(const `[`CSparseFeatures`](#classshogun_1_1CSparseFeatures)` & orig)` {#classshogun_1_1CSparseFeatures_1a337640d02feb5d1894d125977ccc53bb}

copy constructor

#### `public  `[`CSparseFeatures`](#classshogun_1_1CSparseFeatures_1a9aa5e9d7914378ff802909a6cb4ea4df)`(`[`CDenseFeatures`](#classshogun_1_1CDenseFeatures)`< ST > * dense)` {#classshogun_1_1CSparseFeatures_1a9aa5e9d7914378ff802909a6cb4ea4df}

copy constructor from DenseFeatures

#### `public  `[`CSparseFeatures`](#classshogun_1_1CSparseFeatures_1a0a4554f19043005bd2530c8c8414a1be)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` {#classshogun_1_1CSparseFeatures_1a0a4554f19043005bd2530c8c8414a1be}

constructor loading features from file

#### Parameters
* `loader` File object to load data from

#### `public virtual  `[`~CSparseFeatures`](#classshogun_1_1CSparseFeatures_1a9a588e07feac3260d3e9ea05c86e6d0f)`()` {#classshogun_1_1CSparseFeatures_1a9a588e07feac3260d3e9ea05c86e6d0f}

default destructor

#### `public void `[`free_sparse_feature_matrix`](#classshogun_1_1CSparseFeatures_1a7d1791c8d5684f8508e478eaa95a0a7c)`()` {#classshogun_1_1CSparseFeatures_1a7d1791c8d5684f8508e478eaa95a0a7c}

free sparse feature matrix

any subset is removed

#### `public void `[`free_sparse_features`](#classshogun_1_1CSparseFeatures_1a51881f6fcd5a266ebaef20a5e382199c)`()` {#classshogun_1_1CSparseFeatures_1a51881f6fcd5a266ebaef20a5e382199c}

free sparse feature matrix and cache

any subset is removed

#### `public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`duplicate`](#classshogun_1_1CSparseFeatures_1a451c5fd7954842d7a19f1b0faa710e0c)`() const` {#classshogun_1_1CSparseFeatures_1a451c5fd7954842d7a19f1b0faa710e0c}

duplicate feature object

#### Returns
feature object

#### `public ST `[`get_feature`](#classshogun_1_1CSparseFeatures_1a457ca9c3e75d88b33364c4dff73db372)`(int32_t num,int32_t index)` {#classshogun_1_1CSparseFeatures_1a457ca9c3e75d88b33364c4dff73db372}

get a single feature

possible with subset

#### Parameters
* `num` number of feature vector to retrieve 

* `index` index of feature in this vector

#### Returns
sum of features that match dimension index and 0 if none is found

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< ST > `[`get_full_feature_vector`](#classshogun_1_1CSparseFeatures_1ab1fe225ab22e1a370aa7015260a95370)`(int32_t num)` {#classshogun_1_1CSparseFeatures_1ab1fe225ab22e1a370aa7015260a95370}

get the fully expanded dense feature vector num

#### Returns
dense feature vector 

#### Parameters
* `num` index of feature vector

#### `public virtual int32_t `[`get_nnz_features_for_vector`](#classshogun_1_1CSparseFeatures_1ab7b680a2262f123880faae88061830cb)`(int32_t num)` {#classshogun_1_1CSparseFeatures_1ab7b680a2262f123880faae88061830cb}

get number of non-zero features in vector

#### Parameters
* `num` which vector 

#### Returns
number of non-zero features in vector

#### `public `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< ST > `[`get_sparse_feature_vector`](#classshogun_1_1CSparseFeatures_1aef6eae81a9bc8c951de5493fe53adcdf)`(int32_t num)` {#classshogun_1_1CSparseFeatures_1aef6eae81a9bc8c951de5493fe53adcdf}

get sparse feature vector for sample num from the matrix as it is if matrix is initialized, else return preprocessed compute_feature_vector

possible with subset

#### Parameters
* `num` index of feature vector 

#### Returns
sparse feature vector

#### `public ST `[`dense_dot`](#classshogun_1_1CSparseFeatures_1a2d0e500f551684261674d709859e7fb1)`(ST alpha,int32_t num,ST * vec,int32_t dim,ST b)` {#classshogun_1_1CSparseFeatures_1a2d0e500f551684261674d709859e7fb1}

compute the dot product between dense weights and a sparse feature vector alpha * sparse^T * w + b

possible with subset

#### Parameters
* `alpha` scalar to multiply with 

* `num` index of feature vector 

* `vec` dense vector to compute dot product with 

* `dim` length of the dense vector 

* `b` bias 

#### Returns
dot product between dense weights and a sparse feature vector

#### `public virtual void `[`add_to_dense_vec`](#classshogun_1_1CSparseFeatures_1a05ee86f75779fe7b29638f131d843868)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` alpha,int32_t num,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * vec,int32_t dim,bool abs_val)` {#classshogun_1_1CSparseFeatures_1a05ee86f75779fe7b29638f131d843868}

add a sparse feature vector onto a dense one dense+=alpha*sparse

possible with subset

#### Parameters
* `alpha` scalar to multiply with 

* `num` index of feature vector 

* `vec` dense vector 

* `dim` length of the dense vector 

* `abs_val` if true, do dense+=alpha*abs(sparse)

#### `public void `[`free_sparse_feature_vector`](#classshogun_1_1CSparseFeatures_1abb38feee4815fd4b0ca1a5d581003bb7)`(int32_t num)` {#classshogun_1_1CSparseFeatures_1abb38feee4815fd4b0ca1a5d581003bb7}

free sparse feature vector

possible with subset

#### Parameters
* `num` index of this vector in the cache

#### `public `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< ST > * `[`get_sparse_feature_matrix`](#classshogun_1_1CSparseFeatures_1a2941f8e93a187097b8b2dd90955049eb)`(int32_t & num_feat,int32_t & num_vec)` {#classshogun_1_1CSparseFeatures_1a2941f8e93a187097b8b2dd90955049eb}

get the pointer to the sparse feature matrix num_feat,num_vectors are returned by reference

not possible with subset

#### Parameters
* `num_feat` number of features in matrix 

* `num_vec` number of vectors in matrix 

#### Returns
feature matrix

#### `public `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< ST > `[`get_sparse_feature_matrix`](#classshogun_1_1CSparseFeatures_1a1f76335e82bcc10155dddc9ba53fe8c9)`()` {#classshogun_1_1CSparseFeatures_1a1f76335e82bcc10155dddc9ba53fe8c9}

get the sparse feature matrix

not possible with subset

#### Returns
sparse matrix

#### `public `[`CSparseFeatures`](#classshogun_1_1CSparseFeatures)`< ST > * `[`get_transposed`](#classshogun_1_1CSparseFeatures_1a6fb4c681fc001c28e452a3254f410fd7)`()` {#classshogun_1_1CSparseFeatures_1a6fb4c681fc001c28e452a3254f410fd7}

get a transposed copy of the features

not possible with subset

#### Returns
transposed copy

#### `public `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< ST > * `[`get_transposed`](#classshogun_1_1CSparseFeatures_1a32ba325366b4457400edc86f6137b7ab)`(int32_t & num_feat,int32_t & num_vec)` {#classshogun_1_1CSparseFeatures_1a32ba325366b4457400edc86f6137b7ab}

compute and return the transpose of the sparse feature matrix which will be prepocessed. num_feat, num_vectors are returned by reference caller has to clean up

possible with subset

#### Parameters
* `num_feat` number of features in matrix 

* `num_vec` number of vectors in matrix 

#### Returns
transposed sparse feature matrix

#### `public void `[`set_sparse_feature_matrix`](#classshogun_1_1CSparseFeatures_1a9925b7247d1ec2f61d3eb0458b1c7f83)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< ST > sm)` {#classshogun_1_1CSparseFeatures_1a9925b7247d1ec2f61d3eb0458b1c7f83}

set sparse feature matrix

not possible with subset

#### Parameters
* `sm` sparse feature matrix

#### `public `[`SGMatrix`](#classshogun_1_1SGMatrix)`< ST > `[`get_full_feature_matrix`](#classshogun_1_1CSparseFeatures_1a9c3af84f8076ce6bccc8c9b20bc23be3)`()` {#classshogun_1_1CSparseFeatures_1a9c3af84f8076ce6bccc8c9b20bc23be3}

gets a copy of a full feature matrix

possible with subset

#### Returns
full dense feature matrix

#### `public virtual void `[`set_full_feature_matrix`](#classshogun_1_1CSparseFeatures_1a70f397556c4ace1ac9b569c130f3c29e)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< ST > full)` {#classshogun_1_1CSparseFeatures_1a70f397556c4ace1ac9b569c130f3c29e}

creates a sparse feature matrix from a full dense feature matrix necessary to set feature_matrix, num_features and num_vectors where num_features is the column offset, and columns are linear in memory see above for definition of sparse_feature_matrix

any subset is removed before

#### Parameters
* `full` full feature matrix

#### `public virtual int32_t `[`get_num_vectors`](#classshogun_1_1CSparseFeatures_1a25a45bd4c25c9d7d72826dd195a7c696)`() const` {#classshogun_1_1CSparseFeatures_1a25a45bd4c25c9d7d72826dd195a7c696}

get number of feature vectors, possibly of subset

#### Returns
number of feature vectors

#### `public int32_t `[`get_num_features`](#classshogun_1_1CSparseFeatures_1ac8a43465974b1625cd461d1e19d290ff)`() const` {#classshogun_1_1CSparseFeatures_1ac8a43465974b1625cd461d1e19d290ff}

get number of features

#### Returns
number of features

#### `public int32_t `[`set_num_features`](#classshogun_1_1CSparseFeatures_1ac09e081001f3f6c602c5e1b4642ed3f3)`(int32_t num)` {#classshogun_1_1CSparseFeatures_1ac09e081001f3f6c602c5e1b4642ed3f3}

set number of features

Sometimes when loading sparse features not all possible dimensions are used. This may pose a problem to classifiers when being applied to higher dimensional test-data. This function allows to artificially explode the feature space

#### Parameters
* `num` the number of features, must be larger than the current number of features 

#### Returns
previous number of features

#### `public virtual `[`EFeatureClass`](#namespaceshogun_1a9e2a4d8b86b9e061779c3fdbcda57c3b)` `[`get_feature_class`](#classshogun_1_1CSparseFeatures_1ae83dd54e69a4e8f1c7a571545fa1c8c1)`() const` {#classshogun_1_1CSparseFeatures_1ae83dd54e69a4e8f1c7a571545fa1c8c1}

get feature class

#### Returns
feature class SPARSE

#### `public virtual `[`EFeatureType`](#namespaceshogun_1a064eec90e91f56435546d77f38c0b618)` `[`get_feature_type`](#classshogun_1_1CSparseFeatures_1a48ec5bbd5022e2ffa67a31613fd257f9)`() const` {#classshogun_1_1CSparseFeatures_1a48ec5bbd5022e2ffa67a31613fd257f9}

get feature type

#### Returns
templated feature type

#### `public void `[`free_feature_vector`](#classshogun_1_1CSparseFeatures_1a1f7aaef030fc753b2622779af19ca3ae)`(int32_t num)` {#classshogun_1_1CSparseFeatures_1a1f7aaef030fc753b2622779af19ca3ae}

free feature vector

possible with subset

#### Parameters
* `num` index of vector in cache

#### `public int64_t `[`get_num_nonzero_entries`](#classshogun_1_1CSparseFeatures_1af10874a583f1aecd35e0374535a8411d)`()` {#classshogun_1_1CSparseFeatures_1af10874a583f1aecd35e0374535a8411d}

get number of non-zero entries in sparse feature matrix

#### Returns
number of non-zero entries in sparse feature matrix

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`compute_squared`](#classshogun_1_1CSparseFeatures_1af16c85d52cd4baece591def958c2de16)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * sq)` {#classshogun_1_1CSparseFeatures_1af16c85d52cd4baece591def958c2de16}

compute a^2 on all feature vectors

possible with subset

#### Parameters
* `sq` the square for each vector is stored in here 

#### Returns
the square for each vector

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_squared_norm`](#classshogun_1_1CSparseFeatures_1a36853f4e7ff0735cc39befea4222f30c)`(`[`CSparseFeatures](#classshogun_1_1CSparseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * lhs,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * sq_lhs,int32_t idx_a,`[`CSparseFeatures](#classshogun_1_1CSparseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * rhs,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * sq_rhs,int32_t idx_b)` {#classshogun_1_1CSparseFeatures_1a36853f4e7ff0735cc39befea4222f30c}

compute (a-b)^2 (== a^2+b^2-2ab) usually called by kernels'/distances' compute functions works on two feature vectors, although it is a member of a single feature: can either be called by lhs or rhs.

possible wiht subsets on lhs or rhs

#### Parameters
* `lhs` left-hand side features 

* `sq_lhs` squared values of left-hand side 

* `idx_a` index of left-hand side's vector to compute 

* `rhs` right-hand side features 

* `sq_rhs` squared values of right-hand side 

* `idx_b` index of right-hand side's vector to compute

#### `public virtual void `[`load`](#classshogun_1_1CSparseFeatures_1a5d33ec59a4be25056cca1f3b6691ad00)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` {#classshogun_1_1CSparseFeatures_1a5d33ec59a4be25056cca1f3b6691ad00}

load features from file

any subset is removed before

#### Parameters
* `loader` File object to load data from

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`load_with_labels`](#classshogun_1_1CSparseFeatures_1a280b249dd4ccf9556944c8a91c8c00e1)`(`[`CLibSVMFile`](#classshogun_1_1CLibSVMFile)` * loader)` {#classshogun_1_1CSparseFeatures_1a280b249dd4ccf9556944c8a91c8c00e1}

load features from file

any subset is removed before

#### Parameters
* `loader` File object to load data from 

#### Returns
label vector

#### `public virtual void `[`save`](#classshogun_1_1CSparseFeatures_1a2ec11d78c7f60dfbc77bc2f56d211033)`(`[`CFile`](#classshogun_1_1CFile)` * writer)` {#classshogun_1_1CSparseFeatures_1a2ec11d78c7f60dfbc77bc2f56d211033}

save features to file

not possible with subset

#### Parameters
* `writer` File object to write data to

#### `public void `[`save_with_labels`](#classshogun_1_1CSparseFeatures_1a4f9660cee348dfcedd859fd1170c5750)`(`[`CLibSVMFile`](#classshogun_1_1CLibSVMFile)` * writer,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > labels)` {#classshogun_1_1CSparseFeatures_1a4f9660cee348dfcedd859fd1170c5750}

save features to file

not possible with subset

#### Parameters
* `writer` File object to write data to 

* `labels` vector with labels to write out

#### `public void `[`sort_features`](#classshogun_1_1CSparseFeatures_1aa0010ddb91f3132cf24e5266551b7215)`()` {#classshogun_1_1CSparseFeatures_1aa0010ddb91f3132cf24e5266551b7215}

ensure that features occur in ascending order, only call when no preprocessors are attached

not possiblwe with subset

#### `public virtual int32_t `[`get_dim_feature_space`](#classshogun_1_1CSparseFeatures_1a13fbd248e2925b0a24f49889c542e74c)`() const` {#classshogun_1_1CSparseFeatures_1a13fbd248e2925b0a24f49889c542e74c}

obtain the dimensionality of the feature space

(not mix this up with the dimensionality of the input space, usually obtained via [get_num_features()](#classshogun_1_1CSparseFeatures_1ac8a43465974b1625cd461d1e19d290ff))

#### Returns
dimensionality

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`dot`](#classshogun_1_1CSparseFeatures_1a1f97967a070acb388927a27a449b9bae)`(int32_t vec_idx1,`[`CDotFeatures`](#classshogun_1_1CDotFeatures)` * df,int32_t vec_idx2)` {#classshogun_1_1CSparseFeatures_1a1f97967a070acb388927a27a449b9bae}

compute dot product between vector1 and vector2, appointed by their indices

possible with subset of this instance and of DotFeatures

#### Parameters
* `vec_idx1` index of first vector 

* `df` DotFeatures (of same kind) to compute dot product with 

* `vec_idx2` index of second vector

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`dense_dot`](#classshogun_1_1CSparseFeatures_1a403b986eccb3fb295a77f2e699f02105)`(int32_t vec_idx1,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * vec2,int32_t vec2_len)` {#classshogun_1_1CSparseFeatures_1a403b986eccb3fb295a77f2e699f02105}

compute dot product between vector1 and a dense vector

possible with subset

#### Parameters
* `vec_idx1` index of first vector 

* `vec2` pointer to real valued vector 

* `vec2_len` length of real valued vector

#### `public virtual void * `[`get_feature_iterator`](#classshogun_1_1CSparseFeatures_1a05368260e526dd61037bf36049f7a458)`(int32_t vector_index)` {#classshogun_1_1CSparseFeatures_1a05368260e526dd61037bf36049f7a458}

iterate over the non-zero features

call get_feature_iterator first, followed by get_next_feature and free_feature_iterator to cleanup

possible with subset

#### Parameters
* `vector_index` the index of the vector over whose components to iterate over 

#### Returns
feature iterator (to be passed to get_next_feature)

#### `public virtual bool `[`get_next_feature`](#classshogun_1_1CSparseFeatures_1a55dc88fdfa05cbcb8ffee8d191481123)`(int32_t & index,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` & value,void * iterator)` {#classshogun_1_1CSparseFeatures_1a55dc88fdfa05cbcb8ffee8d191481123}

iterate over the non-zero features

call this function with the iterator returned by get_first_feature and call free_feature_iterator to cleanup

#### Parameters
* `index` is returned by reference (-1 when not available) 

* `value` is returned by reference 

* `iterator` as returned by get_first_feature 

#### Returns
true if a new non-zero feature got returned

#### `public virtual void `[`free_feature_iterator`](#classshogun_1_1CSparseFeatures_1a3e93f36c6ec2624036a0f8d961c15d9f)`(void * iterator)` {#classshogun_1_1CSparseFeatures_1a3e93f36c6ec2624036a0f8d961c15d9f}

clean up iterator call this function with the iterator returned by get_first_feature

#### Parameters
* `iterator` as returned by get_first_feature

#### `public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`copy_subset`](#classshogun_1_1CSparseFeatures_1adf4a1baaff0c06456ceca3b217c46338)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CSparseFeatures_1adf4a1baaff0c06456ceca3b217c46338}

Creates a new [CFeatures](#classshogun_1_1CFeatures) instance containing copies of the elements which are specified by the provided indices.

#### Parameters
* `indices` indices of feature elements to copy 

#### Returns
new [CFeatures](#classshogun_1_1CFeatures) instance with copies of feature data

#### `public inline virtual const char * `[`get_name`](#classshogun_1_1CSparseFeatures_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` {#classshogun_1_1CSparseFeatures_1a9cb485686dd7a1e6f7103cf42e87717e}

#### Returns
object name

#### `public template<>`  <br/>` `[`CSparseFeatures`](#classshogun_1_1CSparseFeatures_1ae1057a99dcf60605ef972ffa8c1ac389)`(`[`CDenseFeatures](#classshogun_1_1CDenseFeatures)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > * dense)` {#classshogun_1_1CSparseFeatures_1ae1057a99dcf60605ef972ffa8c1ac389}

#### `public template<>`  <br/>`virtual void `[`add_to_dense_vec`](#classshogun_1_1CSparseFeatures_1aad4da1ab509c3a70a9c74d1f374d6195)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` alpha,int32_t vec_idx1,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * vec2,int32_t vec2_len,bool abs_val)` {#classshogun_1_1CSparseFeatures_1aad4da1ab509c3a70a9c74d1f374d6195}

add vector 1 multiplied with alpha to dense vector2

#### Parameters
* `alpha` scalar alpha 

* `vec_idx1` index of first vector 

* `vec2` pointer to real valued vector 

* `vec2_len` length of real valued vector 

* `abs_val` if true add the absolute value

#### `public template<>`  <br/>[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`compute_squared`](#classshogun_1_1CSparseFeatures_1a91df3d94e7f3aceaa561287d3c323a19)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * sq)` {#classshogun_1_1CSparseFeatures_1a91df3d94e7f3aceaa561287d3c323a19}

#### `public template<>`  <br/>`virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`dot`](#classshogun_1_1CSparseFeatures_1a58a7125f3ee6d08bec5bfef985a0eac1)`(int32_t vec_idx1,`[`CDotFeatures`](#classshogun_1_1CDotFeatures)` * df,int32_t vec_idx2)` {#classshogun_1_1CSparseFeatures_1a58a7125f3ee6d08bec5bfef985a0eac1}

compute dot product between vector1 and vector2, appointed by their indices

#### Parameters
* `vec_idx1` index of first vector 

* `df` DotFeatures (of same kind) to compute dot product with 

* `vec_idx2` index of second vector

#### `public template<>`  <br/>`virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`dense_dot`](#classshogun_1_1CSparseFeatures_1aa8f01741b4e4abf9428a3441d5e01572)`(int32_t vec_idx1,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * vec2,int32_t vec2_len)` {#classshogun_1_1CSparseFeatures_1aa8f01741b4e4abf9428a3441d5e01572}

compute dot product between vector1 and a dense vector

#### Parameters
* `vec_idx1` index of first vector 

* `vec2` pointer to real valued vector 

* `vec2_len` length of real valued vector

#### `public template<>`  <br/>`virtual bool `[`get_next_feature`](#classshogun_1_1CSparseFeatures_1aaa606c5e0c9dae930acdab018ee1f462)`(int32_t & index,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` & value,void * iterator)` {#classshogun_1_1CSparseFeatures_1aaa606c5e0c9dae930acdab018ee1f462}

iterate over the non-zero features

call this function with the iterator returned by get_feature_iterator and call free_feature_iterator to cleanup

#### Parameters
* `index` is returned by reference (-1 when not available) 

* `value` is returned by reference 

* `iterator` as returned by get_feature_iterator 

#### Returns
true if a new non-zero feature got returned

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`dense_dot_sgvec`](#classshogun_1_1CDotFeatures_1ab7d8fd6dbd49dd8bf718c52f48739270)`(int32_t vec_idx1,const `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > vec2)` {#classshogun_1_1CDotFeatures_1ab7d8fd6dbd49dd8bf718c52f48739270}

compute dot product between vector1 and a dense vector

#### Parameters
* `vec_idx1` index of first vector 

* `vec2` dense vector

#### `public virtual void `[`dense_dot_range`](#classshogun_1_1CDotFeatures_1aa42ca5ff67f737f667b744f3aaaa2c09)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * output,int32_t start,int32_t stop,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * alphas,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * vec,int32_t dim,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` b)` {#classshogun_1_1CDotFeatures_1aa42ca5ff67f737f667b744f3aaaa2c09}

Compute the dot product for a range of vectors. This function makes use of dense_dot alphas[i] * sparse[i]^T * w + b

#### Parameters
* `output` result for the given vector range 

* `start` start vector range from this idx 

* `stop` stop vector range at this idx 

* `alphas` scalars to multiply with, may be NULL 

* `vec` dense vector to compute dot product with 

* `dim` length of the dense vector 

* `b` bias

note that the result will be written to output[0...(stop-start-1)]

#### `public virtual void `[`dense_dot_range_subset`](#classshogun_1_1CDotFeatures_1ad60b812407a0f68110ce5b2e968b05da)`(int32_t * sub_index,int32_t num,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * output,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * alphas,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * vec,int32_t dim,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` b)` {#classshogun_1_1CDotFeatures_1ad60b812407a0f68110ce5b2e968b05da}

Compute the dot product for a subset of vectors. This function makes use of dense_dot alphas[i] * sparse[i]^T * w + b

#### Parameters
* `sub_index` index for which to compute outputs 

* `num` length of index 

* `output` result for the given vector range 

* `alphas` scalars to multiply with, may be NULL 

* `vec` dense vector to compute dot product with 

* `dim` length of the dense vector 

* `b` bias

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_combined_feature_weight`](#classshogun_1_1CDotFeatures_1aded91b11393d1add2d2bc112bd3eb5f7)`()` {#classshogun_1_1CDotFeatures_1aded91b11393d1add2d2bc112bd3eb5f7}

get combined feature weight

#### Returns
combined feature weight

#### `public inline void `[`set_combined_feature_weight`](#classshogun_1_1CDotFeatures_1acdef16d18b5739e57eb089c0acbb843b)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` nw)` {#classshogun_1_1CDotFeatures_1acdef16d18b5739e57eb089c0acbb843b}

set combined kernel weight

#### Parameters
* `nw` new combined feature weight

#### `public `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_computed_dot_feature_matrix`](#classshogun_1_1CDotFeatures_1a5c737a3c973bf08b30f9e43c56a6efa4)`()` {#classshogun_1_1CDotFeatures_1a5c737a3c973bf08b30f9e43c56a6efa4}

compute the feature matrix in feature space

#### Returns
computed feature matrix

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_computed_dot_feature_vector`](#classshogun_1_1CDotFeatures_1a28c4e362056c07a3a47bfcd5aa8f90f9)`(int32_t num)` {#classshogun_1_1CDotFeatures_1a28c4e362056c07a3a47bfcd5aa8f90f9}

compute the feature vector in feature space

#### Returns
computed feature vector

#### `public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_mean`](#classshogun_1_1CDotFeatures_1a92d96916c774173e59d8a960648ebd78)`()` {#classshogun_1_1CDotFeatures_1a92d96916c774173e59d8a960648ebd78}

get mean

#### Returns
mean returned

#### `public virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_cov`](#classshogun_1_1CDotFeatures_1a5796ce37031e0fd989686840e26b276e)`(bool copy_data_for_speed)` {#classshogun_1_1CDotFeatures_1a5796ce37031e0fd989686840e26b276e}

get covariance

#### Parameters
* `copy_data_for_speed` if true, the method stores explicitly the centered data matrix and the covariance is calculated by matrix product of the centered data with its transpose, this make it possible to take advantage of multithreaded matrix product, this may not be possible if the data doesn't fit into memory, in such case set this parameter to false to compute iteratively the covariance matrix without storing the centered data. [default = true] 

#### Returns
covariance

#### `public inline virtual `[`Range`](#classshogun_1_1Range)`< int32_t > `[`index_iterator`](#classshogun_1_1CFeatures_1a71bb6f4167a24d55e8e12fca77baabcd)`() const` {#classshogun_1_1CFeatures_1a71bb6f4167a24d55e8e12fca77baabcd}

returns an iterator of indices from 0 to [CFeatures::get_num_vectors](#classshogun_1_1CFeatures_1a91f8bf82dad4bb05accdc606d85a0da3)

Should be used in algorithms in the following way: 
```cpp
for (auto idx : features->index_iterator()) { ... }
```

#### `public virtual void `[`add_preprocessor`](#classshogun_1_1CFeatures_1a53d5b6b17d8e4b44117d404b119faca6)`(`[`CPreprocessor`](#classshogun_1_1CPreprocessor)` * p)` {#classshogun_1_1CFeatures_1a53d5b6b17d8e4b44117d404b119faca6}

add preprocessor

#### Parameters
* `p` preprocessor to set

#### `public virtual void `[`del_preprocessor`](#classshogun_1_1CFeatures_1af2ad4fb4c64ea892dc73a288f1be27a2)`(int32_t num)` {#classshogun_1_1CFeatures_1af2ad4fb4c64ea892dc73a288f1be27a2}

delete preprocessor from list

#### Parameters
* `num` index of preprocessor in list

#### `public `[`CPreprocessor`](#classshogun_1_1CPreprocessor)` * `[`get_preprocessor`](#classshogun_1_1CFeatures_1a16a2c185a1d7059892ef6ffb2d09f19b)`(int32_t num) const` {#classshogun_1_1CFeatures_1a16a2c185a1d7059892ef6ffb2d09f19b}

get specified preprocessor

#### Parameters
* `num` index of preprocessor in list

#### `public int32_t `[`get_num_preprocessors`](#classshogun_1_1CFeatures_1aa1b9b05b4535ba2c8c888aa107321c54)`() const` {#classshogun_1_1CFeatures_1aa1b9b05b4535ba2c8c888aa107321c54}

get number of preprocessors

#### Returns
number of preprocessors

#### `public void `[`clean_preprocessors`](#classshogun_1_1CFeatures_1aa6b20826d18617fc3bc0482c73908fb2)`()` {#classshogun_1_1CFeatures_1aa6b20826d18617fc3bc0482c73908fb2}

clears all preprocs

#### `public void `[`list_preprocessors`](#classshogun_1_1CFeatures_1a476493a28014c60a6006106f3d846147)`()` {#classshogun_1_1CFeatures_1a476493a28014c60a6006106f3d846147}

print preprocessors

#### `public int32_t `[`get_cache_size`](#classshogun_1_1CFeatures_1a6b599085eff3dab5a66cce6f133ae47e)`() const` {#classshogun_1_1CFeatures_1a6b599085eff3dab5a66cce6f133ae47e}

get cache size

#### Returns
cache size

#### `public virtual bool `[`reshape`](#classshogun_1_1CFeatures_1ad2a12e099e61e61e3872253a13cc0287)`(int32_t num_features,int32_t num_vectors)` {#classshogun_1_1CFeatures_1ad2a12e099e61e61e3872253a13cc0287}

in case there is a feature matrix allow for reshaping

NOT IMPLEMENTED!

#### Parameters
* `num_features` new number of features 

* `num_vectors` new number of vectors 

#### Returns
if reshaping was successful

#### `public void `[`list_feature_obj`](#classshogun_1_1CFeatures_1aff469383824e5b8736c191cd4e4476b7)`() const` {#classshogun_1_1CFeatures_1aff469383824e5b8736c191cd4e4476b7}

list feature object

#### `public bool `[`check_feature_compatibility`](#classshogun_1_1CFeatures_1a7fe9c8b9c4e4474b1893f837ea29fa21)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * f) const` {#classshogun_1_1CFeatures_1a7fe9c8b9c4e4474b1893f837ea29fa21}

check feature compatibility

#### Parameters
* `f` features to check for compatibility 

#### Returns
if features are compatible

#### `public bool `[`has_property`](#classshogun_1_1CFeatures_1af181de39b142f32c3bb00a19bea32bcc)`(`[`EFeatureProperty`](#namespaceshogun_1add4a728b32cf3898a63b2ef4564c1925)` p) const` {#classshogun_1_1CFeatures_1af181de39b142f32c3bb00a19bea32bcc}

check if features have given property

#### Parameters
* `p` feature property 

#### Returns
if features have given property

#### `public void `[`set_property`](#classshogun_1_1CFeatures_1a732ec5df91b2d7d80ae25a79fe068055)`(`[`EFeatureProperty`](#namespaceshogun_1add4a728b32cf3898a63b2ef4564c1925)` p)` {#classshogun_1_1CFeatures_1a732ec5df91b2d7d80ae25a79fe068055}

set property

#### Parameters
* `p` kernel property to set

#### `public void `[`unset_property`](#classshogun_1_1CFeatures_1affaad72e745ecc61e93d676d78705b1e)`(`[`EFeatureProperty`](#namespaceshogun_1add4a728b32cf3898a63b2ef4564c1925)` p)` {#classshogun_1_1CFeatures_1affaad72e745ecc61e93d676d78705b1e}

unset property

#### Parameters
* `p` kernel property to unset

#### `public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`create_merged_copy`](#classshogun_1_1CFeatures_1abba142f59793094f4f324787d43e0b4e)`(`[`CList`](#classshogun_1_1CList)` * others) const` {#classshogun_1_1CFeatures_1abba142f59793094f4f324787d43e0b4e}

Takes a list of feature instances and returns a new instance being a concatenation of a copy of this instace's data and the given instancess data. Note that the feature types have to be equal.

NOT IMPLEMENTED!

#### Parameters
* `others` list of feature objects to append 

#### Returns
new feature object which contains copy of data of this instance and given ones

#### `public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`create_merged_copy`](#classshogun_1_1CFeatures_1aef378f04b4eb3b6a21752a5400260769)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * other) const` {#classshogun_1_1CFeatures_1aef378f04b4eb3b6a21752a5400260769}

Convenience method for method with same name and list as parameter.

NOT IMPLEMENTED!

#### Parameters
* `other` feature object to append 

#### Returns
new feature object which contains copy of data of this instance and of given one

#### `public virtual void `[`add_subset`](#classshogun_1_1CFeatures_1acb58d8008e2ef9bb83e6b5fc5fb42f71)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > subset)` {#classshogun_1_1CFeatures_1acb58d8008e2ef9bb83e6b5fc5fb42f71}

Adds a subset of indices on top of the current subsets (possibly subset of subset). Every call causes a new active index vector to be stored. Added subsets can be removed one-by-one. If this is not needed, [add_subset_in_place()](#classshogun_1_1CFeatures_1a6dabbf53b34ca64a7645191b8ea04e31) should be used (does not store intermediate index vectors)

Calls [subset_changed_post()](#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7) afterwards

#### Parameters
* `subset` subset of indices to add

#### `public virtual void `[`add_subset_in_place`](#classshogun_1_1CFeatures_1a6dabbf53b34ca64a7645191b8ea04e31)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > subset)` {#classshogun_1_1CFeatures_1a6dabbf53b34ca64a7645191b8ea04e31}

Sets/changes latest added subset. This allows to add multiple subsets with in-place memory requirements. They cannot be removed one-by-one afterwards, only the latest active can. If this is needed, use [add_subset()](#classshogun_1_1CFeatures_1acb58d8008e2ef9bb83e6b5fc5fb42f71). If no subset is active, this just adds.

Calls [subset_changed_post()](#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7) afterwards

#### Parameters
* `subset` subset of indices to replace the latest one with.

#### `public virtual void `[`remove_subset`](#classshogun_1_1CFeatures_1a5c8a113b96b3d3a2d565ed9fffeed172)`()` {#classshogun_1_1CFeatures_1a5c8a113b96b3d3a2d565ed9fffeed172}

removes that last added subset from subset stack, if existing Calls [subset_changed_post()](#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7) afterwards

#### `public virtual void `[`remove_all_subsets`](#classshogun_1_1CFeatures_1a434b4feb76767ed0adc9ccdd55a3ef61)`()` {#classshogun_1_1CFeatures_1a434b4feb76767ed0adc9ccdd55a3ef61}

removes all subsets Calls [subset_changed_post()](#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7) afterwards

#### `public virtual `[`CSubsetStack`](#classshogun_1_1CSubsetStack)` * `[`get_subset_stack`](#classshogun_1_1CFeatures_1a47944f23a63a0eed56ff3d0bba40d253)`()` {#classshogun_1_1CFeatures_1a47944f23a63a0eed56ff3d0bba40d253}

returns subset stack

#### Returns
subset stack

#### `public inline virtual void `[`subset_changed_post`](#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7)`()` {#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7}

method may be overwritten to update things that depend on subset

#### `public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`copy_dimension_subset`](#classshogun_1_1CFeatures_1ab5e4da6272e74503f9ac4405d8ac92b5)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > dims)` {#classshogun_1_1CFeatures_1ab5e4da6272e74503f9ac4405d8ac92b5}

Creates a new [CFeatures](#classshogun_1_1CFeatures) instance containing only the dimensions of the feature vector which are specified by the provided indices.

This method is needed for feature selection tasks NOT IMPLEMENTED!

#### Parameters
* `dims` indices of feature dimensions to copy 

#### Returns
new [CFeatures](#classshogun_1_1CFeatures) instance with copies of specified features

#### `public inline virtual bool `[`support_compatible_class`](#classshogun_1_1CFeatures_1a0e8af4cc2f64bde8fe2b3dd4557e9a4f)`() const` {#classshogun_1_1CFeatures_1a0e8af4cc2f64bde8fe2b3dd4557e9a4f}

does this class support compatible computation bewteen difference classes? for example, this->dot(rhs_prt), can rhs_prt be an instance of a difference class?

#### Returns
whether this class supports compatible computation

#### `public virtual bool `[`get_feature_class_compatibility`](#classshogun_1_1CFeatures_1a3f98caf024a0a4713f5201f44b71dcd6)`(`[`EFeatureClass`](#namespaceshogun_1a9e2a4d8b86b9e061779c3fdbcda57c3b)` rhs) const` {#classshogun_1_1CFeatures_1a3f98caf024a0a4713f5201f44b71dcd6}

Given a class in right hand side, does this class support compatible computation?

for example, is this->dot(rhs_prt) valid, where rhs_prt is the class in right hand side

#### Parameters
* `rhs` the class in right hand side 

#### Returns
whether this class supports compatible computation

#### `public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CFeatures_1ad3711d9770e4b96ae8e89a99c9f530f7)`(const `[`Tag`](#classshogun_1_1Tag)`< T > & _tag,const T & value)` {#classshogun_1_1CFeatures_1ad3711d9770e4b96ae8e89a99c9f530f7}

Throws an error, as features are immutable

#### `public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CSGObject_1ade486add69a3fb33395968d9ad8fc4be)`(const std::string & name,T * value)` {#classshogun_1_1CSGObject_1ade486add69a3fb33395968d9ad8fc4be}

Typed setter for an object class parameter of a [Shogun](#classShogun) base class type, identified by a name.

#### Parameters
* `name` name of the parameter 

* `value` value of the parameter

#### `public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CSGObject_1a7c9acb98546f6fab79715f3c151b0de4)`(const std::string & name,`[`Some`](#classshogun_1_1Some)`< T > value)` {#classshogun_1_1CSGObject_1a7c9acb98546f6fab79715f3c151b0de4}

Typed setter for an object class parameter of a [Shogun](#classShogun) base class type, identified by a name.

#### Parameters
* `name` name of the parameter 

* `value` value of the parameter

#### `public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CSGObject_1a21240124c06dd6296b254555e15cbf2d)`(const std::string & name,T value)` {#classshogun_1_1CSGObject_1a21240124c06dd6296b254555e15cbf2d}

Typed setter for a non-object class parameter, identified by a name.

#### Parameters
* `name` name of the parameter 

* `value` value of the parameter along with type information

#### `public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`shallow_subset_copy`](#classshogun_1_1CFeatures_1a896eb199c1413950bbf9a89226817fb4)`()` {#classshogun_1_1CFeatures_1a896eb199c1413950bbf9a89226817fb4}

#### `public int32_t `[`ref`](#classshogun_1_1CSGObject_1ab8c24b912ee57d3f2c81ecccd083582a)`()` {#classshogun_1_1CSGObject_1ab8c24b912ee57d3f2c81ecccd083582a}

increase reference counter

#### Returns
reference count

#### `public int32_t `[`ref_count`](#classshogun_1_1CSGObject_1a6401d138f63be4c245f1f556f197689d)`()` {#classshogun_1_1CSGObject_1a6401d138f63be4c245f1f556f197689d}

display reference counter

#### Returns
reference count

#### `public int32_t `[`unref`](#classshogun_1_1CSGObject_1ad99bde1a142a1c07a963169123166e01)`()` {#classshogun_1_1CSGObject_1ad99bde1a142a1c07a963169123166e01}

decrement reference counter and deallocate object if refcount is zero before or after decrementing it

#### Returns
reference count

#### `public virtual `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`shallow_copy`](#classshogun_1_1CSGObject_1a3a25f61e5062adfce5df46be45e7e8c4)`() const` {#classshogun_1_1CSGObject_1a3a25f61e5062adfce5df46be45e7e8c4}

A shallow copy. All the SGObject instance variables will be simply assigned and SG_REF-ed.

#### `public virtual `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`deep_copy`](#classshogun_1_1CSGObject_1afa9949a366159a39ab8118918b57f578)`() const` {#classshogun_1_1CSGObject_1afa9949a366159a39ab8118918b57f578}

A deep copy. All the instance variables will also be copied.

#### `public virtual bool `[`is_generic`](#classshogun_1_1CSGObject_1a6801eb416eadc35f5499a48436e1cf43)`(EPrimitiveType * generic) const` {#classshogun_1_1CSGObject_1a6801eb416eadc35f5499a48436e1cf43}

If the SGSerializable is a class template then TRUE will be returned and GENERIC is set to the type of the generic.

#### Parameters
* `generic` set to the type of the generic if returning TRUE

#### Returns
TRUE if a class template.

#### `public template<>`  <br/>`void `[`set_generic`](#classshogun_1_1CSGObject_1ad3463e866082d6707af04276ae8aa477)`()` {#classshogun_1_1CSGObject_1ad3463e866082d6707af04276ae8aa477}

set generic type to T

#### `public template<>`  <br/>`void `[`set_generic`](#classshogun_1_1CSGObject_1a9fca24ed1095acc6c52f3c5353156d74)`()` {#classshogun_1_1CSGObject_1a9fca24ed1095acc6c52f3c5353156d74}

#### `public inline EPrimitiveType `[`get_generic`](#classshogun_1_1CSGObject_1a3329cfa1654e757472c9098770635530)`() const` {#classshogun_1_1CSGObject_1a3329cfa1654e757472c9098770635530}

Returns generic type. 
#### Returns
generic type of this object

#### `public void `[`unset_generic`](#classshogun_1_1CSGObject_1aa15afe4277334593139dae884cc951e1)`()` {#classshogun_1_1CSGObject_1aa15afe4277334593139dae884cc951e1}

unset generic type

this has to be called in classes specializing a template class

#### `public virtual void `[`print_serializable`](#classshogun_1_1CSGObject_1ade3b14c2f62ba4d8f2f6422e08567ae9)`(const char * prefix)` {#classshogun_1_1CSGObject_1ade3b14c2f62ba4d8f2f6422e08567ae9}

prints registered parameters out

#### Parameters
* `prefix` prefix for members

#### `public virtual bool `[`save_serializable`](#classshogun_1_1CSGObject_1aa9787e341533c4970885ce6d3022a935)`(`[`CSerializableFile`](#classshogun_1_1CSerializableFile)` * file,const char * prefix)` {#classshogun_1_1CSGObject_1aa9787e341533c4970885ce6d3022a935}

Save this object to file.

#### Parameters
* `file` where to save the object; will be closed during returning if PREFIX is an empty string. 

* `prefix` prefix for members 

#### Returns
TRUE if done, otherwise FALSE

#### `public virtual bool `[`load_serializable`](#classshogun_1_1CSGObject_1ad67e38ad80d4152151081f838c0a13e1)`(`[`CSerializableFile`](#classshogun_1_1CSerializableFile)` * file,const char * prefix)` {#classshogun_1_1CSGObject_1ad67e38ad80d4152151081f838c0a13e1}

Load this object from file. If it will fail (returning FALSE) then this object will contain inconsistent data and should not be used!

#### Parameters
* `file` where to load from 

* `prefix` prefix for members

#### Returns
TRUE if done, otherwise FALSE

#### `public void `[`set_global_io`](#classshogun_1_1CSGObject_1a36d256e2d05357b57e83f31f7e358f69)`(`[`SGIO`](#classshogun_1_1SGIO)` * io)` {#classshogun_1_1CSGObject_1a36d256e2d05357b57e83f31f7e358f69}

set the io object

#### Parameters
* `io` io object to use

#### `public `[`SGIO`](#classshogun_1_1SGIO)` * `[`get_global_io`](#classshogun_1_1CSGObject_1ac6c994717cb550f81c70129e839ea98b)`()` {#classshogun_1_1CSGObject_1ac6c994717cb550f81c70129e839ea98b}

get the io object

#### Returns
io object

#### `public void `[`set_global_parallel`](#classshogun_1_1CSGObject_1a9543b75e320e477d12553f2aa8593e8a)`(`[`Parallel`](#classshogun_1_1Parallel)` * parallel)` {#classshogun_1_1CSGObject_1a9543b75e320e477d12553f2aa8593e8a}

set the parallel object

#### Parameters
* `parallel` parallel object to use

#### `public `[`Parallel`](#classshogun_1_1Parallel)` * `[`get_global_parallel`](#classshogun_1_1CSGObject_1a2cd3ba36c7e0ef6e5234393cc7e22bb0)`()` {#classshogun_1_1CSGObject_1a2cd3ba36c7e0ef6e5234393cc7e22bb0}

get the parallel object

#### Returns
parallel object

#### `public void `[`set_global_version`](#classshogun_1_1CSGObject_1a1ba2ee8842e30d8ceaaf5d44c567efe1)`(`[`Version`](#classshogun_1_1Version)` * version)` {#classshogun_1_1CSGObject_1a1ba2ee8842e30d8ceaaf5d44c567efe1}

set the version object

#### Parameters
* `version` version object to use

#### `public `[`Version`](#classshogun_1_1Version)` * `[`get_global_version`](#classshogun_1_1CSGObject_1a03ce854ec4f745dbe219533dc36c9e20)`()` {#classshogun_1_1CSGObject_1a03ce854ec4f745dbe219533dc36c9e20}

get the version object

#### Returns
version object

#### `public `[`SGStringList`](#classshogun_1_1SGStringList)`< char > `[`get_modelsel_names`](#classshogun_1_1CSGObject_1a730ecbf7f326b93350f00cc937e59ac0)`()` {#classshogun_1_1CSGObject_1a730ecbf7f326b93350f00cc937e59ac0}

#### Returns
vector of names of all parameters which are registered for model selection

#### `public void `[`print_modsel_params`](#classshogun_1_1CSGObject_1a8dcb739fd760f227b3fa1dc0684f762d)`()` {#classshogun_1_1CSGObject_1a8dcb739fd760f227b3fa1dc0684f762d}

prints all parameter registered for model selection and their type

#### `public char * `[`get_modsel_param_descr`](#classshogun_1_1CSGObject_1ac26fd2403c6a5c334f4a2d8094be9833)`(const char * param_name)` {#classshogun_1_1CSGObject_1ac26fd2403c6a5c334f4a2d8094be9833}

Returns description of a given parameter string, if it exists. SG_ERROR otherwise

#### Parameters
* `param_name` name of the parameter 

#### Returns
description of the parameter

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`get_modsel_param_index`](#classshogun_1_1CSGObject_1aeb1f5a55b8170409ff2a94e3a3664c05)`(const char * param_name)` {#classshogun_1_1CSGObject_1aeb1f5a55b8170409ff2a94e3a3664c05}

Returns index of model selection parameter with provided index

#### Parameters
* `param_name` name of model selection parameter 

#### Returns
index of model selection parameter with provided name, -1 if there is no such

#### `public void `[`build_gradient_parameter_dictionary`](#classshogun_1_1CSGObject_1a17f448c257ccf4083987c4670c86a967)`(`[`CMap](#classshogun_1_1CMap)< [TParameter](#structshogun_1_1TParameter) *, [CSGObject`](#classshogun_1_1CSGObject)` *> * dict)` {#classshogun_1_1CSGObject_1a17f448c257ccf4083987c4670c86a967}

Builds a dictionary of all parameters in SGObject as well of those of SGObjects that are parameters of this object. Dictionary maps parameters to the objects that own them.

#### Parameters
* `dict` dictionary of parameters to be built.

#### `public bool `[`has`](#classshogun_1_1CSGObject_1aa911ba3ef90e0b3179e0a8dc10586424)`(const std::string & name) const` {#classshogun_1_1CSGObject_1aa911ba3ef90e0b3179e0a8dc10586424}

Checks if object has a class parameter identified by a name.

#### Parameters
* `name` name of the parameter 

#### Returns
true if the parameter exists with the input name

#### `public template<>`  <br/>`inline bool `[`has`](#classshogun_1_1CSGObject_1a0ba98fe70db33bb2036e76fd4ec28e04)`(const `[`Tag`](#classshogun_1_1Tag)`< T > & tag) const` {#classshogun_1_1CSGObject_1a0ba98fe70db33bb2036e76fd4ec28e04}

Checks if object has a class parameter identified by a [Tag](#classshogun_1_1Tag).

#### Parameters
* `tag` tag of the parameter containing name and type information 

#### Returns
true if the parameter exists with the input tag

#### `public template<>`  <br/>`inline bool `[`has`](#classshogun_1_1CSGObject_1ac947804131f9937507db2da99f36e933)`(const std::string & name) const` {#classshogun_1_1CSGObject_1ac947804131f9937507db2da99f36e933}

Checks if a type exists for a class parameter identified by a name.

#### Parameters
* `name` name of the parameter 

#### Returns
true if the parameter exists with the input name and type

#### `public template<>`  <br/>`inline void `[`add`](#classshogun_1_1CSGObject_1a3b1dff76eb6397801f84101060c5956c)`(const std::string & name,T * value)` {#classshogun_1_1CSGObject_1a3b1dff76eb6397801f84101060c5956c}

Typed appender for an object class parameter of a [Shogun](#classShogun) base class type, identified by a name.

#### Parameters
* `name` name of the parameter 

* `value` value of the parameter

#### `public template<>`  <br/>`inline void `[`add`](#classshogun_1_1CSGObject_1a98738b2423f4eb9cee078924311a9e04)`(const std::string & name,`[`Some`](#classshogun_1_1Some)`< T > value)` {#classshogun_1_1CSGObject_1a98738b2423f4eb9cee078924311a9e04}

Typed appender for an object class parameter of a [Shogun](#classShogun) base class type, identified by a name.

#### Parameters
* `name` name of the parameter 

* `value` value of the parameter

#### `public `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`get`](#classshogun_1_1CSGObject_1a4de6e15966500093d2c04db29bbf4ac7)`(const std::string & name)` {#classshogun_1_1CSGObject_1a4de6e15966500093d2c04db29bbf4ac7}

Untyped getter for an object class parameter, identified by a name. Will attempt to get specified object of appropriate internal type.

#### Parameters
* `name` name of the parameter 

#### Returns
object parameter

#### `public template<>`  <br/>`inline T `[`get`](#classshogun_1_1CSGObject_1a081b48e5b14e9ff75e7e56c941870ed5)`(const `[`Tag`](#classshogun_1_1Tag)`< T > & _tag) const` {#classshogun_1_1CSGObject_1a081b48e5b14e9ff75e7e56c941870ed5}

Getter for a class parameter, identified by a [Tag](#classshogun_1_1Tag). Throws an exception if the class does not have such a parameter.

#### Parameters
* `_tag` name and type information of parameter 

#### Returns
value of the parameter identified by the input tag

#### `public template<>`  <br/>`inline T `[`get`](#classshogun_1_1CSGObject_1adeb49b89495067e83e4208d1d60bea60)`(const std::string & name) const` {#classshogun_1_1CSGObject_1adeb49b89495067e83e4208d1d60bea60}

Getter for a class parameter, identified by a name. Throws an exception if the class does not have such a parameter.

#### Parameters
* `name` name of the parameter 

#### Returns
value of the parameter corresponding to the input name and type

#### `public virtual std::string `[`to_string`](#classshogun_1_1CSGObject_1aac993ecccd3d88aafefb6b8e3caa1dee)`() const` {#classshogun_1_1CSGObject_1aac993ecccd3d88aafefb6b8e3caa1dee}

Returns string representation of the object that contains its name and parameters.

#### `public std::vector< std::string > `[`parameter_names`](#classshogun_1_1CSGObject_1a924f620b4718c3367cf5403c52a30074)`() const` {#classshogun_1_1CSGObject_1a924f620b4718c3367cf5403c52a30074}

Returns set of all parameter names of the object.

#### `public template<>`  <br/>`inline T * `[`as`](#classshogun_1_1CSGObject_1aa4cdefb81ca8c583f1c2ef0d20d8feeb)`()` {#classshogun_1_1CSGObject_1aa4cdefb81ca8c583f1c2ef0d20d8feeb}

Specializes the object to the specified type. Throws exception if the object cannot be specialized.

#### Returns
The requested type

#### `public inline `[`SGObservable`](#classshogun_1_1CSGObject_1a3f344a622ab6c3e0dd73b5dd3f7aa556)` * `[`get_parameters_observable`](#classshogun_1_1CSGObject_1a539800ba1bbe5a4260df8c5641305afc)`()` {#classshogun_1_1CSGObject_1a539800ba1bbe5a4260df8c5641305afc}

Get parameters observable 
#### Returns
RxCpp observable

#### `public void `[`subscribe_to_parameters`](#classshogun_1_1CSGObject_1aeb13a31ffeb912767b6f16f1bc1d3e61)`(`[`ParameterObserverInterface`](#classshogun_1_1ParameterObserverInterface)` * obs)` {#classshogun_1_1CSGObject_1aeb13a31ffeb912767b6f16f1bc1d3e61}

Subscribe a parameter observer to watch over params

#### `public void `[`list_observable_parameters`](#classshogun_1_1CSGObject_1aac0c9d125edd61f235eeba5efed47142)`()` {#classshogun_1_1CSGObject_1aac0c9d125edd61f235eeba5efed47142}

Print to stdout a list of observable parameters

#### `public virtual void `[`update_parameter_hash`](#classshogun_1_1CSGObject_1afd6d5beea40c6d1222d361fb706d4651)`()` {#classshogun_1_1CSGObject_1afd6d5beea40c6d1222d361fb706d4651}

Updates the hash of current parameter combination

#### `public virtual bool `[`parameter_hash_changed`](#classshogun_1_1CSGObject_1aeb270031640bb2f00ec9452c637bfbc2)`()` {#classshogun_1_1CSGObject_1aeb270031640bb2f00ec9452c637bfbc2}

#### Returns
whether parameter combination has changed since last update

#### `public virtual bool `[`equals`](#classshogun_1_1CSGObject_1afe6a79f0c2c3db09f98ebdbe23a8a5d9)`(const `[`CSGObject`](#classshogun_1_1CSGObject)` * other) const` {#classshogun_1_1CSGObject_1afe6a79f0c2c3db09f98ebdbe23a8a5d9}

Deep comparison of two objects.

#### Parameters
* `other` object to compare with 

#### Returns
true if all parameters are equal

#### `public virtual `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`clone`](#classshogun_1_1CSGObject_1a4ae46a8c294896b69fc21384f6d86fad)`()` {#classshogun_1_1CSGObject_1a4ae46a8c294896b69fc21384f6d86fad}

Creates a clone of the current object. This is done via recursively traversing all parameters, which corresponds to a deep copy. Calling equals on the cloned object always returns true although none of the memory of both objects overlaps.

#### Returns
an identical copy of the given object, which is disjoint in memory. NULL if the clone fails. Note that the returned object is SG_REF'ed

#### `protected `[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< ST > `[`sparse_feature_matrix`](#classshogun_1_1CSparseFeatures_1a7e0b7c3ad27442fa4fb39c86c8d53346) {#classshogun_1_1CSparseFeatures_1a7e0b7c3ad27442fa4fb39c86c8d53346}

array of sparse vectors of size num_vectors

#### `protected `[`CCache](#classshogun_1_1CCache)< [SGSparseVectorEntry`](#structshogun_1_1SGSparseVectorEntry)`< ST > > * `[`feature_cache`](#classshogun_1_1CSparseFeatures_1a3b6d9e774ba060c3ee9a063db7c1547e) {#classshogun_1_1CSparseFeatures_1a3b6d9e774ba060c3ee9a063db7c1547e}

feature cache

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`combined_weight`](#classshogun_1_1CDotFeatures_1a900f01e3d31c1ed4470c2972433f958d) {#classshogun_1_1CDotFeatures_1a900f01e3d31c1ed4470c2972433f958d}

feature weighting in combined dot features

#### `protected `[`CSubsetStack`](#classshogun_1_1CSubsetStack)` * `[`m_subset_stack`](#classshogun_1_1CFeatures_1ac406fc1620ad5a8714a1c34c935ae328) {#classshogun_1_1CFeatures_1ac406fc1620ad5a8714a1c34c935ae328}

subset used for index transformations

#### `protected virtual `[`SGSparseVectorEntry`](#structshogun_1_1SGSparseVectorEntry)`< ST > * `[`compute_sparse_feature_vector`](#classshogun_1_1CSparseFeatures_1a25afcb83ea08a98851a3232854f1c7f0)`(int32_t num,int32_t & len,`[`SGSparseVectorEntry`](#structshogun_1_1SGSparseVectorEntry)`< ST > * target)` {#classshogun_1_1CSparseFeatures_1a25afcb83ea08a98851a3232854f1c7f0}

compute feature vector for sample num if target is set the vector is written to target len is returned by reference

NOT IMPLEMENTED!

#### Parameters
* `num` num 

* `len` len 

* `target` target

#### `protected template<>`  <br/>`inline `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`get_sgobject_type_dispatcher`](#classshogun_1_1CSGObject_1a7de7c1e11c3d4322d74a9a8cf5cc13f1)`(const std::string & name)` {#classshogun_1_1CSGObject_1a7de7c1e11c3d4322d74a9a8cf5cc13f1}

#### `protected virtual void `[`load_serializable_pre`](#classshogun_1_1CSGObject_1a7361535fc1a8b13beb9dd0b4ac2dd790)`()` {#classshogun_1_1CSGObject_1a7361535fc1a8b13beb9dd0b4ac2dd790}

Can (optionally) be overridden to pre-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::LOAD_SERIALIZABLE_PRE is called.

#### Exceptions
* `[ShogunException](#classshogun_1_1ShogunException)` will be thrown if an error occurs.

#### `protected virtual void `[`load_serializable_post`](#classshogun_1_1CSGObject_1a4c8da771d1ddf319cabc6b9e896326f2)`()` {#classshogun_1_1CSGObject_1a4c8da771d1ddf319cabc6b9e896326f2}

Can (optionally) be overridden to post-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::LOAD_SERIALIZABLE_POST is called.

#### Exceptions
* `[ShogunException](#classshogun_1_1ShogunException)` will be thrown if an error occurs.

#### `protected virtual void `[`save_serializable_pre`](#classshogun_1_1CSGObject_1a44300a33d16909f1bf7a129d19d4ca41)`()` {#classshogun_1_1CSGObject_1a44300a33d16909f1bf7a129d19d4ca41}

Can (optionally) be overridden to pre-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::SAVE_SERIALIZABLE_PRE is called.

#### Exceptions
* `[ShogunException](#classshogun_1_1ShogunException)` will be thrown if an error occurs.

#### `protected virtual void `[`save_serializable_post`](#classshogun_1_1CSGObject_1ab63af4bfbc71bb737703e48425db1aa2)`()` {#classshogun_1_1CSGObject_1ab63af4bfbc71bb737703e48425db1aa2}

Can (optionally) be overridden to post-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::SAVE_SERIALIZABLE_POST is called.

#### Exceptions
* `[ShogunException](#classshogun_1_1ShogunException)` will be thrown if an error occurs.

#### `protected template<>`  <br/>`inline void `[`register_param`](#classshogun_1_1CSGObject_1ac0fdc76cf24d242d99d8d862475131a6)`(`[`Tag`](#classshogun_1_1Tag)`< T > & _tag,const T & value)` {#classshogun_1_1CSGObject_1ac0fdc76cf24d242d99d8d862475131a6}

Registers a class parameter which is identified by a tag. This enables the parameter to be modified by [put()](#classshogun_1_1CSGObject_1ad3711d9770e4b96ae8e89a99c9f530f7) and retrieved by [get()](#classshogun_1_1CSGObject_1a4de6e15966500093d2c04db29bbf4ac7). Parameters can be registered in the constructor of the class.

#### Parameters
* `_tag` name and type information of parameter 

* `value` value of the parameter

#### `protected template<>`  <br/>`inline void `[`register_param`](#classshogun_1_1CSGObject_1ad06fb7206a6d3cecfb21fb270cdefbc5)`(const std::string & name,const T & value)` {#classshogun_1_1CSGObject_1ad06fb7206a6d3cecfb21fb270cdefbc5}

Registers a class parameter which is identified by a name. This enables the parameter to be modified by [put()](#classshogun_1_1CSGObject_1ad3711d9770e4b96ae8e89a99c9f530f7) and retrieved by [get()](#classshogun_1_1CSGObject_1a4de6e15966500093d2c04db29bbf4ac7). Parameters can be registered in the constructor of the class.

#### Parameters
* `name` name of the parameter 

* `value` value of the parameter along with type information

#### `protected template<>`  <br/>`inline void `[`watch_param`](#classshogun_1_1CSGObject_1a430010070f8439a0b49b647fa6f60296)`(const std::string & name,T * value,`[`AnyParameterProperties`](#classshogun_1_1AnyParameterProperties)` properties)` {#classshogun_1_1CSGObject_1a430010070f8439a0b49b647fa6f60296}

Puts a pointer to some parameter into the parameter map.

#### Parameters
* `name` name of the parameter 

* `value` pointer to the parameter value 

* `properties` properties of the parameter (e.g. if model selection is supported)

#### `protected template<>`  <br/>`inline void `[`watch_param`](#classshogun_1_1CSGObject_1ad0e74133e14d5cba696532db034671ec)`(const std::string & name,T ** value,S * len,`[`AnyParameterProperties`](#classshogun_1_1AnyParameterProperties)` properties)` {#classshogun_1_1CSGObject_1ad0e74133e14d5cba696532db034671ec}

Puts a pointer to some parameter array into the parameter map.

#### Parameters
* `name` name of the parameter array 

* `value` pointer to the first element of the parameter array 

* `len` number of elements in the array 

* `properties` properties of the parameter (e.g. if model selection is supported)

#### `protected template<>`  <br/>`inline void `[`watch_param`](#classshogun_1_1CSGObject_1a7e9db200a31d2d1faaca5a83828aeee5)`(const std::string & name,T ** value,S * rows,S * cols,`[`AnyParameterProperties`](#classshogun_1_1AnyParameterProperties)` properties)` {#classshogun_1_1CSGObject_1a7e9db200a31d2d1faaca5a83828aeee5}

Puts a pointer to some 2d parameter array (i.e. a matrix) into the parameter map.

#### Parameters
* `name` name of the parameter array 

* `value` pointer to the first element of the parameter array 

* `rows` number of rows in the array 

* `cols` number of columns in the array 

* `properties` properties of the parameter (e.g. if model selection is supported)

#### `protected template<>`  <br/>`inline void `[`watch_method`](#classshogun_1_1CSGObject_1ad4c5a49c32b7640f955bd3c2ca844b8f)`(const std::string & name,T(S::*)() const method)` {#classshogun_1_1CSGObject_1ad4c5a49c32b7640f955bd3c2ca844b8f}

Puts a pointer to a (lazily evaluated) function into the parameter map.

#### Parameters
* `name` name of the parameter 

* `method` pointer to the method

#### `protected virtual `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`create_empty`](#classshogun_1_1CSGObject_1adf79c57eee99ece954548a61ca38cd80)`() const` {#classshogun_1_1CSGObject_1adf79c57eee99ece954548a61ca38cd80}

Returns an empty instance of own type.

When inheriting from [CSGObject](#classshogun_1_1CSGObject) from outside the main source tree (i.e. customized classes, or in a unit test), then this method has to be overloaded manually to return an empty instance. [Shogun](#classShogun) can only instantiate empty class instances from its source tree.

#### Returns
empty instance of own type

#### `protected void `[`observe`](#classshogun_1_1CSGObject_1ab7f66a33081e42252d9c0bb971bbb019)`(const `[`ObservedValue`](#classshogun_1_1ObservedValue)` value)` {#classshogun_1_1CSGObject_1ab7f66a33081e42252d9c0bb971bbb019}

Observe a parameter value and emit them to observer. 
#### Parameters
* `value` Observed parameter's value

#### `protected void `[`register_observable_param`](#classshogun_1_1CSGObject_1a0fe3525aebc1dd5896191740320e20cd)`(const std::string & name,const `[`SG_OBS_VALUE_TYPE`](#namespaceshogun_1adcef34436f03207dcc3b97db8b4794d9)` type,const std::string & description)` {#classshogun_1_1CSGObject_1a0fe3525aebc1dd5896191740320e20cd}

Register which params this object can emit. 
#### Parameters
* `name` the param name 

* `type` the param type 

* `description` a user oriented description

#### `typedef `[`SGSubject`](#classshogun_1_1CSGObject_1a52509313192ce488ae91f9d7e2b16267) {#classshogun_1_1CSGObject_1a52509313192ce488ae91f9d7e2b16267}

Definition of observed subject

#### `typedef `[`SGObservable`](#classshogun_1_1CSGObject_1a3f344a622ab6c3e0dd73b5dd3f7aa556) {#classshogun_1_1CSGObject_1a3f344a622ab6c3e0dd73b5dd3f7aa556}

Definition of observable

#### `typedef `[`SGSubscriber`](#classshogun_1_1CSGObject_1a658eb47ba606529e8ffc5090d36e34e8) {#classshogun_1_1CSGObject_1a658eb47ba606529e8ffc5090d36e34e8}

Definition of subscriber

