---
classname: "shogun::CDynamicObjectArray"
type: "class"
parents:
   - CSGObject
---

# class `shogun::CDynamicObjectArray` {#classshogun_1_1CDynamicObjectArray}

```
class shogun::CDynamicObjectArray
  : public CSGObject
```

Dynamic array class for [CSGObject](#classshogun_1_1CSGObject) pointers that creates an array that can be used like a list or an array.

It grows and shrinks dynamically, while elements can be accessed via index. It only stores [CSGObject](#classshogun_1_1CSGObject) pointers, which ARE automagically SG_REF'd/deleted.

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
`public inline  `[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray_1a141bc45c618880ae6d14c7a0dbb4d8ff)`()` | default constructor
`public inline  `[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray_1ac2680fa9ec6131260806790e72ac840f)`(int32_t dim1,int32_t dim2,int32_t dim3)` | constructor
`public inline  `[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray_1a1b844225c4ad1f3b2b7d2f3d7cb314b2)`(`[`CSGObject`](#classshogun_1_1CSGObject)` ** p_array,int32_t p_dim1_size,bool p_free_array,bool p_copy_array)` | constructor
`public inline  `[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray_1a33544618f3426c0468769da0630c0497)`(`[`CSGObject`](#classshogun_1_1CSGObject)` ** p_array,int32_t p_dim1_size,int32_t p_dim2_size,bool p_free_array,bool p_copy_array)` | constructor
`public inline  `[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray_1a545349703c4d493a5f1d34854bd2226c)`(`[`CSGObject`](#classshogun_1_1CSGObject)` ** p_array,int32_t p_dim1_size,int32_t p_dim2_size,int32_t p_dim3_size,bool p_free_array,bool p_copy_array)` | constructor
`public inline virtual  `[`~CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray_1a1946fdd768eaf9a022dea4382793b288)`()` | 
`public inline int32_t `[`set_granularity`](#classshogun_1_1CDynamicObjectArray_1a2850663a352f44e69a6896fcd7f6bb76)`(int32_t g)` | set the resize granularity
`public inline int32_t `[`get_array_size`](#classshogun_1_1CDynamicObjectArray_1afcebc78497e0a544114757059bff49fc)`()` | get array size (including granularity buffer)
`public inline void `[`get_array_size`](#classshogun_1_1CDynamicObjectArray_1a604c1cd3419ef013b9b2e77e49a00c28)`(int32_t & dim1,int32_t & dim2)` | return 2d array size
`public inline void `[`get_array_size`](#classshogun_1_1CDynamicObjectArray_1a8a605733cebc9b05bb9f8e7612a1b95f)`(int32_t & dim1,int32_t & dim2,int32_t & dim3)` | return 3d array size
`public inline int32_t `[`get_dim1`](#classshogun_1_1CDynamicObjectArray_1aeb484e13b72a09e1a9b6af5f7c68c3d2)`()` | get dimension 1
`public inline int32_t `[`get_dim2`](#classshogun_1_1CDynamicObjectArray_1a5fea23d554404903a9306936be6a9533)`()` | get dimension 2
`public inline int32_t `[`get_dim3`](#classshogun_1_1CDynamicObjectArray_1a59054b15793946a39e04ffe8dd706b6b)`()` | get dimension 3
`public inline int32_t `[`get_num_elements`](#classshogun_1_1CDynamicObjectArray_1aa1a8c34958f199dc0209b1ef9c23b72d)`() const` | get number of elements
`public inline `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`get_element`](#classshogun_1_1CDynamicObjectArray_1ad11f39a01ca0fc4978e393839cef31a6)`(int32_t index) const` | get array element at index
`public inline `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`element`](#classshogun_1_1CDynamicObjectArray_1a7331c5993854bdd5bf2f6a88108ff31a)`(int32_t idx1,int32_t idx2,int32_t idx3)` | get array element at index
`public inline `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`get_last_element`](#classshogun_1_1CDynamicObjectArray_1aca6baf82295e0056a3ac4a802e1523a9)`() const` | get last array element
`public inline `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`get_element_safe`](#classshogun_1_1CDynamicObjectArray_1a7c97ac5460188d2ac95826115a2dd30b)`(int32_t index) const` | get array element at index
`public inline bool `[`set_element`](#classshogun_1_1CDynamicObjectArray_1a0658ce6252d910f9dd8c1fc1a4c2359b)`(`[`CSGObject`](#classshogun_1_1CSGObject)` * e,int32_t idx1,int32_t idx2,int32_t idx3)` | set array element at index
`public inline bool `[`insert_element`](#classshogun_1_1CDynamicObjectArray_1a64389a1ed8a175e365cffc37a01f1f79)`(`[`CSGObject`](#classshogun_1_1CSGObject)` * e,int32_t index)` | insert array element at index
`public template<>`  <br/>`inline bool `[`append_element`](#classshogun_1_1CDynamicObjectArray_1aed461494c4f4be43f61f0f99edbcdffd)`(T e,const char * name)` | 
`public template<>`  <br/>`inline bool `[`append_element`](#classshogun_1_1CDynamicObjectArray_1ac94548cc7bf68592f16b53d368511a76)`(`[`SGVector`](#classshogun_1_1SGVector)`< T > e,const char * name)` | 
`public template<>`  <br/>`inline bool `[`append_element`](#classshogun_1_1CDynamicObjectArray_1a4fa2b7652d0a0815eb515f49b6bbbef8)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > e,const char * name)` | 
`public inline bool `[`append_element`](#classshogun_1_1CDynamicObjectArray_1aefecc30d8acf5bfa544e7e6488834163)`(`[`CSGObject`](#classshogun_1_1CSGObject)` * e)` | append array element to the end of array
`public inline void `[`push_back`](#classshogun_1_1CDynamicObjectArray_1ac4f5cf1b7c29fec78cde64cd7dc7e9fc)`(`[`CSGObject`](#classshogun_1_1CSGObject)` * e)` | STD VECTOR compatible. Append array element to the end of array.
`public inline void `[`pop_back`](#classshogun_1_1CDynamicObjectArray_1a058bda4957df6a97b1ea6c9fd783f672)`()` | STD VECTOR compatible. Delete array element at the end of array.
`public inline `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`back`](#classshogun_1_1CDynamicObjectArray_1a47f7afb3c6f5773fdf357bffa3f9a66e)`() const` | STD VECTOR compatible. Return array element at the end of array.
`public inline int32_t `[`find_element`](#classshogun_1_1CDynamicObjectArray_1a19788a6e170fe749cb030911f99008ae)`(`[`CSGObject`](#classshogun_1_1CSGObject)` * elem) const` | find first occurence of array element and return its index or -1 if not available
`public inline bool `[`delete_element`](#classshogun_1_1CDynamicObjectArray_1af1e028b3c9d27ca9cbf78ebec9e79b93)`(int32_t idx)` | delete array element at idx (does not call SG_FREE() or the like)
`public inline void `[`clear_array`](#classshogun_1_1CDynamicObjectArray_1a2aace7f126c9c0fca0c740c443fb2cbc)`()` | clear the array (with zeros)
`public inline void `[`reset_array`](#classshogun_1_1CDynamicObjectArray_1a6bf8adb1a6ff9266cc2c4ead0a6d4496)`()` | resets the array
`public inline `[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` & `[`operator=`](#classshogun_1_1CDynamicObjectArray_1adbb8548314f4f556216e48e225b80f05)`(`[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` & orig)` | operator overload for array assignment
`public inline `[`CSGObject`](#classshogun_1_1CSGObject)` ** `[`get_array`](#classshogun_1_1CDynamicObjectArray_1ab70d39ddc3a5aa4ac9142c28f1b72cd3)`() const` | #### Returns
`public inline void `[`shuffle`](#classshogun_1_1CDynamicObjectArray_1a1905fe84eb39f020b32c58baf7a76758)`()` | shuffles the array (not thread safe!)
`public inline void `[`shuffle`](#classshogun_1_1CDynamicObjectArray_1aab5aeea2dba53b2995b58f400be7db1a)`(`[`CRandom`](#classshogun_1_1CRandom)` * rand)` | shuffles the array with external random state
`public inline virtual const char * `[`get_name`](#classshogun_1_1CDynamicObjectArray_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` | #### Returns
`public inline virtual void `[`load_serializable_pre`](#classshogun_1_1CDynamicObjectArray_1aad7268c7592cbb6613b444a8ed6a827d)`()` | Can (optionally) be overridden to pre-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::LOAD_SERIALIZABLE_PRE is called.
`public inline virtual void `[`save_serializable_pre`](#classshogun_1_1CDynamicObjectArray_1ae588cf420dfbd31ec90b95972e4d5dc9)`()` | Can (optionally) be overridden to pre-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::SAVE_SERIALIZABLE_PRE is called.
`public inline virtual `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`clone`](#classshogun_1_1CDynamicObjectArray_1a290165350894020201ade71ee7951da4)`()` | Creates a clone of the current object. This is done via recursively traversing all parameters, which corresponds to a deep copy. Calling equals on the cloned object always returns true although none of the memory of both objects overlaps.
`public bool `[`save_serializable`](#classshogun_1_1CDynamicObjectArray_1aa9787e341533c4970885ce6d3022a935)`()` | Save this object to file.
`public bool `[`load_serializable`](#classshogun_1_1CDynamicObjectArray_1ad67e38ad80d4152151081f838c0a13e1)`()` | Load this object from file. If it will fail (returning FALSE) then this object will contain inconsistent data and should not be used!
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
`protected template<>`  <br/>`inline `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`get_sgobject_type_dispatcher`](#classshogun_1_1CSGObject_1a7de7c1e11c3d4322d74a9a8cf5cc13f1)`(const std::string & name)` | 
`protected virtual void `[`load_serializable_post`](#classshogun_1_1CSGObject_1a4c8da771d1ddf319cabc6b9e896326f2)`()` | Can (optionally) be overridden to post-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::LOAD_SERIALIZABLE_POST is called.
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

#### `public inline  `[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray_1a141bc45c618880ae6d14c7a0dbb4d8ff)`()` {#classshogun_1_1CDynamicObjectArray_1a141bc45c618880ae6d14c7a0dbb4d8ff}

default constructor

#### `public inline  `[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray_1ac2680fa9ec6131260806790e72ac840f)`(int32_t dim1,int32_t dim2,int32_t dim3)` {#classshogun_1_1CDynamicObjectArray_1ac2680fa9ec6131260806790e72ac840f}

constructor

#### Parameters
* `dim1` dimension 1 

* `dim2` dimension 2 

* `dim3` dimension 3

#### `public inline  `[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray_1a1b844225c4ad1f3b2b7d2f3d7cb314b2)`(`[`CSGObject`](#classshogun_1_1CSGObject)` ** p_array,int32_t p_dim1_size,bool p_free_array,bool p_copy_array)` {#classshogun_1_1CDynamicObjectArray_1a1b844225c4ad1f3b2b7d2f3d7cb314b2}

constructor

#### Parameters
* `p_array` another array 

* `p_dim1_size` dimension 1 

* `p_free_array` if array must be freed 

* `p_copy_array` if array must be copied

#### `public inline  `[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray_1a33544618f3426c0468769da0630c0497)`(`[`CSGObject`](#classshogun_1_1CSGObject)` ** p_array,int32_t p_dim1_size,int32_t p_dim2_size,bool p_free_array,bool p_copy_array)` {#classshogun_1_1CDynamicObjectArray_1a33544618f3426c0468769da0630c0497}

constructor

#### Parameters
* `p_array` another array 

* `p_dim1_size` dimension 1 

* `p_dim2_size` dimension 2 

* `p_free_array` if array must be freed 

* `p_copy_array` if array must be copied

#### `public inline  `[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray_1a545349703c4d493a5f1d34854bd2226c)`(`[`CSGObject`](#classshogun_1_1CSGObject)` ** p_array,int32_t p_dim1_size,int32_t p_dim2_size,int32_t p_dim3_size,bool p_free_array,bool p_copy_array)` {#classshogun_1_1CDynamicObjectArray_1a545349703c4d493a5f1d34854bd2226c}

constructor

#### Parameters
* `p_array` another array 

* `p_dim1_size` dimension 1 

* `p_dim2_size` dimension 2 

* `p_dim3_size` dimension 3 

* `p_free_array` if array must be freed 

* `p_copy_array` if array must be copied

#### `public inline virtual  `[`~CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray_1a1946fdd768eaf9a022dea4382793b288)`()` {#classshogun_1_1CDynamicObjectArray_1a1946fdd768eaf9a022dea4382793b288}

#### `public inline int32_t `[`set_granularity`](#classshogun_1_1CDynamicObjectArray_1a2850663a352f44e69a6896fcd7f6bb76)`(int32_t g)` {#classshogun_1_1CDynamicObjectArray_1a2850663a352f44e69a6896fcd7f6bb76}

set the resize granularity

#### Parameters
* `g` new granularity 

#### Returns
what has been set (minimum is 128)

#### `public inline int32_t `[`get_array_size`](#classshogun_1_1CDynamicObjectArray_1afcebc78497e0a544114757059bff49fc)`()` {#classshogun_1_1CDynamicObjectArray_1afcebc78497e0a544114757059bff49fc}

get array size (including granularity buffer)

#### Returns
total array size (including granularity buffer)

#### `public inline void `[`get_array_size`](#classshogun_1_1CDynamicObjectArray_1a604c1cd3419ef013b9b2e77e49a00c28)`(int32_t & dim1,int32_t & dim2)` {#classshogun_1_1CDynamicObjectArray_1a604c1cd3419ef013b9b2e77e49a00c28}

return 2d array size

#### Parameters
* `dim1` dimension 1 will be stored here 

* `dim2` dimension 2 will be stored here

#### `public inline void `[`get_array_size`](#classshogun_1_1CDynamicObjectArray_1a8a605733cebc9b05bb9f8e7612a1b95f)`(int32_t & dim1,int32_t & dim2,int32_t & dim3)` {#classshogun_1_1CDynamicObjectArray_1a8a605733cebc9b05bb9f8e7612a1b95f}

return 3d array size

#### Parameters
* `dim1` dimension 1 will be stored here 

* `dim2` dimension 2 will be stored here 

* `dim3` dimension 3 will be stored here

#### `public inline int32_t `[`get_dim1`](#classshogun_1_1CDynamicObjectArray_1aeb484e13b72a09e1a9b6af5f7c68c3d2)`()` {#classshogun_1_1CDynamicObjectArray_1aeb484e13b72a09e1a9b6af5f7c68c3d2}

get dimension 1

#### Returns
dimension 1

#### `public inline int32_t `[`get_dim2`](#classshogun_1_1CDynamicObjectArray_1a5fea23d554404903a9306936be6a9533)`()` {#classshogun_1_1CDynamicObjectArray_1a5fea23d554404903a9306936be6a9533}

get dimension 2

#### Returns
dimension 2

#### `public inline int32_t `[`get_dim3`](#classshogun_1_1CDynamicObjectArray_1a59054b15793946a39e04ffe8dd706b6b)`()` {#classshogun_1_1CDynamicObjectArray_1a59054b15793946a39e04ffe8dd706b6b}

get dimension 3

#### Returns
dimension 3

#### `public inline int32_t `[`get_num_elements`](#classshogun_1_1CDynamicObjectArray_1aa1a8c34958f199dc0209b1ef9c23b72d)`() const` {#classshogun_1_1CDynamicObjectArray_1aa1a8c34958f199dc0209b1ef9c23b72d}

get number of elements

#### Returns
number of elements

#### `public inline `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`get_element`](#classshogun_1_1CDynamicObjectArray_1ad11f39a01ca0fc4978e393839cef31a6)`(int32_t index) const` {#classshogun_1_1CDynamicObjectArray_1ad11f39a01ca0fc4978e393839cef31a6}

get array element at index

(does NOT do bounds checking)

#### Parameters
* `index` index 

#### Returns
array element at index

#### `public inline `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`element`](#classshogun_1_1CDynamicObjectArray_1a7331c5993854bdd5bf2f6a88108ff31a)`(int32_t idx1,int32_t idx2,int32_t idx3)` {#classshogun_1_1CDynamicObjectArray_1a7331c5993854bdd5bf2f6a88108ff31a}

get array element at index

#### Parameters
* `idx1` index 1 

* `idx2` index 2 

* `idx3` index 3 

#### Returns
array element at index

#### `public inline `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`get_last_element`](#classshogun_1_1CDynamicObjectArray_1aca6baf82295e0056a3ac4a802e1523a9)`() const` {#classshogun_1_1CDynamicObjectArray_1aca6baf82295e0056a3ac4a802e1523a9}

get last array element

#### Returns
last array element

#### `public inline `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`get_element_safe`](#classshogun_1_1CDynamicObjectArray_1a7c97ac5460188d2ac95826115a2dd30b)`(int32_t index) const` {#classshogun_1_1CDynamicObjectArray_1a7c97ac5460188d2ac95826115a2dd30b}

get array element at index

(does bounds checking)

#### Parameters
* `index` index 

#### Returns
array element at index

#### `public inline bool `[`set_element`](#classshogun_1_1CDynamicObjectArray_1a0658ce6252d910f9dd8c1fc1a4c2359b)`(`[`CSGObject`](#classshogun_1_1CSGObject)` * e,int32_t idx1,int32_t idx2,int32_t idx3)` {#classshogun_1_1CDynamicObjectArray_1a0658ce6252d910f9dd8c1fc1a4c2359b}

set array element at index

#### Parameters
* `e` element to set 

* `idx1` index 1 

* `idx2` index 2 

* `idx3` index 2 

#### Returns
if setting was successful

#### `public inline bool `[`insert_element`](#classshogun_1_1CDynamicObjectArray_1a64389a1ed8a175e365cffc37a01f1f79)`(`[`CSGObject`](#classshogun_1_1CSGObject)` * e,int32_t index)` {#classshogun_1_1CDynamicObjectArray_1a64389a1ed8a175e365cffc37a01f1f79}

insert array element at index

#### Parameters
* `e` element to insert 

* `index` index 

#### Returns
if setting was successful

#### `public template<>`  <br/>`inline bool `[`append_element`](#classshogun_1_1CDynamicObjectArray_1aed461494c4f4be43f61f0f99edbcdffd)`(T e,const char * name)` {#classshogun_1_1CDynamicObjectArray_1aed461494c4f4be43f61f0f99edbcdffd}

#### `public template<>`  <br/>`inline bool `[`append_element`](#classshogun_1_1CDynamicObjectArray_1ac94548cc7bf68592f16b53d368511a76)`(`[`SGVector`](#classshogun_1_1SGVector)`< T > e,const char * name)` {#classshogun_1_1CDynamicObjectArray_1ac94548cc7bf68592f16b53d368511a76}

#### `public template<>`  <br/>`inline bool `[`append_element`](#classshogun_1_1CDynamicObjectArray_1a4fa2b7652d0a0815eb515f49b6bbbef8)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > e,const char * name)` {#classshogun_1_1CDynamicObjectArray_1a4fa2b7652d0a0815eb515f49b6bbbef8}

#### `public inline bool `[`append_element`](#classshogun_1_1CDynamicObjectArray_1aefecc30d8acf5bfa544e7e6488834163)`(`[`CSGObject`](#classshogun_1_1CSGObject)` * e)` {#classshogun_1_1CDynamicObjectArray_1aefecc30d8acf5bfa544e7e6488834163}

append array element to the end of array

#### Parameters
* `e` element to append 

#### Returns
if setting was successful

#### `public inline void `[`push_back`](#classshogun_1_1CDynamicObjectArray_1ac4f5cf1b7c29fec78cde64cd7dc7e9fc)`(`[`CSGObject`](#classshogun_1_1CSGObject)` * e)` {#classshogun_1_1CDynamicObjectArray_1ac4f5cf1b7c29fec78cde64cd7dc7e9fc}

STD VECTOR compatible. Append array element to the end of array.

#### Parameters
* `e` element to append

#### `public inline void `[`pop_back`](#classshogun_1_1CDynamicObjectArray_1a058bda4957df6a97b1ea6c9fd783f672)`()` {#classshogun_1_1CDynamicObjectArray_1a058bda4957df6a97b1ea6c9fd783f672}

STD VECTOR compatible. Delete array element at the end of array.

#### `public inline `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`back`](#classshogun_1_1CDynamicObjectArray_1a47f7afb3c6f5773fdf357bffa3f9a66e)`() const` {#classshogun_1_1CDynamicObjectArray_1a47f7afb3c6f5773fdf357bffa3f9a66e}

STD VECTOR compatible. Return array element at the end of array.

#### Returns
element at the end of array

#### `public inline int32_t `[`find_element`](#classshogun_1_1CDynamicObjectArray_1a19788a6e170fe749cb030911f99008ae)`(`[`CSGObject`](#classshogun_1_1CSGObject)` * elem) const` {#classshogun_1_1CDynamicObjectArray_1a19788a6e170fe749cb030911f99008ae}

find first occurence of array element and return its index or -1 if not available

#### Parameters
* `elem` element to search for 

#### Returns
index of element or -1

#### `public inline bool `[`delete_element`](#classshogun_1_1CDynamicObjectArray_1af1e028b3c9d27ca9cbf78ebec9e79b93)`(int32_t idx)` {#classshogun_1_1CDynamicObjectArray_1af1e028b3c9d27ca9cbf78ebec9e79b93}

delete array element at idx (does not call SG_FREE() or the like)

#### Parameters
* `idx` index 

#### Returns
if deleting was successful

#### `public inline void `[`clear_array`](#classshogun_1_1CDynamicObjectArray_1a2aace7f126c9c0fca0c740c443fb2cbc)`()` {#classshogun_1_1CDynamicObjectArray_1a2aace7f126c9c0fca0c740c443fb2cbc}

clear the array (with zeros)

#### `public inline void `[`reset_array`](#classshogun_1_1CDynamicObjectArray_1a6bf8adb1a6ff9266cc2c4ead0a6d4496)`()` {#classshogun_1_1CDynamicObjectArray_1a6bf8adb1a6ff9266cc2c4ead0a6d4496}

resets the array

#### `public inline `[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` & `[`operator=`](#classshogun_1_1CDynamicObjectArray_1adbb8548314f4f556216e48e225b80f05)`(`[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` & orig)` {#classshogun_1_1CDynamicObjectArray_1adbb8548314f4f556216e48e225b80f05}

operator overload for array assignment

#### Parameters
* `orig` original array 

#### Returns
new array

#### `public inline `[`CSGObject`](#classshogun_1_1CSGObject)` ** `[`get_array`](#classshogun_1_1CDynamicObjectArray_1ab70d39ddc3a5aa4ac9142c28f1b72cd3)`() const` {#classshogun_1_1CDynamicObjectArray_1ab70d39ddc3a5aa4ac9142c28f1b72cd3}

#### Returns
underlying array of pointers

#### `public inline void `[`shuffle`](#classshogun_1_1CDynamicObjectArray_1a1905fe84eb39f020b32c58baf7a76758)`()` {#classshogun_1_1CDynamicObjectArray_1a1905fe84eb39f020b32c58baf7a76758}

shuffles the array (not thread safe!)

#### `public inline void `[`shuffle`](#classshogun_1_1CDynamicObjectArray_1aab5aeea2dba53b2995b58f400be7db1a)`(`[`CRandom`](#classshogun_1_1CRandom)` * rand)` {#classshogun_1_1CDynamicObjectArray_1aab5aeea2dba53b2995b58f400be7db1a}

shuffles the array with external random state

#### `public inline virtual const char * `[`get_name`](#classshogun_1_1CDynamicObjectArray_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` {#classshogun_1_1CDynamicObjectArray_1a9cb485686dd7a1e6f7103cf42e87717e}

#### Returns
object name

#### `public inline virtual void `[`load_serializable_pre`](#classshogun_1_1CDynamicObjectArray_1aad7268c7592cbb6613b444a8ed6a827d)`()` {#classshogun_1_1CDynamicObjectArray_1aad7268c7592cbb6613b444a8ed6a827d}

Can (optionally) be overridden to pre-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::LOAD_SERIALIZABLE_PRE is called.

#### Exceptions
* `[ShogunException](#classshogun_1_1ShogunException)` Will be thrown if an error occurres.

#### `public inline virtual void `[`save_serializable_pre`](#classshogun_1_1CDynamicObjectArray_1ae588cf420dfbd31ec90b95972e4d5dc9)`()` {#classshogun_1_1CDynamicObjectArray_1ae588cf420dfbd31ec90b95972e4d5dc9}

Can (optionally) be overridden to pre-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::SAVE_SERIALIZABLE_PRE is called.

#### Exceptions
* `[ShogunException](#classshogun_1_1ShogunException)` Will be thrown if an error occurres.

#### `public inline virtual `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`clone`](#classshogun_1_1CDynamicObjectArray_1a290165350894020201ade71ee7951da4)`()` {#classshogun_1_1CDynamicObjectArray_1a290165350894020201ade71ee7951da4}

Creates a clone of the current object. This is done via recursively traversing all parameters, which corresponds to a deep copy. Calling equals on the cloned object always returns true although none of the memory of both objects overlaps.

#### Returns
an identical copy of the given object, which is disjoint in memory. NULL if the clone fails. Note that the returned object is SG_REF'ed

#### `public bool `[`save_serializable`](#classshogun_1_1CDynamicObjectArray_1aa9787e341533c4970885ce6d3022a935)`()` {#classshogun_1_1CDynamicObjectArray_1aa9787e341533c4970885ce6d3022a935}

Save this object to file.

#### Parameters
* `file` where to save the object; will be closed during returning if PREFIX is an empty string. 

* `prefix` prefix for members 

#### Returns
TRUE if done, otherwise FALSE

#### `public bool `[`load_serializable`](#classshogun_1_1CDynamicObjectArray_1ad67e38ad80d4152151081f838c0a13e1)`()` {#classshogun_1_1CDynamicObjectArray_1ad67e38ad80d4152151081f838c0a13e1}

Load this object from file. If it will fail (returning FALSE) then this object will contain inconsistent data and should not be used!

#### Parameters
* `file` where to load from 

* `prefix` prefix for members

#### Returns
TRUE if done, otherwise FALSE

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

#### `protected template<>`  <br/>`inline `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`get_sgobject_type_dispatcher`](#classshogun_1_1CSGObject_1a7de7c1e11c3d4322d74a9a8cf5cc13f1)`(const std::string & name)` {#classshogun_1_1CSGObject_1a7de7c1e11c3d4322d74a9a8cf5cc13f1}

#### `protected virtual void `[`load_serializable_post`](#classshogun_1_1CSGObject_1a4c8da771d1ddf319cabc6b9e896326f2)`()` {#classshogun_1_1CSGObject_1a4c8da771d1ddf319cabc6b9e896326f2}

Can (optionally) be overridden to post-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::LOAD_SERIALIZABLE_POST is called.

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

