---
classname: "shogun::CCustomMahalanobisDistance"
type: "class"
parents:
   - CRealDistance
---

# class `shogun::CCustomMahalanobisDistance` {#classshogun_1_1CCustomMahalanobisDistance}

```
class shogun::CCustomMahalanobisDistance
  : public CRealDistance
```

Class CustomMahalanobisDistance used to compute the distance between feature vectors $ \vec{x_i} $ and $ \vec{x_j} $ as $ (\vec{x_i} - \vec{x_j})^T \mathbf{M} (\vec{x_i} - \vec{x_j}) $, given the matrix $ \mathbf{M} $ which will be referred to as Mahalanobis matrix.

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
`public  `[`CCustomMahalanobisDistance`](#classshogun_1_1CCustomMahalanobisDistance_1acf6167eba0705513e530d0e8d57050a9)`()` | default constructor
`public  `[`CCustomMahalanobisDistance`](#classshogun_1_1CCustomMahalanobisDistance_1a074d948343fe481a243a631f84469161)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * l,`[`CFeatures`](#classshogun_1_1CFeatures)` * r,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > m)` | standard constructor
`public virtual  `[`~CCustomMahalanobisDistance`](#classshogun_1_1CCustomMahalanobisDistance_1a190a1b4e1749e77819315e525aba1f05)`()` | destructor
`public virtual void `[`cleanup`](#classshogun_1_1CCustomMahalanobisDistance_1a4b66d5e31b5dc18b314c8a68163263bd)`()` | cleanup distance, here only because it is abstract in [CDistance](#classshogun_1_1CDistance). It does nothing
`public virtual const char * `[`get_name`](#classshogun_1_1CCustomMahalanobisDistance_1a635420c59837dceb825845c2301c6db8)`() const` | #### Returns
`public virtual `[`EDistanceType`](#namespaceshogun_1abd13d51eb89a564855252691bebca9bf)` `[`get_distance_type`](#classshogun_1_1CCustomMahalanobisDistance_1a80a5dc4c10af400e982db8c6275984d9)`()` | get distance type
`public inline virtual bool `[`init`](#classshogun_1_1CRealDistance_1abbc0c5c395db2eef959417242bf5853e)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * l,`[`CFeatures`](#classshogun_1_1CFeatures)` * r)` | init distance
`public inline virtual `[`EFeatureType`](#namespaceshogun_1a064eec90e91f56435546d77f38c0b618)` `[`get_feature_type`](#classshogun_1_1CRealDistance_1ac6916b730dc608dbccb96cd1b0bfa528)`()` | get feature type the distance can deal with
`public inline virtual `[`EFeatureClass`](#namespaceshogun_1a9e2a4d8b86b9e061779c3fdbcda57c3b)` `[`get_feature_class`](#classshogun_1_1CDenseDistance_1a8d0329d5baef949e5c640bb18ff7aae5)`()` | get feature class the distance can deal with
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`distance`](#classshogun_1_1CDistance_1a2671d0f623d6495e4aaf2fffae022fa3)`(int32_t idx_a,int32_t idx_b)` | get distance function for lhs feature vector a and rhs feature vector b
`public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`distance_upper_bounded`](#classshogun_1_1CDistance_1ac40d441939fab88fc6d96159f7b535c0)`(int32_t idx_a,int32_t idx_b,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` upper_bound)` | get distance function for lhs feature vector a and rhs feature vector b. The computation of the distance stops if the intermediate result is larger than upper_bound. This is useful to use with John Langford's Cover Tree and it is ONLY implemented for Euclidean distance
`public inline virtual void `[`precompute_rhs`](#classshogun_1_1CDistance_1a25a94d2c2fc599b286417b11553ce8b4)`()` | Precomputation related to features of right hand side WARNING : Make sure to reset computations using [reset_precompute()](#classshogun_1_1CDistance_1a224d4df57b2bcc24b3a00b349590954b) when features or feature matrix are changed. This method is empty, should be overloaded in derived class.
`public inline virtual void `[`precompute_lhs`](#classshogun_1_1CDistance_1a32f02eac3c8d17a69cabfe554ef2001d)`()` | Precomputation related to features of left hand side WARNING : Make sure to reset computations using [reset_precompute()](#classshogun_1_1CDistance_1a224d4df57b2bcc24b3a00b349590954b) when features or feature matrix are changed. This method is empty, should be overloaded in derived class.
`public inline virtual void `[`reset_precompute`](#classshogun_1_1CDistance_1a224d4df57b2bcc24b3a00b349590954b)`()` | Reset precomputations for features of both sides Should be used to reset whenever features or feature matrix are changed. This method is empty, should be overloaded in derived class.
`public inline `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_distance_matrix`](#classshogun_1_1CDistance_1a635930bf7269ae837be1f6e0b1d454cd)`()` | get distance matrix
`public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`get_distance_matrix`](#classshogun_1_1CDistance_1a36155309cd3d010aed7fa2593fcac916)`()` | get distance matrix (templated)
`public inline int32_t `[`compute_row_start`](#classshogun_1_1CDistance_1a8476cd069409e0b64c2fe6099e07cfcb)`(int64_t offs,int32_t n,bool symmetric)` | compute row start offset for parallel kernel matrix computation
`public void `[`load`](#classshogun_1_1CDistance_1a5d33ec59a4be25056cca1f3b6691ad00)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` | load the kernel matrix
`public void `[`save`](#classshogun_1_1CDistance_1a2ec11d78c7f60dfbc77bc2f56d211033)`(`[`CFile`](#classshogun_1_1CFile)` * writer)` | save kernel matrix
`public inline `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`get_lhs`](#classshogun_1_1CDistance_1aa3e521f9c3df80da4bc44c2ba0b6c0be)`()` | get left-hand side features used in distance matrix
`public inline `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`get_rhs`](#classshogun_1_1CDistance_1a28c50c34fc59a74f2b015ba87dc133d9)`()` | get right-hand side features used in distance matrix
`public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`replace_rhs`](#classshogun_1_1CDistance_1a976d9eaf32a5eb81c8e3db7899e60e58)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * rhs)` | replace right-hand side features used in distance matrix
`public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`replace_lhs`](#classshogun_1_1CDistance_1ab9dc6b5d4b13a22145b6e931c1246c58)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * lhs)` | replace left-hand side features used in distance matrix
`public virtual void `[`remove_lhs_and_rhs`](#classshogun_1_1CDistance_1a69d2fffafdc0984cea96e3f4a4f737cb)`()` | remove lhs and rhs from distance
`public virtual void `[`remove_lhs`](#classshogun_1_1CDistance_1a214e795fd785274e29d97d4b16aa6fc4)`()` | takes all necessary steps if the lhs is removed from distance matrix
`public virtual void `[`remove_rhs`](#classshogun_1_1CDistance_1af6c99208795e1ff43d204e3e5adb78ec)`()` | takes all necessary steps if the rhs is removed from distance matrix
`public inline bool `[`get_precompute_matrix`](#classshogun_1_1CDistance_1a5f0a9460e1dd25becf8c36ee98303b2e)`()` | FIXME: precompute matrix should be dropped, handling should be via customdistance
`public inline virtual void `[`set_precompute_matrix`](#classshogun_1_1CDistance_1a15c399a4bd6dba711e1f9dda8a5180a9)`(bool flag)` | FIXME: precompute matrix should be dropped, handling should be via customdistance
`public inline virtual int32_t `[`get_num_vec_lhs`](#classshogun_1_1CDistance_1af81140e34d38612802e1b8783424260a)`()` | get number of vectors of lhs features
`public inline virtual int32_t `[`get_num_vec_rhs`](#classshogun_1_1CDistance_1aabc415a305914c27567a1343f7957cac)`()` | get number of vectors of rhs features
`public inline virtual bool `[`has_features`](#classshogun_1_1CDistance_1abcd71e362bf0042668c5527e17968fe6)`()` | test whether features have been assigned to lhs and rhs
`public inline bool `[`lhs_equals_rhs`](#classshogun_1_1CDistance_1a1b87103224ffb38549a4b17e1f06e84f)`()` | test whether features on lhs and rhs are the same
`public void `[`run_distance_rhs`](#classshogun_1_1CDistance_1a998a2d08cb8004b16335f3a6ff2c40b2)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > & result,const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` idx_r_start,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` idx_start,const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` idx_stop,const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` idx_a)` | Function for computing distance values
`public void `[`run_distance_lhs`](#classshogun_1_1CDistance_1a6af8774620d9ef70946a0b2f5858fd0d)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > & result,const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` idx_r_start,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` idx_start,const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` idx_stop,const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` idx_b)` | Function for computing distance values
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
`protected `[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * `[`precomputed_matrix`](#classshogun_1_1CDistance_1a1c6bff72cc869dbc8b8e42ed8b87952c) | FIXME: precompute matrix should be dropped, handling should be via customdistance
`protected bool `[`precompute_matrix`](#classshogun_1_1CDistance_1aad9b7603ed8e4fca708b69a6a548695c) | FIXME: precompute matrix should be dropped, handling should be via customdistance
`protected `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`lhs`](#classshogun_1_1CDistance_1a5bb6375a26075c34dc856a477828ad52) | feature vectors to occur on the left hand side
`protected `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`rhs`](#classshogun_1_1CDistance_1a8e375dd40df7b063ba9f2da598e1a3a9) | feature vectors to occur on the right hand side
`protected int32_t `[`num_lhs`](#classshogun_1_1CDistance_1ac6a6d53fdb5fd47fffd56b1b03d41e09) | number of feature vectors on the left hand side
`protected int32_t `[`num_rhs`](#classshogun_1_1CDistance_1a84e7d5029b76c7b2b5903c6600adc036) | number of feature vectors on the right hand side
`protected virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute`](#classshogun_1_1CCustomMahalanobisDistance_1ad7ca3fc200d88ca7dc4cab77723e3eea)`(int32_t idx_a,int32_t idx_b)` | compute distance between feature idx_a in lhs features and feature idx_b in rhs features
`protected void `[`do_precompute_matrix`](#classshogun_1_1CDistance_1a5a630425f711927c6e07fc05ae383078)`()` | matrix precomputation
`protected virtual bool `[`check_compatibility`](#classshogun_1_1CDistance_1ad8b2d4c6b0697d0fcfe3b254ec0622db)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * l,`[`CFeatures`](#classshogun_1_1CFeatures)` * r)` | Checks the compatibility between two supplied features
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

#### `public  `[`CCustomMahalanobisDistance`](#classshogun_1_1CCustomMahalanobisDistance_1acf6167eba0705513e530d0e8d57050a9)`()` {#classshogun_1_1CCustomMahalanobisDistance_1acf6167eba0705513e530d0e8d57050a9}

default constructor

#### `public  `[`CCustomMahalanobisDistance`](#classshogun_1_1CCustomMahalanobisDistance_1a074d948343fe481a243a631f84469161)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * l,`[`CFeatures`](#classshogun_1_1CFeatures)` * r,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > m)` {#classshogun_1_1CCustomMahalanobisDistance_1a074d948343fe481a243a631f84469161}

standard constructor

#### Parameters
* `l` features of left hand side 

* `r` features of right hand side 

* `m` Mahalanobis matrix used to compute distances

#### `public virtual  `[`~CCustomMahalanobisDistance`](#classshogun_1_1CCustomMahalanobisDistance_1a190a1b4e1749e77819315e525aba1f05)`()` {#classshogun_1_1CCustomMahalanobisDistance_1a190a1b4e1749e77819315e525aba1f05}

destructor

#### `public virtual void `[`cleanup`](#classshogun_1_1CCustomMahalanobisDistance_1a4b66d5e31b5dc18b314c8a68163263bd)`()` {#classshogun_1_1CCustomMahalanobisDistance_1a4b66d5e31b5dc18b314c8a68163263bd}

cleanup distance, here only because it is abstract in [CDistance](#classshogun_1_1CDistance). It does nothing

#### `public virtual const char * `[`get_name`](#classshogun_1_1CCustomMahalanobisDistance_1a635420c59837dceb825845c2301c6db8)`() const` {#classshogun_1_1CCustomMahalanobisDistance_1a635420c59837dceb825845c2301c6db8}

#### Returns
name of SGSerializable

#### `public virtual `[`EDistanceType`](#namespaceshogun_1abd13d51eb89a564855252691bebca9bf)` `[`get_distance_type`](#classshogun_1_1CCustomMahalanobisDistance_1a80a5dc4c10af400e982db8c6275984d9)`()` {#classshogun_1_1CCustomMahalanobisDistance_1a80a5dc4c10af400e982db8c6275984d9}

get distance type

#### Returns
distance type CUSTOMMAHALANOBIS

#### `public inline virtual bool `[`init`](#classshogun_1_1CRealDistance_1abbc0c5c395db2eef959417242bf5853e)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * l,`[`CFeatures`](#classshogun_1_1CFeatures)` * r)` {#classshogun_1_1CRealDistance_1abbc0c5c395db2eef959417242bf5853e}

init distance

#### Parameters
* `l` features of left-hand side 

* `r` features of right-hand side 

#### Returns
if init was successful

#### `public inline virtual `[`EFeatureType`](#namespaceshogun_1a064eec90e91f56435546d77f38c0b618)` `[`get_feature_type`](#classshogun_1_1CRealDistance_1ac6916b730dc608dbccb96cd1b0bfa528)`()` {#classshogun_1_1CRealDistance_1ac6916b730dc608dbccb96cd1b0bfa528}

get feature type the distance can deal with

#### Returns
feature type DREAL

#### `public inline virtual `[`EFeatureClass`](#namespaceshogun_1a9e2a4d8b86b9e061779c3fdbcda57c3b)` `[`get_feature_class`](#classshogun_1_1CDenseDistance_1a8d0329d5baef949e5c640bb18ff7aae5)`()` {#classshogun_1_1CDenseDistance_1a8d0329d5baef949e5c640bb18ff7aae5}

get feature class the distance can deal with

#### Returns
feature class DENSE

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`distance`](#classshogun_1_1CDistance_1a2671d0f623d6495e4aaf2fffae022fa3)`(int32_t idx_a,int32_t idx_b)` {#classshogun_1_1CDistance_1a2671d0f623d6495e4aaf2fffae022fa3}

get distance function for lhs feature vector a and rhs feature vector b

#### Parameters
* `idx_a` feature vector a at idx_a 

* `idx_b` feature vector b at idx_b 

#### Returns
distance value

#### `public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`distance_upper_bounded`](#classshogun_1_1CDistance_1ac40d441939fab88fc6d96159f7b535c0)`(int32_t idx_a,int32_t idx_b,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` upper_bound)` {#classshogun_1_1CDistance_1ac40d441939fab88fc6d96159f7b535c0}

get distance function for lhs feature vector a and rhs feature vector b. The computation of the distance stops if the intermediate result is larger than upper_bound. This is useful to use with John Langford's Cover Tree and it is ONLY implemented for Euclidean distance

#### Parameters
* `idx_a` feature vector a at idx_a 

* `idx_b` feature vector b at idx_b 

* `upper_bound` value above which the computation halts 

#### Returns
distance value or upper_bound

#### `public inline virtual void `[`precompute_rhs`](#classshogun_1_1CDistance_1a25a94d2c2fc599b286417b11553ce8b4)`()` {#classshogun_1_1CDistance_1a25a94d2c2fc599b286417b11553ce8b4}

Precomputation related to features of right hand side WARNING : Make sure to reset computations using [reset_precompute()](#classshogun_1_1CDistance_1a224d4df57b2bcc24b3a00b349590954b) when features or feature matrix are changed. This method is empty, should be overloaded in derived class.

#### `public inline virtual void `[`precompute_lhs`](#classshogun_1_1CDistance_1a32f02eac3c8d17a69cabfe554ef2001d)`()` {#classshogun_1_1CDistance_1a32f02eac3c8d17a69cabfe554ef2001d}

Precomputation related to features of left hand side WARNING : Make sure to reset computations using [reset_precompute()](#classshogun_1_1CDistance_1a224d4df57b2bcc24b3a00b349590954b) when features or feature matrix are changed. This method is empty, should be overloaded in derived class.

#### `public inline virtual void `[`reset_precompute`](#classshogun_1_1CDistance_1a224d4df57b2bcc24b3a00b349590954b)`()` {#classshogun_1_1CDistance_1a224d4df57b2bcc24b3a00b349590954b}

Reset precomputations for features of both sides Should be used to reset whenever features or feature matrix are changed. This method is empty, should be overloaded in derived class.

#### `public inline `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_distance_matrix`](#classshogun_1_1CDistance_1a635930bf7269ae837be1f6e0b1d454cd)`()` {#classshogun_1_1CDistance_1a635930bf7269ae837be1f6e0b1d454cd}

get distance matrix

#### Returns
computed distance matrix (needs to be cleaned up)

#### `public template<>`  <br/>[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`get_distance_matrix`](#classshogun_1_1CDistance_1a36155309cd3d010aed7fa2593fcac916)`()` {#classshogun_1_1CDistance_1a36155309cd3d010aed7fa2593fcac916}

get distance matrix (templated)

#### Returns
the distance matrix

#### `public inline int32_t `[`compute_row_start`](#classshogun_1_1CDistance_1a8476cd069409e0b64c2fe6099e07cfcb)`(int64_t offs,int32_t n,bool symmetric)` {#classshogun_1_1CDistance_1a8476cd069409e0b64c2fe6099e07cfcb}

compute row start offset for parallel kernel matrix computation

#### Parameters
* `offs` offset 

* `n` number of columns 

* `symmetric` whether matrix is symmetric

#### `public void `[`load`](#classshogun_1_1CDistance_1a5d33ec59a4be25056cca1f3b6691ad00)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` {#classshogun_1_1CDistance_1a5d33ec59a4be25056cca1f3b6691ad00}

load the kernel matrix

#### Parameters
* `loader` File object via which to load data

#### `public void `[`save`](#classshogun_1_1CDistance_1a2ec11d78c7f60dfbc77bc2f56d211033)`(`[`CFile`](#classshogun_1_1CFile)` * writer)` {#classshogun_1_1CDistance_1a2ec11d78c7f60dfbc77bc2f56d211033}

save kernel matrix

#### Parameters
* `writer` File object via which to save data

#### `public inline `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`get_lhs`](#classshogun_1_1CDistance_1aa3e521f9c3df80da4bc44c2ba0b6c0be)`()` {#classshogun_1_1CDistance_1aa3e521f9c3df80da4bc44c2ba0b6c0be}

get left-hand side features used in distance matrix

#### Returns
left-hand side features

#### `public inline `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`get_rhs`](#classshogun_1_1CDistance_1a28c50c34fc59a74f2b015ba87dc133d9)`()` {#classshogun_1_1CDistance_1a28c50c34fc59a74f2b015ba87dc133d9}

get right-hand side features used in distance matrix

#### Returns
right-hand side features

#### `public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`replace_rhs`](#classshogun_1_1CDistance_1a976d9eaf32a5eb81c8e3db7899e60e58)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * rhs)` {#classshogun_1_1CDistance_1a976d9eaf32a5eb81c8e3db7899e60e58}

replace right-hand side features used in distance matrix

make sure to check that your distance can deal with the supplied features (!)

#### Parameters
* `rhs` features of right-hand side 

#### Returns
replaced right-hand side features

#### `public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`replace_lhs`](#classshogun_1_1CDistance_1ab9dc6b5d4b13a22145b6e931c1246c58)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * lhs)` {#classshogun_1_1CDistance_1ab9dc6b5d4b13a22145b6e931c1246c58}

replace left-hand side features used in distance matrix

make sure to check that your distance can deal with the supplied features (!)

#### Parameters
* `lhs` features of right-hand side 

#### Returns
replaced left-hand side features

#### `public virtual void `[`remove_lhs_and_rhs`](#classshogun_1_1CDistance_1a69d2fffafdc0984cea96e3f4a4f737cb)`()` {#classshogun_1_1CDistance_1a69d2fffafdc0984cea96e3f4a4f737cb}

remove lhs and rhs from distance

#### `public virtual void `[`remove_lhs`](#classshogun_1_1CDistance_1a214e795fd785274e29d97d4b16aa6fc4)`()` {#classshogun_1_1CDistance_1a214e795fd785274e29d97d4b16aa6fc4}

takes all necessary steps if the lhs is removed from distance matrix

#### `public virtual void `[`remove_rhs`](#classshogun_1_1CDistance_1af6c99208795e1ff43d204e3e5adb78ec)`()` {#classshogun_1_1CDistance_1af6c99208795e1ff43d204e3e5adb78ec}

takes all necessary steps if the rhs is removed from distance matrix

takes all necessary steps if the rhs is removed from distance

#### `public inline bool `[`get_precompute_matrix`](#classshogun_1_1CDistance_1a5f0a9460e1dd25becf8c36ee98303b2e)`()` {#classshogun_1_1CDistance_1a5f0a9460e1dd25becf8c36ee98303b2e}

FIXME: precompute matrix should be dropped, handling should be via customdistance

#### Returns
if precompute_matrix

#### `public inline virtual void `[`set_precompute_matrix`](#classshogun_1_1CDistance_1a15c399a4bd6dba711e1f9dda8a5180a9)`(bool flag)` {#classshogun_1_1CDistance_1a15c399a4bd6dba711e1f9dda8a5180a9}

FIXME: precompute matrix should be dropped, handling should be via customdistance

#### Parameters
* `flag` if precompute_matrix

#### `public inline virtual int32_t `[`get_num_vec_lhs`](#classshogun_1_1CDistance_1af81140e34d38612802e1b8783424260a)`()` {#classshogun_1_1CDistance_1af81140e34d38612802e1b8783424260a}

get number of vectors of lhs features

#### Returns
number of vectors of left-hand side

#### `public inline virtual int32_t `[`get_num_vec_rhs`](#classshogun_1_1CDistance_1aabc415a305914c27567a1343f7957cac)`()` {#classshogun_1_1CDistance_1aabc415a305914c27567a1343f7957cac}

get number of vectors of rhs features

#### Returns
number of vectors of right-hand side

#### `public inline virtual bool `[`has_features`](#classshogun_1_1CDistance_1abcd71e362bf0042668c5527e17968fe6)`()` {#classshogun_1_1CDistance_1abcd71e362bf0042668c5527e17968fe6}

test whether features have been assigned to lhs and rhs

#### Returns
true if features are assigned

#### `public inline bool `[`lhs_equals_rhs`](#classshogun_1_1CDistance_1a1b87103224ffb38549a4b17e1f06e84f)`()` {#classshogun_1_1CDistance_1a1b87103224ffb38549a4b17e1f06e84f}

test whether features on lhs and rhs are the same

#### Returns
true if features are the same

#### `public void `[`run_distance_rhs`](#classshogun_1_1CDistance_1a998a2d08cb8004b16335f3a6ff2c40b2)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > & result,const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` idx_r_start,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` idx_start,const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` idx_stop,const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` idx_a)` {#classshogun_1_1CDistance_1a998a2d08cb8004b16335f3a6ff2c40b2}

Function for computing distance values

#### Parameters
* `result` array of distance values 

* `idx_r_start` iteration start value 

* `idx_start` start 

* `idx_stop` iteration end value 

* `idx_a` feature vector a at idx_a

#### `public void `[`run_distance_lhs`](#classshogun_1_1CDistance_1a6af8774620d9ef70946a0b2f5858fd0d)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > & result,const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` idx_r_start,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` idx_start,const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` idx_stop,const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` idx_b)` {#classshogun_1_1CDistance_1a6af8774620d9ef70946a0b2f5858fd0d}

Function for computing distance values

#### Parameters
* `result` array of distance values 

* `idx_r_start` iteration start value 

* `idx_start` start 

* `idx_stop` iteration end value 

* `idx_b` feature vector b at idx_b

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

#### `protected `[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * `[`precomputed_matrix`](#classshogun_1_1CDistance_1a1c6bff72cc869dbc8b8e42ed8b87952c) {#classshogun_1_1CDistance_1a1c6bff72cc869dbc8b8e42ed8b87952c}

FIXME: precompute matrix should be dropped, handling should be via customdistance

#### `protected bool `[`precompute_matrix`](#classshogun_1_1CDistance_1aad9b7603ed8e4fca708b69a6a548695c) {#classshogun_1_1CDistance_1aad9b7603ed8e4fca708b69a6a548695c}

FIXME: precompute matrix should be dropped, handling should be via customdistance

#### `protected `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`lhs`](#classshogun_1_1CDistance_1a5bb6375a26075c34dc856a477828ad52) {#classshogun_1_1CDistance_1a5bb6375a26075c34dc856a477828ad52}

feature vectors to occur on the left hand side

#### `protected `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`rhs`](#classshogun_1_1CDistance_1a8e375dd40df7b063ba9f2da598e1a3a9) {#classshogun_1_1CDistance_1a8e375dd40df7b063ba9f2da598e1a3a9}

feature vectors to occur on the right hand side

#### `protected int32_t `[`num_lhs`](#classshogun_1_1CDistance_1ac6a6d53fdb5fd47fffd56b1b03d41e09) {#classshogun_1_1CDistance_1ac6a6d53fdb5fd47fffd56b1b03d41e09}

number of feature vectors on the left hand side

#### `protected int32_t `[`num_rhs`](#classshogun_1_1CDistance_1a84e7d5029b76c7b2b5903c6600adc036) {#classshogun_1_1CDistance_1a84e7d5029b76c7b2b5903c6600adc036}

number of feature vectors on the right hand side

#### `protected virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute`](#classshogun_1_1CCustomMahalanobisDistance_1ad7ca3fc200d88ca7dc4cab77723e3eea)`(int32_t idx_a,int32_t idx_b)` {#classshogun_1_1CCustomMahalanobisDistance_1ad7ca3fc200d88ca7dc4cab77723e3eea}

compute distance between feature idx_a in lhs features and feature idx_b in rhs features

#### Parameters
* `idx_a` feature vector in lhs at idx_a 

* `idx_b` feature vector in rhs at idx_b

#### Returns
distance value

#### `protected void `[`do_precompute_matrix`](#classshogun_1_1CDistance_1a5a630425f711927c6e07fc05ae383078)`()` {#classshogun_1_1CDistance_1a5a630425f711927c6e07fc05ae383078}

matrix precomputation

#### `protected virtual bool `[`check_compatibility`](#classshogun_1_1CDistance_1ad8b2d4c6b0697d0fcfe3b254ec0622db)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * l,`[`CFeatures`](#classshogun_1_1CFeatures)` * r)` {#classshogun_1_1CDistance_1ad8b2d4c6b0697d0fcfe3b254ec0622db}

Checks the compatibility between two supplied features

#### Parameters
* `l` left hand side features 

* `r` right hand side features 

#### Returns
true if the features are compatible

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

