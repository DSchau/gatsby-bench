---
classname: "shogun::CNeuralNetwork"
type: "class"
parents:
   - CMachine
---

# class `shogun::CNeuralNetwork` {#classshogun_1_1CNeuralNetwork}

```
class shogun::CNeuralNetwork
  : public CMachine
```

A generic multi-layer neural network.

A [Neural network]([http://en.wikipedia.org/wiki/Artificial_neural_network](http://en.wikipedia.org/wiki/Artificial_neural_network)) is constructed using an array of [CNeuralLayer](#classshogun_1_1CNeuralLayer) objects. The NeuralLayer class defines the interface necessary for forward and [backpropagation]([http://en.wikipedia.org/wiki/Backpropagation](http://en.wikipedia.org/wiki/Backpropagation)).

The network can be constructed as any arbitrary directed acyclic graph.

How to use the network:

* Prepare a [CDynamicObjectArray](#classshogun_1_1CDynamicObjectArray) of CNeuralLayer-based objects that specify the type of layers used in the network. The array must contain at least one input layer. The last layer in the array is treated as the output layer. Also note that forward propagation is performed in the order at which the layers appear in the array. So if layer j takes its input from layer i then i must be less than j.

* Specify how the layers are connected together. This can be done using either [connect()](#classshogun_1_1CNeuralNetwork_1a82f8cdcc3b5cb1d13fb986a217c299ce) or [quick_connect()](#classshogun_1_1CNeuralNetwork_1a06e9e9cc5c2425123911ea0f5805c1ef).

* Call [initialize_neural_network()](#classshogun_1_1CNeuralNetwork_1ad305d5766182085e6f9dba86684c5900)

* Specify the training parameters if needed

* Train [set_labels()](#classshogun_1_1CNeuralNetwork_1a5f0cfd09e37bd5e793cacecb8d3c818b) and [train()](#classshogun_1_1CMachine_1aa0ece9fd14892c6dfed1bb8c78f3b3ed)

* If needed, the network with the learned parameters can be stored on disk using [save_serializable()](#classshogun_1_1CSGObject_1aa9787e341533c4970885ce6d3022a935) (loaded using [load_serializable()](#classshogun_1_1CSGObject_1ad67e38ad80d4152151081f838c0a13e1))

* Apply the network using [apply()](#classshogun_1_1CMachine_1afd5d402257972c78456594234d13eb4c)

The network can also be initialized from a JSON file using CNeuralNetworkFileReader.

Supported feature types: [CDenseFeatures<float64_t>](#classshogun_1_1CDenseFeatures) Supported label types:

* [CBinaryLabels](#classshogun_1_1CBinaryLabels)

* [CMulticlassLabels](#classshogun_1_1CMulticlassLabels)

* [CRegressionLabels](#classshogun_1_1CRegressionLabels)

The neural network can be trained using [L-BFGS]([http://en.wikipedia.org/wiki/Limited-memory_BFGS](http://en.wikipedia.org/wiki/Limited-memory_BFGS)) (default) or [mini-batch gradient descent] ([http://en.wikipedia.org/wiki/Stochastic_gradient_descent](http://en.wikipedia.org/wiki/Stochastic_gradient_descent)).

NOTE: LBFGS does not work properly when using dropout/max-norm regularization due to their stochastic nature. Use gradient descent instead.

During training, the error at each iteration is logged as MSG_INFO. (to turn on info messages call sg_io->set_loglevel(MSG_INFO)).

The network stores the parameters of all the layers in a single array. This makes it easy to train a network of any combination of arbitrary layer types using any optimization method (gradient descent, L-BFGS, ..)

All the matrices the network (and related classes) deal with are in column-major format

When implemnting new layer types, the function [check_gradients()](#classshogun_1_1CNeuralNetwork_1a774aef9dd4054b1f7608c859688b8334) can be used to make sure the gradient computations are correct.

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
`public  `[`CNeuralNetwork`](#classshogun_1_1CNeuralNetwork_1a0ea77cbc69188e84fe6593e88878a61e)`()` | default constuctor
`public  `[`CNeuralNetwork`](#classshogun_1_1CNeuralNetwork_1a1cb686914ea6786bc2819f41dfcebdee)`(`[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` * layers)` | Sets the layers of the network
`public virtual void `[`set_layers`](#classshogun_1_1CNeuralNetwork_1a2cefbd8c2c469b0fb8d8fca4cde9e82b)`(`[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` * layers)` | Sets the layers of the network
`public virtual void `[`connect`](#classshogun_1_1CNeuralNetwork_1a82f8cdcc3b5cb1d13fb986a217c299ce)`(int32_t i,int32_t j)` | Connects layer i as input to layer j. In order for forward and backpropagation to work correctly, i must be less that j
`public virtual void `[`init_adj_matrix`](#classshogun_1_1CNeuralNetwork_1afac54e76bbf5cf17669bd25add587b4b)`()` | Initialize adjacency matrix
`public virtual void `[`quick_connect`](#classshogun_1_1CNeuralNetwork_1a06e9e9cc5c2425123911ea0f5805c1ef)`()` | Connects each layer to the layer after it. That is, connects layer i to as input to layer i+1 for all i.
`public virtual void `[`disconnect`](#classshogun_1_1CNeuralNetwork_1a1f0f1f3df5f8d0b1bb0c959be11d95e8)`(int32_t i,int32_t j)` | Disconnects layer i from layer j
`public virtual void `[`disconnect_all`](#classshogun_1_1CNeuralNetwork_1a02922e7231c3a315b2bfd1049b675365)`()` | Removes all connections in the network
`public virtual void `[`initialize_neural_network`](#classshogun_1_1CNeuralNetwork_1ad305d5766182085e6f9dba86684c5900)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` sigma)` | Initializes the network
`public virtual  `[`~CNeuralNetwork`](#classshogun_1_1CNeuralNetwork_1a660c12934593583eb75b597f10417113)`()` | 
`public virtual `[`CBinaryLabels`](#classshogun_1_1CBinaryLabels)` * `[`apply_binary`](#classshogun_1_1CNeuralNetwork_1aaffb86a617d7acafe814302fe05b8132)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data in means of binary classification problem
`public virtual `[`CRegressionLabels`](#classshogun_1_1CRegressionLabels)` * `[`apply_regression`](#classshogun_1_1CNeuralNetwork_1a5583c1b05368a6addb730420fbc43ac9)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data in means of regression problem
`public virtual `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * `[`apply_multiclass`](#classshogun_1_1CNeuralNetwork_1a860ce9657aa41604154212b7f1f422d3)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data in means of multiclass classification problem
`public virtual `[`CDenseFeatures](#classshogun_1_1CDenseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * `[`transform`](#classshogun_1_1CNeuralNetwork_1a9b315544d06f0a0fe6f6f6113466bd83)`(`[`CDenseFeatures](#classshogun_1_1CDenseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * data)` | Applies the network as a feature transformation
`public virtual void `[`set_labels`](#classshogun_1_1CNeuralNetwork_1a5f0cfd09e37bd5e793cacecb8d3c818b)`(`[`CLabels`](#classshogun_1_1CLabels)` * lab)` | set labels
`public inline virtual `[`EMachineType`](#namespaceshogun_1af181c832c12de7a0c3b02425986106cc)` `[`get_classifier_type`](#classshogun_1_1CNeuralNetwork_1ab0ee71eb4f9097a9b7ad2b72b1b310e2)`()` | get classifier type
`public virtual `[`EProblemType`](#namespaceshogun_1a0aa89aa872f89f6a174de2f45b7596d4)` `[`get_machine_problem_type`](#classshogun_1_1CNeuralNetwork_1a135f8d82da3fc55807d1640080358500)`() const` | returns type of problem machine solves
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`check_gradients`](#classshogun_1_1CNeuralNetwork_1a774aef9dd4054b1f7608c859688b8334)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` approx_epsilon,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` s)` | Checks if the gradients computed using backpropagation are correct by comparing them with gradients computed using numerical approximation. Used for testing purposes only.
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * `[`get_layer_parameters`](#classshogun_1_1CNeuralNetwork_1a26a5fe12bb334b92478462a020d6c3ed)`(int32_t i)` | returns a copy of a layer's parameters array
`public inline int32_t `[`get_num_parameters`](#classshogun_1_1CNeuralNetwork_1a3adb14d9f900d24099dd289ea25480b8)`()` | returns the totat number of parameters in the network
`public inline `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_parameters`](#classshogun_1_1CNeuralNetwork_1a9f8ebaa5d6a822e29b39133c5c8b668f)`()` | return the network's parameter array
`public inline int32_t `[`get_num_inputs`](#classshogun_1_1CNeuralNetwork_1a2684a371ae1b5fc6dd2b2189b26c1e47)`()` | returns the number of inputs the network takes
`public int32_t `[`get_num_outputs`](#classshogun_1_1CNeuralNetwork_1a6d88ac18968e25f18aee7f3241234db2)`()` | returns the number of neurons in the output layer
`public `[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` * `[`get_layers`](#classshogun_1_1CNeuralNetwork_1af83006457e52d5fd9a6fe69d132bf8a9)`()` | Returns an array holding the network's layers
`public inline virtual const char * `[`get_name`](#classshogun_1_1CNeuralNetwork_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` | Returns the name of the SGSerializable instance. It MUST BE the CLASS NAME without the prefixed `C'.
`public inline void `[`set_optimization_method`](#classshogun_1_1CNeuralNetwork_1ae6c3a26d80235c8a3595809224b9dd00)`(`[`ENNOptimizationMethod`](#namespaceshogun_1afc5d4c2c14dc1ccf25e474b4f53c1cf5)` optimization_method)` | Sets optimization method default is NNOM_LBFGS 
`public inline `[`ENNOptimizationMethod`](#namespaceshogun_1afc5d4c2c14dc1ccf25e474b4f53c1cf5)` `[`get_optimization_method`](#classshogun_1_1CNeuralNetwork_1a08d3efa11428d74e677325ad76a0fe14)`() const` | Returns optimization method
`public inline void `[`set_l2_coefficient`](#classshogun_1_1CNeuralNetwork_1a7ec86f645fdaaf951533dc00000444f1)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` l2_coefficient)` | Sets L2 Regularization coeff default value is 0.0 
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_l2_coefficient`](#classshogun_1_1CNeuralNetwork_1ab75edf716ce15352435bb24e3371cb44)`() const` | Returns L2 coefficient
`public inline void `[`set_l1_coefficient`](#classshogun_1_1CNeuralNetwork_1a22ba708c3403575afc5ade0b6709839f)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` l1_coefficient)` | Sets L1 Regularization coeff default value is 0.0 
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_l1_coefficient`](#classshogun_1_1CNeuralNetwork_1a583b67b124b3bd0e0b9656beeb02949a)`() const` | Returns L1 coefficient
`public inline void `[`set_dropout_hidden`](#classshogun_1_1CNeuralNetwork_1ac750d47359f6d479349e3441cf9b6527)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` dropout_hidden)` | Sets the probabilty that a hidden layer neuron will be dropped out When using this, the recommended value is 0.5 default value 0.0 (no dropout)
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_dropout_hidden`](#classshogun_1_1CNeuralNetwork_1a15209c974f555786c713975b05d55ccd)`() const` | Returns dropout probability for hidden layers
`public inline void `[`set_dropout_input`](#classshogun_1_1CNeuralNetwork_1ae5630682b9c8f2d1d2bf5e4757b512cc)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` dropout_input)` | Sets the probabilty that an input layer neuron will be dropped out When using this, a good value might be 0.2 default value 0.0 (no dropout)
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_dropout_input`](#classshogun_1_1CNeuralNetwork_1a16ff92cd8240b9bfc7c1697b6b23b0dd)`() const` | Returns dropout probability for input layers
`public inline void `[`set_max_norm`](#classshogun_1_1CNeuralNetwork_1a4659677f77dfa3b8d56c090b81b02031)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` max_norm)` | Sets maximum allowable L2 norm for a neurons weights When using this, a good value might be 15 default value -1 (max-norm regularization disabled) 
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_max_norm`](#classshogun_1_1CNeuralNetwork_1a93384fb1df0b2359ef76dc15034f4575)`() const` | Returns maximum allowable L2 norm
`public inline void `[`set_epsilon`](#classshogun_1_1CNeuralNetwork_1a3b8392d8584df5bdba1d4af92346db31)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` epsilon)` | Sets convergence criteria training stops when (E'- E)/E < epsilon where E is the error at the current iterations and E' is the error at the previous iteration default value is 1.0e-5 
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_epsilon`](#classshogun_1_1CNeuralNetwork_1a0813512911649cc6fa462bad06b877ee)`() const` | Returns epsilon
`public inline void `[`set_max_num_epochs`](#classshogun_1_1CNeuralNetwork_1a911c489977144f76ed52f213d4c56ba4)`(int32_t max_num_epochs)` | Sets maximum number of iterations over the training set. If 0, training will continue until convergence. defualt value is 0 
`public inline int32_t `[`get_max_num_epochs`](#classshogun_1_1CNeuralNetwork_1a36b6b29dd7e2ec95a593d18d2a9d78a8)`() const` | Returns maximum number of epochs
`public inline void `[`set_gd_mini_batch_size`](#classshogun_1_1CNeuralNetwork_1abd80a633223bdbc84ddf4d3c96fcd6d7)`(int32_t gd_mini_batch_size)` | Sets size of the mini-batch used during gradient descent training, if 0 full-batch training is performed default value is 0 
`public inline int32_t `[`get_gd_mini_batch_size`](#classshogun_1_1CNeuralNetwork_1a71b79ef9e968280ea329a508bd0e2658)`() const` | Returns mini batch size
`public inline void `[`set_gd_learning_rate`](#classshogun_1_1CNeuralNetwork_1ace44b3eef4895e16124e247a541354d1)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` gd_learning_rate)` | Sets gradient descent learning rate defualt value 0.1 
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_gd_learning_rate`](#classshogun_1_1CNeuralNetwork_1a04a39cfec3a58b2e02f09bbfa35ba478)`() const` | Returns gradient descent learning rate
`public inline void `[`set_gd_learning_rate_decay`](#classshogun_1_1CNeuralNetwork_1afdfe04cff6e60176db27bd93196c96f2)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` gd_learning_rate_decay)` | Sets gradient descent learning rate decay learning rate is updated at each iteration i according to: alpha(i)=decay*alpha(i-1) default value is 1.0 (no decay) 
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_gd_learning_rate_decay`](#classshogun_1_1CNeuralNetwork_1a178443fc53cb12f120dbfc81dd5c2daf)`() const` | Returns gradient descent learning rate decay
`public inline void `[`set_gd_momentum`](#classshogun_1_1CNeuralNetwork_1a82e0a2cb6f405d6697ca522c9ad7d77d)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` gd_momentum)` | Sets gradient descent momentum multiplier
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_gd_momentum`](#classshogun_1_1CNeuralNetwork_1af6a017a8771ae55dc3aa77546757d204)`() const` | Returns gradient descent momentum multiplier
`public inline void `[`set_gd_error_damping_coeff`](#classshogun_1_1CNeuralNetwork_1a32bc669352d1b4d22a75d1fe4a8a9175)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` gd_error_damping_coeff)` | Sets gradient descent error damping coefficient Used to damp the error fluctuations when stochastic gradient descent is used. damping is done according to: error_damped(i) = c*error(i) + (1-c)*error_damped(i-1) where c is the damping coefficient
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_gd_error_damping_coeff`](#classshogun_1_1CNeuralNetwork_1a2a9e0d9548de7635fc1cb338144adc1f)`() const` | 
`public virtual bool `[`train`](#classshogun_1_1CMachine_1aa0ece9fd14892c6dfed1bb8c78f3b3ed)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | train machine
`public virtual bool `[`train_locked`](#classshogun_1_1CMachine_1aab4927bdae8da7f0c85efdfce22c86c2)`()` | Trains a locked machine on a set of indices. Error if machine is not locked 
`public inline virtual bool `[`train_locked`](#classshogun_1_1CMachine_1a6211015eaf19161e4c469c8ff38bfeba)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | Trains a locked machine on a set of indices. Error if machine is not locked
`public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`apply`](#classshogun_1_1CMachine_1afd5d402257972c78456594234d13eb4c)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data if data is not specified apply to the current features
`public virtual `[`CStructuredLabels`](#classshogun_1_1CStructuredLabels)` * `[`apply_structured`](#classshogun_1_1CMachine_1a588efa92a0696e1d2a61a8cd21d8ebee)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data in means of SO classification problem
`public virtual `[`CLatentLabels`](#classshogun_1_1CLatentLabels)` * `[`apply_latent`](#classshogun_1_1CMachine_1a276d23b37202ecb31367df26a5600cf7)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data in means of latent problem
`public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`get_labels`](#classshogun_1_1CMachine_1a065f0797777044cb0dbf786781982e3d)`()` | get labels
`public void `[`set_max_train_time`](#classshogun_1_1CMachine_1af660b1b03c475c3c638d2c995ea4b54a)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` t)` | set maximum training time
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_max_train_time`](#classshogun_1_1CMachine_1a7c75c86ff1cfd61d8275e62f0477d797)`()` | get maximum training time
`public void `[`set_solver_type`](#classshogun_1_1CMachine_1af8876022111114d5d3b0579ee161a8ff)`(`[`ESolverType`](#namespaceshogun_1af43428a9cb6c6de54cc7085c7c9b273e)` st)` | set solver type
`public `[`ESolverType`](#namespaceshogun_1af43428a9cb6c6de54cc7085c7c9b273e)` `[`get_solver_type`](#classshogun_1_1CMachine_1a97ee8b11465427d28498437279229ebe)`()` | get solver type
`public virtual void `[`set_store_model_features`](#classshogun_1_1CMachine_1a872d1cc0904edaa3c5701b049ee2993d)`(bool store_model)` | Setter for store-model-features-after-training flag
`public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`apply_one`](#classshogun_1_1CMachine_1a60afa91e5d08a95aff60510ecad7b59e)`(int32_t i)` | applies to one vector
`public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`apply_locked`](#classshogun_1_1CMachine_1add0cb383e34472fdc66db18b0a5a4bc5)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | Applies a locked machine on a set of indices. Error if machine is not locked
`public virtual `[`CBinaryLabels`](#classshogun_1_1CBinaryLabels)` * `[`apply_locked_binary`](#classshogun_1_1CMachine_1ac417f13423c17ebd9b0aa742f5e78c4c)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | applies a locked machine on a set of indices for binary problems
`public virtual `[`CRegressionLabels`](#classshogun_1_1CRegressionLabels)` * `[`apply_locked_regression`](#classshogun_1_1CMachine_1a764464fca138ac17692cb994824a1d93)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | applies a locked machine on a set of indices for regression problems
`public virtual `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * `[`apply_locked_multiclass`](#classshogun_1_1CMachine_1a9a97b605764f96da5aaadda76a05d21d)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | applies a locked machine on a set of indices for multiclass problems
`public virtual `[`CStructuredLabels`](#classshogun_1_1CStructuredLabels)` * `[`apply_locked_structured`](#classshogun_1_1CMachine_1a8c63b6efbfe361a91794937f6fda544c)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | applies a locked machine on a set of indices for structured problems
`public virtual `[`CLatentLabels`](#classshogun_1_1CLatentLabels)` * `[`apply_locked_latent`](#classshogun_1_1CMachine_1ab4e951edb0bafda3d57fe80d648190d6)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | applies a locked machine on a set of indices for latent problems
`public virtual void `[`data_lock`](#classshogun_1_1CMachine_1a4006ffabe6a752081d3f0e2831ae0c6e)`(`[`CLabels`](#classshogun_1_1CLabels)` * labs,`[`CFeatures`](#classshogun_1_1CFeatures)` * features)` | Locks the machine on given labels and data. After this call, only train_locked and apply_locked may be called
`public inline virtual void `[`post_lock`](#classshogun_1_1CMachine_1a0ad27205b36008a86beb4da016ceef0d)`(`[`CLabels`](#classshogun_1_1CLabels)` * labs,`[`CFeatures`](#classshogun_1_1CFeatures)` * features)` | post lock
`public virtual void `[`data_unlock`](#classshogun_1_1CMachine_1a72933e4edad4e2daabeeafd9f1069e47)`()` | Unlocks a locked machine and restores previous state
`public inline virtual bool `[`supports_locking`](#classshogun_1_1CMachine_1a36e1fd34f65274fa2cf54c3c9b105fcb)`() const` | #### Returns
`public inline bool `[`is_data_locked`](#classshogun_1_1CMachine_1a2996bc9c87fd16414792bca4aa0a14ec)`() const` | #### Returns
`public inline virtual bool `[`train_require_labels`](#classshogun_1_1CMachine_1a47f97bf5de534202ae00e77e485f3740)`() const` | returns whether machine require labels for training
`public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` bool `[`cancel_computation`](#classshogun_1_1CStoppableSGObject_1a107504a021e88eec67012e1706e062c5)`() const` | #### Returns
`public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` void `[`pause_computation`](#classshogun_1_1CStoppableSGObject_1a2168b46919701793fa1558393c30eab4)`()` | Pause the algorithm if the flag is set
`public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` void `[`resume_computation`](#classshogun_1_1CStoppableSGObject_1ab4c36831267ed4c90c5992b45ae33263)`()` | Resume current computation (sets the flag)
`public void `[`set_callback`](#classshogun_1_1CStoppableSGObject_1ab6f4a2a3e5df1521ef427e3fd63f0d21)`(std::function< bool()> callback)` | Set an additional stopping condition 
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
`protected int32_t `[`m_num_inputs`](#classshogun_1_1CNeuralNetwork_1ad7175a3833fb4f78154db13f56a335e7) | number of neurons in the input layer
`protected int32_t `[`m_num_layers`](#classshogun_1_1CNeuralNetwork_1a86b4738d433b735f9ee0f0e5af75fc8b) | number of layer
`protected `[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` * `[`m_layers`](#classshogun_1_1CNeuralNetwork_1ad795d32139fa8c9d1462e9fdb3541302) | network's layers
`protected `[`SGMatrix`](#classshogun_1_1SGMatrix)`< bool > `[`m_adj_matrix`](#classshogun_1_1CNeuralNetwork_1a3a477cee6cf649042f3ed4e39c058038) | Describes the connections in the network: if there's a connection from layer i to layer j then m_adj_matrix(i,j) = 1.
`protected int32_t `[`m_total_num_parameters`](#classshogun_1_1CNeuralNetwork_1ac3f14c5cd11deff0b82a086922988ed6) | total number of parameters in the network
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_params`](#classshogun_1_1CNeuralNetwork_1a95b3dfe8abbc77638c890fd7d90abb56) | array where all the parameters of the network are stored
`protected `[`SGVector`](#classshogun_1_1SGVector)`< bool > `[`m_param_regularizable`](#classshogun_1_1CNeuralNetwork_1a707d5312683ba39938559c579eb1aedf) | Array that specifies which parameters are to be regularized. This is used to turn off regularization for bias parameters
`protected `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`m_index_offsets`](#classshogun_1_1CNeuralNetwork_1a25cbed7bd471fac114418e0ba647f00f) | offsets specifying where each layer's parameters and parameter gradients are stored, i.e layer i's parameters are stored at m_params + m_index_offsets[i]
`protected int32_t `[`m_batch_size`](#classshogun_1_1CNeuralNetwork_1acb2482e04fe13be6830ef0128acd4f68) | number of train/test cases the network is expected to deal with. Default value is 1
`protected bool `[`m_is_training`](#classshogun_1_1CNeuralNetwork_1ab54ccba4ebf6200f64a12eb9c6f9992b) | True if the network is currently being trained initial value is false
`protected bool `[`m_auto_quick_initialize`](#classshogun_1_1CNeuralNetwork_1a0d9982c5532a7edeb3d3e16e9333f591) | True if the network layers are to be quick connected and initialized initial value is False
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_sigma`](#classshogun_1_1CNeuralNetwork_1a1cb9be87291a3d3f3ca4957a6a81d27c) | Standard deviation of the gaussian used to randomly initialize the parameters
`protected `[`ENNOptimizationMethod`](#namespaceshogun_1afc5d4c2c14dc1ccf25e474b4f53c1cf5)` `[`m_optimization_method`](#classshogun_1_1CNeuralNetwork_1abfd89485d8df45b15ff45c6112e3bea5) | Optimization method, default is NNOM_LBFGS
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_l2_coefficient`](#classshogun_1_1CNeuralNetwork_1a18a5328b2456fe3280b47384c23e5129) | L2 Regularization coeff, default value is 0.0
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_l1_coefficient`](#classshogun_1_1CNeuralNetwork_1a324259098e079390a77e1d713baf7315) | L1 Regularization coeff, default value is 0.0
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_dropout_hidden`](#classshogun_1_1CNeuralNetwork_1a3bc0c18dadbeeec2c3593781fdb3b3f7) | Probabilty that a hidden layer neuron will be dropped out When using this, the recommended value is 0.5
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_dropout_input`](#classshogun_1_1CNeuralNetwork_1a816344a964ad8d4327e8c9d6e441b3ab) | Probabilty that a input layer neuron will be dropped out When using this, a good value might be 0.2
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_max_norm`](#classshogun_1_1CNeuralNetwork_1a075bb8a0b9978c4308b2f2071ee709b9) | Maximum allowable L2 norm for a neurons weights When using this, a good value might be 15
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_epsilon`](#classshogun_1_1CNeuralNetwork_1af4806209595723fa21dc4dab36541f45) | convergence criteria training stops when (E'- E)/E < epsilon where E is the error at the current iterations and E' is the error at the previous iteration default value is 1.0e-5
`protected int32_t `[`m_max_num_epochs`](#classshogun_1_1CNeuralNetwork_1acf6bc403f270179fd17a0eb0628d2b16) | maximum number of iterations over the training set. If 0, training will continue until convergence. defualt value is 0
`protected int32_t `[`m_gd_mini_batch_size`](#classshogun_1_1CNeuralNetwork_1abf5ba2ca10463fb6139e8094a5fe61be) | size of the mini-batch used during gradient descent training, if 0 full-batch training is performed default value is 0
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_gd_learning_rate`](#classshogun_1_1CNeuralNetwork_1a8a7c892c0b394f20a87e7c217158408d) | gradient descent learning rate, defualt value 0.1
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_gd_learning_rate_decay`](#classshogun_1_1CNeuralNetwork_1a16690277b66837f868eef7d92b71b572) | gradient descent learning rate decay learning rate is updated at each iteration i according to: alpha(i)=decay*alpha(i-1) default value is 1.0 (no decay)
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_gd_momentum`](#classshogun_1_1CNeuralNetwork_1a4a2d8cf6f933d2c8ee055d8c249ef693) | gradient descent momentum multiplier
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_gd_error_damping_coeff`](#classshogun_1_1CNeuralNetwork_1a887b6161a7f0ff98ea8b9d21cd059ebb) | Used to damp the error fluctuations when stochastic gradient descent is used. damping is done according to: error_damped(i) = c*error(i) + (1-c)*error_damped(i-1) where c is the damping coefficient
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_max_train_time`](#classshogun_1_1CMachine_1a0d6a5a8aca2e1e91685c1ddf23442fd8) | maximum training time
`protected `[`CLabels`](#classshogun_1_1CLabels)` * `[`m_labels`](#classshogun_1_1CMachine_1af3451cc972288f8c92ef7369952b805b) | labels
`protected `[`ESolverType`](#namespaceshogun_1af43428a9cb6c6de54cc7085c7c9b273e)` `[`m_solver_type`](#classshogun_1_1CMachine_1a4cc9c480f9e3535d05837670a124c080) | solver type
`protected bool `[`m_store_model_features`](#classshogun_1_1CMachine_1ac359a14e48915341e9dd44c8fee21ac6) | whether model features should be stored after training
`protected bool `[`m_data_locked`](#classshogun_1_1CMachine_1a93d71ccf0a5f7a1dad42f35dd7b932e2) | whether data is locked
`protected std::atomic< bool > `[`m_cancel_computation`](#classshogun_1_1CStoppableSGObject_1a263b9ed7fb7b659634a6182daa5e4d33) | Cancel computation
`protected std::atomic< bool > `[`m_pause_computation_flag`](#classshogun_1_1CStoppableSGObject_1a7054f653d8ec45c524c1137d24fd66df) | Pause computation flag
`protected std::condition_variable `[`m_pause_computation`](#classshogun_1_1CStoppableSGObject_1af0e6de5887e6f425f0b62b34e62bcf5d) | Conditional variable to make threads wait
`protected std::mutex `[`m_mutex`](#classshogun_1_1CStoppableSGObject_1a5c751dae9068bdb864af14129bbe0fa1) | Mutex used to pause threads
`protected std::function< bool(void)> `[`m_callback`](#classshogun_1_1CStoppableSGObject_1ac68af0b9914ee5a4159295e140cb906c) | 
`protected virtual bool `[`train_machine`](#classshogun_1_1CNeuralNetwork_1ac6ad4326a1641cb16d8d74d2ac00e9d3)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | trains the network
`protected virtual bool `[`train_gradient_descent`](#classshogun_1_1CNeuralNetwork_1ab5a71a0198cf40f7e1ccbb4f30a490a8)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > inputs,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > targets)` | trains the network using gradient descent
`protected virtual bool `[`train_lbfgs`](#classshogun_1_1CNeuralNetwork_1a0ae46f9e8ae7c5151685b25664542a22)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > inputs,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > targets)` | trains the network using L-BFGS
`protected virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`forward_propagate`](#classshogun_1_1CNeuralNetwork_1a3501eb1009bfa0ad1b2620ea63eb9c0c)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data,int32_t j)` | Applies forward propagation, computes the activations of each layer up to layer j
`protected virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`forward_propagate`](#classshogun_1_1CNeuralNetwork_1a8637dcdff043906fa36b86d1948091d1)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > inputs,int32_t j)` | Applies forward propagation, computes the activations of each layer up to layer j
`protected virtual void `[`set_batch_size`](#classshogun_1_1CNeuralNetwork_1a2fb212dd86732ebf70f0a692257422d5)`(int32_t batch_size)` | Sets the batch size (the number of train/test cases) the network is expected to deal with. Allocates memory for the activations, local gradients, input gradients if necessary (if the batch size is different from it's previous value)
`protected virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_gradients`](#classshogun_1_1CNeuralNetwork_1a6ba743f03a2c0ccd09eff57b8a0f7cd2)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > inputs,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > targets,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > gradients)` | Applies backpropagation to compute the gradients of the error with repsect to every parameter in the network.
`protected virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_error`](#classshogun_1_1CNeuralNetwork_1aa2b92865fc0e056843a501301209eebf)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > inputs,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > targets)` | Forward propagates the inputs and computes the error between the output layer's activations and the given target activations.
`protected virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_error`](#classshogun_1_1CNeuralNetwork_1a0cb7071826ea91246031bc9ace734cc3)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > targets)` | Computes the error between the output layer's activations and the given target activations.
`protected virtual bool `[`is_label_valid`](#classshogun_1_1CNeuralNetwork_1abc2e336339ace0a7656f4822a98fad0a)`(`[`CLabels`](#classshogun_1_1CLabels)` * lab) const` | check whether the labels is valid.
`protected `[`CNeuralLayer`](#classshogun_1_1CNeuralLayer)` * `[`get_layer`](#classshogun_1_1CNeuralNetwork_1af03c8141230ae1ccd4a43a81babe193c)`(int32_t i)` | returns a pointer to layer i in the network
`protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`features_to_matrix`](#classshogun_1_1CNeuralNetwork_1a222f7b1543b027e556d35e65dd66e864)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * features)` | Ensures the given features are suitable for use with the network and returns their feature matrix
`protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`labels_to_matrix`](#classshogun_1_1CNeuralNetwork_1a24a7aa21cfa7aebcf3debaa523405fb1)`(`[`CLabels`](#classshogun_1_1CLabels)` * labs)` | converts the given labels into a matrix suitable for use with network
`protected inline virtual bool `[`train_dense`](#classshogun_1_1CMachine_1a2f4984079885c8a49f40fc6bc8366d67)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | 
`protected inline virtual bool `[`train_string`](#classshogun_1_1CMachine_1aa7f306efec16f95e741472046dee440d)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | 
`protected inline virtual bool `[`support_feature_dispatching`](#classshogun_1_1CMachine_1a6d0cdca08d31651c73d028199634bb6e)`()` | 
`protected inline virtual bool `[`support_dense_dispatching`](#classshogun_1_1CMachine_1a44486c95636e8e11e3fd83fc8073a860)`()` | 
`protected inline virtual bool `[`support_string_dispatching`](#classshogun_1_1CMachine_1a3f800163b86742f0edfdabf452a627f8)`()` | 
`protected inline virtual bool `[`continue_train`](#classshogun_1_1CMachine_1a0d918d8b628c91f0c22f2a623b495812)`()` | Continue Training
`protected inline virtual void `[`store_model_features`](#classshogun_1_1CMachine_1ae0a84ada96561ce09c35e2839f8ca512)`()` | Stores feature data of underlying model. After this method has been called, it is possible to change the machine's feature data and call [apply()](#classshogun_1_1CMachine_1afd5d402257972c78456594234d13eb4c), which is then performed on the training feature data that is part of the machine's model.
`protected rxcpp::subscription `[`connect_to_signal_handler`](#classshogun_1_1CStoppableSGObject_1a4e732c6748fe2895f401c66647863e39)`()` | connect the machine instance to the signal handler
`protected void `[`reset_computation_variables`](#classshogun_1_1CStoppableSGObject_1ae1ce696f8c07b4884cbc1311fd9f5a37)`()` | reset the computation variables
`protected void `[`on_next`](#classshogun_1_1CStoppableSGObject_1a4362088c65601a14e98c19c9f0b48034)`()` | sets cancel computation flag
`protected virtual void `[`on_next_impl`](#classshogun_1_1CStoppableSGObject_1aecd947301711b0871ecc7e4608e2e794)`()` | The action which will be done when the user decides to premature stop the [CMachine](#classshogun_1_1CMachine) execution
`protected void `[`on_pause`](#classshogun_1_1CStoppableSGObject_1aae61636109c2e67b8313c19b639c8dcd)`()` | sets pause computation flag and resumes after action is complete
`protected virtual void `[`on_pause_impl`](#classshogun_1_1CStoppableSGObject_1a2fa805bcc33be124bea5b51cd9353524)`()` | The action which will be done when the user decides to pause the [CMachine](#classshogun_1_1CMachine) execution
`protected void `[`on_complete`](#classshogun_1_1CStoppableSGObject_1a4f7551e636a9ecc3826dd729b219e532)`()` | These actions which will be done when the user decides to return to prompt and terminate the program execution
`protected virtual void `[`on_complete_impl`](#classshogun_1_1CStoppableSGObject_1a0aac1762c8df8870a5242a710457c6a3)`()` | 
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

#### `public  `[`CNeuralNetwork`](#classshogun_1_1CNeuralNetwork_1a0ea77cbc69188e84fe6593e88878a61e)`()` {#classshogun_1_1CNeuralNetwork_1a0ea77cbc69188e84fe6593e88878a61e}

default constuctor

#### `public  `[`CNeuralNetwork`](#classshogun_1_1CNeuralNetwork_1a1cb686914ea6786bc2819f41dfcebdee)`(`[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` * layers)` {#classshogun_1_1CNeuralNetwork_1a1cb686914ea6786bc2819f41dfcebdee}

Sets the layers of the network

#### Parameters
* `layers` An array of [CNeuralLayer](#classshogun_1_1CNeuralLayer) objects specifying the layers of the network. Must contain at least one input layer. The last layer in the array is treated as the output layer

#### `public virtual void `[`set_layers`](#classshogun_1_1CNeuralNetwork_1a2cefbd8c2c469b0fb8d8fca4cde9e82b)`(`[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` * layers)` {#classshogun_1_1CNeuralNetwork_1a2cefbd8c2c469b0fb8d8fca4cde9e82b}

Sets the layers of the network

#### Parameters
* `layers` An array of [CNeuralLayer](#classshogun_1_1CNeuralLayer) objects specifying the layers of the network. Must contain at least one input layer. The last layer in the array is treated as the output layer

#### `public virtual void `[`connect`](#classshogun_1_1CNeuralNetwork_1a82f8cdcc3b5cb1d13fb986a217c299ce)`(int32_t i,int32_t j)` {#classshogun_1_1CNeuralNetwork_1a82f8cdcc3b5cb1d13fb986a217c299ce}

Connects layer i as input to layer j. In order for forward and backpropagation to work correctly, i must be less that j

#### `public virtual void `[`init_adj_matrix`](#classshogun_1_1CNeuralNetwork_1afac54e76bbf5cf17669bd25add587b4b)`()` {#classshogun_1_1CNeuralNetwork_1afac54e76bbf5cf17669bd25add587b4b}

Initialize adjacency matrix

#### `public virtual void `[`quick_connect`](#classshogun_1_1CNeuralNetwork_1a06e9e9cc5c2425123911ea0f5805c1ef)`()` {#classshogun_1_1CNeuralNetwork_1a06e9e9cc5c2425123911ea0f5805c1ef}

Connects each layer to the layer after it. That is, connects layer i to as input to layer i+1 for all i.

#### `public virtual void `[`disconnect`](#classshogun_1_1CNeuralNetwork_1a1f0f1f3df5f8d0b1bb0c959be11d95e8)`(int32_t i,int32_t j)` {#classshogun_1_1CNeuralNetwork_1a1f0f1f3df5f8d0b1bb0c959be11d95e8}

Disconnects layer i from layer j

#### `public virtual void `[`disconnect_all`](#classshogun_1_1CNeuralNetwork_1a02922e7231c3a315b2bfd1049b675365)`()` {#classshogun_1_1CNeuralNetwork_1a02922e7231c3a315b2bfd1049b675365}

Removes all connections in the network

#### `public virtual void `[`initialize_neural_network`](#classshogun_1_1CNeuralNetwork_1ad305d5766182085e6f9dba86684c5900)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` sigma)` {#classshogun_1_1CNeuralNetwork_1ad305d5766182085e6f9dba86684c5900}

Initializes the network

#### Parameters
* `sigma` standard deviation of the gaussian used to randomly initialize the parameters

#### `public virtual  `[`~CNeuralNetwork`](#classshogun_1_1CNeuralNetwork_1a660c12934593583eb75b597f10417113)`()` {#classshogun_1_1CNeuralNetwork_1a660c12934593583eb75b597f10417113}

#### `public virtual `[`CBinaryLabels`](#classshogun_1_1CBinaryLabels)` * `[`apply_binary`](#classshogun_1_1CNeuralNetwork_1aaffb86a617d7acafe814302fe05b8132)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CNeuralNetwork_1aaffb86a617d7acafe814302fe05b8132}

apply machine to data in means of binary classification problem

#### `public virtual `[`CRegressionLabels`](#classshogun_1_1CRegressionLabels)` * `[`apply_regression`](#classshogun_1_1CNeuralNetwork_1a5583c1b05368a6addb730420fbc43ac9)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CNeuralNetwork_1a5583c1b05368a6addb730420fbc43ac9}

apply machine to data in means of regression problem

#### `public virtual `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * `[`apply_multiclass`](#classshogun_1_1CNeuralNetwork_1a860ce9657aa41604154212b7f1f422d3)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CNeuralNetwork_1a860ce9657aa41604154212b7f1f422d3}

apply machine to data in means of multiclass classification problem

#### `public virtual `[`CDenseFeatures](#classshogun_1_1CDenseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * `[`transform`](#classshogun_1_1CNeuralNetwork_1a9b315544d06f0a0fe6f6f6113466bd83)`(`[`CDenseFeatures](#classshogun_1_1CDenseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * data)` {#classshogun_1_1CNeuralNetwork_1a9b315544d06f0a0fe6f6f6113466bd83}

Applies the network as a feature transformation

Forward-propagates the data through the network and returns the activations of the last layer

#### Parameters
* `data` Input features

#### Returns
Transformed features

#### `public virtual void `[`set_labels`](#classshogun_1_1CNeuralNetwork_1a5f0cfd09e37bd5e793cacecb8d3c818b)`(`[`CLabels`](#classshogun_1_1CLabels)` * lab)` {#classshogun_1_1CNeuralNetwork_1a5f0cfd09e37bd5e793cacecb8d3c818b}

set labels

#### Parameters
* `lab` labels

#### `public inline virtual `[`EMachineType`](#namespaceshogun_1af181c832c12de7a0c3b02425986106cc)` `[`get_classifier_type`](#classshogun_1_1CNeuralNetwork_1ab0ee71eb4f9097a9b7ad2b72b1b310e2)`()` {#classshogun_1_1CNeuralNetwork_1ab0ee71eb4f9097a9b7ad2b72b1b310e2}

get classifier type

#### Returns
classifier type CT_NEURALNETWORK

#### `public virtual `[`EProblemType`](#namespaceshogun_1a0aa89aa872f89f6a174de2f45b7596d4)` `[`get_machine_problem_type`](#classshogun_1_1CNeuralNetwork_1a135f8d82da3fc55807d1640080358500)`() const` {#classshogun_1_1CNeuralNetwork_1a135f8d82da3fc55807d1640080358500}

returns type of problem machine solves

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`check_gradients`](#classshogun_1_1CNeuralNetwork_1a774aef9dd4054b1f7608c859688b8334)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` approx_epsilon,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` s)` {#classshogun_1_1CNeuralNetwork_1a774aef9dd4054b1f7608c859688b8334}

Checks if the gradients computed using backpropagation are correct by comparing them with gradients computed using numerical approximation. Used for testing purposes only.

Gradients are numerically approximated according to: 
$$
c = max(\epsilon x, s)
$$

$$
f'(x) = \frac{f(x + c)-f(x - c)}{2c}
$$

#### Parameters
* `approx_epsilon` Constant used during gradient approximation

* `s` [Some](#classshogun_1_1Some) small value, used to prevent division by zero

#### Returns
Average difference between numerical gradients and backpropagation gradients

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * `[`get_layer_parameters`](#classshogun_1_1CNeuralNetwork_1a26a5fe12bb334b92478462a020d6c3ed)`(int32_t i)` {#classshogun_1_1CNeuralNetwork_1a26a5fe12bb334b92478462a020d6c3ed}

returns a copy of a layer's parameters array

#### Parameters
* `i` index of the layer

#### `public inline int32_t `[`get_num_parameters`](#classshogun_1_1CNeuralNetwork_1a3adb14d9f900d24099dd289ea25480b8)`()` {#classshogun_1_1CNeuralNetwork_1a3adb14d9f900d24099dd289ea25480b8}

returns the totat number of parameters in the network

#### `public inline `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_parameters`](#classshogun_1_1CNeuralNetwork_1a9f8ebaa5d6a822e29b39133c5c8b668f)`()` {#classshogun_1_1CNeuralNetwork_1a9f8ebaa5d6a822e29b39133c5c8b668f}

return the network's parameter array

#### `public inline int32_t `[`get_num_inputs`](#classshogun_1_1CNeuralNetwork_1a2684a371ae1b5fc6dd2b2189b26c1e47)`()` {#classshogun_1_1CNeuralNetwork_1a2684a371ae1b5fc6dd2b2189b26c1e47}

returns the number of inputs the network takes

#### `public int32_t `[`get_num_outputs`](#classshogun_1_1CNeuralNetwork_1a6d88ac18968e25f18aee7f3241234db2)`()` {#classshogun_1_1CNeuralNetwork_1a6d88ac18968e25f18aee7f3241234db2}

returns the number of neurons in the output layer

#### `public `[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` * `[`get_layers`](#classshogun_1_1CNeuralNetwork_1af83006457e52d5fd9a6fe69d132bf8a9)`()` {#classshogun_1_1CNeuralNetwork_1af83006457e52d5fd9a6fe69d132bf8a9}

Returns an array holding the network's layers

#### `public inline virtual const char * `[`get_name`](#classshogun_1_1CNeuralNetwork_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` {#classshogun_1_1CNeuralNetwork_1a9cb485686dd7a1e6f7103cf42e87717e}

Returns the name of the SGSerializable instance. It MUST BE the CLASS NAME without the prefixed `C'.

#### Returns
name of the SGSerializable

#### `public inline void `[`set_optimization_method`](#classshogun_1_1CNeuralNetwork_1ae6c3a26d80235c8a3595809224b9dd00)`(`[`ENNOptimizationMethod`](#namespaceshogun_1afc5d4c2c14dc1ccf25e474b4f53c1cf5)` optimization_method)` {#classshogun_1_1CNeuralNetwork_1ae6c3a26d80235c8a3595809224b9dd00}

Sets optimization method default is NNOM_LBFGS 
#### Parameters
* `optimization_method` optimiation method

#### `public inline `[`ENNOptimizationMethod`](#namespaceshogun_1afc5d4c2c14dc1ccf25e474b4f53c1cf5)` `[`get_optimization_method`](#classshogun_1_1CNeuralNetwork_1a08d3efa11428d74e677325ad76a0fe14)`() const` {#classshogun_1_1CNeuralNetwork_1a08d3efa11428d74e677325ad76a0fe14}

Returns optimization method

#### `public inline void `[`set_l2_coefficient`](#classshogun_1_1CNeuralNetwork_1a7ec86f645fdaaf951533dc00000444f1)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` l2_coefficient)` {#classshogun_1_1CNeuralNetwork_1a7ec86f645fdaaf951533dc00000444f1}

Sets L2 Regularization coeff default value is 0.0 
#### Parameters
* `l2_coefficient` l2_coefficient

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_l2_coefficient`](#classshogun_1_1CNeuralNetwork_1ab75edf716ce15352435bb24e3371cb44)`() const` {#classshogun_1_1CNeuralNetwork_1ab75edf716ce15352435bb24e3371cb44}

Returns L2 coefficient

#### `public inline void `[`set_l1_coefficient`](#classshogun_1_1CNeuralNetwork_1a22ba708c3403575afc5ade0b6709839f)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` l1_coefficient)` {#classshogun_1_1CNeuralNetwork_1a22ba708c3403575afc5ade0b6709839f}

Sets L1 Regularization coeff default value is 0.0 
#### Parameters
* `l1_coefficient` l1_coefficient

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_l1_coefficient`](#classshogun_1_1CNeuralNetwork_1a583b67b124b3bd0e0b9656beeb02949a)`() const` {#classshogun_1_1CNeuralNetwork_1a583b67b124b3bd0e0b9656beeb02949a}

Returns L1 coefficient

#### `public inline void `[`set_dropout_hidden`](#classshogun_1_1CNeuralNetwork_1ac750d47359f6d479349e3441cf9b6527)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` dropout_hidden)` {#classshogun_1_1CNeuralNetwork_1ac750d47359f6d479349e3441cf9b6527}

Sets the probabilty that a hidden layer neuron will be dropped out When using this, the recommended value is 0.5 default value 0.0 (no dropout)

For more details on dropout, see [paper]([http://arxiv.org/abs/1207.0580](http://arxiv.org/abs/1207.0580)) [Hinton, 2012]

#### Parameters
* `dropout_hidden` dropout probability

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_dropout_hidden`](#classshogun_1_1CNeuralNetwork_1a15209c974f555786c713975b05d55ccd)`() const` {#classshogun_1_1CNeuralNetwork_1a15209c974f555786c713975b05d55ccd}

Returns dropout probability for hidden layers

#### `public inline void `[`set_dropout_input`](#classshogun_1_1CNeuralNetwork_1ae5630682b9c8f2d1d2bf5e4757b512cc)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` dropout_input)` {#classshogun_1_1CNeuralNetwork_1ae5630682b9c8f2d1d2bf5e4757b512cc}

Sets the probabilty that an input layer neuron will be dropped out When using this, a good value might be 0.2 default value 0.0 (no dropout)

For more details on dropout, see this [paper]([http://arxiv.org/abs/1207.0580](http://arxiv.org/abs/1207.0580)) [Hinton, 2012]

#### Parameters
* `dropout_input` dropout probability

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_dropout_input`](#classshogun_1_1CNeuralNetwork_1a16ff92cd8240b9bfc7c1697b6b23b0dd)`() const` {#classshogun_1_1CNeuralNetwork_1a16ff92cd8240b9bfc7c1697b6b23b0dd}

Returns dropout probability for input layers

#### `public inline void `[`set_max_norm`](#classshogun_1_1CNeuralNetwork_1a4659677f77dfa3b8d56c090b81b02031)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` max_norm)` {#classshogun_1_1CNeuralNetwork_1a4659677f77dfa3b8d56c090b81b02031}

Sets maximum allowable L2 norm for a neurons weights When using this, a good value might be 15 default value -1 (max-norm regularization disabled) 
#### Parameters
* `max_norm` maximum allowable L2 norm

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_max_norm`](#classshogun_1_1CNeuralNetwork_1a93384fb1df0b2359ef76dc15034f4575)`() const` {#classshogun_1_1CNeuralNetwork_1a93384fb1df0b2359ef76dc15034f4575}

Returns maximum allowable L2 norm

#### `public inline void `[`set_epsilon`](#classshogun_1_1CNeuralNetwork_1a3b8392d8584df5bdba1d4af92346db31)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` epsilon)` {#classshogun_1_1CNeuralNetwork_1a3b8392d8584df5bdba1d4af92346db31}

Sets convergence criteria training stops when (E'- E)/E < epsilon where E is the error at the current iterations and E' is the error at the previous iteration default value is 1.0e-5 
#### Parameters
* `epsilon` convergence criteria

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_epsilon`](#classshogun_1_1CNeuralNetwork_1a0813512911649cc6fa462bad06b877ee)`() const` {#classshogun_1_1CNeuralNetwork_1a0813512911649cc6fa462bad06b877ee}

Returns epsilon

#### `public inline void `[`set_max_num_epochs`](#classshogun_1_1CNeuralNetwork_1a911c489977144f76ed52f213d4c56ba4)`(int32_t max_num_epochs)` {#classshogun_1_1CNeuralNetwork_1a911c489977144f76ed52f213d4c56ba4}

Sets maximum number of iterations over the training set. If 0, training will continue until convergence. defualt value is 0 
#### Parameters
* `max_num_epochs` maximum number of iterations over the training set

#### `public inline int32_t `[`get_max_num_epochs`](#classshogun_1_1CNeuralNetwork_1a36b6b29dd7e2ec95a593d18d2a9d78a8)`() const` {#classshogun_1_1CNeuralNetwork_1a36b6b29dd7e2ec95a593d18d2a9d78a8}

Returns maximum number of epochs

#### `public inline void `[`set_gd_mini_batch_size`](#classshogun_1_1CNeuralNetwork_1abd80a633223bdbc84ddf4d3c96fcd6d7)`(int32_t gd_mini_batch_size)` {#classshogun_1_1CNeuralNetwork_1abd80a633223bdbc84ddf4d3c96fcd6d7}

Sets size of the mini-batch used during gradient descent training, if 0 full-batch training is performed default value is 0 
#### Parameters
* `gd_mini_batch_size` mini batch size

#### `public inline int32_t `[`get_gd_mini_batch_size`](#classshogun_1_1CNeuralNetwork_1a71b79ef9e968280ea329a508bd0e2658)`() const` {#classshogun_1_1CNeuralNetwork_1a71b79ef9e968280ea329a508bd0e2658}

Returns mini batch size

#### `public inline void `[`set_gd_learning_rate`](#classshogun_1_1CNeuralNetwork_1ace44b3eef4895e16124e247a541354d1)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` gd_learning_rate)` {#classshogun_1_1CNeuralNetwork_1ace44b3eef4895e16124e247a541354d1}

Sets gradient descent learning rate defualt value 0.1 
#### Parameters
* `gd_learning_rate` gradient descent learning rate

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_gd_learning_rate`](#classshogun_1_1CNeuralNetwork_1a04a39cfec3a58b2e02f09bbfa35ba478)`() const` {#classshogun_1_1CNeuralNetwork_1a04a39cfec3a58b2e02f09bbfa35ba478}

Returns gradient descent learning rate

#### `public inline void `[`set_gd_learning_rate_decay`](#classshogun_1_1CNeuralNetwork_1afdfe04cff6e60176db27bd93196c96f2)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` gd_learning_rate_decay)` {#classshogun_1_1CNeuralNetwork_1afdfe04cff6e60176db27bd93196c96f2}

Sets gradient descent learning rate decay learning rate is updated at each iteration i according to: alpha(i)=decay*alpha(i-1) default value is 1.0 (no decay) 
#### Parameters
* `gd_learning_rate_decay` gradient descent learning rate decay

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_gd_learning_rate_decay`](#classshogun_1_1CNeuralNetwork_1a178443fc53cb12f120dbfc81dd5c2daf)`() const` {#classshogun_1_1CNeuralNetwork_1a178443fc53cb12f120dbfc81dd5c2daf}

Returns gradient descent learning rate decay

#### `public inline void `[`set_gd_momentum`](#classshogun_1_1CNeuralNetwork_1a82e0a2cb6f405d6697ca522c9ad7d77d)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` gd_momentum)` {#classshogun_1_1CNeuralNetwork_1a82e0a2cb6f405d6697ca522c9ad7d77d}

Sets gradient descent momentum multiplier

default value is 0.9

For more details on momentum, see this [paper]([http://jmlr.org/proceedings/papers/v28/sutskever13.html](http://jmlr.org/proceedings/papers/v28/sutskever13.html)) [Sutskever, 2013]

#### Parameters
* `gd_momentum` gradient descent momentum multiplier

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_gd_momentum`](#classshogun_1_1CNeuralNetwork_1af6a017a8771ae55dc3aa77546757d204)`() const` {#classshogun_1_1CNeuralNetwork_1af6a017a8771ae55dc3aa77546757d204}

Returns gradient descent momentum multiplier

#### `public inline void `[`set_gd_error_damping_coeff`](#classshogun_1_1CNeuralNetwork_1a32bc669352d1b4d22a75d1fe4a8a9175)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` gd_error_damping_coeff)` {#classshogun_1_1CNeuralNetwork_1a32bc669352d1b4d22a75d1fe4a8a9175}

Sets gradient descent error damping coefficient Used to damp the error fluctuations when stochastic gradient descent is used. damping is done according to: error_damped(i) = c*error(i) + (1-c)*error_damped(i-1) where c is the damping coefficient

If -1, the damping coefficient is automatically computed according to: c = 0.99*gd_mini_batch_size/training_set_size + 1e-2;

default value is -1

#### Parameters
* `gd_error_damping_coeff` error damping coefficient

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_gd_error_damping_coeff`](#classshogun_1_1CNeuralNetwork_1a2a9e0d9548de7635fc1cb338144adc1f)`() const` {#classshogun_1_1CNeuralNetwork_1a2a9e0d9548de7635fc1cb338144adc1f}

#### `public virtual bool `[`train`](#classshogun_1_1CMachine_1aa0ece9fd14892c6dfed1bb8c78f3b3ed)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMachine_1aa0ece9fd14892c6dfed1bb8c78f3b3ed}

train machine

#### Parameters
* `data` training data (parameter can be avoided if distance or kernel-based classifiers are used and distance/kernels are initialized with train data). If flag is set, model features will be stored after training.

#### Returns
whether training was successful

#### `public virtual bool `[`train_locked`](#classshogun_1_1CMachine_1aab4927bdae8da7f0c85efdfce22c86c2)`()` {#classshogun_1_1CMachine_1aab4927bdae8da7f0c85efdfce22c86c2}

Trains a locked machine on a set of indices. Error if machine is not locked 
#### Returns
whether training was successful

#### `public inline virtual bool `[`train_locked`](#classshogun_1_1CMachine_1a6211015eaf19161e4c469c8ff38bfeba)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CMachine_1a6211015eaf19161e4c469c8ff38bfeba}

Trains a locked machine on a set of indices. Error if machine is not locked

NOT IMPLEMENTED

#### Parameters
* `indices` index vector (of locked features) that is used for training 

#### Returns
whether training was successful

#### `public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`apply`](#classshogun_1_1CMachine_1afd5d402257972c78456594234d13eb4c)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMachine_1afd5d402257972c78456594234d13eb4c}

apply machine to data if data is not specified apply to the current features

#### Parameters
* `data` (test)data to be classified 

#### Returns
classified labels

#### `public virtual `[`CStructuredLabels`](#classshogun_1_1CStructuredLabels)` * `[`apply_structured`](#classshogun_1_1CMachine_1a588efa92a0696e1d2a61a8cd21d8ebee)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMachine_1a588efa92a0696e1d2a61a8cd21d8ebee}

apply machine to data in means of SO classification problem

#### `public virtual `[`CLatentLabels`](#classshogun_1_1CLatentLabels)` * `[`apply_latent`](#classshogun_1_1CMachine_1a276d23b37202ecb31367df26a5600cf7)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMachine_1a276d23b37202ecb31367df26a5600cf7}

apply machine to data in means of latent problem

#### `public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`get_labels`](#classshogun_1_1CMachine_1a065f0797777044cb0dbf786781982e3d)`()` {#classshogun_1_1CMachine_1a065f0797777044cb0dbf786781982e3d}

get labels

#### Returns
labels

#### `public void `[`set_max_train_time`](#classshogun_1_1CMachine_1af660b1b03c475c3c638d2c995ea4b54a)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` t)` {#classshogun_1_1CMachine_1af660b1b03c475c3c638d2c995ea4b54a}

set maximum training time

#### Parameters
* `t` maximimum training time

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_max_train_time`](#classshogun_1_1CMachine_1a7c75c86ff1cfd61d8275e62f0477d797)`()` {#classshogun_1_1CMachine_1a7c75c86ff1cfd61d8275e62f0477d797}

get maximum training time

#### Returns
maximum training time

#### `public void `[`set_solver_type`](#classshogun_1_1CMachine_1af8876022111114d5d3b0579ee161a8ff)`(`[`ESolverType`](#namespaceshogun_1af43428a9cb6c6de54cc7085c7c9b273e)` st)` {#classshogun_1_1CMachine_1af8876022111114d5d3b0579ee161a8ff}

set solver type

#### Parameters
* `st` solver type

#### `public `[`ESolverType`](#namespaceshogun_1af43428a9cb6c6de54cc7085c7c9b273e)` `[`get_solver_type`](#classshogun_1_1CMachine_1a97ee8b11465427d28498437279229ebe)`()` {#classshogun_1_1CMachine_1a97ee8b11465427d28498437279229ebe}

get solver type

#### Returns
solver

#### `public virtual void `[`set_store_model_features`](#classshogun_1_1CMachine_1a872d1cc0904edaa3c5701b049ee2993d)`(bool store_model)` {#classshogun_1_1CMachine_1a872d1cc0904edaa3c5701b049ee2993d}

Setter for store-model-features-after-training flag

#### Parameters
* `store_model` whether model should be stored after training

#### `public inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`apply_one`](#classshogun_1_1CMachine_1a60afa91e5d08a95aff60510ecad7b59e)`(int32_t i)` {#classshogun_1_1CMachine_1a60afa91e5d08a95aff60510ecad7b59e}

applies to one vector

#### `public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`apply_locked`](#classshogun_1_1CMachine_1add0cb383e34472fdc66db18b0a5a4bc5)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CMachine_1add0cb383e34472fdc66db18b0a5a4bc5}

Applies a locked machine on a set of indices. Error if machine is not locked

#### Parameters
* `indices` index vector (of locked features) that is predicted

#### `public virtual `[`CBinaryLabels`](#classshogun_1_1CBinaryLabels)` * `[`apply_locked_binary`](#classshogun_1_1CMachine_1ac417f13423c17ebd9b0aa742f5e78c4c)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CMachine_1ac417f13423c17ebd9b0aa742f5e78c4c}

applies a locked machine on a set of indices for binary problems

#### `public virtual `[`CRegressionLabels`](#classshogun_1_1CRegressionLabels)` * `[`apply_locked_regression`](#classshogun_1_1CMachine_1a764464fca138ac17692cb994824a1d93)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CMachine_1a764464fca138ac17692cb994824a1d93}

applies a locked machine on a set of indices for regression problems

#### `public virtual `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * `[`apply_locked_multiclass`](#classshogun_1_1CMachine_1a9a97b605764f96da5aaadda76a05d21d)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CMachine_1a9a97b605764f96da5aaadda76a05d21d}

applies a locked machine on a set of indices for multiclass problems

#### `public virtual `[`CStructuredLabels`](#classshogun_1_1CStructuredLabels)` * `[`apply_locked_structured`](#classshogun_1_1CMachine_1a8c63b6efbfe361a91794937f6fda544c)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CMachine_1a8c63b6efbfe361a91794937f6fda544c}

applies a locked machine on a set of indices for structured problems

#### `public virtual `[`CLatentLabels`](#classshogun_1_1CLatentLabels)` * `[`apply_locked_latent`](#classshogun_1_1CMachine_1ab4e951edb0bafda3d57fe80d648190d6)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CMachine_1ab4e951edb0bafda3d57fe80d648190d6}

applies a locked machine on a set of indices for latent problems

#### `public virtual void `[`data_lock`](#classshogun_1_1CMachine_1a4006ffabe6a752081d3f0e2831ae0c6e)`(`[`CLabels`](#classshogun_1_1CLabels)` * labs,`[`CFeatures`](#classshogun_1_1CFeatures)` * features)` {#classshogun_1_1CMachine_1a4006ffabe6a752081d3f0e2831ae0c6e}

Locks the machine on given labels and data. After this call, only train_locked and apply_locked may be called

Only possible if [supports_locking()](#classshogun_1_1CMachine_1a36e1fd34f65274fa2cf54c3c9b105fcb) returns true

#### Parameters
* `labs` labels used for locking 

* `features` features used for locking

#### `public inline virtual void `[`post_lock`](#classshogun_1_1CMachine_1a0ad27205b36008a86beb4da016ceef0d)`(`[`CLabels`](#classshogun_1_1CLabels)` * labs,`[`CFeatures`](#classshogun_1_1CFeatures)` * features)` {#classshogun_1_1CMachine_1a0ad27205b36008a86beb4da016ceef0d}

post lock

#### `public virtual void `[`data_unlock`](#classshogun_1_1CMachine_1a72933e4edad4e2daabeeafd9f1069e47)`()` {#classshogun_1_1CMachine_1a72933e4edad4e2daabeeafd9f1069e47}

Unlocks a locked machine and restores previous state

#### `public inline virtual bool `[`supports_locking`](#classshogun_1_1CMachine_1a36e1fd34f65274fa2cf54c3c9b105fcb)`() const` {#classshogun_1_1CMachine_1a36e1fd34f65274fa2cf54c3c9b105fcb}

#### Returns
whether this machine supports locking

#### `public inline bool `[`is_data_locked`](#classshogun_1_1CMachine_1a2996bc9c87fd16414792bca4aa0a14ec)`() const` {#classshogun_1_1CMachine_1a2996bc9c87fd16414792bca4aa0a14ec}

#### Returns
whether this machine is locked

#### `public inline virtual bool `[`train_require_labels`](#classshogun_1_1CMachine_1a47f97bf5de534202ae00e77e485f3740)`() const` {#classshogun_1_1CMachine_1a47f97bf5de534202ae00e77e485f3740}

returns whether machine require labels for training

#### `public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` bool `[`cancel_computation`](#classshogun_1_1CStoppableSGObject_1a107504a021e88eec67012e1706e062c5)`() const` {#classshogun_1_1CStoppableSGObject_1a107504a021e88eec67012e1706e062c5}

#### Returns
whether the algorithm needs to be stopped

#### `public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` void `[`pause_computation`](#classshogun_1_1CStoppableSGObject_1a2168b46919701793fa1558393c30eab4)`()` {#classshogun_1_1CStoppableSGObject_1a2168b46919701793fa1558393c30eab4}

Pause the algorithm if the flag is set

#### `public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` void `[`resume_computation`](#classshogun_1_1CStoppableSGObject_1ab4c36831267ed4c90c5992b45ae33263)`()` {#classshogun_1_1CStoppableSGObject_1ab4c36831267ed4c90c5992b45ae33263}

Resume current computation (sets the flag)

#### `public void `[`set_callback`](#classshogun_1_1CStoppableSGObject_1ab6f4a2a3e5df1521ef427e3fd63f0d21)`(std::function< bool()> callback)` {#classshogun_1_1CStoppableSGObject_1ab6f4a2a3e5df1521ef427e3fd63f0d21}

Set an additional stopping condition 
#### Parameters
* `callback` method that implements an additional stopping condition

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

#### `protected int32_t `[`m_num_inputs`](#classshogun_1_1CNeuralNetwork_1ad7175a3833fb4f78154db13f56a335e7) {#classshogun_1_1CNeuralNetwork_1ad7175a3833fb4f78154db13f56a335e7}

number of neurons in the input layer

#### `protected int32_t `[`m_num_layers`](#classshogun_1_1CNeuralNetwork_1a86b4738d433b735f9ee0f0e5af75fc8b) {#classshogun_1_1CNeuralNetwork_1a86b4738d433b735f9ee0f0e5af75fc8b}

number of layer

#### `protected `[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` * `[`m_layers`](#classshogun_1_1CNeuralNetwork_1ad795d32139fa8c9d1462e9fdb3541302) {#classshogun_1_1CNeuralNetwork_1ad795d32139fa8c9d1462e9fdb3541302}

network's layers

#### `protected `[`SGMatrix`](#classshogun_1_1SGMatrix)`< bool > `[`m_adj_matrix`](#classshogun_1_1CNeuralNetwork_1a3a477cee6cf649042f3ed4e39c058038) {#classshogun_1_1CNeuralNetwork_1a3a477cee6cf649042f3ed4e39c058038}

Describes the connections in the network: if there's a connection from layer i to layer j then m_adj_matrix(i,j) = 1.

#### `protected int32_t `[`m_total_num_parameters`](#classshogun_1_1CNeuralNetwork_1ac3f14c5cd11deff0b82a086922988ed6) {#classshogun_1_1CNeuralNetwork_1ac3f14c5cd11deff0b82a086922988ed6}

total number of parameters in the network

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_params`](#classshogun_1_1CNeuralNetwork_1a95b3dfe8abbc77638c890fd7d90abb56) {#classshogun_1_1CNeuralNetwork_1a95b3dfe8abbc77638c890fd7d90abb56}

array where all the parameters of the network are stored

#### `protected `[`SGVector`](#classshogun_1_1SGVector)`< bool > `[`m_param_regularizable`](#classshogun_1_1CNeuralNetwork_1a707d5312683ba39938559c579eb1aedf) {#classshogun_1_1CNeuralNetwork_1a707d5312683ba39938559c579eb1aedf}

Array that specifies which parameters are to be regularized. This is used to turn off regularization for bias parameters

#### `protected `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`m_index_offsets`](#classshogun_1_1CNeuralNetwork_1a25cbed7bd471fac114418e0ba647f00f) {#classshogun_1_1CNeuralNetwork_1a25cbed7bd471fac114418e0ba647f00f}

offsets specifying where each layer's parameters and parameter gradients are stored, i.e layer i's parameters are stored at m_params + m_index_offsets[i]

#### `protected int32_t `[`m_batch_size`](#classshogun_1_1CNeuralNetwork_1acb2482e04fe13be6830ef0128acd4f68) {#classshogun_1_1CNeuralNetwork_1acb2482e04fe13be6830ef0128acd4f68}

number of train/test cases the network is expected to deal with. Default value is 1

#### `protected bool `[`m_is_training`](#classshogun_1_1CNeuralNetwork_1ab54ccba4ebf6200f64a12eb9c6f9992b) {#classshogun_1_1CNeuralNetwork_1ab54ccba4ebf6200f64a12eb9c6f9992b}

True if the network is currently being trained initial value is false

#### `protected bool `[`m_auto_quick_initialize`](#classshogun_1_1CNeuralNetwork_1a0d9982c5532a7edeb3d3e16e9333f591) {#classshogun_1_1CNeuralNetwork_1a0d9982c5532a7edeb3d3e16e9333f591}

True if the network layers are to be quick connected and initialized initial value is False

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_sigma`](#classshogun_1_1CNeuralNetwork_1a1cb9be87291a3d3f3ca4957a6a81d27c) {#classshogun_1_1CNeuralNetwork_1a1cb9be87291a3d3f3ca4957a6a81d27c}

Standard deviation of the gaussian used to randomly initialize the parameters

#### `protected `[`ENNOptimizationMethod`](#namespaceshogun_1afc5d4c2c14dc1ccf25e474b4f53c1cf5)` `[`m_optimization_method`](#classshogun_1_1CNeuralNetwork_1abfd89485d8df45b15ff45c6112e3bea5) {#classshogun_1_1CNeuralNetwork_1abfd89485d8df45b15ff45c6112e3bea5}

Optimization method, default is NNOM_LBFGS

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_l2_coefficient`](#classshogun_1_1CNeuralNetwork_1a18a5328b2456fe3280b47384c23e5129) {#classshogun_1_1CNeuralNetwork_1a18a5328b2456fe3280b47384c23e5129}

L2 Regularization coeff, default value is 0.0

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_l1_coefficient`](#classshogun_1_1CNeuralNetwork_1a324259098e079390a77e1d713baf7315) {#classshogun_1_1CNeuralNetwork_1a324259098e079390a77e1d713baf7315}

L1 Regularization coeff, default value is 0.0

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_dropout_hidden`](#classshogun_1_1CNeuralNetwork_1a3bc0c18dadbeeec2c3593781fdb3b3f7) {#classshogun_1_1CNeuralNetwork_1a3bc0c18dadbeeec2c3593781fdb3b3f7}

Probabilty that a hidden layer neuron will be dropped out When using this, the recommended value is 0.5

default value 0.0 (no dropout)

For more details on dropout, see [paper]([http://arxiv.org/abs/1207.0580](http://arxiv.org/abs/1207.0580)) [Hinton, 2012]

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_dropout_input`](#classshogun_1_1CNeuralNetwork_1a816344a964ad8d4327e8c9d6e441b3ab) {#classshogun_1_1CNeuralNetwork_1a816344a964ad8d4327e8c9d6e441b3ab}

Probabilty that a input layer neuron will be dropped out When using this, a good value might be 0.2

default value 0.0 (no dropout)

For more details on dropout, see this [paper]([http://arxiv.org/abs/1207.0580](http://arxiv.org/abs/1207.0580)) [Hinton, 2012]

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_max_norm`](#classshogun_1_1CNeuralNetwork_1a075bb8a0b9978c4308b2f2071ee709b9) {#classshogun_1_1CNeuralNetwork_1a075bb8a0b9978c4308b2f2071ee709b9}

Maximum allowable L2 norm for a neurons weights When using this, a good value might be 15

default value -1 (max-norm regularization disabled)

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_epsilon`](#classshogun_1_1CNeuralNetwork_1af4806209595723fa21dc4dab36541f45) {#classshogun_1_1CNeuralNetwork_1af4806209595723fa21dc4dab36541f45}

convergence criteria training stops when (E'- E)/E < epsilon where E is the error at the current iterations and E' is the error at the previous iteration default value is 1.0e-5

#### `protected int32_t `[`m_max_num_epochs`](#classshogun_1_1CNeuralNetwork_1acf6bc403f270179fd17a0eb0628d2b16) {#classshogun_1_1CNeuralNetwork_1acf6bc403f270179fd17a0eb0628d2b16}

maximum number of iterations over the training set. If 0, training will continue until convergence. defualt value is 0

#### `protected int32_t `[`m_gd_mini_batch_size`](#classshogun_1_1CNeuralNetwork_1abf5ba2ca10463fb6139e8094a5fe61be) {#classshogun_1_1CNeuralNetwork_1abf5ba2ca10463fb6139e8094a5fe61be}

size of the mini-batch used during gradient descent training, if 0 full-batch training is performed default value is 0

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_gd_learning_rate`](#classshogun_1_1CNeuralNetwork_1a8a7c892c0b394f20a87e7c217158408d) {#classshogun_1_1CNeuralNetwork_1a8a7c892c0b394f20a87e7c217158408d}

gradient descent learning rate, defualt value 0.1

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_gd_learning_rate_decay`](#classshogun_1_1CNeuralNetwork_1a16690277b66837f868eef7d92b71b572) {#classshogun_1_1CNeuralNetwork_1a16690277b66837f868eef7d92b71b572}

gradient descent learning rate decay learning rate is updated at each iteration i according to: alpha(i)=decay*alpha(i-1) default value is 1.0 (no decay)

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_gd_momentum`](#classshogun_1_1CNeuralNetwork_1a4a2d8cf6f933d2c8ee055d8c249ef693) {#classshogun_1_1CNeuralNetwork_1a4a2d8cf6f933d2c8ee055d8c249ef693}

gradient descent momentum multiplier

default value is 0.9

For more details on momentum, see this [paper]([http://jmlr.org/proceedings/papers/v28/sutskever13.html](http://jmlr.org/proceedings/papers/v28/sutskever13.html)) [Sutskever, 2013]

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_gd_error_damping_coeff`](#classshogun_1_1CNeuralNetwork_1a887b6161a7f0ff98ea8b9d21cd059ebb) {#classshogun_1_1CNeuralNetwork_1a887b6161a7f0ff98ea8b9d21cd059ebb}

Used to damp the error fluctuations when stochastic gradient descent is used. damping is done according to: error_damped(i) = c*error(i) + (1-c)*error_damped(i-1) where c is the damping coefficient

If -1, the damping coefficient is automatically computed according to: c = 0.99*gd_mini_batch_size/training_set_size + 1e-2;

default value is -1

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_max_train_time`](#classshogun_1_1CMachine_1a0d6a5a8aca2e1e91685c1ddf23442fd8) {#classshogun_1_1CMachine_1a0d6a5a8aca2e1e91685c1ddf23442fd8}

maximum training time

#### `protected `[`CLabels`](#classshogun_1_1CLabels)` * `[`m_labels`](#classshogun_1_1CMachine_1af3451cc972288f8c92ef7369952b805b) {#classshogun_1_1CMachine_1af3451cc972288f8c92ef7369952b805b}

labels

#### `protected `[`ESolverType`](#namespaceshogun_1af43428a9cb6c6de54cc7085c7c9b273e)` `[`m_solver_type`](#classshogun_1_1CMachine_1a4cc9c480f9e3535d05837670a124c080) {#classshogun_1_1CMachine_1a4cc9c480f9e3535d05837670a124c080}

solver type

#### `protected bool `[`m_store_model_features`](#classshogun_1_1CMachine_1ac359a14e48915341e9dd44c8fee21ac6) {#classshogun_1_1CMachine_1ac359a14e48915341e9dd44c8fee21ac6}

whether model features should be stored after training

#### `protected bool `[`m_data_locked`](#classshogun_1_1CMachine_1a93d71ccf0a5f7a1dad42f35dd7b932e2) {#classshogun_1_1CMachine_1a93d71ccf0a5f7a1dad42f35dd7b932e2}

whether data is locked

#### `protected std::atomic< bool > `[`m_cancel_computation`](#classshogun_1_1CStoppableSGObject_1a263b9ed7fb7b659634a6182daa5e4d33) {#classshogun_1_1CStoppableSGObject_1a263b9ed7fb7b659634a6182daa5e4d33}

Cancel computation

#### `protected std::atomic< bool > `[`m_pause_computation_flag`](#classshogun_1_1CStoppableSGObject_1a7054f653d8ec45c524c1137d24fd66df) {#classshogun_1_1CStoppableSGObject_1a7054f653d8ec45c524c1137d24fd66df}

Pause computation flag

#### `protected std::condition_variable `[`m_pause_computation`](#classshogun_1_1CStoppableSGObject_1af0e6de5887e6f425f0b62b34e62bcf5d) {#classshogun_1_1CStoppableSGObject_1af0e6de5887e6f425f0b62b34e62bcf5d}

Conditional variable to make threads wait

#### `protected std::mutex `[`m_mutex`](#classshogun_1_1CStoppableSGObject_1a5c751dae9068bdb864af14129bbe0fa1) {#classshogun_1_1CStoppableSGObject_1a5c751dae9068bdb864af14129bbe0fa1}

Mutex used to pause threads

#### `protected std::function< bool(void)> `[`m_callback`](#classshogun_1_1CStoppableSGObject_1ac68af0b9914ee5a4159295e140cb906c) {#classshogun_1_1CStoppableSGObject_1ac68af0b9914ee5a4159295e140cb906c}

#### `protected virtual bool `[`train_machine`](#classshogun_1_1CNeuralNetwork_1ac6ad4326a1641cb16d8d74d2ac00e9d3)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CNeuralNetwork_1ac6ad4326a1641cb16d8d74d2ac00e9d3}

trains the network

#### `protected virtual bool `[`train_gradient_descent`](#classshogun_1_1CNeuralNetwork_1ab5a71a0198cf40f7e1ccbb4f30a490a8)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > inputs,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > targets)` {#classshogun_1_1CNeuralNetwork_1ab5a71a0198cf40f7e1ccbb4f30a490a8}

trains the network using gradient descent

#### `protected virtual bool `[`train_lbfgs`](#classshogun_1_1CNeuralNetwork_1a0ae46f9e8ae7c5151685b25664542a22)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > inputs,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > targets)` {#classshogun_1_1CNeuralNetwork_1a0ae46f9e8ae7c5151685b25664542a22}

trains the network using L-BFGS

#### `protected virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`forward_propagate`](#classshogun_1_1CNeuralNetwork_1a3501eb1009bfa0ad1b2620ea63eb9c0c)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data,int32_t j)` {#classshogun_1_1CNeuralNetwork_1a3501eb1009bfa0ad1b2620ea63eb9c0c}

Applies forward propagation, computes the activations of each layer up to layer j

#### Parameters
* `data` input features 

* `j` layer index at which the propagation should stop. If -1, the propagation continues up to the last layer

#### Returns
activations of the last layer

#### `protected virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`forward_propagate`](#classshogun_1_1CNeuralNetwork_1a8637dcdff043906fa36b86d1948091d1)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > inputs,int32_t j)` {#classshogun_1_1CNeuralNetwork_1a8637dcdff043906fa36b86d1948091d1}

Applies forward propagation, computes the activations of each layer up to layer j

#### Parameters
* `inputs` inputs to the network, a matrix of size m_num_inputs*m_batch_size 

* `j` layer index at which the propagation should stop. If -1, the propagation continues up to the last layer

#### Returns
activations of the last layer

#### `protected virtual void `[`set_batch_size`](#classshogun_1_1CNeuralNetwork_1a2fb212dd86732ebf70f0a692257422d5)`(int32_t batch_size)` {#classshogun_1_1CNeuralNetwork_1a2fb212dd86732ebf70f0a692257422d5}

Sets the batch size (the number of train/test cases) the network is expected to deal with. Allocates memory for the activations, local gradients, input gradients if necessary (if the batch size is different from it's previous value)

#### Parameters
* `batch_size` number of train/test cases the network is expected to deal with.

#### `protected virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_gradients`](#classshogun_1_1CNeuralNetwork_1a6ba743f03a2c0ccd09eff57b8a0f7cd2)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > inputs,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > targets,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > gradients)` {#classshogun_1_1CNeuralNetwork_1a6ba743f03a2c0ccd09eff57b8a0f7cd2}

Applies backpropagation to compute the gradients of the error with repsect to every parameter in the network.

#### Parameters
* `inputs` inputs to the network, a matrix of size m_num_inputs*m_batch_size

* `targets` desired values for the output layer's activations. matrix of size m_layers[m_num_layers-1].get_num_neurons()*m_batch_size

* `gradients` array to be filled with gradient values.

#### Returns
error between the targets and the activations of the last layer

#### `protected virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_error`](#classshogun_1_1CNeuralNetwork_1aa2b92865fc0e056843a501301209eebf)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > inputs,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > targets)` {#classshogun_1_1CNeuralNetwork_1aa2b92865fc0e056843a501301209eebf}

Forward propagates the inputs and computes the error between the output layer's activations and the given target activations.

#### Parameters
* `inputs` inputs to the network, a matrix of size m_num_inputs*m_batch_size

* `targets` desired values for the network's output, matrix of size num_neurons_output_layer*batch_size

#### `protected virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_error`](#classshogun_1_1CNeuralNetwork_1a0cb7071826ea91246031bc9ace734cc3)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > targets)` {#classshogun_1_1CNeuralNetwork_1a0cb7071826ea91246031bc9ace734cc3}

Computes the error between the output layer's activations and the given target activations.

#### Parameters
* `targets` desired values for the network's output, matrix of size num_neurons_output_layer*batch_size

#### `protected virtual bool `[`is_label_valid`](#classshogun_1_1CNeuralNetwork_1abc2e336339ace0a7656f4822a98fad0a)`(`[`CLabels`](#classshogun_1_1CLabels)` * lab) const` {#classshogun_1_1CNeuralNetwork_1abc2e336339ace0a7656f4822a98fad0a}

check whether the labels is valid.

Subclasses can override this to implement their check of label types.

#### Parameters
* `lab` the labels being checked, guaranteed to be non-NULL

#### `protected `[`CNeuralLayer`](#classshogun_1_1CNeuralLayer)` * `[`get_layer`](#classshogun_1_1CNeuralNetwork_1af03c8141230ae1ccd4a43a81babe193c)`(int32_t i)` {#classshogun_1_1CNeuralNetwork_1af03c8141230ae1ccd4a43a81babe193c}

returns a pointer to layer i in the network

#### `protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`features_to_matrix`](#classshogun_1_1CNeuralNetwork_1a222f7b1543b027e556d35e65dd66e864)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * features)` {#classshogun_1_1CNeuralNetwork_1a222f7b1543b027e556d35e65dd66e864}

Ensures the given features are suitable for use with the network and returns their feature matrix

#### `protected `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`labels_to_matrix`](#classshogun_1_1CNeuralNetwork_1a24a7aa21cfa7aebcf3debaa523405fb1)`(`[`CLabels`](#classshogun_1_1CLabels)` * labs)` {#classshogun_1_1CNeuralNetwork_1a24a7aa21cfa7aebcf3debaa523405fb1}

converts the given labels into a matrix suitable for use with network

#### Returns
matrix of size [get_num_outputs()](#classshogun_1_1CNeuralNetwork_1a6d88ac18968e25f18aee7f3241234db2)*num_labels

#### `protected inline virtual bool `[`train_dense`](#classshogun_1_1CMachine_1a2f4984079885c8a49f40fc6bc8366d67)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMachine_1a2f4984079885c8a49f40fc6bc8366d67}

#### `protected inline virtual bool `[`train_string`](#classshogun_1_1CMachine_1aa7f306efec16f95e741472046dee440d)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMachine_1aa7f306efec16f95e741472046dee440d}

#### `protected inline virtual bool `[`support_feature_dispatching`](#classshogun_1_1CMachine_1a6d0cdca08d31651c73d028199634bb6e)`()` {#classshogun_1_1CMachine_1a6d0cdca08d31651c73d028199634bb6e}

#### `protected inline virtual bool `[`support_dense_dispatching`](#classshogun_1_1CMachine_1a44486c95636e8e11e3fd83fc8073a860)`()` {#classshogun_1_1CMachine_1a44486c95636e8e11e3fd83fc8073a860}

#### `protected inline virtual bool `[`support_string_dispatching`](#classshogun_1_1CMachine_1a3f800163b86742f0edfdabf452a627f8)`()` {#classshogun_1_1CMachine_1a3f800163b86742f0edfdabf452a627f8}

#### `protected inline virtual bool `[`continue_train`](#classshogun_1_1CMachine_1a0d918d8b628c91f0c22f2a623b495812)`()` {#classshogun_1_1CMachine_1a0d918d8b628c91f0c22f2a623b495812}

Continue Training

This method can be used to continue a prematurely stopped call to [CMachine::train](#classshogun_1_1CMachine_1aa0ece9fd14892c6dfed1bb8c78f3b3ed). This is available for Iterative models and throws an error if the feature is not supported.

#### Returns
whether training was successful

#### `protected inline virtual void `[`store_model_features`](#classshogun_1_1CMachine_1ae0a84ada96561ce09c35e2839f8ca512)`()` {#classshogun_1_1CMachine_1ae0a84ada96561ce09c35e2839f8ca512}

Stores feature data of underlying model. After this method has been called, it is possible to change the machine's feature data and call [apply()](#classshogun_1_1CMachine_1afd5d402257972c78456594234d13eb4c), which is then performed on the training feature data that is part of the machine's model.

Base method, has to be implemented in order to allow cross-validation and model selection.

NOT IMPLEMENTED! Has to be done in subclasses

#### `protected rxcpp::subscription `[`connect_to_signal_handler`](#classshogun_1_1CStoppableSGObject_1a4e732c6748fe2895f401c66647863e39)`()` {#classshogun_1_1CStoppableSGObject_1a4e732c6748fe2895f401c66647863e39}

connect the machine instance to the signal handler

#### `protected void `[`reset_computation_variables`](#classshogun_1_1CStoppableSGObject_1ae1ce696f8c07b4884cbc1311fd9f5a37)`()` {#classshogun_1_1CStoppableSGObject_1ae1ce696f8c07b4884cbc1311fd9f5a37}

reset the computation variables

#### `protected void `[`on_next`](#classshogun_1_1CStoppableSGObject_1a4362088c65601a14e98c19c9f0b48034)`()` {#classshogun_1_1CStoppableSGObject_1a4362088c65601a14e98c19c9f0b48034}

sets cancel computation flag

#### `protected virtual void `[`on_next_impl`](#classshogun_1_1CStoppableSGObject_1aecd947301711b0871ecc7e4608e2e794)`()` {#classshogun_1_1CStoppableSGObject_1aecd947301711b0871ecc7e4608e2e794}

The action which will be done when the user decides to premature stop the [CMachine](#classshogun_1_1CMachine) execution

#### `protected void `[`on_pause`](#classshogun_1_1CStoppableSGObject_1aae61636109c2e67b8313c19b639c8dcd)`()` {#classshogun_1_1CStoppableSGObject_1aae61636109c2e67b8313c19b639c8dcd}

sets pause computation flag and resumes after action is complete

#### `protected virtual void `[`on_pause_impl`](#classshogun_1_1CStoppableSGObject_1a2fa805bcc33be124bea5b51cd9353524)`()` {#classshogun_1_1CStoppableSGObject_1a2fa805bcc33be124bea5b51cd9353524}

The action which will be done when the user decides to pause the [CMachine](#classshogun_1_1CMachine) execution

#### `protected void `[`on_complete`](#classshogun_1_1CStoppableSGObject_1a4f7551e636a9ecc3826dd729b219e532)`()` {#classshogun_1_1CStoppableSGObject_1a4f7551e636a9ecc3826dd729b219e532}

These actions which will be done when the user decides to return to prompt and terminate the program execution

#### `protected virtual void `[`on_complete_impl`](#classshogun_1_1CStoppableSGObject_1a0aac1762c8df8870a5242a710457c6a3)`()` {#classshogun_1_1CStoppableSGObject_1a0aac1762c8df8870a5242a710457c6a3}

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

