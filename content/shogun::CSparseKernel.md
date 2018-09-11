---
classname: "shogun::CSparseKernel"
type: "class"
parents:
   - CKernel
---

# class `shogun::CSparseKernel` {#classshogun_1_1CSparseKernel}

```
class shogun::CSparseKernel
  : public CKernel
```

Template class SparseKernel, is the base class of kernels working on sparse features.

See e.g. the CSparseGaussianKernel for an example.

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
`public inline  `[`CSparseKernel`](#classshogun_1_1CSparseKernel_1a31ed9391bc537f45f72c0bd9c50db8e2)`(int32_t cachesize)` | constructor
`public inline  `[`CSparseKernel`](#classshogun_1_1CSparseKernel_1aaa36dc7d789b5c33ed8e5f22dd94bf87)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * l,`[`CFeatures`](#classshogun_1_1CFeatures)` * r)` | constructor
`public inline virtual bool `[`init`](#classshogun_1_1CSparseKernel_1abbc0c5c395db2eef959417242bf5853e)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * l,`[`CFeatures`](#classshogun_1_1CFeatures)` * r)` | initialize kernel
`public inline virtual `[`EFeatureClass`](#namespaceshogun_1a9e2a4d8b86b9e061779c3fdbcda57c3b)` `[`get_feature_class`](#classshogun_1_1CSparseKernel_1a8d0329d5baef949e5c640bb18ff7aae5)`()` | return feature class the kernel can deal with
`public virtual `[`EFeatureType`](#namespaceshogun_1a064eec90e91f56435546d77f38c0b618)` `[`get_feature_type`](#classshogun_1_1CSparseKernel_1ac6916b730dc608dbccb96cd1b0bfa528)`()` | return feature type the kernel can deal with
`public inline virtual const char * `[`get_name`](#classshogun_1_1CSparseKernel_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` | Returns the name of the SGSerializable instance. It MUST BE the CLASS NAME without the prefixed `C'.
`public `[`EKernelType`](#namespaceshogun_1abd72ef8a797cb6f894866dff8586dbe2)` `[`get_kernel_type`](#classshogun_1_1CSparseKernel_1a3bbc33d28d407d2f5d76bfa102095a6d)`()` | return what type of kernel we are, e.g. Linear,Polynomial, Gaussian,...
`public template<>`  <br/>`inline virtual `[`EFeatureType`](#namespaceshogun_1a064eec90e91f56435546d77f38c0b618)` `[`get_feature_type`](#classshogun_1_1CSparseKernel_1a5c2663373829bede6e18ef9f655b8fd3)`()` | return feature type the kernel can deal with
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`kernel`](#classshogun_1_1CKernel_1aa62dbbae3e63a09350f4eda6acacb03c)`(int32_t idx_a,int32_t idx_b)` | get kernel function for lhs feature vector a and rhs feature vector b
`public inline `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_kernel_matrix`](#classshogun_1_1CKernel_1a731a6b48f9c6f9298f4962d46dae374d)`()` | get kernel matrix
`public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`get_kernel_matrix`](#classshogun_1_1CKernel_1af8aa689d45bb4dcf861169744ef7c100)`()` | get kernel matrix (templated)
`public inline `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_kernel_diagonal`](#classshogun_1_1CKernel_1a449d331d9088d0c6cde4d2300e8e580e)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > preallocated)` | #### Returns
`public inline virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_kernel_col`](#classshogun_1_1CKernel_1a56c2d85a003ced70897263138745b29c)`(int32_t j)` | get column j
`public inline virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_kernel_row`](#classshogun_1_1CKernel_1a312dae761350d98f6a6a4283277836a5)`(int32_t i)` | get row i
`public void `[`get_kernel_row`](#classshogun_1_1CKernel_1acbcd848290e6cac1784878c1ca1927b4)`(int32_t docnum,int32_t * active2dnum,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * buffer,bool full_line)` | get kernel row
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`sum_symmetric_block`](#classshogun_1_1CKernel_1ac9b728569d9187d41be07ed9a0dadc6c)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_begin,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_size,bool no_diag)` | Computes sum from a symmetric part of the kernel matrix that always is supposed to contain the main upper diagonal. This method is useful while computing statistical estimation of mean/variance over kernel values but the kernel matrix is too huge to be fit inside memory.
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`sum_block`](#classshogun_1_1CKernel_1aa55981e8bdd935ed1796b8db2c39d2f9)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_begin_row,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_begin_col,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_size_row,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_size_col,bool no_diag)` | Computes sum of kernel values from a specified block. This method is useful while computing statistical estimation of mean/variance over kernel values but the kernel matrix is too huge to be fit inside memory.
`public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`row_wise_sum_symmetric_block`](#classshogun_1_1CKernel_1a47c35bee65870513a3ea376c3ae74163)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_begin,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_size,bool no_diag)` | Computes row-wise/col-wise sum from a symmetric part of the kernel matrix that always is supposed to contain the main upper diagonal. This method is useful while computing statistical estimation of mean/variance over kernel values but the kernel matrix is too huge to be fit inside memory.
`public virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`row_wise_sum_squared_sum_symmetric_block`](#classshogun_1_1CKernel_1ae717558a9f96fa987dac46b2e9d5c7da)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_begin,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_size,bool no_diag)` | Computes row-wise/col-wise sum and squared sum of kernel values from a symmetric part of the kernel matrix that always is supposed to contain the main upper diagonal. This method is useful while computing statistical estimation of mean/variance over kernel values but the kernel matrix is too huge to be fit inside memory.
`public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`row_col_wise_sum_block`](#classshogun_1_1CKernel_1ab6b675e22517e46914e70adaf90e6b8c)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_begin_row,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_begin_col,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_size_row,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_size_col,bool no_diag)` | Computes row-wise/col-wise sum of kernel values. This method is useful while computing statistical estimation of mean/variance over kernel values but the kernel matrix is too huge to be fit inside memory.
`public virtual bool `[`set_normalizer`](#classshogun_1_1CKernel_1a7b4b54a6b18761a5fc2e00080d65f2a6)`(`[`CKernelNormalizer`](#classshogun_1_1CKernelNormalizer)` * normalizer)` | set the current kernel normalizer
`public virtual `[`CKernelNormalizer`](#classshogun_1_1CKernelNormalizer)` * `[`get_normalizer`](#classshogun_1_1CKernel_1abcba15494b772139077b7e71db562e58)`()` | obtain the current kernel normalizer
`public virtual bool `[`init_normalizer`](#classshogun_1_1CKernel_1aa7df874ba16e360949f66100aad43e23)`()` | initialize the current kernel normalizer 
`public virtual void `[`cleanup`](#classshogun_1_1CKernel_1a4b66d5e31b5dc18b314c8a68163263bd)`()` | clean up your kernel
`public void `[`load`](#classshogun_1_1CKernel_1a5d33ec59a4be25056cca1f3b6691ad00)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` | load the kernel matrix
`public void `[`save`](#classshogun_1_1CKernel_1a2ec11d78c7f60dfbc77bc2f56d211033)`(`[`CFile`](#classshogun_1_1CFile)` * writer)` | save kernel matrix
`public inline `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`get_lhs`](#classshogun_1_1CKernel_1aa3e521f9c3df80da4bc44c2ba0b6c0be)`()` | get left-hand side of features used in kernel
`public inline `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`get_rhs`](#classshogun_1_1CKernel_1a28c50c34fc59a74f2b015ba87dc133d9)`()` | get right-hand side of features used in kernel
`public inline virtual int32_t `[`get_num_vec_lhs`](#classshogun_1_1CKernel_1af81140e34d38612802e1b8783424260a)`()` | get number of vectors of lhs features
`public inline virtual int32_t `[`get_num_vec_rhs`](#classshogun_1_1CKernel_1aabc415a305914c27567a1343f7957cac)`()` | get number of vectors of rhs features
`public inline virtual bool `[`has_features`](#classshogun_1_1CKernel_1abcd71e362bf0042668c5527e17968fe6)`()` | test whether features have been assigned to lhs and rhs
`public inline bool `[`get_lhs_equals_rhs`](#classshogun_1_1CKernel_1a79527726c2f525e4236e186d77a63849)`()` | test whether features on lhs and rhs are the same
`public virtual void `[`remove_lhs_and_rhs`](#classshogun_1_1CKernel_1a69d2fffafdc0984cea96e3f4a4f737cb)`()` | remove lhs and rhs from kernel
`public virtual void `[`remove_lhs`](#classshogun_1_1CKernel_1a214e795fd785274e29d97d4b16aa6fc4)`()` | remove lhs from kernel
`public virtual void `[`remove_rhs`](#classshogun_1_1CKernel_1af6c99208795e1ff43d204e3e5adb78ec)`()` | takes all necessary steps if the rhs is removed from kernel
`public inline void `[`set_cache_size`](#classshogun_1_1CKernel_1ae5c0887476ce715d70b0bdf837c277b7)`(int32_t size)` | set the size of the kernel cache
`public inline int32_t `[`get_cache_size`](#classshogun_1_1CKernel_1a7cd5c5d069c93cc98539fcb7baff0567)`()` | return the size of the kernel cache
`public inline void `[`cache_reset`](#classshogun_1_1CKernel_1ac7acb3ba30d154651c3ab1afd9c0bc41)`()` | cache reset
`public inline int32_t `[`get_max_elems_cache`](#classshogun_1_1CKernel_1a408e958c004d1e28e90f885909a135a9)`()` | get maximum elements in cache
`public inline int32_t `[`get_activenum_cache`](#classshogun_1_1CKernel_1ae7f812236ff0dd3e44069daa0c0558e4)`()` | get activenum cache
`public void `[`cache_kernel_row`](#classshogun_1_1CKernel_1ae1ac999b5941145f254e21fba6e97240)`(int32_t x)` | cache kernel row
`public void `[`cache_multiple_kernel_rows`](#classshogun_1_1CKernel_1abdce614df171105f0eb3796fa238dbef)`(int32_t * key,int32_t varnum)` | cache multiple kernel rows
`public void `[`kernel_cache_reset_lru`](#classshogun_1_1CKernel_1a795988d5cfd87cd02cfaf8cf3ad92c3b)`()` | kernel cache reset lru
`public void `[`kernel_cache_shrink`](#classshogun_1_1CKernel_1abaf9323473978dc5159541b5458226c0)`(int32_t totdoc,int32_t num_shrink,int32_t * after)` | kernel cache shrink
`public void `[`resize_kernel_cache`](#classshogun_1_1CKernel_1af3e54d2ca0a3c2bfe30905eeab6a5e88)`(`[`KERNELCACHE_IDX`](#namespaceshogun_1a80ec34b03eaf01338e02ebd002ded245)` size,bool regression_hack)` | resize kernel cache
`public inline void `[`set_time`](#classshogun_1_1CKernel_1aafee0a28cbbf03c56b988736382c5e3f)`(int32_t t)` | set the lru time
`public inline int32_t `[`kernel_cache_touch`](#classshogun_1_1CKernel_1a222e848c2960c2e74ff00ee0182ce8e9)`(int32_t cacheidx)` | update lru time of item at given index to avoid removal from cache
`public inline int32_t `[`kernel_cache_check`](#classshogun_1_1CKernel_1a387fbc5855ff829980ae52f0eb295b62)`(int32_t cacheidx)` | check if row at given index is cached
`public inline int32_t `[`kernel_cache_space_available`](#classshogun_1_1CKernel_1a8261cb96381df464c9d9d63537224a16)`()` | check if there is room for one more row in kernel cache
`public void `[`kernel_cache_init`](#classshogun_1_1CKernel_1a6550676493b70dc4bfd4c7ce865f0aaf)`(int32_t size,bool regression_hack)` | initialize kernel cache
`public void `[`kernel_cache_cleanup`](#classshogun_1_1CKernel_1a4c7e6d6e223aa13629e241c804a34694)`()` | cleanup kernel cache
`public void `[`list_kernel`](#classshogun_1_1CKernel_1a2c56cf3c1a9b6fb1a66ea83bb0b89e6d)`()` | list kernel
`public inline virtual bool `[`has_property`](#classshogun_1_1CKernel_1a535b6b6715d5957b004af00a5a8b1858)`(`[`EKernelProperty`](#namespaceshogun_1a3280191ade233d4393b7b6181dcec00c)` p)` | check if kernel has given property
`public virtual void `[`clear_normal`](#classshogun_1_1CKernel_1ac86fdff79b1cdfa071d4e56edfae178c)`()` | for optimizable kernels, i.e. kernels where the weight vector can be computed explicitly (if it fits into memory)
`public virtual void `[`add_to_normal`](#classshogun_1_1CKernel_1a881dcf9c3c9bb8940eb5b625e8e18860)`(int32_t vector_idx,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` weight)` | add vector*factor to 'virtual' normal vector
`public inline `[`EOptimizationType`](#namespaceshogun_1a0864e2ed51fdcd3fe0fac7f7d0429cbc)` `[`get_optimization_type`](#classshogun_1_1CKernel_1a231c6ef0246fd030129378ce4aa2ff23)`()` | get optimization type
`public inline virtual void `[`set_optimization_type`](#classshogun_1_1CKernel_1a0115f60f8d9d977dec2a2fd72fd50c7b)`(`[`EOptimizationType`](#namespaceshogun_1a0864e2ed51fdcd3fe0fac7f7d0429cbc)` t)` | set optimization type
`public inline bool `[`get_is_initialized`](#classshogun_1_1CKernel_1ac7083cb2099c1de0a702f53665c7e256)`()` | check if optimization is initialized
`public virtual bool `[`init_optimization`](#classshogun_1_1CKernel_1a8b5139637c80888fb957da9e78262930)`(int32_t count,int32_t * IDX,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * weights)` | initialize optimization
`public virtual bool `[`delete_optimization`](#classshogun_1_1CKernel_1adbfd9c323b8f18e99a724e9d31de082c)`()` | delete optimization
`public bool `[`init_optimization_svm`](#classshogun_1_1CKernel_1a033a692905152791779c2db666a508b2)`(`[`CSVM`](#classshogun_1_1CSVM)` * svm)` | initialize optimization
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_optimized`](#classshogun_1_1CKernel_1af6e91433913335a43a418c32e5add461)`(int32_t vector_idx)` | compute optimized
`public virtual void `[`compute_batch`](#classshogun_1_1CKernel_1abbbe72b9a886d60eade98489d6ffa273)`(int32_t num_vec,int32_t * vec_idx,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * target,int32_t num_suppvec,int32_t * IDX,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * alphas,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` factor)` | computes output for a batch of examples in an optimized fashion (favorable if kernel supports it, i.e. has KP_BATCHEVALUATION. to the outputvector target (of length num_vec elements) the output for the examples enumerated in vec_idx are added. therefore make sure that it is initialized with ZERO. the following num_suppvec, IDX, alphas arguments are the number of support vectors, their indices and weights
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_combined_kernel_weight`](#classshogun_1_1CKernel_1aca8b2ae0268d160ab41531ed8bfea849)`()` | get combined kernel weight
`public inline void `[`set_combined_kernel_weight`](#classshogun_1_1CKernel_1a7abf31f4bf05f91f3fe724dc20f4dba5)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` nw)` | set combined kernel weight
`public virtual int32_t `[`get_num_subkernels`](#classshogun_1_1CKernel_1a462e89b5ef214f1460057fe65c91993b)`()` | get number of subkernels
`public virtual void `[`compute_by_subkernel`](#classshogun_1_1CKernel_1a6238f812ab53a3ae36e176a303fb205a)`(int32_t vector_idx,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * subkernel_contrib)` | compute by subkernel
`public virtual const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`get_subkernel_weights`](#classshogun_1_1CKernel_1a55ee24f23e9819656501c3bffefe1063)`(int32_t & num_weights)` | get subkernel weights
`public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_subkernel_weights`](#classshogun_1_1CKernel_1adb9aa3ff6a6ad8fd0bd84ffa7db2e459)`()` | get subkernel weights (swig compatible)
`public virtual void `[`set_subkernel_weights`](#classshogun_1_1CKernel_1a65ebc4353804603d7b630e54050d90ed)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > weights)` | set subkernel weights
`public inline virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_parameter_gradient`](#classshogun_1_1CKernel_1ac1d79ae65ddb803f672223f8c61cffde)`(const `[`TParameter`](#structshogun_1_1TParameter)` * param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index)` | return derivative with respect to specified parameter
`public inline virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_parameter_gradient_diagonal`](#classshogun_1_1CKernel_1a2f0b7215dd7ef0628d43d67ef360369a)`(const `[`TParameter`](#structshogun_1_1TParameter)` * param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index)` | return diagonal part of derivative with respect to specified parameter
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
`public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CSGObject_1ad3711d9770e4b96ae8e89a99c9f530f7)`(const `[`Tag`](#classshogun_1_1Tag)`< T > & _tag,const T & value)` | Setter for a class parameter, identified by a [Tag](#classshogun_1_1Tag). Throws an exception if the class does not have such a parameter.
`public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CSGObject_1ade486add69a3fb33395968d9ad8fc4be)`(const std::string & name,T * value)` | Typed setter for an object class parameter of a [Shogun](#classShogun) base class type, identified by a name.
`public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CSGObject_1a7c9acb98546f6fab79715f3c151b0de4)`(const std::string & name,`[`Some`](#classshogun_1_1Some)`< T > value)` | Typed setter for an object class parameter of a [Shogun](#classShogun) base class type, identified by a name.
`public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CSGObject_1a21240124c06dd6296b254555e15cbf2d)`(const std::string & name,T value)` | Typed setter for a non-object class parameter, identified by a name.
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
`protected int32_t `[`cache_size`](#classshogun_1_1CKernel_1a05f0572d7f5c701ff73f186b45a1d815) | cache_size in MB
`protected KERNEL_CACHE `[`kernel_cache`](#classshogun_1_1CKernel_1a49c6c2cecb82271cf4bc3ea2f552913e) | kernel cache
`protected `[`KERNELCACHE_ELEM`](#namespaceshogun_1ab6286d846462ad5d8abee6a985150754)` * `[`kernel_matrix`](#classshogun_1_1CKernel_1a171add209887a004b5b06e4f839947e2) | this *COULD* store the whole kernel matrix usually not applicable / necessary to compute the whole matrix
`protected `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`lhs`](#classshogun_1_1CKernel_1a5bb6375a26075c34dc856a477828ad52) | feature vectors to occur on left hand side
`protected `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`rhs`](#classshogun_1_1CKernel_1a8e375dd40df7b063ba9f2da598e1a3a9) | feature vectors to occur on right hand side
`protected bool `[`lhs_equals_rhs`](#classshogun_1_1CKernel_1afda5656b0c2b69ca8ee7a6a6bc1758ff) | lhs
`protected int32_t `[`num_lhs`](#classshogun_1_1CKernel_1ac6a6d53fdb5fd47fffd56b1b03d41e09) | number of feature vectors on left hand side
`protected int32_t `[`num_rhs`](#classshogun_1_1CKernel_1a84e7d5029b76c7b2b5903c6600adc036) | number of feature vectors on right hand side
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`combined_kernel_weight`](#classshogun_1_1CKernel_1a742203c256bc90e4fcc329eebe7d02a9) | combined kernel weight
`protected bool `[`optimization_initialized`](#classshogun_1_1CKernel_1a9948eae33d1441baa52cb9f0943d250a) | if optimization is initialized
`protected `[`EOptimizationType`](#namespaceshogun_1a0864e2ed51fdcd3fe0fac7f7d0429cbc)` `[`opt_type`](#classshogun_1_1CKernel_1a10d9465919ff381c40f0a308746a3dee) | optimization type (currently FASTBUTMEMHUNGRY and SLOWBUTMEMEFFICIENT)
`protected uint64_t `[`properties`](#classshogun_1_1CKernel_1a07267159f65dd3ece9cfd00bbaf1c99c) | kernel properties
`protected `[`CKernelNormalizer`](#classshogun_1_1CKernelNormalizer)` * `[`normalizer`](#classshogun_1_1CKernel_1aa98b2c40e3a7b7c76e35b58df4570022) | normalize the kernel(i,j) function based on this normalization function
`protected inline void `[`set_property`](#classshogun_1_1CKernel_1a9124fc95acc6a5a8b8006539b92684b8)`(`[`EKernelProperty`](#namespaceshogun_1a3280191ade233d4393b7b6181dcec00c)` p)` | set property
`protected inline void `[`unset_property`](#classshogun_1_1CKernel_1a8fc3fa0bd8870e260221708e5a1c71d3)`(`[`EKernelProperty`](#namespaceshogun_1a3280191ade233d4393b7b6181dcec00c)` p)` | unset property
`protected inline void `[`set_is_initialized`](#classshogun_1_1CKernel_1a4c62e85d1f0681dbd84ff6a15f66a864)`(bool p_init)` | set is initialized
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute`](#classshogun_1_1CKernel_1ac6a01ee581de85069a4b697db55e34b5)`(int32_t x,int32_t y)` | compute kernel function for features a and b idx_{a,b} denote the index of the feature vectors in the corresponding feature object
`protected inline int32_t `[`compute_row_start`](#classshogun_1_1CKernel_1a8476cd069409e0b64c2fe6099e07cfcb)`(int64_t offs,int32_t n,bool symmetric)` | compute row start offset for parallel kernel matrix computation
`protected virtual void `[`load_serializable_post`](#classshogun_1_1CKernel_1a4c8da771d1ddf319cabc6b9e896326f2)`()` | Can (optionally) be overridden to post-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::LOAD_SERIALIZABLE_POST is called.
`protected virtual void `[`save_serializable_pre`](#classshogun_1_1CKernel_1a44300a33d16909f1bf7a129d19d4ca41)`()` | Can (optionally) be overridden to pre-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::SAVE_SERIALIZABLE_PRE is called.
`protected virtual void `[`save_serializable_post`](#classshogun_1_1CKernel_1ab63af4bfbc71bb737703e48425db1aa2)`()` | Can (optionally) be overridden to post-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::SAVE_SERIALIZABLE_POST is called.
`protected virtual void `[`register_params`](#classshogun_1_1CKernel_1a5a7bc37cc5ce93e9444637bbd72f703e)`()` | Separate the function of parameter registration This can be the first stage of a *general* framework for cross-validation or other parameter-based operations
`protected template<>`  <br/>`inline `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`get_sgobject_type_dispatcher`](#classshogun_1_1CSGObject_1a7de7c1e11c3d4322d74a9a8cf5cc13f1)`(const std::string & name)` | 
`protected virtual void `[`load_serializable_pre`](#classshogun_1_1CSGObject_1a7361535fc1a8b13beb9dd0b4ac2dd790)`()` | Can (optionally) be overridden to pre-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::LOAD_SERIALIZABLE_PRE is called.
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

#### `public inline  `[`CSparseKernel`](#classshogun_1_1CSparseKernel_1a31ed9391bc537f45f72c0bd9c50db8e2)`(int32_t cachesize)` {#classshogun_1_1CSparseKernel_1a31ed9391bc537f45f72c0bd9c50db8e2}

constructor

#### Parameters
* `cachesize` cache size

#### `public inline  `[`CSparseKernel`](#classshogun_1_1CSparseKernel_1aaa36dc7d789b5c33ed8e5f22dd94bf87)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * l,`[`CFeatures`](#classshogun_1_1CFeatures)` * r)` {#classshogun_1_1CSparseKernel_1aaa36dc7d789b5c33ed8e5f22dd94bf87}

constructor

#### Parameters
* `l` features for left-hand side 

* `r` features for right-hand side

#### `public inline virtual bool `[`init`](#classshogun_1_1CSparseKernel_1abbc0c5c395db2eef959417242bf5853e)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * l,`[`CFeatures`](#classshogun_1_1CFeatures)` * r)` {#classshogun_1_1CSparseKernel_1abbc0c5c395db2eef959417242bf5853e}

initialize kernel

#### Parameters
* `l` features of left-hand side 

* `r` features of right-hand side 

#### Returns
if initializing was successful

#### `public inline virtual `[`EFeatureClass`](#namespaceshogun_1a9e2a4d8b86b9e061779c3fdbcda57c3b)` `[`get_feature_class`](#classshogun_1_1CSparseKernel_1a8d0329d5baef949e5c640bb18ff7aae5)`()` {#classshogun_1_1CSparseKernel_1a8d0329d5baef949e5c640bb18ff7aae5}

return feature class the kernel can deal with

#### Returns
feature class SPARSE

#### `public virtual `[`EFeatureType`](#namespaceshogun_1a064eec90e91f56435546d77f38c0b618)` `[`get_feature_type`](#classshogun_1_1CSparseKernel_1ac6916b730dc608dbccb96cd1b0bfa528)`()` {#classshogun_1_1CSparseKernel_1ac6916b730dc608dbccb96cd1b0bfa528}

return feature type the kernel can deal with

#### Returns
templated feature type

#### `public inline virtual const char * `[`get_name`](#classshogun_1_1CSparseKernel_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` {#classshogun_1_1CSparseKernel_1a9cb485686dd7a1e6f7103cf42e87717e}

Returns the name of the SGSerializable instance. It MUST BE the CLASS NAME without the prefixed `C'.

#### Returns
name of the SGSerializable

#### `public `[`EKernelType`](#namespaceshogun_1abd72ef8a797cb6f894866dff8586dbe2)` `[`get_kernel_type`](#classshogun_1_1CSparseKernel_1a3bbc33d28d407d2f5d76bfa102095a6d)`()` {#classshogun_1_1CSparseKernel_1a3bbc33d28d407d2f5d76bfa102095a6d}

return what type of kernel we are, e.g. Linear,Polynomial, Gaussian,...

abstract base method

#### Returns
kernel type

#### `public template<>`  <br/>`inline virtual `[`EFeatureType`](#namespaceshogun_1a064eec90e91f56435546d77f38c0b618)` `[`get_feature_type`](#classshogun_1_1CSparseKernel_1a5c2663373829bede6e18ef9f655b8fd3)`()` {#classshogun_1_1CSparseKernel_1a5c2663373829bede6e18ef9f655b8fd3}

return feature type the kernel can deal with

abstract base method

#### Returns
feature type

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`kernel`](#classshogun_1_1CKernel_1aa62dbbae3e63a09350f4eda6acacb03c)`(int32_t idx_a,int32_t idx_b)` {#classshogun_1_1CKernel_1aa62dbbae3e63a09350f4eda6acacb03c}

get kernel function for lhs feature vector a and rhs feature vector b

#### Parameters
* `idx_a` index of feature vector a 

* `idx_b` index of feature vector b 

#### Returns
computed kernel function

#### `public inline `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_kernel_matrix`](#classshogun_1_1CKernel_1a731a6b48f9c6f9298f4962d46dae374d)`()` {#classshogun_1_1CKernel_1a731a6b48f9c6f9298f4962d46dae374d}

get kernel matrix

#### Returns
computed kernel matrix (needs to be cleaned up)

#### `public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`get_kernel_matrix`](#classshogun_1_1CKernel_1af8aa689d45bb4dcf861169744ef7c100)`()` {#classshogun_1_1CKernel_1af8aa689d45bb4dcf861169744ef7c100}

get kernel matrix (templated)

#### Returns
the kernel matrix

#### `public inline `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_kernel_diagonal`](#classshogun_1_1CKernel_1a449d331d9088d0c6cde4d2300e8e580e)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > preallocated)` {#classshogun_1_1CKernel_1a449d331d9088d0c6cde4d2300e8e580e}

#### Returns
Vector with diagonal elements of the kernel matrix. Note that left- and right-handside features must be set and of equal size

#### Parameters
* `preallocated` vector with space for results

#### `public inline virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_kernel_col`](#classshogun_1_1CKernel_1a56c2d85a003ced70897263138745b29c)`(int32_t j)` {#classshogun_1_1CKernel_1a56c2d85a003ced70897263138745b29c}

get column j

#### Returns
the jth column of the kernel matrix

#### `public inline virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_kernel_row`](#classshogun_1_1CKernel_1a312dae761350d98f6a6a4283277836a5)`(int32_t i)` {#classshogun_1_1CKernel_1a312dae761350d98f6a6a4283277836a5}

get row i

#### Returns
the ith row of the kernel matrix

#### `public void `[`get_kernel_row`](#classshogun_1_1CKernel_1acbcd848290e6cac1784878c1ca1927b4)`(int32_t docnum,int32_t * active2dnum,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * buffer,bool full_line)` {#classshogun_1_1CKernel_1acbcd848290e6cac1784878c1ca1927b4}

get kernel row

#### Parameters
* `docnum` docnum 

* `active2dnum` active2dnum 

* `buffer` buffer 

* `full_line` full line

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`sum_symmetric_block`](#classshogun_1_1CKernel_1ac9b728569d9187d41be07ed9a0dadc6c)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_begin,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_size,bool no_diag)` {#classshogun_1_1CKernel_1ac9b728569d9187d41be07ed9a0dadc6c}

Computes sum from a symmetric part of the kernel matrix that always is supposed to contain the main upper diagonal. This method is useful while computing statistical estimation of mean/variance over kernel values but the kernel matrix is too huge to be fit inside memory.

#### Parameters
* `block_begin` the row and col index at which the block starts 

* `block_size` the number of rows and cols in the block

For example, block_begin 4 and block_size 5 represents the block that starts at index (4,4) in the kernel matrix and goes upto (4+5-1,4+5-1) i.e. (8,8) both inclusive

#### Parameters
* `no_diag` if true (default), the diagonal elements are excluded from the sum

#### Returns
sum of kernel values within the block computed as 
$$
\sum_{i}\sum_{j}k(i+\text{block-begin}, j+\text{block-begin})
$$
 where $i,j\in[0,\text{block-size}-1]$

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`sum_block`](#classshogun_1_1CKernel_1aa55981e8bdd935ed1796b8db2c39d2f9)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_begin_row,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_begin_col,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_size_row,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_size_col,bool no_diag)` {#classshogun_1_1CKernel_1aa55981e8bdd935ed1796b8db2c39d2f9}

Computes sum of kernel values from a specified block. This method is useful while computing statistical estimation of mean/variance over kernel values but the kernel matrix is too huge to be fit inside memory.

#### Parameters
* `block_begin_row` the row index at which the block starts 

* `block_begin_col` the col index at which the block starts 

* `block_size_row` the number of rows in the block 

* `block_size_col` the number of cols in the block

For example, block_begin_row 0, block_begin_col 4 and block_size_row 5, block_size_col 6 represents the block that starts at index (0,4) in the kernel matrix and goes upto (0+5-1,4+6-1) i.e. (4,9) both inclusive

#### Parameters
* `no_diag` if true (default is false), the diagonal elements are excluded from the sum, provided that block_size_row and block_size_col are same (i.e. the block is square). Otherwise, these are always added

#### Returns
sum of kernel values within the block computed as 
$$
\sum_{i}\sum_{j}k(i+\text{block-begin-row}, j+\text{block-begin-col})
$$
 where $i\in[0,\text{block-size-row}-1]$ and $j\in[0,\text{block-size-col}-1]$

#### `public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`row_wise_sum_symmetric_block`](#classshogun_1_1CKernel_1a47c35bee65870513a3ea376c3ae74163)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_begin,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_size,bool no_diag)` {#classshogun_1_1CKernel_1a47c35bee65870513a3ea376c3ae74163}

Computes row-wise/col-wise sum from a symmetric part of the kernel matrix that always is supposed to contain the main upper diagonal. This method is useful while computing statistical estimation of mean/variance over kernel values but the kernel matrix is too huge to be fit inside memory.

#### Parameters
* `block_begin` the row and col index at which the block starts 

* `block_size` the number of rows and cols in the block

For [Example](#classshogun_1_1Example), block_begin 4 and block_size 5 represents the block that starts at index (4,4) in the kernel matrix and goes upto (4+5-1,4+5-1) i.e. (8,8) both inclusive

#### Parameters
* `no_diag` if true (default), the diagonal elements are excluded from the row/col-wise sum

#### Returns
vector containing row-wise sum computed as 
$$
v[i]=\sum_{j}k(i+\text{block-begin}, j+\text{block-begin})
$$
 where $i,j\in[0,\text{block-size}-1]$

#### `public virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`row_wise_sum_squared_sum_symmetric_block`](#classshogun_1_1CKernel_1ae717558a9f96fa987dac46b2e9d5c7da)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_begin,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_size,bool no_diag)` {#classshogun_1_1CKernel_1ae717558a9f96fa987dac46b2e9d5c7da}

Computes row-wise/col-wise sum and squared sum of kernel values from a symmetric part of the kernel matrix that always is supposed to contain the main upper diagonal. This method is useful while computing statistical estimation of mean/variance over kernel values but the kernel matrix is too huge to be fit inside memory.

#### Parameters
* `block_begin` the row and col index at which the block starts 

* `block_size` the number of rows and cols in the block

For [Example](#classshogun_1_1Example), block_begin 4 and block_size 5 represents the block that starts at index (4,4) in the kernel matrix and goes upto (4+5-1,4+5-1) i.e. (8,8) both inclusive

#### Parameters
* `no_diag` if true (default), the diagonal elements are excluded from the row/col-wise sum

#### Returns
a matrix whose first column contains the row-wise sum of kernel values computed as 
$$
v_0[i]=\sum_{j}k(i+\text{block-begin}, j+\text{block-begin})
$$
 and second column contains the row-wise sum of squared kernel values 
$$
v_1[i]=\sum_{j}^k^2(i+\text{block-begin}, j+\text{block-begin})
$$
 where $i,j\in[0,\text{block-size}-1]$

#### `public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`row_col_wise_sum_block`](#classshogun_1_1CKernel_1ab6b675e22517e46914e70adaf90e6b8c)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_begin_row,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_begin_col,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_size_row,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` block_size_col,bool no_diag)` {#classshogun_1_1CKernel_1ab6b675e22517e46914e70adaf90e6b8c}

Computes row-wise/col-wise sum of kernel values. This method is useful while computing statistical estimation of mean/variance over kernel values but the kernel matrix is too huge to be fit inside memory.

#### Parameters
* `block_begin_row` the row index at which the block starts 

* `block_begin_col` the col index at which the block starts 

* `block_size_row` the number of rows in the block 

* `block_size_col` the number of cols in the block

For [Example](#classshogun_1_1Example), block_begin_row 0, block_begin_col 4 and block_size_row 5, block_size_col 6 represents the block that starts at index (0,4) in the kernel matrix and goes upto (0+5-1,4+6-1) i.e. (4,9) both inclusive

#### Parameters
* `no_diag` if true (default is false), the diagonal elements are excluded from the row/col-wise sum, provided that block_size_row and block_size_col are same (i.e. the block is square). Otherwise, these are always added

#### Returns
a vector whose first block_size_row entries contain row-wise sum of kernel values computed as 
$$
v[i]=\sum_{j}k(i+\text{block-begin-row}, j+\text{block-begin-col})
$$
 and rest block_size_col entries col-wise sum of kernel values computed as 
$$
v[\text{block-size-row}+j]=\sum_{i}k(i+\text{block-begin-row}, j+\text{block-begin-col})
$$
 where $i\in[0,\text{block-size-row}-1]$ and $j\in[0,\text{block-size-col}-1]$

#### `public virtual bool `[`set_normalizer`](#classshogun_1_1CKernel_1a7b4b54a6b18761a5fc2e00080d65f2a6)`(`[`CKernelNormalizer`](#classshogun_1_1CKernelNormalizer)` * normalizer)` {#classshogun_1_1CKernel_1a7b4b54a6b18761a5fc2e00080d65f2a6}

set the current kernel normalizer

#### Returns
if successful

#### `public virtual `[`CKernelNormalizer`](#classshogun_1_1CKernelNormalizer)` * `[`get_normalizer`](#classshogun_1_1CKernel_1abcba15494b772139077b7e71db562e58)`()` {#classshogun_1_1CKernel_1abcba15494b772139077b7e71db562e58}

obtain the current kernel normalizer

#### Returns
the kernel normalizer

#### `public virtual bool `[`init_normalizer`](#classshogun_1_1CKernel_1aa7df874ba16e360949f66100aad43e23)`()` {#classshogun_1_1CKernel_1aa7df874ba16e360949f66100aad43e23}

initialize the current kernel normalizer 
#### Returns
if init was successful

#### `public virtual void `[`cleanup`](#classshogun_1_1CKernel_1a4b66d5e31b5dc18b314c8a68163263bd)`()` {#classshogun_1_1CKernel_1a4b66d5e31b5dc18b314c8a68163263bd}

clean up your kernel

base method only removes lhs and rhs overload to add further cleanup but make sure [CKernel::cleanup()](#classshogun_1_1CKernel_1a4b66d5e31b5dc18b314c8a68163263bd) is called

#### `public void `[`load`](#classshogun_1_1CKernel_1a5d33ec59a4be25056cca1f3b6691ad00)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` {#classshogun_1_1CKernel_1a5d33ec59a4be25056cca1f3b6691ad00}

load the kernel matrix

#### Parameters
* `loader` File object via which to load data

#### `public void `[`save`](#classshogun_1_1CKernel_1a2ec11d78c7f60dfbc77bc2f56d211033)`(`[`CFile`](#classshogun_1_1CFile)` * writer)` {#classshogun_1_1CKernel_1a2ec11d78c7f60dfbc77bc2f56d211033}

save kernel matrix

#### Parameters
* `writer` File object via which to save data

#### `public inline `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`get_lhs`](#classshogun_1_1CKernel_1aa3e521f9c3df80da4bc44c2ba0b6c0be)`()` {#classshogun_1_1CKernel_1aa3e521f9c3df80da4bc44c2ba0b6c0be}

get left-hand side of features used in kernel

#### Returns
features of left-hand side

#### `public inline `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`get_rhs`](#classshogun_1_1CKernel_1a28c50c34fc59a74f2b015ba87dc133d9)`()` {#classshogun_1_1CKernel_1a28c50c34fc59a74f2b015ba87dc133d9}

get right-hand side of features used in kernel

#### Returns
features of right-hand side

#### `public inline virtual int32_t `[`get_num_vec_lhs`](#classshogun_1_1CKernel_1af81140e34d38612802e1b8783424260a)`()` {#classshogun_1_1CKernel_1af81140e34d38612802e1b8783424260a}

get number of vectors of lhs features

#### Returns
number of vectors of left-hand side

#### `public inline virtual int32_t `[`get_num_vec_rhs`](#classshogun_1_1CKernel_1aabc415a305914c27567a1343f7957cac)`()` {#classshogun_1_1CKernel_1aabc415a305914c27567a1343f7957cac}

get number of vectors of rhs features

#### Returns
number of vectors of right-hand side

#### `public inline virtual bool `[`has_features`](#classshogun_1_1CKernel_1abcd71e362bf0042668c5527e17968fe6)`()` {#classshogun_1_1CKernel_1abcd71e362bf0042668c5527e17968fe6}

test whether features have been assigned to lhs and rhs

#### Returns
true if features are assigned

#### `public inline bool `[`get_lhs_equals_rhs`](#classshogun_1_1CKernel_1a79527726c2f525e4236e186d77a63849)`()` {#classshogun_1_1CKernel_1a79527726c2f525e4236e186d77a63849}

test whether features on lhs and rhs are the same

#### Returns
true if features are the same

#### `public virtual void `[`remove_lhs_and_rhs`](#classshogun_1_1CKernel_1a69d2fffafdc0984cea96e3f4a4f737cb)`()` {#classshogun_1_1CKernel_1a69d2fffafdc0984cea96e3f4a4f737cb}

remove lhs and rhs from kernel

#### `public virtual void `[`remove_lhs`](#classshogun_1_1CKernel_1a214e795fd785274e29d97d4b16aa6fc4)`()` {#classshogun_1_1CKernel_1a214e795fd785274e29d97d4b16aa6fc4}

remove lhs from kernel

#### `public virtual void `[`remove_rhs`](#classshogun_1_1CKernel_1af6c99208795e1ff43d204e3e5adb78ec)`()` {#classshogun_1_1CKernel_1af6c99208795e1ff43d204e3e5adb78ec}

takes all necessary steps if the rhs is removed from kernel

remove rhs from kernel

#### `public inline void `[`set_cache_size`](#classshogun_1_1CKernel_1ae5c0887476ce715d70b0bdf837c277b7)`(int32_t size)` {#classshogun_1_1CKernel_1ae5c0887476ce715d70b0bdf837c277b7}

set the size of the kernel cache

#### Parameters
* `size` of kernel cache

#### `public inline int32_t `[`get_cache_size`](#classshogun_1_1CKernel_1a7cd5c5d069c93cc98539fcb7baff0567)`()` {#classshogun_1_1CKernel_1a7cd5c5d069c93cc98539fcb7baff0567}

return the size of the kernel cache

#### Returns
size of kernel cache

#### `public inline void `[`cache_reset`](#classshogun_1_1CKernel_1ac7acb3ba30d154651c3ab1afd9c0bc41)`()` {#classshogun_1_1CKernel_1ac7acb3ba30d154651c3ab1afd9c0bc41}

cache reset

#### `public inline int32_t `[`get_max_elems_cache`](#classshogun_1_1CKernel_1a408e958c004d1e28e90f885909a135a9)`()` {#classshogun_1_1CKernel_1a408e958c004d1e28e90f885909a135a9}

get maximum elements in cache

#### Returns
maximum elements in cache

#### `public inline int32_t `[`get_activenum_cache`](#classshogun_1_1CKernel_1ae7f812236ff0dd3e44069daa0c0558e4)`()` {#classshogun_1_1CKernel_1ae7f812236ff0dd3e44069daa0c0558e4}

get activenum cache

#### Returns
activecnum cache

#### `public void `[`cache_kernel_row`](#classshogun_1_1CKernel_1ae1ac999b5941145f254e21fba6e97240)`(int32_t x)` {#classshogun_1_1CKernel_1ae1ac999b5941145f254e21fba6e97240}

cache kernel row

#### Parameters
* `x` x

#### `public void `[`cache_multiple_kernel_rows`](#classshogun_1_1CKernel_1abdce614df171105f0eb3796fa238dbef)`(int32_t * key,int32_t varnum)` {#classshogun_1_1CKernel_1abdce614df171105f0eb3796fa238dbef}

cache multiple kernel rows

#### Parameters
* `key` key 

* `varnum`

#### `public void `[`kernel_cache_reset_lru`](#classshogun_1_1CKernel_1a795988d5cfd87cd02cfaf8cf3ad92c3b)`()` {#classshogun_1_1CKernel_1a795988d5cfd87cd02cfaf8cf3ad92c3b}

kernel cache reset lru

#### `public void `[`kernel_cache_shrink`](#classshogun_1_1CKernel_1abaf9323473978dc5159541b5458226c0)`(int32_t totdoc,int32_t num_shrink,int32_t * after)` {#classshogun_1_1CKernel_1abaf9323473978dc5159541b5458226c0}

kernel cache shrink

#### Parameters
* `totdoc` totdoc 

* `num_shrink` number of shrink 

* `after` after

#### `public void `[`resize_kernel_cache`](#classshogun_1_1CKernel_1af3e54d2ca0a3c2bfe30905eeab6a5e88)`(`[`KERNELCACHE_IDX`](#namespaceshogun_1a80ec34b03eaf01338e02ebd002ded245)` size,bool regression_hack)` {#classshogun_1_1CKernel_1af3e54d2ca0a3c2bfe30905eeab6a5e88}

resize kernel cache

#### Parameters
* `size` new size 

* `regression_hack` hack for regression

#### `public inline void `[`set_time`](#classshogun_1_1CKernel_1aafee0a28cbbf03c56b988736382c5e3f)`(int32_t t)` {#classshogun_1_1CKernel_1aafee0a28cbbf03c56b988736382c5e3f}

set the lru time

#### Parameters
* `t` the time to use

#### `public inline int32_t `[`kernel_cache_touch`](#classshogun_1_1CKernel_1a222e848c2960c2e74ff00ee0182ce8e9)`(int32_t cacheidx)` {#classshogun_1_1CKernel_1a222e848c2960c2e74ff00ee0182ce8e9}

update lru time of item at given index to avoid removal from cache

#### Parameters
* `cacheidx` index in cache 

#### Returns
if updating was successful

#### `public inline int32_t `[`kernel_cache_check`](#classshogun_1_1CKernel_1a387fbc5855ff829980ae52f0eb295b62)`(int32_t cacheidx)` {#classshogun_1_1CKernel_1a387fbc5855ff829980ae52f0eb295b62}

check if row at given index is cached

#### Parameters
* `cacheidx` index in cache 

#### Returns
if row at given index is cached

#### `public inline int32_t `[`kernel_cache_space_available`](#classshogun_1_1CKernel_1a8261cb96381df464c9d9d63537224a16)`()` {#classshogun_1_1CKernel_1a8261cb96381df464c9d9d63537224a16}

check if there is room for one more row in kernel cache

#### Returns
if there is room for one more row in kernel cache

#### `public void `[`kernel_cache_init`](#classshogun_1_1CKernel_1a6550676493b70dc4bfd4c7ce865f0aaf)`(int32_t size,bool regression_hack)` {#classshogun_1_1CKernel_1a6550676493b70dc4bfd4c7ce865f0aaf}

initialize kernel cache

#### Parameters
* `size` size to initialize to 

* `regression_hack` if hack for regression shall be applied

#### `public void `[`kernel_cache_cleanup`](#classshogun_1_1CKernel_1a4c7e6d6e223aa13629e241c804a34694)`()` {#classshogun_1_1CKernel_1a4c7e6d6e223aa13629e241c804a34694}

cleanup kernel cache

#### `public void `[`list_kernel`](#classshogun_1_1CKernel_1a2c56cf3c1a9b6fb1a66ea83bb0b89e6d)`()` {#classshogun_1_1CKernel_1a2c56cf3c1a9b6fb1a66ea83bb0b89e6d}

list kernel

#### `public inline virtual bool `[`has_property`](#classshogun_1_1CKernel_1a535b6b6715d5957b004af00a5a8b1858)`(`[`EKernelProperty`](#namespaceshogun_1a3280191ade233d4393b7b6181dcec00c)` p)` {#classshogun_1_1CKernel_1a535b6b6715d5957b004af00a5a8b1858}

check if kernel has given property

#### Parameters
* `p` kernel property 

#### Returns
if kernel has given property

#### `public virtual void `[`clear_normal`](#classshogun_1_1CKernel_1ac86fdff79b1cdfa071d4e56edfae178c)`()` {#classshogun_1_1CKernel_1ac86fdff79b1cdfa071d4e56edfae178c}

for optimizable kernels, i.e. kernels where the weight vector can be computed explicitly (if it fits into memory)

#### `public virtual void `[`add_to_normal`](#classshogun_1_1CKernel_1a881dcf9c3c9bb8940eb5b625e8e18860)`(int32_t vector_idx,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` weight)` {#classshogun_1_1CKernel_1a881dcf9c3c9bb8940eb5b625e8e18860}

add vector*factor to 'virtual' normal vector

#### Parameters
* `vector_idx` index 

* `weight` weight

#### `public inline `[`EOptimizationType`](#namespaceshogun_1a0864e2ed51fdcd3fe0fac7f7d0429cbc)` `[`get_optimization_type`](#classshogun_1_1CKernel_1a231c6ef0246fd030129378ce4aa2ff23)`()` {#classshogun_1_1CKernel_1a231c6ef0246fd030129378ce4aa2ff23}

get optimization type

#### Returns
optimization type

#### `public inline virtual void `[`set_optimization_type`](#classshogun_1_1CKernel_1a0115f60f8d9d977dec2a2fd72fd50c7b)`(`[`EOptimizationType`](#namespaceshogun_1a0864e2ed51fdcd3fe0fac7f7d0429cbc)` t)` {#classshogun_1_1CKernel_1a0115f60f8d9d977dec2a2fd72fd50c7b}

set optimization type

#### Parameters
* `t` optimization type to set

#### `public inline bool `[`get_is_initialized`](#classshogun_1_1CKernel_1ac7083cb2099c1de0a702f53665c7e256)`()` {#classshogun_1_1CKernel_1ac7083cb2099c1de0a702f53665c7e256}

check if optimization is initialized

#### Returns
if optimization is initialized

#### `public virtual bool `[`init_optimization`](#classshogun_1_1CKernel_1a8b5139637c80888fb957da9e78262930)`(int32_t count,int32_t * IDX,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * weights)` {#classshogun_1_1CKernel_1a8b5139637c80888fb957da9e78262930}

initialize optimization

#### Parameters
* `count` count 

* `IDX` index 

* `weights` weights 

#### Returns
if initializing was successful

#### `public virtual bool `[`delete_optimization`](#classshogun_1_1CKernel_1adbfd9c323b8f18e99a724e9d31de082c)`()` {#classshogun_1_1CKernel_1adbfd9c323b8f18e99a724e9d31de082c}

delete optimization

#### Returns
if deleting was successful

#### `public bool `[`init_optimization_svm`](#classshogun_1_1CKernel_1a033a692905152791779c2db666a508b2)`(`[`CSVM`](#classshogun_1_1CSVM)` * svm)` {#classshogun_1_1CKernel_1a033a692905152791779c2db666a508b2}

initialize optimization

#### Parameters
* `svm` svm model 

#### Returns
if initializing was successful

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_optimized`](#classshogun_1_1CKernel_1af6e91433913335a43a418c32e5add461)`(int32_t vector_idx)` {#classshogun_1_1CKernel_1af6e91433913335a43a418c32e5add461}

compute optimized

#### Parameters
* `vector_idx` index to compute 

#### Returns
optimized value at given index

#### `public virtual void `[`compute_batch`](#classshogun_1_1CKernel_1abbbe72b9a886d60eade98489d6ffa273)`(int32_t num_vec,int32_t * vec_idx,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * target,int32_t num_suppvec,int32_t * IDX,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * alphas,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` factor)` {#classshogun_1_1CKernel_1abbbe72b9a886d60eade98489d6ffa273}

computes output for a batch of examples in an optimized fashion (favorable if kernel supports it, i.e. has KP_BATCHEVALUATION. to the outputvector target (of length num_vec elements) the output for the examples enumerated in vec_idx are added. therefore make sure that it is initialized with ZERO. the following num_suppvec, IDX, alphas arguments are the number of support vectors, their indices and weights

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_combined_kernel_weight`](#classshogun_1_1CKernel_1aca8b2ae0268d160ab41531ed8bfea849)`()` {#classshogun_1_1CKernel_1aca8b2ae0268d160ab41531ed8bfea849}

get combined kernel weight

#### Returns
combined kernel weight

#### `public inline void `[`set_combined_kernel_weight`](#classshogun_1_1CKernel_1a7abf31f4bf05f91f3fe724dc20f4dba5)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` nw)` {#classshogun_1_1CKernel_1a7abf31f4bf05f91f3fe724dc20f4dba5}

set combined kernel weight

#### Parameters
* `nw` new combined kernel weight

#### `public virtual int32_t `[`get_num_subkernels`](#classshogun_1_1CKernel_1a462e89b5ef214f1460057fe65c91993b)`()` {#classshogun_1_1CKernel_1a462e89b5ef214f1460057fe65c91993b}

get number of subkernels

#### Returns
number of subkernels

#### `public virtual void `[`compute_by_subkernel`](#classshogun_1_1CKernel_1a6238f812ab53a3ae36e176a303fb205a)`(int32_t vector_idx,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * subkernel_contrib)` {#classshogun_1_1CKernel_1a6238f812ab53a3ae36e176a303fb205a}

compute by subkernel

#### Parameters
* `vector_idx` index 

* `subkernel_contrib` subkernel contribution

#### `public virtual const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`get_subkernel_weights`](#classshogun_1_1CKernel_1a55ee24f23e9819656501c3bffefe1063)`(int32_t & num_weights)` {#classshogun_1_1CKernel_1a55ee24f23e9819656501c3bffefe1063}

get subkernel weights

#### Parameters
* `num_weights` number of weights will be stored here 

#### Returns
subkernel weights

#### `public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_subkernel_weights`](#classshogun_1_1CKernel_1adb9aa3ff6a6ad8fd0bd84ffa7db2e459)`()` {#classshogun_1_1CKernel_1adb9aa3ff6a6ad8fd0bd84ffa7db2e459}

get subkernel weights (swig compatible)

#### Returns
subkernel weights

#### `public virtual void `[`set_subkernel_weights`](#classshogun_1_1CKernel_1a65ebc4353804603d7b630e54050d90ed)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > weights)` {#classshogun_1_1CKernel_1a65ebc4353804603d7b630e54050d90ed}

set subkernel weights

#### Parameters
* `weights` new subkernel weights

#### `public inline virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_parameter_gradient`](#classshogun_1_1CKernel_1ac1d79ae65ddb803f672223f8c61cffde)`(const `[`TParameter`](#structshogun_1_1TParameter)` * param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index)` {#classshogun_1_1CKernel_1ac1d79ae65ddb803f672223f8c61cffde}

return derivative with respect to specified parameter

#### Parameters
* `param` the parameter 

* `index` the index of the element if parameter is a vector

#### Returns
gradient with respect to parameter

#### `public inline virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_parameter_gradient_diagonal`](#classshogun_1_1CKernel_1a2f0b7215dd7ef0628d43d67ef360369a)`(const `[`TParameter`](#structshogun_1_1TParameter)` * param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index)` {#classshogun_1_1CKernel_1a2f0b7215dd7ef0628d43d67ef360369a}

return diagonal part of derivative with respect to specified parameter

#### Parameters
* `param` the parameter 

* `index` the index of the element if parameter is a vector

#### Returns
diagonal part of gradient with respect to parameter

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

#### `public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CSGObject_1ad3711d9770e4b96ae8e89a99c9f530f7)`(const `[`Tag`](#classshogun_1_1Tag)`< T > & _tag,const T & value)` {#classshogun_1_1CSGObject_1ad3711d9770e4b96ae8e89a99c9f530f7}

Setter for a class parameter, identified by a [Tag](#classshogun_1_1Tag). Throws an exception if the class does not have such a parameter.

#### Parameters
* `_tag` name and type information of parameter 

* `value` value of the parameter

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

#### `protected int32_t `[`cache_size`](#classshogun_1_1CKernel_1a05f0572d7f5c701ff73f186b45a1d815) {#classshogun_1_1CKernel_1a05f0572d7f5c701ff73f186b45a1d815}

cache_size in MB

#### `protected KERNEL_CACHE `[`kernel_cache`](#classshogun_1_1CKernel_1a49c6c2cecb82271cf4bc3ea2f552913e) {#classshogun_1_1CKernel_1a49c6c2cecb82271cf4bc3ea2f552913e}

kernel cache

#### `protected `[`KERNELCACHE_ELEM`](#namespaceshogun_1ab6286d846462ad5d8abee6a985150754)` * `[`kernel_matrix`](#classshogun_1_1CKernel_1a171add209887a004b5b06e4f839947e2) {#classshogun_1_1CKernel_1a171add209887a004b5b06e4f839947e2}

this *COULD* store the whole kernel matrix usually not applicable / necessary to compute the whole matrix

#### `protected `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`lhs`](#classshogun_1_1CKernel_1a5bb6375a26075c34dc856a477828ad52) {#classshogun_1_1CKernel_1a5bb6375a26075c34dc856a477828ad52}

feature vectors to occur on left hand side

#### `protected `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`rhs`](#classshogun_1_1CKernel_1a8e375dd40df7b063ba9f2da598e1a3a9) {#classshogun_1_1CKernel_1a8e375dd40df7b063ba9f2da598e1a3a9}

feature vectors to occur on right hand side

#### `protected bool `[`lhs_equals_rhs`](#classshogun_1_1CKernel_1afda5656b0c2b69ca8ee7a6a6bc1758ff) {#classshogun_1_1CKernel_1afda5656b0c2b69ca8ee7a6a6bc1758ff}

lhs

#### `protected int32_t `[`num_lhs`](#classshogun_1_1CKernel_1ac6a6d53fdb5fd47fffd56b1b03d41e09) {#classshogun_1_1CKernel_1ac6a6d53fdb5fd47fffd56b1b03d41e09}

number of feature vectors on left hand side

#### `protected int32_t `[`num_rhs`](#classshogun_1_1CKernel_1a84e7d5029b76c7b2b5903c6600adc036) {#classshogun_1_1CKernel_1a84e7d5029b76c7b2b5903c6600adc036}

number of feature vectors on right hand side

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`combined_kernel_weight`](#classshogun_1_1CKernel_1a742203c256bc90e4fcc329eebe7d02a9) {#classshogun_1_1CKernel_1a742203c256bc90e4fcc329eebe7d02a9}

combined kernel weight

#### `protected bool `[`optimization_initialized`](#classshogun_1_1CKernel_1a9948eae33d1441baa52cb9f0943d250a) {#classshogun_1_1CKernel_1a9948eae33d1441baa52cb9f0943d250a}

if optimization is initialized

#### `protected `[`EOptimizationType`](#namespaceshogun_1a0864e2ed51fdcd3fe0fac7f7d0429cbc)` `[`opt_type`](#classshogun_1_1CKernel_1a10d9465919ff381c40f0a308746a3dee) {#classshogun_1_1CKernel_1a10d9465919ff381c40f0a308746a3dee}

optimization type (currently FASTBUTMEMHUNGRY and SLOWBUTMEMEFFICIENT)

#### `protected uint64_t `[`properties`](#classshogun_1_1CKernel_1a07267159f65dd3ece9cfd00bbaf1c99c) {#classshogun_1_1CKernel_1a07267159f65dd3ece9cfd00bbaf1c99c}

kernel properties

#### `protected `[`CKernelNormalizer`](#classshogun_1_1CKernelNormalizer)` * `[`normalizer`](#classshogun_1_1CKernel_1aa98b2c40e3a7b7c76e35b58df4570022) {#classshogun_1_1CKernel_1aa98b2c40e3a7b7c76e35b58df4570022}

normalize the kernel(i,j) function based on this normalization function

#### `protected inline void `[`set_property`](#classshogun_1_1CKernel_1a9124fc95acc6a5a8b8006539b92684b8)`(`[`EKernelProperty`](#namespaceshogun_1a3280191ade233d4393b7b6181dcec00c)` p)` {#classshogun_1_1CKernel_1a9124fc95acc6a5a8b8006539b92684b8}

set property

#### Parameters
* `p` kernel property to set

#### `protected inline void `[`unset_property`](#classshogun_1_1CKernel_1a8fc3fa0bd8870e260221708e5a1c71d3)`(`[`EKernelProperty`](#namespaceshogun_1a3280191ade233d4393b7b6181dcec00c)` p)` {#classshogun_1_1CKernel_1a8fc3fa0bd8870e260221708e5a1c71d3}

unset property

#### Parameters
* `p` kernel property to unset

#### `protected inline void `[`set_is_initialized`](#classshogun_1_1CKernel_1a4c62e85d1f0681dbd84ff6a15f66a864)`(bool p_init)` {#classshogun_1_1CKernel_1a4c62e85d1f0681dbd84ff6a15f66a864}

set is initialized

#### Parameters
* `p_init` if optimization shall be set to initialized

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute`](#classshogun_1_1CKernel_1ac6a01ee581de85069a4b697db55e34b5)`(int32_t x,int32_t y)` {#classshogun_1_1CKernel_1ac6a01ee581de85069a4b697db55e34b5}

compute kernel function for features a and b idx_{a,b} denote the index of the feature vectors in the corresponding feature object

abstract base method

#### Parameters
* `x` index a 

* `y` index b 

#### Returns
computed kernel function at indices a,b

#### `protected inline int32_t `[`compute_row_start`](#classshogun_1_1CKernel_1a8476cd069409e0b64c2fe6099e07cfcb)`(int64_t offs,int32_t n,bool symmetric)` {#classshogun_1_1CKernel_1a8476cd069409e0b64c2fe6099e07cfcb}

compute row start offset for parallel kernel matrix computation

#### Parameters
* `offs` offset 

* `n` number of columns 

* `symmetric` whether matrix is symmetric

#### `protected virtual void `[`load_serializable_post`](#classshogun_1_1CKernel_1a4c8da771d1ddf319cabc6b9e896326f2)`()` {#classshogun_1_1CKernel_1a4c8da771d1ddf319cabc6b9e896326f2}

Can (optionally) be overridden to post-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::LOAD_SERIALIZABLE_POST is called.

#### Exceptions
* `[ShogunException](#classshogun_1_1ShogunException)` Will be thrown if an error occurres.

#### `protected virtual void `[`save_serializable_pre`](#classshogun_1_1CKernel_1a44300a33d16909f1bf7a129d19d4ca41)`()` {#classshogun_1_1CKernel_1a44300a33d16909f1bf7a129d19d4ca41}

Can (optionally) be overridden to pre-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::SAVE_SERIALIZABLE_PRE is called.

#### Exceptions
* `[ShogunException](#classshogun_1_1ShogunException)` Will be thrown if an error occurres.

#### `protected virtual void `[`save_serializable_post`](#classshogun_1_1CKernel_1ab63af4bfbc71bb737703e48425db1aa2)`()` {#classshogun_1_1CKernel_1ab63af4bfbc71bb737703e48425db1aa2}

Can (optionally) be overridden to post-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::SAVE_SERIALIZABLE_POST is called.

#### Exceptions
* `[ShogunException](#classshogun_1_1ShogunException)` Will be thrown if an error occurres.

#### `protected virtual void `[`register_params`](#classshogun_1_1CKernel_1a5a7bc37cc5ce93e9444637bbd72f703e)`()` {#classshogun_1_1CKernel_1a5a7bc37cc5ce93e9444637bbd72f703e}

Separate the function of parameter registration This can be the first stage of a *general* framework for cross-validation or other parameter-based operations

#### `protected template<>`  <br/>`inline `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`get_sgobject_type_dispatcher`](#classshogun_1_1CSGObject_1a7de7c1e11c3d4322d74a9a8cf5cc13f1)`(const std::string & name)` {#classshogun_1_1CSGObject_1a7de7c1e11c3d4322d74a9a8cf5cc13f1}

#### `protected virtual void `[`load_serializable_pre`](#classshogun_1_1CSGObject_1a7361535fc1a8b13beb9dd0b4ac2dd790)`()` {#classshogun_1_1CSGObject_1a7361535fc1a8b13beb9dd0b4ac2dd790}

Can (optionally) be overridden to pre-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::LOAD_SERIALIZABLE_PRE is called.

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

