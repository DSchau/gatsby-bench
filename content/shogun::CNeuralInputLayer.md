---
classname: "shogun::CNeuralInputLayer"
type: "class"
parents:
   - CNeuralLayer
---

# class `shogun::CNeuralInputLayer` {#classshogun_1_1CNeuralInputLayer}

```
class shogun::CNeuralInputLayer
  : public CNeuralLayer
```

Represents an input layer. The layer can be either connected to all the input features that a network receives (default) or connected to just a small part of those features.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`gaussian_noise`](#classshogun_1_1CNeuralInputLayer_1a88fa12e98aa653cd963c019e89f2a8e7) | Standard deviation of the gaussian noise added to the activations of the layer. Useful for denoising autoencoders. Default value is 0.0.
`public bool `[`is_training`](#classshogun_1_1CNeuralLayer_1a673c291a9195d1de6147e5e9a97ca633) | Should be true if the layer is currently used during training initial value is false
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`dropout_prop`](#classshogun_1_1CNeuralLayer_1ac03a059a28d2b7be607fb21437c18363) | probabilty of dropping out a neuron in the layer
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`contraction_coefficient`](#classshogun_1_1CNeuralLayer_1acd6991c39faf537d39a4caffe6432104) | For hidden layers in a contractive autoencoders [Rifai, 2011] a term: 
`public `[`ENLAutoencoderPosition`](#namespaceshogun_1aedb2adb9649185615d1a620bdd8d8164)` `[`autoencoder_position`](#classshogun_1_1CNeuralLayer_1af4af7d506b318956ec87b906e87c0152) | For autoencoders, specifies the position of the layer in the autoencoder, i.e an encoding layer or a decoding layer. Default value is NLAP_NONE
`public `[`SGIO`](#classshogun_1_1SGIO)` * `[`io`](#classshogun_1_1CSGObject_1ab3ff22f724961ace985100941ba0364d) | io
`public `[`Parallel`](#classshogun_1_1Parallel)` * `[`parallel`](#classshogun_1_1CSGObject_1a1401044636b5c2353226b974526302e9) | parallel
`public `[`Version`](#classshogun_1_1Version)` * `[`version`](#classshogun_1_1CSGObject_1afc25f30ab1a6d04798c360a2ce70b87d) | version
`public `[`Parameter`](#classshogun_1_1Parameter)` * `[`m_parameters`](#classshogun_1_1CSGObject_1a70e59038292e669701bad2af7715aa1e) | parameters
`public `[`Parameter`](#classshogun_1_1Parameter)` * `[`m_model_selection_parameters`](#classshogun_1_1CSGObject_1a113f5ae82840ac3f354f94456c10f59b) | model selection parameters
`public `[`Parameter`](#classshogun_1_1Parameter)` * `[`m_gradient_parameters`](#classshogun_1_1CSGObject_1ac3f51364b93830b9c9d991cb2d5801f4) | parameters wrt which we can compute gradients
`public uint32_t `[`m_hash`](#classshogun_1_1CSGObject_1a170f14be9561242f924939c56b372a41) | Hash of parameter values
`public  `[`CNeuralInputLayer`](#classshogun_1_1CNeuralInputLayer_1a48d1dcebb78e1461d0f0f4a8780ced76)`()` | default constructor
`public  `[`CNeuralInputLayer`](#classshogun_1_1CNeuralInputLayer_1ada501b1f909bd591db72ed62c9176ed5)`(int32_t num_neurons,int32_t start_index)` | Constuctor
`public  `[`CNeuralInputLayer`](#classshogun_1_1CNeuralInputLayer_1ad9d97db4551129e2620459fe088725c1)`(int32_t width,int32_t height,int32_t num_channels,int32_t start_index)` | Constructs an input layer that deals with images (for convolutional nets). Sets the number of neurons to width*height*num_channels
`public inline virtual  `[`~CNeuralInputLayer`](#classshogun_1_1CNeuralInputLayer_1adec3c670af089bf0bac02ee0ab0aabf7)`()` | 
`public inline virtual bool `[`is_input`](#classshogun_1_1CNeuralInputLayer_1acadc1f3fdee8bc3396d446b6ddff738e)`()` | Returns true
`public virtual void `[`compute_activations`](#classshogun_1_1CNeuralInputLayer_1a78c5c3b118f06a22cc048013b772d19b)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > inputs)` | Copies inputs[start_index:start_index+num_neurons, :] into the layer's activations
`public inline virtual int32_t `[`get_start_index`](#classshogun_1_1CNeuralInputLayer_1a12e9b233542d82882b7c16d8b7db0800)`()` | Gets the index of the first feature that the layer connects to, i.e the activations of the layer are copied from input_features[start_index:start_index+num_neurons]
`public inline virtual void `[`set_start_index`](#classshogun_1_1CNeuralInputLayer_1ac06ca8ac067b514c3d87992a4d0ef0b3)`(int32_t i)` | Sets the index of the first feature that the layer connects to, i.e the activations of the layer are copied from input_features[start_index:start_index+num_neurons]
`public inline virtual const char * `[`get_name`](#classshogun_1_1CNeuralInputLayer_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` | Returns the name of the SGSerializable instance. It MUST BE the CLASS NAME without the prefixed `C'.
`public virtual void `[`initialize_neural_layer`](#classshogun_1_1CNeuralLayer_1a55a59cd2d580c56225e343e635d9b00c)`(`[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` * layers,`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > input_indices)` | Initializes the layer
`public virtual void `[`set_batch_size`](#classshogun_1_1CNeuralLayer_1a2fb212dd86732ebf70f0a692257422d5)`(int32_t batch_size)` | Sets the batch_size and allocates memory for m_activations and m_input_gradients accordingly. Must be called before forward or backward propagation is performed
`public inline virtual void `[`initialize_parameters`](#classshogun_1_1CNeuralLayer_1aeab208d7ec218f6985f122c9640e300e)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > parameters,`[`SGVector`](#classshogun_1_1SGVector)`< bool > parameter_regularizable,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` sigma)` | Initializes the layer's parameters. The layer should fill the given arrays with the initial value for its parameters
`public inline virtual void `[`compute_activations`](#classshogun_1_1CNeuralLayer_1afee6abbe964ac762eb7c3b10a0d89fe6)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > parameters,`[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` * layers)` | Computes the activations of the neurons in this layer, results should be stored in m_activations. To be used only with non-input layers
`public inline virtual void `[`compute_gradients`](#classshogun_1_1CNeuralLayer_1aa3f49deb9f619d0374bbecf8492b32f4)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > parameters,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > targets,`[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` * layers,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > parameter_gradients)` | Computes the gradients that are relevent to this layer:
`public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_error`](#classshogun_1_1CNeuralLayer_1a7d5c51c4f61aa9ddc26bb60f1f69cc06)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > targets)` | Computes the error between the layer's current activations and the given target activations. Should only be used with output layers
`public inline virtual void `[`enforce_max_norm`](#classshogun_1_1CNeuralLayer_1a9fdf9a256c468ef5302955dd9cb8331a)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > parameters,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` max_norm)` | Constrains the weights of each neuron in the layer to have an L2 norm of at most max_norm
`public virtual void `[`dropout_activations`](#classshogun_1_1CNeuralLayer_1a49fb31f58ffac6c3d704eeaac21d36d6)`()` | Applies [dropout]([http://arxiv.org/abs/1207.0580](http://arxiv.org/abs/1207.0580)) [Hinton, 2012] to the activations of the layer
`public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_contraction_term`](#classshogun_1_1CNeuralLayer_1a816831519314f4ea3be402f60410daa3)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > parameters)` | Computes 
`public inline virtual int32_t `[`get_num_neurons`](#classshogun_1_1CNeuralLayer_1adfb5e980c98768b760e1e6ba4f95bc8e)`()` | Gets the number of neurons in the layer
`public inline virtual int32_t `[`get_width`](#classshogun_1_1CNeuralLayer_1ac5a77d98ea975bdb5ad41db79311cd50)`()` | Returns the width assuming that the layer's activations are interpreted as images (i.e for convolutional nets)
`public inline virtual int32_t `[`get_height`](#classshogun_1_1CNeuralLayer_1a505afb8a93a20d1e1d3ad6327ce5d1a8)`()` | Returns the height assuming that the layer's activations are interpreted as images (i.e for convolutional nets)
`public inline virtual void `[`set_num_neurons`](#classshogun_1_1CNeuralLayer_1aeba0ddbdc7dd358bf2f1cadf8f8fa5a8)`(int32_t num_neurons)` | Gets the number of neurons in the layer
`public inline virtual int32_t `[`get_num_parameters`](#classshogun_1_1CNeuralLayer_1a281773525d07066cd375200e4e9b0343)`()` | Gets the number of parameters used in this layer
`public inline virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_activations`](#classshogun_1_1CNeuralLayer_1a0b8dc65e6da47651bbaaa938e676ef6f)`()` | Gets the layer's activations, a matrix of size num_neurons * batch_size
`public inline virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_activation_gradients`](#classshogun_1_1CNeuralLayer_1ac23a17bde04fbf9f1a3b44e225e2addf)`()` | Gets the layer's activation gradients, a matrix of size num_neurons * batch_size
`public inline virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_local_gradients`](#classshogun_1_1CNeuralLayer_1aa2a397251220515c59032fabf213a3c7)`()` | Gets the layer's local gradients, a matrix of size num_neurons * batch_size
`public inline virtual `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`get_input_indices`](#classshogun_1_1CNeuralLayer_1a2bf582d5c501b10e8fdae0e9f2200e38)`()` | Gets the indices of the layers that are connected to this layer as input
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
`protected int32_t `[`m_start_index`](#classshogun_1_1CNeuralInputLayer_1aef18ee2e03fd85f83b759e428701f195) | Index of the first feature that the layer connects to, i.e the activations of the layer are copied from input_features[start_index:start_index+num_neurons]
`protected int32_t `[`m_num_neurons`](#classshogun_1_1CNeuralLayer_1ac9d797779840389c391816066b3f169b) | Number of neurons in this layer
`protected int32_t `[`m_width`](#classshogun_1_1CNeuralLayer_1a417f1165d2192cca456a2c623a38da73) | Width of the image (if the layer's activations are to be interpreted as images. Default value is m_num_neurons
`protected int32_t `[`m_height`](#classshogun_1_1CNeuralLayer_1a32e992b500cf0cd4c428e143a4bbbcb6) | Width of the image (if the layer's activations are to be interpreted as images. Default value is 1
`protected int32_t `[`m_num_parameters`](#classshogun_1_1CNeuralLayer_1ad081072081024ddc9d49e590184edb60) | Number of neurons in this layer
`protected `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`m_input_indices`](#classshogun_1_1CNeuralLayer_1ae49d0c18d6db0c36a46ecbef46ccf0cd) | Indices of the layers that are connected to this layer as input
`protected `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`m_input_sizes`](#classshogun_1_1CNeuralLayer_1ae4e78aaf0de4f121c130918ed58d0338) | Number of neurons in the layers that are connected to this layer as input
`protected int32_t `[`m_batch_size`](#classshogun_1_1CNeuralLayer_1acb2482e04fe13be6830ef0128acd4f68) | number of training/test cases the network is currently working with
`protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_activations`](#classshogun_1_1CNeuralLayer_1a5ec119fbcb9d66196a7ee474afc3ee2c) | activations of the neurons in this layer size num_neurons * batch_size
`protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_activation_gradients`](#classshogun_1_1CNeuralLayer_1a026290f025b7f011db95150c2c1f00c1) | gradients of the error with respect to the layer's inputs size previous_layer_num_neurons * batch_size
`protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_local_gradients`](#classshogun_1_1CNeuralLayer_1a96bf7ad8d3a5e27f2945dd37b2b16812) | gradients of the error with respect to the layer's pre-activations, this is usually used as a buffer when computing the input gradients size num_neurons * batch_size
`protected `[`SGMatrix`](#classshogun_1_1SGMatrix)`< bool > `[`m_dropout_mask`](#classshogun_1_1CNeuralLayer_1ab43cbe318297728b3ccaa9c20c849012) | binary mask that determines whether a neuron will be kept or dropped out during the current iteration of training size num_neurons * batch_size
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

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`gaussian_noise`](#classshogun_1_1CNeuralInputLayer_1a88fa12e98aa653cd963c019e89f2a8e7) {#classshogun_1_1CNeuralInputLayer_1a88fa12e98aa653cd963c019e89f2a8e7}

Standard deviation of the gaussian noise added to the activations of the layer. Useful for denoising autoencoders. Default value is 0.0.

#### `public bool `[`is_training`](#classshogun_1_1CNeuralLayer_1a673c291a9195d1de6147e5e9a97ca633) {#classshogun_1_1CNeuralLayer_1a673c291a9195d1de6147e5e9a97ca633}

Should be true if the layer is currently used during training initial value is false

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`dropout_prop`](#classshogun_1_1CNeuralLayer_1ac03a059a28d2b7be607fb21437c18363) {#classshogun_1_1CNeuralLayer_1ac03a059a28d2b7be607fb21437c18363}

probabilty of dropping out a neuron in the layer

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`contraction_coefficient`](#classshogun_1_1CNeuralLayer_1acd6991c39faf537d39a4caffe6432104) {#classshogun_1_1CNeuralLayer_1acd6991c39faf537d39a4caffe6432104}

For hidden layers in a contractive autoencoders [Rifai, 2011] a term: 
$$
\frac{\lambda}{N} \sum_{k=0}^{N-1} \left \| J(x_k) \right \|^2_F
$$
 is added to the error, where $ \left \| J(x_k)) \right \|^2_F $ is the Frobenius norm of the Jacobian of the activations of the hidden layer with respect to its inputs, $ N $ is the batch size, and $ \lambda $ is the contraction coefficient.

Default value is 0.0.

#### `public `[`ENLAutoencoderPosition`](#namespaceshogun_1aedb2adb9649185615d1a620bdd8d8164)` `[`autoencoder_position`](#classshogun_1_1CNeuralLayer_1af4af7d506b318956ec87b906e87c0152) {#classshogun_1_1CNeuralLayer_1af4af7d506b318956ec87b906e87c0152}

For autoencoders, specifies the position of the layer in the autoencoder, i.e an encoding layer or a decoding layer. Default value is NLAP_NONE

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

#### `public  `[`CNeuralInputLayer`](#classshogun_1_1CNeuralInputLayer_1a48d1dcebb78e1461d0f0f4a8780ced76)`()` {#classshogun_1_1CNeuralInputLayer_1a48d1dcebb78e1461d0f0f4a8780ced76}

default constructor

#### `public  `[`CNeuralInputLayer`](#classshogun_1_1CNeuralInputLayer_1ada501b1f909bd591db72ed62c9176ed5)`(int32_t num_neurons,int32_t start_index)` {#classshogun_1_1CNeuralInputLayer_1ada501b1f909bd591db72ed62c9176ed5}

Constuctor

#### Parameters
* `num_neurons` Number of neurons in this layer

* `start_index` Index of the first feature that the layer connects to, i.e the activations of the layer are copied from input_features[start_index:start_index+num_neurons]

#### `public  `[`CNeuralInputLayer`](#classshogun_1_1CNeuralInputLayer_1ad9d97db4551129e2620459fe088725c1)`(int32_t width,int32_t height,int32_t num_channels,int32_t start_index)` {#classshogun_1_1CNeuralInputLayer_1ad9d97db4551129e2620459fe088725c1}

Constructs an input layer that deals with images (for convolutional nets). Sets the number of neurons to width*height*num_channels

#### Parameters
* `width` Width of the image

* `height` Width of the image

* `num_channels` Number of channels

* `start_index` Index of the first feature that the layer connects to, i.e the activations of the layer are copied from input_features[start_index:start_index+num_neurons]

#### `public inline virtual  `[`~CNeuralInputLayer`](#classshogun_1_1CNeuralInputLayer_1adec3c670af089bf0bac02ee0ab0aabf7)`()` {#classshogun_1_1CNeuralInputLayer_1adec3c670af089bf0bac02ee0ab0aabf7}

#### `public inline virtual bool `[`is_input`](#classshogun_1_1CNeuralInputLayer_1acadc1f3fdee8bc3396d446b6ddff738e)`()` {#classshogun_1_1CNeuralInputLayer_1acadc1f3fdee8bc3396d446b6ddff738e}

Returns true

#### `public virtual void `[`compute_activations`](#classshogun_1_1CNeuralInputLayer_1a78c5c3b118f06a22cc048013b772d19b)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > inputs)` {#classshogun_1_1CNeuralInputLayer_1a78c5c3b118f06a22cc048013b772d19b}

Copies inputs[start_index:start_index+num_neurons, :] into the layer's activations

#### Parameters
* `inputs` Input features matrix, size num_features*num_cases

#### `public inline virtual int32_t `[`get_start_index`](#classshogun_1_1CNeuralInputLayer_1a12e9b233542d82882b7c16d8b7db0800)`()` {#classshogun_1_1CNeuralInputLayer_1a12e9b233542d82882b7c16d8b7db0800}

Gets the index of the first feature that the layer connects to, i.e the activations of the layer are copied from input_features[start_index:start_index+num_neurons]

#### `public inline virtual void `[`set_start_index`](#classshogun_1_1CNeuralInputLayer_1ac06ca8ac067b514c3d87992a4d0ef0b3)`(int32_t i)` {#classshogun_1_1CNeuralInputLayer_1ac06ca8ac067b514c3d87992a4d0ef0b3}

Sets the index of the first feature that the layer connects to, i.e the activations of the layer are copied from input_features[start_index:start_index+num_neurons]

#### `public inline virtual const char * `[`get_name`](#classshogun_1_1CNeuralInputLayer_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` {#classshogun_1_1CNeuralInputLayer_1a9cb485686dd7a1e6f7103cf42e87717e}

Returns the name of the SGSerializable instance. It MUST BE the CLASS NAME without the prefixed `C'.

#### Returns
name of the SGSerializable

#### `public virtual void `[`initialize_neural_layer`](#classshogun_1_1CNeuralLayer_1a55a59cd2d580c56225e343e635d9b00c)`(`[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` * layers,`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > input_indices)` {#classshogun_1_1CNeuralLayer_1a55a59cd2d580c56225e343e635d9b00c}

Initializes the layer

#### Parameters
* `layers` Array of layers that form the network that this layer is being used with

* `input_indices` Indices of the layers that are connected to this layer as input

#### `public virtual void `[`set_batch_size`](#classshogun_1_1CNeuralLayer_1a2fb212dd86732ebf70f0a692257422d5)`(int32_t batch_size)` {#classshogun_1_1CNeuralLayer_1a2fb212dd86732ebf70f0a692257422d5}

Sets the batch_size and allocates memory for m_activations and m_input_gradients accordingly. Must be called before forward or backward propagation is performed

#### Parameters
* `batch_size` number of training/test cases the network is currently working with

#### `public inline virtual void `[`initialize_parameters`](#classshogun_1_1CNeuralLayer_1aeab208d7ec218f6985f122c9640e300e)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > parameters,`[`SGVector`](#classshogun_1_1SGVector)`< bool > parameter_regularizable,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` sigma)` {#classshogun_1_1CNeuralLayer_1aeab208d7ec218f6985f122c9640e300e}

Initializes the layer's parameters. The layer should fill the given arrays with the initial value for its parameters

#### Parameters
* `parameters` Vector of size [get_num_parameters()](#classshogun_1_1CNeuralLayer_1a281773525d07066cd375200e4e9b0343)

* `parameter_regularizable` Vector of size [get_num_parameters()](#classshogun_1_1CNeuralLayer_1a281773525d07066cd375200e4e9b0343). This controls which of the layer's parameter are subject to regularization, i.e to turn off regularization for parameter i, set parameter_regularizable[i] = false. This is usally used to turn off regularization for bias parameters.

* `sigma` standard deviation of the gaussian used to random the parameters

#### `public inline virtual void `[`compute_activations`](#classshogun_1_1CNeuralLayer_1afee6abbe964ac762eb7c3b10a0d89fe6)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > parameters,`[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` * layers)` {#classshogun_1_1CNeuralLayer_1afee6abbe964ac762eb7c3b10a0d89fe6}

Computes the activations of the neurons in this layer, results should be stored in m_activations. To be used only with non-input layers

#### Parameters
* `parameters` Vector of size [get_num_parameters()](#classshogun_1_1CNeuralLayer_1a281773525d07066cd375200e4e9b0343), contains the parameters of the layer

* `layers` Array of layers that form the network that this layer is being used with

#### `public inline virtual void `[`compute_gradients`](#classshogun_1_1CNeuralLayer_1aa3f49deb9f619d0374bbecf8492b32f4)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > parameters,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > targets,`[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` * layers,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > parameter_gradients)` {#classshogun_1_1CNeuralLayer_1aa3f49deb9f619d0374bbecf8492b32f4}

Computes the gradients that are relevent to this layer:

* The gradients of the error with respect to the layer's parameters -The gradients of the error with respect to the layer's inputs

Input gradients for layer i that connects into this layer as input are added to m_layers.element(i).[get_activation_gradients()](#classshogun_1_1CNeuralLayer_1ac23a17bde04fbf9f1a3b44e225e2addf)

Deriving classes should make sure to account for [dropout]([http://arxiv.org/abs/1207.0580](http://arxiv.org/abs/1207.0580)) [Hinton, 2012] during gradient computations

Deriving classes should also account for contraction_coefficient if they can be used in as a hidden layer in a contractive autoencoder.

#### Parameters
* `parameters` Vector of size [get_num_parameters()](#classshogun_1_1CNeuralLayer_1a281773525d07066cd375200e4e9b0343), contains the parameters of the layer

* `targets` a matrix of size num_neurons*batch_size. If the layer is being used as an output layer, targets is the desired values for the layer's activations, otherwise it's an empty matrix

* `layers` Array of layers that form the network that this layer is being used with

* `parameter_gradients` Vector of size [get_num_parameters()](#classshogun_1_1CNeuralLayer_1a281773525d07066cd375200e4e9b0343). To be filled with gradients of the error with respect to each parameter of the layer

#### `public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_error`](#classshogun_1_1CNeuralLayer_1a7d5c51c4f61aa9ddc26bb60f1f69cc06)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > targets)` {#classshogun_1_1CNeuralLayer_1a7d5c51c4f61aa9ddc26bb60f1f69cc06}

Computes the error between the layer's current activations and the given target activations. Should only be used with output layers

#### Parameters
* `targets` desired values for the layer's activations, matrix of size num_neurons*batch_size

#### `public inline virtual void `[`enforce_max_norm`](#classshogun_1_1CNeuralLayer_1a9fdf9a256c468ef5302955dd9cb8331a)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > parameters,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` max_norm)` {#classshogun_1_1CNeuralLayer_1a9fdf9a256c468ef5302955dd9cb8331a}

Constrains the weights of each neuron in the layer to have an L2 norm of at most max_norm

#### Parameters
* `parameters` pointer to the layer's parameters, array of size [get_num_parameters()](#classshogun_1_1CNeuralLayer_1a281773525d07066cd375200e4e9b0343)

* `max_norm` maximum allowable norm for a neuron's weights

#### `public virtual void `[`dropout_activations`](#classshogun_1_1CNeuralLayer_1a49fb31f58ffac6c3d704eeaac21d36d6)`()` {#classshogun_1_1CNeuralLayer_1a49fb31f58ffac6c3d704eeaac21d36d6}

Applies [dropout]([http://arxiv.org/abs/1207.0580](http://arxiv.org/abs/1207.0580)) [Hinton, 2012] to the activations of the layer

If is_training is true, fills m_dropout_mask with random values (according to dropout_prop) and multiplies it into the activations, otherwise, multiplies the activations by (1-dropout_prop) to compensate for using dropout during training

#### `public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_contraction_term`](#classshogun_1_1CNeuralLayer_1a816831519314f4ea3be402f60410daa3)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > parameters)` {#classshogun_1_1CNeuralLayer_1a816831519314f4ea3be402f60410daa3}

Computes 
$$
\frac{\lambda}{N} \sum_{k=0}^{N-1} \left \| J(x_k) \right \|^2_F
$$
 where $ \left \| J(x_k)) \right \|^2_F $ is the Frobenius norm of the Jacobian of the activations of the hidden layer with respect to its inputs, $ N $ is the batch size, and $ \lambda $ is the contraction coefficient.

Should be implemented by layers that support being used as a hidden layer in a contractive autoencoder.

#### Parameters
* `parameters` Vector of size [get_num_parameters()](#classshogun_1_1CNeuralLayer_1a281773525d07066cd375200e4e9b0343), contains the parameters of the layer

#### `public inline virtual int32_t `[`get_num_neurons`](#classshogun_1_1CNeuralLayer_1adfb5e980c98768b760e1e6ba4f95bc8e)`()` {#classshogun_1_1CNeuralLayer_1adfb5e980c98768b760e1e6ba4f95bc8e}

Gets the number of neurons in the layer

#### Returns
number of neurons in the layer

#### `public inline virtual int32_t `[`get_width`](#classshogun_1_1CNeuralLayer_1ac5a77d98ea975bdb5ad41db79311cd50)`()` {#classshogun_1_1CNeuralLayer_1ac5a77d98ea975bdb5ad41db79311cd50}

Returns the width assuming that the layer's activations are interpreted as images (i.e for convolutional nets)

#### Returns
Width

#### `public inline virtual int32_t `[`get_height`](#classshogun_1_1CNeuralLayer_1a505afb8a93a20d1e1d3ad6327ce5d1a8)`()` {#classshogun_1_1CNeuralLayer_1a505afb8a93a20d1e1d3ad6327ce5d1a8}

Returns the height assuming that the layer's activations are interpreted as images (i.e for convolutional nets)

#### Returns
Height

#### `public inline virtual void `[`set_num_neurons`](#classshogun_1_1CNeuralLayer_1aeba0ddbdc7dd358bf2f1cadf8f8fa5a8)`(int32_t num_neurons)` {#classshogun_1_1CNeuralLayer_1aeba0ddbdc7dd358bf2f1cadf8f8fa5a8}

Gets the number of neurons in the layer

#### Parameters
* `num_neurons` number of neurons in the layer

#### `public inline virtual int32_t `[`get_num_parameters`](#classshogun_1_1CNeuralLayer_1a281773525d07066cd375200e4e9b0343)`()` {#classshogun_1_1CNeuralLayer_1a281773525d07066cd375200e4e9b0343}

Gets the number of parameters used in this layer

#### Returns
number of parameters used in this layer

#### `public inline virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_activations`](#classshogun_1_1CNeuralLayer_1a0b8dc65e6da47651bbaaa938e676ef6f)`()` {#classshogun_1_1CNeuralLayer_1a0b8dc65e6da47651bbaaa938e676ef6f}

Gets the layer's activations, a matrix of size num_neurons * batch_size

#### Returns
layer's activations

#### `public inline virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_activation_gradients`](#classshogun_1_1CNeuralLayer_1ac23a17bde04fbf9f1a3b44e225e2addf)`()` {#classshogun_1_1CNeuralLayer_1ac23a17bde04fbf9f1a3b44e225e2addf}

Gets the layer's activation gradients, a matrix of size num_neurons * batch_size

#### Returns
layer's activation gradients

#### `public inline virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_local_gradients`](#classshogun_1_1CNeuralLayer_1aa2a397251220515c59032fabf213a3c7)`()` {#classshogun_1_1CNeuralLayer_1aa2a397251220515c59032fabf213a3c7}

Gets the layer's local gradients, a matrix of size num_neurons * batch_size

#### Returns
layer's local gradients

#### `public inline virtual `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`get_input_indices`](#classshogun_1_1CNeuralLayer_1a2bf582d5c501b10e8fdae0e9f2200e38)`()` {#classshogun_1_1CNeuralLayer_1a2bf582d5c501b10e8fdae0e9f2200e38}

Gets the indices of the layers that are connected to this layer as input

#### Returns
layer's input indices

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

#### `protected int32_t `[`m_start_index`](#classshogun_1_1CNeuralInputLayer_1aef18ee2e03fd85f83b759e428701f195) {#classshogun_1_1CNeuralInputLayer_1aef18ee2e03fd85f83b759e428701f195}

Index of the first feature that the layer connects to, i.e the activations of the layer are copied from input_features[start_index:start_index+num_neurons]

#### `protected int32_t `[`m_num_neurons`](#classshogun_1_1CNeuralLayer_1ac9d797779840389c391816066b3f169b) {#classshogun_1_1CNeuralLayer_1ac9d797779840389c391816066b3f169b}

Number of neurons in this layer

#### `protected int32_t `[`m_width`](#classshogun_1_1CNeuralLayer_1a417f1165d2192cca456a2c623a38da73) {#classshogun_1_1CNeuralLayer_1a417f1165d2192cca456a2c623a38da73}

Width of the image (if the layer's activations are to be interpreted as images. Default value is m_num_neurons

#### `protected int32_t `[`m_height`](#classshogun_1_1CNeuralLayer_1a32e992b500cf0cd4c428e143a4bbbcb6) {#classshogun_1_1CNeuralLayer_1a32e992b500cf0cd4c428e143a4bbbcb6}

Width of the image (if the layer's activations are to be interpreted as images. Default value is 1

#### `protected int32_t `[`m_num_parameters`](#classshogun_1_1CNeuralLayer_1ad081072081024ddc9d49e590184edb60) {#classshogun_1_1CNeuralLayer_1ad081072081024ddc9d49e590184edb60}

Number of neurons in this layer

#### `protected `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`m_input_indices`](#classshogun_1_1CNeuralLayer_1ae49d0c18d6db0c36a46ecbef46ccf0cd) {#classshogun_1_1CNeuralLayer_1ae49d0c18d6db0c36a46ecbef46ccf0cd}

Indices of the layers that are connected to this layer as input

#### `protected `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`m_input_sizes`](#classshogun_1_1CNeuralLayer_1ae4e78aaf0de4f121c130918ed58d0338) {#classshogun_1_1CNeuralLayer_1ae4e78aaf0de4f121c130918ed58d0338}

Number of neurons in the layers that are connected to this layer as input

#### `protected int32_t `[`m_batch_size`](#classshogun_1_1CNeuralLayer_1acb2482e04fe13be6830ef0128acd4f68) {#classshogun_1_1CNeuralLayer_1acb2482e04fe13be6830ef0128acd4f68}

number of training/test cases the network is currently working with

#### `protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_activations`](#classshogun_1_1CNeuralLayer_1a5ec119fbcb9d66196a7ee474afc3ee2c) {#classshogun_1_1CNeuralLayer_1a5ec119fbcb9d66196a7ee474afc3ee2c}

activations of the neurons in this layer size num_neurons * batch_size

#### `protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_activation_gradients`](#classshogun_1_1CNeuralLayer_1a026290f025b7f011db95150c2c1f00c1) {#classshogun_1_1CNeuralLayer_1a026290f025b7f011db95150c2c1f00c1}

gradients of the error with respect to the layer's inputs size previous_layer_num_neurons * batch_size

#### `protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_local_gradients`](#classshogun_1_1CNeuralLayer_1a96bf7ad8d3a5e27f2945dd37b2b16812) {#classshogun_1_1CNeuralLayer_1a96bf7ad8d3a5e27f2945dd37b2b16812}

gradients of the error with respect to the layer's pre-activations, this is usually used as a buffer when computing the input gradients size num_neurons * batch_size

#### `protected `[`SGMatrix`](#classshogun_1_1SGMatrix)`< bool > `[`m_dropout_mask`](#classshogun_1_1CNeuralLayer_1ab43cbe318297728b3ccaa9c20c849012) {#classshogun_1_1CNeuralLayer_1ab43cbe318297728b3ccaa9c20c849012}

binary mask that determines whether a neuron will be kept or dropped out during the current iteration of training size num_neurons * batch_size

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

