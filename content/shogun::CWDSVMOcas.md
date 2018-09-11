---
classname: "shogun::CWDSVMOcas"
type: "class"
parents:
   - CMachine
---

# class `shogun::CWDSVMOcas` {#classshogun_1_1CWDSVMOcas}

```
class shogun::CWDSVMOcas
  : public CMachine
```

class WDSVMOcas

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
`public  `[`MACHINE_PROBLEM_TYPE`](#classshogun_1_1CWDSVMOcas_1aa2d22990d22f93916c7b9675db96f0ea)`(`[`PT_BINARY`](#namespaceshogun_1a0aa89aa872f89f6a174de2f45b7596d4a17ea40d0e25bb381c98ce350e05a66a6)`)` | problem type
`public  `[`CWDSVMOcas`](#classshogun_1_1CWDSVMOcas_1afb54281c842fb03a045562659985a76c)`()` | default constructor
`public  `[`CWDSVMOcas`](#classshogun_1_1CWDSVMOcas_1a246a83b8d4558d4334a91af4aa5913b0)`(E_SVM_TYPE type)` | constructor
`public  `[`CWDSVMOcas`](#classshogun_1_1CWDSVMOcas_1af8902e17dd72fa6c377981a4beeffa65)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` C,int32_t d,int32_t from_d,`[`CStringFeatures`](#classshogun_1_1CStringFeatures)`< uint8_t > * traindat,`[`CLabels`](#classshogun_1_1CLabels)` * trainlab)` | constructor
`public virtual  `[`~CWDSVMOcas`](#classshogun_1_1CWDSVMOcas_1afd7720dd144b07e87e3ed26f661f44a3)`()` | 
`public inline virtual `[`EMachineType`](#namespaceshogun_1af181c832c12de7a0c3b02425986106cc)` `[`get_classifier_type`](#classshogun_1_1CWDSVMOcas_1ab0ee71eb4f9097a9b7ad2b72b1b310e2)`()` | get classifier type
`public inline void `[`set_C`](#classshogun_1_1CWDSVMOcas_1a272a6477be80601077c22e17a530a460)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` c_neg,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` c_pos)` | set C
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_C1`](#classshogun_1_1CWDSVMOcas_1a106ca4c7bad3e1779f80eae35c203144)`()` | get C1
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_C2`](#classshogun_1_1CWDSVMOcas_1a48b19829cbf87b2f540aa68db4ed50fa)`()` | get C2
`public inline void `[`set_epsilon`](#classshogun_1_1CWDSVMOcas_1ae3931ee9091f751d7584919fb92dde53)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` eps)` | set epsilon
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_epsilon`](#classshogun_1_1CWDSVMOcas_1acc649b6e3439428fe014ae45f8db19b0)`()` | get epsilon
`public inline void `[`set_features`](#classshogun_1_1CWDSVMOcas_1af33bbcf25a4760e896242a3d80c48b72)`(`[`CStringFeatures`](#classshogun_1_1CStringFeatures)`< uint8_t > * feat)` | set features
`public inline `[`CStringFeatures`](#classshogun_1_1CStringFeatures)`< uint8_t > * `[`get_features`](#classshogun_1_1CWDSVMOcas_1aab187c950486017c0d9142991b05942d)`()` | get features
`public inline void `[`set_bias_enabled`](#classshogun_1_1CWDSVMOcas_1a5b773e2eeec54d607c1add0864a701ab)`(bool enable_bias)` | set if bias shall be enabled
`public inline bool `[`get_bias_enabled`](#classshogun_1_1CWDSVMOcas_1a24209179a0e8592371857af993da1c51)`()` | check if bias is enabled
`public inline void `[`set_bufsize`](#classshogun_1_1CWDSVMOcas_1ac85479938f92b2850cefae6c57e10490)`(int32_t sz)` | set buffer size
`public inline int32_t `[`get_bufsize`](#classshogun_1_1CWDSVMOcas_1ad4f0aeefcb2a8e743f97e6bb2222a5d1)`()` | get buffer size
`public inline void `[`set_degree`](#classshogun_1_1CWDSVMOcas_1a7c9529f794834d5c6212add2c6363182)`(int32_t d,int32_t from_d)` | set degree
`public inline int32_t `[`get_degree`](#classshogun_1_1CWDSVMOcas_1a94209fc79868a8102b03088d5fad8127)`()` | get degree
`public virtual `[`CBinaryLabels`](#classshogun_1_1CBinaryLabels)` * `[`apply_binary`](#classshogun_1_1CWDSVMOcas_1a16a7dee83bb61aedc93792df578d4a77)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | classify objects for binary classification problems
`public virtual `[`CRegressionLabels`](#classshogun_1_1CRegressionLabels)` * `[`apply_regression`](#classshogun_1_1CWDSVMOcas_1aaeea92e0e4795e7f63f067c16f162302)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | classify objects for regression problems
`public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`apply_one`](#classshogun_1_1CWDSVMOcas_1ace8614a2d279fe05db3648a1214e59e1)`(int32_t num)` | classify one example
`public inline void `[`set_normalization_const`](#classshogun_1_1CWDSVMOcas_1aee156d52143a464c9164cead3f74f480)`()` | set normalization const
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_normalization_const`](#classshogun_1_1CWDSVMOcas_1a149f9dbb2a444a8e0519abd933382bbe)`()` | get normalization const
`public virtual bool `[`train`](#classshogun_1_1CMachine_1aa0ece9fd14892c6dfed1bb8c78f3b3ed)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | train machine
`public virtual bool `[`train_locked`](#classshogun_1_1CMachine_1aab4927bdae8da7f0c85efdfce22c86c2)`()` | Trains a locked machine on a set of indices. Error if machine is not locked 
`public inline virtual bool `[`train_locked`](#classshogun_1_1CMachine_1a6211015eaf19161e4c469c8ff38bfeba)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | Trains a locked machine on a set of indices. Error if machine is not locked
`public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`apply`](#classshogun_1_1CMachine_1afd5d402257972c78456594234d13eb4c)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data if data is not specified apply to the current features
`public virtual `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * `[`apply_multiclass`](#classshogun_1_1CMachine_1a250aa566fff0edb31433db98f70a7f15)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data in means of multiclass classification problem
`public virtual `[`CStructuredLabels`](#classshogun_1_1CStructuredLabels)` * `[`apply_structured`](#classshogun_1_1CMachine_1a588efa92a0696e1d2a61a8cd21d8ebee)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data in means of SO classification problem
`public virtual `[`CLatentLabels`](#classshogun_1_1CLatentLabels)` * `[`apply_latent`](#classshogun_1_1CMachine_1a276d23b37202ecb31367df26a5600cf7)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data in means of latent problem
`public virtual void `[`set_labels`](#classshogun_1_1CMachine_1a5f0cfd09e37bd5e793cacecb8d3c818b)`(`[`CLabels`](#classshogun_1_1CLabels)` * lab)` | set labels
`public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`get_labels`](#classshogun_1_1CMachine_1a065f0797777044cb0dbf786781982e3d)`()` | get labels
`public void `[`set_max_train_time`](#classshogun_1_1CMachine_1af660b1b03c475c3c638d2c995ea4b54a)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` t)` | set maximum training time
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_max_train_time`](#classshogun_1_1CMachine_1a7c75c86ff1cfd61d8275e62f0477d797)`()` | get maximum training time
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
`protected `[`CStringFeatures`](#classshogun_1_1CStringFeatures)`< uint8_t > * `[`features`](#classshogun_1_1CWDSVMOcas_1ae235e7798f684526bed10e35263309bf) | features
`protected bool `[`use_bias`](#classshogun_1_1CWDSVMOcas_1a1c58e9e70ed28387a69429e81707f9ba) | if bias shall be used
`protected int32_t `[`bufsize`](#classshogun_1_1CWDSVMOcas_1ae53500e44db36ee44f4d774441dcaa1d) | buffer size
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`C1`](#classshogun_1_1CWDSVMOcas_1a1ecd274e8562cfd7010dffbe7af07054) | C1
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`C2`](#classshogun_1_1CWDSVMOcas_1aadda42a3db2f58cc3a5e885d27053f4c) | C2
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`epsilon`](#classshogun_1_1CWDSVMOcas_1a0bde8d297e19e73b20b99110ba38f7bd) | epsilon
`protected E_SVM_TYPE `[`method`](#classshogun_1_1CWDSVMOcas_1a54b349b320e683dce087dfd6a10f7ef2) | method
`protected int32_t `[`degree`](#classshogun_1_1CWDSVMOcas_1a192432a474907a70b37aa10ddabc0c97) | degree
`protected int32_t `[`from_degree`](#classshogun_1_1CWDSVMOcas_1ad917c276e6189abd80e43bcaa63b4bbb) | from degree
`protected `[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * `[`wd_weights`](#classshogun_1_1CWDSVMOcas_1a8f3504396456b7c162f8685f93fff009) | wd weights
`protected int32_t `[`num_vec`](#classshogun_1_1CWDSVMOcas_1a0c51e73be26a6d77a5fc852609e53761) | num vectors
`protected int32_t `[`string_length`](#classshogun_1_1CWDSVMOcas_1a0f92b1f7b64d4de4c1a8a10d8a9f7c94) | length of string in vector
`protected int32_t `[`alphabet_size`](#classshogun_1_1CWDSVMOcas_1a5b523537ad89946b28c528b3cb09bb3f) | size of alphabet
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`normalization_const`](#classshogun_1_1CWDSVMOcas_1a7a97639b3837eae3d948ec757daab43b) | normalization const
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`bias`](#classshogun_1_1CWDSVMOcas_1a387f3356ebb50f52c60199d35c797451) | bias
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`old_bias`](#classshogun_1_1CWDSVMOcas_1ad29835644fb2153f77a07632d15eaaa1) | old_bias
`protected int32_t * `[`w_offsets`](#classshogun_1_1CWDSVMOcas_1a145e06575f6da6b11249ce7d0e283614) | w offsets
`protected int32_t `[`w_dim`](#classshogun_1_1CWDSVMOcas_1a87d5fcf2afc5fec83eca4eeb48c1f81f) | w dim
`protected int32_t `[`w_dim_single_char`](#classshogun_1_1CWDSVMOcas_1a90302fee2ec89078f4fdcb02e7914445) | w dim of a single char
`protected `[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * `[`w`](#classshogun_1_1CWDSVMOcas_1afc1141ab4160b7a8deda34b5106b17fb) | w
`protected `[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * `[`old_w`](#classshogun_1_1CWDSVMOcas_1a91a0587d0e2eae41ec04f652e1e86352) | old w
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`lab`](#classshogun_1_1CWDSVMOcas_1aec00a4f25e5bc8a95678abe191f4798b) | labels
`protected `[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` ** `[`cuts`](#classshogun_1_1CWDSVMOcas_1ad12cb98b2c984d1f1caf64ad052e1563) | cuts
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`cp_bias`](#classshogun_1_1CWDSVMOcas_1a766eb0ed29db7a41073161ba7d8307ad) | bias dimensions
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
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`apply_get_outputs`](#classshogun_1_1CWDSVMOcas_1a4b696cdfb849ca73d178431c06ddf3ff)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | get real outputs
`protected int32_t `[`set_wd_weights`](#classshogun_1_1CWDSVMOcas_1a98d1b8acac164f2ccb9ec6fa4cc00fdb)`()` | set wd weights
`protected inline virtual const char * `[`get_name`](#classshogun_1_1CWDSVMOcas_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` | #### Returns
`protected virtual bool `[`train_machine`](#classshogun_1_1CWDSVMOcas_1ac6ad4326a1641cb16d8d74d2ac00e9d3)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | train classifier
`protected inline virtual bool `[`train_dense`](#classshogun_1_1CMachine_1a2f4984079885c8a49f40fc6bc8366d67)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | 
`protected inline virtual bool `[`train_string`](#classshogun_1_1CMachine_1aa7f306efec16f95e741472046dee440d)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | 
`protected inline virtual bool `[`support_feature_dispatching`](#classshogun_1_1CMachine_1a6d0cdca08d31651c73d028199634bb6e)`()` | 
`protected inline virtual bool `[`support_dense_dispatching`](#classshogun_1_1CMachine_1a44486c95636e8e11e3fd83fc8073a860)`()` | 
`protected inline virtual bool `[`support_string_dispatching`](#classshogun_1_1CMachine_1a3f800163b86742f0edfdabf452a627f8)`()` | 
`protected inline virtual bool `[`continue_train`](#classshogun_1_1CMachine_1a0d918d8b628c91f0c22f2a623b495812)`()` | Continue Training
`protected inline virtual void `[`store_model_features`](#classshogun_1_1CMachine_1ae0a84ada96561ce09c35e2839f8ca512)`()` | Stores feature data of underlying model. After this method has been called, it is possible to change the machine's feature data and call [apply()](#classshogun_1_1CMachine_1afd5d402257972c78456594234d13eb4c), which is then performed on the training feature data that is part of the machine's model.
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

#### `public  `[`MACHINE_PROBLEM_TYPE`](#classshogun_1_1CWDSVMOcas_1aa2d22990d22f93916c7b9675db96f0ea)`(`[`PT_BINARY`](#namespaceshogun_1a0aa89aa872f89f6a174de2f45b7596d4a17ea40d0e25bb381c98ce350e05a66a6)`)` {#classshogun_1_1CWDSVMOcas_1aa2d22990d22f93916c7b9675db96f0ea}

problem type

#### `public  `[`CWDSVMOcas`](#classshogun_1_1CWDSVMOcas_1afb54281c842fb03a045562659985a76c)`()` {#classshogun_1_1CWDSVMOcas_1afb54281c842fb03a045562659985a76c}

default constructor

#### `public  `[`CWDSVMOcas`](#classshogun_1_1CWDSVMOcas_1a246a83b8d4558d4334a91af4aa5913b0)`(E_SVM_TYPE type)` {#classshogun_1_1CWDSVMOcas_1a246a83b8d4558d4334a91af4aa5913b0}

constructor

#### Parameters
* `type` type of SVM

#### `public  `[`CWDSVMOcas`](#classshogun_1_1CWDSVMOcas_1af8902e17dd72fa6c377981a4beeffa65)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` C,int32_t d,int32_t from_d,`[`CStringFeatures`](#classshogun_1_1CStringFeatures)`< uint8_t > * traindat,`[`CLabels`](#classshogun_1_1CLabels)` * trainlab)` {#classshogun_1_1CWDSVMOcas_1af8902e17dd72fa6c377981a4beeffa65}

constructor

#### Parameters
* `C` constant C 

* `d` degree 

* `from_d` from degree 

* `traindat` training features 

* `trainlab` labels for training features

#### `public virtual  `[`~CWDSVMOcas`](#classshogun_1_1CWDSVMOcas_1afd7720dd144b07e87e3ed26f661f44a3)`()` {#classshogun_1_1CWDSVMOcas_1afd7720dd144b07e87e3ed26f661f44a3}

#### `public inline virtual `[`EMachineType`](#namespaceshogun_1af181c832c12de7a0c3b02425986106cc)` `[`get_classifier_type`](#classshogun_1_1CWDSVMOcas_1ab0ee71eb4f9097a9b7ad2b72b1b310e2)`()` {#classshogun_1_1CWDSVMOcas_1ab0ee71eb4f9097a9b7ad2b72b1b310e2}

get classifier type

#### Returns
classifier type WDSVMOCAS

#### `public inline void `[`set_C`](#classshogun_1_1CWDSVMOcas_1a272a6477be80601077c22e17a530a460)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` c_neg,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` c_pos)` {#classshogun_1_1CWDSVMOcas_1a272a6477be80601077c22e17a530a460}

set C

#### Parameters
* `c_neg` new C constant for negatively labeled examples 

* `c_pos` new C constant for positively labeled examples

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_C1`](#classshogun_1_1CWDSVMOcas_1a106ca4c7bad3e1779f80eae35c203144)`()` {#classshogun_1_1CWDSVMOcas_1a106ca4c7bad3e1779f80eae35c203144}

get C1

#### Returns
C1

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_C2`](#classshogun_1_1CWDSVMOcas_1a48b19829cbf87b2f540aa68db4ed50fa)`()` {#classshogun_1_1CWDSVMOcas_1a48b19829cbf87b2f540aa68db4ed50fa}

get C2

#### Returns
C2

#### `public inline void `[`set_epsilon`](#classshogun_1_1CWDSVMOcas_1ae3931ee9091f751d7584919fb92dde53)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` eps)` {#classshogun_1_1CWDSVMOcas_1ae3931ee9091f751d7584919fb92dde53}

set epsilon

#### Parameters
* `eps` new epsilon

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_epsilon`](#classshogun_1_1CWDSVMOcas_1acc649b6e3439428fe014ae45f8db19b0)`()` {#classshogun_1_1CWDSVMOcas_1acc649b6e3439428fe014ae45f8db19b0}

get epsilon

#### Returns
epsilon

#### `public inline void `[`set_features`](#classshogun_1_1CWDSVMOcas_1af33bbcf25a4760e896242a3d80c48b72)`(`[`CStringFeatures`](#classshogun_1_1CStringFeatures)`< uint8_t > * feat)` {#classshogun_1_1CWDSVMOcas_1af33bbcf25a4760e896242a3d80c48b72}

set features

#### Parameters
* `feat` features to set

#### `public inline `[`CStringFeatures`](#classshogun_1_1CStringFeatures)`< uint8_t > * `[`get_features`](#classshogun_1_1CWDSVMOcas_1aab187c950486017c0d9142991b05942d)`()` {#classshogun_1_1CWDSVMOcas_1aab187c950486017c0d9142991b05942d}

get features

#### Returns
features

#### `public inline void `[`set_bias_enabled`](#classshogun_1_1CWDSVMOcas_1a5b773e2eeec54d607c1add0864a701ab)`(bool enable_bias)` {#classshogun_1_1CWDSVMOcas_1a5b773e2eeec54d607c1add0864a701ab}

set if bias shall be enabled

#### Parameters
* `enable_bias` if bias shall be enabled

#### `public inline bool `[`get_bias_enabled`](#classshogun_1_1CWDSVMOcas_1a24209179a0e8592371857af993da1c51)`()` {#classshogun_1_1CWDSVMOcas_1a24209179a0e8592371857af993da1c51}

check if bias is enabled

#### Returns
if bias is enabled

#### `public inline void `[`set_bufsize`](#classshogun_1_1CWDSVMOcas_1ac85479938f92b2850cefae6c57e10490)`(int32_t sz)` {#classshogun_1_1CWDSVMOcas_1ac85479938f92b2850cefae6c57e10490}

set buffer size

#### Parameters
* `sz` buffer size

#### `public inline int32_t `[`get_bufsize`](#classshogun_1_1CWDSVMOcas_1ad4f0aeefcb2a8e743f97e6bb2222a5d1)`()` {#classshogun_1_1CWDSVMOcas_1ad4f0aeefcb2a8e743f97e6bb2222a5d1}

get buffer size

#### Returns
buffer size

#### `public inline void `[`set_degree`](#classshogun_1_1CWDSVMOcas_1a7c9529f794834d5c6212add2c6363182)`(int32_t d,int32_t from_d)` {#classshogun_1_1CWDSVMOcas_1a7c9529f794834d5c6212add2c6363182}

set degree

#### Parameters
* `d` degree 

* `from_d` from degree

#### `public inline int32_t `[`get_degree`](#classshogun_1_1CWDSVMOcas_1a94209fc79868a8102b03088d5fad8127)`()` {#classshogun_1_1CWDSVMOcas_1a94209fc79868a8102b03088d5fad8127}

get degree

#### Returns
degree

#### `public virtual `[`CBinaryLabels`](#classshogun_1_1CBinaryLabels)` * `[`apply_binary`](#classshogun_1_1CWDSVMOcas_1a16a7dee83bb61aedc93792df578d4a77)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CWDSVMOcas_1a16a7dee83bb61aedc93792df578d4a77}

classify objects for binary classification problems

#### Parameters
* `data` (test)data to be classified 

#### Returns
classified labels

#### `public virtual `[`CRegressionLabels`](#classshogun_1_1CRegressionLabels)` * `[`apply_regression`](#classshogun_1_1CWDSVMOcas_1aaeea92e0e4795e7f63f067c16f162302)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CWDSVMOcas_1aaeea92e0e4795e7f63f067c16f162302}

classify objects for regression problems

#### Parameters
* `data` (test)data to be classified 

#### Returns
classified labels

#### `public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`apply_one`](#classshogun_1_1CWDSVMOcas_1ace8614a2d279fe05db3648a1214e59e1)`(int32_t num)` {#classshogun_1_1CWDSVMOcas_1ace8614a2d279fe05db3648a1214e59e1}

classify one example

#### Parameters
* `num` number of example to classify 

#### Returns
classified result

#### `public inline void `[`set_normalization_const`](#classshogun_1_1CWDSVMOcas_1aee156d52143a464c9164cead3f74f480)`()` {#classshogun_1_1CWDSVMOcas_1aee156d52143a464c9164cead3f74f480}

set normalization const

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_normalization_const`](#classshogun_1_1CWDSVMOcas_1a149f9dbb2a444a8e0519abd933382bbe)`()` {#classshogun_1_1CWDSVMOcas_1a149f9dbb2a444a8e0519abd933382bbe}

get normalization const

#### Returns
normalization const

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

#### `public virtual `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * `[`apply_multiclass`](#classshogun_1_1CMachine_1a250aa566fff0edb31433db98f70a7f15)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMachine_1a250aa566fff0edb31433db98f70a7f15}

apply machine to data in means of multiclass classification problem

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

#### `protected `[`CStringFeatures`](#classshogun_1_1CStringFeatures)`< uint8_t > * `[`features`](#classshogun_1_1CWDSVMOcas_1ae235e7798f684526bed10e35263309bf) {#classshogun_1_1CWDSVMOcas_1ae235e7798f684526bed10e35263309bf}

features

#### `protected bool `[`use_bias`](#classshogun_1_1CWDSVMOcas_1a1c58e9e70ed28387a69429e81707f9ba) {#classshogun_1_1CWDSVMOcas_1a1c58e9e70ed28387a69429e81707f9ba}

if bias shall be used

#### `protected int32_t `[`bufsize`](#classshogun_1_1CWDSVMOcas_1ae53500e44db36ee44f4d774441dcaa1d) {#classshogun_1_1CWDSVMOcas_1ae53500e44db36ee44f4d774441dcaa1d}

buffer size

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`C1`](#classshogun_1_1CWDSVMOcas_1a1ecd274e8562cfd7010dffbe7af07054) {#classshogun_1_1CWDSVMOcas_1a1ecd274e8562cfd7010dffbe7af07054}

C1

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`C2`](#classshogun_1_1CWDSVMOcas_1aadda42a3db2f58cc3a5e885d27053f4c) {#classshogun_1_1CWDSVMOcas_1aadda42a3db2f58cc3a5e885d27053f4c}

C2

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`epsilon`](#classshogun_1_1CWDSVMOcas_1a0bde8d297e19e73b20b99110ba38f7bd) {#classshogun_1_1CWDSVMOcas_1a0bde8d297e19e73b20b99110ba38f7bd}

epsilon

#### `protected E_SVM_TYPE `[`method`](#classshogun_1_1CWDSVMOcas_1a54b349b320e683dce087dfd6a10f7ef2) {#classshogun_1_1CWDSVMOcas_1a54b349b320e683dce087dfd6a10f7ef2}

method

#### `protected int32_t `[`degree`](#classshogun_1_1CWDSVMOcas_1a192432a474907a70b37aa10ddabc0c97) {#classshogun_1_1CWDSVMOcas_1a192432a474907a70b37aa10ddabc0c97}

degree

#### `protected int32_t `[`from_degree`](#classshogun_1_1CWDSVMOcas_1ad917c276e6189abd80e43bcaa63b4bbb) {#classshogun_1_1CWDSVMOcas_1ad917c276e6189abd80e43bcaa63b4bbb}

from degree

#### `protected `[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * `[`wd_weights`](#classshogun_1_1CWDSVMOcas_1a8f3504396456b7c162f8685f93fff009) {#classshogun_1_1CWDSVMOcas_1a8f3504396456b7c162f8685f93fff009}

wd weights

#### `protected int32_t `[`num_vec`](#classshogun_1_1CWDSVMOcas_1a0c51e73be26a6d77a5fc852609e53761) {#classshogun_1_1CWDSVMOcas_1a0c51e73be26a6d77a5fc852609e53761}

num vectors

#### `protected int32_t `[`string_length`](#classshogun_1_1CWDSVMOcas_1a0f92b1f7b64d4de4c1a8a10d8a9f7c94) {#classshogun_1_1CWDSVMOcas_1a0f92b1f7b64d4de4c1a8a10d8a9f7c94}

length of string in vector

#### `protected int32_t `[`alphabet_size`](#classshogun_1_1CWDSVMOcas_1a5b523537ad89946b28c528b3cb09bb3f) {#classshogun_1_1CWDSVMOcas_1a5b523537ad89946b28c528b3cb09bb3f}

size of alphabet

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`normalization_const`](#classshogun_1_1CWDSVMOcas_1a7a97639b3837eae3d948ec757daab43b) {#classshogun_1_1CWDSVMOcas_1a7a97639b3837eae3d948ec757daab43b}

normalization const

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`bias`](#classshogun_1_1CWDSVMOcas_1a387f3356ebb50f52c60199d35c797451) {#classshogun_1_1CWDSVMOcas_1a387f3356ebb50f52c60199d35c797451}

bias

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`old_bias`](#classshogun_1_1CWDSVMOcas_1ad29835644fb2153f77a07632d15eaaa1) {#classshogun_1_1CWDSVMOcas_1ad29835644fb2153f77a07632d15eaaa1}

old_bias

#### `protected int32_t * `[`w_offsets`](#classshogun_1_1CWDSVMOcas_1a145e06575f6da6b11249ce7d0e283614) {#classshogun_1_1CWDSVMOcas_1a145e06575f6da6b11249ce7d0e283614}

w offsets

#### `protected int32_t `[`w_dim`](#classshogun_1_1CWDSVMOcas_1a87d5fcf2afc5fec83eca4eeb48c1f81f) {#classshogun_1_1CWDSVMOcas_1a87d5fcf2afc5fec83eca4eeb48c1f81f}

w dim

#### `protected int32_t `[`w_dim_single_char`](#classshogun_1_1CWDSVMOcas_1a90302fee2ec89078f4fdcb02e7914445) {#classshogun_1_1CWDSVMOcas_1a90302fee2ec89078f4fdcb02e7914445}

w dim of a single char

#### `protected `[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * `[`w`](#classshogun_1_1CWDSVMOcas_1afc1141ab4160b7a8deda34b5106b17fb) {#classshogun_1_1CWDSVMOcas_1afc1141ab4160b7a8deda34b5106b17fb}

w

#### `protected `[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * `[`old_w`](#classshogun_1_1CWDSVMOcas_1a91a0587d0e2eae41ec04f652e1e86352) {#classshogun_1_1CWDSVMOcas_1a91a0587d0e2eae41ec04f652e1e86352}

old w

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`lab`](#classshogun_1_1CWDSVMOcas_1aec00a4f25e5bc8a95678abe191f4798b) {#classshogun_1_1CWDSVMOcas_1aec00a4f25e5bc8a95678abe191f4798b}

labels

#### `protected `[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` ** `[`cuts`](#classshogun_1_1CWDSVMOcas_1ad12cb98b2c984d1f1caf64ad052e1563) {#classshogun_1_1CWDSVMOcas_1ad12cb98b2c984d1f1caf64ad052e1563}

cuts

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`cp_bias`](#classshogun_1_1CWDSVMOcas_1a766eb0ed29db7a41073161ba7d8307ad) {#classshogun_1_1CWDSVMOcas_1a766eb0ed29db7a41073161ba7d8307ad}

bias dimensions

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

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`apply_get_outputs`](#classshogun_1_1CWDSVMOcas_1a4b696cdfb849ca73d178431c06ddf3ff)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CWDSVMOcas_1a4b696cdfb849ca73d178431c06ddf3ff}

get real outputs

#### Parameters
* `data` features to apply for

#### `protected int32_t `[`set_wd_weights`](#classshogun_1_1CWDSVMOcas_1a98d1b8acac164f2ccb9ec6fa4cc00fdb)`()` {#classshogun_1_1CWDSVMOcas_1a98d1b8acac164f2ccb9ec6fa4cc00fdb}

set wd weights

#### Returns
w_dim_single_c

#### `protected inline virtual const char * `[`get_name`](#classshogun_1_1CWDSVMOcas_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` {#classshogun_1_1CWDSVMOcas_1a9cb485686dd7a1e6f7103cf42e87717e}

#### Returns
object name

#### `protected virtual bool `[`train_machine`](#classshogun_1_1CWDSVMOcas_1ac6ad4326a1641cb16d8d74d2ac00e9d3)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CWDSVMOcas_1ac6ad4326a1641cb16d8d74d2ac00e9d3}

train classifier

#### Parameters
* `data` training data (parameter can be avoided if distance or kernel-based classifiers are used and distance/kernels are initialized with train data)

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

#### `protected inline virtual void `[`store_model_features`](#classshogun_1_1CMachine_1ae0a84ada96561ce09c35e2839f8ca512)`()` {#classshogun_1_1CMachine_1ae0a84ada96561ce09c35e2839f8ca512}

Stores feature data of underlying model. After this method has been called, it is possible to change the machine's feature data and call [apply()](#classshogun_1_1CMachine_1afd5d402257972c78456594234d13eb4c), which is then performed on the training feature data that is part of the machine's model.

Base method, has to be implemented in order to allow cross-validation and model selection.

NOT IMPLEMENTED! Has to be done in subclasses

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

