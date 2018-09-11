---
classname: "shogun::CDynProg"
type: "class"
parents:
   - CSGObject
---

# class `shogun::CDynProg` {#classshogun_1_1CDynProg}

```
class shogun::CDynProg
  : public CSGObject
```

Dynamic Programming Class.

Structure and Function collection. This Class implements a Dynamic Programming functions.

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
`public  `[`CDynProg`](#classshogun_1_1CDynProg_1a27ff321ed0e54e4d52fc9ab1e7f99e33)`(int32_t p_num_svms)` | constructor
`public virtual  `[`~CDynProg`](#classshogun_1_1CDynProg_1a21f836a198f4493294e6cc41fcd91118)`()` | 
`public void `[`set_num_states`](#classshogun_1_1CDynProg_1a57e0149176b87c1b90137b925c8f0b35)`(int32_t N)` | set number of states use this to set N first
`public int32_t `[`get_num_states`](#classshogun_1_1CDynProg_1a14e34b70e7f3b0b35ef0a133e6415394)`()` | get num states
`public int32_t `[`get_num_svms`](#classshogun_1_1CDynProg_1ad0d98f4a4c9a1cf579a58b2188ee4f11)`()` | get num svms
`public void `[`init_content_svm_value_array`](#classshogun_1_1CDynProg_1a857f58dfba65946c1baebd5200b27b10)`(const int32_t p_num_svms)` | init [CDynamicArray](#classshogun_1_1CDynamicArray) for precomputed content svm values with size seq_len x num_svms
`public void `[`init_tiling_data`](#classshogun_1_1CDynProg_1a224e9df4d58dfc7e23d32e563de0e3c8)`(int32_t * probe_pos,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * intensities,const int32_t num_probes)` | init [CDynamicArray](#classshogun_1_1CDynamicArray) for precomputed tiling intensitie-plif-values with size seq_len x num_svms
`public void `[`precompute_tiling_plifs`](#classshogun_1_1CDynProg_1ac75bf779f027db6b4d8ec475208bbf6b)`(`[`CPlif`](#classshogun_1_1CPlif)` ** PEN,const int32_t * tiling_plif_ids,const int32_t num_tiling_plifs)` | precompute tiling Plifs
`public void `[`resize_lin_feat`](#classshogun_1_1CDynProg_1aa7e866053715eab41995c4b5f8c621ff)`(int32_t num_new_feat)` | append rows to linear features array
`public void `[`set_p_vector`](#classshogun_1_1CDynProg_1a3613b05160b55f69fed26bcecc25087b)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > p)` | set vector p
`public void `[`set_q_vector`](#classshogun_1_1CDynProg_1a45809b481de85ac2e3d8c0a432cd4738)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > q)` | set vector q
`public void `[`set_a`](#classshogun_1_1CDynProg_1a385a4f12495f07113edb6dc6f74dd76e)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > a)` | set matrix a
`public void `[`set_a_id`](#classshogun_1_1CDynProg_1ad5d70c175242f5c6fdda346590c949dc)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< int32_t > a)` | set a id
`public void `[`set_a_trans_matrix`](#classshogun_1_1CDynProg_1a9f66d6e343b7ff988720db76fc1c7a78)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > a_trans)` | set a transition matrix
`public void `[`init_mod_words_array`](#classshogun_1_1CDynProg_1a4d1a5dd080c7040f33c17e58ec834281)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< int32_t > p_mod_words_array)` | init mod words array
`public bool `[`check_svm_arrays`](#classshogun_1_1CDynProg_1af55fe99feaea35b351fd19e1f84af39d)`()` | check SVM arrays call this function to check consistency
`public void `[`set_observation_matrix`](#classshogun_1_1CDynProg_1a30e7d5b369ab97aaa98f9f5a4bde2e2a)`(`[`SGNDArray](#classshogun_1_1SGNDArray)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > seq)` | set best path seq
`public int32_t `[`get_num_positions`](#classshogun_1_1CDynProg_1ad595d38102e449f257f4e18d13865ecc)`()` | get number of positions; the dynamic program is sparse encoded and this function gives the number of positions that can actually be part of a predicted path
`public void `[`set_content_type_array`](#classshogun_1_1CDynProg_1acfa133db85aed93515247c648bde9d5b)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > seg_path)` | set an array of length #(candidate positions) which specifies the content type of each pos and a mask that determines to which extend the loss should be applied to this position; this is a way to encode label confidence via weights between zero and one
`public void `[`set_pos`](#classshogun_1_1CDynProg_1aa362074f7b74200ed03435b9d3179396)`(`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > pos)` | set best path pos
`public void `[`set_orf_info`](#classshogun_1_1CDynProg_1ac0e06325eb9074a86595508201d82a3f)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< int32_t > orf_info)` | set best path orf info only for compute_nbest_paths
`public void `[`set_gene_string`](#classshogun_1_1CDynProg_1a3ae8f885e16af6c4b1ba182b6d3ce3b9)`(`[`SGVector`](#classshogun_1_1SGVector)`< char > genestr)` | set best path genesstr
`public void `[`set_dict_weights`](#classshogun_1_1CDynProg_1ab9530b06b1396b2366d1253ce028c50e)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > dictionary_weights)` | set best path dict weights
`public void `[`best_path_set_segment_loss`](#classshogun_1_1CDynProg_1ab640514cedb788c2a9bf245ef4ce18df)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > segment_loss)` | set best path segment loss
`public void `[`best_path_set_segment_ids_mask`](#classshogun_1_1CDynProg_1a40eaf722e9c1de2cb88adb88a5ded04f)`(int32_t * segment_ids,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * segment_mask,int32_t m)` | set best path segmend ids mask
`public void `[`set_sparse_features`](#classshogun_1_1CDynProg_1ad26eaf9119f4a2dcf98fdbd54d92cf95)`(`[`CSparseFeatures](#classshogun_1_1CSparseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * seq_sparse1,`[`CSparseFeatures](#classshogun_1_1CSparseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * seq_sparse2)` | set sparse feature matrices
`public void `[`set_plif_matrices`](#classshogun_1_1CDynProg_1aa69ef6966845487ba9ddac5fce163f10)`(`[`CPlifMatrix`](#classshogun_1_1CPlifMatrix)` * pm)` | set plif matrices
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_scores`](#classshogun_1_1CDynProg_1acc36c78d5cf30f191e5850dbdbb98e88)`()` | best path get scores
`public `[`SGMatrix`](#classshogun_1_1SGMatrix)`< int32_t > `[`get_states`](#classshogun_1_1CDynProg_1a4722364db736a863c4c8f77c46b0482a)`()` | best path get states
`public `[`SGMatrix`](#classshogun_1_1SGMatrix)`< int32_t > `[`get_positions`](#classshogun_1_1CDynProg_1a9611a80d1cf221c6b138118998ce232e)`()` | best path get positions
`public void `[`compute_nbest_paths`](#classshogun_1_1CDynProg_1a6c6bff56801a2761e431c9dae493112c)`(int32_t max_num_signals,bool use_orf,int16_t nbest,bool with_loss,bool with_multiple_sequences)` | run the viterbi algorithm to compute the n best viterbi paths
`public void `[`best_path_trans_deriv`](#classshogun_1_1CDynProg_1a05d878932ca526cc9bec8274331a2223)`(int32_t * my_state_seq,int32_t * my_pos_seq,int32_t my_seq_len,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * seq_array,int32_t max_num_signals)` | given a path though the state model and the corresponding positions compute the features. This can be seen as the derivative of the score (output of dynamic program) with respect to the parameters
`public void `[`set_my_state_seq`](#classshogun_1_1CDynProg_1a9a1f0dbfc847d25afa82616298fedf19)`(int32_t * my_state_seq)` | set best path my state sequence
`public void `[`set_my_pos_seq`](#classshogun_1_1CDynProg_1a9915c365b0a17ca03013eabf8ce74088)`(int32_t * my_pos_seq)` | set best path my position sequence
`public void `[`get_path_scores`](#classshogun_1_1CDynProg_1adbf865ec2e89b1e215138ca92caab653)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` ** my_scores,int32_t * seq_len)` | get path scores
`public void `[`get_path_losses`](#classshogun_1_1CDynProg_1a8a06229c78de394a63d9ea392bf1679a)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` ** my_losses,int32_t * seq_len)` | get path losses
`public inline `[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` `[`get_N`](#classshogun_1_1CDynProg_1a0faa46357d58665b16ccbe3ecc151cc4)`() const` | access function for number of states N
`public inline void `[`set_q`](#classshogun_1_1CDynProg_1affcb5bc5c634af0046c2f18ba3019034)`(`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` offset,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` value)` | access function for probability of end states 
`public inline void `[`set_p`](#classshogun_1_1CDynProg_1a00dc9157bbe651b3a0c5d96d51e8f787)`(`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` offset,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` value)` | access function for probability of first state 
`public inline void `[`set_a`](#classshogun_1_1CDynProg_1a948bfbabf53bd9ddf0483037fd800523)`(`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` line_,`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` column,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` value)` | access function for matrix a
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_q`](#classshogun_1_1CDynProg_1a688fb8b85067ee3dc15ef8f209aeb317)`(`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` offset) const` | access function for probability of end states
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_q_deriv`](#classshogun_1_1CDynProg_1a06c72fa3363a68f3a3f9f016af8b7c3b)`(`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` offset) const` | access function for derivated probability of end states
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_p`](#classshogun_1_1CDynProg_1add631aa92d258b32e8f8aab9727689a0)`(`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` offset) const` | access function for probability of initial states
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_p_deriv`](#classshogun_1_1CDynProg_1aab4af3184530339318dddc51d25f37ae)`(`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` offset) const` | access function for derivated probability of initial states
`public void `[`precompute_content_values`](#classshogun_1_1CDynProg_1a099e5d22e30f58db09cfd8c5ceba877d)`()` | create array of precomputed content svm values
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`get_lin_feat`](#classshogun_1_1CDynProg_1a64b22c688a241df26cefcb0f67f47962)`(int32_t & dim1,int32_t & dim2)` | return array of precomputed linear features like content predictions and PLiFed tiling array data Jonas
`public inline void `[`set_lin_feat`](#classshogun_1_1CDynProg_1a237f047cd00c5a743ec58a8668a27888)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * p_lin_feat,int32_t p_num_svms,int32_t p_seq_len)` | set your own array of precomputed linear features like content predictions and PLiFed tiling array data Jonas
`public void `[`create_word_string`](#classshogun_1_1CDynProg_1a011a18ce8abe5791cde3c65372ff18bf)`()` | create word string from char* Jonas
`public void `[`precompute_stop_codons`](#classshogun_1_1CDynProg_1a7aef75295ac5b0305f81d6e1c7d84a39)`()` | precompute stop codons
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_a`](#classshogun_1_1CDynProg_1acabe9a67be107baa5e0d215ce8a36aae)`(`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` line_,`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` column) const` | access function for matrix a
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_a_deriv`](#classshogun_1_1CDynProg_1a4d41624896af12d754e5deb6171cba33)`(`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` line_,`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` column) const` | access function for matrix a derivated
`public void `[`set_intron_list`](#classshogun_1_1CDynProg_1a551977c8b8dbd31a90e3e415c202a526)`(`[`CIntronList`](#classshogun_1_1CIntronList)` * intron_list,int32_t num_plifs)` | set intron list
`public inline `[`CSegmentLoss`](#classshogun_1_1CSegmentLoss)` * `[`get_segment_loss_object`](#classshogun_1_1CDynProg_1a8298508c1b763a6b9619ef67c613073b)`()` | get the segment loss object
`public inline void `[`long_transition_settings`](#classshogun_1_1CDynProg_1a7356b176bbf8b353ab7089684b775b74)`(bool use_long_transitions,int32_t threshold,int32_t max_len)` | settings for long transition handling
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
`protected int32_t `[`m_num_degrees`](#classshogun_1_1CDynProg_1a367b0ebc41bdcfc8a9be258f87036fc3) | number of degress
`protected int32_t `[`m_num_svms`](#classshogun_1_1CDynProg_1a50244e60b5d90658d4423fa892abd9b0) | number of SVMs
`protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_word_degree`](#classshogun_1_1CDynProg_1a62e9315c4342d411d9bb366e1fcbc5c6) | word degree
`protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_cum_num_words`](#classshogun_1_1CDynProg_1a42dd441c7ad1476157bfaaeeeeaca3b6) | cum num words
`protected int32_t * `[`m_cum_num_words_array`](#classshogun_1_1CDynProg_1a9dc50527b8ca7ecb08bc12858887c9d6) | cum num words array
`protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_num_words`](#classshogun_1_1CDynProg_1aa2bcc679f5f98579b309270b07c4262d) | num words
`protected int32_t * `[`m_num_words_array`](#classshogun_1_1CDynProg_1acf7bac9fb892e16c499839a0e1ec9326) | num words array
`protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_mod_words`](#classshogun_1_1CDynProg_1a24527c7037ea964092a41808088b29cc) | mod words
`protected int32_t * `[`m_mod_words_array`](#classshogun_1_1CDynProg_1adcf533c8d6407536e84bfefac1408148) | mod words array
`protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< bool > `[`m_sign_words`](#classshogun_1_1CDynProg_1a675c7f6b4ee6f7446bd8fe3f4f8f1e74) | sign words
`protected bool * `[`m_sign_words_array`](#classshogun_1_1CDynProg_1a2be26b66e8dea2959b689e741088bc35) | sign words array
`protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_string_words`](#classshogun_1_1CDynProg_1ab9e535d23bdc4b44cdf12c39ba9cd4a3) | string words
`protected int32_t * `[`m_string_words_array`](#classshogun_1_1CDynProg_1a6c916933ce4ea3d27c579a093342e712) | string words array
`protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_num_unique_words`](#classshogun_1_1CDynProg_1aaba8e39cbb0184f1ed709959bda6210e) | SVM start position number of unique words
`protected bool `[`m_svm_arrays_clean`](#classshogun_1_1CDynProg_1aabaa85d02040381fae30bc97cc3fbf10) | SVM arrays clean
`protected int32_t `[`m_max_a_id`](#classshogun_1_1CDynProg_1aeeceb871f482672408039dba4e48b760) | max a id
`protected `[`CDynamicArray](#classshogun_1_1CDynamicArray)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_observation_matrix`](#classshogun_1_1CDynProg_1ad0d75e543a7b1fcf2984625df2d5181f) | sequence
`protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_pos`](#classshogun_1_1CDynProg_1a9303766db162c41b3573f85832229278) | candidate position
`protected int32_t `[`m_seq_len`](#classshogun_1_1CDynProg_1a3a504e9ee5462ccac4717b1682ce65ad) | number of candidate positions
`protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_orf_info`](#classshogun_1_1CDynProg_1a22d106b703a54a47d1fcd0b681b93c70) | orf info
`protected `[`CDynamicArray](#classshogun_1_1CDynamicArray)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_segment_sum_weights`](#classshogun_1_1CDynProg_1a87f291f21d8e277475bcf85cfca4ff76) | segment sum weights
`protected `[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` `[`m_plif_list`](#classshogun_1_1CDynProg_1a4331f8f0b261cefe9eac0b1c38997151) | Plif list
`protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< char > `[`m_genestr`](#classshogun_1_1CDynProg_1ad8899de40c111310d21afd3a3613ee9c) | a single string (to be segmented)
`protected uint16_t *** `[`m_wordstr`](#classshogun_1_1CDynProg_1a03e704ba5e57f4033389dd8a3c043295) | wordstr is a vector of L n-gram indices, with wordstr(i) representing a number betweeen 0 and 4095 corresponding to the 6-mer in genestr(i-5:i) pos is a vector of candidate transition positions (it is input to compute_nbest_paths) t_end is some index in pos
`protected `[`CDynamicArray](#classshogun_1_1CDynamicArray)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_dict_weights`](#classshogun_1_1CDynProg_1af21b4733c6b7bf88534949afd53d1e85) | dict weights
`protected `[`CDynamicArray](#classshogun_1_1CDynamicArray)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_segment_loss`](#classshogun_1_1CDynProg_1ab061fa7fdcbb512ccda6701e1eba81b9) | segment loss
`protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_segment_ids`](#classshogun_1_1CDynProg_1a3329906a7f3c8e1a0709df1a9c7de4d4) | segment IDs
`protected `[`CDynamicArray](#classshogun_1_1CDynamicArray)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_segment_mask`](#classshogun_1_1CDynProg_1af147f4cfc62f621e3e7474fbf21c4a22) | segment mask
`protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_my_state_seq`](#classshogun_1_1CDynProg_1ab0904df5d08c97ffcaadaf0d374cb852) | my state seq
`protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_my_pos_seq`](#classshogun_1_1CDynProg_1a6c01bf48cc81476cbad9f92b3c9f6021) | my position sequence
`protected `[`CDynamicArray](#classshogun_1_1CDynamicArray)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_my_scores`](#classshogun_1_1CDynProg_1a6793fa5a9df2af73391b75c2d2ccfb6b) | my scores
`protected `[`CDynamicArray](#classshogun_1_1CDynamicArray)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_my_losses`](#classshogun_1_1CDynProg_1a05a84d743b1c3e1ddbcd299940ccb246) | my losses
`protected `[`CSegmentLoss`](#classshogun_1_1CSegmentLoss)` * `[`m_seg_loss_obj`](#classshogun_1_1CDynProg_1ad2c830d06ae332c2f0255d3f3b55dd86) | segment loss object containing the functions to compute the segment loss
`protected `[`CDynamicArray](#classshogun_1_1CDynamicArray)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_scores`](#classshogun_1_1CDynProg_1ac51bd058c3378f1cfcce53d189f9ab58) | scores
`protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_states`](#classshogun_1_1CDynProg_1a0ba92d1590484e1df2780ce629c4b9fe) | states
`protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_positions`](#classshogun_1_1CDynProg_1ab1d87fe86af2d2c8ba0f2bd808cd57e7) | positions
`protected `[`CSparseFeatures](#classshogun_1_1CSparseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * `[`m_seq_sparse1`](#classshogun_1_1CDynProg_1a9ec2dc54953bddd398dcda7f3feb7721) | sparse feature matrix dim1
`protected `[`CSparseFeatures](#classshogun_1_1CSparseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * `[`m_seq_sparse2`](#classshogun_1_1CDynProg_1ab753e47a12e65582a01f8ff80293baa0) | sparse feature matrix dim2
`protected `[`CPlifMatrix`](#classshogun_1_1CPlifMatrix)` * `[`m_plif_matrices`](#classshogun_1_1CDynProg_1a6ff8af3c85978d51a9cb8626cd92524b) | plif matrices
`protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< bool > `[`m_genestr_stop`](#classshogun_1_1CDynProg_1a53ffdfa661170471c75a2798efa0b331) | storeage of stop codons array of size length(sequence)
`protected `[`CIntronList`](#classshogun_1_1CIntronList)` * `[`m_intron_list`](#classshogun_1_1CDynProg_1a49df13b1237518586a93829cf3d08f63) | administers a list of introns and quality scores and provides functions for fast access
`protected int32_t `[`m_num_intron_plifs`](#classshogun_1_1CDynProg_1ad112775259a716bb5f46f72011ea3654) | number of intron features and plifs
`protected `[`CDynamicArray](#classshogun_1_1CDynamicArray)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_lin_feat`](#classshogun_1_1CDynProg_1aa776be3db62d3d55dfa05d33dd04adea) | array for storage of precomputed linear features linge content svm values or pliffed tiling data Jonas
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`m_raw_intensities`](#classshogun_1_1CDynProg_1a19536d9c21632e852917879d646e9300) | raw intensities
`protected int32_t * `[`m_probe_pos`](#classshogun_1_1CDynProg_1ad592a2d93aa39ad322ed0002ca229d63) | probe position
`protected int32_t * `[`m_num_probes_cum`](#classshogun_1_1CDynProg_1a11a3f37656d6e8ec2c11665572cc8f82) | number of probes
`protected int32_t * `[`m_num_lin_feat_plifs_cum`](#classshogun_1_1CDynProg_1ac671de8dc0c1a228d6971f68459dcc7d) | num lin feat plifs cum
`protected int32_t `[`m_num_raw_data`](#classshogun_1_1CDynProg_1aca9d758f6c39ee7848df23bd8cbf13e2) | number of additional data tracks like tiling, RNA-Seq, ...
`protected bool `[`m_long_transitions`](#classshogun_1_1CDynProg_1a467e20b2b645981955301b80f8d55d76) | use long transition approximation
`protected int32_t `[`m_long_transition_threshold`](#classshogun_1_1CDynProg_1ae2b1e846dfe744c0f362a2c6976afb24) | threshold for transitions that are computed the traditional way
`protected void `[`lookup_content_svm_values`](#classshogun_1_1CDynProg_1a15bf99ea5b26093da2bbb6917bdd23d5)`(const int32_t from_state,const int32_t to_state,const int32_t from_pos,const int32_t to_pos,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * svm_values,int32_t frame)` | lookup content SVM values
`protected inline void `[`lookup_tiling_plif_values`](#classshogun_1_1CDynProg_1a97d3c27407c59dcab30c4c8283427bb4)`(const int32_t from_state,const int32_t to_state,const int32_t len,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * svm_values)` | lookup tiling Plif values
`protected inline int32_t `[`find_frame`](#classshogun_1_1CDynProg_1a9a2af9e788d0bdbb065b1a25ec265861)`(const int32_t from_state)` | find frame
`protected inline int32_t `[`raw_intensities_interval_query`](#classshogun_1_1CDynProg_1a9bc3f4e512122eff1fa8930e141d26f8)`(const int32_t from_pos,const int32_t to_pos,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * intensities,int32_t type)` | raw intensities interval query
`protected bool `[`extend_orf`](#classshogun_1_1CDynProg_1a9dfb12f3fac92fe77a8bed03e579d4db)`(int32_t orf_from,int32_t orf_to,int32_t start,int32_t & last_pos,int32_t to)` | extend orf
`protected inline virtual const char * `[`get_name`](#classshogun_1_1CDynProg_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` | #### Returns
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

#### `public  `[`CDynProg`](#classshogun_1_1CDynProg_1a27ff321ed0e54e4d52fc9ab1e7f99e33)`(int32_t p_num_svms)` {#classshogun_1_1CDynProg_1a27ff321ed0e54e4d52fc9ab1e7f99e33}

constructor

#### Parameters
* `p_num_svms` number of SVMs

#### `public virtual  `[`~CDynProg`](#classshogun_1_1CDynProg_1a21f836a198f4493294e6cc41fcd91118)`()` {#classshogun_1_1CDynProg_1a21f836a198f4493294e6cc41fcd91118}

#### `public void `[`set_num_states`](#classshogun_1_1CDynProg_1a57e0149176b87c1b90137b925c8f0b35)`(int32_t N)` {#classshogun_1_1CDynProg_1a57e0149176b87c1b90137b925c8f0b35}

set number of states use this to set N first

#### Parameters
* `N` new N

#### `public int32_t `[`get_num_states`](#classshogun_1_1CDynProg_1a14e34b70e7f3b0b35ef0a133e6415394)`()` {#classshogun_1_1CDynProg_1a14e34b70e7f3b0b35ef0a133e6415394}

get num states

#### `public int32_t `[`get_num_svms`](#classshogun_1_1CDynProg_1ad0d98f4a4c9a1cf579a58b2188ee4f11)`()` {#classshogun_1_1CDynProg_1ad0d98f4a4c9a1cf579a58b2188ee4f11}

get num svms

#### `public void `[`init_content_svm_value_array`](#classshogun_1_1CDynProg_1a857f58dfba65946c1baebd5200b27b10)`(const int32_t p_num_svms)` {#classshogun_1_1CDynProg_1a857f58dfba65946c1baebd5200b27b10}

init [CDynamicArray](#classshogun_1_1CDynamicArray) for precomputed content svm values with size seq_len x num_svms

#### Parameters
* `p_num_svms` number of svm weight vectors for content prediction

#### `public void `[`init_tiling_data`](#classshogun_1_1CDynProg_1a224e9df4d58dfc7e23d32e563de0e3c8)`(int32_t * probe_pos,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * intensities,const int32_t num_probes)` {#classshogun_1_1CDynProg_1a224e9df4d58dfc7e23d32e563de0e3c8}

init [CDynamicArray](#classshogun_1_1CDynamicArray) for precomputed tiling intensitie-plif-values with size seq_len x num_svms

#### Parameters
* `probe_pos` local positions of probes 

* `intensities` intensities of probes 

* `num_probes` number of probes

#### `public void `[`precompute_tiling_plifs`](#classshogun_1_1CDynProg_1ac75bf779f027db6b4d8ec475208bbf6b)`(`[`CPlif`](#classshogun_1_1CPlif)` ** PEN,const int32_t * tiling_plif_ids,const int32_t num_tiling_plifs)` {#classshogun_1_1CDynProg_1ac75bf779f027db6b4d8ec475208bbf6b}

precompute tiling Plifs

#### Parameters
* `PEN` Plif PEN 

* `tiling_plif_ids` tiling plif id's 

* `num_tiling_plifs` number of tiling plifs

#### `public void `[`resize_lin_feat`](#classshogun_1_1CDynProg_1aa7e866053715eab41995c4b5f8c621ff)`(int32_t num_new_feat)` {#classshogun_1_1CDynProg_1aa7e866053715eab41995c4b5f8c621ff}

append rows to linear features array

#### Parameters
* `num_new_feat` number of new rows to add

#### `public void `[`set_p_vector`](#classshogun_1_1CDynProg_1a3613b05160b55f69fed26bcecc25087b)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > p)` {#classshogun_1_1CDynProg_1a3613b05160b55f69fed26bcecc25087b}

set vector p

#### Parameters
* `p` new vector p

#### `public void `[`set_q_vector`](#classshogun_1_1CDynProg_1a45809b481de85ac2e3d8c0a432cd4738)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > q)` {#classshogun_1_1CDynProg_1a45809b481de85ac2e3d8c0a432cd4738}

set vector q

#### Parameters
* `q` new vector q

#### `public void `[`set_a`](#classshogun_1_1CDynProg_1a385a4f12495f07113edb6dc6f74dd76e)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > a)` {#classshogun_1_1CDynProg_1a385a4f12495f07113edb6dc6f74dd76e}

set matrix a

#### Parameters
* `a` new matrix a

#### `public void `[`set_a_id`](#classshogun_1_1CDynProg_1ad5d70c175242f5c6fdda346590c949dc)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< int32_t > a)` {#classshogun_1_1CDynProg_1ad5d70c175242f5c6fdda346590c949dc}

set a id

#### Parameters
* `a` new a id

#### `public void `[`set_a_trans_matrix`](#classshogun_1_1CDynProg_1a9f66d6e343b7ff988720db76fc1c7a78)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > a_trans)` {#classshogun_1_1CDynProg_1a9f66d6e343b7ff988720db76fc1c7a78}

set a transition matrix

#### Parameters
* `a_trans` transition matrix a

#### `public void `[`init_mod_words_array`](#classshogun_1_1CDynProg_1a4d1a5dd080c7040f33c17e58ec834281)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< int32_t > p_mod_words_array)` {#classshogun_1_1CDynProg_1a4d1a5dd080c7040f33c17e58ec834281}

init mod words array

#### Parameters
* `p_mod_words_array` new mod words array

#### `public bool `[`check_svm_arrays`](#classshogun_1_1CDynProg_1af55fe99feaea35b351fd19e1f84af39d)`()` {#classshogun_1_1CDynProg_1af55fe99feaea35b351fd19e1f84af39d}

check SVM arrays call this function to check consistency

#### Returns
whether arrays are ok

#### `public void `[`set_observation_matrix`](#classshogun_1_1CDynProg_1a30e7d5b369ab97aaa98f9f5a4bde2e2a)`(`[`SGNDArray](#classshogun_1_1SGNDArray)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > seq)` {#classshogun_1_1CDynProg_1a30e7d5b369ab97aaa98f9f5a4bde2e2a}

set best path seq

#### Parameters
* `seq` signal features

#### `public int32_t `[`get_num_positions`](#classshogun_1_1CDynProg_1ad595d38102e449f257f4e18d13865ecc)`()` {#classshogun_1_1CDynProg_1ad595d38102e449f257f4e18d13865ecc}

get number of positions; the dynamic program is sparse encoded and this function gives the number of positions that can actually be part of a predicted path

#### Returns
number of positions

#### `public void `[`set_content_type_array`](#classshogun_1_1CDynProg_1acfa133db85aed93515247c648bde9d5b)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > seg_path)` {#classshogun_1_1CDynProg_1acfa133db85aed93515247c648bde9d5b}

set an array of length #(candidate positions) which specifies the content type of each pos and a mask that determines to which extend the loss should be applied to this position; this is a way to encode label confidence via weights between zero and one

#### Parameters
* `seg_path` seg path

#### `public void `[`set_pos`](#classshogun_1_1CDynProg_1aa362074f7b74200ed03435b9d3179396)`(`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > pos)` {#classshogun_1_1CDynProg_1aa362074f7b74200ed03435b9d3179396}

set best path pos

#### Parameters
* `pos` the position vector

#### `public void `[`set_orf_info`](#classshogun_1_1CDynProg_1ac0e06325eb9074a86595508201d82a3f)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< int32_t > orf_info)` {#classshogun_1_1CDynProg_1ac0e06325eb9074a86595508201d82a3f}

set best path orf info only for compute_nbest_paths

#### Parameters
* `orf_info` the orf info

#### `public void `[`set_gene_string`](#classshogun_1_1CDynProg_1a3ae8f885e16af6c4b1ba182b6d3ce3b9)`(`[`SGVector`](#classshogun_1_1SGVector)`< char > genestr)` {#classshogun_1_1CDynProg_1a3ae8f885e16af6c4b1ba182b6d3ce3b9}

set best path genesstr

#### Parameters
* `genestr` gene string

#### `public void `[`set_dict_weights`](#classshogun_1_1CDynProg_1ab9530b06b1396b2366d1253ce028c50e)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > dictionary_weights)` {#classshogun_1_1CDynProg_1ab9530b06b1396b2366d1253ce028c50e}

set best path dict weights

#### Parameters
* `dictionary_weights` dictionary weights

#### `public void `[`best_path_set_segment_loss`](#classshogun_1_1CDynProg_1ab640514cedb788c2a9bf245ef4ce18df)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > segment_loss)` {#classshogun_1_1CDynProg_1ab640514cedb788c2a9bf245ef4ce18df}

set best path segment loss

#### Parameters
* `segment_loss` segment loss

#### `public void `[`best_path_set_segment_ids_mask`](#classshogun_1_1CDynProg_1a40eaf722e9c1de2cb88adb88a5ded04f)`(int32_t * segment_ids,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * segment_mask,int32_t m)` {#classshogun_1_1CDynProg_1a40eaf722e9c1de2cb88adb88a5ded04f}

set best path segmend ids mask

#### Parameters
* `segment_ids` segment ids 

* `segment_mask` segment mask 

* `m` dimension m

#### `public void `[`set_sparse_features`](#classshogun_1_1CDynProg_1ad26eaf9119f4a2dcf98fdbd54d92cf95)`(`[`CSparseFeatures](#classshogun_1_1CSparseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * seq_sparse1,`[`CSparseFeatures](#classshogun_1_1CSparseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * seq_sparse2)` {#classshogun_1_1CDynProg_1ad26eaf9119f4a2dcf98fdbd54d92cf95}

set sparse feature matrices

#### `public void `[`set_plif_matrices`](#classshogun_1_1CDynProg_1aa69ef6966845487ba9ddac5fce163f10)`(`[`CPlifMatrix`](#classshogun_1_1CPlifMatrix)` * pm)` {#classshogun_1_1CDynProg_1aa69ef6966845487ba9ddac5fce163f10}

set plif matrices

#### Parameters
* `pm` plif matrix object

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_scores`](#classshogun_1_1CDynProg_1acc36c78d5cf30f191e5850dbdbb98e88)`()` {#classshogun_1_1CDynProg_1acc36c78d5cf30f191e5850dbdbb98e88}

best path get scores

#### Returns
scores scores

#### `public `[`SGMatrix`](#classshogun_1_1SGMatrix)`< int32_t > `[`get_states`](#classshogun_1_1CDynProg_1a4722364db736a863c4c8f77c46b0482a)`()` {#classshogun_1_1CDynProg_1a4722364db736a863c4c8f77c46b0482a}

best path get states

#### Returns
states states

#### `public `[`SGMatrix`](#classshogun_1_1SGMatrix)`< int32_t > `[`get_positions`](#classshogun_1_1CDynProg_1a9611a80d1cf221c6b138118998ce232e)`()` {#classshogun_1_1CDynProg_1a9611a80d1cf221c6b138118998ce232e}

best path get positions

#### Returns
positions positions

#### `public void `[`compute_nbest_paths`](#classshogun_1_1CDynProg_1a6c6bff56801a2761e431c9dae493112c)`(int32_t max_num_signals,bool use_orf,int16_t nbest,bool with_loss,bool with_multiple_sequences)` {#classshogun_1_1CDynProg_1a6c6bff56801a2761e431c9dae493112c}

run the viterbi algorithm to compute the n best viterbi paths

#### Parameters
* `max_num_signals` maximal number of signals for a single state 

* `use_orf` whether orf shall be used 

* `nbest` number of best paths (n) 

* `with_loss` use loss 

* `with_multiple_sequences` !!!not functional set to false!!!

#### `public void `[`best_path_trans_deriv`](#classshogun_1_1CDynProg_1a05d878932ca526cc9bec8274331a2223)`(int32_t * my_state_seq,int32_t * my_pos_seq,int32_t my_seq_len,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * seq_array,int32_t max_num_signals)` {#classshogun_1_1CDynProg_1a05d878932ca526cc9bec8274331a2223}

given a path though the state model and the corresponding positions compute the features. This can be seen as the derivative of the score (output of dynamic program) with respect to the parameters

#### Parameters
* `my_state_seq` state sequence of the path 

* `my_pos_seq` sequence of positions 

* `my_seq_len` length of state and position sequences 

* `seq_array` array of features 

* `max_num_signals` maximal number of signals

#### `public void `[`set_my_state_seq`](#classshogun_1_1CDynProg_1a9a1f0dbfc847d25afa82616298fedf19)`(int32_t * my_state_seq)` {#classshogun_1_1CDynProg_1a9a1f0dbfc847d25afa82616298fedf19}

set best path my state sequence

#### Parameters
* `my_state_seq` my state sequence

#### `public void `[`set_my_pos_seq`](#classshogun_1_1CDynProg_1a9915c365b0a17ca03013eabf8ce74088)`(int32_t * my_pos_seq)` {#classshogun_1_1CDynProg_1a9915c365b0a17ca03013eabf8ce74088}

set best path my position sequence

#### Parameters
* `my_pos_seq` my position sequence

#### `public void `[`get_path_scores`](#classshogun_1_1CDynProg_1adbf865ec2e89b1e215138ca92caab653)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` ** my_scores,int32_t * seq_len)` {#classshogun_1_1CDynProg_1adbf865ec2e89b1e215138ca92caab653}

get path scores

best_path_trans_deriv result retrieval functions

#### Parameters
* `my_scores` scores 

* `seq_len` length of sequence

#### `public void `[`get_path_losses`](#classshogun_1_1CDynProg_1a8a06229c78de394a63d9ea392bf1679a)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` ** my_losses,int32_t * seq_len)` {#classshogun_1_1CDynProg_1a8a06229c78de394a63d9ea392bf1679a}

get path losses

best_path_trans_deriv result retrieval functions

#### Parameters
* `my_losses` my losses 

* `seq_len` length of sequence

#### `public inline `[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` `[`get_N`](#classshogun_1_1CDynProg_1a0faa46357d58665b16ccbe3ecc151cc4)`() const` {#classshogun_1_1CDynProg_1a0faa46357d58665b16ccbe3ecc151cc4}

access function for number of states N

#### `public inline void `[`set_q`](#classshogun_1_1CDynProg_1affcb5bc5c634af0046c2f18ba3019034)`(`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` offset,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` value)` {#classshogun_1_1CDynProg_1affcb5bc5c634af0046c2f18ba3019034}

access function for probability of end states 
#### Parameters
* `offset` index 0...N-1 

* `value` value to be set

#### `public inline void `[`set_p`](#classshogun_1_1CDynProg_1a00dc9157bbe651b3a0c5d96d51e8f787)`(`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` offset,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` value)` {#classshogun_1_1CDynProg_1a00dc9157bbe651b3a0c5d96d51e8f787}

access function for probability of first state 
#### Parameters
* `offset` index 0...N-1 

* `value` value to be set

#### `public inline void `[`set_a`](#classshogun_1_1CDynProg_1a948bfbabf53bd9ddf0483037fd800523)`(`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` line_,`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` column,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` value)` {#classshogun_1_1CDynProg_1a948bfbabf53bd9ddf0483037fd800523}

access function for matrix a

#### Parameters
* `line_` row in matrix 0...N-1 

* `column` column in matrix 0...N-1 

* `value` value to be set

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_q`](#classshogun_1_1CDynProg_1a688fb8b85067ee3dc15ef8f209aeb317)`(`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` offset) const` {#classshogun_1_1CDynProg_1a688fb8b85067ee3dc15ef8f209aeb317}

access function for probability of end states

#### Parameters
* `offset` index 0...N-1 

#### Returns
value at offset

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_q_deriv`](#classshogun_1_1CDynProg_1a06c72fa3363a68f3a3f9f016af8b7c3b)`(`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` offset) const` {#classshogun_1_1CDynProg_1a06c72fa3363a68f3a3f9f016af8b7c3b}

access function for derivated probability of end states

#### Parameters
* `offset` index 0...N-1 

#### Returns
value at offset

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_p`](#classshogun_1_1CDynProg_1add631aa92d258b32e8f8aab9727689a0)`(`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` offset) const` {#classshogun_1_1CDynProg_1add631aa92d258b32e8f8aab9727689a0}

access function for probability of initial states

#### Parameters
* `offset` index 0...N-1 

#### Returns
value at offset

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_p_deriv`](#classshogun_1_1CDynProg_1aab4af3184530339318dddc51d25f37ae)`(`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` offset) const` {#classshogun_1_1CDynProg_1aab4af3184530339318dddc51d25f37ae}

access function for derivated probability of initial states

#### Parameters
* `offset` index 0...N-1 

#### Returns
value at offset

#### `public void `[`precompute_content_values`](#classshogun_1_1CDynProg_1a099e5d22e30f58db09cfd8c5ceba877d)`()` {#classshogun_1_1CDynProg_1a099e5d22e30f58db09cfd8c5ceba877d}

create array of precomputed content svm values

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`get_lin_feat`](#classshogun_1_1CDynProg_1a64b22c688a241df26cefcb0f67f47962)`(int32_t & dim1,int32_t & dim2)` {#classshogun_1_1CDynProg_1a64b22c688a241df26cefcb0f67f47962}

return array of precomputed linear features like content predictions and PLiFed tiling array data Jonas

#### Returns
lin_feat_array

#### `public inline void `[`set_lin_feat`](#classshogun_1_1CDynProg_1a237f047cd00c5a743ec58a8668a27888)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * p_lin_feat,int32_t p_num_svms,int32_t p_seq_len)` {#classshogun_1_1CDynProg_1a237f047cd00c5a743ec58a8668a27888}

set your own array of precomputed linear features like content predictions and PLiFed tiling array data Jonas

#### Parameters
* `p_lin_feat` array of features 

* `p_num_svms` number of tracks 

* `p_seq_len` number of candidate positions

#### `public void `[`create_word_string`](#classshogun_1_1CDynProg_1a011a18ce8abe5791cde3c65372ff18bf)`()` {#classshogun_1_1CDynProg_1a011a18ce8abe5791cde3c65372ff18bf}

create word string from char* Jonas

#### `public void `[`precompute_stop_codons`](#classshogun_1_1CDynProg_1a7aef75295ac5b0305f81d6e1c7d84a39)`()` {#classshogun_1_1CDynProg_1a7aef75295ac5b0305f81d6e1c7d84a39}

precompute stop codons

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_a`](#classshogun_1_1CDynProg_1acabe9a67be107baa5e0d215ce8a36aae)`(`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` line_,`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` column) const` {#classshogun_1_1CDynProg_1acabe9a67be107baa5e0d215ce8a36aae}

access function for matrix a

#### Parameters
* `line_` row in matrix 0...N-1 

* `column` column in matrix 0...N-1 

#### Returns
value at position line colum

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_a_deriv`](#classshogun_1_1CDynProg_1a4d41624896af12d754e5deb6171cba33)`(`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` line_,`[`T_STATES`](#namespaceshogun_1a32f3d7d5a01812f43cdadb523aee5c51)` column) const` {#classshogun_1_1CDynProg_1a4d41624896af12d754e5deb6171cba33}

access function for matrix a derivated

#### Parameters
* `line_` row in matrix 0...N-1 

* `column` column in matrix 0...N-1 

#### Returns
value at position line colum

#### `public void `[`set_intron_list`](#classshogun_1_1CDynProg_1a551977c8b8dbd31a90e3e415c202a526)`(`[`CIntronList`](#classshogun_1_1CIntronList)` * intron_list,int32_t num_plifs)` {#classshogun_1_1CDynProg_1a551977c8b8dbd31a90e3e415c202a526}

set intron list

#### Parameters
* `intron_list` 

* `num_plifs` number of intron plifs

#### `public inline `[`CSegmentLoss`](#classshogun_1_1CSegmentLoss)` * `[`get_segment_loss_object`](#classshogun_1_1CDynProg_1a8298508c1b763a6b9619ef67c613073b)`()` {#classshogun_1_1CDynProg_1a8298508c1b763a6b9619ef67c613073b}

get the segment loss object

#### `public inline void `[`long_transition_settings`](#classshogun_1_1CDynProg_1a7356b176bbf8b353ab7089684b775b74)`(bool use_long_transitions,int32_t threshold,int32_t max_len)` {#classshogun_1_1CDynProg_1a7356b176bbf8b353ab7089684b775b74}

settings for long transition handling

#### Parameters
* `use_long_transitions` use the long transition approximation 

* `threshold` use long transition for segments larger than 

* `max_len` allow transitions up to

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

#### `protected int32_t `[`m_num_degrees`](#classshogun_1_1CDynProg_1a367b0ebc41bdcfc8a9be258f87036fc3) {#classshogun_1_1CDynProg_1a367b0ebc41bdcfc8a9be258f87036fc3}

number of degress

#### `protected int32_t `[`m_num_svms`](#classshogun_1_1CDynProg_1a50244e60b5d90658d4423fa892abd9b0) {#classshogun_1_1CDynProg_1a50244e60b5d90658d4423fa892abd9b0}

number of SVMs

#### `protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_word_degree`](#classshogun_1_1CDynProg_1a62e9315c4342d411d9bb366e1fcbc5c6) {#classshogun_1_1CDynProg_1a62e9315c4342d411d9bb366e1fcbc5c6}

word degree

#### `protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_cum_num_words`](#classshogun_1_1CDynProg_1a42dd441c7ad1476157bfaaeeeeaca3b6) {#classshogun_1_1CDynProg_1a42dd441c7ad1476157bfaaeeeeaca3b6}

cum num words

#### `protected int32_t * `[`m_cum_num_words_array`](#classshogun_1_1CDynProg_1a9dc50527b8ca7ecb08bc12858887c9d6) {#classshogun_1_1CDynProg_1a9dc50527b8ca7ecb08bc12858887c9d6}

cum num words array

#### `protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_num_words`](#classshogun_1_1CDynProg_1aa2bcc679f5f98579b309270b07c4262d) {#classshogun_1_1CDynProg_1aa2bcc679f5f98579b309270b07c4262d}

num words

#### `protected int32_t * `[`m_num_words_array`](#classshogun_1_1CDynProg_1acf7bac9fb892e16c499839a0e1ec9326) {#classshogun_1_1CDynProg_1acf7bac9fb892e16c499839a0e1ec9326}

num words array

#### `protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_mod_words`](#classshogun_1_1CDynProg_1a24527c7037ea964092a41808088b29cc) {#classshogun_1_1CDynProg_1a24527c7037ea964092a41808088b29cc}

mod words

#### `protected int32_t * `[`m_mod_words_array`](#classshogun_1_1CDynProg_1adcf533c8d6407536e84bfefac1408148) {#classshogun_1_1CDynProg_1adcf533c8d6407536e84bfefac1408148}

mod words array

#### `protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< bool > `[`m_sign_words`](#classshogun_1_1CDynProg_1a675c7f6b4ee6f7446bd8fe3f4f8f1e74) {#classshogun_1_1CDynProg_1a675c7f6b4ee6f7446bd8fe3f4f8f1e74}

sign words

#### `protected bool * `[`m_sign_words_array`](#classshogun_1_1CDynProg_1a2be26b66e8dea2959b689e741088bc35) {#classshogun_1_1CDynProg_1a2be26b66e8dea2959b689e741088bc35}

sign words array

#### `protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_string_words`](#classshogun_1_1CDynProg_1ab9e535d23bdc4b44cdf12c39ba9cd4a3) {#classshogun_1_1CDynProg_1ab9e535d23bdc4b44cdf12c39ba9cd4a3}

string words

#### `protected int32_t * `[`m_string_words_array`](#classshogun_1_1CDynProg_1a6c916933ce4ea3d27c579a093342e712) {#classshogun_1_1CDynProg_1a6c916933ce4ea3d27c579a093342e712}

string words array

#### `protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_num_unique_words`](#classshogun_1_1CDynProg_1aaba8e39cbb0184f1ed709959bda6210e) {#classshogun_1_1CDynProg_1aaba8e39cbb0184f1ed709959bda6210e}

SVM start position number of unique words

#### `protected bool `[`m_svm_arrays_clean`](#classshogun_1_1CDynProg_1aabaa85d02040381fae30bc97cc3fbf10) {#classshogun_1_1CDynProg_1aabaa85d02040381fae30bc97cc3fbf10}

SVM arrays clean

#### `protected int32_t `[`m_max_a_id`](#classshogun_1_1CDynProg_1aeeceb871f482672408039dba4e48b760) {#classshogun_1_1CDynProg_1aeeceb871f482672408039dba4e48b760}

max a id

#### `protected `[`CDynamicArray](#classshogun_1_1CDynamicArray)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_observation_matrix`](#classshogun_1_1CDynProg_1ad0d75e543a7b1fcf2984625df2d5181f) {#classshogun_1_1CDynProg_1ad0d75e543a7b1fcf2984625df2d5181f}

sequence

#### `protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_pos`](#classshogun_1_1CDynProg_1a9303766db162c41b3573f85832229278) {#classshogun_1_1CDynProg_1a9303766db162c41b3573f85832229278}

candidate position

#### `protected int32_t `[`m_seq_len`](#classshogun_1_1CDynProg_1a3a504e9ee5462ccac4717b1682ce65ad) {#classshogun_1_1CDynProg_1a3a504e9ee5462ccac4717b1682ce65ad}

number of candidate positions

#### `protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_orf_info`](#classshogun_1_1CDynProg_1a22d106b703a54a47d1fcd0b681b93c70) {#classshogun_1_1CDynProg_1a22d106b703a54a47d1fcd0b681b93c70}

orf info

#### `protected `[`CDynamicArray](#classshogun_1_1CDynamicArray)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_segment_sum_weights`](#classshogun_1_1CDynProg_1a87f291f21d8e277475bcf85cfca4ff76) {#classshogun_1_1CDynProg_1a87f291f21d8e277475bcf85cfca4ff76}

segment sum weights

#### `protected `[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` `[`m_plif_list`](#classshogun_1_1CDynProg_1a4331f8f0b261cefe9eac0b1c38997151) {#classshogun_1_1CDynProg_1a4331f8f0b261cefe9eac0b1c38997151}

Plif list

#### `protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< char > `[`m_genestr`](#classshogun_1_1CDynProg_1ad8899de40c111310d21afd3a3613ee9c) {#classshogun_1_1CDynProg_1ad8899de40c111310d21afd3a3613ee9c}

a single string (to be segmented)

#### `protected uint16_t *** `[`m_wordstr`](#classshogun_1_1CDynProg_1a03e704ba5e57f4033389dd8a3c043295) {#classshogun_1_1CDynProg_1a03e704ba5e57f4033389dd8a3c043295}

wordstr is a vector of L n-gram indices, with wordstr(i) representing a number betweeen 0 and 4095 corresponding to the 6-mer in genestr(i-5:i) pos is a vector of candidate transition positions (it is input to compute_nbest_paths) t_end is some index in pos

svs has been initialized by init_svm_values

At the end of this procedure, svs.svm_values[i+s*svs.seqlen] has the value of the s-th SVM on genestr(pos(t_end-i):pos(t_end)) for every i satisfying pos(t_end)-pos(t_end-i) <= svs.maxlookback

The SVM weights are precomputed in m_dict_weights

#### `protected `[`CDynamicArray](#classshogun_1_1CDynamicArray)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_dict_weights`](#classshogun_1_1CDynProg_1af21b4733c6b7bf88534949afd53d1e85) {#classshogun_1_1CDynProg_1af21b4733c6b7bf88534949afd53d1e85}

dict weights

#### `protected `[`CDynamicArray](#classshogun_1_1CDynamicArray)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_segment_loss`](#classshogun_1_1CDynProg_1ab061fa7fdcbb512ccda6701e1eba81b9) {#classshogun_1_1CDynProg_1ab061fa7fdcbb512ccda6701e1eba81b9}

segment loss

#### `protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_segment_ids`](#classshogun_1_1CDynProg_1a3329906a7f3c8e1a0709df1a9c7de4d4) {#classshogun_1_1CDynProg_1a3329906a7f3c8e1a0709df1a9c7de4d4}

segment IDs

#### `protected `[`CDynamicArray](#classshogun_1_1CDynamicArray)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_segment_mask`](#classshogun_1_1CDynProg_1af147f4cfc62f621e3e7474fbf21c4a22) {#classshogun_1_1CDynProg_1af147f4cfc62f621e3e7474fbf21c4a22}

segment mask

#### `protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_my_state_seq`](#classshogun_1_1CDynProg_1ab0904df5d08c97ffcaadaf0d374cb852) {#classshogun_1_1CDynProg_1ab0904df5d08c97ffcaadaf0d374cb852}

my state seq

#### `protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_my_pos_seq`](#classshogun_1_1CDynProg_1a6c01bf48cc81476cbad9f92b3c9f6021) {#classshogun_1_1CDynProg_1a6c01bf48cc81476cbad9f92b3c9f6021}

my position sequence

#### `protected `[`CDynamicArray](#classshogun_1_1CDynamicArray)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_my_scores`](#classshogun_1_1CDynProg_1a6793fa5a9df2af73391b75c2d2ccfb6b) {#classshogun_1_1CDynProg_1a6793fa5a9df2af73391b75c2d2ccfb6b}

my scores

#### `protected `[`CDynamicArray](#classshogun_1_1CDynamicArray)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_my_losses`](#classshogun_1_1CDynProg_1a05a84d743b1c3e1ddbcd299940ccb246) {#classshogun_1_1CDynProg_1a05a84d743b1c3e1ddbcd299940ccb246}

my losses

#### `protected `[`CSegmentLoss`](#classshogun_1_1CSegmentLoss)` * `[`m_seg_loss_obj`](#classshogun_1_1CDynProg_1ad2c830d06ae332c2f0255d3f3b55dd86) {#classshogun_1_1CDynProg_1ad2c830d06ae332c2f0255d3f3b55dd86}

segment loss object containing the functions to compute the segment loss

#### `protected `[`CDynamicArray](#classshogun_1_1CDynamicArray)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_scores`](#classshogun_1_1CDynProg_1ac51bd058c3378f1cfcce53d189f9ab58) {#classshogun_1_1CDynProg_1ac51bd058c3378f1cfcce53d189f9ab58}

scores

#### `protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_states`](#classshogun_1_1CDynProg_1a0ba92d1590484e1df2780ce629c4b9fe) {#classshogun_1_1CDynProg_1a0ba92d1590484e1df2780ce629c4b9fe}

states

#### `protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > `[`m_positions`](#classshogun_1_1CDynProg_1ab1d87fe86af2d2c8ba0f2bd808cd57e7) {#classshogun_1_1CDynProg_1ab1d87fe86af2d2c8ba0f2bd808cd57e7}

positions

#### `protected `[`CSparseFeatures](#classshogun_1_1CSparseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * `[`m_seq_sparse1`](#classshogun_1_1CDynProg_1a9ec2dc54953bddd398dcda7f3feb7721) {#classshogun_1_1CDynProg_1a9ec2dc54953bddd398dcda7f3feb7721}

sparse feature matrix dim1

#### `protected `[`CSparseFeatures](#classshogun_1_1CSparseFeatures)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * `[`m_seq_sparse2`](#classshogun_1_1CDynProg_1ab753e47a12e65582a01f8ff80293baa0) {#classshogun_1_1CDynProg_1ab753e47a12e65582a01f8ff80293baa0}

sparse feature matrix dim2

#### `protected `[`CPlifMatrix`](#classshogun_1_1CPlifMatrix)` * `[`m_plif_matrices`](#classshogun_1_1CDynProg_1a6ff8af3c85978d51a9cb8626cd92524b) {#classshogun_1_1CDynProg_1a6ff8af3c85978d51a9cb8626cd92524b}

plif matrices

#### `protected `[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< bool > `[`m_genestr_stop`](#classshogun_1_1CDynProg_1a53ffdfa661170471c75a2798efa0b331) {#classshogun_1_1CDynProg_1a53ffdfa661170471c75a2798efa0b331}

storeage of stop codons array of size length(sequence)

#### `protected `[`CIntronList`](#classshogun_1_1CIntronList)` * `[`m_intron_list`](#classshogun_1_1CDynProg_1a49df13b1237518586a93829cf3d08f63) {#classshogun_1_1CDynProg_1a49df13b1237518586a93829cf3d08f63}

administers a list of introns and quality scores and provides functions for fast access

#### `protected int32_t `[`m_num_intron_plifs`](#classshogun_1_1CDynProg_1ad112775259a716bb5f46f72011ea3654) {#classshogun_1_1CDynProg_1ad112775259a716bb5f46f72011ea3654}

number of intron features and plifs

#### `protected `[`CDynamicArray](#classshogun_1_1CDynamicArray)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_lin_feat`](#classshogun_1_1CDynProg_1aa776be3db62d3d55dfa05d33dd04adea) {#classshogun_1_1CDynProg_1aa776be3db62d3d55dfa05d33dd04adea}

array for storage of precomputed linear features linge content svm values or pliffed tiling data Jonas

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`m_raw_intensities`](#classshogun_1_1CDynProg_1a19536d9c21632e852917879d646e9300) {#classshogun_1_1CDynProg_1a19536d9c21632e852917879d646e9300}

raw intensities

#### `protected int32_t * `[`m_probe_pos`](#classshogun_1_1CDynProg_1ad592a2d93aa39ad322ed0002ca229d63) {#classshogun_1_1CDynProg_1ad592a2d93aa39ad322ed0002ca229d63}

probe position

#### `protected int32_t * `[`m_num_probes_cum`](#classshogun_1_1CDynProg_1a11a3f37656d6e8ec2c11665572cc8f82) {#classshogun_1_1CDynProg_1a11a3f37656d6e8ec2c11665572cc8f82}

number of probes

#### `protected int32_t * `[`m_num_lin_feat_plifs_cum`](#classshogun_1_1CDynProg_1ac671de8dc0c1a228d6971f68459dcc7d) {#classshogun_1_1CDynProg_1ac671de8dc0c1a228d6971f68459dcc7d}

num lin feat plifs cum

#### `protected int32_t `[`m_num_raw_data`](#classshogun_1_1CDynProg_1aca9d758f6c39ee7848df23bd8cbf13e2) {#classshogun_1_1CDynProg_1aca9d758f6c39ee7848df23bd8cbf13e2}

number of additional data tracks like tiling, RNA-Seq, ...

#### `protected bool `[`m_long_transitions`](#classshogun_1_1CDynProg_1a467e20b2b645981955301b80f8d55d76) {#classshogun_1_1CDynProg_1a467e20b2b645981955301b80f8d55d76}

use long transition approximation

#### `protected int32_t `[`m_long_transition_threshold`](#classshogun_1_1CDynProg_1ae2b1e846dfe744c0f362a2c6976afb24) {#classshogun_1_1CDynProg_1ae2b1e846dfe744c0f362a2c6976afb24}

threshold for transitions that are computed the traditional way

#### `protected void `[`lookup_content_svm_values`](#classshogun_1_1CDynProg_1a15bf99ea5b26093da2bbb6917bdd23d5)`(const int32_t from_state,const int32_t to_state,const int32_t from_pos,const int32_t to_pos,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * svm_values,int32_t frame)` {#classshogun_1_1CDynProg_1a15bf99ea5b26093da2bbb6917bdd23d5}

lookup content SVM values

#### Parameters
* `from_state` from state 

* `to_state` to state 

* `from_pos` from position 

* `to_pos` to position 

* `svm_values` SVM values 

* `frame` frame

#### `protected inline void `[`lookup_tiling_plif_values`](#classshogun_1_1CDynProg_1a97d3c27407c59dcab30c4c8283427bb4)`(const int32_t from_state,const int32_t to_state,const int32_t len,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * svm_values)` {#classshogun_1_1CDynProg_1a97d3c27407c59dcab30c4c8283427bb4}

lookup tiling Plif values

#### Parameters
* `from_state` from state 

* `to_state` to state 

* `len` length 

* `svm_values` SVM values

#### `protected inline int32_t `[`find_frame`](#classshogun_1_1CDynProg_1a9a2af9e788d0bdbb065b1a25ec265861)`(const int32_t from_state)` {#classshogun_1_1CDynProg_1a9a2af9e788d0bdbb065b1a25ec265861}

find frame

#### Parameters
* `from_state` from state

#### `protected inline int32_t `[`raw_intensities_interval_query`](#classshogun_1_1CDynProg_1a9bc3f4e512122eff1fa8930e141d26f8)`(const int32_t from_pos,const int32_t to_pos,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * intensities,int32_t type)` {#classshogun_1_1CDynProg_1a9bc3f4e512122eff1fa8930e141d26f8}

raw intensities interval query

#### Parameters
* `from_pos` from position 

* `to_pos` to position 

* `intensities` intensities 

* `type` type 

#### Returns
an integer

#### `protected bool `[`extend_orf`](#classshogun_1_1CDynProg_1a9dfb12f3fac92fe77a8bed03e579d4db)`(int32_t orf_from,int32_t orf_to,int32_t start,int32_t & last_pos,int32_t to)` {#classshogun_1_1CDynProg_1a9dfb12f3fac92fe77a8bed03e579d4db}

extend orf

#### Parameters
* `orf_from` orf from 

* `orf_to` orf to 

* `start` start 

* `last_pos` last position 

* `to` to

#### `protected inline virtual const char * `[`get_name`](#classshogun_1_1CDynProg_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` {#classshogun_1_1CDynProg_1a9cb485686dd7a1e6f7103cf42e87717e}

#### Returns
object name

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

