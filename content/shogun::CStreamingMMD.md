---
classname: "shogun::CStreamingMMD"
type: "class"
parents:
   - CMMD
---

# class `shogun::CStreamingMMD` {#classshogun_1_1CStreamingMMD}

```
class shogun::CStreamingMMD
  : public CMMD
```

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
`public  `[`CStreamingMMD`](#classshogun_1_1CStreamingMMD_1aac969a9262c8e3416ae14e47aad975f7)`()` | 
`public virtual  `[`~CStreamingMMD`](#classshogun_1_1CStreamingMMD_1ab07b79a3192621334d5a1b38d4c7a47b)`()` | 
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_statistic`](#classshogun_1_1CStreamingMMD_1a0e996f144cb6c5a55b96220277d8e4ab)`()` | Interface for computing the test-statistic for the hypothesis test.
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_variance`](#classshogun_1_1CStreamingMMD_1a26ba5642588a887a058bd19ba2b2c000)`()` | 
`public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`compute_multiple`](#classshogun_1_1CStreamingMMD_1a10ffca7fc0e80141ab5d1f1d2cd04a94)`()` | 
`public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`sample_null`](#classshogun_1_1CStreamingMMD_1acae0723217d3f9860e02d93fd7e75179)`()` | Interface for computing the samples under the null-hypothesis.
`public void `[`use_gpu`](#classshogun_1_1CStreamingMMD_1af036850137392a2ae968193abce41d0f)`(bool gpu)` | 
`public void `[`cleanup`](#classshogun_1_1CStreamingMMD_1a4b66d5e31b5dc18b314c8a68163263bd)`()` | 
`public void `[`set_statistic_type`](#classshogun_1_1CStreamingMMD_1a4dad7915265959fc58541146594300a5)`(`[`EStatisticType`](#namespaceshogun_1a5a80ae6ebd7a27c0ed742eedff5fc7ea)` stype)` | 
`public const `[`EStatisticType`](#namespaceshogun_1a5a80ae6ebd7a27c0ed742eedff5fc7ea)` `[`get_statistic_type`](#classshogun_1_1CStreamingMMD_1aac325d4ac329c7e1d021d7df02522f1d)`() const` | 
`public void `[`set_variance_estimation_method`](#classshogun_1_1CStreamingMMD_1aa7c3897f82540b0a34eaad1e903078f5)`(`[`EVarianceEstimationMethod`](#namespaceshogun_1afeb20b9694e12d43119e5d9eccda55ed)` vmethod)` | 
`public const `[`EVarianceEstimationMethod`](#namespaceshogun_1afeb20b9694e12d43119e5d9eccda55ed)` `[`get_variance_estimation_method`](#classshogun_1_1CStreamingMMD_1aca1833de4e430a150f3da83693569a47)`() const` | 
`public void `[`set_num_null_samples`](#classshogun_1_1CStreamingMMD_1a2df2ca2fd12885426fc1fca605250cc1)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` null_samples)` | 
`public const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`get_num_null_samples`](#classshogun_1_1CStreamingMMD_1a0f2296d510ff6052af63bdb4aee00ab9)`() const` | 
`public void `[`set_null_approximation_method`](#classshogun_1_1CStreamingMMD_1ac6c646700a7d38454498f4c616ec3b05)`(`[`ENullApproximationMethod`](#namespaceshogun_1a8689bc4b26fd52cabc92b1afd8df1e7e)` nmethod)` | 
`public const `[`ENullApproximationMethod`](#namespaceshogun_1a8689bc4b26fd52cabc92b1afd8df1e7e)` `[`get_null_approximation_method`](#classshogun_1_1CStreamingMMD_1a843c2414cfd4415a12a5f71fc3488f79)`() const` | 
`public virtual const char * `[`get_name`](#classshogun_1_1CStreamingMMD_1a635420c59837dceb825845c2301c6db8)`() const` | #### Returns
`public void `[`set_kernel_selection_strategy`](#classshogun_1_1CMMD_1a3ba8bd5c65b343483a04387480af0fe3)`(`[`machine_int_t`](#common_8h_1a63fd98ca6959e851452e59a5eb06121b)` method,bool weighted)` | Method that sets the specific kernel selection strategy based on the specific parameters provided. Please see class documentation for details. Use this method for every other strategy other than KSM_CROSS_VALIDATION.
`public void `[`set_kernel_selection_strategy`](#classshogun_1_1CMMD_1a931a73ec238014d47fdd1231da747d1b)`(`[`machine_int_t`](#common_8h_1a63fd98ca6959e851452e59a5eb06121b)` method,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_runs,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_folds,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` alpha)` | Method that sets the specific kernel selection strategy based on the specific parameters provided. Please see class documentation for details. Use this method for KSM_CROSS_VALIDATION.
`public void `[`add_kernel`](#classshogun_1_1CMMD_1a59e0d731e09933fe2b31c4474d4d5ff9)`(`[`CKernel`](#classshogun_1_1CKernel)` * kernel)` | Method that adds a kernel instance to be used for kernel selection. Please note that the kernels added by this method are NOT set as the main test kernel unless [select_kernel()](#classshogun_1_1CMMD_1a909e67c8a59e31e8ffa761620d668a39) method is executed.
`public virtual void `[`select_kernel`](#classshogun_1_1CMMD_1a909e67c8a59e31e8ffa761620d668a39)`()` | Method that selects/learns the kernel based on the defined kernel selection strategy. If no explicit kernel selection strategy was set using [set_kernel_selection_strategy()](#classshogun_1_1CMMD_1a3ba8bd5c65b343483a04387480af0fe3) method, then a default strategy is used. Please see EKernelSelectionMethod for the default strategy.
`public CKernelSelectionStrategy const  * `[`get_kernel_selection_strategy`](#classshogun_1_1CMMD_1a436d8d2d204924e40dd49da660d60cdd)`() const` | Method that returns the kernel selection strategy wrapper object that will be/ was used in the last kernel learning algorithm. Use this method when results of intermediate steps taken by the kernel selection algorithms are of interest.
`public void `[`set_statistic_type`](#classshogun_1_1CMMD_1acc50df5e70369f30e4de87b556b5e452)`(`[`machine_int_t`](#common_8h_1a63fd98ca6959e851452e59a5eb06121b)` stype)` | Method that sets the type of the estimator for MMD^2
`public void `[`set_null_approximation_method`](#classshogun_1_1CMMD_1a861197ca7a557f5a331c983c573f696c)`(`[`machine_int_t`](#common_8h_1a63fd98ca6959e851452e59a5eb06121b)` nmethod)` | Method that sets the approach to be taken while approximating the null-samples.
`public virtual void `[`set_kernel`](#classshogun_1_1CTwoSampleTest_1aa84bf8a5e494a1fb896e69502c1f5bc8)`(`[`CKernel`](#classshogun_1_1CKernel)` * kernel)` | Method that sets the kernel that is used for performing the two-sample test. It is kept virtual so that sub-classes can perform other initialization tasks that has to be trigger every time a kernel is set/updated.
`public `[`CKernel`](#classshogun_1_1CKernel)` * `[`get_kernel`](#classshogun_1_1CTwoSampleTest_1a1b19268b627db7c8e9699e5d4462d75b)`() const` | #### Returns
`public virtual void `[`set_p`](#classshogun_1_1CTwoDistributionTest_1a658e051805d5a8e06f9fb4596a143203)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * samples_from_p)` | Method that initializes the samples from $\mathbf{P}$. This method is kept virtual for the sub-classes to perform additional initialization tasks that have to be performed every time features are set/updated.
`public `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`get_p`](#classshogun_1_1CTwoDistributionTest_1ab29a9ed2365f6f5397403011ef26c34e)`() const` | #### Returns
`public virtual void `[`set_q`](#classshogun_1_1CTwoDistributionTest_1ac11e0c06a3d4f07609ee96238886b614)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * samples_from_q)` | Method that initializes the samples from $\mathbf{Q}$. This method is kept virtual for the sub-classes to perform additional initialization tasks that have to be performed every time features are set/updated.
`public `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`get_q`](#classshogun_1_1CTwoDistributionTest_1a799d862b6af7a55f876fd22fa6ffd334)`() const` | #### Returns
`public void `[`set_num_samples_p`](#classshogun_1_1CTwoDistributionTest_1aa5fd5e5337ad66259af4682a7e9c566e)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_samples_from_p)` | Method that initializes the number of samples to be drawn from distribution $\mathbf{P}$. Please ensure to call this method if you are intending to use streaming data generators that generate the samples on the fly. For other types of features, the number of samples is set internally from the features object itself, therefore this method should not be used.
`public const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`get_num_samples_p`](#classshogun_1_1CTwoDistributionTest_1a3219d4f0999b8097e5d9e929e651e77c)`() const` | #### Returns
`public void `[`set_num_samples_q`](#classshogun_1_1CTwoDistributionTest_1a94ae9907b1f0ad8e99cd43e7ff5b5d3b)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_samples_from_q)` | Method that initializes the number of samples to be drawn from distribution $\mathbf{Q}$. Please ensure to call this method if you are intending to use streaming data generators that generate the samples on the fly. For other types of features, the number of samples is set internally from the features object itself, therefore this method should not be used.
`public const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`get_num_samples_q`](#classshogun_1_1CTwoDistributionTest_1a26a22c6ef3b7eadca722c16784b7a787)`() const` | #### Returns
`public `[`CCustomDistance`](#classshogun_1_1CCustomDistance)` * `[`compute_distance`](#classshogun_1_1CTwoDistributionTest_1ae511631d50ddd73a112fd2bb9071b059)`(`[`CDistance`](#classshogun_1_1CDistance)` * distance)` | Method that pre-computes the pair-wise distance between the samples using the provided distance instance.
`public `[`CCustomDistance`](#classshogun_1_1CCustomDistance)` * `[`compute_joint_distance`](#classshogun_1_1CTwoDistributionTest_1a7418567a0967d4a81f4b89f45851e310)`(`[`CDistance`](#classshogun_1_1CDistance)` * distance)` | Method that pre-computes the pair-wise distance between the joint samples using the provided distance instance. A temporary object appending the samples from both the distributions is created in order to perform the task.
`public void `[`set_train_test_mode`](#classshogun_1_1CHypothesisTest_1ad6fa6dd354bcb74f8e3f3578044e006c)`(bool on)` | Method that enables/disables the training-testing mode. If this option is turned on, then the samples would be split in two pieces: one chunk would be used for training algorithms and the other chunk would be used for performing tests. If this option is turned off, the entire data would be used for performing the test. Before running any training algorithms, make sure to turn this mode on.
`public void `[`set_train_test_ratio`](#classshogun_1_1CHypothesisTest_1a4c47e7c2767338217d38cdc8ff74c26d)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` ratio)` | Method that specifies the ratio of training-testing data split for the algorithms. Note that this is NOT the percentage of samples to be used for training, rather the ratio of the number of samples to be used for training and that of testing.
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_p_value`](#classshogun_1_1CHypothesisTest_1ab09c3589d1c5d5cb0633b6321962f8df)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` statistic)` | Method that computes a p-value based on current method for approximating the null-distribution. The p-value is the 1-p quantile of the null- distribution where the given statistic lies in.
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_threshold`](#classshogun_1_1CHypothesisTest_1a29af5e0abb3029944041e306eae2a268)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` alpha)` | Method that computes a threshold based on current method for approximating the null-distribution. The threshold is the value that a statistic has to have in ordner to reject the null-hypothesis.
`public bool `[`perform_test`](#classshogun_1_1CHypothesisTest_1a7297163c177f49c41084f50703a525ad)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` alpha)` | Method that performs the complete hypothesis test on current data and returns a binary answer: wheter null hypothesis is rejected or not.
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
`protected const `[`operation`](#classshogun_1_1CStreamingMMD_1a32a4df506ce120c916bd01e3846f4d7b)` `[`get_direct_estimation_method`](#classshogun_1_1CStreamingMMD_1afe010666d1cac664a6150d441e29c0ba)`() const` | 
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`normalize_statistic`](#classshogun_1_1CStreamingMMD_1aca66b030e47d5a982a894f004376f331)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` statistic) const` | 
`protected const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`normalize_variance`](#classshogun_1_1CStreamingMMD_1ab4cc47e53e6dc7e485a116b61d30d8d4)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` variance) const` | 
`protected bool `[`use_gpu`](#classshogun_1_1CStreamingMMD_1a82c98ee7afa297e082c21a2dfc16232c)`() const` | 
`protected std::shared_ptr< CKernelSelectionStrategy > `[`get_strategy`](#classshogun_1_1CStreamingMMD_1ae843427e7cee7babd7e22447ccccb36e)`()` | 
`protected internal::KernelManager & `[`get_kernel_mgr`](#classshogun_1_1CTwoSampleTest_1a4e2669e9c00532f1e3a98d4b90eda373)`()` | 
`protected const internal::KernelManager & `[`get_kernel_mgr`](#classshogun_1_1CTwoSampleTest_1a1feac99c74187040e825d1d6461a8df7)`() const` | 
`protected `[`internal::DataManager`](#classshogun_1_1internal_1_1DataManager)` & `[`get_data_mgr`](#classshogun_1_1CHypothesisTest_1abe6dc46444bc45eb8db1b97f7cd72ce8)`()` | 
`protected const `[`internal::DataManager`](#classshogun_1_1internal_1_1DataManager)` & `[`get_data_mgr`](#classshogun_1_1CHypothesisTest_1a76d5d77e667a70df25310aa06160399b)`() const` | 
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
`typedef `[`operation`](#classshogun_1_1CStreamingMMD_1a32a4df506ce120c916bd01e3846f4d7b) | 
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

#### `public  `[`CStreamingMMD`](#classshogun_1_1CStreamingMMD_1aac969a9262c8e3416ae14e47aad975f7)`()` {#classshogun_1_1CStreamingMMD_1aac969a9262c8e3416ae14e47aad975f7}

#### `public virtual  `[`~CStreamingMMD`](#classshogun_1_1CStreamingMMD_1ab07b79a3192621334d5a1b38d4c7a47b)`()` {#classshogun_1_1CStreamingMMD_1ab07b79a3192621334d5a1b38d4c7a47b}

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_statistic`](#classshogun_1_1CStreamingMMD_1a0e996f144cb6c5a55b96220277d8e4ab)`()` {#classshogun_1_1CStreamingMMD_1a0e996f144cb6c5a55b96220277d8e4ab}

Interface for computing the test-statistic for the hypothesis test.

#### Returns
test statistic for the given data/parameters/methods

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_variance`](#classshogun_1_1CStreamingMMD_1a26ba5642588a887a058bd19ba2b2c000)`()` {#classshogun_1_1CStreamingMMD_1a26ba5642588a887a058bd19ba2b2c000}

#### `public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`compute_multiple`](#classshogun_1_1CStreamingMMD_1a10ffca7fc0e80141ab5d1f1d2cd04a94)`()` {#classshogun_1_1CStreamingMMD_1a10ffca7fc0e80141ab5d1f1d2cd04a94}

#### `public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`sample_null`](#classshogun_1_1CStreamingMMD_1acae0723217d3f9860e02d93fd7e75179)`()` {#classshogun_1_1CStreamingMMD_1acae0723217d3f9860e02d93fd7e75179}

Interface for computing the samples under the null-hypothesis.

#### Returns
vector of all statistics

#### `public void `[`use_gpu`](#classshogun_1_1CStreamingMMD_1af036850137392a2ae968193abce41d0f)`(bool gpu)` {#classshogun_1_1CStreamingMMD_1af036850137392a2ae968193abce41d0f}

#### `public void `[`cleanup`](#classshogun_1_1CStreamingMMD_1a4b66d5e31b5dc18b314c8a68163263bd)`()` {#classshogun_1_1CStreamingMMD_1a4b66d5e31b5dc18b314c8a68163263bd}

#### `public void `[`set_statistic_type`](#classshogun_1_1CStreamingMMD_1a4dad7915265959fc58541146594300a5)`(`[`EStatisticType`](#namespaceshogun_1a5a80ae6ebd7a27c0ed742eedff5fc7ea)` stype)` {#classshogun_1_1CStreamingMMD_1a4dad7915265959fc58541146594300a5}

#### `public const `[`EStatisticType`](#namespaceshogun_1a5a80ae6ebd7a27c0ed742eedff5fc7ea)` `[`get_statistic_type`](#classshogun_1_1CStreamingMMD_1aac325d4ac329c7e1d021d7df02522f1d)`() const` {#classshogun_1_1CStreamingMMD_1aac325d4ac329c7e1d021d7df02522f1d}

#### `public void `[`set_variance_estimation_method`](#classshogun_1_1CStreamingMMD_1aa7c3897f82540b0a34eaad1e903078f5)`(`[`EVarianceEstimationMethod`](#namespaceshogun_1afeb20b9694e12d43119e5d9eccda55ed)` vmethod)` {#classshogun_1_1CStreamingMMD_1aa7c3897f82540b0a34eaad1e903078f5}

#### `public const `[`EVarianceEstimationMethod`](#namespaceshogun_1afeb20b9694e12d43119e5d9eccda55ed)` `[`get_variance_estimation_method`](#classshogun_1_1CStreamingMMD_1aca1833de4e430a150f3da83693569a47)`() const` {#classshogun_1_1CStreamingMMD_1aca1833de4e430a150f3da83693569a47}

#### `public void `[`set_num_null_samples`](#classshogun_1_1CStreamingMMD_1a2df2ca2fd12885426fc1fca605250cc1)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` null_samples)` {#classshogun_1_1CStreamingMMD_1a2df2ca2fd12885426fc1fca605250cc1}

#### `public const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`get_num_null_samples`](#classshogun_1_1CStreamingMMD_1a0f2296d510ff6052af63bdb4aee00ab9)`() const` {#classshogun_1_1CStreamingMMD_1a0f2296d510ff6052af63bdb4aee00ab9}

#### `public void `[`set_null_approximation_method`](#classshogun_1_1CStreamingMMD_1ac6c646700a7d38454498f4c616ec3b05)`(`[`ENullApproximationMethod`](#namespaceshogun_1a8689bc4b26fd52cabc92b1afd8df1e7e)` nmethod)` {#classshogun_1_1CStreamingMMD_1ac6c646700a7d38454498f4c616ec3b05}

#### `public const `[`ENullApproximationMethod`](#namespaceshogun_1a8689bc4b26fd52cabc92b1afd8df1e7e)` `[`get_null_approximation_method`](#classshogun_1_1CStreamingMMD_1a843c2414cfd4415a12a5f71fc3488f79)`() const` {#classshogun_1_1CStreamingMMD_1a843c2414cfd4415a12a5f71fc3488f79}

#### `public virtual const char * `[`get_name`](#classshogun_1_1CStreamingMMD_1a635420c59837dceb825845c2301c6db8)`() const` {#classshogun_1_1CStreamingMMD_1a635420c59837dceb825845c2301c6db8}

#### Returns
The name of this class

#### `public void `[`set_kernel_selection_strategy`](#classshogun_1_1CMMD_1a3ba8bd5c65b343483a04387480af0fe3)`(`[`machine_int_t`](#common_8h_1a63fd98ca6959e851452e59a5eb06121b)` method,bool weighted)` {#classshogun_1_1CMMD_1a3ba8bd5c65b343483a04387480af0fe3}

Method that sets the specific kernel selection strategy based on the specific parameters provided. Please see class documentation for details. Use this method for every other strategy other than KSM_CROSS_VALIDATION.

#### Parameters
* `method` The kernel selection method as specified in EKernelSelectionMethod. 

* `weighted` If true, then an weighted combination of the kernel is used after solving an optimization. If false, only a single kernel is selected among the provided ones.

#### `public void `[`set_kernel_selection_strategy`](#classshogun_1_1CMMD_1a931a73ec238014d47fdd1231da747d1b)`(`[`machine_int_t`](#common_8h_1a63fd98ca6959e851452e59a5eb06121b)` method,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_runs,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_folds,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` alpha)` {#classshogun_1_1CMMD_1a931a73ec238014d47fdd1231da747d1b}

Method that sets the specific kernel selection strategy based on the specific parameters provided. Please see class documentation for details. Use this method for KSM_CROSS_VALIDATION.

#### Parameters
* `method` The kernel selection method as specified in EKernelSelectionMethod. 

* `num_runs` The number of total runs of the cross-validation algorithm. 

* `num_folds` The number of folds (k) to be used in k-fold stratified cross-validation. 

* `alpha` The threshold to be used while performing test for the test-folds.

#### `public void `[`add_kernel`](#classshogun_1_1CMMD_1a59e0d731e09933fe2b31c4474d4d5ff9)`(`[`CKernel`](#classshogun_1_1CKernel)` * kernel)` {#classshogun_1_1CMMD_1a59e0d731e09933fe2b31c4474d4d5ff9}

Method that adds a kernel instance to be used for kernel selection. Please note that the kernels added by this method are NOT set as the main test kernel unless [select_kernel()](#classshogun_1_1CMMD_1a909e67c8a59e31e8ffa761620d668a39) method is executed.

This method is NOT thread safe. Please DO NOT use this method from multiple threads.

#### Parameters
* `kernel` One of the kernel instances with which learning algorithm will work.

#### `public virtual void `[`select_kernel`](#classshogun_1_1CMMD_1a909e67c8a59e31e8ffa761620d668a39)`()` {#classshogun_1_1CMMD_1a909e67c8a59e31e8ffa761620d668a39}

Method that selects/learns the kernel based on the defined kernel selection strategy. If no explicit kernel selection strategy was set using [set_kernel_selection_strategy()](#classshogun_1_1CMMD_1a3ba8bd5c65b343483a04387480af0fe3) method, then a default strategy is used. Please see EKernelSelectionMethod for the default strategy.

This method is NOT thread safe. It replaces the internel kernel set by [set_kernel()](#classshogun_1_1CTwoSampleTest_1aa84bf8a5e494a1fb896e69502c1f5bc8) method, if there was any. Please DO NOT use this method from multiple threads.

The learned/selected kernel can be obtained from a subsequent [get_kernel()](#classshogun_1_1CTwoSampleTest_1a1b19268b627db7c8e9699e5d4462d75b) call.

This method expects train-test mode to be turned on at the time of invocation. Please see the class documentation of [CHypothesisTest](#classshogun_1_1CHypothesisTest).

#### `public CKernelSelectionStrategy const  * `[`get_kernel_selection_strategy`](#classshogun_1_1CMMD_1a436d8d2d204924e40dd49da660d60cdd)`() const` {#classshogun_1_1CMMD_1a436d8d2d204924e40dd49da660d60cdd}

Method that returns the kernel selection strategy wrapper object that will be/ was used in the last kernel learning algorithm. Use this method when results of intermediate steps taken by the kernel selection algorithms are of interest.

#### Returns
The internal instance of [CKernelSelectionStrategy](#namespaceCKernelSelectionStrategy) that holds intermediate measures computed at the time of the last kernel selection algorithm invocation.

#### `public void `[`set_statistic_type`](#classshogun_1_1CMMD_1acc50df5e70369f30e4de87b556b5e452)`(`[`machine_int_t`](#common_8h_1a63fd98ca6959e851452e59a5eb06121b)` stype)` {#classshogun_1_1CMMD_1acc50df5e70369f30e4de87b556b5e452}

Method that sets the type of the estimator for MMD^2

#### Parameters
* `stype` The type of the estimator for MMD^2

#### `public void `[`set_null_approximation_method`](#classshogun_1_1CMMD_1a861197ca7a557f5a331c983c573f696c)`(`[`machine_int_t`](#common_8h_1a63fd98ca6959e851452e59a5eb06121b)` nmethod)` {#classshogun_1_1CMMD_1a861197ca7a557f5a331c983c573f696c}

Method that sets the approach to be taken while approximating the null-samples.

The null-approximation method

#### `public virtual void `[`set_kernel`](#classshogun_1_1CTwoSampleTest_1aa84bf8a5e494a1fb896e69502c1f5bc8)`(`[`CKernel`](#classshogun_1_1CKernel)` * kernel)` {#classshogun_1_1CTwoSampleTest_1aa84bf8a5e494a1fb896e69502c1f5bc8}

Method that sets the kernel that is used for performing the two-sample test. It is kept virtual so that sub-classes can perform other initialization tasks that has to be trigger every time a kernel is set/updated.

#### Parameters
* `kernel` The kernel instance.

#### `public `[`CKernel`](#classshogun_1_1CKernel)` * `[`get_kernel`](#classshogun_1_1CTwoSampleTest_1a1b19268b627db7c8e9699e5d4462d75b)`() const` {#classshogun_1_1CTwoSampleTest_1a1b19268b627db7c8e9699e5d4462d75b}

#### Returns
The kernel instance that is presently being used for performing the test

#### `public virtual void `[`set_p`](#classshogun_1_1CTwoDistributionTest_1a658e051805d5a8e06f9fb4596a143203)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * samples_from_p)` {#classshogun_1_1CTwoDistributionTest_1a658e051805d5a8e06f9fb4596a143203}

Method that initializes the samples from $\mathbf{P}$. This method is kept virtual for the sub-classes to perform additional initialization tasks that have to be performed every time features are set/updated.

#### Parameters
* `samples_from_p` The [CFeatures](#classshogun_1_1CFeatures) instance representing the samples from $\mathbf{P}$.

#### `public `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`get_p`](#classshogun_1_1CTwoDistributionTest_1ab29a9ed2365f6f5397403011ef26c34e)`() const` {#classshogun_1_1CTwoDistributionTest_1ab29a9ed2365f6f5397403011ef26c34e}

#### Returns
The samples from $\mathbf{P}$.

#### `public virtual void `[`set_q`](#classshogun_1_1CTwoDistributionTest_1ac11e0c06a3d4f07609ee96238886b614)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * samples_from_q)` {#classshogun_1_1CTwoDistributionTest_1ac11e0c06a3d4f07609ee96238886b614}

Method that initializes the samples from $\mathbf{Q}$. This method is kept virtual for the sub-classes to perform additional initialization tasks that have to be performed every time features are set/updated.

#### Parameters
* `samples_from_q` The [CFeatures](#classshogun_1_1CFeatures) instance representing the samples from $\mathbf{Q}$.

#### `public `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`get_q`](#classshogun_1_1CTwoDistributionTest_1a799d862b6af7a55f876fd22fa6ffd334)`() const` {#classshogun_1_1CTwoDistributionTest_1a799d862b6af7a55f876fd22fa6ffd334}

#### Returns
The samples from $\mathbf{Q}$.

#### `public void `[`set_num_samples_p`](#classshogun_1_1CTwoDistributionTest_1aa5fd5e5337ad66259af4682a7e9c566e)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_samples_from_p)` {#classshogun_1_1CTwoDistributionTest_1aa5fd5e5337ad66259af4682a7e9c566e}

Method that initializes the number of samples to be drawn from distribution $\mathbf{P}$. Please ensure to call this method if you are intending to use streaming data generators that generate the samples on the fly. For other types of features, the number of samples is set internally from the features object itself, therefore this method should not be used.

#### Parameters
* `num_samples_from_p` The [CFeatures](#classshogun_1_1CFeatures) instance representing the samples from $\mathbf{P}$.

#### `public const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`get_num_samples_p`](#classshogun_1_1CTwoDistributionTest_1a3219d4f0999b8097e5d9e929e651e77c)`() const` {#classshogun_1_1CTwoDistributionTest_1a3219d4f0999b8097e5d9e929e651e77c}

#### Returns
The number of samples from $\mathbf{P}$.

#### `public void `[`set_num_samples_q`](#classshogun_1_1CTwoDistributionTest_1a94ae9907b1f0ad8e99cd43e7ff5b5d3b)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_samples_from_q)` {#classshogun_1_1CTwoDistributionTest_1a94ae9907b1f0ad8e99cd43e7ff5b5d3b}

Method that initializes the number of samples to be drawn from distribution $\mathbf{Q}$. Please ensure to call this method if you are intending to use streaming data generators that generate the samples on the fly. For other types of features, the number of samples is set internally from the features object itself, therefore this method should not be used.

#### Parameters
* `num_samples_from_q` The [CFeatures](#classshogun_1_1CFeatures) instance representing the samples from $\mathbf{Q}$.

#### `public const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`get_num_samples_q`](#classshogun_1_1CTwoDistributionTest_1a26a22c6ef3b7eadca722c16784b7a787)`() const` {#classshogun_1_1CTwoDistributionTest_1a26a22c6ef3b7eadca722c16784b7a787}

#### Returns
The number of samples from $\mathbf{Q}$.

#### `public `[`CCustomDistance`](#classshogun_1_1CCustomDistance)` * `[`compute_distance`](#classshogun_1_1CTwoDistributionTest_1ae511631d50ddd73a112fd2bb9071b059)`(`[`CDistance`](#classshogun_1_1CDistance)` * distance)` {#classshogun_1_1CTwoDistributionTest_1ae511631d50ddd73a112fd2bb9071b059}

Method that pre-computes the pair-wise distance between the samples using the provided distance instance.

#### Parameters
* `distance` The distance instance used for pre-computing the pair-wise distance. 

#### Returns
A newly created [CCustomDistance](#classshogun_1_1CCustomDistance) instance representing the pre-computed pair-wise distance between the samples.

#### `public `[`CCustomDistance`](#classshogun_1_1CCustomDistance)` * `[`compute_joint_distance`](#classshogun_1_1CTwoDistributionTest_1a7418567a0967d4a81f4b89f45851e310)`(`[`CDistance`](#classshogun_1_1CDistance)` * distance)` {#classshogun_1_1CTwoDistributionTest_1a7418567a0967d4a81f4b89f45851e310}

Method that pre-computes the pair-wise distance between the joint samples using the provided distance instance. A temporary object appending the samples from both the distributions is created in order to perform the task.

#### Parameters
* `distance` The distance instance used for pre-computing the pair-wise distance. 

#### Returns
A newly created [CCustomDistance](#classshogun_1_1CCustomDistance) instance representing the pre-computed pair-wise distance between the joint samples.

#### `public void `[`set_train_test_mode`](#classshogun_1_1CHypothesisTest_1ad6fa6dd354bcb74f8e3f3578044e006c)`(bool on)` {#classshogun_1_1CHypothesisTest_1ad6fa6dd354bcb74f8e3f3578044e006c}

Method that enables/disables the training-testing mode. If this option is turned on, then the samples would be split in two pieces: one chunk would be used for training algorithms and the other chunk would be used for performing tests. If this option is turned off, the entire data would be used for performing the test. Before running any training algorithms, make sure to turn this mode on.

By default, the training-testing mode is turned off.

**See also**: {[set_train_test_ratio()](#classshogun_1_1CHypothesisTest_1a4c47e7c2767338217d38cdc8ff74c26d)}

#### Parameters
* `on` Whether to enable/disable the training-testing mode

#### `public void `[`set_train_test_ratio`](#classshogun_1_1CHypothesisTest_1a4c47e7c2767338217d38cdc8ff74c26d)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` ratio)` {#classshogun_1_1CHypothesisTest_1a4c47e7c2767338217d38cdc8ff74c26d}

Method that specifies the ratio of training-testing data split for the algorithms. Note that this is NOT the percentage of samples to be used for training, rather the ratio of the number of samples to be used for training and that of testing.

By default, an equal 50-50 split (ratio = 1) is made.

**See also**: {[set_train_test_mode()](#classshogun_1_1CHypothesisTest_1ad6fa6dd354bcb74f8e3f3578044e006c)}

#### Parameters
* `ratio` The ratio of the number of samples to be used for training and that of testing

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_p_value`](#classshogun_1_1CHypothesisTest_1ab09c3589d1c5d5cb0633b6321962f8df)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` statistic)` {#classshogun_1_1CHypothesisTest_1ab09c3589d1c5d5cb0633b6321962f8df}

Method that computes a p-value based on current method for approximating the null-distribution. The p-value is the 1-p quantile of the null- distribution where the given statistic lies in.

This method depends on the implementation of sample_null method which should be implemented by the sub-classes.

#### Parameters
* `statistic` statistic value to compute the p-value for 

#### Returns
p-value parameter statistic is the (1-p) percentile of the null distribution

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_threshold`](#classshogun_1_1CHypothesisTest_1a29af5e0abb3029944041e306eae2a268)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` alpha)` {#classshogun_1_1CHypothesisTest_1a29af5e0abb3029944041e306eae2a268}

Method that computes a threshold based on current method for approximating the null-distribution. The threshold is the value that a statistic has to have in ordner to reject the null-hypothesis.

This method depends on the implementation of sample_null method which should be implemented by the sub-classes.

#### Parameters
* `alpha` test level to reject null-hypothesis 

#### Returns
Threshold for statistics to reject null-hypothesis

#### `public bool `[`perform_test`](#classshogun_1_1CHypothesisTest_1a7297163c177f49c41084f50703a525ad)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` alpha)` {#classshogun_1_1CHypothesisTest_1a7297163c177f49c41084f50703a525ad}

Method that performs the complete hypothesis test on current data and returns a binary answer: wheter null hypothesis is rejected or not.

This is just a wrapper for the above [compute_p_value()](#classshogun_1_1CHypothesisTest_1ab09c3589d1c5d5cb0633b6321962f8df) method that returns a p-value. If this p-value lies below the test level alpha, the null hypothesis is rejected.

Should not be overwritten in subclasses. (Therefore not virtual)

#### Parameters
* `alpha` test level alpha. 

#### Returns
true if null hypothesis is rejected and false otherwise

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

#### `protected const `[`operation`](#classshogun_1_1CStreamingMMD_1a32a4df506ce120c916bd01e3846f4d7b)` `[`get_direct_estimation_method`](#classshogun_1_1CStreamingMMD_1afe010666d1cac664a6150d441e29c0ba)`() const` {#classshogun_1_1CStreamingMMD_1afe010666d1cac664a6150d441e29c0ba}

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`normalize_statistic`](#classshogun_1_1CStreamingMMD_1aca66b030e47d5a982a894f004376f331)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` statistic) const` {#classshogun_1_1CStreamingMMD_1aca66b030e47d5a982a894f004376f331}

#### `protected const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`normalize_variance`](#classshogun_1_1CStreamingMMD_1ab4cc47e53e6dc7e485a116b61d30d8d4)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` variance) const` {#classshogun_1_1CStreamingMMD_1ab4cc47e53e6dc7e485a116b61d30d8d4}

#### `protected bool `[`use_gpu`](#classshogun_1_1CStreamingMMD_1a82c98ee7afa297e082c21a2dfc16232c)`() const` {#classshogun_1_1CStreamingMMD_1a82c98ee7afa297e082c21a2dfc16232c}

#### `protected std::shared_ptr< CKernelSelectionStrategy > `[`get_strategy`](#classshogun_1_1CStreamingMMD_1ae843427e7cee7babd7e22447ccccb36e)`()` {#classshogun_1_1CStreamingMMD_1ae843427e7cee7babd7e22447ccccb36e}

#### `protected internal::KernelManager & `[`get_kernel_mgr`](#classshogun_1_1CTwoSampleTest_1a4e2669e9c00532f1e3a98d4b90eda373)`()` {#classshogun_1_1CTwoSampleTest_1a4e2669e9c00532f1e3a98d4b90eda373}

#### `protected const internal::KernelManager & `[`get_kernel_mgr`](#classshogun_1_1CTwoSampleTest_1a1feac99c74187040e825d1d6461a8df7)`() const` {#classshogun_1_1CTwoSampleTest_1a1feac99c74187040e825d1d6461a8df7}

#### `protected `[`internal::DataManager`](#classshogun_1_1internal_1_1DataManager)` & `[`get_data_mgr`](#classshogun_1_1CHypothesisTest_1abe6dc46444bc45eb8db1b97f7cd72ce8)`()` {#classshogun_1_1CHypothesisTest_1abe6dc46444bc45eb8db1b97f7cd72ce8}

#### `protected const `[`internal::DataManager`](#classshogun_1_1internal_1_1DataManager)` & `[`get_data_mgr`](#classshogun_1_1CHypothesisTest_1a76d5d77e667a70df25310aa06160399b)`() const` {#classshogun_1_1CHypothesisTest_1a76d5d77e667a70df25310aa06160399b}

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

#### `typedef `[`operation`](#classshogun_1_1CStreamingMMD_1a32a4df506ce120c916bd01e3846f4d7b) {#classshogun_1_1CStreamingMMD_1a32a4df506ce120c916bd01e3846f4d7b}

#### `typedef `[`SGSubject`](#classshogun_1_1CSGObject_1a52509313192ce488ae91f9d7e2b16267) {#classshogun_1_1CSGObject_1a52509313192ce488ae91f9d7e2b16267}

Definition of observed subject

#### `typedef `[`SGObservable`](#classshogun_1_1CSGObject_1a3f344a622ab6c3e0dd73b5dd3f7aa556) {#classshogun_1_1CSGObject_1a3f344a622ab6c3e0dd73b5dd3f7aa556}

Definition of observable

#### `typedef `[`SGSubscriber`](#classshogun_1_1CSGObject_1a658eb47ba606529e8ffc5090d36e34e8) {#classshogun_1_1CSGObject_1a658eb47ba606529e8ffc5090d36e34e8}

Definition of subscriber

