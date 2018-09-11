---
classname: "shogun::CDomainAdaptationMulticlassLibLinear"
type: "class"
parents:
   - CMulticlassLibLinear
---

# class `shogun::CDomainAdaptationMulticlassLibLinear` {#classshogun_1_1CDomainAdaptationMulticlassLibLinear}

```
class shogun::CDomainAdaptationMulticlassLibLinear
  : public CMulticlassLibLinear
```

domain adaptation multiclass LibLinear wrapper Source domain is assumed to b

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
`public  `[`CDomainAdaptationMulticlassLibLinear`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a0dd38e875b181a9fa17d2e89d9342904)`()` | default constructor
`public  `[`CDomainAdaptationMulticlassLibLinear`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a8d98e810d9f08d34afb4ee35d79c256e)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` target_C,`[`CDotFeatures`](#classshogun_1_1CDotFeatures)` * target_features,`[`CLabels`](#classshogun_1_1CLabels)` * target_labels,`[`CLinearMulticlassMachine`](#classshogun_1_1CLinearMulticlassMachine)` * source_machine)` | standard constructor 
`public virtual  `[`~CDomainAdaptationMulticlassLibLinear`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a7d5f1665d24bcdef241ccd8852d5b676)`()` | destructor
`public virtual `[`CBinaryLabels`](#classshogun_1_1CBinaryLabels)` * `[`get_submachine_outputs`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1ad1c98a924da31c1108e007d24e131649)`(int32_t)` | get submachine outputs
`public inline virtual const char * `[`get_name`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` | get name
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_source_bias`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a453002c2173b86c5b2577591db8ebf71)`() const` | getter for source bias 
`public void `[`set_source_bias`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a9db842b8be1d5f18268c8a913192b833)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` source_bias)` | setter for source bias 
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_train_factor`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a087b7100c080f3c30acef833318e31e4)`() const` | getter for train factor 
`public void `[`set_train_factor`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a3a9c0210fbc4dc1b1c5c66f75e4b9f50)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` train_factor)` | setter for train factor 
`public `[`CLinearMulticlassMachine`](#classshogun_1_1CLinearMulticlassMachine)` * `[`get_source_machine`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1afb8dbbc0fafd03e350e9236626465bfe)`() const` | getter for source machine 
`public void `[`set_source_machine`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a8b2f6dcf98c83fa50ed31b38771b7145)`(`[`CLinearMulticlassMachine`](#classshogun_1_1CLinearMulticlassMachine)` * source_machine)` | setter for source machine 
`public inline void `[`set_C`](#classshogun_1_1CMulticlassLibLinear_1ac9fe07daf542e2ed0a1e4767060825ef)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` C)` | set C 
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_C`](#classshogun_1_1CMulticlassLibLinear_1ad3cfa73b8c673ea486f9b4446ca43b14)`() const` | get C 
`public inline void `[`set_epsilon`](#classshogun_1_1CMulticlassLibLinear_1a3b8392d8584df5bdba1d4af92346db31)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` epsilon)` | set epsilon 
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_epsilon`](#classshogun_1_1CMulticlassLibLinear_1a0813512911649cc6fa462bad06b877ee)`() const` | get epsilon 
`public inline void `[`set_use_bias`](#classshogun_1_1CMulticlassLibLinear_1a07586b1e614c4cd560c2210c4fac06eb)`(bool use_bias)` | set use bias 
`public inline bool `[`get_use_bias`](#classshogun_1_1CMulticlassLibLinear_1a162ef637cf4e1083cca513707cec0431)`() const` | get use bias 
`public inline void `[`set_save_train_state`](#classshogun_1_1CMulticlassLibLinear_1a3e7b00200f3bcf1b9f09de83ab81609d)`(bool save_train_state)` | set save train state 
`public inline bool `[`get_save_train_state`](#classshogun_1_1CMulticlassLibLinear_1a9f1969e13a58835758beec1901244a08)`() const` | get save train state 
`public inline void `[`set_max_iter`](#classshogun_1_1CMulticlassLibLinear_1a52c7c34361fd2d0320a3cb8b48fcfd42)`(int32_t max_iter)` | set max iter 
`public inline int32_t `[`get_max_iter`](#classshogun_1_1CMulticlassLibLinear_1a9246ba8e23c5f0ea11a07fc73a993573)`() const` | get max iter 
`public inline void `[`reset_train_state`](#classshogun_1_1CMulticlassLibLinear_1a8ab367535a10d1cee6c97b15be00fc15)`()` | reset train state
`public `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`get_support_vectors`](#classshogun_1_1CMulticlassLibLinear_1a0b6fc6248b5951a4672f43a8c80d2cec)`() const` | get support vector indices 
`public inline void `[`set_features`](#classshogun_1_1CLinearMulticlassMachine_1ae19c50b43fab4a7c68bf425bea93c98f)`(`[`CDotFeatures`](#classshogun_1_1CDotFeatures)` * f)` | set features
`public inline `[`CDotFeatures`](#classshogun_1_1CDotFeatures)` * `[`get_features`](#classshogun_1_1CLinearMulticlassMachine_1af6ee2fc558f82576b4458771a65f5f4d)`() const` | get features
`public virtual void `[`set_labels`](#classshogun_1_1CMulticlassMachine_1a5f0cfd09e37bd5e793cacecb8d3c818b)`(`[`CLabels`](#classshogun_1_1CLabels)` * lab)` | set labels
`public inline bool `[`set_machine`](#classshogun_1_1CMulticlassMachine_1ac10c2065b2f88cd96702bf62142735e1)`(int32_t num,`[`CMachine`](#classshogun_1_1CMachine)` * machine)` | set machine
`public inline `[`CMachine`](#classshogun_1_1CMachine)` * `[`get_machine`](#classshogun_1_1CMulticlassMachine_1a92cbc044179e524bce3000e9884e0368)`(int32_t num) const` | get machine
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_submachine_output`](#classshogun_1_1CMulticlassMachine_1ab88dc1b9614d23db76dc2b7e2ee683a2)`(int32_t i,int32_t num)` | get output of i-th submachine for num-th vector 
`public virtual `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * `[`apply_multiclass`](#classshogun_1_1CMulticlassMachine_1a250aa566fff0edb31433db98f70a7f15)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | classify all examples
`public virtual `[`CMultilabelLabels`](#classshogun_1_1CMultilabelLabels)` * `[`apply_multilabel_output`](#classshogun_1_1CMulticlassMachine_1a6f2a839aa4ebc25cb9f37edc1739f328)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data,int32_t n_outputs)` | classify all examples with multiple output
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`apply_one`](#classshogun_1_1CMulticlassMachine_1aa3e372f16ab13497b59cc12b2118ffdb)`(int32_t vec_idx)` | classify one example 
`public inline `[`CMulticlassStrategy`](#classshogun_1_1CMulticlassStrategy)` * `[`get_multiclass_strategy`](#classshogun_1_1CMulticlassMachine_1a0d8d56d6a79db5c58daa9c250ce31684)`() const` | get the type of multiclass'ness
`public inline `[`CRejectionStrategy`](#classshogun_1_1CRejectionStrategy)` * `[`get_rejection_strategy`](#classshogun_1_1CMulticlassMachine_1a9d9957c5a644d992be728dbd3946146a)`() const` | returns rejection strategy
`public inline void `[`set_rejection_strategy`](#classshogun_1_1CMulticlassMachine_1aa301bb9b887b69737640870f56e7f2b0)`(`[`CRejectionStrategy`](#classshogun_1_1CRejectionStrategy)` * rejection_strategy)` | sets rejection strategy
`public inline `[`EProbHeuristicType`](#namespaceshogun_1ad7ce6e7dfc495887fab183cd2f3a3351)` `[`get_prob_heuris`](#classshogun_1_1CMulticlassMachine_1ad1e8ccf13b994458c29d76421dbbed63)`()` | get prob output heuristic of multiclass strategy
`public inline void `[`set_prob_heuris`](#classshogun_1_1CMulticlassMachine_1a5ee2f2f764552ffb587128071af91cd6)`(`[`EProbHeuristicType`](#namespaceshogun_1ad7ce6e7dfc495887fab183cd2f3a3351)` prob_heuris)` | set prob output heuristic of multiclass strategy 
`public int32_t `[`get_num_machines`](#classshogun_1_1CBaseMulticlassMachine_1a61596dedd23969cf46312187ee17afe5)`() const` | get number of machines
`public virtual `[`EProblemType`](#namespaceshogun_1a0aa89aa872f89f6a174de2f45b7596d4)` `[`get_machine_problem_type`](#classshogun_1_1CBaseMulticlassMachine_1a135f8d82da3fc55807d1640080358500)`() const` | get problem type
`public virtual bool `[`is_label_valid`](#classshogun_1_1CBaseMulticlassMachine_1abc2e336339ace0a7656f4822a98fad0a)`(`[`CLabels`](#classshogun_1_1CLabels)` * lab) const` | check whether the labels is valid.
`public virtual bool `[`train`](#classshogun_1_1CMachine_1aa0ece9fd14892c6dfed1bb8c78f3b3ed)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | train machine
`public virtual bool `[`train_locked`](#classshogun_1_1CMachine_1aab4927bdae8da7f0c85efdfce22c86c2)`()` | Trains a locked machine on a set of indices. Error if machine is not locked 
`public inline virtual bool `[`train_locked`](#classshogun_1_1CMachine_1a6211015eaf19161e4c469c8ff38bfeba)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | Trains a locked machine on a set of indices. Error if machine is not locked
`public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`apply`](#classshogun_1_1CMachine_1afd5d402257972c78456594234d13eb4c)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data if data is not specified apply to the current features
`public virtual `[`CBinaryLabels`](#classshogun_1_1CBinaryLabels)` * `[`apply_binary`](#classshogun_1_1CMachine_1a16a7dee83bb61aedc93792df578d4a77)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data in means of binary classification problem
`public virtual `[`CRegressionLabels`](#classshogun_1_1CRegressionLabels)` * `[`apply_regression`](#classshogun_1_1CMachine_1aaeea92e0e4795e7f63f067c16f162302)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data in means of regression problem
`public virtual `[`CStructuredLabels`](#classshogun_1_1CStructuredLabels)` * `[`apply_structured`](#classshogun_1_1CMachine_1a588efa92a0696e1d2a61a8cd21d8ebee)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data in means of SO classification problem
`public virtual `[`CLatentLabels`](#classshogun_1_1CLatentLabels)` * `[`apply_latent`](#classshogun_1_1CMachine_1a276d23b37202ecb31367df26a5600cf7)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data in means of latent problem
`public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`get_labels`](#classshogun_1_1CMachine_1a065f0797777044cb0dbf786781982e3d)`()` | get labels
`public void `[`set_max_train_time`](#classshogun_1_1CMachine_1af660b1b03c475c3c638d2c995ea4b54a)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` t)` | set maximum training time
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_max_train_time`](#classshogun_1_1CMachine_1a7c75c86ff1cfd61d8275e62f0477d797)`()` | get maximum training time
`public virtual `[`EMachineType`](#namespaceshogun_1af181c832c12de7a0c3b02425986106cc)` `[`get_classifier_type`](#classshogun_1_1CMachine_1a177dc18a9a5639da395099947cb44501)`()` | get classifier type
`public void `[`set_solver_type`](#classshogun_1_1CMachine_1af8876022111114d5d3b0579ee161a8ff)`(`[`ESolverType`](#namespaceshogun_1af43428a9cb6c6de54cc7085c7c9b273e)` st)` | set solver type
`public `[`ESolverType`](#namespaceshogun_1af43428a9cb6c6de54cc7085c7c9b273e)` `[`get_solver_type`](#classshogun_1_1CMachine_1a97ee8b11465427d28498437279229ebe)`()` | get solver type
`public virtual void `[`set_store_model_features`](#classshogun_1_1CMachine_1a872d1cc0904edaa3c5701b049ee2993d)`(bool store_model)` | Setter for store-model-features-after-training flag
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
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_train_factor`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1abe6bf179fab6adbea480bc324223a8cf) | train factor
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_source_bias`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a633511a34e9ae2637d00f6a7ea443056) | source bias
`protected `[`CLinearMulticlassMachine`](#classshogun_1_1CLinearMulticlassMachine)` * `[`m_source_machine`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a9d63efb4180842da42905363f1768906) | source domain machine
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_C`](#classshogun_1_1CMulticlassLibLinear_1a5c2dd8f13b5a4936ebadc023c854e9d1) | regularization constant for each machine
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_epsilon`](#classshogun_1_1CMulticlassLibLinear_1af4806209595723fa21dc4dab36541f45) | tolerance
`protected int32_t `[`m_max_iter`](#classshogun_1_1CMulticlassLibLinear_1aff3aa88417a9ec8ed59a3c8fec0d093d) | max number of iterations
`protected bool `[`m_use_bias`](#classshogun_1_1CMulticlassLibLinear_1acef1b85919183268aad9933f8b60b01c) | use bias
`protected bool `[`m_save_train_state`](#classshogun_1_1CMulticlassLibLinear_1af2a60bc94f8bd9a75b6704657581d124) | save train state
`protected mcsvm_state * `[`m_train_state`](#classshogun_1_1CMulticlassLibLinear_1aee9ba6cd266c2322c2098a04d923822a) | solver state
`protected `[`CDotFeatures`](#classshogun_1_1CDotFeatures)` * `[`m_features`](#classshogun_1_1CLinearMulticlassMachine_1a69c7ea341f231739924f54ee0fe48521) | features
`protected `[`CMulticlassStrategy`](#classshogun_1_1CMulticlassStrategy)` * `[`m_multiclass_strategy`](#classshogun_1_1CMulticlassMachine_1ad6eb1bc28c3ab3d390a88968040dcabe) | type of multiclass strategy
`protected `[`CMachine`](#classshogun_1_1CMachine)` * `[`m_machine`](#classshogun_1_1CMulticlassMachine_1acd634baf350a2c33a0701b3ca935d677) | machine
`protected `[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` * `[`m_machines`](#classshogun_1_1CBaseMulticlassMachine_1acd59fab07dd68c8bd831e76bd870fbbb) | machines
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
`protected virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`obtain_regularizer_matrix`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a6873aff648f0d0a5bbe4d6816ce46689)`() const` | obtain regularizer (w0) matrix
`protected virtual bool `[`train_machine`](#classshogun_1_1CMulticlassLibLinear_1ac6ad4326a1641cb16d8d74d2ac00e9d3)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | train machine
`protected inline virtual bool `[`init_machine_for_train`](#classshogun_1_1CLinearMulticlassMachine_1a18b2a5959cd2156ea0315c19be8ddd90)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | init machine for train with setting features
`protected inline virtual bool `[`init_machines_for_apply`](#classshogun_1_1CLinearMulticlassMachine_1a1fdce1052c1cc6ce067bfe6b678f8b2c)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | init machines for applying with setting features
`protected inline virtual bool `[`is_ready`](#classshogun_1_1CLinearMulticlassMachine_1ab9f470c03cafceb7df880bc25ca7a713)`()` | check features availability
`protected inline virtual `[`CMachine`](#classshogun_1_1CMachine)` * `[`get_machine_from_trained`](#classshogun_1_1CLinearMulticlassMachine_1a746274f0ba4151b38527852bbd0360e4)`(`[`CMachine`](#classshogun_1_1CMachine)` * machine)` | construct linear machine from given linear machine
`protected inline virtual int32_t `[`get_num_rhs_vectors`](#classshogun_1_1CLinearMulticlassMachine_1aa9b066abb858b4dc0684bac22d004e4f)`()` | get number of rhs feature vectors
`protected inline virtual void `[`add_machine_subset`](#classshogun_1_1CLinearMulticlassMachine_1a3573ec176ce08901d5329d1d39047a90)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > subset)` | set subset to the features of the machine, deletes old one
`protected inline virtual void `[`remove_machine_subset`](#classshogun_1_1CLinearMulticlassMachine_1a00b440d35fa9b4a7727a85daebe6d848)`()` | deletes any subset set to the features of the machine
`protected inline virtual void `[`store_model_features`](#classshogun_1_1CLinearMulticlassMachine_1ae0a84ada96561ce09c35e2839f8ca512)`()` | Stores feature data of underlying model. Does nothing because Linear machines store the normal vector of the separating hyperplane and therefore the model anyway
`protected void `[`init_strategy`](#classshogun_1_1CMulticlassMachine_1aee05c0d5e1aa151f0e55b27b906611ea)`()` | init strategy
`protected void `[`clear_machines`](#classshogun_1_1CMulticlassMachine_1a7e5d0a721abdf9fc144ce8560e3d77ea)`()` | clear machines
`protected inline virtual bool `[`is_acceptable_machine`](#classshogun_1_1CMulticlassMachine_1ae4b20841b2638e5ca452e6a1cd7c2021)`(`[`CMachine`](#classshogun_1_1CMachine)` * machine)` | whether the machine is acceptable in set_machine
`protected inline virtual bool `[`train_dense`](#classshogun_1_1CMachine_1a2f4984079885c8a49f40fc6bc8366d67)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | 
`protected inline virtual bool `[`train_string`](#classshogun_1_1CMachine_1aa7f306efec16f95e741472046dee440d)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | 
`protected inline virtual bool `[`support_feature_dispatching`](#classshogun_1_1CMachine_1a6d0cdca08d31651c73d028199634bb6e)`()` | 
`protected inline virtual bool `[`support_dense_dispatching`](#classshogun_1_1CMachine_1a44486c95636e8e11e3fd83fc8073a860)`()` | 
`protected inline virtual bool `[`support_string_dispatching`](#classshogun_1_1CMachine_1a3f800163b86742f0edfdabf452a627f8)`()` | 
`protected inline virtual bool `[`continue_train`](#classshogun_1_1CMachine_1a0d918d8b628c91f0c22f2a623b495812)`()` | Continue Training
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

#### `public  `[`CDomainAdaptationMulticlassLibLinear`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a0dd38e875b181a9fa17d2e89d9342904)`()` {#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a0dd38e875b181a9fa17d2e89d9342904}

default constructor

#### `public  `[`CDomainAdaptationMulticlassLibLinear`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a8d98e810d9f08d34afb4ee35d79c256e)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` target_C,`[`CDotFeatures`](#classshogun_1_1CDotFeatures)` * target_features,`[`CLabels`](#classshogun_1_1CLabels)` * target_labels,`[`CLinearMulticlassMachine`](#classshogun_1_1CLinearMulticlassMachine)` * source_machine)` {#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a8d98e810d9f08d34afb4ee35d79c256e}

standard constructor 
#### Parameters
* `target_C` C regularization constant value for target domain 

* `target_features` target domain features 

* `target_labels` target domain labels 

* `source_machine` source domain machine to regularize against

#### `public virtual  `[`~CDomainAdaptationMulticlassLibLinear`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a7d5f1665d24bcdef241ccd8852d5b676)`()` {#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a7d5f1665d24bcdef241ccd8852d5b676}

destructor

#### `public virtual `[`CBinaryLabels`](#classshogun_1_1CBinaryLabels)` * `[`get_submachine_outputs`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1ad1c98a924da31c1108e007d24e131649)`(int32_t)` {#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1ad1c98a924da31c1108e007d24e131649}

get submachine outputs

#### `public inline virtual const char * `[`get_name`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` {#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a9cb485686dd7a1e6f7103cf42e87717e}

get name

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_source_bias`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a453002c2173b86c5b2577591db8ebf71)`() const` {#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a453002c2173b86c5b2577591db8ebf71}

getter for source bias 
#### Returns
source bias

#### `public void `[`set_source_bias`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a9db842b8be1d5f18268c8a913192b833)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` source_bias)` {#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a9db842b8be1d5f18268c8a913192b833}

setter for source bias 
#### Parameters
* `source_bias` source bias

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_train_factor`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a087b7100c080f3c30acef833318e31e4)`() const` {#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a087b7100c080f3c30acef833318e31e4}

getter for train factor 
#### Returns
train factor

#### `public void `[`set_train_factor`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a3a9c0210fbc4dc1b1c5c66f75e4b9f50)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` train_factor)` {#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a3a9c0210fbc4dc1b1c5c66f75e4b9f50}

setter for train factor 
#### Parameters
* `train_factor` train factor

#### `public `[`CLinearMulticlassMachine`](#classshogun_1_1CLinearMulticlassMachine)` * `[`get_source_machine`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1afb8dbbc0fafd03e350e9236626465bfe)`() const` {#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1afb8dbbc0fafd03e350e9236626465bfe}

getter for source machine 
#### Returns
source machine

#### `public void `[`set_source_machine`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a8b2f6dcf98c83fa50ed31b38771b7145)`(`[`CLinearMulticlassMachine`](#classshogun_1_1CLinearMulticlassMachine)` * source_machine)` {#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a8b2f6dcf98c83fa50ed31b38771b7145}

setter for source machine 
#### Parameters
* `source_machine` source machine

#### `public inline void `[`set_C`](#classshogun_1_1CMulticlassLibLinear_1ac9fe07daf542e2ed0a1e4767060825ef)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` C)` {#classshogun_1_1CMulticlassLibLinear_1ac9fe07daf542e2ed0a1e4767060825ef}

set C 
#### Parameters
* `C` C value

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_C`](#classshogun_1_1CMulticlassLibLinear_1ad3cfa73b8c673ea486f9b4446ca43b14)`() const` {#classshogun_1_1CMulticlassLibLinear_1ad3cfa73b8c673ea486f9b4446ca43b14}

get C 
#### Returns
C value

#### `public inline void `[`set_epsilon`](#classshogun_1_1CMulticlassLibLinear_1a3b8392d8584df5bdba1d4af92346db31)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` epsilon)` {#classshogun_1_1CMulticlassLibLinear_1a3b8392d8584df5bdba1d4af92346db31}

set epsilon 
#### Parameters
* `epsilon` epsilon value

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_epsilon`](#classshogun_1_1CMulticlassLibLinear_1a0813512911649cc6fa462bad06b877ee)`() const` {#classshogun_1_1CMulticlassLibLinear_1a0813512911649cc6fa462bad06b877ee}

get epsilon 
#### Returns
epsilon value

#### `public inline void `[`set_use_bias`](#classshogun_1_1CMulticlassLibLinear_1a07586b1e614c4cd560c2210c4fac06eb)`(bool use_bias)` {#classshogun_1_1CMulticlassLibLinear_1a07586b1e614c4cd560c2210c4fac06eb}

set use bias 
#### Parameters
* `use_bias` use_bias value

#### `public inline bool `[`get_use_bias`](#classshogun_1_1CMulticlassLibLinear_1a162ef637cf4e1083cca513707cec0431)`() const` {#classshogun_1_1CMulticlassLibLinear_1a162ef637cf4e1083cca513707cec0431}

get use bias 
#### Returns
use_bias value

#### `public inline void `[`set_save_train_state`](#classshogun_1_1CMulticlassLibLinear_1a3e7b00200f3bcf1b9f09de83ab81609d)`(bool save_train_state)` {#classshogun_1_1CMulticlassLibLinear_1a3e7b00200f3bcf1b9f09de83ab81609d}

set save train state 
#### Parameters
* `save_train_state` save train state value

#### `public inline bool `[`get_save_train_state`](#classshogun_1_1CMulticlassLibLinear_1a9f1969e13a58835758beec1901244a08)`() const` {#classshogun_1_1CMulticlassLibLinear_1a9f1969e13a58835758beec1901244a08}

get save train state 
#### Returns
save_train_state value

#### `public inline void `[`set_max_iter`](#classshogun_1_1CMulticlassLibLinear_1a52c7c34361fd2d0320a3cb8b48fcfd42)`(int32_t max_iter)` {#classshogun_1_1CMulticlassLibLinear_1a52c7c34361fd2d0320a3cb8b48fcfd42}

set max iter 
#### Parameters
* `max_iter` max iter value

#### `public inline int32_t `[`get_max_iter`](#classshogun_1_1CMulticlassLibLinear_1a9246ba8e23c5f0ea11a07fc73a993573)`() const` {#classshogun_1_1CMulticlassLibLinear_1a9246ba8e23c5f0ea11a07fc73a993573}

get max iter 
#### Returns
max iter value

#### `public inline void `[`reset_train_state`](#classshogun_1_1CMulticlassLibLinear_1a8ab367535a10d1cee6c97b15be00fc15)`()` {#classshogun_1_1CMulticlassLibLinear_1a8ab367535a10d1cee6c97b15be00fc15}

reset train state

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`get_support_vectors`](#classshogun_1_1CMulticlassLibLinear_1a0b6fc6248b5951a4672f43a8c80d2cec)`() const` {#classshogun_1_1CMulticlassLibLinear_1a0b6fc6248b5951a4672f43a8c80d2cec}

get support vector indices 
#### Returns
support vector indices

#### `public inline void `[`set_features`](#classshogun_1_1CLinearMulticlassMachine_1ae19c50b43fab4a7c68bf425bea93c98f)`(`[`CDotFeatures`](#classshogun_1_1CDotFeatures)` * f)` {#classshogun_1_1CLinearMulticlassMachine_1ae19c50b43fab4a7c68bf425bea93c98f}

set features

#### Parameters
* `f` features

#### `public inline `[`CDotFeatures`](#classshogun_1_1CDotFeatures)` * `[`get_features`](#classshogun_1_1CLinearMulticlassMachine_1af6ee2fc558f82576b4458771a65f5f4d)`() const` {#classshogun_1_1CLinearMulticlassMachine_1af6ee2fc558f82576b4458771a65f5f4d}

get features

#### Returns
features

#### `public virtual void `[`set_labels`](#classshogun_1_1CMulticlassMachine_1a5f0cfd09e37bd5e793cacecb8d3c818b)`(`[`CLabels`](#classshogun_1_1CLabels)` * lab)` {#classshogun_1_1CMulticlassMachine_1a5f0cfd09e37bd5e793cacecb8d3c818b}

set labels

#### Parameters
* `lab` labels

#### `public inline bool `[`set_machine`](#classshogun_1_1CMulticlassMachine_1ac10c2065b2f88cd96702bf62142735e1)`(int32_t num,`[`CMachine`](#classshogun_1_1CMachine)` * machine)` {#classshogun_1_1CMulticlassMachine_1ac10c2065b2f88cd96702bf62142735e1}

set machine

#### Parameters
* `num` index of machine 

* `machine` machine to set 

#### Returns
if setting was successful

#### `public inline `[`CMachine`](#classshogun_1_1CMachine)` * `[`get_machine`](#classshogun_1_1CMulticlassMachine_1a92cbc044179e524bce3000e9884e0368)`(int32_t num) const` {#classshogun_1_1CMulticlassMachine_1a92cbc044179e524bce3000e9884e0368}

get machine

#### Parameters
* `num` index of machine to get 

#### Returns
SVM at number num

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_submachine_output`](#classshogun_1_1CMulticlassMachine_1ab88dc1b9614d23db76dc2b7e2ee683a2)`(int32_t i,int32_t num)` {#classshogun_1_1CMulticlassMachine_1ab88dc1b9614d23db76dc2b7e2ee683a2}

get output of i-th submachine for num-th vector 
#### Parameters
* `i` number of submachine 

* `num` number of feature vector 

#### Returns
output

#### `public virtual `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * `[`apply_multiclass`](#classshogun_1_1CMulticlassMachine_1a250aa566fff0edb31433db98f70a7f15)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMulticlassMachine_1a250aa566fff0edb31433db98f70a7f15}

classify all examples

#### Returns
resulting labels

#### `public virtual `[`CMultilabelLabels`](#classshogun_1_1CMultilabelLabels)` * `[`apply_multilabel_output`](#classshogun_1_1CMulticlassMachine_1a6f2a839aa4ebc25cb9f37edc1739f328)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data,int32_t n_outputs)` {#classshogun_1_1CMulticlassMachine_1a6f2a839aa4ebc25cb9f37edc1739f328}

classify all examples with multiple output

#### Returns
resulting labels

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`apply_one`](#classshogun_1_1CMulticlassMachine_1aa3e372f16ab13497b59cc12b2118ffdb)`(int32_t vec_idx)` {#classshogun_1_1CMulticlassMachine_1aa3e372f16ab13497b59cc12b2118ffdb}

classify one example 
#### Parameters
* `vec_idx` 

#### Returns
label

#### `public inline `[`CMulticlassStrategy`](#classshogun_1_1CMulticlassStrategy)` * `[`get_multiclass_strategy`](#classshogun_1_1CMulticlassMachine_1a0d8d56d6a79db5c58daa9c250ce31684)`() const` {#classshogun_1_1CMulticlassMachine_1a0d8d56d6a79db5c58daa9c250ce31684}

get the type of multiclass'ness

#### Returns
multiclass type one vs one etc

#### `public inline `[`CRejectionStrategy`](#classshogun_1_1CRejectionStrategy)` * `[`get_rejection_strategy`](#classshogun_1_1CMulticlassMachine_1a9d9957c5a644d992be728dbd3946146a)`() const` {#classshogun_1_1CMulticlassMachine_1a9d9957c5a644d992be728dbd3946146a}

returns rejection strategy

#### Returns
rejection strategy

#### `public inline void `[`set_rejection_strategy`](#classshogun_1_1CMulticlassMachine_1aa301bb9b887b69737640870f56e7f2b0)`(`[`CRejectionStrategy`](#classshogun_1_1CRejectionStrategy)` * rejection_strategy)` {#classshogun_1_1CMulticlassMachine_1aa301bb9b887b69737640870f56e7f2b0}

sets rejection strategy

#### Parameters
* `rejection_strategy` rejection strategy to be set

#### `public inline `[`EProbHeuristicType`](#namespaceshogun_1ad7ce6e7dfc495887fab183cd2f3a3351)` `[`get_prob_heuris`](#classshogun_1_1CMulticlassMachine_1ad1e8ccf13b994458c29d76421dbbed63)`()` {#classshogun_1_1CMulticlassMachine_1ad1e8ccf13b994458c29d76421dbbed63}

get prob output heuristic of multiclass strategy

#### `public inline void `[`set_prob_heuris`](#classshogun_1_1CMulticlassMachine_1a5ee2f2f764552ffb587128071af91cd6)`(`[`EProbHeuristicType`](#namespaceshogun_1ad7ce6e7dfc495887fab183cd2f3a3351)` prob_heuris)` {#classshogun_1_1CMulticlassMachine_1a5ee2f2f764552ffb587128071af91cd6}

set prob output heuristic of multiclass strategy 
#### Parameters
* `prob_heuris` type of probability heuristic

#### `public int32_t `[`get_num_machines`](#classshogun_1_1CBaseMulticlassMachine_1a61596dedd23969cf46312187ee17afe5)`() const` {#classshogun_1_1CBaseMulticlassMachine_1a61596dedd23969cf46312187ee17afe5}

get number of machines

#### Returns
number of machines

#### `public virtual `[`EProblemType`](#namespaceshogun_1a0aa89aa872f89f6a174de2f45b7596d4)` `[`get_machine_problem_type`](#classshogun_1_1CBaseMulticlassMachine_1a135f8d82da3fc55807d1640080358500)`() const` {#classshogun_1_1CBaseMulticlassMachine_1a135f8d82da3fc55807d1640080358500}

get problem type

#### `public virtual bool `[`is_label_valid`](#classshogun_1_1CBaseMulticlassMachine_1abc2e336339ace0a7656f4822a98fad0a)`(`[`CLabels`](#classshogun_1_1CLabels)` * lab) const` {#classshogun_1_1CBaseMulticlassMachine_1abc2e336339ace0a7656f4822a98fad0a}

check whether the labels is valid.

#### Parameters
* `lab` the labels being checked, guaranteed to be non-NULL

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

#### `public virtual `[`CBinaryLabels`](#classshogun_1_1CBinaryLabels)` * `[`apply_binary`](#classshogun_1_1CMachine_1a16a7dee83bb61aedc93792df578d4a77)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMachine_1a16a7dee83bb61aedc93792df578d4a77}

apply machine to data in means of binary classification problem

#### `public virtual `[`CRegressionLabels`](#classshogun_1_1CRegressionLabels)` * `[`apply_regression`](#classshogun_1_1CMachine_1aaeea92e0e4795e7f63f067c16f162302)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMachine_1aaeea92e0e4795e7f63f067c16f162302}

apply machine to data in means of regression problem

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

#### `public virtual `[`EMachineType`](#namespaceshogun_1af181c832c12de7a0c3b02425986106cc)` `[`get_classifier_type`](#classshogun_1_1CMachine_1a177dc18a9a5639da395099947cb44501)`()` {#classshogun_1_1CMachine_1a177dc18a9a5639da395099947cb44501}

get classifier type

#### Returns
classifier type NONE

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

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_train_factor`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1abe6bf179fab6adbea480bc324223a8cf) {#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1abe6bf179fab6adbea480bc324223a8cf}

train factor

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_source_bias`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a633511a34e9ae2637d00f6a7ea443056) {#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a633511a34e9ae2637d00f6a7ea443056}

source bias

#### `protected `[`CLinearMulticlassMachine`](#classshogun_1_1CLinearMulticlassMachine)` * `[`m_source_machine`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a9d63efb4180842da42905363f1768906) {#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a9d63efb4180842da42905363f1768906}

source domain machine

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_C`](#classshogun_1_1CMulticlassLibLinear_1a5c2dd8f13b5a4936ebadc023c854e9d1) {#classshogun_1_1CMulticlassLibLinear_1a5c2dd8f13b5a4936ebadc023c854e9d1}

regularization constant for each machine

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_epsilon`](#classshogun_1_1CMulticlassLibLinear_1af4806209595723fa21dc4dab36541f45) {#classshogun_1_1CMulticlassLibLinear_1af4806209595723fa21dc4dab36541f45}

tolerance

#### `protected int32_t `[`m_max_iter`](#classshogun_1_1CMulticlassLibLinear_1aff3aa88417a9ec8ed59a3c8fec0d093d) {#classshogun_1_1CMulticlassLibLinear_1aff3aa88417a9ec8ed59a3c8fec0d093d}

max number of iterations

#### `protected bool `[`m_use_bias`](#classshogun_1_1CMulticlassLibLinear_1acef1b85919183268aad9933f8b60b01c) {#classshogun_1_1CMulticlassLibLinear_1acef1b85919183268aad9933f8b60b01c}

use bias

#### `protected bool `[`m_save_train_state`](#classshogun_1_1CMulticlassLibLinear_1af2a60bc94f8bd9a75b6704657581d124) {#classshogun_1_1CMulticlassLibLinear_1af2a60bc94f8bd9a75b6704657581d124}

save train state

#### `protected mcsvm_state * `[`m_train_state`](#classshogun_1_1CMulticlassLibLinear_1aee9ba6cd266c2322c2098a04d923822a) {#classshogun_1_1CMulticlassLibLinear_1aee9ba6cd266c2322c2098a04d923822a}

solver state

#### `protected `[`CDotFeatures`](#classshogun_1_1CDotFeatures)` * `[`m_features`](#classshogun_1_1CLinearMulticlassMachine_1a69c7ea341f231739924f54ee0fe48521) {#classshogun_1_1CLinearMulticlassMachine_1a69c7ea341f231739924f54ee0fe48521}

features

#### `protected `[`CMulticlassStrategy`](#classshogun_1_1CMulticlassStrategy)` * `[`m_multiclass_strategy`](#classshogun_1_1CMulticlassMachine_1ad6eb1bc28c3ab3d390a88968040dcabe) {#classshogun_1_1CMulticlassMachine_1ad6eb1bc28c3ab3d390a88968040dcabe}

type of multiclass strategy

#### `protected `[`CMachine`](#classshogun_1_1CMachine)` * `[`m_machine`](#classshogun_1_1CMulticlassMachine_1acd634baf350a2c33a0701b3ca935d677) {#classshogun_1_1CMulticlassMachine_1acd634baf350a2c33a0701b3ca935d677}

machine

#### `protected `[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` * `[`m_machines`](#classshogun_1_1CBaseMulticlassMachine_1acd59fab07dd68c8bd831e76bd870fbbb) {#classshogun_1_1CBaseMulticlassMachine_1acd59fab07dd68c8bd831e76bd870fbbb}

machines

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

#### `protected virtual `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`obtain_regularizer_matrix`](#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a6873aff648f0d0a5bbe4d6816ce46689)`() const` {#classshogun_1_1CDomainAdaptationMulticlassLibLinear_1a6873aff648f0d0a5bbe4d6816ce46689}

obtain regularizer (w0) matrix

#### `protected virtual bool `[`train_machine`](#classshogun_1_1CMulticlassLibLinear_1ac6ad4326a1641cb16d8d74d2ac00e9d3)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMulticlassLibLinear_1ac6ad4326a1641cb16d8d74d2ac00e9d3}

train machine

#### `protected inline virtual bool `[`init_machine_for_train`](#classshogun_1_1CLinearMulticlassMachine_1a18b2a5959cd2156ea0315c19be8ddd90)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CLinearMulticlassMachine_1a18b2a5959cd2156ea0315c19be8ddd90}

init machine for train with setting features

#### `protected inline virtual bool `[`init_machines_for_apply`](#classshogun_1_1CLinearMulticlassMachine_1a1fdce1052c1cc6ce067bfe6b678f8b2c)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CLinearMulticlassMachine_1a1fdce1052c1cc6ce067bfe6b678f8b2c}

init machines for applying with setting features

#### `protected inline virtual bool `[`is_ready`](#classshogun_1_1CLinearMulticlassMachine_1ab9f470c03cafceb7df880bc25ca7a713)`()` {#classshogun_1_1CLinearMulticlassMachine_1ab9f470c03cafceb7df880bc25ca7a713}

check features availability

#### `protected inline virtual `[`CMachine`](#classshogun_1_1CMachine)` * `[`get_machine_from_trained`](#classshogun_1_1CLinearMulticlassMachine_1a746274f0ba4151b38527852bbd0360e4)`(`[`CMachine`](#classshogun_1_1CMachine)` * machine)` {#classshogun_1_1CLinearMulticlassMachine_1a746274f0ba4151b38527852bbd0360e4}

construct linear machine from given linear machine

#### `protected inline virtual int32_t `[`get_num_rhs_vectors`](#classshogun_1_1CLinearMulticlassMachine_1aa9b066abb858b4dc0684bac22d004e4f)`()` {#classshogun_1_1CLinearMulticlassMachine_1aa9b066abb858b4dc0684bac22d004e4f}

get number of rhs feature vectors

#### `protected inline virtual void `[`add_machine_subset`](#classshogun_1_1CLinearMulticlassMachine_1a3573ec176ce08901d5329d1d39047a90)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > subset)` {#classshogun_1_1CLinearMulticlassMachine_1a3573ec176ce08901d5329d1d39047a90}

set subset to the features of the machine, deletes old one

#### Parameters
* `subset` subset instance to set

#### `protected inline virtual void `[`remove_machine_subset`](#classshogun_1_1CLinearMulticlassMachine_1a00b440d35fa9b4a7727a85daebe6d848)`()` {#classshogun_1_1CLinearMulticlassMachine_1a00b440d35fa9b4a7727a85daebe6d848}

deletes any subset set to the features of the machine

#### `protected inline virtual void `[`store_model_features`](#classshogun_1_1CLinearMulticlassMachine_1ae0a84ada96561ce09c35e2839f8ca512)`()` {#classshogun_1_1CLinearMulticlassMachine_1ae0a84ada96561ce09c35e2839f8ca512}

Stores feature data of underlying model. Does nothing because Linear machines store the normal vector of the separating hyperplane and therefore the model anyway

#### `protected void `[`init_strategy`](#classshogun_1_1CMulticlassMachine_1aee05c0d5e1aa151f0e55b27b906611ea)`()` {#classshogun_1_1CMulticlassMachine_1aee05c0d5e1aa151f0e55b27b906611ea}

init strategy

#### `protected void `[`clear_machines`](#classshogun_1_1CMulticlassMachine_1a7e5d0a721abdf9fc144ce8560e3d77ea)`()` {#classshogun_1_1CMulticlassMachine_1a7e5d0a721abdf9fc144ce8560e3d77ea}

clear machines

#### `protected inline virtual bool `[`is_acceptable_machine`](#classshogun_1_1CMulticlassMachine_1ae4b20841b2638e5ca452e6a1cd7c2021)`(`[`CMachine`](#classshogun_1_1CMachine)` * machine)` {#classshogun_1_1CMulticlassMachine_1ae4b20841b2638e5ca452e6a1cd7c2021}

whether the machine is acceptable in set_machine

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

