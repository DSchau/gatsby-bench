---
classname: "shogun::CPlif"
type: "class"
parents:
   - CPlifBase
---

# class `shogun::CPlif` {#classshogun_1_1CPlif}

```
class shogun::CPlif
  : public CPlifBase
```

class Plif

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
`public  `[`CPlif`](#classshogun_1_1CPlif_1a111154c5451341fe5f7b49dc65357237)`(int32_t len)` | constructor
`public virtual  `[`~CPlif`](#classshogun_1_1CPlif_1ab7b2564ab7f4396157347d62928eb31d)`()` | 
`public void `[`init_penalty_struct_cache`](#classshogun_1_1CPlif_1a7a4a24d91ed72e4292844b6d639eaa56)`()` | init penalty struct cache
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`lookup_penalty_svm`](#classshogun_1_1CPlif_1a306b23d4ba2608c7b6c744fae9aac393)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` p_value,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * d_values) const` | lookup penalty SVM
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`lookup_penalty`](#classshogun_1_1CPlif_1ade2d01279721bfc8744cea1102c368ed)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` p_value,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * svm_values) const` | lookup penalty float64_t
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`lookup_penalty`](#classshogun_1_1CPlif_1a61ce4bffe8f62c84a1610d7927548b93)`(int32_t p_value,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * svm_values) const` | lookup penalty int32_t
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`lookup`](#classshogun_1_1CPlif_1a460380b8f3109de2d34dd91a0590663f)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` p_value)` | lookup
`public virtual void `[`penalty_clear_derivative`](#classshogun_1_1CPlif_1a6339cd87aa805bf746398f1577ab9ef3)`()` | penalty clear derivative
`public void `[`penalty_add_derivative_svm`](#classshogun_1_1CPlif_1a439c95e39d9d1381ebf926a131b500df)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` p_value,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * svm_values,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` factor)` | penalty add derivative SVM
`public virtual void `[`penalty_add_derivative`](#classshogun_1_1CPlif_1a6a6394f2119a36b0a5f3e11636cd21c4)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` p_value,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * svm_values,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` factor)` | penalty add derivative
`public inline const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`get_cum_derivative`](#classshogun_1_1CPlif_1a9a7adfdefbed7d8febad0b45b2b65c1c)`(int32_t & p_len) const` | get cum derivative
`public bool `[`set_transform_type`](#classshogun_1_1CPlif_1a495d36c47cfd586f3492da31dd20a9e4)`(const char * type_str)` | set transform type
`public inline const char * `[`get_transform_type`](#classshogun_1_1CPlif_1a39701956964c5f3ae7d8acf0dc35d4f4)`()` | get transform type
`public inline void `[`set_id`](#classshogun_1_1CPlif_1a24a4d3aac36caa48c0989116531b0a87)`(int32_t p_id)` | set ID
`public inline int32_t `[`get_id`](#classshogun_1_1CPlif_1a993bbe8205a2faa3235bcf33c36d6b01)`() const` | get ID
`public inline virtual int32_t `[`get_max_id`](#classshogun_1_1CPlif_1aa17d90d39964824eb7cde277a72f8ddb)`() const` | get maximum ID
`public inline void `[`set_use_svm`](#classshogun_1_1CPlif_1aa8702750de6ea24bf4230d87482a48da)`(int32_t p_use_svm)` | set use SVM
`public inline int32_t `[`get_use_svm`](#classshogun_1_1CPlif_1a4d6bc610091e24d24c929f8283d8004c)`() const` | get use SVM
`public inline virtual bool `[`uses_svm_values`](#classshogun_1_1CPlif_1a4b46fd3d936767813984a783083ac84e)`() const` | check if plif uses SVM values
`public inline void `[`set_use_cache`](#classshogun_1_1CPlif_1a21080ea05433c30295f75c60d25a47df)`(int32_t p_use_cache)` | set use cache
`public inline void `[`invalidate_cache`](#classshogun_1_1CPlif_1a6915a1793325a01b8048fb493f519c8b)`()` | invalidate the cache
`public inline int32_t `[`get_use_cache`](#classshogun_1_1CPlif_1a0a8d51bba6ec1e33d9bec063097c0187)`()` | get use cache
`public inline void `[`set_plif`](#classshogun_1_1CPlif_1a70451d8d1ea99fc15af039dc4fe28799)`(int32_t p_len,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * p_limits,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * p_penalties)` | set plif
`public inline void `[`set_plif_limits`](#classshogun_1_1CPlif_1a6520ad754bf0d22043b816d77b1f300a)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > p_limits)` | set plif_limits
`public inline void `[`set_plif_penalty`](#classshogun_1_1CPlif_1aad7c99dec0d7d1939bc02fc0ae10ec2b)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > p_penalties)` | set plif penalty
`public inline void `[`set_plif_length`](#classshogun_1_1CPlif_1a0d11cadb3b6e76bd0322090634bc75da)`(int32_t p_len)` | set plif length
`public inline `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_plif_limits`](#classshogun_1_1CPlif_1aeca8aac45e024e84db8f397b82198f5b)`()` | get Plif limits
`public inline `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_plif_penalties`](#classshogun_1_1CPlif_1adf1eec3ff8a58deeb3168d21a82d215b)`()` | get plif penalty
`public inline void `[`set_max_value`](#classshogun_1_1CPlif_1acdab54f08d71542a27b95cd84127e6a5)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` p_max_value)` | set maximum value
`public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_max_value`](#classshogun_1_1CPlif_1a94f290fb96856966189618c433834fa6)`() const` | get maximum value
`public inline void `[`set_min_value`](#classshogun_1_1CPlif_1ad4aa7d309a497ea16c955c7ab61de1bf)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` p_min_value)` | set minimum value
`public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_min_value`](#classshogun_1_1CPlif_1a11243e8768ac4fdf8cad40b851c5ec7f)`() const` | get minimum value
`public void `[`set_plif_name`](#classshogun_1_1CPlif_1a34c87e63e02b78a8eaf021245241e1a8)`(char * p_name)` | set name
`public char * `[`get_plif_name`](#classshogun_1_1CPlif_1aeab85a2bca251da499fa3123edfd2958)`() const` | get name
`public bool `[`get_do_calc`](#classshogun_1_1CPlif_1aa83aed28b8989b4d255b7c48b6ad0875)`()` | get do calc
`public void `[`set_do_calc`](#classshogun_1_1CPlif_1ade472c30369c1900bdad533ee13eb053)`(bool b)` | set do calc
`public virtual void `[`get_used_svms`](#classshogun_1_1CPlif_1aa9c015e499978e7788d39b7fff12e6eb)`(int32_t * num_svms,int32_t * svm_ids)` | get SVM_ids and number of SVMs used
`public inline int32_t `[`get_plif_len`](#classshogun_1_1CPlif_1a71783f1175b0a5ee98d236fc9b5a4d2b)`()` | get plif len
`public inline virtual void `[`list_plif`](#classshogun_1_1CPlif_1a3713e7d73bb3759c564921ea0ddb4c14)`() const` | print PLIF
`public inline virtual const char * `[`get_name`](#classshogun_1_1CPlif_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` | #### Returns
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
`protected int32_t `[`len`](#classshogun_1_1CPlif_1a6858c4011b5cad020222e9ca5c2786f5) | len
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`limits`](#classshogun_1_1CPlif_1a3b00652a914a823d1233424c0aa3ea3d) | limits
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`penalties`](#classshogun_1_1CPlif_1a1e52439b36dd909df73ad4218b208118) | penalties
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`cum_derivatives`](#classshogun_1_1CPlif_1a4c852f6d040c19c6686c60880dcfe31d) | cum derivatives
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`max_value`](#classshogun_1_1CPlif_1a2dbc82cedc41e666349ac899468480d2) | maximum value
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`min_value`](#classshogun_1_1CPlif_1a0aef9658021fe2f19e16e91afac4bbef) | minimum value
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`cache`](#classshogun_1_1CPlif_1abc97a8b402305f839d19b248d38eb52c) | cache
`protected enum `[`ETransformType`](#namespaceshogun_1a79547fd1956b6478ed77ac0c56d2cde5)` `[`transform`](#classshogun_1_1CPlif_1abda16113a963bd18a69502cf42d0e91e) | transform type
`protected int32_t `[`id`](#classshogun_1_1CPlif_1a2708c0bbb6f926149707c2c61fe43c3e) | id
`protected char * `[`name`](#classshogun_1_1CPlif_1a5ac083a645d964373f022d03df4849c8) | name
`protected int32_t `[`use_svm`](#classshogun_1_1CPlif_1ab08342d20262ceb4069c3d7e4551ec4c) | if SVM shall be used
`protected bool `[`use_cache`](#classshogun_1_1CPlif_1ae7232526e932edeec381ff9ec2eae547) | if cache shall be used
`protected bool `[`do_calc`](#classshogun_1_1CPlif_1a0c2b7d49351f84b315777ba2fb920554) | do calc if this is true: lookup_penalty behaves normal else: lookup_penalty returns the p_value untransformed
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

#### `public  `[`CPlif`](#classshogun_1_1CPlif_1a111154c5451341fe5f7b49dc65357237)`(int32_t len)` {#classshogun_1_1CPlif_1a111154c5451341fe5f7b49dc65357237}

constructor

#### Parameters
* `len` len

#### `public virtual  `[`~CPlif`](#classshogun_1_1CPlif_1ab7b2564ab7f4396157347d62928eb31d)`()` {#classshogun_1_1CPlif_1ab7b2564ab7f4396157347d62928eb31d}

#### `public void `[`init_penalty_struct_cache`](#classshogun_1_1CPlif_1a7a4a24d91ed72e4292844b6d639eaa56)`()` {#classshogun_1_1CPlif_1a7a4a24d91ed72e4292844b6d639eaa56}

init penalty struct cache

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`lookup_penalty_svm`](#classshogun_1_1CPlif_1a306b23d4ba2608c7b6c744fae9aac393)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` p_value,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * d_values) const` {#classshogun_1_1CPlif_1a306b23d4ba2608c7b6c744fae9aac393}

lookup penalty SVM

#### Parameters
* `p_value` value 

* `d_values` d values 

#### Returns
the penalty

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`lookup_penalty`](#classshogun_1_1CPlif_1ade2d01279721bfc8744cea1102c368ed)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` p_value,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * svm_values) const` {#classshogun_1_1CPlif_1ade2d01279721bfc8744cea1102c368ed}

lookup penalty float64_t

#### Parameters
* `p_value` value 

* `svm_values` SVM values 

#### Returns
the penalty

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`lookup_penalty`](#classshogun_1_1CPlif_1a61ce4bffe8f62c84a1610d7927548b93)`(int32_t p_value,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * svm_values) const` {#classshogun_1_1CPlif_1a61ce4bffe8f62c84a1610d7927548b93}

lookup penalty int32_t

#### Parameters
* `p_value` value 

* `svm_values` SVM values 

#### Returns
the penalty

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`lookup`](#classshogun_1_1CPlif_1a460380b8f3109de2d34dd91a0590663f)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` p_value)` {#classshogun_1_1CPlif_1a460380b8f3109de2d34dd91a0590663f}

lookup

#### Parameters
* `p_value` value 

#### Returns
a penalty

#### `public virtual void `[`penalty_clear_derivative`](#classshogun_1_1CPlif_1a6339cd87aa805bf746398f1577ab9ef3)`()` {#classshogun_1_1CPlif_1a6339cd87aa805bf746398f1577ab9ef3}

penalty clear derivative

#### `public void `[`penalty_add_derivative_svm`](#classshogun_1_1CPlif_1a439c95e39d9d1381ebf926a131b500df)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` p_value,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * svm_values,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` factor)` {#classshogun_1_1CPlif_1a439c95e39d9d1381ebf926a131b500df}

penalty add derivative SVM

#### Parameters
* `p_value` value 

* `svm_values` SVM values 

* `factor` factor weighting the added value

#### `public virtual void `[`penalty_add_derivative`](#classshogun_1_1CPlif_1a6a6394f2119a36b0a5f3e11636cd21c4)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` p_value,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * svm_values,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` factor)` {#classshogun_1_1CPlif_1a6a6394f2119a36b0a5f3e11636cd21c4}

penalty add derivative

#### Parameters
* `p_value` value 

* `svm_values` SVM values 

* `factor` factor weighting the added value

#### `public inline const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`get_cum_derivative`](#classshogun_1_1CPlif_1a9a7adfdefbed7d8febad0b45b2b65c1c)`(int32_t & p_len) const` {#classshogun_1_1CPlif_1a9a7adfdefbed7d8febad0b45b2b65c1c}

get cum derivative

#### Parameters
* `p_len` len 

#### Returns
cum derivative

#### `public bool `[`set_transform_type`](#classshogun_1_1CPlif_1a495d36c47cfd586f3492da31dd20a9e4)`(const char * type_str)` {#classshogun_1_1CPlif_1a495d36c47cfd586f3492da31dd20a9e4}

set transform type

#### Parameters
* `type_str` type (string) 

#### Returns
if setting was successful

#### `public inline const char * `[`get_transform_type`](#classshogun_1_1CPlif_1a39701956964c5f3ae7d8acf0dc35d4f4)`()` {#classshogun_1_1CPlif_1a39701956964c5f3ae7d8acf0dc35d4f4}

get transform type

#### Returns
type_str type (string)

#### `public inline void `[`set_id`](#classshogun_1_1CPlif_1a24a4d3aac36caa48c0989116531b0a87)`(int32_t p_id)` {#classshogun_1_1CPlif_1a24a4d3aac36caa48c0989116531b0a87}

set ID

#### Parameters
* `p_id` the id to set

#### `public inline int32_t `[`get_id`](#classshogun_1_1CPlif_1a993bbe8205a2faa3235bcf33c36d6b01)`() const` {#classshogun_1_1CPlif_1a993bbe8205a2faa3235bcf33c36d6b01}

get ID

#### Returns
the ID

#### `public inline virtual int32_t `[`get_max_id`](#classshogun_1_1CPlif_1aa17d90d39964824eb7cde277a72f8ddb)`() const` {#classshogun_1_1CPlif_1aa17d90d39964824eb7cde277a72f8ddb}

get maximum ID

#### Returns
maximum ID

#### `public inline void `[`set_use_svm`](#classshogun_1_1CPlif_1aa8702750de6ea24bf4230d87482a48da)`(int32_t p_use_svm)` {#classshogun_1_1CPlif_1aa8702750de6ea24bf4230d87482a48da}

set use SVM

#### Parameters
* `p_use_svm` if SVM shall be used

#### `public inline int32_t `[`get_use_svm`](#classshogun_1_1CPlif_1a4d6bc610091e24d24c929f8283d8004c)`() const` {#classshogun_1_1CPlif_1a4d6bc610091e24d24c929f8283d8004c}

get use SVM

#### Returns
if SVM is used

#### `public inline virtual bool `[`uses_svm_values`](#classshogun_1_1CPlif_1a4b46fd3d936767813984a783083ac84e)`() const` {#classshogun_1_1CPlif_1a4b46fd3d936767813984a783083ac84e}

check if plif uses SVM values

#### Returns
if plif uses SVM values

#### `public inline void `[`set_use_cache`](#classshogun_1_1CPlif_1a21080ea05433c30295f75c60d25a47df)`(int32_t p_use_cache)` {#classshogun_1_1CPlif_1a21080ea05433c30295f75c60d25a47df}

set use cache

#### Parameters
* `p_use_cache` if cache shall be used

#### `public inline void `[`invalidate_cache`](#classshogun_1_1CPlif_1a6915a1793325a01b8048fb493f519c8b)`()` {#classshogun_1_1CPlif_1a6915a1793325a01b8048fb493f519c8b}

invalidate the cache

#### `public inline int32_t `[`get_use_cache`](#classshogun_1_1CPlif_1a0a8d51bba6ec1e33d9bec063097c0187)`()` {#classshogun_1_1CPlif_1a0a8d51bba6ec1e33d9bec063097c0187}

get use cache

#### Returns
if cache is used

#### `public inline void `[`set_plif`](#classshogun_1_1CPlif_1a70451d8d1ea99fc15af039dc4fe28799)`(int32_t p_len,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * p_limits,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * p_penalties)` {#classshogun_1_1CPlif_1a70451d8d1ea99fc15af039dc4fe28799}

set plif

#### Parameters
* `p_len` len 

* `p_limits` limit 

* `p_penalties` penalties

#### `public inline void `[`set_plif_limits`](#classshogun_1_1CPlif_1a6520ad754bf0d22043b816d77b1f300a)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > p_limits)` {#classshogun_1_1CPlif_1a6520ad754bf0d22043b816d77b1f300a}

set plif_limits

#### Parameters
* `p_limits` limit

#### `public inline void `[`set_plif_penalty`](#classshogun_1_1CPlif_1aad7c99dec0d7d1939bc02fc0ae10ec2b)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > p_penalties)` {#classshogun_1_1CPlif_1aad7c99dec0d7d1939bc02fc0ae10ec2b}

set plif penalty

#### Parameters
* `p_penalties` penalties

#### `public inline void `[`set_plif_length`](#classshogun_1_1CPlif_1a0d11cadb3b6e76bd0322090634bc75da)`(int32_t p_len)` {#classshogun_1_1CPlif_1a0d11cadb3b6e76bd0322090634bc75da}

set plif length

#### Parameters
* `p_len` len

#### `public inline `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_plif_limits`](#classshogun_1_1CPlif_1aeca8aac45e024e84db8f397b82198f5b)`()` {#classshogun_1_1CPlif_1aeca8aac45e024e84db8f397b82198f5b}

get Plif limits

#### Returns
limits

#### `public inline `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_plif_penalties`](#classshogun_1_1CPlif_1adf1eec3ff8a58deeb3168d21a82d215b)`()` {#classshogun_1_1CPlif_1adf1eec3ff8a58deeb3168d21a82d215b}

get plif penalty

#### Returns
plif penalty

#### `public inline void `[`set_max_value`](#classshogun_1_1CPlif_1acdab54f08d71542a27b95cd84127e6a5)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` p_max_value)` {#classshogun_1_1CPlif_1acdab54f08d71542a27b95cd84127e6a5}

set maximum value

#### Parameters
* `p_max_value` maximum value

#### `public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_max_value`](#classshogun_1_1CPlif_1a94f290fb96856966189618c433834fa6)`() const` {#classshogun_1_1CPlif_1a94f290fb96856966189618c433834fa6}

get maximum value

#### Returns
maximum value

#### `public inline void `[`set_min_value`](#classshogun_1_1CPlif_1ad4aa7d309a497ea16c955c7ab61de1bf)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` p_min_value)` {#classshogun_1_1CPlif_1ad4aa7d309a497ea16c955c7ab61de1bf}

set minimum value

#### Parameters
* `p_min_value` minimum value

#### `public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_min_value`](#classshogun_1_1CPlif_1a11243e8768ac4fdf8cad40b851c5ec7f)`() const` {#classshogun_1_1CPlif_1a11243e8768ac4fdf8cad40b851c5ec7f}

get minimum value

#### Returns
minimum value

#### `public void `[`set_plif_name`](#classshogun_1_1CPlif_1a34c87e63e02b78a8eaf021245241e1a8)`(char * p_name)` {#classshogun_1_1CPlif_1a34c87e63e02b78a8eaf021245241e1a8}

set name

#### Parameters
* `p_name` name

#### `public char * `[`get_plif_name`](#classshogun_1_1CPlif_1aeab85a2bca251da499fa3123edfd2958)`() const` {#classshogun_1_1CPlif_1aeab85a2bca251da499fa3123edfd2958}

get name

#### Returns
name

#### `public bool `[`get_do_calc`](#classshogun_1_1CPlif_1aa83aed28b8989b4d255b7c48b6ad0875)`()` {#classshogun_1_1CPlif_1aa83aed28b8989b4d255b7c48b6ad0875}

get do calc

#### Returns
if calc shall be done

#### `public void `[`set_do_calc`](#classshogun_1_1CPlif_1ade472c30369c1900bdad533ee13eb053)`(bool b)` {#classshogun_1_1CPlif_1ade472c30369c1900bdad533ee13eb053}

set do calc

#### Parameters
* `b` if calc shall be done

#### `public virtual void `[`get_used_svms`](#classshogun_1_1CPlif_1aa9c015e499978e7788d39b7fff12e6eb)`(int32_t * num_svms,int32_t * svm_ids)` {#classshogun_1_1CPlif_1aa9c015e499978e7788d39b7fff12e6eb}

get SVM_ids and number of SVMs used

#### `public inline int32_t `[`get_plif_len`](#classshogun_1_1CPlif_1a71783f1175b0a5ee98d236fc9b5a4d2b)`()` {#classshogun_1_1CPlif_1a71783f1175b0a5ee98d236fc9b5a4d2b}

get plif len

#### Returns
plif len

#### `public inline virtual void `[`list_plif`](#classshogun_1_1CPlif_1a3713e7d73bb3759c564921ea0ddb4c14)`() const` {#classshogun_1_1CPlif_1a3713e7d73bb3759c564921ea0ddb4c14}

print PLIF

lists some properties of the PLIF

#### `public inline virtual const char * `[`get_name`](#classshogun_1_1CPlif_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` {#classshogun_1_1CPlif_1a9cb485686dd7a1e6f7103cf42e87717e}

#### Returns
object name

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

#### `protected int32_t `[`len`](#classshogun_1_1CPlif_1a6858c4011b5cad020222e9ca5c2786f5) {#classshogun_1_1CPlif_1a6858c4011b5cad020222e9ca5c2786f5}

len

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`limits`](#classshogun_1_1CPlif_1a3b00652a914a823d1233424c0aa3ea3d) {#classshogun_1_1CPlif_1a3b00652a914a823d1233424c0aa3ea3d}

limits

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`penalties`](#classshogun_1_1CPlif_1a1e52439b36dd909df73ad4218b208118) {#classshogun_1_1CPlif_1a1e52439b36dd909df73ad4218b208118}

penalties

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`cum_derivatives`](#classshogun_1_1CPlif_1a4c852f6d040c19c6686c60880dcfe31d) {#classshogun_1_1CPlif_1a4c852f6d040c19c6686c60880dcfe31d}

cum derivatives

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`max_value`](#classshogun_1_1CPlif_1a2dbc82cedc41e666349ac899468480d2) {#classshogun_1_1CPlif_1a2dbc82cedc41e666349ac899468480d2}

maximum value

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`min_value`](#classshogun_1_1CPlif_1a0aef9658021fe2f19e16e91afac4bbef) {#classshogun_1_1CPlif_1a0aef9658021fe2f19e16e91afac4bbef}

minimum value

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`cache`](#classshogun_1_1CPlif_1abc97a8b402305f839d19b248d38eb52c) {#classshogun_1_1CPlif_1abc97a8b402305f839d19b248d38eb52c}

cache

#### `protected enum `[`ETransformType`](#namespaceshogun_1a79547fd1956b6478ed77ac0c56d2cde5)` `[`transform`](#classshogun_1_1CPlif_1abda16113a963bd18a69502cf42d0e91e) {#classshogun_1_1CPlif_1abda16113a963bd18a69502cf42d0e91e}

transform type

#### `protected int32_t `[`id`](#classshogun_1_1CPlif_1a2708c0bbb6f926149707c2c61fe43c3e) {#classshogun_1_1CPlif_1a2708c0bbb6f926149707c2c61fe43c3e}

id

#### `protected char * `[`name`](#classshogun_1_1CPlif_1a5ac083a645d964373f022d03df4849c8) {#classshogun_1_1CPlif_1a5ac083a645d964373f022d03df4849c8}

name

#### `protected int32_t `[`use_svm`](#classshogun_1_1CPlif_1ab08342d20262ceb4069c3d7e4551ec4c) {#classshogun_1_1CPlif_1ab08342d20262ceb4069c3d7e4551ec4c}

if SVM shall be used

#### `protected bool `[`use_cache`](#classshogun_1_1CPlif_1ae7232526e932edeec381ff9ec2eae547) {#classshogun_1_1CPlif_1ae7232526e932edeec381ff9ec2eae547}

if cache shall be used

#### `protected bool `[`do_calc`](#classshogun_1_1CPlif_1a0c2b7d49351f84b315777ba2fb920554) {#classshogun_1_1CPlif_1a0c2b7d49351f84b315777ba2fb920554}

do calc if this is true: lookup_penalty behaves normal else: lookup_penalty returns the p_value untransformed

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

