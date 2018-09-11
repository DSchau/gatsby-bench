---
classname: "shogun::CLinearHMM"
type: "class"
parents:
   - CDistribution
---

# class `shogun::CLinearHMM` {#classshogun_1_1CLinearHMM}

```
class shogun::CLinearHMM
  : public CDistribution
```

The class LinearHMM is for learning Higher Order Markov chains.

While learning the parameters ${\bf \theta}$ in

$$
\begin{eqnarray*} P({\bf x}|{\bf \theta}^\pm)&=&P(x_1, \ldots, x_N|{\bf \theta}^\pm)\\ &=&P(x_1,\ldots,x_{d}|{\bf \theta}^\pm)\prod_{i=d+1}^N P(x_i|x_{i-1},\ldots,x_{i-d},{\bf \theta}^\pm) \end{eqnarray*}
$$

are determined.

A more detailed description can be found in

Durbin et.al, Biological Sequence Analysis -Probabilistic Models of Proteins and Nucleic Acids, 1998

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
`public  `[`CLinearHMM`](#classshogun_1_1CLinearHMM_1ac51f1bfc9201b000b84a47cbcdc4a917)`()` | default constructor
`public  `[`CLinearHMM`](#classshogun_1_1CLinearHMM_1accb9301b5eebb6329abf8e94aba00843)`(`[`CStringFeatures`](#classshogun_1_1CStringFeatures)`< uint16_t > * f)` | constructor
`public  `[`CLinearHMM`](#classshogun_1_1CLinearHMM_1a5f882d4dba169da7faf65c191e63bc17)`(int32_t p_num_features,int32_t p_num_symbols)` | constructor
`public virtual  `[`~CLinearHMM`](#classshogun_1_1CLinearHMM_1aaea5dd7c60823eeb9c8c453348ee281d)`()` | 
`public virtual bool `[`train`](#classshogun_1_1CLinearHMM_1aa0ece9fd14892c6dfed1bb8c78f3b3ed)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | estimate LinearHMM distribution
`public bool `[`train`](#classshogun_1_1CLinearHMM_1a8e92aed0cf43b39bb91d79b1bf90d115)`(const int32_t * indizes,int32_t num_indizes,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` pseudo_count)` | alternative train distribution
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_log_likelihood_example`](#classshogun_1_1CLinearHMM_1a6e61d7f85c72a3cb3223f3c333249fd1)`(uint16_t * vector,int32_t len)` | get logarithm of one example's likelihood
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_likelihood_example`](#classshogun_1_1CLinearHMM_1a92bf086a57dba8cf535c47151933eb9e)`(uint16_t * vector,int32_t len)` | get one example's likelihood
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_likelihood_example`](#classshogun_1_1CLinearHMM_1a637c8b5f848315124a9e3a78dc0b00b8)`(int32_t num_example)` | compute likelihood for example
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_log_likelihood_example`](#classshogun_1_1CLinearHMM_1a010d74d3406ab0805cf02cd1a7bfe1e7)`(int32_t num_example)` | get logarithm of one example's likelihood
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_log_derivative`](#classshogun_1_1CLinearHMM_1a61b03425333b84df8942e44b876d8769)`(int32_t num_param,int32_t num_example)` | get logarithm of one example's derivative's likelihood
`public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_log_derivative_obsolete`](#classshogun_1_1CLinearHMM_1ae14aaff11e09eb6d33c465644ad80db6)`(uint16_t obs,int32_t pos)` | obsolete get logarithm of one example's derivative's likelihood
`public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_derivative_obsolete`](#classshogun_1_1CLinearHMM_1a348e68d08062a38b3c897b0f958000ce)`(uint16_t * vector,int32_t len,int32_t pos)` | obsolete get one example's derivative
`public inline virtual int32_t `[`get_sequence_length`](#classshogun_1_1CLinearHMM_1a7be850203d60167ca568a699f75e0522)`()` | get sequence length of each example
`public inline virtual int32_t `[`get_num_symbols`](#classshogun_1_1CLinearHMM_1aa32b716c1034d1b2bc07aee7e9e4a0e1)`()` | get number of symbols in examples
`public inline virtual int32_t `[`get_num_model_parameters`](#classshogun_1_1CLinearHMM_1a46c7560aadd676a37b433f0fb3b3f68c)`()` | get number of model parameters
`public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_positional_log_parameter`](#classshogun_1_1CLinearHMM_1ab5af21ec8d7ba6498f889f95b2aeef4a)`(uint16_t obs,int32_t position)` | get positional log parameter
`public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_log_model_parameter`](#classshogun_1_1CLinearHMM_1ac9496ae3be6e14b8aa3c3ea0b78195fa)`(int32_t num_param)` | get logarithm of given model parameter
`public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_log_transition_probs`](#classshogun_1_1CLinearHMM_1a427d3057bc9b6f94c2b8d6fce6212f9b)`()` | get logarithm of all transition probs
`public virtual bool `[`set_log_transition_probs`](#classshogun_1_1CLinearHMM_1af064032859139840f0c865592d1fda3a)`(const `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > probs)` | set logarithm of all transition probs
`public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_transition_probs`](#classshogun_1_1CLinearHMM_1a1eb3756191c30e688ba89eab38a8b3f5)`()` | get all transition probs
`public virtual bool `[`set_transition_probs`](#classshogun_1_1CLinearHMM_1a61739b80fe10436fe39f7d4993a717c6)`(const `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > probs)` | set all transition probs
`public inline virtual const char * `[`get_name`](#classshogun_1_1CLinearHMM_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` | #### Returns
`public virtual int32_t `[`get_num_relevant_model_parameters`](#classshogun_1_1CDistribution_1a45be67a46092d6ee5f8adbe29f9b1ce7)`()` | get number of parameters in model that are relevant, i.e. > ALMOST_NEG_INFTY
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_log_likelihood_sample`](#classshogun_1_1CDistribution_1a8c82b0f4c807e5586f167589bbc11030)`()` | compute log likelihood for whole sample
`public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_log_likelihood`](#classshogun_1_1CDistribution_1a8ad472d42384d515a37f5ab7a4382431)`()` | compute log likelihood for each example
`public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_model_parameter`](#classshogun_1_1CDistribution_1aee8c6fc9aa8692e5516b2546784a1d5e)`(int32_t num_param)` | get model parameter
`public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_derivative`](#classshogun_1_1CDistribution_1aaf3029c0023abbb870eb79e97b6396b4)`(int32_t num_param,int32_t num_example)` | get partial derivative of likelihood function
`public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_likelihood_for_all_examples`](#classshogun_1_1CDistribution_1a1b07d5df60e7e132aa6968dc800c2a8d)`()` | compute likelihood for all vectors in sample
`public inline virtual void `[`set_features`](#classshogun_1_1CDistribution_1a7da63724621f5ac05359326a7b44a124)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * f)` | set feature vectors
`public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`get_features`](#classshogun_1_1CDistribution_1a7ec6aec639e612c981d12d436950bf57)`()` | get feature vectors
`public inline virtual void `[`set_pseudo_count`](#classshogun_1_1CDistribution_1aa1f8ca81f62f6064a98de561c309e6e6)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` pseudo)` | set pseudo count
`public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_pseudo_count`](#classshogun_1_1CDistribution_1a6684463212585b1b2b997fe506a576a0)`()` | get pseudo count
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`update_params_em`](#classshogun_1_1CDistribution_1acc91a9853e2028d5379d67501ee8297b)`(const `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > alpha_k)` | update parameters in the em maximization step for mixture model of which this distribution is a part
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
`protected int32_t `[`sequence_length`](#classshogun_1_1CLinearHMM_1ae7361002243edd88a0db92a794d23424) | examples' sequence length
`protected int32_t `[`num_symbols`](#classshogun_1_1CLinearHMM_1a9871eb10850931bc75e5663d5462e149) | number of symbols in examples
`protected int32_t `[`num_params`](#classshogun_1_1CLinearHMM_1a14b05b0af545224f977cd3bd4fe33f0b) | number of parameters
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`transition_probs`](#classshogun_1_1CLinearHMM_1a5a49551f0ebdad0ea754952cbe51f68b) | transition probs
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`log_transition_probs`](#classshogun_1_1CLinearHMM_1a7af18e81318c460ed1bf2272acb61c58) | logarithm of transition probs
`protected `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`features`](#classshogun_1_1CDistribution_1a0f509925a504265b882b7f01a69fe9bc) | feature vectors
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`pseudo_count`](#classshogun_1_1CDistribution_1aaa5172c589a609b3488ccc34796a3783) | pseudo count
`protected virtual void `[`load_serializable_post`](#classshogun_1_1CLinearHMM_1a4c8da771d1ddf319cabc6b9e896326f2)`()` | Can (optionally) be overridden to post-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::LOAD_SERIALIZABLE_POST is called.
`protected template<>`  <br/>`inline `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`get_sgobject_type_dispatcher`](#classshogun_1_1CSGObject_1a7de7c1e11c3d4322d74a9a8cf5cc13f1)`(const std::string & name)` | 
`protected virtual void `[`load_serializable_pre`](#classshogun_1_1CSGObject_1a7361535fc1a8b13beb9dd0b4ac2dd790)`()` | Can (optionally) be overridden to pre-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::LOAD_SERIALIZABLE_PRE is called.
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

#### `public  `[`CLinearHMM`](#classshogun_1_1CLinearHMM_1ac51f1bfc9201b000b84a47cbcdc4a917)`()` {#classshogun_1_1CLinearHMM_1ac51f1bfc9201b000b84a47cbcdc4a917}

default constructor

#### `public  `[`CLinearHMM`](#classshogun_1_1CLinearHMM_1accb9301b5eebb6329abf8e94aba00843)`(`[`CStringFeatures`](#classshogun_1_1CStringFeatures)`< uint16_t > * f)` {#classshogun_1_1CLinearHMM_1accb9301b5eebb6329abf8e94aba00843}

constructor

#### Parameters
* `f` features to use

#### `public  `[`CLinearHMM`](#classshogun_1_1CLinearHMM_1a5f882d4dba169da7faf65c191e63bc17)`(int32_t p_num_features,int32_t p_num_symbols)` {#classshogun_1_1CLinearHMM_1a5f882d4dba169da7faf65c191e63bc17}

constructor

#### Parameters
* `p_num_features` number of features 

* `p_num_symbols` number of symbols in features

#### `public virtual  `[`~CLinearHMM`](#classshogun_1_1CLinearHMM_1aaea5dd7c60823eeb9c8c453348ee281d)`()` {#classshogun_1_1CLinearHMM_1aaea5dd7c60823eeb9c8c453348ee281d}

#### `public virtual bool `[`train`](#classshogun_1_1CLinearHMM_1aa0ece9fd14892c6dfed1bb8c78f3b3ed)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CLinearHMM_1aa0ece9fd14892c6dfed1bb8c78f3b3ed}

estimate LinearHMM distribution

#### Parameters
* `data` training data (parameter can be avoided if distance or kernel-based classifiers are used and distance/kernels are initialized with train data)

#### Returns
whether training was successful

#### `public bool `[`train`](#classshogun_1_1CLinearHMM_1a8e92aed0cf43b39bb91d79b1bf90d115)`(const int32_t * indizes,int32_t num_indizes,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` pseudo_count)` {#classshogun_1_1CLinearHMM_1a8e92aed0cf43b39bb91d79b1bf90d115}

alternative train distribution

#### Parameters
* `indizes` indices 

* `num_indizes` number of indices 

* `pseudo_count` pseudo count 

#### Returns
if training was successful

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_log_likelihood_example`](#classshogun_1_1CLinearHMM_1a6e61d7f85c72a3cb3223f3c333249fd1)`(uint16_t * vector,int32_t len)` {#classshogun_1_1CLinearHMM_1a6e61d7f85c72a3cb3223f3c333249fd1}

get logarithm of one example's likelihood

#### Parameters
* `vector` the example 

* `len` length of vector 

#### Returns
logarithm of likelihood

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_likelihood_example`](#classshogun_1_1CLinearHMM_1a92bf086a57dba8cf535c47151933eb9e)`(uint16_t * vector,int32_t len)` {#classshogun_1_1CLinearHMM_1a92bf086a57dba8cf535c47151933eb9e}

get one example's likelihood

#### Parameters
* `vector` the example 

* `len` length of vector 

#### Returns
likelihood

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_likelihood_example`](#classshogun_1_1CLinearHMM_1a637c8b5f848315124a9e3a78dc0b00b8)`(int32_t num_example)` {#classshogun_1_1CLinearHMM_1a637c8b5f848315124a9e3a78dc0b00b8}

compute likelihood for example

#### Parameters
* `num_example` which example 

#### Returns
likelihood for example

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_log_likelihood_example`](#classshogun_1_1CLinearHMM_1a010d74d3406ab0805cf02cd1a7bfe1e7)`(int32_t num_example)` {#classshogun_1_1CLinearHMM_1a010d74d3406ab0805cf02cd1a7bfe1e7}

get logarithm of one example's likelihood

#### Parameters
* `num_example` which example 

#### Returns
logarithm of example's likelihood

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_log_derivative`](#classshogun_1_1CLinearHMM_1a61b03425333b84df8942e44b876d8769)`(int32_t num_param,int32_t num_example)` {#classshogun_1_1CLinearHMM_1a61b03425333b84df8942e44b876d8769}

get logarithm of one example's derivative's likelihood

#### Parameters
* `num_param` which example's param 

* `num_example` which example 

#### Returns
logarithm of example's derivative

#### `public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_log_derivative_obsolete`](#classshogun_1_1CLinearHMM_1ae14aaff11e09eb6d33c465644ad80db6)`(uint16_t obs,int32_t pos)` {#classshogun_1_1CLinearHMM_1ae14aaff11e09eb6d33c465644ad80db6}

obsolete get logarithm of one example's derivative's likelihood

#### Parameters
* `obs` observation 

* `pos` position

#### `public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_derivative_obsolete`](#classshogun_1_1CLinearHMM_1a348e68d08062a38b3c897b0f958000ce)`(uint16_t * vector,int32_t len,int32_t pos)` {#classshogun_1_1CLinearHMM_1a348e68d08062a38b3c897b0f958000ce}

obsolete get one example's derivative

#### Parameters
* `vector` vector 

* `len` length 

* `pos` position

#### `public inline virtual int32_t `[`get_sequence_length`](#classshogun_1_1CLinearHMM_1a7be850203d60167ca568a699f75e0522)`()` {#classshogun_1_1CLinearHMM_1a7be850203d60167ca568a699f75e0522}

get sequence length of each example

#### Returns
sequence length of each example

#### `public inline virtual int32_t `[`get_num_symbols`](#classshogun_1_1CLinearHMM_1aa32b716c1034d1b2bc07aee7e9e4a0e1)`()` {#classshogun_1_1CLinearHMM_1aa32b716c1034d1b2bc07aee7e9e4a0e1}

get number of symbols in examples

#### Returns
number of symbols in examples

#### `public inline virtual int32_t `[`get_num_model_parameters`](#classshogun_1_1CLinearHMM_1a46c7560aadd676a37b433f0fb3b3f68c)`()` {#classshogun_1_1CLinearHMM_1a46c7560aadd676a37b433f0fb3b3f68c}

get number of model parameters

#### Returns
number of model parameters

#### `public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_positional_log_parameter`](#classshogun_1_1CLinearHMM_1ab5af21ec8d7ba6498f889f95b2aeef4a)`(uint16_t obs,int32_t position)` {#classshogun_1_1CLinearHMM_1ab5af21ec8d7ba6498f889f95b2aeef4a}

get positional log parameter

#### Parameters
* `obs` observation 

* `position` position 

#### Returns
positional log parameter

#### `public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_log_model_parameter`](#classshogun_1_1CLinearHMM_1ac9496ae3be6e14b8aa3c3ea0b78195fa)`(int32_t num_param)` {#classshogun_1_1CLinearHMM_1ac9496ae3be6e14b8aa3c3ea0b78195fa}

get logarithm of given model parameter

#### Parameters
* `num_param` which param 

#### Returns
logarithm of given model parameter

#### `public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_log_transition_probs`](#classshogun_1_1CLinearHMM_1a427d3057bc9b6f94c2b8d6fce6212f9b)`()` {#classshogun_1_1CLinearHMM_1a427d3057bc9b6f94c2b8d6fce6212f9b}

get logarithm of all transition probs

#### Returns
logarithm of transition probs vector

#### `public virtual bool `[`set_log_transition_probs`](#classshogun_1_1CLinearHMM_1af064032859139840f0c865592d1fda3a)`(const `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > probs)` {#classshogun_1_1CLinearHMM_1af064032859139840f0c865592d1fda3a}

set logarithm of all transition probs

#### Parameters
* `probs` new logarithm transition probs 

#### Returns
if setting was successful

#### `public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_transition_probs`](#classshogun_1_1CLinearHMM_1a1eb3756191c30e688ba89eab38a8b3f5)`()` {#classshogun_1_1CLinearHMM_1a1eb3756191c30e688ba89eab38a8b3f5}

get all transition probs

#### Returns
vector of transition probs

#### `public virtual bool `[`set_transition_probs`](#classshogun_1_1CLinearHMM_1a61739b80fe10436fe39f7d4993a717c6)`(const `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > probs)` {#classshogun_1_1CLinearHMM_1a61739b80fe10436fe39f7d4993a717c6}

set all transition probs

#### Parameters
* `probs` new transition probs 

#### Returns
if setting was successful

#### `public inline virtual const char * `[`get_name`](#classshogun_1_1CLinearHMM_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` {#classshogun_1_1CLinearHMM_1a9cb485686dd7a1e6f7103cf42e87717e}

#### Returns
object name

#### `public virtual int32_t `[`get_num_relevant_model_parameters`](#classshogun_1_1CDistribution_1a45be67a46092d6ee5f8adbe29f9b1ce7)`()` {#classshogun_1_1CDistribution_1a45be67a46092d6ee5f8adbe29f9b1ce7}

get number of parameters in model that are relevant, i.e. > ALMOST_NEG_INFTY

#### Returns
number of relevant model parameters

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_log_likelihood_sample`](#classshogun_1_1CDistribution_1a8c82b0f4c807e5586f167589bbc11030)`()` {#classshogun_1_1CDistribution_1a8c82b0f4c807e5586f167589bbc11030}

compute log likelihood for whole sample

#### Returns
log likelihood for whole sample

#### `public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_log_likelihood`](#classshogun_1_1CDistribution_1a8ad472d42384d515a37f5ab7a4382431)`()` {#classshogun_1_1CDistribution_1a8ad472d42384d515a37f5ab7a4382431}

compute log likelihood for each example

#### Returns
log likelihood vector

#### `public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_model_parameter`](#classshogun_1_1CDistribution_1aee8c6fc9aa8692e5516b2546784a1d5e)`(int32_t num_param)` {#classshogun_1_1CDistribution_1aee8c6fc9aa8692e5516b2546784a1d5e}

get model parameter

#### Parameters
* `num_param` which param 

#### Returns
model parameter

#### `public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_derivative`](#classshogun_1_1CDistribution_1aaf3029c0023abbb870eb79e97b6396b4)`(int32_t num_param,int32_t num_example)` {#classshogun_1_1CDistribution_1aaf3029c0023abbb870eb79e97b6396b4}

get partial derivative of likelihood function

#### Parameters
* `num_param` partial derivative against which param 

* `num_example` which example 

#### Returns
derivative of likelihood function

#### `public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_likelihood_for_all_examples`](#classshogun_1_1CDistribution_1a1b07d5df60e7e132aa6968dc800c2a8d)`()` {#classshogun_1_1CDistribution_1a1b07d5df60e7e132aa6968dc800c2a8d}

compute likelihood for all vectors in sample

#### Returns
likelihood vector for all examples

#### `public inline virtual void `[`set_features`](#classshogun_1_1CDistribution_1a7da63724621f5ac05359326a7b44a124)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * f)` {#classshogun_1_1CDistribution_1a7da63724621f5ac05359326a7b44a124}

set feature vectors

#### Parameters
* `f` new feature vectors

#### `public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`get_features`](#classshogun_1_1CDistribution_1a7ec6aec639e612c981d12d436950bf57)`()` {#classshogun_1_1CDistribution_1a7ec6aec639e612c981d12d436950bf57}

get feature vectors

#### Returns
feature vectors

#### `public inline virtual void `[`set_pseudo_count`](#classshogun_1_1CDistribution_1aa1f8ca81f62f6064a98de561c309e6e6)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` pseudo)` {#classshogun_1_1CDistribution_1aa1f8ca81f62f6064a98de561c309e6e6}

set pseudo count

#### Parameters
* `pseudo` new pseudo count

#### `public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_pseudo_count`](#classshogun_1_1CDistribution_1a6684463212585b1b2b997fe506a576a0)`()` {#classshogun_1_1CDistribution_1a6684463212585b1b2b997fe506a576a0}

get pseudo count

#### Returns
pseudo count

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`update_params_em`](#classshogun_1_1CDistribution_1acc91a9853e2028d5379d67501ee8297b)`(const `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > alpha_k)` {#classshogun_1_1CDistribution_1acc91a9853e2028d5379d67501ee8297b}

update parameters in the em maximization step for mixture model of which this distribution is a part

abstract base method

#### Parameters
* `alpha_k` "belongingness" values of various data points 

#### Returns
sum of alpha_k values

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

#### `protected int32_t `[`sequence_length`](#classshogun_1_1CLinearHMM_1ae7361002243edd88a0db92a794d23424) {#classshogun_1_1CLinearHMM_1ae7361002243edd88a0db92a794d23424}

examples' sequence length

#### `protected int32_t `[`num_symbols`](#classshogun_1_1CLinearHMM_1a9871eb10850931bc75e5663d5462e149) {#classshogun_1_1CLinearHMM_1a9871eb10850931bc75e5663d5462e149}

number of symbols in examples

#### `protected int32_t `[`num_params`](#classshogun_1_1CLinearHMM_1a14b05b0af545224f977cd3bd4fe33f0b) {#classshogun_1_1CLinearHMM_1a14b05b0af545224f977cd3bd4fe33f0b}

number of parameters

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`transition_probs`](#classshogun_1_1CLinearHMM_1a5a49551f0ebdad0ea754952cbe51f68b) {#classshogun_1_1CLinearHMM_1a5a49551f0ebdad0ea754952cbe51f68b}

transition probs

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`log_transition_probs`](#classshogun_1_1CLinearHMM_1a7af18e81318c460ed1bf2272acb61c58) {#classshogun_1_1CLinearHMM_1a7af18e81318c460ed1bf2272acb61c58}

logarithm of transition probs

#### `protected `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`features`](#classshogun_1_1CDistribution_1a0f509925a504265b882b7f01a69fe9bc) {#classshogun_1_1CDistribution_1a0f509925a504265b882b7f01a69fe9bc}

feature vectors

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`pseudo_count`](#classshogun_1_1CDistribution_1aaa5172c589a609b3488ccc34796a3783) {#classshogun_1_1CDistribution_1aaa5172c589a609b3488ccc34796a3783}

pseudo count

#### `protected virtual void `[`load_serializable_post`](#classshogun_1_1CLinearHMM_1a4c8da771d1ddf319cabc6b9e896326f2)`()` {#classshogun_1_1CLinearHMM_1a4c8da771d1ddf319cabc6b9e896326f2}

Can (optionally) be overridden to post-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::LOAD_SERIALIZABLE_POST is called.

#### Exceptions
* `[ShogunException](#classshogun_1_1ShogunException)` will be thrown if an error occurs.

#### `protected template<>`  <br/>`inline `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`get_sgobject_type_dispatcher`](#classshogun_1_1CSGObject_1a7de7c1e11c3d4322d74a9a8cf5cc13f1)`(const std::string & name)` {#classshogun_1_1CSGObject_1a7de7c1e11c3d4322d74a9a8cf5cc13f1}

#### `protected virtual void `[`load_serializable_pre`](#classshogun_1_1CSGObject_1a7361535fc1a8b13beb9dd0b4ac2dd790)`()` {#classshogun_1_1CSGObject_1a7361535fc1a8b13beb9dd0b4ac2dd790}

Can (optionally) be overridden to pre-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::LOAD_SERIALIZABLE_PRE is called.

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

