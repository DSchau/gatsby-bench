---
classname: "shogun::CPCA"
type: "class"
parents:
   - CDensePreprocessor< float64_t >
---

# class `shogun::CPCA` {#classshogun_1_1CPCA}

```
class shogun::CPCA
  : public CDensePreprocessor< float64_t >
```

Preprocessor PCA performs principial component analysis on input feature vectors/matrices. When the init method in PCA is called with proper feature matrix X (with say N number of vectors and D feature dimension), a transformation matrix is computed and stored internally. This transformation matrix is then used to transform all D-dimensional feature vectors or feature matrices (with D feature dimensions) supplied via apply_to_feature_matrix or apply_to_feature_vector methods. This tranformation outputs the T-Dimensional approximation of all these input vectors and matrices (where T<=min(D,N)). The transformation matrix is essentially a DxT matrix, the columns of which correspond to the eigenvectors of the covariance matrix(XX') having top T eigenvalues.

This class provides 3 method options to compute the transformation matrix : *EVD* : [Eigen](#namespaceEigen) Value Decomposition of Covariance Matrix ( $XX^T$) The covariance matrix $XX^T$ is first formed internally and then its eigenvectors and eigenvalues are computed. The time complexity of this method is $~10D^3$ and should be used when N > D.

*SVD* : Singular Value Decomposition of feature matrix X The transpose of feature matrix, $X^T$, is decomposed using SVD. $X^T = UDV^T$ The matrix V in this decomposition contains the required eigenvectors and the diagonal entries of the diagonal matrix D correspond to the non-negative eigenvalues. Eigenvalue, $e_i$, is derived from a diagonal element, $d_i$, using the formula $e_i = \frac{\sqrt{d_i}}{N-1}$. The time complexity of this method is $~14DN^2$ and should be used when N < D.

*AUTO* : This mode automagically chooses one of the above modes for the user based on whether N > D (chooses EVD) or N < D (chooses SVD).

This class provides 3 modes to determine the value of T :

*FIXED_NUMBER* : T is supplied by user directly using set_target_dims method

*VARIANCE_EXPLAINED* : The user supplies the fractional variance that he wants preserved in the target dimension T. From this supplied fractional variance (thresh), T is calculated as the smallest k such that the ratio of sum of largest k eigenvalues over total sum of all eigenvalues is greater than thresh.

*THRESH* : The user supplies a threshold. All eigenvectors with corresponding eigenvalue greater than the supplied threshold are chosen.

An option for whitening the transformation matrix is also given - do_whitening. Setting this option normalizes the eigenvectors (ie. the columns of transformation matrix) by dividing them with the square root of corresponding eigenvalues.

Note that vectors/matrices don't have to have zero mean as it is substracted within the class.

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
`public  `[`CPCA`](#classshogun_1_1CPCA_1a04bccdb2ed035e016a4d322bbb9dfebe)`(bool do_whitening,`[`EPCAMode`](#namespaceshogun_1a071a8ca3a05606f4869ea52b7a7fa049)` mode,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` thresh,`[`EPCAMethod`](#namespaceshogun_1a993bafb98a8a6d82925f9683f7a6eabf)` method,`[`EPCAMemoryMode`](#namespaceshogun_1a374639d69db184f2509606cfea78b899)` mem_mode)` | standard constructor
`public  `[`CPCA`](#classshogun_1_1CPCA_1a8e601030332aaae2828c9d92c3398464)`(`[`EPCAMethod`](#namespaceshogun_1a993bafb98a8a6d82925f9683f7a6eabf)` method,bool do_whitening,`[`EPCAMemoryMode`](#namespaceshogun_1a374639d69db184f2509606cfea78b899)` mem)` | special constructor for FIXED_NUMBER mode
`public virtual  `[`~CPCA`](#classshogun_1_1CPCA_1a6b0f74862f98136c60dbba616de99e4f)`()` | destructor
`public virtual void `[`fit`](#classshogun_1_1CPCA_1a92c77f552b5c903eb6dde3b739556075)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * features)` | Fit transformer to features 
`public virtual void `[`cleanup`](#classshogun_1_1CPCA_1a4b66d5e31b5dc18b314c8a68163263bd)`()` | cleanup
`public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`apply_to_feature_vector`](#classshogun_1_1CPCA_1a45584b03dc12df6e0e4e3d266e1810ef)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > vector)` | apply preprocessor to feature vector 
`public `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_transformation_matrix`](#classshogun_1_1CPCA_1acd1f9e21cdb441ef5d7567e167180a8e)`()` | get transformation matrix, i.e. eigenvectors (potentially scaled if do_whitening is true)
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_eigenvalues`](#classshogun_1_1CPCA_1a3572b0e224c79f48884f4af1b60307e1)`()` | get eigenvalues of PCA
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_mean`](#classshogun_1_1CPCA_1a92d96916c774173e59d8a960648ebd78)`()` | get mean vector of original data
`public inline virtual const char * `[`get_name`](#classshogun_1_1CPCA_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` | #### Returns
`public inline virtual `[`EPreprocessorType`](#namespaceshogun_1af6317e92a2bed0d86257f3a589a5e9f3)` `[`get_type`](#classshogun_1_1CPCA_1afa592e9c6f9e700c293061fceaaac7f2)`() const` | #### Returns
`public `[`EPCAMemoryMode`](#namespaceshogun_1a374639d69db184f2509606cfea78b899)` `[`get_memory_mode`](#classshogun_1_1CPCA_1a8a76cc0a5fbcfb1af856d575485d66ed)`() const` | return the PCA memory mode being used
`public void `[`set_memory_mode`](#classshogun_1_1CPCA_1a8df99c085206c29c5b65d1c51a7683b9)`(`[`EPCAMemoryMode`](#namespaceshogun_1a374639d69db184f2509606cfea78b899)` e)` | set PCA memory mode to be used 
`public void `[`set_eigenvalue_zero_tolerance`](#classshogun_1_1CPCA_1a050b824111b3d827b92e1dabced63df4)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` eigenvalue_zero_tolerance)` | set zero tolerance of eigenvalues during data whitening 
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_eigenvalue_zero_tolerance`](#classshogun_1_1CPCA_1af3296418fd90ad632dc093f24fe95a16)`() const` | get zero tolerance of eigenvalues during data whitening 
`public void `[`set_target_dim`](#classshogun_1_1CPCA_1a626c39e21bb5842525ea02561084dc00)`(int32_t dim)` | setter for target dimension 
`public int32_t `[`get_target_dim`](#classshogun_1_1CPCA_1abc02f1d05f1877d5b2b16b1c9482e5fb)`() const` | getter for target dimension 
`public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`transform`](#classshogun_1_1CDensePreprocessor_1a801a3d5a27cc8ad45c887a93e768a987)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * features,bool inplace)` | Apply transformation to dense features.
`public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`inverse_transform`](#classshogun_1_1CDensePreprocessor_1aea5d40ee0debdddaa64170453f7afea5)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * features,bool inplace)` | Apply inverse transformation to dense features.
`public virtual `[`EFeatureClass`](#namespaceshogun_1a9e2a4d8b86b9e061779c3fdbcda57c3b)` `[`get_feature_class`](#classshogun_1_1CDensePreprocessor_1a00c0270aae194f8c691f0bd5e897e716)`()` | return that we are dense features (just fixed size matrices)
`public virtual `[`EFeatureType`](#namespaceshogun_1a064eec90e91f56435546d77f38c0b618)` `[`get_feature_type`](#classshogun_1_1CDensePreprocessor_1ac6916b730dc608dbccb96cd1b0bfa528)`()` | return feature type
`public virtual `[`EFeatureType`](#namespaceshogun_1a064eec90e91f56435546d77f38c0b618)` `[`get_feature_type`](#classshogun_1_1CDensePreprocessor_1a5c2663373829bede6e18ef9f655b8fd3)`()` | #### Returns
`public inline virtual void `[`fit`](#classshogun_1_1CTransformer_1ac651a02333f3e64518cdfca084cec90b)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * features,`[`CLabels`](#classshogun_1_1CLabels)` * labels)` | Fit transformer to features and labels 
`public inline virtual bool `[`train_require_labels`](#classshogun_1_1CTransformer_1a47f97bf5de534202ae00e77e485f3740)`() const` | 
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
`protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_transformation_matrix`](#classshogun_1_1CPCA_1a79fc753072325f2447a10079e3d2cca0) | transformation matrix
`protected int32_t `[`num_dim`](#classshogun_1_1CPCA_1a9f8d6c6b33c67688f6230e8db34d7d00) | num dim
`protected int32_t `[`num_old_dim`](#classshogun_1_1CPCA_1af219bad49a5a7e5401f9565d5e0afeda) | num old dim
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_mean_vector`](#classshogun_1_1CPCA_1a8483cfb64208abf02e32762a2c54e903) | mean vector
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_eigenvalues_vector`](#classshogun_1_1CPCA_1a8d07af893a081ef32ef8534d6f9c7802) | eigenvalues vector
`protected bool `[`m_whitening`](#classshogun_1_1CPCA_1aac3df5860d870a6ddfc4503cd60bb36e) | whitening
`protected `[`EPCAMode`](#namespaceshogun_1a071a8ca3a05606f4869ea52b7a7fa049)` `[`m_mode`](#classshogun_1_1CPCA_1a3b1b014e7c64b80c9e8edd750cf9f88b) | PCA mode
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_thresh`](#classshogun_1_1CPCA_1a24f0f29d1eba4c059a120abc137e369c) | thresh
`protected `[`EPCAMemoryMode`](#namespaceshogun_1a374639d69db184f2509606cfea78b899)` `[`m_mem_mode`](#classshogun_1_1CPCA_1abd88cf0b6512674efdba1cfd8a9bd8e9) | PCA memory mode
`protected `[`EPCAMethod`](#namespaceshogun_1a993bafb98a8a6d82925f9683f7a6eabf)` `[`m_method`](#classshogun_1_1CPCA_1abdf596f307570a48e6f55060b8b00352) | PCA method
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_eigenvalue_zero_tolerance`](#classshogun_1_1CPCA_1abbb746cb133d5e801e7d1430482286bf) | eigenvalues within zero tolerance region are considered 0 while whitening to tackle numerical issues
`protected int32_t `[`m_target_dim`](#classshogun_1_1CPCA_1a5e3eefc4485af0a00c0b6b9d69eb5e38) | target dimension
`protected bool `[`m_fitted`](#classshogun_1_1CTransformer_1ac7a9f470db2627f8ba58a3880fb34b2e) | 
`protected void `[`init`](#classshogun_1_1CPCA_1a02fd73d861ef2e4aabb38c0c9ff82947)`()` | 
`protected virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`apply_to_matrix`](#classshogun_1_1CPCA_1a34a2b3c8cecffe4f7b64621ace8733e7)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > matrix)` | Apply preprocessor on matrix. Subclasses should try to apply in place to avoid copying. 
`protected virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`inverse_apply_to_matrix`](#classshogun_1_1CDensePreprocessor_1a20690602d6f44cb26ba63e7c6e8aef23)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > matrix)` | Inverse apply preprocessor on matrix. Subclasses should try to apply in place to avoid copying. 
`protected void `[`assert_fitted`](#classshogun_1_1CTransformer_1ae1679ea842202ddfa8825779c7912311)`() const` | Check current transformer has been fitted, throw [NotFittedException](#classshogun_1_1NotFittedException) otherwise.
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

#### `public  `[`CPCA`](#classshogun_1_1CPCA_1a04bccdb2ed035e016a4d322bbb9dfebe)`(bool do_whitening,`[`EPCAMode`](#namespaceshogun_1a071a8ca3a05606f4869ea52b7a7fa049)` mode,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` thresh,`[`EPCAMethod`](#namespaceshogun_1a993bafb98a8a6d82925f9683f7a6eabf)` method,`[`EPCAMemoryMode`](#namespaceshogun_1a374639d69db184f2509606cfea78b899)` mem_mode)` {#classshogun_1_1CPCA_1a04bccdb2ed035e016a4d322bbb9dfebe}

standard constructor

#### Parameters
* `do_whitening` normalize columns(eigenvectors) in transformation matrix 

* `mode` mode of pca : FIXED_NUMBER/VARIANCE_EXPLAINED/THRESHOLD 

* `thresh` threshold value for VARIANCE_EXPLAINED or THRESHOLD mode 

* `method` Matrix decomposition method used : SVD/EVD/AUTO[default] 

* `mem_mode` memory usage mode of PCA : MEM_REALLOCATE/MEM_IN_PLACE

#### `public  `[`CPCA`](#classshogun_1_1CPCA_1a8e601030332aaae2828c9d92c3398464)`(`[`EPCAMethod`](#namespaceshogun_1a993bafb98a8a6d82925f9683f7a6eabf)` method,bool do_whitening,`[`EPCAMemoryMode`](#namespaceshogun_1a374639d69db184f2509606cfea78b899)` mem)` {#classshogun_1_1CPCA_1a8e601030332aaae2828c9d92c3398464}

special constructor for FIXED_NUMBER mode

#### Parameters
* `method` Matrix decomposition method used : SVD/EVD/AUTO[default] 

* `do_whitening` normalize columns(eigenvectors) in transformation matrix 

* `mem` memory usage mode of PCA : MEM_REALLOCATE/MEM_IN_PLACE

#### `public virtual  `[`~CPCA`](#classshogun_1_1CPCA_1a6b0f74862f98136c60dbba616de99e4f)`()` {#classshogun_1_1CPCA_1a6b0f74862f98136c60dbba616de99e4f}

destructor

#### `public virtual void `[`fit`](#classshogun_1_1CPCA_1a92c77f552b5c903eb6dde3b739556075)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * features)` {#classshogun_1_1CPCA_1a92c77f552b5c903eb6dde3b739556075}

Fit transformer to features 
#### Parameters
* `features` the training features

#### `public virtual void `[`cleanup`](#classshogun_1_1CPCA_1a4b66d5e31b5dc18b314c8a68163263bd)`()` {#classshogun_1_1CPCA_1a4b66d5e31b5dc18b314c8a68163263bd}

cleanup

#### `public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`apply_to_feature_vector`](#classshogun_1_1CPCA_1a45584b03dc12df6e0e4e3d266e1810ef)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > vector)` {#classshogun_1_1CPCA_1a45584b03dc12df6e0e4e3d266e1810ef}

apply preprocessor to feature vector 
#### Parameters
* `vector` feature vector 

#### Returns
processed feature vector

#### `public `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_transformation_matrix`](#classshogun_1_1CPCA_1acd1f9e21cdb441ef5d7567e167180a8e)`()` {#classshogun_1_1CPCA_1acd1f9e21cdb441ef5d7567e167180a8e}

get transformation matrix, i.e. eigenvectors (potentially scaled if do_whitening is true)

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_eigenvalues`](#classshogun_1_1CPCA_1a3572b0e224c79f48884f4af1b60307e1)`()` {#classshogun_1_1CPCA_1a3572b0e224c79f48884f4af1b60307e1}

get eigenvalues of PCA

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_mean`](#classshogun_1_1CPCA_1a92d96916c774173e59d8a960648ebd78)`()` {#classshogun_1_1CPCA_1a92d96916c774173e59d8a960648ebd78}

get mean vector of original data

#### `public inline virtual const char * `[`get_name`](#classshogun_1_1CPCA_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` {#classshogun_1_1CPCA_1a9cb485686dd7a1e6f7103cf42e87717e}

#### Returns
object name

#### `public inline virtual `[`EPreprocessorType`](#namespaceshogun_1af6317e92a2bed0d86257f3a589a5e9f3)` `[`get_type`](#classshogun_1_1CPCA_1afa592e9c6f9e700c293061fceaaac7f2)`() const` {#classshogun_1_1CPCA_1afa592e9c6f9e700c293061fceaaac7f2}

#### Returns
a type of preprocessor

#### `public `[`EPCAMemoryMode`](#namespaceshogun_1a374639d69db184f2509606cfea78b899)` `[`get_memory_mode`](#classshogun_1_1CPCA_1a8a76cc0a5fbcfb1af856d575485d66ed)`() const` {#classshogun_1_1CPCA_1a8a76cc0a5fbcfb1af856d575485d66ed}

return the PCA memory mode being used

#### `public void `[`set_memory_mode`](#classshogun_1_1CPCA_1a8df99c085206c29c5b65d1c51a7683b9)`(`[`EPCAMemoryMode`](#namespaceshogun_1a374639d69db184f2509606cfea78b899)` e)` {#classshogun_1_1CPCA_1a8df99c085206c29c5b65d1c51a7683b9}

set PCA memory mode to be used 
#### Parameters
* `e` hoice between MEM_REALLOCATE and MEM_IN_PLACE

#### `public void `[`set_eigenvalue_zero_tolerance`](#classshogun_1_1CPCA_1a050b824111b3d827b92e1dabced63df4)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` eigenvalue_zero_tolerance)` {#classshogun_1_1CPCA_1a050b824111b3d827b92e1dabced63df4}

set zero tolerance of eigenvalues during data whitening 
#### Parameters
* `eigenvalue_zero_tolerance` zero tolerance value

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_eigenvalue_zero_tolerance`](#classshogun_1_1CPCA_1af3296418fd90ad632dc093f24fe95a16)`() const` {#classshogun_1_1CPCA_1af3296418fd90ad632dc093f24fe95a16}

get zero tolerance of eigenvalues during data whitening 
#### Returns
zero tolerance value

#### `public void `[`set_target_dim`](#classshogun_1_1CPCA_1a626c39e21bb5842525ea02561084dc00)`(int32_t dim)` {#classshogun_1_1CPCA_1a626c39e21bb5842525ea02561084dc00}

setter for target dimension 
#### Parameters
* `dim` target dimension

#### `public int32_t `[`get_target_dim`](#classshogun_1_1CPCA_1abc02f1d05f1877d5b2b16b1c9482e5fb)`() const` {#classshogun_1_1CPCA_1abc02f1d05f1877d5b2b16b1c9482e5fb}

getter for target dimension 
#### Returns
target dimension

#### `public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`transform`](#classshogun_1_1CDensePreprocessor_1a801a3d5a27cc8ad45c887a93e768a987)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * features,bool inplace)` {#classshogun_1_1CDensePreprocessor_1a801a3d5a27cc8ad45c887a93e768a987}

Apply transformation to dense features.

#### Parameters
* `features` the dense input features 

* `inplace` whether transform in place 

#### Returns
the result feature object after applying the preprocessor

#### `public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`inverse_transform`](#classshogun_1_1CDensePreprocessor_1aea5d40ee0debdddaa64170453f7afea5)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * features,bool inplace)` {#classshogun_1_1CDensePreprocessor_1aea5d40ee0debdddaa64170453f7afea5}

Apply inverse transformation to dense features.

#### Parameters
* `features` the dense input features 

* `inplace` whether transform in place 

#### Returns
the result feature object after inverse applying the preprocessor

#### `public virtual `[`EFeatureClass`](#namespaceshogun_1a9e2a4d8b86b9e061779c3fdbcda57c3b)` `[`get_feature_class`](#classshogun_1_1CDensePreprocessor_1a00c0270aae194f8c691f0bd5e897e716)`()` {#classshogun_1_1CDensePreprocessor_1a00c0270aae194f8c691f0bd5e897e716}

return that we are dense features (just fixed size matrices)

#### `public virtual `[`EFeatureType`](#namespaceshogun_1a064eec90e91f56435546d77f38c0b618)` `[`get_feature_type`](#classshogun_1_1CDensePreprocessor_1ac6916b730dc608dbccb96cd1b0bfa528)`()` {#classshogun_1_1CDensePreprocessor_1ac6916b730dc608dbccb96cd1b0bfa528}

return feature type

#### `public virtual `[`EFeatureType`](#namespaceshogun_1a064eec90e91f56435546d77f38c0b618)` `[`get_feature_type`](#classshogun_1_1CDensePreprocessor_1a5c2663373829bede6e18ef9f655b8fd3)`()` {#classshogun_1_1CDensePreprocessor_1a5c2663373829bede6e18ef9f655b8fd3}

#### Returns
type of objects preprocessor can deal with

#### `public inline virtual void `[`fit`](#classshogun_1_1CTransformer_1ac651a02333f3e64518cdfca084cec90b)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * features,`[`CLabels`](#classshogun_1_1CLabels)` * labels)` {#classshogun_1_1CTransformer_1ac651a02333f3e64518cdfca084cec90b}

Fit transformer to features and labels 
#### Parameters
* `features` the training features 

* `labels` the training labels

#### `public inline virtual bool `[`train_require_labels`](#classshogun_1_1CTransformer_1a47f97bf5de534202ae00e77e485f3740)`() const` {#classshogun_1_1CTransformer_1a47f97bf5de534202ae00e77e485f3740}

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

#### `protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_transformation_matrix`](#classshogun_1_1CPCA_1a79fc753072325f2447a10079e3d2cca0) {#classshogun_1_1CPCA_1a79fc753072325f2447a10079e3d2cca0}

transformation matrix

#### `protected int32_t `[`num_dim`](#classshogun_1_1CPCA_1a9f8d6c6b33c67688f6230e8db34d7d00) {#classshogun_1_1CPCA_1a9f8d6c6b33c67688f6230e8db34d7d00}

num dim

#### `protected int32_t `[`num_old_dim`](#classshogun_1_1CPCA_1af219bad49a5a7e5401f9565d5e0afeda) {#classshogun_1_1CPCA_1af219bad49a5a7e5401f9565d5e0afeda}

num old dim

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_mean_vector`](#classshogun_1_1CPCA_1a8483cfb64208abf02e32762a2c54e903) {#classshogun_1_1CPCA_1a8483cfb64208abf02e32762a2c54e903}

mean vector

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_eigenvalues_vector`](#classshogun_1_1CPCA_1a8d07af893a081ef32ef8534d6f9c7802) {#classshogun_1_1CPCA_1a8d07af893a081ef32ef8534d6f9c7802}

eigenvalues vector

#### `protected bool `[`m_whitening`](#classshogun_1_1CPCA_1aac3df5860d870a6ddfc4503cd60bb36e) {#classshogun_1_1CPCA_1aac3df5860d870a6ddfc4503cd60bb36e}

whitening

#### `protected `[`EPCAMode`](#namespaceshogun_1a071a8ca3a05606f4869ea52b7a7fa049)` `[`m_mode`](#classshogun_1_1CPCA_1a3b1b014e7c64b80c9e8edd750cf9f88b) {#classshogun_1_1CPCA_1a3b1b014e7c64b80c9e8edd750cf9f88b}

PCA mode

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_thresh`](#classshogun_1_1CPCA_1a24f0f29d1eba4c059a120abc137e369c) {#classshogun_1_1CPCA_1a24f0f29d1eba4c059a120abc137e369c}

thresh

#### `protected `[`EPCAMemoryMode`](#namespaceshogun_1a374639d69db184f2509606cfea78b899)` `[`m_mem_mode`](#classshogun_1_1CPCA_1abd88cf0b6512674efdba1cfd8a9bd8e9) {#classshogun_1_1CPCA_1abd88cf0b6512674efdba1cfd8a9bd8e9}

PCA memory mode

#### `protected `[`EPCAMethod`](#namespaceshogun_1a993bafb98a8a6d82925f9683f7a6eabf)` `[`m_method`](#classshogun_1_1CPCA_1abdf596f307570a48e6f55060b8b00352) {#classshogun_1_1CPCA_1abdf596f307570a48e6f55060b8b00352}

PCA method

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_eigenvalue_zero_tolerance`](#classshogun_1_1CPCA_1abbb746cb133d5e801e7d1430482286bf) {#classshogun_1_1CPCA_1abbb746cb133d5e801e7d1430482286bf}

eigenvalues within zero tolerance region are considered 0 while whitening to tackle numerical issues

#### `protected int32_t `[`m_target_dim`](#classshogun_1_1CPCA_1a5e3eefc4485af0a00c0b6b9d69eb5e38) {#classshogun_1_1CPCA_1a5e3eefc4485af0a00c0b6b9d69eb5e38}

target dimension

#### `protected bool `[`m_fitted`](#classshogun_1_1CTransformer_1ac7a9f470db2627f8ba58a3880fb34b2e) {#classshogun_1_1CTransformer_1ac7a9f470db2627f8ba58a3880fb34b2e}

#### `protected void `[`init`](#classshogun_1_1CPCA_1a02fd73d861ef2e4aabb38c0c9ff82947)`()` {#classshogun_1_1CPCA_1a02fd73d861ef2e4aabb38c0c9ff82947}

#### `protected virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`apply_to_matrix`](#classshogun_1_1CPCA_1a34a2b3c8cecffe4f7b64621ace8733e7)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > matrix)` {#classshogun_1_1CPCA_1a34a2b3c8cecffe4f7b64621ace8733e7}

Apply preprocessor on matrix. Subclasses should try to apply in place to avoid copying. 
#### Parameters
* `matrix` the input feature matrix 

#### Returns
the matrix after applying the preprocessor

#### `protected virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`inverse_apply_to_matrix`](#classshogun_1_1CDensePreprocessor_1a20690602d6f44cb26ba63e7c6e8aef23)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > matrix)` {#classshogun_1_1CDensePreprocessor_1a20690602d6f44cb26ba63e7c6e8aef23}

Inverse apply preprocessor on matrix. Subclasses should try to apply in place to avoid copying. 
#### Parameters
* `matrix` the input feature matrix 

#### Returns
the matrix after applying the preprocessor

#### `protected void `[`assert_fitted`](#classshogun_1_1CTransformer_1ae1679ea842202ddfa8825779c7912311)`() const` {#classshogun_1_1CTransformer_1ae1679ea842202ddfa8825779c7912311}

Check current transformer has been fitted, throw [NotFittedException](#classshogun_1_1NotFittedException) otherwise.

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

