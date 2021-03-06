---
classname: "shogun::CStreamingFeatures"
type: "class"
parents:
   - CFeatures
---

# class `shogun::CStreamingFeatures` {#classshogun_1_1CStreamingFeatures}

```
class shogun::CStreamingFeatures
  : public CFeatures
```

Streaming features are features which are used for online algorithms.

Reading/parsing of input, and learning through the algorithm are carried out in separate threads. Input is from a [CStreamingFile](#classshogun_1_1CStreamingFile) object.

A StreamingFeatures object usually stores only one example at a time, and any function like [dot()](#namespaceshogun_1_1linalg_1aae325216f018daabe22528936b009f82), add_to_dense_vec() etc. apply with this example as one implicit operand.

Similarly, when we refer to the "feature vector" of a StreamingFeatures object, it refers to the vector of the example currently stored in that object.

It is up to the user to indicate when he is done using the example so that the next one can be fetched and stored in its place.

[Example](#classshogun_1_1Example) objects are fetched one-by-one through a [CInputParser](#classshogun_1_1CInputParser) object, and therefore a StreamingFeatures object must implement the following methods in the derived class:

* [start_parser()](#classshogun_1_1CStreamingFeatures_1a63f7baa945e9f36edf871f72e35d0c6d): a function to begin processing of the input.

* [end_parser()](#classshogun_1_1CStreamingFeatures_1a4e8b525b2b76468755c1502d022b82e2): end the parser; wait for the parsing thread to finish.

* [get_next_example()](#classshogun_1_1CStreamingFeatures_1acbf87bddb7fb5c23d0fd50f2c999aee5): instruct the parser to get the next example.

* [release_example()](#classshogun_1_1CStreamingFeatures_1a6221e49be7a20336dc65996aa43f2721): instruct the parser to release the current example.

* [get_label()](#classshogun_1_1CStreamingFeatures_1a7791fdff6c5424dd6a6d12faf9a283fb): returns the label (if applicable) for the current example.

* [get_num_features()](#classshogun_1_1CStreamingFeatures_1a820c06a0720897ec49ca0a87bd6851f8): returns the number of features for the current example.

* [release_example()](#classshogun_1_1CStreamingFeatures_1a6221e49be7a20336dc65996aa43f2721) must be called before [get_next_example()](#classshogun_1_1CStreamingFeatures_1acbf87bddb7fb5c23d0fd50f2c999aee5).

* [get_streamed_features()](#classshogun_1_1CStreamingFeatures_1a28a9485cfe9d295474555b512aa554ae) to retreive a non-streaming instance of a certain size (has to be implemented in subclasses)

* from_non_streaming() to stream features from an existing features object (has to be implemented in subclasses)

The feature vector itself may be returned through a derived class since at the moment the parser is templated for each data type.

Thus, a templated or specialized version of get_vector(SGVector<T>) must be implemented in the derived class.

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
`public  `[`CStreamingFeatures`](#classshogun_1_1CStreamingFeatures_1a999e580c8a87f0d2dcc3c3398d00db52)`()` | Default constructor with no args. Doesn't do anything yet.
`public  `[`CStreamingFeatures`](#classshogun_1_1CStreamingFeatures_1ac16fb744fbc2f13aec01b235e481ca66)`(const `[`CStreamingFeatures`](#classshogun_1_1CStreamingFeatures)` &) = delete` | 
`public virtual  `[`~CStreamingFeatures`](#classshogun_1_1CStreamingFeatures_1aa59ab1267b2e9196a485664c2e0ca220)`()` | Destructor
`public void `[`set_read_functions`](#classshogun_1_1CStreamingFeatures_1a4fbbbc398671e657437fdf37d59489d1)`()` | Set the vector reading functions.
`public void `[`set_vector_reader`](#classshogun_1_1CStreamingFeatures_1ade9a2fd19ebf69e179df3aaa3e4046a4)`()` | The derived object must set the function which will be used for reading one vector from the file. This function should be a member of the [CStreamingFile](#classshogun_1_1CStreamingFile) class.
`public void `[`set_vector_and_label_reader`](#classshogun_1_1CStreamingFeatures_1ac42301c8736a4d9f9529d70d5eaec221)`()` | The derived object must set the function which will be used by the parser for reading one vector and label from the file. This function should be a member of the [CStreamingFile](#classshogun_1_1CStreamingFile) class.
`public void `[`start_parser`](#classshogun_1_1CStreamingFeatures_1a63f7baa945e9f36edf871f72e35d0c6d)`()` | Start the parser. It stores parsed examples from the input in a separate thread.
`public void `[`end_parser`](#classshogun_1_1CStreamingFeatures_1a4e8b525b2b76468755c1502d022b82e2)`()` | End the parser. Wait for the parsing thread to complete.
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_label`](#classshogun_1_1CStreamingFeatures_1a7791fdff6c5424dd6a6d12faf9a283fb)`()` | Return the label of the current example.
`public bool `[`get_next_example`](#classshogun_1_1CStreamingFeatures_1acbf87bddb7fb5c23d0fd50f2c999aee5)`()` | Indicate to the parser that it must fetch the next example.
`public void `[`release_example`](#classshogun_1_1CStreamingFeatures_1a6221e49be7a20336dc65996aa43f2721)`()` | Indicate that processing of the current example is done. The parser then considers it safe to dispose of that example and replace it with another one.
`public int32_t `[`get_num_features`](#classshogun_1_1CStreamingFeatures_1a820c06a0720897ec49ca0a87bd6851f8)`()` | Get the number of features in the current example.
`public virtual bool `[`get_has_labels`](#classshogun_1_1CStreamingFeatures_1ad3bf3f11810ab28653b01a20a08afe22)`()` | Return whether the examples are labelled or not.
`public virtual bool `[`is_seekable`](#classshogun_1_1CStreamingFeatures_1a18cbb4c042cbc4a268d13d4487620914)`()` | Whether the stream is seekable (to check if multiple epochs are possible), i.e., whether we can process examples in a batch fashion.
`public virtual void `[`reset_stream`](#classshogun_1_1CStreamingFeatures_1ae43311be283c1e503ac4ac4791db4922)`()` | Function to reset the stream (if possible).
`public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`get_streamed_features`](#classshogun_1_1CStreamingFeatures_1a28a9485cfe9d295474555b512aa554ae)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_elements)` | Returns a new [CFeatures](#classshogun_1_1CFeatures) instance which contains num_elements elements from the underlying stream. Not SG_REF'ed
`public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`duplicate`](#classshogun_1_1CStreamingFeatures_1a1af3e52183eff1d8dd311d55ce2eadb1)`() const` | Duplicate the object.
`public `[`EFeatureType`](#namespaceshogun_1a064eec90e91f56435546d77f38c0b618)` `[`get_feature_type`](#classshogun_1_1CFeatures_1a1a59079da3a831192228507e5945c78b)`() const` | get feature type
`public `[`EFeatureClass`](#namespaceshogun_1a9e2a4d8b86b9e061779c3fdbcda57c3b)` `[`get_feature_class`](#classshogun_1_1CFeatures_1a613776af659954ebda6aa77a274b1a1e)`() const` | get feature class
`public inline virtual `[`Range`](#classshogun_1_1Range)`< int32_t > `[`index_iterator`](#classshogun_1_1CFeatures_1a71bb6f4167a24d55e8e12fca77baabcd)`() const` | returns an iterator of indices from 0 to [CFeatures::get_num_vectors](#classshogun_1_1CFeatures_1a91f8bf82dad4bb05accdc606d85a0da3)
`public virtual void `[`add_preprocessor`](#classshogun_1_1CFeatures_1a53d5b6b17d8e4b44117d404b119faca6)`(`[`CPreprocessor`](#classshogun_1_1CPreprocessor)` * p)` | add preprocessor
`public virtual void `[`del_preprocessor`](#classshogun_1_1CFeatures_1af2ad4fb4c64ea892dc73a288f1be27a2)`(int32_t num)` | delete preprocessor from list
`public `[`CPreprocessor`](#classshogun_1_1CPreprocessor)` * `[`get_preprocessor`](#classshogun_1_1CFeatures_1a16a2c185a1d7059892ef6ffb2d09f19b)`(int32_t num) const` | get specified preprocessor
`public int32_t `[`get_num_preprocessors`](#classshogun_1_1CFeatures_1aa1b9b05b4535ba2c8c888aa107321c54)`() const` | get number of preprocessors
`public void `[`clean_preprocessors`](#classshogun_1_1CFeatures_1aa6b20826d18617fc3bc0482c73908fb2)`()` | clears all preprocs
`public void `[`list_preprocessors`](#classshogun_1_1CFeatures_1a476493a28014c60a6006106f3d846147)`()` | print preprocessors
`public int32_t `[`get_cache_size`](#classshogun_1_1CFeatures_1a6b599085eff3dab5a66cce6f133ae47e)`() const` | get cache size
`public int32_t `[`get_num_vectors`](#classshogun_1_1CFeatures_1a91f8bf82dad4bb05accdc606d85a0da3)`() const` | get number of examples/vectors, possibly corresponding to the current subset
`public virtual bool `[`reshape`](#classshogun_1_1CFeatures_1ad2a12e099e61e61e3872253a13cc0287)`(int32_t num_features,int32_t num_vectors)` | in case there is a feature matrix allow for reshaping
`public void `[`list_feature_obj`](#classshogun_1_1CFeatures_1aff469383824e5b8736c191cd4e4476b7)`() const` | list feature object
`public virtual void `[`load`](#classshogun_1_1CFeatures_1a5d33ec59a4be25056cca1f3b6691ad00)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` | load features from file
`public virtual void `[`save`](#classshogun_1_1CFeatures_1a2ec11d78c7f60dfbc77bc2f56d211033)`(`[`CFile`](#classshogun_1_1CFile)` * writer)` | save features to file
`public bool `[`check_feature_compatibility`](#classshogun_1_1CFeatures_1a7fe9c8b9c4e4474b1893f837ea29fa21)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * f) const` | check feature compatibility
`public bool `[`has_property`](#classshogun_1_1CFeatures_1af181de39b142f32c3bb00a19bea32bcc)`(`[`EFeatureProperty`](#namespaceshogun_1add4a728b32cf3898a63b2ef4564c1925)` p) const` | check if features have given property
`public void `[`set_property`](#classshogun_1_1CFeatures_1a732ec5df91b2d7d80ae25a79fe068055)`(`[`EFeatureProperty`](#namespaceshogun_1add4a728b32cf3898a63b2ef4564c1925)` p)` | set property
`public void `[`unset_property`](#classshogun_1_1CFeatures_1affaad72e745ecc61e93d676d78705b1e)`(`[`EFeatureProperty`](#namespaceshogun_1add4a728b32cf3898a63b2ef4564c1925)` p)` | unset property
`public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`create_merged_copy`](#classshogun_1_1CFeatures_1abba142f59793094f4f324787d43e0b4e)`(`[`CList`](#classshogun_1_1CList)` * others) const` | Takes a list of feature instances and returns a new instance being a concatenation of a copy of this instace's data and the given instancess data. Note that the feature types have to be equal.
`public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`create_merged_copy`](#classshogun_1_1CFeatures_1aef378f04b4eb3b6a21752a5400260769)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * other) const` | Convenience method for method with same name and list as parameter.
`public virtual void `[`add_subset`](#classshogun_1_1CFeatures_1acb58d8008e2ef9bb83e6b5fc5fb42f71)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > subset)` | Adds a subset of indices on top of the current subsets (possibly subset of subset). Every call causes a new active index vector to be stored. Added subsets can be removed one-by-one. If this is not needed, [add_subset_in_place()](#classshogun_1_1CFeatures_1a6dabbf53b34ca64a7645191b8ea04e31) should be used (does not store intermediate index vectors)
`public virtual void `[`add_subset_in_place`](#classshogun_1_1CFeatures_1a6dabbf53b34ca64a7645191b8ea04e31)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > subset)` | Sets/changes latest added subset. This allows to add multiple subsets with in-place memory requirements. They cannot be removed one-by-one afterwards, only the latest active can. If this is needed, use [add_subset()](#classshogun_1_1CFeatures_1acb58d8008e2ef9bb83e6b5fc5fb42f71). If no subset is active, this just adds.
`public virtual void `[`remove_subset`](#classshogun_1_1CFeatures_1a5c8a113b96b3d3a2d565ed9fffeed172)`()` | removes that last added subset from subset stack, if existing Calls [subset_changed_post()](#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7) afterwards
`public virtual void `[`remove_all_subsets`](#classshogun_1_1CFeatures_1a434b4feb76767ed0adc9ccdd55a3ef61)`()` | removes all subsets Calls [subset_changed_post()](#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7) afterwards
`public virtual `[`CSubsetStack`](#classshogun_1_1CSubsetStack)` * `[`get_subset_stack`](#classshogun_1_1CFeatures_1a47944f23a63a0eed56ff3d0bba40d253)`()` | returns subset stack
`public inline virtual void `[`subset_changed_post`](#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7)`()` | method may be overwritten to update things that depend on subset
`public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`copy_subset`](#classshogun_1_1CFeatures_1adf4a1baaff0c06456ceca3b217c46338)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | Creates a new [CFeatures](#classshogun_1_1CFeatures) instance containing copies of the elements which are specified by the provided indices.
`public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`copy_dimension_subset`](#classshogun_1_1CFeatures_1ab5e4da6272e74503f9ac4405d8ac92b5)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > dims)` | Creates a new [CFeatures](#classshogun_1_1CFeatures) instance containing only the dimensions of the feature vector which are specified by the provided indices.
`public inline virtual bool `[`support_compatible_class`](#classshogun_1_1CFeatures_1a0e8af4cc2f64bde8fe2b3dd4557e9a4f)`() const` | does this class support compatible computation bewteen difference classes? for example, this->dot(rhs_prt), can rhs_prt be an instance of a difference class?
`public virtual bool `[`get_feature_class_compatibility`](#classshogun_1_1CFeatures_1a3f98caf024a0a4713f5201f44b71dcd6)`(`[`EFeatureClass`](#namespaceshogun_1a9e2a4d8b86b9e061779c3fdbcda57c3b)` rhs) const` | Given a class in right hand side, does this class support compatible computation?
`public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CFeatures_1ad3711d9770e4b96ae8e89a99c9f530f7)`(const `[`Tag`](#classshogun_1_1Tag)`< T > & _tag,const T & value)` | Throws an error, as features are immutable
`public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CSGObject_1ade486add69a3fb33395968d9ad8fc4be)`(const std::string & name,T * value)` | Typed setter for an object class parameter of a [Shogun](#classShogun) base class type, identified by a name.
`public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CSGObject_1a7c9acb98546f6fab79715f3c151b0de4)`(const std::string & name,`[`Some`](#classshogun_1_1Some)`< T > value)` | Typed setter for an object class parameter of a [Shogun](#classShogun) base class type, identified by a name.
`public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CSGObject_1a21240124c06dd6296b254555e15cbf2d)`(const std::string & name,T value)` | Typed setter for a non-object class parameter, identified by a name.
`public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`shallow_subset_copy`](#classshogun_1_1CFeatures_1a896eb199c1413950bbf9a89226817fb4)`()` | 
`public int32_t `[`ref`](#classshogun_1_1CSGObject_1ab8c24b912ee57d3f2c81ecccd083582a)`()` | increase reference counter
`public int32_t `[`ref_count`](#classshogun_1_1CSGObject_1a6401d138f63be4c245f1f556f197689d)`()` | display reference counter
`public int32_t `[`unref`](#classshogun_1_1CSGObject_1ad99bde1a142a1c07a963169123166e01)`()` | decrement reference counter and deallocate object if refcount is zero before or after decrementing it
`public virtual `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`shallow_copy`](#classshogun_1_1CSGObject_1a3a25f61e5062adfce5df46be45e7e8c4)`() const` | A shallow copy. All the SGObject instance variables will be simply assigned and SG_REF-ed.
`public virtual `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`deep_copy`](#classshogun_1_1CSGObject_1afa9949a366159a39ab8118918b57f578)`() const` | A deep copy. All the instance variables will also be copied.
`public const char * `[`get_name`](#classshogun_1_1CSGObject_1a471caa9005cc581cb4514c0705b698ee)`() const` | Returns the name of the SGSerializable instance. It MUST BE the CLASS NAME without the prefixed `C'.
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
`protected bool `[`has_labels`](#classshogun_1_1CStreamingFeatures_1aeb8d0e6cf988582c5c1fd1066c3de27d) | Whether examples are labelled or not.
`protected `[`CStreamingFile`](#classshogun_1_1CStreamingFile)` * `[`working_file`](#classshogun_1_1CStreamingFeatures_1a831025a603a2f50724631b856c81b507) | The StreamingFile object to read from.
`protected bool `[`seekable`](#classshogun_1_1CStreamingFeatures_1a67ff96bae5b692656f9361d69cf70bc2) | Whether the stream is seekable.
`protected `[`CSubsetStack`](#classshogun_1_1CSubsetStack)` * `[`m_subset_stack`](#classshogun_1_1CFeatures_1ac406fc1620ad5a8714a1c34c935ae328) | subset used for index transformations
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

#### `public  `[`CStreamingFeatures`](#classshogun_1_1CStreamingFeatures_1a999e580c8a87f0d2dcc3c3398d00db52)`()` {#classshogun_1_1CStreamingFeatures_1a999e580c8a87f0d2dcc3c3398d00db52}

Default constructor with no args. Doesn't do anything yet.

#### `public  `[`CStreamingFeatures`](#classshogun_1_1CStreamingFeatures_1ac16fb744fbc2f13aec01b235e481ca66)`(const `[`CStreamingFeatures`](#classshogun_1_1CStreamingFeatures)` &) = delete` {#classshogun_1_1CStreamingFeatures_1ac16fb744fbc2f13aec01b235e481ca66}

#### `public virtual  `[`~CStreamingFeatures`](#classshogun_1_1CStreamingFeatures_1aa59ab1267b2e9196a485664c2e0ca220)`()` {#classshogun_1_1CStreamingFeatures_1aa59ab1267b2e9196a485664c2e0ca220}

Destructor

#### `public void `[`set_read_functions`](#classshogun_1_1CStreamingFeatures_1a4fbbbc398671e657437fdf37d59489d1)`()` {#classshogun_1_1CStreamingFeatures_1a4fbbbc398671e657437fdf37d59489d1}

Set the vector reading functions.

The functions are implemented specific to the type in the derived class.

#### `public void `[`set_vector_reader`](#classshogun_1_1CStreamingFeatures_1ade9a2fd19ebf69e179df3aaa3e4046a4)`()` {#classshogun_1_1CStreamingFeatures_1ade9a2fd19ebf69e179df3aaa3e4046a4}

The derived object must set the function which will be used for reading one vector from the file. This function should be a member of the [CStreamingFile](#classshogun_1_1CStreamingFile) class.

See the implementation in StreamingDenseFeatures for details.

#### `public void `[`set_vector_and_label_reader`](#classshogun_1_1CStreamingFeatures_1ac42301c8736a4d9f9529d70d5eaec221)`()` {#classshogun_1_1CStreamingFeatures_1ac42301c8736a4d9f9529d70d5eaec221}

The derived object must set the function which will be used by the parser for reading one vector and label from the file. This function should be a member of the [CStreamingFile](#classshogun_1_1CStreamingFile) class.

See the implementation in StreamingDenseFeatures for details.

#### `public void `[`start_parser`](#classshogun_1_1CStreamingFeatures_1a63f7baa945e9f36edf871f72e35d0c6d)`()` {#classshogun_1_1CStreamingFeatures_1a63f7baa945e9f36edf871f72e35d0c6d}

Start the parser. It stores parsed examples from the input in a separate thread.

#### `public void `[`end_parser`](#classshogun_1_1CStreamingFeatures_1a4e8b525b2b76468755c1502d022b82e2)`()` {#classshogun_1_1CStreamingFeatures_1a4e8b525b2b76468755c1502d022b82e2}

End the parser. Wait for the parsing thread to complete.

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_label`](#classshogun_1_1CStreamingFeatures_1a7791fdff6c5424dd6a6d12faf9a283fb)`()` {#classshogun_1_1CStreamingFeatures_1a7791fdff6c5424dd6a6d12faf9a283fb}

Return the label of the current example.

Raise an error if the input has been specified as unlabelled.

#### Returns
Label (if labelled example)

#### `public bool `[`get_next_example`](#classshogun_1_1CStreamingFeatures_1acbf87bddb7fb5c23d0fd50f2c999aee5)`()` {#classshogun_1_1CStreamingFeatures_1acbf87bddb7fb5c23d0fd50f2c999aee5}

Indicate to the parser that it must fetch the next example.

#### Returns
true on success, false on failure (i.e., no more examples).

#### `public void `[`release_example`](#classshogun_1_1CStreamingFeatures_1a6221e49be7a20336dc65996aa43f2721)`()` {#classshogun_1_1CStreamingFeatures_1a6221e49be7a20336dc65996aa43f2721}

Indicate that processing of the current example is done. The parser then considers it safe to dispose of that example and replace it with another one.

#### `public int32_t `[`get_num_features`](#classshogun_1_1CStreamingFeatures_1a820c06a0720897ec49ca0a87bd6851f8)`()` {#classshogun_1_1CStreamingFeatures_1a820c06a0720897ec49ca0a87bd6851f8}

Get the number of features in the current example.

#### Returns
number of features in current example

#### `public virtual bool `[`get_has_labels`](#classshogun_1_1CStreamingFeatures_1ad3bf3f11810ab28653b01a20a08afe22)`()` {#classshogun_1_1CStreamingFeatures_1ad3bf3f11810ab28653b01a20a08afe22}

Return whether the examples are labelled or not.

#### Returns
true if labelled, else false

#### `public virtual bool `[`is_seekable`](#classshogun_1_1CStreamingFeatures_1a18cbb4c042cbc4a268d13d4487620914)`()` {#classshogun_1_1CStreamingFeatures_1a18cbb4c042cbc4a268d13d4487620914}

Whether the stream is seekable (to check if multiple epochs are possible), i.e., whether we can process examples in a batch fashion.

A stream can usually seekable when it comes from a file or when it comes from another conventional [CFeatures](#classshogun_1_1CFeatures) object.

#### Returns
true if seekable, else false.

#### `public virtual void `[`reset_stream`](#classshogun_1_1CStreamingFeatures_1ae43311be283c1e503ac4ac4791db4922)`()` {#classshogun_1_1CStreamingFeatures_1ae43311be283c1e503ac4ac4791db4922}

Function to reset the stream (if possible).

#### `public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`get_streamed_features`](#classshogun_1_1CStreamingFeatures_1a28a9485cfe9d295474555b512aa554ae)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_elements)` {#classshogun_1_1CStreamingFeatures_1a28a9485cfe9d295474555b512aa554ae}

Returns a new [CFeatures](#classshogun_1_1CFeatures) instance which contains num_elements elements from the underlying stream. Not SG_REF'ed

#### Parameters
* `num_elements` num elements to save from stream 

#### Returns
[CFeatures](#classshogun_1_1CFeatures) object of underlying type, might be smaller than requested if the stream stopped. A warning is issued in this case.

NOT IMPLEMENTED!

#### `public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`duplicate`](#classshogun_1_1CStreamingFeatures_1a1af3e52183eff1d8dd311d55ce2eadb1)`() const` {#classshogun_1_1CStreamingFeatures_1a1af3e52183eff1d8dd311d55ce2eadb1}

Duplicate the object.

#### Returns
a duplicate object as CFeatures*

#### `public `[`EFeatureType`](#namespaceshogun_1a064eec90e91f56435546d77f38c0b618)` `[`get_feature_type`](#classshogun_1_1CFeatures_1a1a59079da3a831192228507e5945c78b)`() const` {#classshogun_1_1CFeatures_1a1a59079da3a831192228507e5945c78b}

get feature type

abstract base method

#### Returns
templated feature type

#### `public `[`EFeatureClass`](#namespaceshogun_1a9e2a4d8b86b9e061779c3fdbcda57c3b)` `[`get_feature_class`](#classshogun_1_1CFeatures_1a613776af659954ebda6aa77a274b1a1e)`() const` {#classshogun_1_1CFeatures_1a613776af659954ebda6aa77a274b1a1e}

get feature class

abstract base method

#### Returns
feature class like STRING, SIMPLE, SPARSE...

#### `public inline virtual `[`Range`](#classshogun_1_1Range)`< int32_t > `[`index_iterator`](#classshogun_1_1CFeatures_1a71bb6f4167a24d55e8e12fca77baabcd)`() const` {#classshogun_1_1CFeatures_1a71bb6f4167a24d55e8e12fca77baabcd}

returns an iterator of indices from 0 to [CFeatures::get_num_vectors](#classshogun_1_1CFeatures_1a91f8bf82dad4bb05accdc606d85a0da3)

Should be used in algorithms in the following way: 
```cpp
for (auto idx : features->index_iterator()) { ... }
```

#### `public virtual void `[`add_preprocessor`](#classshogun_1_1CFeatures_1a53d5b6b17d8e4b44117d404b119faca6)`(`[`CPreprocessor`](#classshogun_1_1CPreprocessor)` * p)` {#classshogun_1_1CFeatures_1a53d5b6b17d8e4b44117d404b119faca6}

add preprocessor

#### Parameters
* `p` preprocessor to set

#### `public virtual void `[`del_preprocessor`](#classshogun_1_1CFeatures_1af2ad4fb4c64ea892dc73a288f1be27a2)`(int32_t num)` {#classshogun_1_1CFeatures_1af2ad4fb4c64ea892dc73a288f1be27a2}

delete preprocessor from list

#### Parameters
* `num` index of preprocessor in list

#### `public `[`CPreprocessor`](#classshogun_1_1CPreprocessor)` * `[`get_preprocessor`](#classshogun_1_1CFeatures_1a16a2c185a1d7059892ef6ffb2d09f19b)`(int32_t num) const` {#classshogun_1_1CFeatures_1a16a2c185a1d7059892ef6ffb2d09f19b}

get specified preprocessor

#### Parameters
* `num` index of preprocessor in list

#### `public int32_t `[`get_num_preprocessors`](#classshogun_1_1CFeatures_1aa1b9b05b4535ba2c8c888aa107321c54)`() const` {#classshogun_1_1CFeatures_1aa1b9b05b4535ba2c8c888aa107321c54}

get number of preprocessors

#### Returns
number of preprocessors

#### `public void `[`clean_preprocessors`](#classshogun_1_1CFeatures_1aa6b20826d18617fc3bc0482c73908fb2)`()` {#classshogun_1_1CFeatures_1aa6b20826d18617fc3bc0482c73908fb2}

clears all preprocs

#### `public void `[`list_preprocessors`](#classshogun_1_1CFeatures_1a476493a28014c60a6006106f3d846147)`()` {#classshogun_1_1CFeatures_1a476493a28014c60a6006106f3d846147}

print preprocessors

#### `public int32_t `[`get_cache_size`](#classshogun_1_1CFeatures_1a6b599085eff3dab5a66cce6f133ae47e)`() const` {#classshogun_1_1CFeatures_1a6b599085eff3dab5a66cce6f133ae47e}

get cache size

#### Returns
cache size

#### `public int32_t `[`get_num_vectors`](#classshogun_1_1CFeatures_1a91f8bf82dad4bb05accdc606d85a0da3)`() const` {#classshogun_1_1CFeatures_1a91f8bf82dad4bb05accdc606d85a0da3}

get number of examples/vectors, possibly corresponding to the current subset

abstract base method

#### Returns
number of examples/vectors (possibly of subset, if implemented)

#### `public virtual bool `[`reshape`](#classshogun_1_1CFeatures_1ad2a12e099e61e61e3872253a13cc0287)`(int32_t num_features,int32_t num_vectors)` {#classshogun_1_1CFeatures_1ad2a12e099e61e61e3872253a13cc0287}

in case there is a feature matrix allow for reshaping

NOT IMPLEMENTED!

#### Parameters
* `num_features` new number of features 

* `num_vectors` new number of vectors 

#### Returns
if reshaping was successful

#### `public void `[`list_feature_obj`](#classshogun_1_1CFeatures_1aff469383824e5b8736c191cd4e4476b7)`() const` {#classshogun_1_1CFeatures_1aff469383824e5b8736c191cd4e4476b7}

list feature object

#### `public virtual void `[`load`](#classshogun_1_1CFeatures_1a5d33ec59a4be25056cca1f3b6691ad00)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` {#classshogun_1_1CFeatures_1a5d33ec59a4be25056cca1f3b6691ad00}

load features from file

#### Parameters
* `loader` File object via which data shall be loaded

#### `public virtual void `[`save`](#classshogun_1_1CFeatures_1a2ec11d78c7f60dfbc77bc2f56d211033)`(`[`CFile`](#classshogun_1_1CFile)` * writer)` {#classshogun_1_1CFeatures_1a2ec11d78c7f60dfbc77bc2f56d211033}

save features to file

#### Parameters
* `writer` File object via which data shall be saved

#### `public bool `[`check_feature_compatibility`](#classshogun_1_1CFeatures_1a7fe9c8b9c4e4474b1893f837ea29fa21)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * f) const` {#classshogun_1_1CFeatures_1a7fe9c8b9c4e4474b1893f837ea29fa21}

check feature compatibility

#### Parameters
* `f` features to check for compatibility 

#### Returns
if features are compatible

#### `public bool `[`has_property`](#classshogun_1_1CFeatures_1af181de39b142f32c3bb00a19bea32bcc)`(`[`EFeatureProperty`](#namespaceshogun_1add4a728b32cf3898a63b2ef4564c1925)` p) const` {#classshogun_1_1CFeatures_1af181de39b142f32c3bb00a19bea32bcc}

check if features have given property

#### Parameters
* `p` feature property 

#### Returns
if features have given property

#### `public void `[`set_property`](#classshogun_1_1CFeatures_1a732ec5df91b2d7d80ae25a79fe068055)`(`[`EFeatureProperty`](#namespaceshogun_1add4a728b32cf3898a63b2ef4564c1925)` p)` {#classshogun_1_1CFeatures_1a732ec5df91b2d7d80ae25a79fe068055}

set property

#### Parameters
* `p` kernel property to set

#### `public void `[`unset_property`](#classshogun_1_1CFeatures_1affaad72e745ecc61e93d676d78705b1e)`(`[`EFeatureProperty`](#namespaceshogun_1add4a728b32cf3898a63b2ef4564c1925)` p)` {#classshogun_1_1CFeatures_1affaad72e745ecc61e93d676d78705b1e}

unset property

#### Parameters
* `p` kernel property to unset

#### `public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`create_merged_copy`](#classshogun_1_1CFeatures_1abba142f59793094f4f324787d43e0b4e)`(`[`CList`](#classshogun_1_1CList)` * others) const` {#classshogun_1_1CFeatures_1abba142f59793094f4f324787d43e0b4e}

Takes a list of feature instances and returns a new instance being a concatenation of a copy of this instace's data and the given instancess data. Note that the feature types have to be equal.

NOT IMPLEMENTED!

#### Parameters
* `others` list of feature objects to append 

#### Returns
new feature object which contains copy of data of this instance and given ones

#### `public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`create_merged_copy`](#classshogun_1_1CFeatures_1aef378f04b4eb3b6a21752a5400260769)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * other) const` {#classshogun_1_1CFeatures_1aef378f04b4eb3b6a21752a5400260769}

Convenience method for method with same name and list as parameter.

NOT IMPLEMENTED!

#### Parameters
* `other` feature object to append 

#### Returns
new feature object which contains copy of data of this instance and of given one

#### `public virtual void `[`add_subset`](#classshogun_1_1CFeatures_1acb58d8008e2ef9bb83e6b5fc5fb42f71)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > subset)` {#classshogun_1_1CFeatures_1acb58d8008e2ef9bb83e6b5fc5fb42f71}

Adds a subset of indices on top of the current subsets (possibly subset of subset). Every call causes a new active index vector to be stored. Added subsets can be removed one-by-one. If this is not needed, [add_subset_in_place()](#classshogun_1_1CFeatures_1a6dabbf53b34ca64a7645191b8ea04e31) should be used (does not store intermediate index vectors)

Calls [subset_changed_post()](#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7) afterwards

#### Parameters
* `subset` subset of indices to add

#### `public virtual void `[`add_subset_in_place`](#classshogun_1_1CFeatures_1a6dabbf53b34ca64a7645191b8ea04e31)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > subset)` {#classshogun_1_1CFeatures_1a6dabbf53b34ca64a7645191b8ea04e31}

Sets/changes latest added subset. This allows to add multiple subsets with in-place memory requirements. They cannot be removed one-by-one afterwards, only the latest active can. If this is needed, use [add_subset()](#classshogun_1_1CFeatures_1acb58d8008e2ef9bb83e6b5fc5fb42f71). If no subset is active, this just adds.

Calls [subset_changed_post()](#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7) afterwards

#### Parameters
* `subset` subset of indices to replace the latest one with.

#### `public virtual void `[`remove_subset`](#classshogun_1_1CFeatures_1a5c8a113b96b3d3a2d565ed9fffeed172)`()` {#classshogun_1_1CFeatures_1a5c8a113b96b3d3a2d565ed9fffeed172}

removes that last added subset from subset stack, if existing Calls [subset_changed_post()](#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7) afterwards

#### `public virtual void `[`remove_all_subsets`](#classshogun_1_1CFeatures_1a434b4feb76767ed0adc9ccdd55a3ef61)`()` {#classshogun_1_1CFeatures_1a434b4feb76767ed0adc9ccdd55a3ef61}

removes all subsets Calls [subset_changed_post()](#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7) afterwards

#### `public virtual `[`CSubsetStack`](#classshogun_1_1CSubsetStack)` * `[`get_subset_stack`](#classshogun_1_1CFeatures_1a47944f23a63a0eed56ff3d0bba40d253)`()` {#classshogun_1_1CFeatures_1a47944f23a63a0eed56ff3d0bba40d253}

returns subset stack

#### Returns
subset stack

#### `public inline virtual void `[`subset_changed_post`](#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7)`()` {#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7}

method may be overwritten to update things that depend on subset

#### `public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`copy_subset`](#classshogun_1_1CFeatures_1adf4a1baaff0c06456ceca3b217c46338)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CFeatures_1adf4a1baaff0c06456ceca3b217c46338}

Creates a new [CFeatures](#classshogun_1_1CFeatures) instance containing copies of the elements which are specified by the provided indices.

This method is needed for a KernelMachine to store its model data. NOT IMPLEMENTED!

#### Parameters
* `indices` indices of feature elements to copy 

#### Returns
new [CFeatures](#classshogun_1_1CFeatures) instance with copies of feature data

#### `public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`copy_dimension_subset`](#classshogun_1_1CFeatures_1ab5e4da6272e74503f9ac4405d8ac92b5)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > dims)` {#classshogun_1_1CFeatures_1ab5e4da6272e74503f9ac4405d8ac92b5}

Creates a new [CFeatures](#classshogun_1_1CFeatures) instance containing only the dimensions of the feature vector which are specified by the provided indices.

This method is needed for feature selection tasks NOT IMPLEMENTED!

#### Parameters
* `dims` indices of feature dimensions to copy 

#### Returns
new [CFeatures](#classshogun_1_1CFeatures) instance with copies of specified features

#### `public inline virtual bool `[`support_compatible_class`](#classshogun_1_1CFeatures_1a0e8af4cc2f64bde8fe2b3dd4557e9a4f)`() const` {#classshogun_1_1CFeatures_1a0e8af4cc2f64bde8fe2b3dd4557e9a4f}

does this class support compatible computation bewteen difference classes? for example, this->dot(rhs_prt), can rhs_prt be an instance of a difference class?

#### Returns
whether this class supports compatible computation

#### `public virtual bool `[`get_feature_class_compatibility`](#classshogun_1_1CFeatures_1a3f98caf024a0a4713f5201f44b71dcd6)`(`[`EFeatureClass`](#namespaceshogun_1a9e2a4d8b86b9e061779c3fdbcda57c3b)` rhs) const` {#classshogun_1_1CFeatures_1a3f98caf024a0a4713f5201f44b71dcd6}

Given a class in right hand side, does this class support compatible computation?

for example, is this->dot(rhs_prt) valid, where rhs_prt is the class in right hand side

#### Parameters
* `rhs` the class in right hand side 

#### Returns
whether this class supports compatible computation

#### `public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CFeatures_1ad3711d9770e4b96ae8e89a99c9f530f7)`(const `[`Tag`](#classshogun_1_1Tag)`< T > & _tag,const T & value)` {#classshogun_1_1CFeatures_1ad3711d9770e4b96ae8e89a99c9f530f7}

Throws an error, as features are immutable

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

#### `public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`shallow_subset_copy`](#classshogun_1_1CFeatures_1a896eb199c1413950bbf9a89226817fb4)`()` {#classshogun_1_1CFeatures_1a896eb199c1413950bbf9a89226817fb4}

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

#### `public const char * `[`get_name`](#classshogun_1_1CSGObject_1a471caa9005cc581cb4514c0705b698ee)`() const` {#classshogun_1_1CSGObject_1a471caa9005cc581cb4514c0705b698ee}

Returns the name of the SGSerializable instance. It MUST BE the CLASS NAME without the prefixed `C'.

#### Returns
name of the SGSerializable

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

#### `protected bool `[`has_labels`](#classshogun_1_1CStreamingFeatures_1aeb8d0e6cf988582c5c1fd1066c3de27d) {#classshogun_1_1CStreamingFeatures_1aeb8d0e6cf988582c5c1fd1066c3de27d}

Whether examples are labelled or not.

#### `protected `[`CStreamingFile`](#classshogun_1_1CStreamingFile)` * `[`working_file`](#classshogun_1_1CStreamingFeatures_1a831025a603a2f50724631b856c81b507) {#classshogun_1_1CStreamingFeatures_1a831025a603a2f50724631b856c81b507}

The StreamingFile object to read from.

#### `protected bool `[`seekable`](#classshogun_1_1CStreamingFeatures_1a67ff96bae5b692656f9361d69cf70bc2) {#classshogun_1_1CStreamingFeatures_1a67ff96bae5b692656f9361d69cf70bc2}

Whether the stream is seekable.

#### `protected `[`CSubsetStack`](#classshogun_1_1CSubsetStack)` * `[`m_subset_stack`](#classshogun_1_1CFeatures_1ac406fc1620ad5a8714a1c34c935ae328) {#classshogun_1_1CFeatures_1ac406fc1620ad5a8714a1c34c935ae328}

subset used for index transformations

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

