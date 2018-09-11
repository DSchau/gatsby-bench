---
classname: "shogun::CMulticlassLabels"
type: "class"
parents:
   - CDenseLabels
---

# class `shogun::CMulticlassLabels` {#classshogun_1_1CMulticlassLabels}

```
class shogun::CMulticlassLabels
  : public CDenseLabels
```

Multiclass Labels for multi-class classification.

valid values for labels are 0...nr_classes-1

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
`public  `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels_1a9898d6e0c0f3d6868c916f188474b8bc)`()` | default constructor
`public  `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels_1a595201f60a0f8492837618eab97cebe6)`(int32_t num_labels)` | constructor
`public  `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels_1acbc1683f258eb8653f107143bb5702dd)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > src)` | constructor
`public  `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels_1a00bdd46824d3a60dd2f1d0c0af8b30df)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` | constructor
`public  `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels_1a86c864164d5bafaee736f0382e2b3a93)`(`[`CBinaryLabels`](#classshogun_1_1CBinaryLabels)` * labels)` | Convert binary labels to multiclass labels, namely -1 is mapped to 0 and 1 to 1.
`public  `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels_1af72eb65716ad4323feb2d632fafc0102)`(const `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` & orig)` | copy constructor
`public  `[`~CMulticlassLabels`](#classshogun_1_1CMulticlassLabels_1acdbcc34b4cf579eea56a976ffab3527d)`()` | destructor
`public virtual void `[`ensure_valid`](#classshogun_1_1CMulticlassLabels_1a1204547969ab64cb4d0ab52826aec464)`(const char * context)` | Make sure the label is valid, otherwise raise SG_ERROR.
`public virtual bool `[`is_valid`](#classshogun_1_1CMulticlassLabels_1a8ca0e76fa665125f1e50bd1ed8dbd213)`() const` | 
`public virtual `[`ELabelType`](#LabelTypes_8h_1a833cc0312f852db7eda3413ce70137f0)` `[`get_label_type`](#classshogun_1_1CMulticlassLabels_1a1da62bc92dfcfad4fd2aec20b1bd3e9f)`() const` | get label type
`public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`duplicate`](#classshogun_1_1CMulticlassLabels_1ad4a0d44c2a04f3b6c8c900494eaa22e1)`() const` | shallow-copy of the labels object
`public `[`CBinaryLabels`](#classshogun_1_1CBinaryLabels)` * `[`get_binary_for_class`](#classshogun_1_1CMulticlassLabels_1ae7d650de203f7fb7072a19bd35523cc0)`(int32_t i)` | returns labels containing +1 at positions with ith class and -1 at other positions 
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_unique_labels`](#classshogun_1_1CMulticlassLabels_1a4d3ad1c2eb511ad1a57a9a0e913b6f8a)`()` | get unique labels (new [SGVector](#classshogun_1_1SGVector))
`public int32_t `[`get_num_classes`](#classshogun_1_1CMulticlassLabels_1a6f4805cadb70916790a9e962ae40e50d)`()` | return number of classes (for multiclass)
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_multiclass_confidences`](#classshogun_1_1CMulticlassLabels_1aaa4a41937bfa1d29ca8424096750c487)`(int32_t i)` | returns multiclass confidences
`public void `[`set_multiclass_confidences`](#classshogun_1_1CMulticlassLabels_1a468647ad16901df8144d50238b4c347d)`(int32_t i,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > confidences)` | sets multiclass confidences. to prepare labels for storing multiclass confidences call [allocate_confidences_for](#classshogun_1_1CMulticlassLabels_1a483d257b755c3f58b70909546e09432a)
`public void `[`allocate_confidences_for`](#classshogun_1_1CMulticlassLabels_1a483d257b755c3f58b70909546e09432a)`(int32_t n_classes)` | allocates matrix to store confidences. should always be called before setting confidences with [set_multiclass_confidences](#classshogun_1_1CMulticlassLabels_1a468647ad16901df8144d50238b4c347d)
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_confidences_for_class`](#classshogun_1_1CMulticlassLabels_1a8f9f8b3c96f6561cd7d9bbce3cec02bc)`(int32_t i)` | Returns confidence scores for given class 
`public inline virtual const char * `[`get_name`](#classshogun_1_1CMulticlassLabels_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` | #### Returns
`public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`shallow_subset_copy`](#classshogun_1_1CMulticlassLabels_1a7b9f050e5296dd55daae0e515a343dac)`()` | 
`public virtual void `[`load`](#classshogun_1_1CDenseLabels_1a5d33ec59a4be25056cca1f3b6691ad00)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` | load labels from file
`public virtual void `[`save`](#classshogun_1_1CDenseLabels_1a2ec11d78c7f60dfbc77bc2f56d211033)`(`[`CFile`](#classshogun_1_1CFile)` * writer)` | save labels to file
`public bool `[`set_label`](#classshogun_1_1CDenseLabels_1ab8b91e2dcef7026a5634357c16f1d6f6)`(int32_t idx,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` label)` | set label
`public bool `[`set_int_label`](#classshogun_1_1CDenseLabels_1ad826cfe684804543f79e0f1e162c376c)`(int32_t idx,int32_t label)` | set INT label
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_labels`](#classshogun_1_1CDenseLabels_1ad351ec499a0ff48cd208387c5acdefc3)`() const` | Getter for labels
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_label`](#classshogun_1_1CDenseLabels_1a3531d71e148d7b7ca53168ac6f4354c8)`(int32_t idx) const` | get label
`public template<>`  <br/>`inline ST `[`get_label_t`](#classshogun_1_1CDenseLabels_1a3e212d80b8eeeb7888163cfe9fc088de)`(int32_t idx)` | get label
`public int32_t `[`get_int_label`](#classshogun_1_1CDenseLabels_1ac3a767518e50c11bc4539e85369d32cd)`(int32_t idx)` | get INT label
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_labels_copy`](#classshogun_1_1CDenseLabels_1a884b1cceecfeec14efbdfbe04855e8b4)`() const` | Gets a copy of the labels.
`public template<>`  <br/>`inline `[`SGVector`](#classshogun_1_1SGVector)`< ST > `[`get_labels_t`](#classshogun_1_1CDenseLabels_1ae711d7c44800eeb48ab3d6b2ca4eb118)`()` | Getter for labels
`public template<>`  <br/>`inline `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_labels_t`](#classshogun_1_1CDenseLabels_1af7277d907ed4cfd32ef0671175033c43)`()` | Specialization of get_labels for float64_t 
`public template<>`  <br/>`inline `[`SGVector`](#classshogun_1_1SGVector)`< ST > `[`get_labels_copy_t`](#classshogun_1_1CDenseLabels_1a5f0fc56694ed0e5c9cfc9fd650b10f27)`()` | Get copy of labels.
`public void `[`set_labels`](#classshogun_1_1CDenseLabels_1a310d7ad853bf2912a51641e5dad32fa1)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > v)` | set labels
`public void `[`set_to_one`](#classshogun_1_1CDenseLabels_1a0c563adbe5a769235dc022528e315ee3)`()` | set all labels to +1
`public void `[`zero`](#classshogun_1_1CDenseLabels_1a0c4493a5d4723940d60164428f11adc3)`()` | set all labels to zero
`public void `[`set_to_const`](#classshogun_1_1CDenseLabels_1a713171399bd2f6a9657db5e69d0f3380)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` c)` | set all labels to a const value
`public `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`get_int_labels`](#classshogun_1_1CDenseLabels_1a40d47772d91ef58945177b3733854ed7)`()` | get INT label vector
`public void `[`set_int_labels`](#classshogun_1_1CDenseLabels_1a1fb70e8eec51294dabb1d9c3a5884147)`(`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > labels)` | set INT labels
`public void `[`set_int_labels`](#classshogun_1_1CDenseLabels_1a308cf278f3517265ddda72be1886cb16)`(`[`SGVector`](#classshogun_1_1SGVector)`< int64_t > labels)` | set INT64 labels
`public virtual int32_t `[`get_num_labels`](#classshogun_1_1CDenseLabels_1a59b093403e4a6044c2110c5f43844568)`() const` | get number of labels, depending on whether a subset is set
`public virtual void `[`add_subset`](#classshogun_1_1CLabels_1acb58d8008e2ef9bb83e6b5fc5fb42f71)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > subset)` | Adds a subset of indices on top of the current subsets (possibly subset of subset). Every call causes a new active index vector to be stored. Added subsets can be removed one-by-one. If this is not needed, [add_subset_in_place()](#classshogun_1_1CLabels_1a6dabbf53b34ca64a7645191b8ea04e31) should be used (does not store intermediate index vectors)
`public virtual void `[`add_subset_in_place`](#classshogun_1_1CLabels_1a6dabbf53b34ca64a7645191b8ea04e31)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > subset)` | Sets/changes latest added subset. This allows to add multiple subsets with in-place memory requirements. They cannot be removed one-by-one afterwards, only the latest active can. If this is needed, use [add_subset()](#classshogun_1_1CLabels_1acb58d8008e2ef9bb83e6b5fc5fb42f71). If no subset is active, this just adds.
`public virtual void `[`remove_subset`](#classshogun_1_1CLabels_1a5c8a113b96b3d3a2d565ed9fffeed172)`()` | removes that last added subset from subset stack, if existing Calls subset_changed_post() afterwards
`public virtual void `[`remove_all_subsets`](#classshogun_1_1CLabels_1a434b4feb76767ed0adc9ccdd55a3ef61)`()` | removes all subsets Calls subset_changed_post() afterwards
`public virtual `[`CSubsetStack`](#classshogun_1_1CSubsetStack)` * `[`get_subset_stack`](#classshogun_1_1CLabels_1a47944f23a63a0eed56ff3d0bba40d253)`()` | #### Returns
`public virtual void `[`set_value`](#classshogun_1_1CLabels_1a49659fe98b31d132e094bdb7a160010e)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` value,int32_t idx)` | set the confidence value for a particular label
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_value`](#classshogun_1_1CLabels_1a39d824bb6ab9225a9a3c4d5048cbb56e)`(int32_t idx)` | get confidence value for a particular label
`public virtual void `[`set_values`](#classshogun_1_1CLabels_1a601a8078ac4c38c63f3d76c988d409c5)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > values)` | set confidence vector
`public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_values`](#classshogun_1_1CLabels_1a78696d29755d27c4e76a52450db1aef3)`() const` | get confidence vector
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
`protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_multiclass_confidences`](#classshogun_1_1CMulticlassLabels_1a742285c71f0b1e48a7c947b5c46cc3b2) | multiclass confidences
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_labels`](#classshogun_1_1CDenseLabels_1acec7a2d58953bf621e3ae4660e90032e) | the label vector
`protected `[`CSubsetStack`](#classshogun_1_1CSubsetStack)` * `[`m_subset_stack`](#classshogun_1_1CLabels_1ac406fc1620ad5a8714a1c34c935ae328) | subset class to enable subset support for this class
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_current_values`](#classshogun_1_1CLabels_1ab559d0f92c583591d35943d65c63cf8f) | current active value vector
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

#### `public  `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels_1a9898d6e0c0f3d6868c916f188474b8bc)`()` {#classshogun_1_1CMulticlassLabels_1a9898d6e0c0f3d6868c916f188474b8bc}

default constructor

#### `public  `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels_1a595201f60a0f8492837618eab97cebe6)`(int32_t num_labels)` {#classshogun_1_1CMulticlassLabels_1a595201f60a0f8492837618eab97cebe6}

constructor

#### Parameters
* `num_labels` number of labels

#### `public  `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels_1acbc1683f258eb8653f107143bb5702dd)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > src)` {#classshogun_1_1CMulticlassLabels_1acbc1683f258eb8653f107143bb5702dd}

constructor

#### Parameters
* `src` labels to set

#### `public  `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels_1a00bdd46824d3a60dd2f1d0c0af8b30df)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` {#classshogun_1_1CMulticlassLabels_1a00bdd46824d3a60dd2f1d0c0af8b30df}

constructor

#### Parameters
* `loader` File object via which to load data

#### `public  `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels_1a86c864164d5bafaee736f0382e2b3a93)`(`[`CBinaryLabels`](#classshogun_1_1CBinaryLabels)` * labels)` {#classshogun_1_1CMulticlassLabels_1a86c864164d5bafaee736f0382e2b3a93}

Convert binary labels to multiclass labels, namely -1 is mapped to 0 and 1 to 1.

#### Parameters
* `labels` Binary labels

#### `public  `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels_1af72eb65716ad4323feb2d632fafc0102)`(const `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` & orig)` {#classshogun_1_1CMulticlassLabels_1af72eb65716ad4323feb2d632fafc0102}

copy constructor

#### `public  `[`~CMulticlassLabels`](#classshogun_1_1CMulticlassLabels_1acdbcc34b4cf579eea56a976ffab3527d)`()` {#classshogun_1_1CMulticlassLabels_1acdbcc34b4cf579eea56a976ffab3527d}

destructor

#### `public virtual void `[`ensure_valid`](#classshogun_1_1CMulticlassLabels_1a1204547969ab64cb4d0ab52826aec464)`(const char * context)` {#classshogun_1_1CMulticlassLabels_1a1204547969ab64cb4d0ab52826aec464}

Make sure the label is valid, otherwise raise SG_ERROR.

possible with subset

#### Parameters
* `context` optional message to convey the context

#### `public virtual bool `[`is_valid`](#classshogun_1_1CMulticlassLabels_1a8ca0e76fa665125f1e50bd1ed8dbd213)`() const` {#classshogun_1_1CMulticlassLabels_1a8ca0e76fa665125f1e50bd1ed8dbd213}

#### `public virtual `[`ELabelType`](#LabelTypes_8h_1a833cc0312f852db7eda3413ce70137f0)` `[`get_label_type`](#classshogun_1_1CMulticlassLabels_1a1da62bc92dfcfad4fd2aec20b1bd3e9f)`() const` {#classshogun_1_1CMulticlassLabels_1a1da62bc92dfcfad4fd2aec20b1bd3e9f}

get label type

#### Returns
label type multiclass

#### `public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`duplicate`](#classshogun_1_1CMulticlassLabels_1ad4a0d44c2a04f3b6c8c900494eaa22e1)`() const` {#classshogun_1_1CMulticlassLabels_1ad4a0d44c2a04f3b6c8c900494eaa22e1}

shallow-copy of the labels object

#### Returns
labels object

#### `public `[`CBinaryLabels`](#classshogun_1_1CBinaryLabels)` * `[`get_binary_for_class`](#classshogun_1_1CMulticlassLabels_1ae7d650de203f7fb7072a19bd35523cc0)`(int32_t i)` {#classshogun_1_1CMulticlassLabels_1ae7d650de203f7fb7072a19bd35523cc0}

returns labels containing +1 at positions with ith class and -1 at other positions 
#### Parameters
* `i` index of class 

#### Returns
new binary labels

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_unique_labels`](#classshogun_1_1CMulticlassLabels_1a4d3ad1c2eb511ad1a57a9a0e913b6f8a)`()` {#classshogun_1_1CMulticlassLabels_1a4d3ad1c2eb511ad1a57a9a0e913b6f8a}

get unique labels (new [SGVector](#classshogun_1_1SGVector))

possible with subset

#### Returns
unique labels

#### `public int32_t `[`get_num_classes`](#classshogun_1_1CMulticlassLabels_1a6f4805cadb70916790a9e962ae40e50d)`()` {#classshogun_1_1CMulticlassLabels_1a6f4805cadb70916790a9e962ae40e50d}

return number of classes (for multiclass)

possible with subset

#### Returns
number of classes

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_multiclass_confidences`](#classshogun_1_1CMulticlassLabels_1aaa4a41937bfa1d29ca8424096750c487)`(int32_t i)` {#classshogun_1_1CMulticlassLabels_1aaa4a41937bfa1d29ca8424096750c487}

returns multiclass confidences

#### Parameters
* `i` index 

#### Returns
confidences of ith result

#### `public void `[`set_multiclass_confidences`](#classshogun_1_1CMulticlassLabels_1a468647ad16901df8144d50238b4c347d)`(int32_t i,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > confidences)` {#classshogun_1_1CMulticlassLabels_1a468647ad16901df8144d50238b4c347d}

sets multiclass confidences. to prepare labels for storing multiclass confidences call [allocate_confidences_for](#classshogun_1_1CMulticlassLabels_1a483d257b755c3f58b70909546e09432a)

#### Parameters
* `i` index 

* `confidences` confidences to be set for ith result

#### `public void `[`allocate_confidences_for`](#classshogun_1_1CMulticlassLabels_1a483d257b755c3f58b70909546e09432a)`(int32_t n_classes)` {#classshogun_1_1CMulticlassLabels_1a483d257b755c3f58b70909546e09432a}

allocates matrix to store confidences. should always be called before setting confidences with [set_multiclass_confidences](#classshogun_1_1CMulticlassLabels_1a468647ad16901df8144d50238b4c347d)

#### Parameters
* `n_classes` number of classes

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_confidences_for_class`](#classshogun_1_1CMulticlassLabels_1a8f9f8b3c96f6561cd7d9bbce3cec02bc)`(int32_t i)` {#classshogun_1_1CMulticlassLabels_1a8f9f8b3c96f6561cd7d9bbce3cec02bc}

Returns confidence scores for given class 
#### Parameters
* `i` Class index 

#### Returns
Confidences of class i

#### `public inline virtual const char * `[`get_name`](#classshogun_1_1CMulticlassLabels_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` {#classshogun_1_1CMulticlassLabels_1a9cb485686dd7a1e6f7103cf42e87717e}

#### Returns
object name

#### `public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`shallow_subset_copy`](#classshogun_1_1CMulticlassLabels_1a7b9f050e5296dd55daae0e515a343dac)`()` {#classshogun_1_1CMulticlassLabels_1a7b9f050e5296dd55daae0e515a343dac}

#### `public virtual void `[`load`](#classshogun_1_1CDenseLabels_1a5d33ec59a4be25056cca1f3b6691ad00)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` {#classshogun_1_1CDenseLabels_1a5d33ec59a4be25056cca1f3b6691ad00}

load labels from file

any subset is removed before

#### Parameters
* `loader` File object via which to load data

#### `public virtual void `[`save`](#classshogun_1_1CDenseLabels_1a2ec11d78c7f60dfbc77bc2f56d211033)`(`[`CFile`](#classshogun_1_1CFile)` * writer)` {#classshogun_1_1CDenseLabels_1a2ec11d78c7f60dfbc77bc2f56d211033}

save labels to file

not possible with subset

#### Parameters
* `writer` File object via which to save data

#### `public bool `[`set_label`](#classshogun_1_1CDenseLabels_1ab8b91e2dcef7026a5634357c16f1d6f6)`(int32_t idx,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` label)` {#classshogun_1_1CDenseLabels_1ab8b91e2dcef7026a5634357c16f1d6f6}

set label

possible with subset

#### Parameters
* `idx` index of label to set 

* `label` value of label 

#### Returns
if setting was successful

#### `public bool `[`set_int_label`](#classshogun_1_1CDenseLabels_1ad826cfe684804543f79e0f1e162c376c)`(int32_t idx,int32_t label)` {#classshogun_1_1CDenseLabels_1ad826cfe684804543f79e0f1e162c376c}

set INT label

possible with subset

#### Parameters
* `idx` index of label to set 

* `label` INT value of label 

#### Returns
if setting was successful

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_labels`](#classshogun_1_1CDenseLabels_1ad351ec499a0ff48cd208387c5acdefc3)`() const` {#classshogun_1_1CDenseLabels_1ad351ec499a0ff48cd208387c5acdefc3}

Getter for labels

#### Returns
labels, a copy if a subset is set

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_label`](#classshogun_1_1CDenseLabels_1a3531d71e148d7b7ca53168ac6f4354c8)`(int32_t idx) const` {#classshogun_1_1CDenseLabels_1a3531d71e148d7b7ca53168ac6f4354c8}

get label

possible with subset

#### Parameters
* `idx` index of label to get 

#### Returns
value of label

#### `public template<>`  <br/>`inline ST `[`get_label_t`](#classshogun_1_1CDenseLabels_1a3e212d80b8eeeb7888163cfe9fc088de)`(int32_t idx)` {#classshogun_1_1CDenseLabels_1a3e212d80b8eeeb7888163cfe9fc088de}

get label

possible with subset

#### Parameters
* `idx` index of label to get 

#### Returns
value of label

#### `public int32_t `[`get_int_label`](#classshogun_1_1CDenseLabels_1ac3a767518e50c11bc4539e85369d32cd)`(int32_t idx)` {#classshogun_1_1CDenseLabels_1ac3a767518e50c11bc4539e85369d32cd}

get INT label

possible with subset

#### Parameters
* `idx` index of label to get 

#### Returns
INT value of label

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_labels_copy`](#classshogun_1_1CDenseLabels_1a884b1cceecfeec14efbdfbe04855e8b4)`() const` {#classshogun_1_1CDenseLabels_1a884b1cceecfeec14efbdfbe04855e8b4}

Gets a copy of the labels.

possible with subset

#### Returns
labels

#### `public template<>`  <br/>`inline `[`SGVector`](#classshogun_1_1SGVector)`< ST > `[`get_labels_t`](#classshogun_1_1CDenseLabels_1ae711d7c44800eeb48ab3d6b2ca4eb118)`()` {#classshogun_1_1CDenseLabels_1ae711d7c44800eeb48ab3d6b2ca4eb118}

Getter for labels

#### Returns
labels, or a copy of them if a subset is set or if ST is not of type float64_t

#### `public template<>`  <br/>`inline `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_labels_t`](#classshogun_1_1CDenseLabels_1af7277d907ed4cfd32ef0671175033c43)`()` {#classshogun_1_1CDenseLabels_1af7277d907ed4cfd32ef0671175033c43}

Specialization of get_labels for float64_t 
#### Returns
labels, or a copy of them if a subset is set

#### `public template<>`  <br/>`inline `[`SGVector`](#classshogun_1_1SGVector)`< ST > `[`get_labels_copy_t`](#classshogun_1_1CDenseLabels_1a5f0fc56694ed0e5c9cfc9fd650b10f27)`()` {#classshogun_1_1CDenseLabels_1a5f0fc56694ed0e5c9cfc9fd650b10f27}

Get copy of labels.

possible with subset

#### Returns
labels

#### `public void `[`set_labels`](#classshogun_1_1CDenseLabels_1a310d7ad853bf2912a51641e5dad32fa1)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > v)` {#classshogun_1_1CDenseLabels_1a310d7ad853bf2912a51641e5dad32fa1}

set labels

not possible with subset

#### Parameters
* `v` labels

#### `public void `[`set_to_one`](#classshogun_1_1CDenseLabels_1a0c563adbe5a769235dc022528e315ee3)`()` {#classshogun_1_1CDenseLabels_1a0c563adbe5a769235dc022528e315ee3}

set all labels to +1

possible with subset

#### `public void `[`zero`](#classshogun_1_1CDenseLabels_1a0c4493a5d4723940d60164428f11adc3)`()` {#classshogun_1_1CDenseLabels_1a0c4493a5d4723940d60164428f11adc3}

set all labels to zero

possible with subset

#### `public void `[`set_to_const`](#classshogun_1_1CDenseLabels_1a713171399bd2f6a9657db5e69d0f3380)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` c)` {#classshogun_1_1CDenseLabels_1a713171399bd2f6a9657db5e69d0f3380}

set all labels to a const value

possible with subset

#### Parameters
* `c` const to set labels to

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`get_int_labels`](#classshogun_1_1CDenseLabels_1a40d47772d91ef58945177b3733854ed7)`()` {#classshogun_1_1CDenseLabels_1a40d47772d91ef58945177b3733854ed7}

get INT label vector

possible with subset

#### Returns
INT labels

#### `public void `[`set_int_labels`](#classshogun_1_1CDenseLabels_1a1fb70e8eec51294dabb1d9c3a5884147)`(`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > labels)` {#classshogun_1_1CDenseLabels_1a1fb70e8eec51294dabb1d9c3a5884147}

set INT labels

not possible on subset

#### Parameters
* `labels` INT labels

#### `public void `[`set_int_labels`](#classshogun_1_1CDenseLabels_1a308cf278f3517265ddda72be1886cb16)`(`[`SGVector`](#classshogun_1_1SGVector)`< int64_t > labels)` {#classshogun_1_1CDenseLabels_1a308cf278f3517265ddda72be1886cb16}

set INT64 labels

not possible on subset

#### Parameters
* `labels` INT labels

#### `public virtual int32_t `[`get_num_labels`](#classshogun_1_1CDenseLabels_1a59b093403e4a6044c2110c5f43844568)`() const` {#classshogun_1_1CDenseLabels_1a59b093403e4a6044c2110c5f43844568}

get number of labels, depending on whether a subset is set

#### Returns
number of labels

#### `public virtual void `[`add_subset`](#classshogun_1_1CLabels_1acb58d8008e2ef9bb83e6b5fc5fb42f71)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > subset)` {#classshogun_1_1CLabels_1acb58d8008e2ef9bb83e6b5fc5fb42f71}

Adds a subset of indices on top of the current subsets (possibly subset of subset). Every call causes a new active index vector to be stored. Added subsets can be removed one-by-one. If this is not needed, [add_subset_in_place()](#classshogun_1_1CLabels_1a6dabbf53b34ca64a7645191b8ea04e31) should be used (does not store intermediate index vectors)

#### Parameters
* `subset` subset of indices to add

#### `public virtual void `[`add_subset_in_place`](#classshogun_1_1CLabels_1a6dabbf53b34ca64a7645191b8ea04e31)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > subset)` {#classshogun_1_1CLabels_1a6dabbf53b34ca64a7645191b8ea04e31}

Sets/changes latest added subset. This allows to add multiple subsets with in-place memory requirements. They cannot be removed one-by-one afterwards, only the latest active can. If this is needed, use [add_subset()](#classshogun_1_1CLabels_1acb58d8008e2ef9bb83e6b5fc5fb42f71). If no subset is active, this just adds.

#### Parameters
* `subset` subset of indices to replace the latest one with.

#### `public virtual void `[`remove_subset`](#classshogun_1_1CLabels_1a5c8a113b96b3d3a2d565ed9fffeed172)`()` {#classshogun_1_1CLabels_1a5c8a113b96b3d3a2d565ed9fffeed172}

removes that last added subset from subset stack, if existing Calls subset_changed_post() afterwards

#### `public virtual void `[`remove_all_subsets`](#classshogun_1_1CLabels_1a434b4feb76767ed0adc9ccdd55a3ef61)`()` {#classshogun_1_1CLabels_1a434b4feb76767ed0adc9ccdd55a3ef61}

removes all subsets Calls subset_changed_post() afterwards

#### `public virtual `[`CSubsetStack`](#classshogun_1_1CSubsetStack)` * `[`get_subset_stack`](#classshogun_1_1CLabels_1a47944f23a63a0eed56ff3d0bba40d253)`()` {#classshogun_1_1CLabels_1a47944f23a63a0eed56ff3d0bba40d253}

#### Returns
subset stack

#### `public virtual void `[`set_value`](#classshogun_1_1CLabels_1a49659fe98b31d132e094bdb7a160010e)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` value,int32_t idx)` {#classshogun_1_1CLabels_1a49659fe98b31d132e094bdb7a160010e}

set the confidence value for a particular label

#### Parameters
* `value` value to set 

* `idx` label index whose conf. value is to be changed

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_value`](#classshogun_1_1CLabels_1a39d824bb6ab9225a9a3c4d5048cbb56e)`(int32_t idx)` {#classshogun_1_1CLabels_1a39d824bb6ab9225a9a3c4d5048cbb56e}

get confidence value for a particular label

#### Parameters
* `idx` label index 

#### Returns
confidence value of label with index idx

#### `public virtual void `[`set_values`](#classshogun_1_1CLabels_1a601a8078ac4c38c63f3d76c988d409c5)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > values)` {#classshogun_1_1CLabels_1a601a8078ac4c38c63f3d76c988d409c5}

set confidence vector

#### Parameters
* `values` to be set (should have zero length to disable values or length must match the number of labels)

#### `public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_values`](#classshogun_1_1CLabels_1a78696d29755d27c4e76a52450db1aef3)`() const` {#classshogun_1_1CLabels_1a78696d29755d27c4e76a52450db1aef3}

get confidence vector

#### Returns
confidences

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

#### `protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_multiclass_confidences`](#classshogun_1_1CMulticlassLabels_1a742285c71f0b1e48a7c947b5c46cc3b2) {#classshogun_1_1CMulticlassLabels_1a742285c71f0b1e48a7c947b5c46cc3b2}

multiclass confidences

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_labels`](#classshogun_1_1CDenseLabels_1acec7a2d58953bf621e3ae4660e90032e) {#classshogun_1_1CDenseLabels_1acec7a2d58953bf621e3ae4660e90032e}

the label vector

#### `protected `[`CSubsetStack`](#classshogun_1_1CSubsetStack)` * `[`m_subset_stack`](#classshogun_1_1CLabels_1ac406fc1620ad5a8714a1c34c935ae328) {#classshogun_1_1CLabels_1ac406fc1620ad5a8714a1c34c935ae328}

subset class to enable subset support for this class

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_current_values`](#classshogun_1_1CLabels_1ab559d0f92c583591d35943d65c63cf8f) {#classshogun_1_1CLabels_1ab559d0f92c583591d35943d65c63cf8f}

current active value vector

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

