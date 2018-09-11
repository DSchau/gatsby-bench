---
classname: "shogun::CDeepBeliefNetwork"
type: "class"
parents:
   - CSGObject
---

# class `shogun::CDeepBeliefNetwork` {#classshogun_1_1CDeepBeliefNetwork}

```
class shogun::CDeepBeliefNetwork
  : public CSGObject
```

A Deep Belief Network.

A [Deep Belief Network]([http://www.scholarpedia.org/article/Deep_belief_networks](http://www.scholarpedia.org/article/Deep_belief_networks)) [Hinton, 2006] is a multilayer probabilistic generative models. It consists of hidden layers and visible layers. The top hidden layer and the layer below it form a Restricted Boltzmann Machine. The rest of connections in the network are directed connections that go from a hidden layer into a visible layer or another hidden layer.

The network can be pre-trained by treating it as a stack of RBMs. Each hidden layer along with the layer below it form an RBM. Each RBM is then trained using (persistent) contrastive divergence. Pre-training often provides a good initialization for the network's parameters.

After pre-training, the parameters can be fine-tuned using a variant of the wake-sleep algorithm [Hinton, 2006].

The DBN can be used to initialize the parameters of a neural network using [convert_to_neural_network()](#classshogun_1_1CDeepBeliefNetwork_1a8c179cd9a503b2fa78b9bfe10ae473e5).

Samples can be drawn from the model by starting with a random state for the top hidden layer, performing some steps of Gibbs sampling in the top RBM to obtain the states of the top hidden layer and then using those to infer the states of the lower layers using a down-pass.

Steps for using the DBN class:

* Specify the number of visible units and their type using the constructor

* Add the hidden layers using add_visible_layer() and [add_hidden_layer()](#classshogun_1_1CDeepBeliefNetwork_1ae765aad072aef83a41906140c9f9a8c5).

* Initialize the DBN using [initialize_neural_network()](#classshogun_1_1CDeepBeliefNetwork_1adda3eec08b052b3af4edec2c80250fbc)

* Pre-train the DBN using [pre_train()](#classshogun_1_1CDeepBeliefNetwork_1aa546814cca87524f01256c04ef1c0305)

* Optionally do some unsupervised fine-tuning using [train()](#classshogun_1_1CDeepBeliefNetwork_1abde12120a9413306f5020c10faf25741)

* If needed, call [convert_to_neural_network()](#classshogun_1_1CDeepBeliefNetwork_1a8c179cd9a503b2fa78b9bfe10ae473e5) to convert the DBN into a neural network

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`pt_cd_num_steps`](#classshogun_1_1CDeepBeliefNetwork_1a0753163b619371f111d55ade639752c4) | [CRBM::cd_num_steps](#classshogun_1_1CRBM_1a883864669f14a89c4ecf1e22b98d34a8) for pre-training each RBM. Default value is 1 for all RBMs
`public `[`SGVector`](#classshogun_1_1SGVector)`< bool > `[`pt_cd_persistent`](#classshogun_1_1CDeepBeliefNetwork_1ae19bd76deeaad4e2a3e673a162188cb6) | [CRBM::cd_persistent](#classshogun_1_1CRBM_1abf0cdced1524987a687535a2a8de5cb3) for pre-training each RBM. Default value is true for all RBMs
`public `[`SGVector`](#classshogun_1_1SGVector)`< bool > `[`pt_cd_sample_visible`](#classshogun_1_1CDeepBeliefNetwork_1a08fe69634e58a23425cdfd85549b6af9) | [CRBM::cd_sample_visible](#classshogun_1_1CRBM_1ac07df04ecdaa151a4f63cdbe533d787f) for pre-training each RBM. Default value is false for all RBMs
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`pt_l2_coefficient`](#classshogun_1_1CDeepBeliefNetwork_1a2ef9cec4075fabb0e961dac94b8d46a9) | [CRBM::l2_coefficient](#classshogun_1_1CRBM_1a3f26018a0859bd75638c11af8baf2a87) for pre-training each RBM. Default value is 0.0 for all RBMs
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`pt_l1_coefficient`](#classshogun_1_1CDeepBeliefNetwork_1a0beec9a47799498ba72d7f3eeb82b570) | [CRBM::l1_coefficient](#classshogun_1_1CRBM_1a1a049ac8941afb416127b024c9679f43) for pre-training each RBM. Default value is 0.0 for all RBMs
`public `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`pt_monitoring_interval`](#classshogun_1_1CDeepBeliefNetwork_1a4b858c97b7e3935e55537d1102b34d58) | [CRBM::monitoring_interval](#classshogun_1_1CRBM_1a31f1201f3db6252c26e050a6a9823ea3) for pre-training each RBM. Default value is 10 for all RBMs
`public `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`pt_monitoring_method`](#classshogun_1_1CDeepBeliefNetwork_1a05675a047d72013ef644ac11eda8c73f) | [CRBM::monitoring_method](#classshogun_1_1CRBM_1ac7593996a9eac7e5c9a1feca62f7e265) for pre-training each RBM. Default value is RBMMM_RECONSTRUCTION_ERROR for all RBMs
`public `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`pt_max_num_epochs`](#classshogun_1_1CDeepBeliefNetwork_1a9fe37bdcf834b258b077cf46b52c3665) | [CRBM::max_num_epochs](#classshogun_1_1CRBM_1a7a2132cd0710750d28eaa4cd51d702af) for pre-training each RBM. Default value is 1 for all RBMs
`public `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`pt_gd_mini_batch_size`](#classshogun_1_1CDeepBeliefNetwork_1a226040b69a6d791ecc464b960b270624) | [CRBM::gd_mini_batch_size](#classshogun_1_1CRBM_1a51755f8af03ebf0259bf44ad6be4096b) for pre-training each RBM. Default value is 0 for all RBMs
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`pt_gd_learning_rate`](#classshogun_1_1CDeepBeliefNetwork_1ac86dc2df4c60f7b061d2a2e027a56093) | [CRBM::gd_learning_rate](#classshogun_1_1CRBM_1a9b287e8ac76f1b6aa6d0439f247595b4) for pre-training each RBM. Default value is 0.1 for all RBMs
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`pt_gd_learning_rate_decay`](#classshogun_1_1CDeepBeliefNetwork_1af84fe45d8b81ae43b67486cf7fd13155) | [CRBM::gd_learning_rate_decay](#classshogun_1_1CRBM_1ab45fe5f5029053c6fb02a0681e3f2581) for pre-training each RBM. Default value is 1.0 for all RBMs
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`pt_gd_momentum`](#classshogun_1_1CDeepBeliefNetwork_1a2895134735b18effe418cf714d722e0a) | [CRBM::gd_momentum](#classshogun_1_1CRBM_1a8d9e9d45f29c8cd0dcdc7625d2f321a5) for pre-training each RBM. Default value is 0.9 for all RBMs
`public int32_t `[`cd_num_steps`](#classshogun_1_1CDeepBeliefNetwork_1a883864669f14a89c4ecf1e22b98d34a8) | Number of Gibbs sampling steps performed before each weight update during wake-sleep training. Default value is 1.
`public int32_t `[`monitoring_interval`](#classshogun_1_1CDeepBeliefNetwork_1a31f1201f3db6252c26e050a6a9823ea3) | Number of weight updates between each evaluation of the reconstruction error during wake-sleep training. Default value is 10.
`public int32_t `[`max_num_epochs`](#classshogun_1_1CDeepBeliefNetwork_1a7a2132cd0710750d28eaa4cd51d702af) | Maximum number of iterations over the training set during wake-sleep training. Defualt value is 1
`public int32_t `[`gd_mini_batch_size`](#classshogun_1_1CDeepBeliefNetwork_1a51755f8af03ebf0259bf44ad6be4096b) | Size of the mini-batch used during gradient descent wake-sleep training, If 0 full-batch training is performed Default value is 0
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`gd_learning_rate`](#classshogun_1_1CDeepBeliefNetwork_1a9b287e8ac76f1b6aa6d0439f247595b4) | Gradient descent learning rate for wake-sleep training, defualt value 0.1
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`gd_learning_rate_decay`](#classshogun_1_1CDeepBeliefNetwork_1ab45fe5f5029053c6fb02a0681e3f2581) | Gradient descent learning rate decay for wake-sleep training. The learning rate is updated at each iteration i according to: alpha(i)=decay*alpha(i-1) Default value is 1.0 (no decay)
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`gd_momentum`](#classshogun_1_1CDeepBeliefNetwork_1a8d9e9d45f29c8cd0dcdc7625d2f321a5) | gradient descent momentum multiplier for wake-sleep training
`public `[`SGIO`](#classshogun_1_1SGIO)` * `[`io`](#classshogun_1_1CSGObject_1ab3ff22f724961ace985100941ba0364d) | io
`public `[`Parallel`](#classshogun_1_1Parallel)` * `[`parallel`](#classshogun_1_1CSGObject_1a1401044636b5c2353226b974526302e9) | parallel
`public `[`Version`](#classshogun_1_1Version)` * `[`version`](#classshogun_1_1CSGObject_1afc25f30ab1a6d04798c360a2ce70b87d) | version
`public `[`Parameter`](#classshogun_1_1Parameter)` * `[`m_parameters`](#classshogun_1_1CSGObject_1a70e59038292e669701bad2af7715aa1e) | parameters
`public `[`Parameter`](#classshogun_1_1Parameter)` * `[`m_model_selection_parameters`](#classshogun_1_1CSGObject_1a113f5ae82840ac3f354f94456c10f59b) | model selection parameters
`public `[`Parameter`](#classshogun_1_1Parameter)` * `[`m_gradient_parameters`](#classshogun_1_1CSGObject_1ac3f51364b93830b9c9d991cb2d5801f4) | parameters wrt which we can compute gradients
`public uint32_t `[`m_hash`](#classshogun_1_1CSGObject_1a170f14be9561242f924939c56b372a41) | Hash of parameter values
`public  `[`CDeepBeliefNetwork`](#classshogun_1_1CDeepBeliefNetwork_1a3c61dc41ee560ed1e611086d6cc64f53)`()` | default constructor
`public  `[`CDeepBeliefNetwork`](#classshogun_1_1CDeepBeliefNetwork_1aeb542a52cee295d29045a988138a3f96)`(int32_t num_visible_units,`[`ERBMVisibleUnitType`](#namespaceshogun_1a3533e5c9af23b141c1ed138077bdacd9)` unit_type)` | Creates a network with one layer of visible units
`public virtual  `[`~CDeepBeliefNetwork`](#classshogun_1_1CDeepBeliefNetwork_1ae6ebf156913085ebd98d5f3fbbd467af)`()` | 
`public virtual void `[`add_hidden_layer`](#classshogun_1_1CDeepBeliefNetwork_1ae765aad072aef83a41906140c9f9a8c5)`(int32_t num_units)` | Adds a layer of hidden units. The layer is connected to the layer that was added directly before it.
`public virtual void `[`initialize_neural_network`](#classshogun_1_1CDeepBeliefNetwork_1adda3eec08b052b3af4edec2c80250fbc)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` sigma)` | Initializes the DBN
`public virtual void `[`set_batch_size`](#classshogun_1_1CDeepBeliefNetwork_1a2fb212dd86732ebf70f0a692257422d5)`(int32_t batch_size)` | Sets the number of train/test cases the RBM will deal with
`public virtual void `[`pre_train`](#classshogun_1_1CDeepBeliefNetwork_1aa546814cca87524f01256c04ef1c0305)`(`[`CDenseFeatures](#classshogun_1_1CDenseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * features)` | Pre-trains the DBN as a stack of RBMs
`public virtual void `[`pre_train`](#classshogun_1_1CDeepBeliefNetwork_1a80d4fcf5f4bd7d66a477396df7bdca7d)`(int32_t index,`[`CDenseFeatures](#classshogun_1_1CDenseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * features)` | Pre-trains a single RBM
`public virtual void `[`train`](#classshogun_1_1CDeepBeliefNetwork_1abde12120a9413306f5020c10faf25741)`(`[`CDenseFeatures](#classshogun_1_1CDenseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * features)` | Trains the DBN using the variant of the wake-sleep algorithm described in [A Fast Learning Algorithm for Deep Belief Nets, Hinton, 2006].
`public virtual `[`CDenseFeatures](#classshogun_1_1CDenseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * `[`transform`](#classshogun_1_1CDeepBeliefNetwork_1a0c7cc4d797115797754d86aad8710d22)`(`[`CDenseFeatures](#classshogun_1_1CDenseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * features,int32_t i)` | Applies the DBN as a features transformation
`public virtual `[`CDenseFeatures](#classshogun_1_1CDenseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * `[`sample`](#classshogun_1_1CDeepBeliefNetwork_1a9018f798a1ab476dee83777ba8615419)`(int32_t num_gibbs_steps,int32_t batch_size)` | Draws samples from the marginal distribution of the visible units. The sampling starts from the values DBN's internal state and result of the sampling is stored there too.
`public virtual void `[`reset_chain`](#classshogun_1_1CDeepBeliefNetwork_1a25339e92d4e6a5786ed02a66b9d11e50)`()` | Resets the state of the markov chain used for sampling
`public virtual `[`CNeuralNetwork`](#classshogun_1_1CNeuralNetwork)` * `[`convert_to_neural_network`](#classshogun_1_1CDeepBeliefNetwork_1a8c179cd9a503b2fa78b9bfe10ae473e5)`(`[`CNeuralLayer`](#classshogun_1_1CNeuralLayer)` * output_layer,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` sigma)` | Converts the DBN into a neural network with the same structure and parameters. The visible layer in the DBN is converted into a [CNeuralInputLayer](#classshogun_1_1CNeuralInputLayer) object, and the hidden layers are converted into [CNeuralLogisticLayer](#classshogun_1_1CNeuralLogisticLayer) objects. An output layer can also be stacked on top of the last hidden layer
`public virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_weights`](#classshogun_1_1CDeepBeliefNetwork_1a4e0314e551d68e99afe563155552f75f)`(int32_t index,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > p)` | Returns the weights matrix between layer i and i+1
`public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_biases`](#classshogun_1_1CDeepBeliefNetwork_1aa949e987ed7372140a6c05526a49f2bb)`(int32_t index,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > p)` | Returns the bias vector of layer i
`public inline virtual const char * `[`get_name`](#classshogun_1_1CDeepBeliefNetwork_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` | Returns the name of the SGSerializable instance. It MUST BE the CLASS NAME without the prefixed `C'.
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
`protected `[`ERBMVisibleUnitType`](#namespaceshogun_1a3533e5c9af23b141c1ed138077bdacd9)` `[`m_visible_units_type`](#classshogun_1_1CDeepBeliefNetwork_1a4c4c1b247129eab2ebce27acdb4c3d9d) | Type of the visible units
`protected int32_t `[`m_num_layers`](#classshogun_1_1CDeepBeliefNetwork_1a86b4738d433b735f9ee0f0e5af75fc8b) | Number of layers
`protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > * `[`m_layer_sizes`](#classshogun_1_1CDeepBeliefNetwork_1a19f67f64c5637979f1b857e877514348) | Size of each layer
`protected `[`SGMatrixList](#classshogun_1_1SGMatrixList)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_states`](#classshogun_1_1CDeepBeliefNetwork_1a927570ba199caee002c77511e1876eaa) | States of each layer
`protected int32_t `[`m_batch_size`](#classshogun_1_1CDeepBeliefNetwork_1acb2482e04fe13be6830ef0128acd4f68) | Number of train/test cases the network is currently dealing with
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_params`](#classshogun_1_1CDeepBeliefNetwork_1a95b3dfe8abbc77638c890fd7d90abb56) | Parameters of the network
`protected int32_t `[`m_num_params`](#classshogun_1_1CDeepBeliefNetwork_1a0a63cb9c71b0e7b6b9dd315b11735ace) | Number of parameters
`protected `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`m_bias_index_offsets`](#classshogun_1_1CDeepBeliefNetwork_1abc61d95de84bf9b76895465be4ee685e) | Index at which the bias of each layer is stored in the parameters vector
`protected `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`m_weights_index_offsets`](#classshogun_1_1CDeepBeliefNetwork_1a5a89b452f914e38a8445ee5e0b72bd0e) | Index at which the weights of each hidden layer is stored in the parameters vector
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_sigma`](#classshogun_1_1CDeepBeliefNetwork_1a1cb9be87291a3d3f3ca4957a6a81d27c) | Standard deviation of the gaussian used to initialize the parameters
`protected virtual void `[`down_step`](#classshogun_1_1CDeepBeliefNetwork_1a922cabd99729bad985bc88b940c1991a)`(int32_t index,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > params,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > input,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > result,bool sample_states)` | Computes the states of some layer using the states of the layer above it
`protected virtual void `[`up_step`](#classshogun_1_1CDeepBeliefNetwork_1a410310b98d7af0e9874240c7ebbe4c8d)`(int32_t index,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > params,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > input,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > result,bool sample_states)` | Computes the states of some layer using the states of the layer below it
`protected virtual void `[`wake_sleep`](#classshogun_1_1CDeepBeliefNetwork_1a0694be23346bc7cedbeb7a0fbd46a228)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > data,`[`CRBM`](#classshogun_1_1CRBM)` * top_rbm,`[`SGMatrixList](#classshogun_1_1SGMatrixList)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > sleep_states,`[`SGMatrixList](#classshogun_1_1SGMatrixList)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > wake_states,`[`SGMatrixList](#classshogun_1_1SGMatrixList)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > psleep_states,`[`SGMatrixList](#classshogun_1_1SGMatrixList)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > pwake_states,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > gen_params,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > rec_params,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > gen_gradients,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > rec_gradients)` | Computes the gradients using the wake-sleep algorithm
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

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`pt_cd_num_steps`](#classshogun_1_1CDeepBeliefNetwork_1a0753163b619371f111d55ade639752c4) {#classshogun_1_1CDeepBeliefNetwork_1a0753163b619371f111d55ade639752c4}

[CRBM::cd_num_steps](#classshogun_1_1CRBM_1a883864669f14a89c4ecf1e22b98d34a8) for pre-training each RBM. Default value is 1 for all RBMs

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< bool > `[`pt_cd_persistent`](#classshogun_1_1CDeepBeliefNetwork_1ae19bd76deeaad4e2a3e673a162188cb6) {#classshogun_1_1CDeepBeliefNetwork_1ae19bd76deeaad4e2a3e673a162188cb6}

[CRBM::cd_persistent](#classshogun_1_1CRBM_1abf0cdced1524987a687535a2a8de5cb3) for pre-training each RBM. Default value is true for all RBMs

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< bool > `[`pt_cd_sample_visible`](#classshogun_1_1CDeepBeliefNetwork_1a08fe69634e58a23425cdfd85549b6af9) {#classshogun_1_1CDeepBeliefNetwork_1a08fe69634e58a23425cdfd85549b6af9}

[CRBM::cd_sample_visible](#classshogun_1_1CRBM_1ac07df04ecdaa151a4f63cdbe533d787f) for pre-training each RBM. Default value is false for all RBMs

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`pt_l2_coefficient`](#classshogun_1_1CDeepBeliefNetwork_1a2ef9cec4075fabb0e961dac94b8d46a9) {#classshogun_1_1CDeepBeliefNetwork_1a2ef9cec4075fabb0e961dac94b8d46a9}

[CRBM::l2_coefficient](#classshogun_1_1CRBM_1a3f26018a0859bd75638c11af8baf2a87) for pre-training each RBM. Default value is 0.0 for all RBMs

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`pt_l1_coefficient`](#classshogun_1_1CDeepBeliefNetwork_1a0beec9a47799498ba72d7f3eeb82b570) {#classshogun_1_1CDeepBeliefNetwork_1a0beec9a47799498ba72d7f3eeb82b570}

[CRBM::l1_coefficient](#classshogun_1_1CRBM_1a1a049ac8941afb416127b024c9679f43) for pre-training each RBM. Default value is 0.0 for all RBMs

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`pt_monitoring_interval`](#classshogun_1_1CDeepBeliefNetwork_1a4b858c97b7e3935e55537d1102b34d58) {#classshogun_1_1CDeepBeliefNetwork_1a4b858c97b7e3935e55537d1102b34d58}

[CRBM::monitoring_interval](#classshogun_1_1CRBM_1a31f1201f3db6252c26e050a6a9823ea3) for pre-training each RBM. Default value is 10 for all RBMs

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`pt_monitoring_method`](#classshogun_1_1CDeepBeliefNetwork_1a05675a047d72013ef644ac11eda8c73f) {#classshogun_1_1CDeepBeliefNetwork_1a05675a047d72013ef644ac11eda8c73f}

[CRBM::monitoring_method](#classshogun_1_1CRBM_1ac7593996a9eac7e5c9a1feca62f7e265) for pre-training each RBM. Default value is RBMMM_RECONSTRUCTION_ERROR for all RBMs

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`pt_max_num_epochs`](#classshogun_1_1CDeepBeliefNetwork_1a9fe37bdcf834b258b077cf46b52c3665) {#classshogun_1_1CDeepBeliefNetwork_1a9fe37bdcf834b258b077cf46b52c3665}

[CRBM::max_num_epochs](#classshogun_1_1CRBM_1a7a2132cd0710750d28eaa4cd51d702af) for pre-training each RBM. Default value is 1 for all RBMs

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`pt_gd_mini_batch_size`](#classshogun_1_1CDeepBeliefNetwork_1a226040b69a6d791ecc464b960b270624) {#classshogun_1_1CDeepBeliefNetwork_1a226040b69a6d791ecc464b960b270624}

[CRBM::gd_mini_batch_size](#classshogun_1_1CRBM_1a51755f8af03ebf0259bf44ad6be4096b) for pre-training each RBM. Default value is 0 for all RBMs

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`pt_gd_learning_rate`](#classshogun_1_1CDeepBeliefNetwork_1ac86dc2df4c60f7b061d2a2e027a56093) {#classshogun_1_1CDeepBeliefNetwork_1ac86dc2df4c60f7b061d2a2e027a56093}

[CRBM::gd_learning_rate](#classshogun_1_1CRBM_1a9b287e8ac76f1b6aa6d0439f247595b4) for pre-training each RBM. Default value is 0.1 for all RBMs

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`pt_gd_learning_rate_decay`](#classshogun_1_1CDeepBeliefNetwork_1af84fe45d8b81ae43b67486cf7fd13155) {#classshogun_1_1CDeepBeliefNetwork_1af84fe45d8b81ae43b67486cf7fd13155}

[CRBM::gd_learning_rate_decay](#classshogun_1_1CRBM_1ab45fe5f5029053c6fb02a0681e3f2581) for pre-training each RBM. Default value is 1.0 for all RBMs

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`pt_gd_momentum`](#classshogun_1_1CDeepBeliefNetwork_1a2895134735b18effe418cf714d722e0a) {#classshogun_1_1CDeepBeliefNetwork_1a2895134735b18effe418cf714d722e0a}

[CRBM::gd_momentum](#classshogun_1_1CRBM_1a8d9e9d45f29c8cd0dcdc7625d2f321a5) for pre-training each RBM. Default value is 0.9 for all RBMs

#### `public int32_t `[`cd_num_steps`](#classshogun_1_1CDeepBeliefNetwork_1a883864669f14a89c4ecf1e22b98d34a8) {#classshogun_1_1CDeepBeliefNetwork_1a883864669f14a89c4ecf1e22b98d34a8}

Number of Gibbs sampling steps performed before each weight update during wake-sleep training. Default value is 1.

#### `public int32_t `[`monitoring_interval`](#classshogun_1_1CDeepBeliefNetwork_1a31f1201f3db6252c26e050a6a9823ea3) {#classshogun_1_1CDeepBeliefNetwork_1a31f1201f3db6252c26e050a6a9823ea3}

Number of weight updates between each evaluation of the reconstruction error during wake-sleep training. Default value is 10.

#### `public int32_t `[`max_num_epochs`](#classshogun_1_1CDeepBeliefNetwork_1a7a2132cd0710750d28eaa4cd51d702af) {#classshogun_1_1CDeepBeliefNetwork_1a7a2132cd0710750d28eaa4cd51d702af}

Maximum number of iterations over the training set during wake-sleep training. Defualt value is 1

#### `public int32_t `[`gd_mini_batch_size`](#classshogun_1_1CDeepBeliefNetwork_1a51755f8af03ebf0259bf44ad6be4096b) {#classshogun_1_1CDeepBeliefNetwork_1a51755f8af03ebf0259bf44ad6be4096b}

Size of the mini-batch used during gradient descent wake-sleep training, If 0 full-batch training is performed Default value is 0

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`gd_learning_rate`](#classshogun_1_1CDeepBeliefNetwork_1a9b287e8ac76f1b6aa6d0439f247595b4) {#classshogun_1_1CDeepBeliefNetwork_1a9b287e8ac76f1b6aa6d0439f247595b4}

Gradient descent learning rate for wake-sleep training, defualt value 0.1

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`gd_learning_rate_decay`](#classshogun_1_1CDeepBeliefNetwork_1ab45fe5f5029053c6fb02a0681e3f2581) {#classshogun_1_1CDeepBeliefNetwork_1ab45fe5f5029053c6fb02a0681e3f2581}

Gradient descent learning rate decay for wake-sleep training. The learning rate is updated at each iteration i according to: alpha(i)=decay*alpha(i-1) Default value is 1.0 (no decay)

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`gd_momentum`](#classshogun_1_1CDeepBeliefNetwork_1a8d9e9d45f29c8cd0dcdc7625d2f321a5) {#classshogun_1_1CDeepBeliefNetwork_1a8d9e9d45f29c8cd0dcdc7625d2f321a5}

gradient descent momentum multiplier for wake-sleep training

default value is 0.9

For more details on momentum, see this [paper]([http://jmlr.org/proceedings/papers/v28/sutskever13.html](http://jmlr.org/proceedings/papers/v28/sutskever13.html)) [Sutskever, 2013]

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

#### `public  `[`CDeepBeliefNetwork`](#classshogun_1_1CDeepBeliefNetwork_1a3c61dc41ee560ed1e611086d6cc64f53)`()` {#classshogun_1_1CDeepBeliefNetwork_1a3c61dc41ee560ed1e611086d6cc64f53}

default constructor

#### `public  `[`CDeepBeliefNetwork`](#classshogun_1_1CDeepBeliefNetwork_1aeb542a52cee295d29045a988138a3f96)`(int32_t num_visible_units,`[`ERBMVisibleUnitType`](#namespaceshogun_1a3533e5c9af23b141c1ed138077bdacd9)` unit_type)` {#classshogun_1_1CDeepBeliefNetwork_1aeb542a52cee295d29045a988138a3f96}

Creates a network with one layer of visible units

#### Parameters
* `num_visible_units` Number of visible units 

* `unit_type` Type of visible units

#### `public virtual  `[`~CDeepBeliefNetwork`](#classshogun_1_1CDeepBeliefNetwork_1ae6ebf156913085ebd98d5f3fbbd467af)`()` {#classshogun_1_1CDeepBeliefNetwork_1ae6ebf156913085ebd98d5f3fbbd467af}

#### `public virtual void `[`add_hidden_layer`](#classshogun_1_1CDeepBeliefNetwork_1ae765aad072aef83a41906140c9f9a8c5)`(int32_t num_units)` {#classshogun_1_1CDeepBeliefNetwork_1ae765aad072aef83a41906140c9f9a8c5}

Adds a layer of hidden units. The layer is connected to the layer that was added directly before it.

#### Parameters
* `num_units` Number of hidden units

#### `public virtual void `[`initialize_neural_network`](#classshogun_1_1CDeepBeliefNetwork_1adda3eec08b052b3af4edec2c80250fbc)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` sigma)` {#classshogun_1_1CDeepBeliefNetwork_1adda3eec08b052b3af4edec2c80250fbc}

Initializes the DBN

#### Parameters
* `sigma` Standard deviation of the gaussian used to initialize the weights

#### `public virtual void `[`set_batch_size`](#classshogun_1_1CDeepBeliefNetwork_1a2fb212dd86732ebf70f0a692257422d5)`(int32_t batch_size)` {#classshogun_1_1CDeepBeliefNetwork_1a2fb212dd86732ebf70f0a692257422d5}

Sets the number of train/test cases the RBM will deal with

#### Parameters
* `batch_size` Batch size

#### `public virtual void `[`pre_train`](#classshogun_1_1CDeepBeliefNetwork_1aa546814cca87524f01256c04ef1c0305)`(`[`CDenseFeatures](#classshogun_1_1CDenseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * features)` {#classshogun_1_1CDeepBeliefNetwork_1aa546814cca87524f01256c04ef1c0305}

Pre-trains the DBN as a stack of RBMs

#### Parameters
* `features` Input features. Should have as many features as the number of visible units in the DBN

#### `public virtual void `[`pre_train`](#classshogun_1_1CDeepBeliefNetwork_1a80d4fcf5f4bd7d66a477396df7bdca7d)`(int32_t index,`[`CDenseFeatures](#classshogun_1_1CDenseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * features)` {#classshogun_1_1CDeepBeliefNetwork_1a80d4fcf5f4bd7d66a477396df7bdca7d}

Pre-trains a single RBM

#### Parameters
* `index` Index of the RBM 

* `features` Input features. Should have as many features as the total number of visible units in the DBN

#### `public virtual void `[`train`](#classshogun_1_1CDeepBeliefNetwork_1abde12120a9413306f5020c10faf25741)`(`[`CDenseFeatures](#classshogun_1_1CDenseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * features)` {#classshogun_1_1CDeepBeliefNetwork_1abde12120a9413306f5020c10faf25741}

Trains the DBN using the variant of the wake-sleep algorithm described in [A Fast Learning Algorithm for Deep Belief Nets, Hinton, 2006].

#### Parameters
* `features` Input features. Should have as many features as the total number of visible units in the DBN

#### `public virtual `[`CDenseFeatures](#classshogun_1_1CDenseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * `[`transform`](#classshogun_1_1CDeepBeliefNetwork_1a0c7cc4d797115797754d86aad8710d22)`(`[`CDenseFeatures](#classshogun_1_1CDenseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * features,int32_t i)` {#classshogun_1_1CDeepBeliefNetwork_1a0c7cc4d797115797754d86aad8710d22}

Applies the DBN as a features transformation

Forward-propagates the input features through the DBN and returns the Mean activations of the $ i^{th} $ hidden layer

#### Parameters
* `features` Input features. Should have as many features as the number of visible units in the DBN 

* `i` Index of the hidden layer. If -1, the activations of the last hidden layer is returned

#### Returns
Mean activations of the $ i^{th} $ hidden layer

#### `public virtual `[`CDenseFeatures](#classshogun_1_1CDenseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * `[`sample`](#classshogun_1_1CDeepBeliefNetwork_1a9018f798a1ab476dee83777ba8615419)`(int32_t num_gibbs_steps,int32_t batch_size)` {#classshogun_1_1CDeepBeliefNetwork_1a9018f798a1ab476dee83777ba8615419}

Draws samples from the marginal distribution of the visible units. The sampling starts from the values DBN's internal state and result of the sampling is stored there too.

#### Parameters
* `num_gibbs_steps` Number of Gibbs sampling steps for the top RBM. 

* `batch_size` Number of samples to be drawn. A seperate chain is used for each sample

#### Returns
Sampled states of the visible units

#### `public virtual void `[`reset_chain`](#classshogun_1_1CDeepBeliefNetwork_1a25339e92d4e6a5786ed02a66b9d11e50)`()` {#classshogun_1_1CDeepBeliefNetwork_1a25339e92d4e6a5786ed02a66b9d11e50}

Resets the state of the markov chain used for sampling

#### `public virtual `[`CNeuralNetwork`](#classshogun_1_1CNeuralNetwork)` * `[`convert_to_neural_network`](#classshogun_1_1CDeepBeliefNetwork_1a8c179cd9a503b2fa78b9bfe10ae473e5)`(`[`CNeuralLayer`](#classshogun_1_1CNeuralLayer)` * output_layer,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` sigma)` {#classshogun_1_1CDeepBeliefNetwork_1a8c179cd9a503b2fa78b9bfe10ae473e5}

Converts the DBN into a neural network with the same structure and parameters. The visible layer in the DBN is converted into a [CNeuralInputLayer](#classshogun_1_1CNeuralInputLayer) object, and the hidden layers are converted into [CNeuralLogisticLayer](#classshogun_1_1CNeuralLogisticLayer) objects. An output layer can also be stacked on top of the last hidden layer

#### Parameters
* `output_layer` An output layer 

* `sigma` Standard deviation of the gaussian used to initialize the parameters of the output layer

#### Returns
Neural network inititialized using the DBN

#### `public virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_weights`](#classshogun_1_1CDeepBeliefNetwork_1a4e0314e551d68e99afe563155552f75f)`(int32_t index,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > p)` {#classshogun_1_1CDeepBeliefNetwork_1a4e0314e551d68e99afe563155552f75f}

Returns the weights matrix between layer i and i+1

#### Parameters
* `index` Layer index 

* `p` If specified, the weight matrix is extracted from it instead of m_params

#### `public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_biases`](#classshogun_1_1CDeepBeliefNetwork_1aa949e987ed7372140a6c05526a49f2bb)`(int32_t index,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > p)` {#classshogun_1_1CDeepBeliefNetwork_1aa949e987ed7372140a6c05526a49f2bb}

Returns the bias vector of layer i

#### Parameters
* `index` Layer index 

* `p` If specified, the bias vector is extracted from it instead of m_params

#### `public inline virtual const char * `[`get_name`](#classshogun_1_1CDeepBeliefNetwork_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` {#classshogun_1_1CDeepBeliefNetwork_1a9cb485686dd7a1e6f7103cf42e87717e}

Returns the name of the SGSerializable instance. It MUST BE the CLASS NAME without the prefixed `C'.

#### Returns
name of the SGSerializable

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

#### `protected `[`ERBMVisibleUnitType`](#namespaceshogun_1a3533e5c9af23b141c1ed138077bdacd9)` `[`m_visible_units_type`](#classshogun_1_1CDeepBeliefNetwork_1a4c4c1b247129eab2ebce27acdb4c3d9d) {#classshogun_1_1CDeepBeliefNetwork_1a4c4c1b247129eab2ebce27acdb4c3d9d}

Type of the visible units

#### `protected int32_t `[`m_num_layers`](#classshogun_1_1CDeepBeliefNetwork_1a86b4738d433b735f9ee0f0e5af75fc8b) {#classshogun_1_1CDeepBeliefNetwork_1a86b4738d433b735f9ee0f0e5af75fc8b}

Number of layers

#### `protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > * `[`m_layer_sizes`](#classshogun_1_1CDeepBeliefNetwork_1a19f67f64c5637979f1b857e877514348) {#classshogun_1_1CDeepBeliefNetwork_1a19f67f64c5637979f1b857e877514348}

Size of each layer

#### `protected `[`SGMatrixList](#classshogun_1_1SGMatrixList)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_states`](#classshogun_1_1CDeepBeliefNetwork_1a927570ba199caee002c77511e1876eaa) {#classshogun_1_1CDeepBeliefNetwork_1a927570ba199caee002c77511e1876eaa}

States of each layer

#### `protected int32_t `[`m_batch_size`](#classshogun_1_1CDeepBeliefNetwork_1acb2482e04fe13be6830ef0128acd4f68) {#classshogun_1_1CDeepBeliefNetwork_1acb2482e04fe13be6830ef0128acd4f68}

Number of train/test cases the network is currently dealing with

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_params`](#classshogun_1_1CDeepBeliefNetwork_1a95b3dfe8abbc77638c890fd7d90abb56) {#classshogun_1_1CDeepBeliefNetwork_1a95b3dfe8abbc77638c890fd7d90abb56}

Parameters of the network

#### `protected int32_t `[`m_num_params`](#classshogun_1_1CDeepBeliefNetwork_1a0a63cb9c71b0e7b6b9dd315b11735ace) {#classshogun_1_1CDeepBeliefNetwork_1a0a63cb9c71b0e7b6b9dd315b11735ace}

Number of parameters

#### `protected `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`m_bias_index_offsets`](#classshogun_1_1CDeepBeliefNetwork_1abc61d95de84bf9b76895465be4ee685e) {#classshogun_1_1CDeepBeliefNetwork_1abc61d95de84bf9b76895465be4ee685e}

Index at which the bias of each layer is stored in the parameters vector

#### `protected `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`m_weights_index_offsets`](#classshogun_1_1CDeepBeliefNetwork_1a5a89b452f914e38a8445ee5e0b72bd0e) {#classshogun_1_1CDeepBeliefNetwork_1a5a89b452f914e38a8445ee5e0b72bd0e}

Index at which the weights of each hidden layer is stored in the parameters vector

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_sigma`](#classshogun_1_1CDeepBeliefNetwork_1a1cb9be87291a3d3f3ca4957a6a81d27c) {#classshogun_1_1CDeepBeliefNetwork_1a1cb9be87291a3d3f3ca4957a6a81d27c}

Standard deviation of the gaussian used to initialize the parameters

#### `protected virtual void `[`down_step`](#classshogun_1_1CDeepBeliefNetwork_1a922cabd99729bad985bc88b940c1991a)`(int32_t index,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > params,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > input,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > result,bool sample_states)` {#classshogun_1_1CDeepBeliefNetwork_1a922cabd99729bad985bc88b940c1991a}

Computes the states of some layer using the states of the layer above it

#### `protected virtual void `[`up_step`](#classshogun_1_1CDeepBeliefNetwork_1a410310b98d7af0e9874240c7ebbe4c8d)`(int32_t index,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > params,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > input,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > result,bool sample_states)` {#classshogun_1_1CDeepBeliefNetwork_1a410310b98d7af0e9874240c7ebbe4c8d}

Computes the states of some layer using the states of the layer below it

#### `protected virtual void `[`wake_sleep`](#classshogun_1_1CDeepBeliefNetwork_1a0694be23346bc7cedbeb7a0fbd46a228)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > data,`[`CRBM`](#classshogun_1_1CRBM)` * top_rbm,`[`SGMatrixList](#classshogun_1_1SGMatrixList)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > sleep_states,`[`SGMatrixList](#classshogun_1_1SGMatrixList)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > wake_states,`[`SGMatrixList](#classshogun_1_1SGMatrixList)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > psleep_states,`[`SGMatrixList](#classshogun_1_1SGMatrixList)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > pwake_states,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > gen_params,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > rec_params,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > gen_gradients,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > rec_gradients)` {#classshogun_1_1CDeepBeliefNetwork_1a0694be23346bc7cedbeb7a0fbd46a228}

Computes the gradients using the wake-sleep algorithm

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

