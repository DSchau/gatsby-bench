---
classname: "shogun::CLSHKNNSolver"
type: "class"
parents:
   - CKNNSolver
---

# class `shogun::CLSHKNNSolver` {#classshogun_1_1CLSHKNNSolver}

```
class shogun::CLSHKNNSolver
  : public CKNNSolver
```

LSH solver. It uses LSH (short for Locality-sensitive hashing) to do the nearest neighbour computation. For more information, see [https://en.wikipedia.org/wiki/Locality-sensitive_hashing](https://en.wikipedia.org/wiki/Locality-sensitive_hashing).

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
`public inline  `[`CLSHKNNSolver`](#classshogun_1_1CLSHKNNSolver_1a9d47cb8069d51d24b20fc410018b7034)`()` | default constructor
`public inline virtual  `[`~CLSHKNNSolver`](#classshogun_1_1CLSHKNNSolver_1abfd6eeffdfe04ce5ab5725b999a6e565)`()` | deconstructor
`public  `[`CLSHKNNSolver`](#classshogun_1_1CLSHKNNSolver_1a5479701288bca5fcaa7239e50112e0fb)`(const int32_t k,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` q,const int32_t num_classes,const int32_t min_label,const `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > train_labels,const int32_t lsh_l,const int32_t lsh_t)` | constructor
`public virtual `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * `[`classify_objects`](#classshogun_1_1CLSHKNNSolver_1a828173dccaa7d9f27a2aa159972a3dee)`(`[`CDistance`](#classshogun_1_1CDistance)` * d,const int32_t num_lab,`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > & train_lab,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > & classes) const` | classify objects, and the implementation will depended on which knn solver been choosen.
`public virtual `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`classify_objects_k`](#classshogun_1_1CLSHKNNSolver_1a9743c709d04f7e5aa51bf07ac7ac5208)`(`[`CDistance`](#classshogun_1_1CDistance)` * d,const int32_t num_lab,`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > & train_lab,`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > & classes) const` | classify all objects, and the implementation will depended on which knn solver been choosen. 
`public inline virtual const char * `[`get_name`](#classshogun_1_1CLSHKNNSolver_1a272dda5e08548168f78061e194511fcf)`() const` | #### Returns
`public int32_t `[`choose_class`](#classshogun_1_1CKNNSolver_1a2aed3e304c1018f9852ace96ed1cc5bd)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * classes,const int32_t * train_lab) const` | compute the histogram of class outputs of the k nearest neighbors to a test vector and return the index of the most frequent class
`public void `[`choose_class_for_multiple_k`](#classshogun_1_1CKNNSolver_1a9d8bc323fb6d6988685d793eb25a0318)`(int32_t * output,int32_t * classes,const int32_t * train_lab,const int32_t step) const` | compute the histogram of class outputs of the k nearest neighbors to a test vector, using k from 1 to m_k, and write the most frequent class for each value of k in output, using a distance equal to step between elements in the output array
`public void `[`set_distance`](#classshogun_1_1CDistanceMachine_1a50595af6ab3dd6d473573eaa1f9180c3)`(`[`CDistance`](#classshogun_1_1CDistance)` * d)` | set distance
`public `[`CDistance`](#classshogun_1_1CDistance)` * `[`get_distance`](#classshogun_1_1CDistanceMachine_1a92b769f193204c8f3b2da018fbf20139)`() const` | get distance
`public void `[`distances_lhs`](#classshogun_1_1CDistanceMachine_1acd9eec8936c081242aa34c1b2518cab3)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > & result,int32_t idx_a1,int32_t idx_a2,int32_t idx_b)` | get distance functions for lhs feature vectors going from a1 to a2 and rhs feature vector b
`public void `[`distances_rhs`](#classshogun_1_1CDistanceMachine_1a0684453cfcb00efb86dbb70612192177)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > & result,int32_t idx_b1,int32_t idx_b2,int32_t idx_a)` | get distance functions for rhs feature vectors going from b1 to b2 and lhs feature vector a
`public virtual `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * `[`apply_multiclass`](#classshogun_1_1CDistanceMachine_1a250aa566fff0edb31433db98f70a7f15)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | Classify all provided features. Cluster index with smallest distance to to be classified element is returned
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`apply_one`](#classshogun_1_1CDistanceMachine_1a541d70682e317105112ba75d3d03624a)`(int32_t num)` | Apply machine to one example. Cluster index with smallest distance to to be classified element is returned
`public virtual bool `[`train`](#classshogun_1_1CMachine_1aa0ece9fd14892c6dfed1bb8c78f3b3ed)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | train machine
`public virtual bool `[`train_locked`](#classshogun_1_1CMachine_1aab4927bdae8da7f0c85efdfce22c86c2)`()` | Trains a locked machine on a set of indices. Error if machine is not locked 
`public inline virtual bool `[`train_locked`](#classshogun_1_1CMachine_1a6211015eaf19161e4c469c8ff38bfeba)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | Trains a locked machine on a set of indices. Error if machine is not locked
`public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`apply`](#classshogun_1_1CMachine_1afd5d402257972c78456594234d13eb4c)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data if data is not specified apply to the current features
`public virtual `[`CBinaryLabels`](#classshogun_1_1CBinaryLabels)` * `[`apply_binary`](#classshogun_1_1CMachine_1a16a7dee83bb61aedc93792df578d4a77)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data in means of binary classification problem
`public virtual `[`CRegressionLabels`](#classshogun_1_1CRegressionLabels)` * `[`apply_regression`](#classshogun_1_1CMachine_1aaeea92e0e4795e7f63f067c16f162302)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data in means of regression problem
`public virtual `[`CStructuredLabels`](#classshogun_1_1CStructuredLabels)` * `[`apply_structured`](#classshogun_1_1CMachine_1a588efa92a0696e1d2a61a8cd21d8ebee)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data in means of SO classification problem
`public virtual `[`CLatentLabels`](#classshogun_1_1CLatentLabels)` * `[`apply_latent`](#classshogun_1_1CMachine_1a276d23b37202ecb31367df26a5600cf7)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data in means of latent problem
`public virtual void `[`set_labels`](#classshogun_1_1CMachine_1a5f0cfd09e37bd5e793cacecb8d3c818b)`(`[`CLabels`](#classshogun_1_1CLabels)` * lab)` | set labels
`public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`get_labels`](#classshogun_1_1CMachine_1a065f0797777044cb0dbf786781982e3d)`()` | get labels
`public void `[`set_max_train_time`](#classshogun_1_1CMachine_1af660b1b03c475c3c638d2c995ea4b54a)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` t)` | set maximum training time
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_max_train_time`](#classshogun_1_1CMachine_1a7c75c86ff1cfd61d8275e62f0477d797)`()` | get maximum training time
`public virtual `[`EMachineType`](#namespaceshogun_1af181c832c12de7a0c3b02425986106cc)` `[`get_classifier_type`](#classshogun_1_1CMachine_1a177dc18a9a5639da395099947cb44501)`()` | get classifier type
`public void `[`set_solver_type`](#classshogun_1_1CMachine_1af8876022111114d5d3b0579ee161a8ff)`(`[`ESolverType`](#namespaceshogun_1af43428a9cb6c6de54cc7085c7c9b273e)` st)` | set solver type
`public `[`ESolverType`](#namespaceshogun_1af43428a9cb6c6de54cc7085c7c9b273e)` `[`get_solver_type`](#classshogun_1_1CMachine_1a97ee8b11465427d28498437279229ebe)`()` | get solver type
`public virtual void `[`set_store_model_features`](#classshogun_1_1CMachine_1a872d1cc0904edaa3c5701b049ee2993d)`(bool store_model)` | Setter for store-model-features-after-training flag
`public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`apply_locked`](#classshogun_1_1CMachine_1add0cb383e34472fdc66db18b0a5a4bc5)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | Applies a locked machine on a set of indices. Error if machine is not locked
`public virtual `[`CBinaryLabels`](#classshogun_1_1CBinaryLabels)` * `[`apply_locked_binary`](#classshogun_1_1CMachine_1ac417f13423c17ebd9b0aa742f5e78c4c)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | applies a locked machine on a set of indices for binary problems
`public virtual `[`CRegressionLabels`](#classshogun_1_1CRegressionLabels)` * `[`apply_locked_regression`](#classshogun_1_1CMachine_1a764464fca138ac17692cb994824a1d93)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | applies a locked machine on a set of indices for regression problems
`public virtual `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * `[`apply_locked_multiclass`](#classshogun_1_1CMachine_1a9a97b605764f96da5aaadda76a05d21d)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | applies a locked machine on a set of indices for multiclass problems
`public virtual `[`CStructuredLabels`](#classshogun_1_1CStructuredLabels)` * `[`apply_locked_structured`](#classshogun_1_1CMachine_1a8c63b6efbfe361a91794937f6fda544c)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | applies a locked machine on a set of indices for structured problems
`public virtual `[`CLatentLabels`](#classshogun_1_1CLatentLabels)` * `[`apply_locked_latent`](#classshogun_1_1CMachine_1ab4e951edb0bafda3d57fe80d648190d6)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | applies a locked machine on a set of indices for latent problems
`public virtual void `[`data_lock`](#classshogun_1_1CMachine_1a4006ffabe6a752081d3f0e2831ae0c6e)`(`[`CLabels`](#classshogun_1_1CLabels)` * labs,`[`CFeatures`](#classshogun_1_1CFeatures)` * features)` | Locks the machine on given labels and data. After this call, only train_locked and apply_locked may be called
`public inline virtual void `[`post_lock`](#classshogun_1_1CMachine_1a0ad27205b36008a86beb4da016ceef0d)`(`[`CLabels`](#classshogun_1_1CLabels)` * labs,`[`CFeatures`](#classshogun_1_1CFeatures)` * features)` | post lock
`public virtual void `[`data_unlock`](#classshogun_1_1CMachine_1a72933e4edad4e2daabeeafd9f1069e47)`()` | Unlocks a locked machine and restores previous state
`public inline virtual bool `[`supports_locking`](#classshogun_1_1CMachine_1a36e1fd34f65274fa2cf54c3c9b105fcb)`() const` | #### Returns
`public inline bool `[`is_data_locked`](#classshogun_1_1CMachine_1a2996bc9c87fd16414792bca4aa0a14ec)`() const` | #### Returns
`public inline virtual `[`EProblemType`](#namespaceshogun_1a0aa89aa872f89f6a174de2f45b7596d4)` `[`get_machine_problem_type`](#classshogun_1_1CMachine_1ac1c69755f623188143fc30188354a039)`() const` | returns type of problem machine solves
`public inline virtual bool `[`train_require_labels`](#classshogun_1_1CMachine_1a47f97bf5de534202ae00e77e485f3740)`() const` | returns whether machine require labels for training
`public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` bool `[`cancel_computation`](#classshogun_1_1CStoppableSGObject_1a107504a021e88eec67012e1706e062c5)`() const` | #### Returns
`public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` void `[`pause_computation`](#classshogun_1_1CStoppableSGObject_1a2168b46919701793fa1558393c30eab4)`()` | Pause the algorithm if the flag is set
`public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` void `[`resume_computation`](#classshogun_1_1CStoppableSGObject_1ab4c36831267ed4c90c5992b45ae33263)`()` | Resume current computation (sets the flag)
`public void `[`set_callback`](#classshogun_1_1CStoppableSGObject_1ab6f4a2a3e5df1521ef427e3fd63f0d21)`(std::function< bool()> callback)` | Set an additional stopping condition 
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
`protected int32_t `[`m_lsh_l`](#classshogun_1_1CLSHKNNSolver_1a4e290a0fb55debbb8e55365e4cd63fb9) | 
`protected int32_t `[`m_lsh_t`](#classshogun_1_1CLSHKNNSolver_1afd94e59c1256fd68de72236a12f08887) | 
`protected int32_t `[`m_k`](#classshogun_1_1CKNNSolver_1aaf848836021c575bd56c452475b53108) | the k parameter in KNN
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_q`](#classshogun_1_1CKNNSolver_1aedb3ae8f211f2e663428deff3b6f715a) | parameter q of rank weighting
`protected int32_t `[`m_num_classes`](#classshogun_1_1CKNNSolver_1a8a382f889cfb0fafcf736831eee5de6f) | number of classes (i.e. number of values labels can take)
`protected int32_t `[`m_min_label`](#classshogun_1_1CKNNSolver_1a0b1f9503399126552343e25507682e7e) | smallest label, i.e. -1
`protected `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`m_train_labels`](#classshogun_1_1CKNNSolver_1a5d7f5f658dd35b02a330bd88ee7a77a6) | the actual trainlabels
`protected `[`CDistance`](#classshogun_1_1CDistance)` * `[`distance`](#classshogun_1_1CDistanceMachine_1a174fa680ce63ca7683b32a2e1267abeb) | the distance
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_max_train_time`](#classshogun_1_1CMachine_1a0d6a5a8aca2e1e91685c1ddf23442fd8) | maximum training time
`protected `[`CLabels`](#classshogun_1_1CLabels)` * `[`m_labels`](#classshogun_1_1CMachine_1af3451cc972288f8c92ef7369952b805b) | labels
`protected `[`ESolverType`](#namespaceshogun_1af43428a9cb6c6de54cc7085c7c9b273e)` `[`m_solver_type`](#classshogun_1_1CMachine_1a4cc9c480f9e3535d05837670a124c080) | solver type
`protected bool `[`m_store_model_features`](#classshogun_1_1CMachine_1ac359a14e48915341e9dd44c8fee21ac6) | whether model features should be stored after training
`protected bool `[`m_data_locked`](#classshogun_1_1CMachine_1a93d71ccf0a5f7a1dad42f35dd7b932e2) | whether data is locked
`protected std::atomic< bool > `[`m_cancel_computation`](#classshogun_1_1CStoppableSGObject_1a263b9ed7fb7b659634a6182daa5e4d33) | Cancel computation
`protected std::atomic< bool > `[`m_pause_computation_flag`](#classshogun_1_1CStoppableSGObject_1a7054f653d8ec45c524c1137d24fd66df) | Pause computation flag
`protected std::condition_variable `[`m_pause_computation`](#classshogun_1_1CStoppableSGObject_1af0e6de5887e6f425f0b62b34e62bcf5d) | Conditional variable to make threads wait
`protected std::mutex `[`m_mutex`](#classshogun_1_1CStoppableSGObject_1a5c751dae9068bdb864af14129bbe0fa1) | Mutex used to pause threads
`protected std::function< bool(void)> `[`m_callback`](#classshogun_1_1CStoppableSGObject_1ac68af0b9914ee5a4159295e140cb906c) | 
`protected virtual void `[`store_model_features`](#classshogun_1_1CDistanceMachine_1a050a168495c7e63e3b77eea1a07c7c3b)`()` | Ensures cluster centers are in lhs of underlying distance
`protected inline virtual bool `[`train_machine`](#classshogun_1_1CMachine_1acff88580df5439ae7154299f7c743b73)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | train machine
`protected inline virtual bool `[`train_dense`](#classshogun_1_1CMachine_1a2f4984079885c8a49f40fc6bc8366d67)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | 
`protected inline virtual bool `[`train_string`](#classshogun_1_1CMachine_1aa7f306efec16f95e741472046dee440d)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | 
`protected inline virtual bool `[`support_feature_dispatching`](#classshogun_1_1CMachine_1a6d0cdca08d31651c73d028199634bb6e)`()` | 
`protected inline virtual bool `[`support_dense_dispatching`](#classshogun_1_1CMachine_1a44486c95636e8e11e3fd83fc8073a860)`()` | 
`protected inline virtual bool `[`support_string_dispatching`](#classshogun_1_1CMachine_1a3f800163b86742f0edfdabf452a627f8)`()` | 
`protected inline virtual bool `[`continue_train`](#classshogun_1_1CMachine_1a0d918d8b628c91f0c22f2a623b495812)`()` | Continue Training
`protected inline virtual bool `[`is_label_valid`](#classshogun_1_1CMachine_1a6749b87bc09701b950e315b287f73e78)`(`[`CLabels`](#classshogun_1_1CLabels)` * lab) const` | check whether the labels is valid.
`protected rxcpp::subscription `[`connect_to_signal_handler`](#classshogun_1_1CStoppableSGObject_1a4e732c6748fe2895f401c66647863e39)`()` | connect the machine instance to the signal handler
`protected void `[`reset_computation_variables`](#classshogun_1_1CStoppableSGObject_1ae1ce696f8c07b4884cbc1311fd9f5a37)`()` | reset the computation variables
`protected void `[`on_next`](#classshogun_1_1CStoppableSGObject_1a4362088c65601a14e98c19c9f0b48034)`()` | sets cancel computation flag
`protected virtual void `[`on_next_impl`](#classshogun_1_1CStoppableSGObject_1aecd947301711b0871ecc7e4608e2e794)`()` | The action which will be done when the user decides to premature stop the [CMachine](#classshogun_1_1CMachine) execution
`protected void `[`on_pause`](#classshogun_1_1CStoppableSGObject_1aae61636109c2e67b8313c19b639c8dcd)`()` | sets pause computation flag and resumes after action is complete
`protected virtual void `[`on_pause_impl`](#classshogun_1_1CStoppableSGObject_1a2fa805bcc33be124bea5b51cd9353524)`()` | The action which will be done when the user decides to pause the [CMachine](#classshogun_1_1CMachine) execution
`protected void `[`on_complete`](#classshogun_1_1CStoppableSGObject_1a4f7551e636a9ecc3826dd729b219e532)`()` | These actions which will be done when the user decides to return to prompt and terminate the program execution
`protected virtual void `[`on_complete_impl`](#classshogun_1_1CStoppableSGObject_1a0aac1762c8df8870a5242a710457c6a3)`()` | 
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

#### `public inline  `[`CLSHKNNSolver`](#classshogun_1_1CLSHKNNSolver_1a9d47cb8069d51d24b20fc410018b7034)`()` {#classshogun_1_1CLSHKNNSolver_1a9d47cb8069d51d24b20fc410018b7034}

default constructor

#### `public inline virtual  `[`~CLSHKNNSolver`](#classshogun_1_1CLSHKNNSolver_1abfd6eeffdfe04ce5ab5725b999a6e565)`()` {#classshogun_1_1CLSHKNNSolver_1abfd6eeffdfe04ce5ab5725b999a6e565}

deconstructor

#### `public  `[`CLSHKNNSolver`](#classshogun_1_1CLSHKNNSolver_1a5479701288bca5fcaa7239e50112e0fb)`(const int32_t k,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` q,const int32_t num_classes,const int32_t min_label,const `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > train_labels,const int32_t lsh_l,const int32_t lsh_t)` {#classshogun_1_1CLSHKNNSolver_1a5479701288bca5fcaa7239e50112e0fb}

constructor

#### Parameters
* `k` k 

* `q` m_q 

* `num_classes` m_num_classes 

* `min_label` m_min_label 

* `train_labels` m_train_labels 

* `lsh_l` m_lsh_l 

* `lsh_t` m_lsh_t

#### `public virtual `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * `[`classify_objects`](#classshogun_1_1CLSHKNNSolver_1a828173dccaa7d9f27a2aa159972a3dee)`(`[`CDistance`](#classshogun_1_1CDistance)` * d,const int32_t num_lab,`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > & train_lab,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > & classes) const` {#classshogun_1_1CLSHKNNSolver_1a828173dccaa7d9f27a2aa159972a3dee}

classify objects, and the implementation will depended on which knn solver been choosen.

#### Parameters
* `d` distance 

* `num_lab` number of labels been used to classify 

* `train_lab` class indices of the training data 

* `classes` vector used to store the histogram 

#### Returns
the classified labels

#### `public virtual `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`classify_objects_k`](#classshogun_1_1CLSHKNNSolver_1a9743c709d04f7e5aa51bf07ac7ac5208)`(`[`CDistance`](#classshogun_1_1CDistance)` * d,const int32_t num_lab,`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > & train_lab,`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > & classes) const` {#classshogun_1_1CLSHKNNSolver_1a9743c709d04f7e5aa51bf07ac7ac5208}

classify all objects, and the implementation will depended on which knn solver been choosen. 
#### Parameters
* `d` distance 

* `num_lab` number of labels been used to classify 

* `train_lab` class indices of the training data 

* `classes` vector used to store the histogram 

#### Returns
the classified labels

#### `public inline virtual const char * `[`get_name`](#classshogun_1_1CLSHKNNSolver_1a272dda5e08548168f78061e194511fcf)`() const` {#classshogun_1_1CLSHKNNSolver_1a272dda5e08548168f78061e194511fcf}

#### Returns
object name

#### `public int32_t `[`choose_class`](#classshogun_1_1CKNNSolver_1a2aed3e304c1018f9852ace96ed1cc5bd)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * classes,const int32_t * train_lab) const` {#classshogun_1_1CKNNSolver_1a2aed3e304c1018f9852ace96ed1cc5bd}

compute the histogram of class outputs of the k nearest neighbors to a test vector and return the index of the most frequent class

#### Parameters
* `classes` vector used to store the histogram 

* `train_lab` class indices of the training data. If the cover tree is not used, the elements are ordered by increasing distance and there are elements for each of the training vectors. If the cover tree is used, it contains just m_k elements not necessary ordered.+ * 

#### Returns
index of the most frequent class, class detected by KNN

#### `public void `[`choose_class_for_multiple_k`](#classshogun_1_1CKNNSolver_1a9d8bc323fb6d6988685d793eb25a0318)`(int32_t * output,int32_t * classes,const int32_t * train_lab,const int32_t step) const` {#classshogun_1_1CKNNSolver_1a9d8bc323fb6d6988685d793eb25a0318}

compute the histogram of class outputs of the k nearest neighbors to a test vector, using k from 1 to m_k, and write the most frequent class for each value of k in output, using a distance equal to step between elements in the output array

#### Parameters
* `output` return value where the most frequent classes are written 

* `classes` vector used to store the histogram 

* `train_lab` class indices of the training data; no matter the cover tree is used or not, the neighbors are ordered by distance to the test vector in ascending order 

* `step` distance between elements to be written in output

#### `public void `[`set_distance`](#classshogun_1_1CDistanceMachine_1a50595af6ab3dd6d473573eaa1f9180c3)`(`[`CDistance`](#classshogun_1_1CDistance)` * d)` {#classshogun_1_1CDistanceMachine_1a50595af6ab3dd6d473573eaa1f9180c3}

set distance

#### Parameters
* `d` distance to set

#### `public `[`CDistance`](#classshogun_1_1CDistance)` * `[`get_distance`](#classshogun_1_1CDistanceMachine_1a92b769f193204c8f3b2da018fbf20139)`() const` {#classshogun_1_1CDistanceMachine_1a92b769f193204c8f3b2da018fbf20139}

get distance

#### Returns
distance

#### `public void `[`distances_lhs`](#classshogun_1_1CDistanceMachine_1acd9eec8936c081242aa34c1b2518cab3)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > & result,int32_t idx_a1,int32_t idx_a2,int32_t idx_b)` {#classshogun_1_1CDistanceMachine_1acd9eec8936c081242aa34c1b2518cab3}

get distance functions for lhs feature vectors going from a1 to a2 and rhs feature vector b

#### Parameters
* `result` array of distance values 

* `idx_a1` first feature vector a1 at idx_a1 

* `idx_a2` last feature vector a2 at idx_a2 

* `idx_b` feature vector b at idx_b

#### `public void `[`distances_rhs`](#classshogun_1_1CDistanceMachine_1a0684453cfcb00efb86dbb70612192177)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > & result,int32_t idx_b1,int32_t idx_b2,int32_t idx_a)` {#classshogun_1_1CDistanceMachine_1a0684453cfcb00efb86dbb70612192177}

get distance functions for rhs feature vectors going from b1 to b2 and lhs feature vector a

#### Parameters
* `result` array of distance values 

* `idx_b1` first feature vector a1 at idx_b1 

* `idx_b2` last feature vector a2 at idx_b2 

* `idx_a` feature vector a at idx_a

#### `public virtual `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * `[`apply_multiclass`](#classshogun_1_1CDistanceMachine_1a250aa566fff0edb31433db98f70a7f15)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CDistanceMachine_1a250aa566fff0edb31433db98f70a7f15}

Classify all provided features. Cluster index with smallest distance to to be classified element is returned

#### Parameters
* `data` (test)data to be classified 

#### Returns
classified labels

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`apply_one`](#classshogun_1_1CDistanceMachine_1a541d70682e317105112ba75d3d03624a)`(int32_t num)` {#classshogun_1_1CDistanceMachine_1a541d70682e317105112ba75d3d03624a}

Apply machine to one example. Cluster index with smallest distance to to be classified element is returned

#### Parameters
* `num` which example to apply machine to 

#### Returns
cluster label nearest to example

#### `public virtual bool `[`train`](#classshogun_1_1CMachine_1aa0ece9fd14892c6dfed1bb8c78f3b3ed)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMachine_1aa0ece9fd14892c6dfed1bb8c78f3b3ed}

train machine

#### Parameters
* `data` training data (parameter can be avoided if distance or kernel-based classifiers are used and distance/kernels are initialized with train data). If flag is set, model features will be stored after training.

#### Returns
whether training was successful

#### `public virtual bool `[`train_locked`](#classshogun_1_1CMachine_1aab4927bdae8da7f0c85efdfce22c86c2)`()` {#classshogun_1_1CMachine_1aab4927bdae8da7f0c85efdfce22c86c2}

Trains a locked machine on a set of indices. Error if machine is not locked 
#### Returns
whether training was successful

#### `public inline virtual bool `[`train_locked`](#classshogun_1_1CMachine_1a6211015eaf19161e4c469c8ff38bfeba)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CMachine_1a6211015eaf19161e4c469c8ff38bfeba}

Trains a locked machine on a set of indices. Error if machine is not locked

NOT IMPLEMENTED

#### Parameters
* `indices` index vector (of locked features) that is used for training 

#### Returns
whether training was successful

#### `public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`apply`](#classshogun_1_1CMachine_1afd5d402257972c78456594234d13eb4c)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMachine_1afd5d402257972c78456594234d13eb4c}

apply machine to data if data is not specified apply to the current features

#### Parameters
* `data` (test)data to be classified 

#### Returns
classified labels

#### `public virtual `[`CBinaryLabels`](#classshogun_1_1CBinaryLabels)` * `[`apply_binary`](#classshogun_1_1CMachine_1a16a7dee83bb61aedc93792df578d4a77)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMachine_1a16a7dee83bb61aedc93792df578d4a77}

apply machine to data in means of binary classification problem

#### `public virtual `[`CRegressionLabels`](#classshogun_1_1CRegressionLabels)` * `[`apply_regression`](#classshogun_1_1CMachine_1aaeea92e0e4795e7f63f067c16f162302)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMachine_1aaeea92e0e4795e7f63f067c16f162302}

apply machine to data in means of regression problem

#### `public virtual `[`CStructuredLabels`](#classshogun_1_1CStructuredLabels)` * `[`apply_structured`](#classshogun_1_1CMachine_1a588efa92a0696e1d2a61a8cd21d8ebee)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMachine_1a588efa92a0696e1d2a61a8cd21d8ebee}

apply machine to data in means of SO classification problem

#### `public virtual `[`CLatentLabels`](#classshogun_1_1CLatentLabels)` * `[`apply_latent`](#classshogun_1_1CMachine_1a276d23b37202ecb31367df26a5600cf7)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMachine_1a276d23b37202ecb31367df26a5600cf7}

apply machine to data in means of latent problem

#### `public virtual void `[`set_labels`](#classshogun_1_1CMachine_1a5f0cfd09e37bd5e793cacecb8d3c818b)`(`[`CLabels`](#classshogun_1_1CLabels)` * lab)` {#classshogun_1_1CMachine_1a5f0cfd09e37bd5e793cacecb8d3c818b}

set labels

#### Parameters
* `lab` labels

#### `public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`get_labels`](#classshogun_1_1CMachine_1a065f0797777044cb0dbf786781982e3d)`()` {#classshogun_1_1CMachine_1a065f0797777044cb0dbf786781982e3d}

get labels

#### Returns
labels

#### `public void `[`set_max_train_time`](#classshogun_1_1CMachine_1af660b1b03c475c3c638d2c995ea4b54a)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` t)` {#classshogun_1_1CMachine_1af660b1b03c475c3c638d2c995ea4b54a}

set maximum training time

#### Parameters
* `t` maximimum training time

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_max_train_time`](#classshogun_1_1CMachine_1a7c75c86ff1cfd61d8275e62f0477d797)`()` {#classshogun_1_1CMachine_1a7c75c86ff1cfd61d8275e62f0477d797}

get maximum training time

#### Returns
maximum training time

#### `public virtual `[`EMachineType`](#namespaceshogun_1af181c832c12de7a0c3b02425986106cc)` `[`get_classifier_type`](#classshogun_1_1CMachine_1a177dc18a9a5639da395099947cb44501)`()` {#classshogun_1_1CMachine_1a177dc18a9a5639da395099947cb44501}

get classifier type

#### Returns
classifier type NONE

#### `public void `[`set_solver_type`](#classshogun_1_1CMachine_1af8876022111114d5d3b0579ee161a8ff)`(`[`ESolverType`](#namespaceshogun_1af43428a9cb6c6de54cc7085c7c9b273e)` st)` {#classshogun_1_1CMachine_1af8876022111114d5d3b0579ee161a8ff}

set solver type

#### Parameters
* `st` solver type

#### `public `[`ESolverType`](#namespaceshogun_1af43428a9cb6c6de54cc7085c7c9b273e)` `[`get_solver_type`](#classshogun_1_1CMachine_1a97ee8b11465427d28498437279229ebe)`()` {#classshogun_1_1CMachine_1a97ee8b11465427d28498437279229ebe}

get solver type

#### Returns
solver

#### `public virtual void `[`set_store_model_features`](#classshogun_1_1CMachine_1a872d1cc0904edaa3c5701b049ee2993d)`(bool store_model)` {#classshogun_1_1CMachine_1a872d1cc0904edaa3c5701b049ee2993d}

Setter for store-model-features-after-training flag

#### Parameters
* `store_model` whether model should be stored after training

#### `public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`apply_locked`](#classshogun_1_1CMachine_1add0cb383e34472fdc66db18b0a5a4bc5)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CMachine_1add0cb383e34472fdc66db18b0a5a4bc5}

Applies a locked machine on a set of indices. Error if machine is not locked

#### Parameters
* `indices` index vector (of locked features) that is predicted

#### `public virtual `[`CBinaryLabels`](#classshogun_1_1CBinaryLabels)` * `[`apply_locked_binary`](#classshogun_1_1CMachine_1ac417f13423c17ebd9b0aa742f5e78c4c)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CMachine_1ac417f13423c17ebd9b0aa742f5e78c4c}

applies a locked machine on a set of indices for binary problems

#### `public virtual `[`CRegressionLabels`](#classshogun_1_1CRegressionLabels)` * `[`apply_locked_regression`](#classshogun_1_1CMachine_1a764464fca138ac17692cb994824a1d93)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CMachine_1a764464fca138ac17692cb994824a1d93}

applies a locked machine on a set of indices for regression problems

#### `public virtual `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * `[`apply_locked_multiclass`](#classshogun_1_1CMachine_1a9a97b605764f96da5aaadda76a05d21d)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CMachine_1a9a97b605764f96da5aaadda76a05d21d}

applies a locked machine on a set of indices for multiclass problems

#### `public virtual `[`CStructuredLabels`](#classshogun_1_1CStructuredLabels)` * `[`apply_locked_structured`](#classshogun_1_1CMachine_1a8c63b6efbfe361a91794937f6fda544c)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CMachine_1a8c63b6efbfe361a91794937f6fda544c}

applies a locked machine on a set of indices for structured problems

#### `public virtual `[`CLatentLabels`](#classshogun_1_1CLatentLabels)` * `[`apply_locked_latent`](#classshogun_1_1CMachine_1ab4e951edb0bafda3d57fe80d648190d6)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CMachine_1ab4e951edb0bafda3d57fe80d648190d6}

applies a locked machine on a set of indices for latent problems

#### `public virtual void `[`data_lock`](#classshogun_1_1CMachine_1a4006ffabe6a752081d3f0e2831ae0c6e)`(`[`CLabels`](#classshogun_1_1CLabels)` * labs,`[`CFeatures`](#classshogun_1_1CFeatures)` * features)` {#classshogun_1_1CMachine_1a4006ffabe6a752081d3f0e2831ae0c6e}

Locks the machine on given labels and data. After this call, only train_locked and apply_locked may be called

Only possible if [supports_locking()](#classshogun_1_1CMachine_1a36e1fd34f65274fa2cf54c3c9b105fcb) returns true

#### Parameters
* `labs` labels used for locking 

* `features` features used for locking

#### `public inline virtual void `[`post_lock`](#classshogun_1_1CMachine_1a0ad27205b36008a86beb4da016ceef0d)`(`[`CLabels`](#classshogun_1_1CLabels)` * labs,`[`CFeatures`](#classshogun_1_1CFeatures)` * features)` {#classshogun_1_1CMachine_1a0ad27205b36008a86beb4da016ceef0d}

post lock

#### `public virtual void `[`data_unlock`](#classshogun_1_1CMachine_1a72933e4edad4e2daabeeafd9f1069e47)`()` {#classshogun_1_1CMachine_1a72933e4edad4e2daabeeafd9f1069e47}

Unlocks a locked machine and restores previous state

#### `public inline virtual bool `[`supports_locking`](#classshogun_1_1CMachine_1a36e1fd34f65274fa2cf54c3c9b105fcb)`() const` {#classshogun_1_1CMachine_1a36e1fd34f65274fa2cf54c3c9b105fcb}

#### Returns
whether this machine supports locking

#### `public inline bool `[`is_data_locked`](#classshogun_1_1CMachine_1a2996bc9c87fd16414792bca4aa0a14ec)`() const` {#classshogun_1_1CMachine_1a2996bc9c87fd16414792bca4aa0a14ec}

#### Returns
whether this machine is locked

#### `public inline virtual `[`EProblemType`](#namespaceshogun_1a0aa89aa872f89f6a174de2f45b7596d4)` `[`get_machine_problem_type`](#classshogun_1_1CMachine_1ac1c69755f623188143fc30188354a039)`() const` {#classshogun_1_1CMachine_1ac1c69755f623188143fc30188354a039}

returns type of problem machine solves

#### `public inline virtual bool `[`train_require_labels`](#classshogun_1_1CMachine_1a47f97bf5de534202ae00e77e485f3740)`() const` {#classshogun_1_1CMachine_1a47f97bf5de534202ae00e77e485f3740}

returns whether machine require labels for training

#### `public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` bool `[`cancel_computation`](#classshogun_1_1CStoppableSGObject_1a107504a021e88eec67012e1706e062c5)`() const` {#classshogun_1_1CStoppableSGObject_1a107504a021e88eec67012e1706e062c5}

#### Returns
whether the algorithm needs to be stopped

#### `public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` void `[`pause_computation`](#classshogun_1_1CStoppableSGObject_1a2168b46919701793fa1558393c30eab4)`()` {#classshogun_1_1CStoppableSGObject_1a2168b46919701793fa1558393c30eab4}

Pause the algorithm if the flag is set

#### `public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` void `[`resume_computation`](#classshogun_1_1CStoppableSGObject_1ab4c36831267ed4c90c5992b45ae33263)`()` {#classshogun_1_1CStoppableSGObject_1ab4c36831267ed4c90c5992b45ae33263}

Resume current computation (sets the flag)

#### `public void `[`set_callback`](#classshogun_1_1CStoppableSGObject_1ab6f4a2a3e5df1521ef427e3fd63f0d21)`(std::function< bool()> callback)` {#classshogun_1_1CStoppableSGObject_1ab6f4a2a3e5df1521ef427e3fd63f0d21}

Set an additional stopping condition 
#### Parameters
* `callback` method that implements an additional stopping condition

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

#### `protected int32_t `[`m_lsh_l`](#classshogun_1_1CLSHKNNSolver_1a4e290a0fb55debbb8e55365e4cd63fb9) {#classshogun_1_1CLSHKNNSolver_1a4e290a0fb55debbb8e55365e4cd63fb9}

#### `protected int32_t `[`m_lsh_t`](#classshogun_1_1CLSHKNNSolver_1afd94e59c1256fd68de72236a12f08887) {#classshogun_1_1CLSHKNNSolver_1afd94e59c1256fd68de72236a12f08887}

#### `protected int32_t `[`m_k`](#classshogun_1_1CKNNSolver_1aaf848836021c575bd56c452475b53108) {#classshogun_1_1CKNNSolver_1aaf848836021c575bd56c452475b53108}

the k parameter in KNN

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_q`](#classshogun_1_1CKNNSolver_1aedb3ae8f211f2e663428deff3b6f715a) {#classshogun_1_1CKNNSolver_1aedb3ae8f211f2e663428deff3b6f715a}

parameter q of rank weighting

#### `protected int32_t `[`m_num_classes`](#classshogun_1_1CKNNSolver_1a8a382f889cfb0fafcf736831eee5de6f) {#classshogun_1_1CKNNSolver_1a8a382f889cfb0fafcf736831eee5de6f}

number of classes (i.e. number of values labels can take)

#### `protected int32_t `[`m_min_label`](#classshogun_1_1CKNNSolver_1a0b1f9503399126552343e25507682e7e) {#classshogun_1_1CKNNSolver_1a0b1f9503399126552343e25507682e7e}

smallest label, i.e. -1

#### `protected `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`m_train_labels`](#classshogun_1_1CKNNSolver_1a5d7f5f658dd35b02a330bd88ee7a77a6) {#classshogun_1_1CKNNSolver_1a5d7f5f658dd35b02a330bd88ee7a77a6}

the actual trainlabels

#### `protected `[`CDistance`](#classshogun_1_1CDistance)` * `[`distance`](#classshogun_1_1CDistanceMachine_1a174fa680ce63ca7683b32a2e1267abeb) {#classshogun_1_1CDistanceMachine_1a174fa680ce63ca7683b32a2e1267abeb}

the distance

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_max_train_time`](#classshogun_1_1CMachine_1a0d6a5a8aca2e1e91685c1ddf23442fd8) {#classshogun_1_1CMachine_1a0d6a5a8aca2e1e91685c1ddf23442fd8}

maximum training time

#### `protected `[`CLabels`](#classshogun_1_1CLabels)` * `[`m_labels`](#classshogun_1_1CMachine_1af3451cc972288f8c92ef7369952b805b) {#classshogun_1_1CMachine_1af3451cc972288f8c92ef7369952b805b}

labels

#### `protected `[`ESolverType`](#namespaceshogun_1af43428a9cb6c6de54cc7085c7c9b273e)` `[`m_solver_type`](#classshogun_1_1CMachine_1a4cc9c480f9e3535d05837670a124c080) {#classshogun_1_1CMachine_1a4cc9c480f9e3535d05837670a124c080}

solver type

#### `protected bool `[`m_store_model_features`](#classshogun_1_1CMachine_1ac359a14e48915341e9dd44c8fee21ac6) {#classshogun_1_1CMachine_1ac359a14e48915341e9dd44c8fee21ac6}

whether model features should be stored after training

#### `protected bool `[`m_data_locked`](#classshogun_1_1CMachine_1a93d71ccf0a5f7a1dad42f35dd7b932e2) {#classshogun_1_1CMachine_1a93d71ccf0a5f7a1dad42f35dd7b932e2}

whether data is locked

#### `protected std::atomic< bool > `[`m_cancel_computation`](#classshogun_1_1CStoppableSGObject_1a263b9ed7fb7b659634a6182daa5e4d33) {#classshogun_1_1CStoppableSGObject_1a263b9ed7fb7b659634a6182daa5e4d33}

Cancel computation

#### `protected std::atomic< bool > `[`m_pause_computation_flag`](#classshogun_1_1CStoppableSGObject_1a7054f653d8ec45c524c1137d24fd66df) {#classshogun_1_1CStoppableSGObject_1a7054f653d8ec45c524c1137d24fd66df}

Pause computation flag

#### `protected std::condition_variable `[`m_pause_computation`](#classshogun_1_1CStoppableSGObject_1af0e6de5887e6f425f0b62b34e62bcf5d) {#classshogun_1_1CStoppableSGObject_1af0e6de5887e6f425f0b62b34e62bcf5d}

Conditional variable to make threads wait

#### `protected std::mutex `[`m_mutex`](#classshogun_1_1CStoppableSGObject_1a5c751dae9068bdb864af14129bbe0fa1) {#classshogun_1_1CStoppableSGObject_1a5c751dae9068bdb864af14129bbe0fa1}

Mutex used to pause threads

#### `protected std::function< bool(void)> `[`m_callback`](#classshogun_1_1CStoppableSGObject_1ac68af0b9914ee5a4159295e140cb906c) {#classshogun_1_1CStoppableSGObject_1ac68af0b9914ee5a4159295e140cb906c}

#### `protected virtual void `[`store_model_features`](#classshogun_1_1CDistanceMachine_1a050a168495c7e63e3b77eea1a07c7c3b)`()` {#classshogun_1_1CDistanceMachine_1a050a168495c7e63e3b77eea1a07c7c3b}

Ensures cluster centers are in lhs of underlying distance

NOT IMPLEMENTED! Base method. Is called automatically after train because flag is always true for distance machines. Since every distance machine has to make sure that cluster centers are in lhs of distance variable, it is unimplemented here and HAS to be implemented in subclasses.

#### `protected inline virtual bool `[`train_machine`](#classshogun_1_1CMachine_1acff88580df5439ae7154299f7c743b73)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMachine_1acff88580df5439ae7154299f7c743b73}

train machine

#### Parameters
* `data` training data (parameter can be avoided if distance or kernel-based classifiers are used and distance/kernels are initialized with train data)

NOT IMPLEMENTED!

#### Returns
whether training was successful

#### `protected inline virtual bool `[`train_dense`](#classshogun_1_1CMachine_1a2f4984079885c8a49f40fc6bc8366d67)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMachine_1a2f4984079885c8a49f40fc6bc8366d67}

#### `protected inline virtual bool `[`train_string`](#classshogun_1_1CMachine_1aa7f306efec16f95e741472046dee440d)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMachine_1aa7f306efec16f95e741472046dee440d}

#### `protected inline virtual bool `[`support_feature_dispatching`](#classshogun_1_1CMachine_1a6d0cdca08d31651c73d028199634bb6e)`()` {#classshogun_1_1CMachine_1a6d0cdca08d31651c73d028199634bb6e}

#### `protected inline virtual bool `[`support_dense_dispatching`](#classshogun_1_1CMachine_1a44486c95636e8e11e3fd83fc8073a860)`()` {#classshogun_1_1CMachine_1a44486c95636e8e11e3fd83fc8073a860}

#### `protected inline virtual bool `[`support_string_dispatching`](#classshogun_1_1CMachine_1a3f800163b86742f0edfdabf452a627f8)`()` {#classshogun_1_1CMachine_1a3f800163b86742f0edfdabf452a627f8}

#### `protected inline virtual bool `[`continue_train`](#classshogun_1_1CMachine_1a0d918d8b628c91f0c22f2a623b495812)`()` {#classshogun_1_1CMachine_1a0d918d8b628c91f0c22f2a623b495812}

Continue Training

This method can be used to continue a prematurely stopped call to [CMachine::train](#classshogun_1_1CMachine_1aa0ece9fd14892c6dfed1bb8c78f3b3ed). This is available for Iterative models and throws an error if the feature is not supported.

#### Returns
whether training was successful

#### `protected inline virtual bool `[`is_label_valid`](#classshogun_1_1CMachine_1a6749b87bc09701b950e315b287f73e78)`(`[`CLabels`](#classshogun_1_1CLabels)` * lab) const` {#classshogun_1_1CMachine_1a6749b87bc09701b950e315b287f73e78}

check whether the labels is valid.

Subclasses can override this to implement their check of label types.

#### Parameters
* `lab` the labels being checked, guaranteed to be non-NULL

#### `protected rxcpp::subscription `[`connect_to_signal_handler`](#classshogun_1_1CStoppableSGObject_1a4e732c6748fe2895f401c66647863e39)`()` {#classshogun_1_1CStoppableSGObject_1a4e732c6748fe2895f401c66647863e39}

connect the machine instance to the signal handler

#### `protected void `[`reset_computation_variables`](#classshogun_1_1CStoppableSGObject_1ae1ce696f8c07b4884cbc1311fd9f5a37)`()` {#classshogun_1_1CStoppableSGObject_1ae1ce696f8c07b4884cbc1311fd9f5a37}

reset the computation variables

#### `protected void `[`on_next`](#classshogun_1_1CStoppableSGObject_1a4362088c65601a14e98c19c9f0b48034)`()` {#classshogun_1_1CStoppableSGObject_1a4362088c65601a14e98c19c9f0b48034}

sets cancel computation flag

#### `protected virtual void `[`on_next_impl`](#classshogun_1_1CStoppableSGObject_1aecd947301711b0871ecc7e4608e2e794)`()` {#classshogun_1_1CStoppableSGObject_1aecd947301711b0871ecc7e4608e2e794}

The action which will be done when the user decides to premature stop the [CMachine](#classshogun_1_1CMachine) execution

#### `protected void `[`on_pause`](#classshogun_1_1CStoppableSGObject_1aae61636109c2e67b8313c19b639c8dcd)`()` {#classshogun_1_1CStoppableSGObject_1aae61636109c2e67b8313c19b639c8dcd}

sets pause computation flag and resumes after action is complete

#### `protected virtual void `[`on_pause_impl`](#classshogun_1_1CStoppableSGObject_1a2fa805bcc33be124bea5b51cd9353524)`()` {#classshogun_1_1CStoppableSGObject_1a2fa805bcc33be124bea5b51cd9353524}

The action which will be done when the user decides to pause the [CMachine](#classshogun_1_1CMachine) execution

#### `protected void `[`on_complete`](#classshogun_1_1CStoppableSGObject_1a4f7551e636a9ecc3826dd729b219e532)`()` {#classshogun_1_1CStoppableSGObject_1a4f7551e636a9ecc3826dd729b219e532}

These actions which will be done when the user decides to return to prompt and terminate the program execution

#### `protected virtual void `[`on_complete_impl`](#classshogun_1_1CStoppableSGObject_1a0aac1762c8df8870a5242a710457c6a3)`()` {#classshogun_1_1CStoppableSGObject_1a0aac1762c8df8870a5242a710457c6a3}

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

