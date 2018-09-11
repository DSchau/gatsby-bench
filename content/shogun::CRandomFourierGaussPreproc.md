---
classname: "shogun::CRandomFourierGaussPreproc"
type: "class"
parents:
   - CDensePreprocessor< float64_t >
---

# class `shogun::CRandomFourierGaussPreproc` {#classshogun_1_1CRandomFourierGaussPreproc}

```
class shogun::CRandomFourierGaussPreproc
  : public CDensePreprocessor< float64_t >
```

Preprocessor [CRandomFourierGaussPreproc](#classshogun_1_1CRandomFourierGaussPreproc) implements Random Fourier Features for the Gauss kernel a la Ali Rahimi and Ben Recht Nips2007 after preprocessing the features using them in a linear kernel approximates a gaussian kernel.

approximation quality depends on dimension of feature space, NOT on number of data.

effectively it requires two parameters for initialization: (A) the dimension of the input features stored in dim_input_space (B) the dimension of the output feature space

in order to make it work there are two ways: (1) if you have already previously computed random fourier features which you want to use together with newly computed ones, then you have to take the random coefficients from the previous computation and provide them via void set_randomcoefficients(...) for the new computation this case is important for example if you compute separately features on training and testing data in two feature objects

in this case you have to set 1a) void set_randomcoefficients(...)

(2) if you compute random fourier features from scratch in this case you have to set 2a) set_kernelwidth(...) 2b) void [set_dim_feature_space(const int32_t dim)](#classshogun_1_1CRandomFourierGaussPreproc_1a28d0060ccf67782ad3ece5556effc8c8); 2c) [set_dim_input_space(const int32_t dim)](#classshogun_1_1CRandomFourierGaussPreproc_1a2f92fc4c8b669cecfc981e4bf1a5a397); 2d) [init_randomcoefficients()](#classshogun_1_1CRandomFourierGaussPreproc_1a996d95f8c661a43bc248c36bea0734e9) or apply_to_feature_matrix(...)

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
`public  `[`CRandomFourierGaussPreproc`](#classshogun_1_1CRandomFourierGaussPreproc_1ae5f0b48d42d76cf1528032a3b54f56cf)`()` | default constructor
`public  `[`CRandomFourierGaussPreproc`](#classshogun_1_1CRandomFourierGaussPreproc_1a032fffc3d7e116a53ae19d80f02a3c83)`(const `[`CRandomFourierGaussPreproc`](#classshogun_1_1CRandomFourierGaussPreproc)` & pr)` | alternative constructor
`public  `[`~CRandomFourierGaussPreproc`](#classshogun_1_1CRandomFourierGaussPreproc_1a1fd50cab2c2b750acd1c25ae463b8524)`()` | default destructor takes care for float64_t* randomcoeff_additive,float64_t* randomcoeff_multiplicative;
`public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`apply_to_feature_vector`](#classshogun_1_1CRandomFourierGaussPreproc_1a45584b03dc12df6e0e4e3d266e1810ef)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > vector)` | alternative processing routine, inherited from base class 
`public virtual `[`EFeatureType`](#namespaceshogun_1a064eec90e91f56435546d77f38c0b618)` `[`get_feature_type`](#classshogun_1_1CRandomFourierGaussPreproc_1a6bb6f080e923887254381abae8af6c76)`()` | inherited from base class 
`public virtual `[`EFeatureClass`](#namespaceshogun_1a9e2a4d8b86b9e061779c3fdbcda57c3b)` `[`get_feature_class`](#classshogun_1_1CRandomFourierGaussPreproc_1a00c0270aae194f8c691f0bd5e897e716)`()` | inherited from base class 
`public virtual void `[`fit`](#classshogun_1_1CRandomFourierGaussPreproc_1a79d18a5ad848eb86c1428da5ea086361)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * f)` | fit to features calls [set_dim_input_space(const int32_t dim)](#classshogun_1_1CRandomFourierGaussPreproc_1a2f92fc4c8b669cecfc981e4bf1a5a397); with the proper value calls [init_randomcoefficients()](#classshogun_1_1CRandomFourierGaussPreproc_1a996d95f8c661a43bc248c36bea0734e9); this call does NOT override a previous call to void set_randomcoefficients(...) IF and ONLY IF the dimensions of input AND feature space are equal to the values from the previous call to void set_randomcoefficients(...) 
`public void `[`set_kernelwidth`](#classshogun_1_1CRandomFourierGaussPreproc_1ac0cd04ef7110d24dd7d6c8827fb7e4c7)`(const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` width)` | setter for kernel width 
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_kernelwidth`](#classshogun_1_1CRandomFourierGaussPreproc_1aea91fcaca2107149967d03ee0fcfff13)`() const` | getter for kernel width 
`public void `[`get_randomcoefficients`](#classshogun_1_1CRandomFourierGaussPreproc_1a62239af5393fbbb0db6d0a9f0f120b00)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` ** randomcoeff_additive2,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` ** randomcoeff_multiplicative2,int32_t * dim_feature_space2,int32_t * dim_input_space2,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * kernelwidth2) const` | getter for the random coefficients necessary for creating random fourier features compatible to the current ones returns values of internal members randomcoeff_additive and randomcoeff_multiplicative
`public void `[`set_randomcoefficients`](#classshogun_1_1CRandomFourierGaussPreproc_1a2cd23030f07e9cd26bbdfea38f8ef72c)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * randomcoeff_additive2,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * randomcoeff_multiplicative2,const int32_t dim_feature_space2,const int32_t dim_input_space2,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` kernelwidth2)` | setter for the random coefficients necessary for creating random fourier features compatible to the previous ones sets values of internal members randomcoeff_additive and randomcoeff_multiplicative simply use as input what you got from get_random_coefficients(...)
`public void `[`set_dim_input_space`](#classshogun_1_1CRandomFourierGaussPreproc_1a2f92fc4c8b669cecfc981e4bf1a5a397)`(const int32_t dim)` | a setter 
`public void `[`set_dim_feature_space`](#classshogun_1_1CRandomFourierGaussPreproc_1a28d0060ccf67782ad3ece5556effc8c8)`(const int32_t dim)` | a setter 
`public bool `[`init_randomcoefficients`](#classshogun_1_1CRandomFourierGaussPreproc_1a996d95f8c661a43bc248c36bea0734e9)`()` | computes new random coefficients IF [test_rfinited()](#classshogun_1_1CRandomFourierGaussPreproc_1a9ae40c30b8175350b26fcb272d638f55) evaluates to false [test_rfinited()](#classshogun_1_1CRandomFourierGaussPreproc_1a9ae40c30b8175350b26fcb272d638f55) evaluates to TRUE if void set_randomcoefficients(...) hase been called and the values set by set_dim_input_space(...) , set_dim_feature_space(...) and set_kernelwidth(...) are consistent to the call of void set_randomcoefficients(...)
`public int32_t `[`get_dim_input_space`](#classshogun_1_1CRandomFourierGaussPreproc_1af08c1d3c1435c7396c51eb1f082dc85d)`() const` | a getter 
`public int32_t `[`get_dim_feature_space`](#classshogun_1_1CRandomFourierGaussPreproc_1a13fbd248e2925b0a24f49889c542e74c)`() const` | a getter 
`public virtual void `[`cleanup`](#classshogun_1_1CRandomFourierGaussPreproc_1a4b66d5e31b5dc18b314c8a68163263bd)`()` | inherited from base class does nothing
`public inline virtual const char * `[`get_name`](#classshogun_1_1CRandomFourierGaussPreproc_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` | return the name of the preprocessor
`public inline virtual `[`EPreprocessorType`](#namespaceshogun_1af6317e92a2bed0d86257f3a589a5e9f3)` `[`get_type`](#classshogun_1_1CRandomFourierGaussPreproc_1afa592e9c6f9e700c293061fceaaac7f2)`() const` | return a type of preprocessor
`public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`transform`](#classshogun_1_1CDensePreprocessor_1a801a3d5a27cc8ad45c887a93e768a987)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * features,bool inplace)` | Apply transformation to dense features.
`public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`inverse_transform`](#classshogun_1_1CDensePreprocessor_1aea5d40ee0debdddaa64170453f7afea5)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * features,bool inplace)` | Apply inverse transformation to dense features.
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
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`kernelwidth`](#classshogun_1_1CRandomFourierGaussPreproc_1a5d4719e1635819a8d7a75071afc4b1aa) | dimension of input features width of gaussian kernel in the form of exp(-x^2 / (2.0 kernelwidth^2) ) NOTE the 2.0 and the power ^2 !
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`cur_kernelwidth`](#classshogun_1_1CRandomFourierGaussPreproc_1ad9613f900cd2737d0a0f26aa9aa9b7d0) | dimension of input features width of gaussian kernel in the form of exp(-x^2 / (2.0 kernelwidth^2) ) NOTE the 2.0 and the power ^2 !
`protected int32_t `[`dim_input_space`](#classshogun_1_1CRandomFourierGaussPreproc_1ab33e340dd7205cf26e60fb10332489aa) | desired dimension of input features as set by void [set_dim_input_space(const int32_t dim)](#classshogun_1_1CRandomFourierGaussPreproc_1a2f92fc4c8b669cecfc981e4bf1a5a397)
`protected int32_t `[`cur_dim_input_space`](#classshogun_1_1CRandomFourierGaussPreproc_1ae4d9512f847895257a0a516bd734fe1b) | actual dimension of input features as set by bool [init_randomcoefficients()](#classshogun_1_1CRandomFourierGaussPreproc_1a996d95f8c661a43bc248c36bea0734e9) or void set_randomcoefficients
`protected int32_t `[`dim_feature_space`](#classshogun_1_1CRandomFourierGaussPreproc_1a16fa41bb143f5f4d0194845963b5f456) | desired dimension of output features as set by void [set_dim_feature_space(const int32_t dim)](#classshogun_1_1CRandomFourierGaussPreproc_1a28d0060ccf67782ad3ece5556effc8c8)
`protected int32_t `[`cur_dim_feature_space`](#classshogun_1_1CRandomFourierGaussPreproc_1a6b76e47958b755a6a7ed85c8e9a71094) | actual dimension of output features as set by bool [init_randomcoefficients()](#classshogun_1_1CRandomFourierGaussPreproc_1a996d95f8c661a43bc248c36bea0734e9) or void set_randomcoefficients
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`randomcoeff_additive`](#classshogun_1_1CRandomFourierGaussPreproc_1a1a960a02e372323dc1df10682865eb3d) | random coefficient length = cur_dim_feature_space
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`randomcoeff_multiplicative`](#classshogun_1_1CRandomFourierGaussPreproc_1a9c835a7ee410a41bc0e0956dae07e5c8) | random coefficient length = cur_dim_feature_space* cur_dim_input_space
`protected bool `[`m_fitted`](#classshogun_1_1CTransformer_1ac7a9f470db2627f8ba58a3880fb34b2e) | 
`protected virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`apply_to_matrix`](#classshogun_1_1CRandomFourierGaussPreproc_1a391ac3239ebff9c47529c19d5dd36d31)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > matrix)` | default processing routine, inherited from base class 
`protected void `[`copy`](#classshogun_1_1CRandomFourierGaussPreproc_1a9ddf854bb0fb7dde02879f456a1d8f5a)`(const `[`CRandomFourierGaussPreproc`](#classshogun_1_1CRandomFourierGaussPreproc)` & feats)` | helper for copy constructor and assignment operator=
`protected bool `[`test_rfinited`](#classshogun_1_1CRandomFourierGaussPreproc_1a9ae40c30b8175350b26fcb272d638f55)`() const` | tests whether rf features have already been initialized
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

#### `public  `[`CRandomFourierGaussPreproc`](#classshogun_1_1CRandomFourierGaussPreproc_1ae5f0b48d42d76cf1528032a3b54f56cf)`()` {#classshogun_1_1CRandomFourierGaussPreproc_1ae5f0b48d42d76cf1528032a3b54f56cf}

default constructor

#### `public  `[`CRandomFourierGaussPreproc`](#classshogun_1_1CRandomFourierGaussPreproc_1a032fffc3d7e116a53ae19d80f02a3c83)`(const `[`CRandomFourierGaussPreproc`](#classshogun_1_1CRandomFourierGaussPreproc)` & pr)` {#classshogun_1_1CRandomFourierGaussPreproc_1a032fffc3d7e116a53ae19d80f02a3c83}

alternative constructor

#### `public  `[`~CRandomFourierGaussPreproc`](#classshogun_1_1CRandomFourierGaussPreproc_1a1fd50cab2c2b750acd1c25ae463b8524)`()` {#classshogun_1_1CRandomFourierGaussPreproc_1a1fd50cab2c2b750acd1c25ae463b8524}

default destructor takes care for float64_t* randomcoeff_additive,float64_t* randomcoeff_multiplicative;

#### `public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`apply_to_feature_vector`](#classshogun_1_1CRandomFourierGaussPreproc_1a45584b03dc12df6e0e4e3d266e1810ef)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > vector)` {#classshogun_1_1CRandomFourierGaussPreproc_1a45584b03dc12df6e0e4e3d266e1810ef}

alternative processing routine, inherited from base class 
#### Parameters
* `vector` the feature vector to be processed 

#### Returns
processed feature vector in order to work this routine requires the steps described above under cases (1) or two (2) before calling this routine

#### `public virtual `[`EFeatureType`](#namespaceshogun_1a064eec90e91f56435546d77f38c0b618)` `[`get_feature_type`](#classshogun_1_1CRandomFourierGaussPreproc_1a6bb6f080e923887254381abae8af6c76)`()` {#classshogun_1_1CRandomFourierGaussPreproc_1a6bb6f080e923887254381abae8af6c76}

inherited from base class 
#### Returns
C_DENSE

#### `public virtual `[`EFeatureClass`](#namespaceshogun_1a9e2a4d8b86b9e061779c3fdbcda57c3b)` `[`get_feature_class`](#classshogun_1_1CRandomFourierGaussPreproc_1a00c0270aae194f8c691f0bd5e897e716)`()` {#classshogun_1_1CRandomFourierGaussPreproc_1a00c0270aae194f8c691f0bd5e897e716}

inherited from base class 
#### Returns
F_DREAL

#### `public virtual void `[`fit`](#classshogun_1_1CRandomFourierGaussPreproc_1a79d18a5ad848eb86c1428da5ea086361)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * f)` {#classshogun_1_1CRandomFourierGaussPreproc_1a79d18a5ad848eb86c1428da5ea086361}

fit to features calls [set_dim_input_space(const int32_t dim)](#classshogun_1_1CRandomFourierGaussPreproc_1a2f92fc4c8b669cecfc981e4bf1a5a397); with the proper value calls [init_randomcoefficients()](#classshogun_1_1CRandomFourierGaussPreproc_1a996d95f8c661a43bc248c36bea0734e9); this call does NOT override a previous call to void set_randomcoefficients(...) IF and ONLY IF the dimensions of input AND feature space are equal to the values from the previous call to void set_randomcoefficients(...) 
#### Parameters
* `f` the features to be processed, must be of type [CDenseFeatures<float64_t>](#classshogun_1_1CDenseFeatures)

#### Returns
true if new random coefficients were generated, false if old ones from a call to set_randomcoefficients(...) are kept

#### `public void `[`set_kernelwidth`](#classshogun_1_1CRandomFourierGaussPreproc_1ac0cd04ef7110d24dd7d6c8827fb7e4c7)`(const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` width)` {#classshogun_1_1CRandomFourierGaussPreproc_1ac0cd04ef7110d24dd7d6c8827fb7e4c7}

setter for kernel width 
#### Parameters
* `width` kernel width to be set

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_kernelwidth`](#classshogun_1_1CRandomFourierGaussPreproc_1aea91fcaca2107149967d03ee0fcfff13)`() const` {#classshogun_1_1CRandomFourierGaussPreproc_1aea91fcaca2107149967d03ee0fcfff13}

getter for kernel width 
#### Returns
kernel width throws exception if kernelwidth <=0

#### `public void `[`get_randomcoefficients`](#classshogun_1_1CRandomFourierGaussPreproc_1a62239af5393fbbb0db6d0a9f0f120b00)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` ** randomcoeff_additive2,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` ** randomcoeff_multiplicative2,int32_t * dim_feature_space2,int32_t * dim_input_space2,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * kernelwidth2) const` {#classshogun_1_1CRandomFourierGaussPreproc_1a62239af5393fbbb0db6d0a9f0f120b00}

getter for the random coefficients necessary for creating random fourier features compatible to the current ones returns values of internal members randomcoeff_additive and randomcoeff_multiplicative

#### `public void `[`set_randomcoefficients`](#classshogun_1_1CRandomFourierGaussPreproc_1a2cd23030f07e9cd26bbdfea38f8ef72c)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * randomcoeff_additive2,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * randomcoeff_multiplicative2,const int32_t dim_feature_space2,const int32_t dim_input_space2,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` kernelwidth2)` {#classshogun_1_1CRandomFourierGaussPreproc_1a2cd23030f07e9cd26bbdfea38f8ef72c}

setter for the random coefficients necessary for creating random fourier features compatible to the previous ones sets values of internal members randomcoeff_additive and randomcoeff_multiplicative simply use as input what you got from get_random_coefficients(...)

#### `public void `[`set_dim_input_space`](#classshogun_1_1CRandomFourierGaussPreproc_1a2f92fc4c8b669cecfc981e4bf1a5a397)`(const int32_t dim)` {#classshogun_1_1CRandomFourierGaussPreproc_1a2f92fc4c8b669cecfc981e4bf1a5a397}

a setter 
#### Parameters
* `dim` the value of protected member dim_input_space throws a shogun exception if dim<=0

#### `public void `[`set_dim_feature_space`](#classshogun_1_1CRandomFourierGaussPreproc_1a28d0060ccf67782ad3ece5556effc8c8)`(const int32_t dim)` {#classshogun_1_1CRandomFourierGaussPreproc_1a28d0060ccf67782ad3ece5556effc8c8}

a setter 
#### Parameters
* `dim` the value of protected member dim_feature_space throws a shogun exception if dim<=0

#### `public bool `[`init_randomcoefficients`](#classshogun_1_1CRandomFourierGaussPreproc_1a996d95f8c661a43bc248c36bea0734e9)`()` {#classshogun_1_1CRandomFourierGaussPreproc_1a996d95f8c661a43bc248c36bea0734e9}

computes new random coefficients IF [test_rfinited()](#classshogun_1_1CRandomFourierGaussPreproc_1a9ae40c30b8175350b26fcb272d638f55) evaluates to false [test_rfinited()](#classshogun_1_1CRandomFourierGaussPreproc_1a9ae40c30b8175350b26fcb272d638f55) evaluates to TRUE if void set_randomcoefficients(...) hase been called and the values set by set_dim_input_space(...) , set_dim_feature_space(...) and set_kernelwidth(...) are consistent to the call of void set_randomcoefficients(...)

throws shogun exception if dim_feature_space <= 0 or dim_input_space <= 0

#### Returns
returns true if [test_rfinited()](#classshogun_1_1CRandomFourierGaussPreproc_1a9ae40c30b8175350b26fcb272d638f55) evaluates to false and new coefficients are computed returns false if [test_rfinited()](#classshogun_1_1CRandomFourierGaussPreproc_1a9ae40c30b8175350b26fcb272d638f55) evaluates to true and old random coefficients are kept which were set by a previous call to void set_randomcoefficients(...)

this function is useful if you want to use apply_to_feature_vector but cannot call before it [fit(CFeatures *f)](#classshogun_1_1CRandomFourierGaussPreproc_1a79d18a5ad848eb86c1428da5ea086361)

#### `public int32_t `[`get_dim_input_space`](#classshogun_1_1CRandomFourierGaussPreproc_1af08c1d3c1435c7396c51eb1f082dc85d)`() const` {#classshogun_1_1CRandomFourierGaussPreproc_1af08c1d3c1435c7396c51eb1f082dc85d}

a getter 
#### Returns
the set value of protected member dim_input_space

#### `public int32_t `[`get_dim_feature_space`](#classshogun_1_1CRandomFourierGaussPreproc_1a13fbd248e2925b0a24f49889c542e74c)`() const` {#classshogun_1_1CRandomFourierGaussPreproc_1a13fbd248e2925b0a24f49889c542e74c}

a getter 
#### Returns
the set value of protected member dim_feature_space

#### `public virtual void `[`cleanup`](#classshogun_1_1CRandomFourierGaussPreproc_1a4b66d5e31b5dc18b314c8a68163263bd)`()` {#classshogun_1_1CRandomFourierGaussPreproc_1a4b66d5e31b5dc18b314c8a68163263bd}

inherited from base class does nothing

#### `public inline virtual const char * `[`get_name`](#classshogun_1_1CRandomFourierGaussPreproc_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` {#classshogun_1_1CRandomFourierGaussPreproc_1a9cb485686dd7a1e6f7103cf42e87717e}

return the name of the preprocessor

#### `public inline virtual `[`EPreprocessorType`](#namespaceshogun_1af6317e92a2bed0d86257f3a589a5e9f3)` `[`get_type`](#classshogun_1_1CRandomFourierGaussPreproc_1afa592e9c6f9e700c293061fceaaac7f2)`() const` {#classshogun_1_1CRandomFourierGaussPreproc_1afa592e9c6f9e700c293061fceaaac7f2}

return a type of preprocessor

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

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`kernelwidth`](#classshogun_1_1CRandomFourierGaussPreproc_1a5d4719e1635819a8d7a75071afc4b1aa) {#classshogun_1_1CRandomFourierGaussPreproc_1a5d4719e1635819a8d7a75071afc4b1aa}

dimension of input features width of gaussian kernel in the form of exp(-x^2 / (2.0 kernelwidth^2) ) NOTE the 2.0 and the power ^2 !

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`cur_kernelwidth`](#classshogun_1_1CRandomFourierGaussPreproc_1ad9613f900cd2737d0a0f26aa9aa9b7d0) {#classshogun_1_1CRandomFourierGaussPreproc_1ad9613f900cd2737d0a0f26aa9aa9b7d0}

dimension of input features width of gaussian kernel in the form of exp(-x^2 / (2.0 kernelwidth^2) ) NOTE the 2.0 and the power ^2 !

#### `protected int32_t `[`dim_input_space`](#classshogun_1_1CRandomFourierGaussPreproc_1ab33e340dd7205cf26e60fb10332489aa) {#classshogun_1_1CRandomFourierGaussPreproc_1ab33e340dd7205cf26e60fb10332489aa}

desired dimension of input features as set by void [set_dim_input_space(const int32_t dim)](#classshogun_1_1CRandomFourierGaussPreproc_1a2f92fc4c8b669cecfc981e4bf1a5a397)

#### `protected int32_t `[`cur_dim_input_space`](#classshogun_1_1CRandomFourierGaussPreproc_1ae4d9512f847895257a0a516bd734fe1b) {#classshogun_1_1CRandomFourierGaussPreproc_1ae4d9512f847895257a0a516bd734fe1b}

actual dimension of input features as set by bool [init_randomcoefficients()](#classshogun_1_1CRandomFourierGaussPreproc_1a996d95f8c661a43bc248c36bea0734e9) or void set_randomcoefficients

#### `protected int32_t `[`dim_feature_space`](#classshogun_1_1CRandomFourierGaussPreproc_1a16fa41bb143f5f4d0194845963b5f456) {#classshogun_1_1CRandomFourierGaussPreproc_1a16fa41bb143f5f4d0194845963b5f456}

desired dimension of output features as set by void [set_dim_feature_space(const int32_t dim)](#classshogun_1_1CRandomFourierGaussPreproc_1a28d0060ccf67782ad3ece5556effc8c8)

#### `protected int32_t `[`cur_dim_feature_space`](#classshogun_1_1CRandomFourierGaussPreproc_1a6b76e47958b755a6a7ed85c8e9a71094) {#classshogun_1_1CRandomFourierGaussPreproc_1a6b76e47958b755a6a7ed85c8e9a71094}

actual dimension of output features as set by bool [init_randomcoefficients()](#classshogun_1_1CRandomFourierGaussPreproc_1a996d95f8c661a43bc248c36bea0734e9) or void set_randomcoefficients

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`randomcoeff_additive`](#classshogun_1_1CRandomFourierGaussPreproc_1a1a960a02e372323dc1df10682865eb3d) {#classshogun_1_1CRandomFourierGaussPreproc_1a1a960a02e372323dc1df10682865eb3d}

random coefficient length = cur_dim_feature_space

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`randomcoeff_multiplicative`](#classshogun_1_1CRandomFourierGaussPreproc_1a9c835a7ee410a41bc0e0956dae07e5c8) {#classshogun_1_1CRandomFourierGaussPreproc_1a9c835a7ee410a41bc0e0956dae07e5c8}

random coefficient length = cur_dim_feature_space* cur_dim_input_space

#### `protected bool `[`m_fitted`](#classshogun_1_1CTransformer_1ac7a9f470db2627f8ba58a3880fb34b2e) {#classshogun_1_1CTransformer_1ac7a9f470db2627f8ba58a3880fb34b2e}

#### `protected virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`apply_to_matrix`](#classshogun_1_1CRandomFourierGaussPreproc_1a391ac3239ebff9c47529c19d5dd36d31)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > matrix)` {#classshogun_1_1CRandomFourierGaussPreproc_1a391ac3239ebff9c47529c19d5dd36d31}

default processing routine, inherited from base class 
#### Parameters
* `matrix` the features matrix to be processed 

#### Returns
the processed feature matrix from the [CDenseFeatures<float64_t>](#classshogun_1_1CDenseFeatures) class in case (2) (see description above) this routine requires only steps 2a) and 2b), the rest is determined automatically

#### `protected void `[`copy`](#classshogun_1_1CRandomFourierGaussPreproc_1a9ddf854bb0fb7dde02879f456a1d8f5a)`(const `[`CRandomFourierGaussPreproc`](#classshogun_1_1CRandomFourierGaussPreproc)` & feats)` {#classshogun_1_1CRandomFourierGaussPreproc_1a9ddf854bb0fb7dde02879f456a1d8f5a}

helper for copy constructor and assignment operator=

#### `protected bool `[`test_rfinited`](#classshogun_1_1CRandomFourierGaussPreproc_1a9ae40c30b8175350b26fcb272d638f55)`() const` {#classshogun_1_1CRandomFourierGaussPreproc_1a9ae40c30b8175350b26fcb272d638f55}

tests whether rf features have already been initialized

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

