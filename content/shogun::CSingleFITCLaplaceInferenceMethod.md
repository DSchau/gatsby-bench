---
classname: "shogun::CSingleFITCLaplaceInferenceMethod"
type: "class"
parents:
   - CSingleFITCInference
---

# class `shogun::CSingleFITCLaplaceInferenceMethod` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod}

```
class shogun::CSingleFITCLaplaceInferenceMethod
  : public CSingleFITCInference
```

The FITC approximation inference method class for regression and binary Classification. Note that the number of inducing points (m) is usually far less than the number of input points (n). (the time complexity is computed based on the assumption m < n)

Warning: the time complexity of method, [CSingleFITCInference::get_derivative_wrt_kernel(const TParameter* param)](#classshogun_1_1CSingleSparseInference_1a7d855b840228424960622229b81773cf), depends on the implementation of virtual kernel method, CKernel::get_parameter_gradient_diagonal(param, i). The default time complexity of the kernel method can be O(n^2)

Warning: the the time complexity increases from O(m^2*n) to O(n^2*m) if method [CSingleFITCLaplaceInferenceMethod::get_posterior_covariance()](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1acfb7e948b3dad546ace3422c6c94ca41) is called

This specific implementation was adapted from the infFITC_Laplace.m file in the GPML toolbox.

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
`public  `[`CSingleFITCLaplaceInferenceMethod`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a27a501f868d62aa7cfc1a7556e7dcd96)`()` | default constructor
`public  `[`CSingleFITCLaplaceInferenceMethod`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a950a002fc3ea2e6ea826eaf1a22151cc)`(`[`CKernel`](#classshogun_1_1CKernel)` * kernel,`[`CFeatures`](#classshogun_1_1CFeatures)` * features,`[`CMeanFunction`](#classshogun_1_1CMeanFunction)` * mean,`[`CLabels`](#classshogun_1_1CLabels)` * labels,`[`CLikelihoodModel`](#classshogun_1_1CLikelihoodModel)` * model,`[`CFeatures`](#classshogun_1_1CFeatures)` * inducing_features)` | constructor
`public virtual  `[`~CSingleFITCLaplaceInferenceMethod`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a787430b0bb1a508f55235cc0be491fad)`()` | 
`public inline virtual const char * `[`get_name`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` | returns the name of the inference method
`public inline virtual `[`EInferenceType`](#namespaceshogun_1af211cbb4dbc85162c4d855bd08e2122b)` `[`get_inference_type`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1aa1690a0c36fecfd3ab9bca7e09e6d62d)`() const` | return what type of inference we are
`public inline virtual bool `[`supports_regression`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a14c93de070b9c7b9b5c87ef2dac1d515)`() const` | #### Returns
`public inline virtual bool `[`supports_binary`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1aeb433012dfd6a925ad198e24d5a41976)`() const` | #### Returns
`public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_diagonal_vector`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1aeeef6125b8cd17aa89459914d6d2ae7b)`()` | get diagonal vector
`public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_posterior_mean`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a354c199b5cc758b9d82b7b6070bba7b0)`()` | returns mean vector $\mu$ of the Gaussian distribution $\mathcal{N}(\mu,\Sigma)$, which is an approximation to the posterior:
`public virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_posterior_covariance`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1acfb7e948b3dad546ace3422c6c94ca41)`()` | returns covariance matrix $\Sigma=(K^{-1}+W)^{-1}$ of the Gaussian distribution $\mathcal{N}(\mu,\Sigma)$, which is an approximation to the posterior:
`public virtual void `[`update`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1ac5c54df7ed3b930268c8d7752c101725)`()` | update matrices except gradients
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_negative_log_marginal_likelihood`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a9d168a7d73ff38d40c1b12929ca1b575)`()` | get negative log marginal likelihood
`public virtual void `[`register_minimizer`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a677b05b09eef6bab839953b794c9096a)`(`[`Minimizer`](#classshogun_1_1Minimizer)` * minimizer)` | Set a minimizer
`public virtual void `[`set_kernel`](#classshogun_1_1CSingleSparseInference_1a2952b17be257e98e4a2bcadf20c11e3a)`(`[`CKernel`](#classshogun_1_1CKernel)` * kern)` | set kernel
`public virtual void `[`optimize_inducing_features`](#classshogun_1_1CSingleSparseInference_1abee0aa1265dc45fb20f2dec6d94fe1f7)`()` | opitmize inducing features
`public virtual void `[`set_lower_bound_of_inducing_features`](#classshogun_1_1CSingleSparseInference_1a947c06b3f127d6c2247ba77e87698d55)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > bound)` | set the lower bound of inducing features
`public virtual void `[`set_upper_bound_of_inducing_features`](#classshogun_1_1CSingleSparseInference_1a961c8444d4d84d2486ad8ebc2f0d1ff1)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > bound)` | set the upper bound of inducing features
`public virtual void `[`set_tolearance_for_inducing_features`](#classshogun_1_1CSingleSparseInference_1a259d3827cd9c645a3cb5bab99fa35faa)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` tol)` | set the tolearance used in optimization of inducing features
`public virtual void `[`set_max_iterations_for_inducing_features`](#classshogun_1_1CSingleSparseInference_1a4ce96b6f9f05c85829aa1dfaefa11466)`(int32_t it)` | set the max number of iterations used in optimization of inducing features
`public virtual void `[`enable_optimizing_inducing_features`](#classshogun_1_1CSingleSparseInference_1a03572b9530025272167c6145940b3e70)`(bool is_optmization,`[`FirstOrderMinimizer`](#classshogun_1_1FirstOrderMinimizer)` * minimizer)` | whether enable to opitmize inducing features
`public inline virtual void `[`set_inducing_features`](#classshogun_1_1CSparseInference_1a45a4fbdc85f275841d46e6455883df73)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * feat)` | set inducing features
`public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`get_inducing_features`](#classshogun_1_1CSparseInference_1ad553e57045ee40819016e8d3fadded4f)`()` | get inducing features
`public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_alpha`](#classshogun_1_1CSparseInference_1a81e656eac199852421b3a51c92418dc4)`()` | get alpha vector
`public virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_cholesky`](#classshogun_1_1CSparseInference_1ae9147e300e23bf1fc49efcd1efc872f5)`()` | get Cholesky decomposition matrix
`public virtual void `[`set_inducing_noise`](#classshogun_1_1CSparseInference_1a41290707e80a0b364b7fe532f5436f44)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` noise)` | set the noise for inducing points
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_inducing_noise`](#classshogun_1_1CSparseInference_1a3cc7fed6b9fb491f884aa28bd437dade)`()` | get the noise for inducing points
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_marginal_likelihood_estimate`](#classshogun_1_1CInference_1a6e4c3c79df2e7dbb33a0cd9d392dbc6b)`(int32_t num_importance_samples,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` ridge_size)` | Computes an unbiased estimate of the marginal-likelihood (in log-domain),
`public virtual `[`CMap](#classshogun_1_1CMap)< [TParameter](#structshogun_1_1TParameter) *, [SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > > * `[`get_negative_log_marginal_likelihood_derivatives`](#classshogun_1_1CInference_1a0c5d57cdb86528e769a2e1b9a355b6fa)`(`[`CMap](#classshogun_1_1CMap)< [TParameter](#structshogun_1_1TParameter) *, [CSGObject`](#classshogun_1_1CSGObject)` *> * parameters)` | get log marginal likelihood gradient
`public inline virtual `[`CMap](#classshogun_1_1CMap)< [TParameter](#structshogun_1_1TParameter) *, [SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > > * `[`get_gradient`](#classshogun_1_1CInference_1a19d9b05672d6ba91505a180bdb51c1a8)`(`[`CMap](#classshogun_1_1CMap)< [TParameter](#structshogun_1_1TParameter) *, [CSGObject`](#classshogun_1_1CSGObject)` *> * parameters)` | get the gradient
`public inline virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_value`](#classshogun_1_1CInference_1a91c887d42da386aabc8765ff395afa30)`()` | get the function value
`public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`get_features`](#classshogun_1_1CInference_1a7ec6aec639e612c981d12d436950bf57)`()` | get features
`public inline virtual void `[`set_features`](#classshogun_1_1CInference_1a1ce34ed4aaad4f9ee4e0fa6f5ca6643e)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * feat)` | set features
`public inline virtual `[`CKernel`](#classshogun_1_1CKernel)` * `[`get_kernel`](#classshogun_1_1CInference_1a7b613c50f18bb224844708c436b9b970)`()` | get kernel
`public inline virtual `[`CMeanFunction`](#classshogun_1_1CMeanFunction)` * `[`get_mean`](#classshogun_1_1CInference_1a707b09ed75d22e85849b3198bf23c591)`()` | get mean
`public inline virtual void `[`set_mean`](#classshogun_1_1CInference_1a1f0f0e7c8ebecbe7bb9cde3901414d93)`(`[`CMeanFunction`](#classshogun_1_1CMeanFunction)` * m)` | set mean
`public inline virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`get_labels`](#classshogun_1_1CInference_1a9dea304fdcdc2dd7be8bed7f10720f77)`()` | get labels
`public inline virtual void `[`set_labels`](#classshogun_1_1CInference_1a018196e9672050b27f59e04a251a060a)`(`[`CLabels`](#classshogun_1_1CLabels)` * lab)` | set labels
`public inline `[`CLikelihoodModel`](#classshogun_1_1CLikelihoodModel)` * `[`get_model`](#classshogun_1_1CInference_1a14f34a32af31dad38950cc5479009521)`()` | get likelihood model
`public inline virtual void `[`set_model`](#classshogun_1_1CInference_1aa73afad18520515ab6ab7eca88b9ab58)`(`[`CLikelihoodModel`](#classshogun_1_1CLikelihoodModel)` * mod)` | set likelihood model
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_scale`](#classshogun_1_1CInference_1af5bf7c06ba4887a1d9178c161ec18153)`() const` | get kernel scale
`public virtual void `[`set_scale`](#classshogun_1_1CInference_1ad9b699b761021293ea97658f2bdb0ca6)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` scale)` | set kernel scale
`public inline virtual bool `[`supports_multiclass`](#classshogun_1_1CInference_1af95ed88e9e900a577e55104b16c93c09)`() const` | whether combination of inference method and given likelihood function supports multiclass classification
`public virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_multiclass_E`](#classshogun_1_1CInference_1ab4ce31c7340d2031f529b11b5336d511)`()` | get the E matrix used for multi classification
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
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_mean_f`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a9857804080a61debb66368a7704af5e2) | a parameter used to compute function value and gradient for LBFGS update
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_sW`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a0ad15ab494883e17a3a1f1aab4916fe9) | square root of W
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_d2lp`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a3f83a9fda6d9fa1d54401457c6feafa6) | second derivative of log likelihood with respect to function location
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_d3lp`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a54a71a30024c3820da8fe3a290fe1147) | third derivative of log likelihood with respect to function location
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_dlp`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1adcdd0d952c755827a551fac2543af8ad) | derivative of log likelihood with respect to function location
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_W`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1ada8808ae54e77ccf819372dcb48c7de6) | noise matrix
`protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_chol_R0`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a277f0cd7be98e7adc2ce3f76d96b7d9b) | Cholesky of inverse covariance of inducing features
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_dfhat`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1aaeaae07cd7d3fdd999afef3230c4bceb) | derivative of negative log (approximated) marginal likelihood wrt f
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_g`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a05e49d6564de3c7373c7f013ec1a6ab1) | g defined in infFITC_Laplace.m
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_Psi`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a3ba2fc0b7b52439cc330c808867868f2) | the negative log likelihood without constant terms of 
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_dg`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1ade1f32b52f5be3688c28c7c278001aaa) | d0 defined in infFITC_Laplace.m
`protected bool `[`m_Wneg`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1afcead5bc781ff0e45ec80d4607bc710d) | whether W contains negative elements
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_al`](#classshogun_1_1CSingleFITCInference_1acb243275b7aeb3c8dfb48c9db6073ca0) | Note that alpha is NOT post.alpha alpha and post.alpha are defined in infFITC.m and infFITC_Laplace.m
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_t`](#classshogun_1_1CSingleFITCInference_1a62de6a998432de37df5636b13c799ae2) | t=1/g_sn2 in regression, where g_sn2 is defined in infFITC.m t=W.*dd in Laplace for binary classification, where W and dd are defined in infFITC_Laplace.m
`protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_B`](#classshogun_1_1CSingleFITCInference_1ad7f2f8705f1a6681553fff80ad797fb3) | B is defined in infFITC.m and infFITC_Laplace.m
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_w`](#classshogun_1_1CSingleFITCInference_1aa81433bf01d10f2e9bbeb5ed96eadd93) | w=B*al
`protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_Rvdd`](#classshogun_1_1CSingleFITCInference_1a1c950db882d4eee7830f6b5e7ae03b43) | Rvdd=W where W is defined in infFITC.m and Rvdd is defined in infFITC_Laplace.m Note that W is NOT the diagonal matrix
`protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_V`](#classshogun_1_1CSingleFITCInference_1a02aed9430b96257abefd934fc0984082) | V defined in infFITC.m and infFITC_Laplace.m
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_lower_bound`](#classshogun_1_1CSingleSparseInference_1a178ca1525cfcac4910869f996b934455) | lower bound of inducing features
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_upper_bound`](#classshogun_1_1CSingleSparseInference_1a152113d2622036eccfc65bdff1129268) | upper bound of inducing features
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_max_ind_iterations`](#classshogun_1_1CSingleSparseInference_1afeed637fee40abda40e73192e79d8dcd) | max number of iterations
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_ind_tolerance`](#classshogun_1_1CSingleSparseInference_1a7115b181ecd2ca9e7810767dd07874de) | tolearance used in optimizing inducing_features
`protected bool `[`m_opt_inducing_features`](#classshogun_1_1CSingleSparseInference_1a1dabe53c54d8428cbd56bb0363e6086f) | whether optimize inducing features
`protected bool `[`m_fully_sparse`](#classshogun_1_1CSingleSparseInference_1a33d67e551071cc5db0327092bb5d2d33) | whether the kernel supports to get the gradient wrt inducing points or not
`protected `[`CLock`](#classshogun_1_1CLock)` * `[`m_lock`](#classshogun_1_1CSingleSparseInference_1ae9abeca94bc2dcc5fccb93433d81f4ff) | a lock used to parallelly compute derivatives wrt hyperparameters
`protected `[`FirstOrderMinimizer`](#classshogun_1_1FirstOrderMinimizer)` * `[`m_inducing_minimizer`](#classshogun_1_1CSingleSparseInference_1af35a9c8ba4944b3c16aa09fd3b0718f0) | minimizer used in finding optimal inducing features
`protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_inducing_features`](#classshogun_1_1CSparseInference_1acb7c01ca79f528405214937ffbf8956f) | inducing features for approximation
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_log_ind_noise`](#classshogun_1_1CSparseInference_1a49749703f291dc88c19734f5e94061c9) | noise of the inducing variables
`protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_kuu`](#classshogun_1_1CSparseInference_1a95912ecbd8b849f3cd6b4860a1c456de) | covariance matrix of inducing features
`protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_ktru`](#classshogun_1_1CSparseInference_1a0923be17e60a5cb5ef81557efdec0693) | covariance matrix of inducing features and training features
`protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_Sigma`](#classshogun_1_1CSparseInference_1afb7c413193e6053a3ef68c688e3837fe) | covariance matrix of the the posterior Gaussian distribution
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_mu`](#classshogun_1_1CSparseInference_1a5573ccd36cd3e2025296478a5e2c5e62) | mean vector of the the posterior Gaussian distribution
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_ktrtr_diag`](#classshogun_1_1CSparseInference_1a9619600b070c1250f501ae18d8a1323d) | diagonal elements of kernel matrix m_ktrtr
`protected `[`Minimizer`](#classshogun_1_1Minimizer)` * `[`m_minimizer`](#classshogun_1_1CInference_1a766c444a5e24ea44e0dc51deefcd83ca) | minimizer
`protected `[`CKernel`](#classshogun_1_1CKernel)` * `[`m_kernel`](#classshogun_1_1CInference_1ada185a4ebba125dd54f4d0d18ae494e0) | covariance function
`protected `[`CMeanFunction`](#classshogun_1_1CMeanFunction)` * `[`m_mean`](#classshogun_1_1CInference_1a76304a61b8f285fd66896aab5d829a57) | mean function
`protected `[`CLikelihoodModel`](#classshogun_1_1CLikelihoodModel)` * `[`m_model`](#classshogun_1_1CInference_1a8dd2ad293c3b26f2decd134a8430f936) | likelihood function to use
`protected `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`m_features`](#classshogun_1_1CInference_1a0d3e1aae112ff755c8e0e651070a4add) | features to use
`protected `[`CLabels`](#classshogun_1_1CLabels)` * `[`m_labels`](#classshogun_1_1CInference_1af3451cc972288f8c92ef7369952b805b) | labels of features
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_alpha`](#classshogun_1_1CInference_1adbf2e7c7892979cd2e78ba11b32855c6) | alpha vector used in process mean calculation
`protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_L`](#classshogun_1_1CInference_1a4eb1f068212c66a37e53fae9d8dd4d7d) | upper triangular factor of Cholesky decomposition
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_log_scale`](#classshogun_1_1CInference_1a48bfe2f7d129b68a09b9a2a25f0b0b67) | kernel scale
`protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_ktrtr`](#classshogun_1_1CInference_1a6df22eadf2014fb840e24b9665eda337) | kernel matrix from features (non-scalled by inference scalling)
`protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_E`](#classshogun_1_1CInference_1a1f854dae153b08f91e345ea5c24366bf) | the matrix used for multi classification
`protected bool `[`m_gradient_update`](#classshogun_1_1CInference_1a05c35b833c45472a266e936b50680191) | Whether gradients are updated
`protected virtual void `[`compute_gradient`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a45f790a0f06e7fe5b94389b5d2ffd911)`()` | update gradients
`protected virtual void `[`update_init`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a93b4c26b29456a89d6b383a881a95a90)`()` | pre-compution for Newton's method
`protected virtual void `[`update_alpha`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1ae68f6c7520ab3314edd7d291079159e3)`()` | update alpha matrix
`protected virtual void `[`update_chol`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a7d5df00b072be0d4f11c9424aea4ba04)`()` | update cholesky matrix
`protected virtual void `[`update_approx_cov`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a4333efb3408d2ae500f12dd2edb5c2cb)`()` | update covariance matrix of the approximation to the posterior
`protected virtual void `[`update_deriv`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a17c88d33d05ee66766ede990fe963bf4)`()` | update matrices which are required to compute negative log marginal likelihood derivatives wrt hyperparameter
`protected virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_derivative_wrt_inference_method`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a4c99bcd6af8c3134f10a79895d8767e4)`(const `[`TParameter`](#structshogun_1_1TParameter)` * param)` | returns derivative of negative log marginal likelihood wrt parameter of [CInference](#classshogun_1_1CInference) class
`protected virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_derivative_wrt_likelihood_model`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a2b5a05afff3755bf8ebb2e94f7c9af8b)`(const `[`TParameter`](#structshogun_1_1TParameter)` * param)` | returns derivative of negative log marginal likelihood wrt parameter of likelihood model
`protected virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_derivative_wrt_kernel`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a7d855b840228424960622229b81773cf)`(const `[`TParameter`](#structshogun_1_1TParameter)` * param)` | returns derivative of negative log marginal likelihood wrt kernel's parameter
`protected virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_derivative_wrt_mean`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a7319c9be33b426c9dfa87c4e4c14bbd0)`(const `[`TParameter`](#structshogun_1_1TParameter)` * param)` | returns derivative of negative log marginal likelihood wrt mean function's parameter
`protected virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_chol_inv`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1aa1b37fead39790feec938bf999e5c935)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > mtx)` | efficiently compute the Cholesky decomposition of inverse of the input matrix chol(inv(mtx))
`protected virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`compute_mvmK`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a6e79ec6211c5bcec9bf9e1b6e06523ce)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > al)` | efficiently compute the matrix-vector product $\Sigma \times al$, where $\Sigma$ is the FITC equivalent covariance n-by-n matrix (prior) of f_n
`protected virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`compute_mvmZ`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a011613073703ad70781ae6e238ae5ca1)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > x)` | efficiently compute the matrix-vector product $ \inv{\inv{W}+\Sigma} \times x$, where $\Sigma$ is the FITC equivalent covariance n-by-n matrix (prior) of f_n
`protected virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_derivative_wrt_inducing_features`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a6a042fa7c7b7865adc44a3dddb53c160)`(const `[`TParameter`](#structshogun_1_1TParameter)` * param)` | returns derivative of negative log marginal likelihood wrt inducing features (input) Note that in order to call this method, kernel must support FITC inference, which means derivatives wrt inducing features can be computed
`protected virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_derivative_wrt_inducing_noise`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a45b7aff01904f73cbc4318557330fdff)`(const `[`TParameter`](#structshogun_1_1TParameter)` * param)` | returns derivative of negative log marginal likelihood wrt inducing noise
`protected virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`derivative_helper_when_Wneg`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a45ba33822548b0c06c0b589422aa2570)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > res,const `[`TParameter`](#structshogun_1_1TParameter)` * param)` | returns derivative of negative log marginal likelihood wrt param when W has at least one negative element
`protected virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_derivative_related_cov`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1ae947766acf33f97e37480d9b7093395d)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > ddiagKi,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > dKuui,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > dKui)` | compute variables which are required to compute negative log marginal likelihood full derivatives wrt cov-like hyperparameter $\theta$
`protected virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_derivative_related_mean`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1ada5430dc9fcf52f8f473583130e965fc)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > dmu)` | helper function to compute variables which are required to compute negative log marginal likelihood derivatives wrt mean $\lambda$
`protected virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_derivative_implicit_term_helper`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1af50cfaad80c1320d89a5290813189761)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > d)` | helper function to compute variables which are required to compute negative log marginal likelihood implicit derivatives
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_psi_wrt_alpha`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a3ffd50c4d7bade14d12dad78784487b2)`()` | compute the function value given the current alpha
`protected void `[`get_gradient_wrt_alpha`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a6101417a4131bd72307898366360aaa6)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > gradient)` | compute the gradient given the current alpha
`protected virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_derivative_related_cov`](#classshogun_1_1CSingleFITCInference_1a4ee1e17a3d58960c9f78fd437aa2217f)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > ddiagKi,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > dKuui,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > dKui,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > v,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > R)` | compute variables which are required to compute negative log marginal likelihood derivatives wrt cov-like hyperparameter $\theta$
`protected virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_derivative_related_cov_helper`](#classshogun_1_1CSingleFITCInference_1ae1675340753f488a2f7ad45102aed5f9)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > dKuui,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > v,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > R)` | helper function to compute variables which are required to compute negative log marginal likelihood derivatives wrt cov-like hyperparameter $\theta$
`protected virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_derivative_related_cov_diagonal`](#classshogun_1_1CSingleFITCInference_1a2a9db00abb7f5e50000925faed509f73)`()` | helper function to compute variables which are required to compute negative log marginal likelihood derivatives wrt the diagonal part of cov-like hyperparameter $\theta$
`protected virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_derivative_related_inducing_features`](#classshogun_1_1CSingleFITCInference_1a989218742ae1577f4dbd6d21cbfbf89a)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > BdK,const `[`TParameter`](#structshogun_1_1TParameter)` * param)` | helper function to compute variables which are required to compute negative log marginal likelihood derivatives wrt inducing features
`protected virtual void `[`check_bound`](#classshogun_1_1CSingleSparseInference_1a0e4939e8788de9d5e526733018e6303a)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > bound,const char * name)` | check the bound constraint is vailid or not
`protected virtual void `[`check_fully_sparse`](#classshogun_1_1CSingleSparseInference_1aabe920d79ee0eed1cbe147ff01fd2f21)`()` | check whether the provided kernel can compute the gradient wrt inducing features
`protected virtual void `[`convert_features`](#classshogun_1_1CSparseInference_1aa2fab9c1eeb074ac376fffb4f738c4c1)`()` | convert inducing features and features to the same represention
`protected virtual void `[`check_features`](#classshogun_1_1CSparseInference_1a1640c0ac6893cfbc0475d647755167c8)`()` | check whether features and inducing features are set
`protected virtual void `[`check_members`](#classshogun_1_1CSparseInference_1a5262280ea3c5c4aa509aeeccb158efcc)`() const` | check if members of object are valid for inference
`protected virtual void `[`update_train_kernel`](#classshogun_1_1CSparseInference_1ab51c0dbc94ad1732dd644a907595e4bb)`()` | update train kernel matrix
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

#### `public  `[`CSingleFITCLaplaceInferenceMethod`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a27a501f868d62aa7cfc1a7556e7dcd96)`()` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a27a501f868d62aa7cfc1a7556e7dcd96}

default constructor

#### `public  `[`CSingleFITCLaplaceInferenceMethod`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a950a002fc3ea2e6ea826eaf1a22151cc)`(`[`CKernel`](#classshogun_1_1CKernel)` * kernel,`[`CFeatures`](#classshogun_1_1CFeatures)` * features,`[`CMeanFunction`](#classshogun_1_1CMeanFunction)` * mean,`[`CLabels`](#classshogun_1_1CLabels)` * labels,`[`CLikelihoodModel`](#classshogun_1_1CLikelihoodModel)` * model,`[`CFeatures`](#classshogun_1_1CFeatures)` * inducing_features)` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a950a002fc3ea2e6ea826eaf1a22151cc}

constructor

#### Parameters
* `kernel` covariance function 

* `features` features to use in inference 

* `mean` mean function 

* `labels` labels of the features 

* `model` Likelihood model to use 

* `inducing_features` features to use

#### `public virtual  `[`~CSingleFITCLaplaceInferenceMethod`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a787430b0bb1a508f55235cc0be491fad)`()` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a787430b0bb1a508f55235cc0be491fad}

#### `public inline virtual const char * `[`get_name`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a9cb485686dd7a1e6f7103cf42e87717e}

returns the name of the inference method

#### Returns
name SingleFITCLaplace

#### `public inline virtual `[`EInferenceType`](#namespaceshogun_1af211cbb4dbc85162c4d855bd08e2122b)` `[`get_inference_type`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1aa1690a0c36fecfd3ab9bca7e09e6d62d)`() const` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1aa1690a0c36fecfd3ab9bca7e09e6d62d}

return what type of inference we are

#### Returns
inference type FITC

#### `public inline virtual bool `[`supports_regression`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a14c93de070b9c7b9b5c87ef2dac1d515)`() const` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a14c93de070b9c7b9b5c87ef2dac1d515}

#### Returns
whether combination of Laplace approximation inference method and given likelihood function supports regression

#### `public inline virtual bool `[`supports_binary`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1aeb433012dfd6a925ad198e24d5a41976)`() const` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1aeb433012dfd6a925ad198e24d5a41976}

#### Returns
whether combination of Laplace approximation inference method and given likelihood function supports binary classification

#### `public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_diagonal_vector`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1aeeef6125b8cd17aa89459914d6d2ae7b)`()` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1aeeef6125b8cd17aa89459914d6d2ae7b}

get diagonal vector

#### Returns
diagonal of matrix used to calculate posterior covariance matrix:

#### `public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_posterior_mean`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a354c199b5cc758b9d82b7b6070bba7b0)`()` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a354c199b5cc758b9d82b7b6070bba7b0}

returns mean vector $\mu$ of the Gaussian distribution $\mathcal{N}(\mu,\Sigma)$, which is an approximation to the posterior:

$$
p(f_n|y) \approx q(f|y) = \mathcal{N}(f|\mu,\Sigma)
$$

Mean vector $\mu$ is evaluated using FITC inference and Newton's method.

#### Returns
mean vector

#### `public virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_posterior_covariance`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1acfb7e948b3dad546ace3422c6c94ca41)`()` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1acfb7e948b3dad546ace3422c6c94ca41}

returns covariance matrix $\Sigma=(K^{-1}+W)^{-1}$ of the Gaussian distribution $\mathcal{N}(\mu,\Sigma)$, which is an approximation to the posterior:

Note that the time complexity of this method is O(n^3), where n is the number of samples

$$
p(f_n|y) \approx q(f|y) = \mathcal{N}(f|\mu,\Sigma)
$$

#### Returns
covariance matrix

#### `public virtual void `[`update`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1ac5c54df7ed3b930268c8d7752c101725)`()` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1ac5c54df7ed3b930268c8d7752c101725}

update matrices except gradients

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_negative_log_marginal_likelihood`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a9d168a7d73ff38d40c1b12929ca1b575)`()` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a9d168a7d73ff38d40c1b12929ca1b575}

get negative log marginal likelihood

#### Returns
the negative log of the (approximated) marginal likelihood function:

$$
-log(p(y|X, \theta))
$$

where $y$ are the labels, $X$ are the features, and $\theta$ represent hyperparameters.

#### `public virtual void `[`register_minimizer`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a677b05b09eef6bab839953b794c9096a)`(`[`Minimizer`](#classshogun_1_1Minimizer)` * minimizer)` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a677b05b09eef6bab839953b794c9096a}

Set a minimizer

#### Parameters
* `minimizer` minimizer used in inference method

#### `public virtual void `[`set_kernel`](#classshogun_1_1CSingleSparseInference_1a2952b17be257e98e4a2bcadf20c11e3a)`(`[`CKernel`](#classshogun_1_1CKernel)` * kern)` {#classshogun_1_1CSingleSparseInference_1a2952b17be257e98e4a2bcadf20c11e3a}

set kernel

#### Parameters
* `kern` kernel to set

#### `public virtual void `[`optimize_inducing_features`](#classshogun_1_1CSingleSparseInference_1abee0aa1265dc45fb20f2dec6d94fe1f7)`()` {#classshogun_1_1CSingleSparseInference_1abee0aa1265dc45fb20f2dec6d94fe1f7}

opitmize inducing features

#### `public virtual void `[`set_lower_bound_of_inducing_features`](#classshogun_1_1CSingleSparseInference_1a947c06b3f127d6c2247ba77e87698d55)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > bound)` {#classshogun_1_1CSingleSparseInference_1a947c06b3f127d6c2247ba77e87698d55}

set the lower bound of inducing features

#### Parameters
* `bound` lower bound constrains of inducing features

Note that if the length of the bound is 1, it means the bound constraint applies to each dimension of all inducing features

Note that if the length of the bound is greater than 1, it means each dimension of the bound constraint applies to the corresponding dimension of inducing features

#### `public virtual void `[`set_upper_bound_of_inducing_features`](#classshogun_1_1CSingleSparseInference_1a961c8444d4d84d2486ad8ebc2f0d1ff1)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > bound)` {#classshogun_1_1CSingleSparseInference_1a961c8444d4d84d2486ad8ebc2f0d1ff1}

set the upper bound of inducing features

#### Parameters
* `bound` upper bound constrains of inducing features

Note that if the length of the bound is 1, it means the bound constraint applies to each dimension of all inducing features

Note that if the length of the bound is greater than 1, it means each dimension of the bound constraint applies to the corresponding dimension of inducing features

#### `public virtual void `[`set_tolearance_for_inducing_features`](#classshogun_1_1CSingleSparseInference_1a259d3827cd9c645a3cb5bab99fa35faa)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` tol)` {#classshogun_1_1CSingleSparseInference_1a259d3827cd9c645a3cb5bab99fa35faa}

set the tolearance used in optimization of inducing features

#### Parameters
* `tol` tolearance

#### `public virtual void `[`set_max_iterations_for_inducing_features`](#classshogun_1_1CSingleSparseInference_1a4ce96b6f9f05c85829aa1dfaefa11466)`(int32_t it)` {#classshogun_1_1CSingleSparseInference_1a4ce96b6f9f05c85829aa1dfaefa11466}

set the max number of iterations used in optimization of inducing features

#### Parameters
* `it` max number of iterations

#### `public virtual void `[`enable_optimizing_inducing_features`](#classshogun_1_1CSingleSparseInference_1a03572b9530025272167c6145940b3e70)`(bool is_optmization,`[`FirstOrderMinimizer`](#classshogun_1_1FirstOrderMinimizer)` * minimizer)` {#classshogun_1_1CSingleSparseInference_1a03572b9530025272167c6145940b3e70}

whether enable to opitmize inducing features

#### Parameters
* `is_optmization` enable optimization 

* `minimizer` minimizer used in optimization

#### `public inline virtual void `[`set_inducing_features`](#classshogun_1_1CSparseInference_1a45a4fbdc85f275841d46e6455883df73)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * feat)` {#classshogun_1_1CSparseInference_1a45a4fbdc85f275841d46e6455883df73}

set inducing features

#### Parameters
* `feat` features to set

#### `public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`get_inducing_features`](#classshogun_1_1CSparseInference_1ad553e57045ee40819016e8d3fadded4f)`()` {#classshogun_1_1CSparseInference_1ad553e57045ee40819016e8d3fadded4f}

get inducing features

#### Returns
features

#### `public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_alpha`](#classshogun_1_1CSparseInference_1a81e656eac199852421b3a51c92418dc4)`()` {#classshogun_1_1CSparseInference_1a81e656eac199852421b3a51c92418dc4}

get alpha vector

#### Returns
vector to compute posterior mean of Gaussian Process:

$$
\mu = K\alpha
$$

where $\mu$ is the mean and $K$ is the prior covariance matrix.

#### `public virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_cholesky`](#classshogun_1_1CSparseInference_1ae9147e300e23bf1fc49efcd1efc872f5)`()` {#classshogun_1_1CSparseInference_1ae9147e300e23bf1fc49efcd1efc872f5}

get Cholesky decomposition matrix

#### Returns
Cholesky decomposition of matrix:

$$
L = Cholesky(sW*K*sW+I)
$$

where $K$ is the prior covariance matrix, $sW$ is the vector returned by [get_diagonal_vector()](#classshogun_1_1CInference_1ac9c87e5d0581ff9d60e545f286e6edc1), and $I$ is the identity matrix.

#### `public virtual void `[`set_inducing_noise`](#classshogun_1_1CSparseInference_1a41290707e80a0b364b7fe532f5436f44)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` noise)` {#classshogun_1_1CSparseInference_1a41290707e80a0b364b7fe532f5436f44}

set the noise for inducing points

#### Parameters
* `noise` noise for inducing points

The noise is used to enfore the kernel matrix about the inducing points are positive definite

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_inducing_noise`](#classshogun_1_1CSparseInference_1a3cc7fed6b9fb491f884aa28bd437dade)`()` {#classshogun_1_1CSparseInference_1a3cc7fed6b9fb491f884aa28bd437dade}

get the noise for inducing points

#### Returns
noise noise for inducing points

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_marginal_likelihood_estimate`](#classshogun_1_1CInference_1a6e4c3c79df2e7dbb33a0cd9d392dbc6b)`(int32_t num_importance_samples,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` ridge_size)` {#classshogun_1_1CInference_1a6e4c3c79df2e7dbb33a0cd9d392dbc6b}

Computes an unbiased estimate of the marginal-likelihood (in log-domain),

$$
p(y|X,\theta),
$$
 where $y$ are the labels, $X$ are the features (omitted from in the following expressions), and $\theta$ represent hyperparameters.

This is done via a Gaussian approximation to the posterior $q(f|y, \theta)\approx p(f|y, \theta)$, which is computed by the underlying [CInference](#classshogun_1_1CInference) instance (if implemented, otherwise error), and then using an importance sample estimator

$$
p(y|\theta)=\int p(y|f)p(f|\theta)df =\int p(y|f)\frac{p(f|\theta)}{q(f|y, \theta)}q(f|y, \theta)df \approx\frac{1}{n}\sum_{i=1}^n p(y|f^{(i)})\frac{p(f^{(i)}|\theta)} {q(f^{(i)}|y, \theta)},
$$

where $ f^{(i)} $ are samples from the posterior approximation $ q(f|y, \theta) $. The resulting estimator has a low variance if $ q(f|y, \theta) $ is a good approximation. It has large variance otherwise (while still being consistent). Storing all number of log-domain ensures numerical stability.

#### Parameters
* `num_importance_samples` the number of importance samples $n$ from $ q(f|y, \theta) $. 

* `ridge_size` scalar that is added to the diagonal of the involved Gaussian distribution's covariance of GP prior and posterior approximation to stabilise things. Increase if covariance matrix is not numerically positive semi-definite.

#### Returns
unbiased estimate of the marginal likelihood function $ p(y|\theta),$ in log-domain.

#### `public virtual `[`CMap](#classshogun_1_1CMap)< [TParameter](#structshogun_1_1TParameter) *, [SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > > * `[`get_negative_log_marginal_likelihood_derivatives`](#classshogun_1_1CInference_1a0c5d57cdb86528e769a2e1b9a355b6fa)`(`[`CMap](#classshogun_1_1CMap)< [TParameter](#structshogun_1_1TParameter) *, [CSGObject`](#classshogun_1_1CSGObject)` *> * parameters)` {#classshogun_1_1CInference_1a0c5d57cdb86528e769a2e1b9a355b6fa}

get log marginal likelihood gradient

#### Returns
vector of the marginal likelihood function gradient with respect to hyperparameters (under the current approximation to the posterior $q(f|y)\approx p(f|y)$:

$$
-\frac{\partial log(p(y|X, \theta))}{\partial \theta}
$$

where $y$ are the labels, $X$ are the features, and $\theta$ represent hyperparameters.

#### `public inline virtual `[`CMap](#classshogun_1_1CMap)< [TParameter](#structshogun_1_1TParameter) *, [SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > > * `[`get_gradient`](#classshogun_1_1CInference_1a19d9b05672d6ba91505a180bdb51c1a8)`(`[`CMap](#classshogun_1_1CMap)< [TParameter](#structshogun_1_1TParameter) *, [CSGObject`](#classshogun_1_1CSGObject)` *> * parameters)` {#classshogun_1_1CInference_1a19d9b05672d6ba91505a180bdb51c1a8}

get the gradient

#### Parameters
* `parameters` parameter's dictionary

#### Returns
map of gradient. Keys are names of parameters, values are values of derivative with respect to that parameter.

#### `public inline virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_value`](#classshogun_1_1CInference_1a91c887d42da386aabc8765ff395afa30)`()` {#classshogun_1_1CInference_1a91c887d42da386aabc8765ff395afa30}

get the function value

#### Returns
vector that represents the function value

#### `public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`get_features`](#classshogun_1_1CInference_1a7ec6aec639e612c981d12d436950bf57)`()` {#classshogun_1_1CInference_1a7ec6aec639e612c981d12d436950bf57}

get features

#### Returns
features

#### `public inline virtual void `[`set_features`](#classshogun_1_1CInference_1a1ce34ed4aaad4f9ee4e0fa6f5ca6643e)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * feat)` {#classshogun_1_1CInference_1a1ce34ed4aaad4f9ee4e0fa6f5ca6643e}

set features

#### Parameters
* `feat` features to set

#### `public inline virtual `[`CKernel`](#classshogun_1_1CKernel)` * `[`get_kernel`](#classshogun_1_1CInference_1a7b613c50f18bb224844708c436b9b970)`()` {#classshogun_1_1CInference_1a7b613c50f18bb224844708c436b9b970}

get kernel

#### Returns
kernel

#### `public inline virtual `[`CMeanFunction`](#classshogun_1_1CMeanFunction)` * `[`get_mean`](#classshogun_1_1CInference_1a707b09ed75d22e85849b3198bf23c591)`()` {#classshogun_1_1CInference_1a707b09ed75d22e85849b3198bf23c591}

get mean

#### Returns
mean

#### `public inline virtual void `[`set_mean`](#classshogun_1_1CInference_1a1f0f0e7c8ebecbe7bb9cde3901414d93)`(`[`CMeanFunction`](#classshogun_1_1CMeanFunction)` * m)` {#classshogun_1_1CInference_1a1f0f0e7c8ebecbe7bb9cde3901414d93}

set mean

#### Parameters
* `m` mean function to set

#### `public inline virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`get_labels`](#classshogun_1_1CInference_1a9dea304fdcdc2dd7be8bed7f10720f77)`()` {#classshogun_1_1CInference_1a9dea304fdcdc2dd7be8bed7f10720f77}

get labels

#### Returns
labels

#### `public inline virtual void `[`set_labels`](#classshogun_1_1CInference_1a018196e9672050b27f59e04a251a060a)`(`[`CLabels`](#classshogun_1_1CLabels)` * lab)` {#classshogun_1_1CInference_1a018196e9672050b27f59e04a251a060a}

set labels

#### Parameters
* `lab` label to set

#### `public inline `[`CLikelihoodModel`](#classshogun_1_1CLikelihoodModel)` * `[`get_model`](#classshogun_1_1CInference_1a14f34a32af31dad38950cc5479009521)`()` {#classshogun_1_1CInference_1a14f34a32af31dad38950cc5479009521}

get likelihood model

#### Returns
likelihood

#### `public inline virtual void `[`set_model`](#classshogun_1_1CInference_1aa73afad18520515ab6ab7eca88b9ab58)`(`[`CLikelihoodModel`](#classshogun_1_1CLikelihoodModel)` * mod)` {#classshogun_1_1CInference_1aa73afad18520515ab6ab7eca88b9ab58}

set likelihood model

#### Parameters
* `mod` model to set

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_scale`](#classshogun_1_1CInference_1af5bf7c06ba4887a1d9178c161ec18153)`() const` {#classshogun_1_1CInference_1af5bf7c06ba4887a1d9178c161ec18153}

get kernel scale

#### Returns
kernel scale

#### `public virtual void `[`set_scale`](#classshogun_1_1CInference_1ad9b699b761021293ea97658f2bdb0ca6)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` scale)` {#classshogun_1_1CInference_1ad9b699b761021293ea97658f2bdb0ca6}

set kernel scale

#### Parameters
* `scale` scale to be set

#### `public inline virtual bool `[`supports_multiclass`](#classshogun_1_1CInference_1af95ed88e9e900a577e55104b16c93c09)`() const` {#classshogun_1_1CInference_1af95ed88e9e900a577e55104b16c93c09}

whether combination of inference method and given likelihood function supports multiclass classification

#### Returns
false

#### `public virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_multiclass_E`](#classshogun_1_1CInference_1ab4ce31c7340d2031f529b11b5336d511)`()` {#classshogun_1_1CInference_1ab4ce31c7340d2031f529b11b5336d511}

get the E matrix used for multi classification

#### Returns
the matrix for multi classification

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

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_mean_f`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a9857804080a61debb66368a7704af5e2) {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a9857804080a61debb66368a7704af5e2}

a parameter used to compute function value and gradient for LBFGS update

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_sW`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a0ad15ab494883e17a3a1f1aab4916fe9) {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a0ad15ab494883e17a3a1f1aab4916fe9}

square root of W

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_d2lp`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a3f83a9fda6d9fa1d54401457c6feafa6) {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a3f83a9fda6d9fa1d54401457c6feafa6}

second derivative of log likelihood with respect to function location

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_d3lp`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a54a71a30024c3820da8fe3a290fe1147) {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a54a71a30024c3820da8fe3a290fe1147}

third derivative of log likelihood with respect to function location

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_dlp`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1adcdd0d952c755827a551fac2543af8ad) {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1adcdd0d952c755827a551fac2543af8ad}

derivative of log likelihood with respect to function location

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_W`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1ada8808ae54e77ccf819372dcb48c7de6) {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1ada8808ae54e77ccf819372dcb48c7de6}

noise matrix

#### `protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_chol_R0`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a277f0cd7be98e7adc2ce3f76d96b7d9b) {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a277f0cd7be98e7adc2ce3f76d96b7d9b}

Cholesky of inverse covariance of inducing features

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_dfhat`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1aaeaae07cd7d3fdd999afef3230c4bceb) {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1aaeaae07cd7d3fdd999afef3230c4bceb}

derivative of negative log (approximated) marginal likelihood wrt f

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_g`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a05e49d6564de3c7373c7f013ec1a6ab1) {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a05e49d6564de3c7373c7f013ec1a6ab1}

g defined in infFITC_Laplace.m

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_Psi`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a3ba2fc0b7b52439cc330c808867868f2) {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a3ba2fc0b7b52439cc330c808867868f2}

the negative log likelihood without constant terms of 
$$
-log(p(f_n|y))
$$
 used in Newton's method

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_dg`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1ade1f32b52f5be3688c28c7c278001aaa) {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1ade1f32b52f5be3688c28c7c278001aaa}

d0 defined in infFITC_Laplace.m

#### `protected bool `[`m_Wneg`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1afcead5bc781ff0e45ec80d4607bc710d) {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1afcead5bc781ff0e45ec80d4607bc710d}

whether W contains negative elements

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_al`](#classshogun_1_1CSingleFITCInference_1acb243275b7aeb3c8dfb48c9db6073ca0) {#classshogun_1_1CSingleFITCInference_1acb243275b7aeb3c8dfb48c9db6073ca0}

Note that alpha is NOT post.alpha alpha and post.alpha are defined in infFITC.m and infFITC_Laplace.m

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_t`](#classshogun_1_1CSingleFITCInference_1a62de6a998432de37df5636b13c799ae2) {#classshogun_1_1CSingleFITCInference_1a62de6a998432de37df5636b13c799ae2}

t=1/g_sn2 in regression, where g_sn2 is defined in infFITC.m t=W.*dd in Laplace for binary classification, where W and dd are defined in infFITC_Laplace.m

#### `protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_B`](#classshogun_1_1CSingleFITCInference_1ad7f2f8705f1a6681553fff80ad797fb3) {#classshogun_1_1CSingleFITCInference_1ad7f2f8705f1a6681553fff80ad797fb3}

B is defined in infFITC.m and infFITC_Laplace.m

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_w`](#classshogun_1_1CSingleFITCInference_1aa81433bf01d10f2e9bbeb5ed96eadd93) {#classshogun_1_1CSingleFITCInference_1aa81433bf01d10f2e9bbeb5ed96eadd93}

w=B*al

#### `protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_Rvdd`](#classshogun_1_1CSingleFITCInference_1a1c950db882d4eee7830f6b5e7ae03b43) {#classshogun_1_1CSingleFITCInference_1a1c950db882d4eee7830f6b5e7ae03b43}

Rvdd=W where W is defined in infFITC.m and Rvdd is defined in infFITC_Laplace.m Note that W is NOT the diagonal matrix

#### `protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_V`](#classshogun_1_1CSingleFITCInference_1a02aed9430b96257abefd934fc0984082) {#classshogun_1_1CSingleFITCInference_1a02aed9430b96257abefd934fc0984082}

V defined in infFITC.m and infFITC_Laplace.m

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_lower_bound`](#classshogun_1_1CSingleSparseInference_1a178ca1525cfcac4910869f996b934455) {#classshogun_1_1CSingleSparseInference_1a178ca1525cfcac4910869f996b934455}

lower bound of inducing features

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_upper_bound`](#classshogun_1_1CSingleSparseInference_1a152113d2622036eccfc65bdff1129268) {#classshogun_1_1CSingleSparseInference_1a152113d2622036eccfc65bdff1129268}

upper bound of inducing features

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_max_ind_iterations`](#classshogun_1_1CSingleSparseInference_1afeed637fee40abda40e73192e79d8dcd) {#classshogun_1_1CSingleSparseInference_1afeed637fee40abda40e73192e79d8dcd}

max number of iterations

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_ind_tolerance`](#classshogun_1_1CSingleSparseInference_1a7115b181ecd2ca9e7810767dd07874de) {#classshogun_1_1CSingleSparseInference_1a7115b181ecd2ca9e7810767dd07874de}

tolearance used in optimizing inducing_features

#### `protected bool `[`m_opt_inducing_features`](#classshogun_1_1CSingleSparseInference_1a1dabe53c54d8428cbd56bb0363e6086f) {#classshogun_1_1CSingleSparseInference_1a1dabe53c54d8428cbd56bb0363e6086f}

whether optimize inducing features

#### `protected bool `[`m_fully_sparse`](#classshogun_1_1CSingleSparseInference_1a33d67e551071cc5db0327092bb5d2d33) {#classshogun_1_1CSingleSparseInference_1a33d67e551071cc5db0327092bb5d2d33}

whether the kernel supports to get the gradient wrt inducing points or not

#### `protected `[`CLock`](#classshogun_1_1CLock)` * `[`m_lock`](#classshogun_1_1CSingleSparseInference_1ae9abeca94bc2dcc5fccb93433d81f4ff) {#classshogun_1_1CSingleSparseInference_1ae9abeca94bc2dcc5fccb93433d81f4ff}

a lock used to parallelly compute derivatives wrt hyperparameters

#### `protected `[`FirstOrderMinimizer`](#classshogun_1_1FirstOrderMinimizer)` * `[`m_inducing_minimizer`](#classshogun_1_1CSingleSparseInference_1af35a9c8ba4944b3c16aa09fd3b0718f0) {#classshogun_1_1CSingleSparseInference_1af35a9c8ba4944b3c16aa09fd3b0718f0}

minimizer used in finding optimal inducing features

#### `protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_inducing_features`](#classshogun_1_1CSparseInference_1acb7c01ca79f528405214937ffbf8956f) {#classshogun_1_1CSparseInference_1acb7c01ca79f528405214937ffbf8956f}

inducing features for approximation

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_log_ind_noise`](#classshogun_1_1CSparseInference_1a49749703f291dc88c19734f5e94061c9) {#classshogun_1_1CSparseInference_1a49749703f291dc88c19734f5e94061c9}

noise of the inducing variables

#### `protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_kuu`](#classshogun_1_1CSparseInference_1a95912ecbd8b849f3cd6b4860a1c456de) {#classshogun_1_1CSparseInference_1a95912ecbd8b849f3cd6b4860a1c456de}

covariance matrix of inducing features

#### `protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_ktru`](#classshogun_1_1CSparseInference_1a0923be17e60a5cb5ef81557efdec0693) {#classshogun_1_1CSparseInference_1a0923be17e60a5cb5ef81557efdec0693}

covariance matrix of inducing features and training features

#### `protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_Sigma`](#classshogun_1_1CSparseInference_1afb7c413193e6053a3ef68c688e3837fe) {#classshogun_1_1CSparseInference_1afb7c413193e6053a3ef68c688e3837fe}

covariance matrix of the the posterior Gaussian distribution

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_mu`](#classshogun_1_1CSparseInference_1a5573ccd36cd3e2025296478a5e2c5e62) {#classshogun_1_1CSparseInference_1a5573ccd36cd3e2025296478a5e2c5e62}

mean vector of the the posterior Gaussian distribution

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_ktrtr_diag`](#classshogun_1_1CSparseInference_1a9619600b070c1250f501ae18d8a1323d) {#classshogun_1_1CSparseInference_1a9619600b070c1250f501ae18d8a1323d}

diagonal elements of kernel matrix m_ktrtr

#### `protected `[`Minimizer`](#classshogun_1_1Minimizer)` * `[`m_minimizer`](#classshogun_1_1CInference_1a766c444a5e24ea44e0dc51deefcd83ca) {#classshogun_1_1CInference_1a766c444a5e24ea44e0dc51deefcd83ca}

minimizer

#### `protected `[`CKernel`](#classshogun_1_1CKernel)` * `[`m_kernel`](#classshogun_1_1CInference_1ada185a4ebba125dd54f4d0d18ae494e0) {#classshogun_1_1CInference_1ada185a4ebba125dd54f4d0d18ae494e0}

covariance function

#### `protected `[`CMeanFunction`](#classshogun_1_1CMeanFunction)` * `[`m_mean`](#classshogun_1_1CInference_1a76304a61b8f285fd66896aab5d829a57) {#classshogun_1_1CInference_1a76304a61b8f285fd66896aab5d829a57}

mean function

#### `protected `[`CLikelihoodModel`](#classshogun_1_1CLikelihoodModel)` * `[`m_model`](#classshogun_1_1CInference_1a8dd2ad293c3b26f2decd134a8430f936) {#classshogun_1_1CInference_1a8dd2ad293c3b26f2decd134a8430f936}

likelihood function to use

#### `protected `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`m_features`](#classshogun_1_1CInference_1a0d3e1aae112ff755c8e0e651070a4add) {#classshogun_1_1CInference_1a0d3e1aae112ff755c8e0e651070a4add}

features to use

#### `protected `[`CLabels`](#classshogun_1_1CLabels)` * `[`m_labels`](#classshogun_1_1CInference_1af3451cc972288f8c92ef7369952b805b) {#classshogun_1_1CInference_1af3451cc972288f8c92ef7369952b805b}

labels of features

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_alpha`](#classshogun_1_1CInference_1adbf2e7c7892979cd2e78ba11b32855c6) {#classshogun_1_1CInference_1adbf2e7c7892979cd2e78ba11b32855c6}

alpha vector used in process mean calculation

#### `protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_L`](#classshogun_1_1CInference_1a4eb1f068212c66a37e53fae9d8dd4d7d) {#classshogun_1_1CInference_1a4eb1f068212c66a37e53fae9d8dd4d7d}

upper triangular factor of Cholesky decomposition

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_log_scale`](#classshogun_1_1CInference_1a48bfe2f7d129b68a09b9a2a25f0b0b67) {#classshogun_1_1CInference_1a48bfe2f7d129b68a09b9a2a25f0b0b67}

kernel scale

#### `protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_ktrtr`](#classshogun_1_1CInference_1a6df22eadf2014fb840e24b9665eda337) {#classshogun_1_1CInference_1a6df22eadf2014fb840e24b9665eda337}

kernel matrix from features (non-scalled by inference scalling)

#### `protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_E`](#classshogun_1_1CInference_1a1f854dae153b08f91e345ea5c24366bf) {#classshogun_1_1CInference_1a1f854dae153b08f91e345ea5c24366bf}

the matrix used for multi classification

#### `protected bool `[`m_gradient_update`](#classshogun_1_1CInference_1a05c35b833c45472a266e936b50680191) {#classshogun_1_1CInference_1a05c35b833c45472a266e936b50680191}

Whether gradients are updated

#### `protected virtual void `[`compute_gradient`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a45f790a0f06e7fe5b94389b5d2ffd911)`()` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a45f790a0f06e7fe5b94389b5d2ffd911}

update gradients

#### `protected virtual void `[`update_init`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a93b4c26b29456a89d6b383a881a95a90)`()` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a93b4c26b29456a89d6b383a881a95a90}

pre-compution for Newton's method

#### `protected virtual void `[`update_alpha`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1ae68f6c7520ab3314edd7d291079159e3)`()` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1ae68f6c7520ab3314edd7d291079159e3}

update alpha matrix

#### `protected virtual void `[`update_chol`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a7d5df00b072be0d4f11c9424aea4ba04)`()` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a7d5df00b072be0d4f11c9424aea4ba04}

update cholesky matrix

#### `protected virtual void `[`update_approx_cov`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a4333efb3408d2ae500f12dd2edb5c2cb)`()` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a4333efb3408d2ae500f12dd2edb5c2cb}

update covariance matrix of the approximation to the posterior

#### `protected virtual void `[`update_deriv`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a17c88d33d05ee66766ede990fe963bf4)`()` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a17c88d33d05ee66766ede990fe963bf4}

update matrices which are required to compute negative log marginal likelihood derivatives wrt hyperparameter

#### `protected virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_derivative_wrt_inference_method`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a4c99bcd6af8c3134f10a79895d8767e4)`(const `[`TParameter`](#structshogun_1_1TParameter)` * param)` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a4c99bcd6af8c3134f10a79895d8767e4}

returns derivative of negative log marginal likelihood wrt parameter of [CInference](#classshogun_1_1CInference) class

#### Parameters
* `param` parameter of [CInference](#classshogun_1_1CInference) class

#### Returns
derivative of negative log marginal likelihood

#### `protected virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_derivative_wrt_likelihood_model`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a2b5a05afff3755bf8ebb2e94f7c9af8b)`(const `[`TParameter`](#structshogun_1_1TParameter)` * param)` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a2b5a05afff3755bf8ebb2e94f7c9af8b}

returns derivative of negative log marginal likelihood wrt parameter of likelihood model

#### Parameters
* `param` parameter of given likelihood model

#### Returns
derivative of negative log marginal likelihood

#### `protected virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_derivative_wrt_kernel`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a7d855b840228424960622229b81773cf)`(const `[`TParameter`](#structshogun_1_1TParameter)` * param)` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a7d855b840228424960622229b81773cf}

returns derivative of negative log marginal likelihood wrt kernel's parameter

#### Parameters
* `param` parameter of given kernel

#### Returns
derivative of negative log marginal likelihood

#### `protected virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_derivative_wrt_mean`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a7319c9be33b426c9dfa87c4e4c14bbd0)`(const `[`TParameter`](#structshogun_1_1TParameter)` * param)` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a7319c9be33b426c9dfa87c4e4c14bbd0}

returns derivative of negative log marginal likelihood wrt mean function's parameter

#### Parameters
* `param` parameter of given mean function

#### Returns
derivative of negative log marginal likelihood

#### `protected virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_chol_inv`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1aa1b37fead39790feec938bf999e5c935)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > mtx)` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1aa1b37fead39790feec938bf999e5c935}

efficiently compute the Cholesky decomposition of inverse of the input matrix chol(inv(mtx))

#### Parameters
* `mtx` symmetric positive definite matrix

#### Returns
Cholesky decomposition of inverse of the input matrix

#### `protected virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`compute_mvmK`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a6e79ec6211c5bcec9bf9e1b6e06523ce)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > al)` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a6e79ec6211c5bcec9bf9e1b6e06523ce}

efficiently compute the matrix-vector product $\Sigma \times al$, where $\Sigma$ is the FITC equivalent covariance n-by-n matrix (prior) of f_n

#### Parameters
* `al` input vector

#### Returns
the matrix-vector product

#### `protected virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`compute_mvmZ`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a011613073703ad70781ae6e238ae5ca1)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > x)` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a011613073703ad70781ae6e238ae5ca1}

efficiently compute the matrix-vector product $ \inv{\inv{W}+\Sigma} \times x$, where $\Sigma$ is the FITC equivalent covariance n-by-n matrix (prior) of f_n

#### Parameters
* `x` input vector

#### Returns
the matrix-vector product

#### `protected virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_derivative_wrt_inducing_features`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a6a042fa7c7b7865adc44a3dddb53c160)`(const `[`TParameter`](#structshogun_1_1TParameter)` * param)` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a6a042fa7c7b7865adc44a3dddb53c160}

returns derivative of negative log marginal likelihood wrt inducing features (input) Note that in order to call this method, kernel must support FITC inference, which means derivatives wrt inducing features can be computed

Note that the kernel must support to compute the derivatives wrt inducing features

#### Parameters
* `param` parameter of given kernel 

#### Returns
derivative of negative log marginal likelihood

#### `protected virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_derivative_wrt_inducing_noise`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a45b7aff01904f73cbc4318557330fdff)`(const `[`TParameter`](#structshogun_1_1TParameter)` * param)` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a45b7aff01904f73cbc4318557330fdff}

returns derivative of negative log marginal likelihood wrt inducing noise

#### Parameters
* `param` parameter of given inference class

#### Returns
derivative of negative log marginal likelihood

#### `protected virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`derivative_helper_when_Wneg`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a45ba33822548b0c06c0b589422aa2570)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > res,const `[`TParameter`](#structshogun_1_1TParameter)` * param)` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a45ba33822548b0c06c0b589422aa2570}

returns derivative of negative log marginal likelihood wrt param when W has at least one negative element

#### Parameters
* `res` raw derivative 

* `param` parameter

#### Returns
derivative when W has negative element(s)

#### `protected virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_derivative_related_cov`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1ae947766acf33f97e37480d9b7093395d)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > ddiagKi,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > dKuui,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > dKui)` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1ae947766acf33f97e37480d9b7093395d}

compute variables which are required to compute negative log marginal likelihood full derivatives wrt cov-like hyperparameter $\theta$

Note that scale, which is a hyperparameter in inference_method, is a cov-like hyperparameter hyperparameters in cov function are cov-like hyperparameters

#### Parameters
* `ddiagKi` $\textbf{diag}(\frac{\partial {\Sigma_{n}}}{\partial {\theta}})$

* `dKuui` $\frac{\partial {\Sigma_{m}}}{\partial {\theta}}$

* `dKui` $\frac{\partial {\Sigma_{m,n}}}{\partial {\theta}}$

#### Returns
derivative of negative log marginal likelihood

#### `protected virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_derivative_related_mean`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1ada5430dc9fcf52f8f473583130e965fc)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > dmu)` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1ada5430dc9fcf52f8f473583130e965fc}

helper function to compute variables which are required to compute negative log marginal likelihood derivatives wrt mean $\lambda$

#### Parameters
* `dmu` $\frac{\partial {\mu_{n}}}{\partial {\lambda}}$

#### Returns
derivative of negative log marginal likelihood

#### `protected virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_derivative_implicit_term_helper`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1af50cfaad80c1320d89a5290813189761)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > d)` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1af50cfaad80c1320d89a5290813189761}

helper function to compute variables which are required to compute negative log marginal likelihood implicit derivatives

#### Parameters
* `d` raw derivative 

#### Returns
derivative of negative log marginal likelihood

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_psi_wrt_alpha`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a3ffd50c4d7bade14d12dad78784487b2)`()` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a3ffd50c4d7bade14d12dad78784487b2}

compute the function value given the current alpha

#### Returns
the function value

#### `protected void `[`get_gradient_wrt_alpha`](#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a6101417a4131bd72307898366360aaa6)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > gradient)` {#classshogun_1_1CSingleFITCLaplaceInferenceMethod_1a6101417a4131bd72307898366360aaa6}

compute the gradient given the current alpha

#### Parameters
* `gradient` derivative of the function wrt alpha

#### `protected virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_derivative_related_cov`](#classshogun_1_1CSingleFITCInference_1a4ee1e17a3d58960c9f78fd437aa2217f)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > ddiagKi,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > dKuui,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > dKui,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > v,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > R)` {#classshogun_1_1CSingleFITCInference_1a4ee1e17a3d58960c9f78fd437aa2217f}

compute variables which are required to compute negative log marginal likelihood derivatives wrt cov-like hyperparameter $\theta$

Note that scale, which is a hyperparameter in inference_method, is a cov-like hyperparameter hyperparameters in cov function are cov-like hyperparameters

#### Parameters
* `ddiagKi` $\textbf{diag}(\frac{\partial {\Sigma_{n}}}{\partial {\theta}})$

* `dKuui` $\frac{\partial {\Sigma_{m}}}{\partial {\theta}}$

* `dKui` $\frac{\partial {\Sigma_{m,n}}}{\partial {\theta}}$

* `v` auxiliary variable related to explicit derivative 

* `R` auxiliary variable related to explicit derivative

#### Returns
derivative of negative log marginal likelihood

#### `protected virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_derivative_related_cov_helper`](#classshogun_1_1CSingleFITCInference_1ae1675340753f488a2f7ad45102aed5f9)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > dKuui,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > v,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > R)` {#classshogun_1_1CSingleFITCInference_1ae1675340753f488a2f7ad45102aed5f9}

helper function to compute variables which are required to compute negative log marginal likelihood derivatives wrt cov-like hyperparameter $\theta$

Note that scale, which is a hyperparameter in inference_method, is a cov-like hyperparameter hyperparameters in cov function are cov-like hyperparameters what is more, derivative wrt inducing_noise will also use this function

#### Parameters
* `dKuui` $\frac{\partial {\Sigma_{m}}}{\partial {\theta}}$

* `v` auxiliary variable related to explicit derivative 

* `R` auxiliary variable related to explicit derivative

#### Returns
derivative of negative log marginal likelihood

#### `protected virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_derivative_related_cov_diagonal`](#classshogun_1_1CSingleFITCInference_1a2a9db00abb7f5e50000925faed509f73)`()` {#classshogun_1_1CSingleFITCInference_1a2a9db00abb7f5e50000925faed509f73}

helper function to compute variables which are required to compute negative log marginal likelihood derivatives wrt the diagonal part of cov-like hyperparameter $\theta$

#### Returns
derivative of negative log marginal likelihood

#### `protected virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_derivative_related_inducing_features`](#classshogun_1_1CSingleFITCInference_1a989218742ae1577f4dbd6d21cbfbf89a)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > BdK,const `[`TParameter`](#structshogun_1_1TParameter)` * param)` {#classshogun_1_1CSingleFITCInference_1a989218742ae1577f4dbd6d21cbfbf89a}

helper function to compute variables which are required to compute negative log marginal likelihood derivatives wrt inducing features

Note that the kernel must support to compute the derivatives wrt inducing features

#### Parameters
* `BdK` auxiliary variable related to explicit derivative or implicit derivative 

* `param` parameter of given kernel 

#### Returns
derivative of negative log marginal likelihood

#### `protected virtual void `[`check_bound`](#classshogun_1_1CSingleSparseInference_1a0e4939e8788de9d5e526733018e6303a)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > bound,const char * name)` {#classshogun_1_1CSingleSparseInference_1a0e4939e8788de9d5e526733018e6303a}

check the bound constraint is vailid or not

#### Parameters
* `bound` bound constrains of inducing features 

* `name` the name of the bound

#### `protected virtual void `[`check_fully_sparse`](#classshogun_1_1CSingleSparseInference_1aabe920d79ee0eed1cbe147ff01fd2f21)`()` {#classshogun_1_1CSingleSparseInference_1aabe920d79ee0eed1cbe147ff01fd2f21}

check whether the provided kernel can compute the gradient wrt inducing features

Note that currently we check the name of the provided kernel to determine whether the kernel can compute the derivatives wrt inducing_features

The name of a supported Kernel must end with "SparseKernel"

#### `protected virtual void `[`convert_features`](#classshogun_1_1CSparseInference_1aa2fab9c1eeb074ac376fffb4f738c4c1)`()` {#classshogun_1_1CSparseInference_1aa2fab9c1eeb074ac376fffb4f738c4c1}

convert inducing features and features to the same represention

Note that these two kinds of features can be different types. The reasons are listed below. 1. The type of the gradient wrt inducing features is float64_t, which is used to update inducing features 2. Reason 1 implies that the type of inducing features can be float64_t while the type of features does not required as float64_t 3. Reason 2 implies that the type of features must be a subclass of [CDotFeatures](#classshogun_1_1CDotFeatures), which can represent features as float64_t

#### `protected virtual void `[`check_features`](#classshogun_1_1CSparseInference_1a1640c0ac6893cfbc0475d647755167c8)`()` {#classshogun_1_1CSparseInference_1a1640c0ac6893cfbc0475d647755167c8}

check whether features and inducing features are set

#### `protected virtual void `[`check_members`](#classshogun_1_1CSparseInference_1a5262280ea3c5c4aa509aeeccb158efcc)`() const` {#classshogun_1_1CSparseInference_1a5262280ea3c5c4aa509aeeccb158efcc}

check if members of object are valid for inference

#### `protected virtual void `[`update_train_kernel`](#classshogun_1_1CSparseInference_1ab51c0dbc94ad1732dd644a907595e4bb)`()` {#classshogun_1_1CSparseInference_1ab51c0dbc94ad1732dd644a907595e4bb}

update train kernel matrix

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

