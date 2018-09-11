---
classname: "shogun::CSVMLightOneClass"
type: "class"
parents:
   - CSVMLight
---

# class `shogun::CSVMLightOneClass` {#classshogun_1_1CSVMLightOneClass}

```
class shogun::CSVMLightOneClass
  : public CSVMLight
```

Trains a one class C SVM.

**See also**: [CSVMLight](#classshogun_1_1CSVMLight)

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
`public  `[`CSVMLightOneClass`](#classshogun_1_1CSVMLightOneClass_1a8235f7ee88030d8bfe2e3a470f4d4ffc)`()` | default constructor
`public  `[`CSVMLightOneClass`](#classshogun_1_1CSVMLightOneClass_1a9a3c855e029a73a65e1dcabd71333220)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` C,`[`CKernel`](#classshogun_1_1CKernel)` * k)` | constructor
`public inline virtual  `[`~CSVMLightOneClass`](#classshogun_1_1CSVMLightOneClass_1a898462dc9b300e6268f3f112d498567b)`()` | default destructor
`public inline virtual `[`EMachineType`](#namespaceshogun_1af181c832c12de7a0c3b02425986106cc)` `[`get_classifier_type`](#classshogun_1_1CSVMLightOneClass_1ab0ee71eb4f9097a9b7ad2b72b1b310e2)`()` | get classifier type
`public inline virtual const char * `[`get_name`](#classshogun_1_1CSVMLightOneClass_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` | Returns the name of the SGSerializable instance.
`public void `[`init`](#classshogun_1_1CSVMLight_1a02fd73d861ef2e4aabb38c0c9ff82947)`()` | init SVM
`public int32_t `[`get_runtime`](#classshogun_1_1CSVMLight_1aaf29fe72c2d687fdcc80ce708321402b)`()` | get runtime
`public void `[`svm_learn`](#classshogun_1_1CSVMLight_1acea249bf2f6f52768fc262fa24287934)`()` | learn SVM
`public int32_t `[`optimize_to_convergence`](#classshogun_1_1CSVMLight_1ac8cca3fe94a16b80eec1a9c8b8d00ee2)`(int32_t * docs,int32_t * label,int32_t totdoc,SHRINK_STATE * shrink_state,int32_t * inconsistent,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c,TIMING * timing_profile,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * maxdiff,int32_t heldout,int32_t retrain)` | optimize to convergence
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_objective_function`](#classshogun_1_1CSVMLight_1a95f392856e00f734793d57e624aae909)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * eps,int32_t * label,int32_t totdoc)` | compute objective function
`public void `[`clear_index`](#classshogun_1_1CSVMLight_1a9be0210d565679fbf22cb1f39129f51f)`(int32_t * index)` | clear index
`public void `[`add_to_index`](#classshogun_1_1CSVMLight_1ac00a77524973a39bf43a6ee1e06fc5b5)`(int32_t * index,int32_t elem)` | add to index
`public int32_t `[`compute_index`](#classshogun_1_1CSVMLight_1aacccc36ee508359a9ebc4c5e3764c682)`(int32_t * binfeature,int32_t range,int32_t * index)` | compute index
`public void `[`optimize_svm`](#classshogun_1_1CSVMLight_1a285ed34ec9a3667ec7926e101d0ce288)`(int32_t * docs,int32_t * label,int32_t * exclude_from_eq_const,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` eq_target,int32_t * chosen,int32_t * active2dnum,int32_t totdoc,int32_t * working2dnum,int32_t varnum,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * aicache,QP * qp,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * epsilon_crit_target)` | optimise SVM
`public void `[`compute_matrices_for_optimization`](#classshogun_1_1CSVMLight_1ade2f276226b2988e2b0b28499c656bbb)`(int32_t * docs,int32_t * label,int32_t * exclude_from_eq_const,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` eq_target,int32_t * chosen,int32_t * active2dnum,int32_t * key,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c,int32_t varnum,int32_t totdoc,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * aicache,QP * qp)` | compute matrices for optimization
`public void `[`compute_matrices_for_optimization_parallel`](#classshogun_1_1CSVMLight_1adf0e72fca21597df8081f09cf156299f)`(int32_t * docs,int32_t * label,int32_t * exclude_from_eq_const,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` eq_target,int32_t * chosen,int32_t * active2dnum,int32_t * key,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c,int32_t varnum,int32_t totdoc,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * aicache,QP * qp)` | compute matrices for optimization in parallel
`public int32_t `[`calculate_svm_model`](#classshogun_1_1CSVMLight_1a18b639ced2d4fcef76b8105031a59e0e)`(int32_t * docs,int32_t * label,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a_old,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c,int32_t * working2dnum,int32_t * active2dnum)` | calculate SVM model
`public int32_t `[`check_optimality`](#classshogun_1_1CSVMLight_1ab0064451b453e29725e053ec1b73cc0c)`(int32_t * label,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c,int32_t totdoc,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * maxdiff,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` epsilon_crit_org,int32_t * misclassified,int32_t * inconsistent,int32_t * active2dnum,int32_t * last_suboptimal_at,int32_t iteration)` | check optimality
`public virtual void `[`update_linear_component`](#classshogun_1_1CSVMLight_1acdba7d487d944c975f64dbf3b753a836)`(int32_t * docs,int32_t * label,int32_t * active2dnum,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a_old,int32_t * working2dnum,int32_t totdoc,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * aicache,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c)` | update linear component
`public void `[`update_linear_component_mkl`](#classshogun_1_1CSVMLight_1ac10ac0f2e6835df436ffcfff2aac156b)`(int32_t * docs,int32_t * label,int32_t * active2dnum,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a_old,int32_t * working2dnum,int32_t totdoc,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * aicache)` | update linear component MKL
`public void `[`update_linear_component_mkl_linadd`](#classshogun_1_1CSVMLight_1aad8b1708b6543ca04191adf7bf07b578)`(int32_t * docs,int32_t * label,int32_t * active2dnum,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a_old,int32_t * working2dnum,int32_t totdoc,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * aicache)` | update linear component MKL
`public void `[`call_mkl_callback`](#classshogun_1_1CSVMLight_1a6d39c21fa2d09a8436508d7014f4cb82)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,int32_t * label,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin)` | 
`public int32_t `[`select_next_qp_subproblem_grad`](#classshogun_1_1CSVMLight_1ae17f95034c5a1c9d881a221176bf6eba)`(int32_t * label,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c,int32_t totdoc,int32_t qp_size,int32_t * inconsistent,int32_t * active2dnum,int32_t * working2dnum,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * selcrit,int32_t * select,int32_t cache_only,int32_t * key,int32_t * chosen)` | select next qp subproblem grad
`public int32_t `[`select_next_qp_subproblem_rand`](#classshogun_1_1CSVMLight_1a4f837dbfa802997c6c3588aedab369d0)`(int32_t * label,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c,int32_t totdoc,int32_t qp_size,int32_t * inconsistent,int32_t * active2dnum,int32_t * working2dnum,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * selcrit,int32_t * select,int32_t * key,int32_t * chosen,int32_t iteration)` | select next qp subproblem rand
`public void `[`select_top_n`](#classshogun_1_1CSVMLight_1abbbd32699279e7b8693c6e1c79e56418)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * selcrit,int32_t range,int32_t * select,int32_t n)` | select top n
`public void `[`init_shrink_state`](#classshogun_1_1CSVMLight_1abb11f6e852cfd459a68828be6689722a)`(SHRINK_STATE * shrink_state,int32_t totdoc,int32_t maxhistory)` | init shrink state
`public void `[`shrink_state_cleanup`](#classshogun_1_1CSVMLight_1aefc3e1093bcb90cc4288079965a46152)`(SHRINK_STATE * shrink_state)` | cleanup shrink state
`public int32_t `[`shrink_problem`](#classshogun_1_1CSVMLight_1a83fc7f196280febc0972f07e3bc37100)`(SHRINK_STATE * shrink_state,int32_t * active2dnum,int32_t * last_suboptimal_at,int32_t iteration,int32_t totdoc,int32_t minshrink,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,int32_t * inconsistent,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,int * label)` | shrink problem
`public virtual void `[`reactivate_inactive_examples`](#classshogun_1_1CSVMLight_1a9bb83012b8d9abd60f2ca0cca569cc7c)`(int32_t * label,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,SHRINK_STATE * shrink_state,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c,int32_t totdoc,int32_t iteration,int32_t * inconsistent,int32_t * docs,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * aicache,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * maxdiff)` | reactivate inactive examples
`public  `[`MACHINE_PROBLEM_TYPE`](#classshogun_1_1CSVM_1aa2d22990d22f93916c7b9675db96f0ea)`(`[`PT_BINARY`](#namespaceshogun_1a0aa89aa872f89f6a174de2f45b7596d4a17ea40d0e25bb381c98ce350e05a66a6)`)` | problem type
`public void `[`set_defaults`](#classshogun_1_1CSVM_1a682c4f9e58f769d5c1f052cd3ff83598)`(int32_t num_sv)` | set default values for members a SVM object
`public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_linear_term`](#classshogun_1_1CSVM_1a1fbcfd825ea31d6c8cf1434fcc39a050)`()` | get linear term
`public virtual void `[`set_linear_term`](#classshogun_1_1CSVM_1a7db3d5c0ba0feac2d70a06e42b5d3ac4)`(const `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > linear_term)` | set linear term of the QP
`public bool `[`load`](#classshogun_1_1CSVM_1a5330d46603b0a4d7b269341db92ad3a3)`(FILE * svm_file)` | load a SVM from file 
`public bool `[`save`](#classshogun_1_1CSVM_1a57adfb729db48725e1c9a30b52eae9a2)`(FILE * svm_file)` | write a SVM to a file 
`public inline void `[`set_nu`](#classshogun_1_1CSVM_1a95e04a495bfc9124526506b427b0fe53)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` nue)` | set nu
`public inline void `[`set_C`](#classshogun_1_1CSVM_1a272a6477be80601077c22e17a530a460)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` c_neg,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` c_pos)` | set C
`public inline void `[`set_epsilon`](#classshogun_1_1CSVM_1ae3931ee9091f751d7584919fb92dde53)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` eps)` | set epsilon
`public inline void `[`set_tube_epsilon`](#classshogun_1_1CSVM_1ad04af32292a7ea673ee2f4b935a68e2c)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` eps)` | set tube epsilon
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_tube_epsilon`](#classshogun_1_1CSVM_1a4aa0557a5bcf6c27002f90b7ac1ea6c1)`()` | get tube epsilon
`public inline void `[`set_qpsize`](#classshogun_1_1CSVM_1a98c5fb91618fdc01a929ee41bff73f7d)`(int32_t qps)` | set qpsize
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_epsilon`](#classshogun_1_1CSVM_1acc649b6e3439428fe014ae45f8db19b0)`()` | get epsilon
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_nu`](#classshogun_1_1CSVM_1af4a7fa8cd6386c1b7a26a67ca062c855)`()` | get nu
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_C1`](#classshogun_1_1CSVM_1a106ca4c7bad3e1779f80eae35c203144)`()` | get C1
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_C2`](#classshogun_1_1CSVM_1a48b19829cbf87b2f540aa68db4ed50fa)`()` | get C2
`public inline int32_t `[`get_qpsize`](#classshogun_1_1CSVM_1a6fd9f6edc2dd733f04ee069bebf653d3)`()` | get qpsize
`public inline void `[`set_shrinking_enabled`](#classshogun_1_1CSVM_1acd0ce5d50e27f8240c843777bfb6b033)`(bool enable)` | set state of shrinking
`public inline bool `[`get_shrinking_enabled`](#classshogun_1_1CSVM_1a5552ede75927d45cbb0165c676ac3045)`()` | get state of shrinking
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_svm_dual_objective`](#classshogun_1_1CSVM_1a5b7f2bbc1d700ef7572ab1018cd2d57d)`()` | compute svm dual objective
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_svm_primal_objective`](#classshogun_1_1CSVM_1a92d7b51b534a0bc4c20afe7983ce1d53)`()` | compute svm primal objective
`public inline void `[`set_objective`](#classshogun_1_1CSVM_1a259ad42da9e35f1416836cd1d48a5aac)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` v)` | set objective
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_objective`](#classshogun_1_1CSVM_1a35324625863981d4196336d7e7443f06)`()` | get objective
`public inline bool `[`get_loaded_status`](#classshogun_1_1CSVM_1a68bd318899d05b99e815913f852e2316)`()` | check if svm been loaded
`public inline void `[`set_loaded_status`](#classshogun_1_1CSVM_1a12cc58040ecd868bfe0e90836477c4f1)`(bool loaded)` | set svm loaded status
`public void `[`set_callback_function`](#classshogun_1_1CSVM_1aa7077ff11811d1a54e61c16f7ea4c8e4)`(`[`CMKL`](#classshogun_1_1CMKL)` * m,bool(*)(`[`CMKL](#classshogun_1_1CMKL) *[mkl](#classshogun_1_1CSVM_1a061a27bdcf1516056edc1d229e80f140), const [float64_t](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4) *sumw, const [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4) suma)` cb)` | set callback function svm optimizers may call when they have a new (small) set of alphas
`public void `[`set_kernel`](#classshogun_1_1CKernelMachine_1aecb33756a13e8e25ee610fce65f48b99)`(`[`CKernel`](#classshogun_1_1CKernel)` * k)` | set kernel
`public `[`CKernel`](#classshogun_1_1CKernel)` * `[`get_kernel`](#classshogun_1_1CKernelMachine_1ab0da30c8a056a80cf85a9ea3638348d0)`()` | get kernel
`public void `[`set_batch_computation_enabled`](#classshogun_1_1CKernelMachine_1a6c10d5b31beb22429fee7a17c4622c78)`(bool enable)` | set batch computation enabled
`public bool `[`get_batch_computation_enabled`](#classshogun_1_1CKernelMachine_1a3f68567b2b10d2ebfa7883da74c02285)`()` | check if batch computation is enabled
`public void `[`set_linadd_enabled`](#classshogun_1_1CKernelMachine_1ac68e75ba55a0286baab70d6a7de84f73)`(bool enable)` | set linadd enabled
`public bool `[`get_linadd_enabled`](#classshogun_1_1CKernelMachine_1ae11f2c49e6b3ab6fcef5975c893e669b)`()` | check if linadd is enabled
`public void `[`set_bias_enabled`](#classshogun_1_1CKernelMachine_1a5b773e2eeec54d607c1add0864a701ab)`(bool enable_bias)` | set state of bias
`public bool `[`get_bias_enabled`](#classshogun_1_1CKernelMachine_1a24209179a0e8592371857af993da1c51)`()` | get state of bias
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_bias`](#classshogun_1_1CKernelMachine_1a3abce3a0d07fad71b9acd49de0d00148)`()` | get bias
`public void `[`set_bias`](#classshogun_1_1CKernelMachine_1a3e9f04b92a597096bcf3e10d472675d4)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` bias)` | set bias to given value
`public int32_t `[`get_support_vector`](#classshogun_1_1CKernelMachine_1acd4c009f894cc6df93812f75a3e69cfc)`(int32_t idx)` | get support vector at given index
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_alpha`](#classshogun_1_1CKernelMachine_1ae0b6d34f42abd02ec4f0d830963a6608)`(int32_t idx)` | get alpha at given index
`public bool `[`set_support_vector`](#classshogun_1_1CKernelMachine_1af3b3665310b7ebff97e268276dd790be)`(int32_t idx,int32_t val)` | set support vector at given index to given value
`public bool `[`set_alpha`](#classshogun_1_1CKernelMachine_1a5f93d1140f943f9a616712d1986d4926)`(int32_t idx,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` val)` | set alpha at given index to given value
`public int32_t `[`get_num_support_vectors`](#classshogun_1_1CKernelMachine_1ae0d36162db143622aecc5fe721ed8b14)`()` | get number of support vectors
`public void `[`set_alphas`](#classshogun_1_1CKernelMachine_1a560c1a5b57e2ca1ed5ba4aaa4334755f)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > alphas)` | set alphas to given values
`public void `[`set_support_vectors`](#classshogun_1_1CKernelMachine_1a2d82aa7e06239e34781ae33a3522f023)`(`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > svs)` | set support vectors to given values
`public `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`get_support_vectors`](#classshogun_1_1CKernelMachine_1ac04d4c9009462250851fdf99ce5255a0)`()` | #### Returns
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_alphas`](#classshogun_1_1CKernelMachine_1a3c649a2215667a363360536155e263b8)`()` | #### Returns
`public bool `[`create_new_model`](#classshogun_1_1CKernelMachine_1a9fa06e8c87b376a4ce8a667bda094b5c)`(int32_t num)` | create new model
`public bool `[`init_kernel_optimization`](#classshogun_1_1CKernelMachine_1ab60ed83e44c460fdac82ec0dfe839590)`()` | initialise kernel optimisation
`public virtual `[`CRegressionLabels`](#classshogun_1_1CRegressionLabels)` * `[`apply_regression`](#classshogun_1_1CKernelMachine_1aaeea92e0e4795e7f63f067c16f162302)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply kernel machine to data for regression task
`public virtual `[`CBinaryLabels`](#classshogun_1_1CBinaryLabels)` * `[`apply_binary`](#classshogun_1_1CKernelMachine_1a16a7dee83bb61aedc93792df578d4a77)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply kernel machine to data for binary classification task
`public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`apply_one`](#classshogun_1_1CKernelMachine_1a541d70682e317105112ba75d3d03624a)`(int32_t num)` | apply kernel machine to one example
`public virtual bool `[`train_locked`](#classshogun_1_1CKernelMachine_1a5a69e66a9ea3f503dfbf7bc2d332d1b1)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | This precomputes the kernel matrix and stores it
`public virtual bool `[`train_locked`](#classshogun_1_1CMachine_1aab4927bdae8da7f0c85efdfce22c86c2)`()` | Trains a locked machine on a set of indices. Error if machine is not locked 
`public virtual `[`CBinaryLabels`](#classshogun_1_1CBinaryLabels)` * `[`apply_locked_binary`](#classshogun_1_1CKernelMachine_1ac417f13423c17ebd9b0aa742f5e78c4c)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | Applies a locked machine on a set of indices. Error if machine is not locked. Binary case
`public virtual `[`CRegressionLabels`](#classshogun_1_1CRegressionLabels)` * `[`apply_locked_regression`](#classshogun_1_1CKernelMachine_1a764464fca138ac17692cb994824a1d93)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | Applies a locked machine on a set of indices. Error if machine is not locked. Binary case
`public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`apply_locked_get_output`](#classshogun_1_1CKernelMachine_1aa9db3cc5c76f3670c3726d03d49a2182)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | Applies a locked machine on a set of indices. Error if machine is not locked
`public virtual void `[`data_lock`](#classshogun_1_1CKernelMachine_1a420e18489602624aa97bf980b87491fc)`(`[`CLabels`](#classshogun_1_1CLabels)` * labs,`[`CFeatures`](#classshogun_1_1CFeatures)` * features)` | Locks the machine on given labels and data. After this call, only train_locked and apply_locked may be called.
`public virtual void `[`data_unlock`](#classshogun_1_1CKernelMachine_1a72933e4edad4e2daabeeafd9f1069e47)`()` | Unlocks a locked machine and restores previous state
`public virtual bool `[`supports_locking`](#classshogun_1_1CKernelMachine_1a9c45ac77f2e73467cd9e566d69dea83d)`() const` | #### Returns
`public virtual bool `[`train`](#classshogun_1_1CMachine_1aa0ece9fd14892c6dfed1bb8c78f3b3ed)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | train machine
`public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`apply`](#classshogun_1_1CMachine_1afd5d402257972c78456594234d13eb4c)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data if data is not specified apply to the current features
`public virtual `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * `[`apply_multiclass`](#classshogun_1_1CMachine_1a250aa566fff0edb31433db98f70a7f15)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data in means of multiclass classification problem
`public virtual `[`CStructuredLabels`](#classshogun_1_1CStructuredLabels)` * `[`apply_structured`](#classshogun_1_1CMachine_1a588efa92a0696e1d2a61a8cd21d8ebee)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data in means of SO classification problem
`public virtual `[`CLatentLabels`](#classshogun_1_1CLatentLabels)` * `[`apply_latent`](#classshogun_1_1CMachine_1a276d23b37202ecb31367df26a5600cf7)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply machine to data in means of latent problem
`public virtual void `[`set_labels`](#classshogun_1_1CMachine_1a5f0cfd09e37bd5e793cacecb8d3c818b)`(`[`CLabels`](#classshogun_1_1CLabels)` * lab)` | set labels
`public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`get_labels`](#classshogun_1_1CMachine_1a065f0797777044cb0dbf786781982e3d)`()` | get labels
`public void `[`set_max_train_time`](#classshogun_1_1CMachine_1af660b1b03c475c3c638d2c995ea4b54a)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` t)` | set maximum training time
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_max_train_time`](#classshogun_1_1CMachine_1a7c75c86ff1cfd61d8275e62f0477d797)`()` | get maximum training time
`public void `[`set_solver_type`](#classshogun_1_1CMachine_1af8876022111114d5d3b0579ee161a8ff)`(`[`ESolverType`](#namespaceshogun_1af43428a9cb6c6de54cc7085c7c9b273e)` st)` | set solver type
`public `[`ESolverType`](#namespaceshogun_1af43428a9cb6c6de54cc7085c7c9b273e)` `[`get_solver_type`](#classshogun_1_1CMachine_1a97ee8b11465427d28498437279229ebe)`()` | get solver type
`public virtual void `[`set_store_model_features`](#classshogun_1_1CMachine_1a872d1cc0904edaa3c5701b049ee2993d)`(bool store_model)` | Setter for store-model-features-after-training flag
`public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`apply_locked`](#classshogun_1_1CMachine_1add0cb383e34472fdc66db18b0a5a4bc5)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | Applies a locked machine on a set of indices. Error if machine is not locked
`public virtual `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * `[`apply_locked_multiclass`](#classshogun_1_1CMachine_1a9a97b605764f96da5aaadda76a05d21d)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | applies a locked machine on a set of indices for multiclass problems
`public virtual `[`CStructuredLabels`](#classshogun_1_1CStructuredLabels)` * `[`apply_locked_structured`](#classshogun_1_1CMachine_1a8c63b6efbfe361a91794937f6fda544c)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | applies a locked machine on a set of indices for structured problems
`public virtual `[`CLatentLabels`](#classshogun_1_1CLatentLabels)` * `[`apply_locked_latent`](#classshogun_1_1CMachine_1ab4e951edb0bafda3d57fe80d648190d6)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | applies a locked machine on a set of indices for latent problems
`public inline virtual void `[`post_lock`](#classshogun_1_1CMachine_1a0ad27205b36008a86beb4da016ceef0d)`(`[`CLabels`](#classshogun_1_1CLabels)` * labs,`[`CFeatures`](#classshogun_1_1CFeatures)` * features)` | post lock
`public inline bool `[`is_data_locked`](#classshogun_1_1CMachine_1a2996bc9c87fd16414792bca4aa0a14ec)`() const` | #### Returns
`public inline virtual `[`EProblemType`](#namespaceshogun_1a0aa89aa872f89f6a174de2f45b7596d4)` `[`get_machine_problem_type`](#classshogun_1_1CMachine_1ac1c69755f623188143fc30188354a039)`() const` | returns type of problem machine solves
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
`protected MODEL * `[`model`](#classshogun_1_1CSVMLight_1a05b8d68085a6371c3f02933a2a007866) | model
`protected LEARN_PARM * `[`learn_parm`](#classshogun_1_1CSVMLight_1ade6f4b01f7240261e6299d741fd702c8) | learn parameters
`protected int32_t `[`verbosity`](#classshogun_1_1CSVMLight_1ae58239b03e562b412748d74dece0fcc8) | verbosity level (0-4)
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`init_margin`](#classshogun_1_1CSVMLight_1a807c081a57e3894502d85014ee1e1805) | init margin
`protected int32_t `[`init_iter`](#classshogun_1_1CSVMLight_1a2a2398dd614018ed5c642739b713b882) | init iter
`protected int32_t `[`precision_violations`](#classshogun_1_1CSVMLight_1a12425692bd8c9dd71dd13b938494bf32) | precision violations
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`model_b`](#classshogun_1_1CSVMLight_1a8b520a07895ec66cef773797f613d365) | model b
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`opt_precision`](#classshogun_1_1CSVMLight_1a7a7eb2bf99e42732382c627140362f99) | opt precision
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`primal`](#classshogun_1_1CSVMLight_1a85d406dfc47fb0241a5c5e881cf7ab5c) | primal
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`dual`](#classshogun_1_1CSVMLight_1adb28191abf363d70a92d349f948ffaf8) | dual
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`W`](#classshogun_1_1CSVMLight_1af812e9640e548a405562e0a0bfd2fcc7) | Matrix that stores the contribution by each kernel for each example (for current alphas)
`protected int32_t `[`count`](#classshogun_1_1CSVMLight_1a4858b400f708a13bd514376ab941b27d) | number of iteration
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`mymaxdiff`](#classshogun_1_1CSVMLight_1a6998ea7dc6695f4d9fb809582cc4ea49) | current alpha gap
`protected bool `[`use_kernel_cache`](#classshogun_1_1CSVMLight_1a20a7b39356cb72dade90878c38536d06) | if kernel cache is used
`protected bool `[`mkl_converged`](#classshogun_1_1CSVMLight_1af9fce52acb3de0a68f2542026299f45d) | mkl converged
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_linear_term`](#classshogun_1_1CSVM_1aa78e3d09ddcd620afb2ea0e0c39ebebe) | linear term in qp
`protected bool `[`svm_loaded`](#classshogun_1_1CSVM_1adb059ae3d435ea174376872d3bc7e161) | if SVM is loaded
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`epsilon`](#classshogun_1_1CSVM_1a0bde8d297e19e73b20b99110ba38f7bd) | epsilon
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`tube_epsilon`](#classshogun_1_1CSVM_1abba40bb38baeb174694a8d8968b79ae8) | tube epsilon for support vector regression
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`nu`](#classshogun_1_1CSVM_1a2772277c0052a522eb99d674f9ab5295) | nu
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`C1`](#classshogun_1_1CSVM_1a1ecd274e8562cfd7010dffbe7af07054) | C1 regularization const
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`C2`](#classshogun_1_1CSVM_1aadda42a3db2f58cc3a5e885d27053f4c) | C2
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`objective`](#classshogun_1_1CSVM_1af9f1d5f9e3e9539281cba7e48aa378cf) | objective
`protected int32_t `[`qpsize`](#classshogun_1_1CSVM_1aaf97cb08dd99dbc61cf59a062ada056d) | qpsize
`protected bool `[`use_shrinking`](#classshogun_1_1CSVM_1aeb303ab18c98a2156c5bf4015335d6bb) | if shrinking shall be used
`protected bool(* `[`callback`](#classshogun_1_1CSVM_1a7dd862c5d7a9281712150ec671d62aed) | callback function svm optimizers may call when they have a new (small) set of alphas
`protected `[`CMKL`](#classshogun_1_1CMKL)` * `[`mkl`](#classshogun_1_1CSVM_1a061a27bdcf1516056edc1d229e80f140) | mkl object that svm optimizers need to pass when calling the callback function
`protected `[`CKernel`](#classshogun_1_1CKernel)` * `[`kernel`](#classshogun_1_1CKernelMachine_1a4065c466d501ac67871c0f79e37b648a) | kernel
`protected `[`CCustomKernel`](#classshogun_1_1CCustomKernel)` * `[`m_custom_kernel`](#classshogun_1_1CKernelMachine_1a5d98aa6af45ac8633c825283b61ca675) | is filled with pre-computed custom kernel on data lock
`protected `[`CKernel`](#classshogun_1_1CKernel)` * `[`m_kernel_backup`](#classshogun_1_1CKernelMachine_1a43ec85cf8d70c23f3a96d131431bd0a1) | old kernel is stored here on data lock
`protected bool `[`use_batch_computation`](#classshogun_1_1CKernelMachine_1a70d4cb83d11df3fe1db70c01253efcd8) | if batch computation is enabled
`protected bool `[`use_linadd`](#classshogun_1_1CKernelMachine_1a7635719f5466cb6969a61b023657eb0e) | if linadd is enabled
`protected bool `[`use_bias`](#classshogun_1_1CKernelMachine_1a1c58e9e70ed28387a69429e81707f9ba) | if bias shall be used
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_bias`](#classshogun_1_1CKernelMachine_1ad72a1b71fbbc87f2a618539e2ecaa4fc) | bias term b
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_alpha`](#classshogun_1_1CKernelMachine_1adbf2e7c7892979cd2e78ba11b32855c6) | coefficients alpha
`protected `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`m_svs`](#classshogun_1_1CKernelMachine_1a1fcca56d5cd66573cd0f074c03270620) | array of ``support vectors'' (indices of feature objects)
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
`protected virtual bool `[`train_machine`](#classshogun_1_1CSVMLightOneClass_1ac6ad4326a1641cb16d8d74d2ac00e9d3)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | train one class svm
`protected inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_kernel`](#classshogun_1_1CSVMLight_1a5935f6eb0c3cb5363bcc7f507addd53a)`(int32_t i,int32_t j)` | compute kernel
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`optimize_qp`](#classshogun_1_1CSVMLight_1ad6763e9c0e35b1aac1a84978c1fb0932)`(QP * qp,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * epsilon_crit,int32_t nx,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * threshold,int32_t & svm_maxqpsize)` | 
`protected virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`get_linear_term_array`](#classshogun_1_1CSVM_1a5335a7ed982616a55579b4d441a9ff92)`()` | get linear term copy as dynamic array
`protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`apply_get_outputs`](#classshogun_1_1CKernelMachine_1a4b696cdfb849ca73d178431c06ddf3ff)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | apply get outputs
`protected virtual void `[`store_model_features`](#classshogun_1_1CKernelMachine_1a050a168495c7e63e3b77eea1a07c7c3b)`()` | Stores feature data of the SV indices and sets it to the lhs of the underlying kernel. Then, all SV indices are set to identity.
`protected inline virtual bool `[`train_dense`](#classshogun_1_1CMachine_1a2f4984079885c8a49f40fc6bc8366d67)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | 
`protected inline virtual bool `[`train_string`](#classshogun_1_1CMachine_1aa7f306efec16f95e741472046dee440d)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | 
`protected inline virtual bool `[`support_feature_dispatching`](#classshogun_1_1CMachine_1a6d0cdca08d31651c73d028199634bb6e)`()` | 
`protected inline virtual bool `[`support_dense_dispatching`](#classshogun_1_1CMachine_1a44486c95636e8e11e3fd83fc8073a860)`()` | 
`protected inline virtual bool `[`support_string_dispatching`](#classshogun_1_1CMachine_1a3f800163b86742f0edfdabf452a627f8)`()` | 
`protected inline virtual bool `[`continue_train`](#classshogun_1_1CMachine_1a0d918d8b628c91f0c22f2a623b495812)`()` | Continue Training
`protected inline virtual bool `[`is_label_valid`](#classshogun_1_1CMachine_1a6749b87bc09701b950e315b287f73e78)`(`[`CLabels`](#classshogun_1_1CLabels)` * lab) const` | check whether the labels is valid.
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

#### `public  `[`CSVMLightOneClass`](#classshogun_1_1CSVMLightOneClass_1a8235f7ee88030d8bfe2e3a470f4d4ffc)`()` {#classshogun_1_1CSVMLightOneClass_1a8235f7ee88030d8bfe2e3a470f4d4ffc}

default constructor

#### `public  `[`CSVMLightOneClass`](#classshogun_1_1CSVMLightOneClass_1a9a3c855e029a73a65e1dcabd71333220)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` C,`[`CKernel`](#classshogun_1_1CKernel)` * k)` {#classshogun_1_1CSVMLightOneClass_1a9a3c855e029a73a65e1dcabd71333220}

constructor

#### Parameters
* `C` constant C 

* `k` kernel

#### `public inline virtual  `[`~CSVMLightOneClass`](#classshogun_1_1CSVMLightOneClass_1a898462dc9b300e6268f3f112d498567b)`()` {#classshogun_1_1CSVMLightOneClass_1a898462dc9b300e6268f3f112d498567b}

default destructor

#### `public inline virtual `[`EMachineType`](#namespaceshogun_1af181c832c12de7a0c3b02425986106cc)` `[`get_classifier_type`](#classshogun_1_1CSVMLightOneClass_1ab0ee71eb4f9097a9b7ad2b72b1b310e2)`()` {#classshogun_1_1CSVMLightOneClass_1ab0ee71eb4f9097a9b7ad2b72b1b310e2}

get classifier type

#### Returns
classifier type LIGHTONECLASS

#### `public inline virtual const char * `[`get_name`](#classshogun_1_1CSVMLightOneClass_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` {#classshogun_1_1CSVMLightOneClass_1a9cb485686dd7a1e6f7103cf42e87717e}

Returns the name of the SGSerializable instance.

#### Returns
name of the SGSerializable

#### `public void `[`init`](#classshogun_1_1CSVMLight_1a02fd73d861ef2e4aabb38c0c9ff82947)`()` {#classshogun_1_1CSVMLight_1a02fd73d861ef2e4aabb38c0c9ff82947}

init SVM

#### `public int32_t `[`get_runtime`](#classshogun_1_1CSVMLight_1aaf29fe72c2d687fdcc80ce708321402b)`()` {#classshogun_1_1CSVMLight_1aaf29fe72c2d687fdcc80ce708321402b}

get runtime

#### Returns
runtime

#### `public void `[`svm_learn`](#classshogun_1_1CSVMLight_1acea249bf2f6f52768fc262fa24287934)`()` {#classshogun_1_1CSVMLight_1acea249bf2f6f52768fc262fa24287934}

learn SVM

#### `public int32_t `[`optimize_to_convergence`](#classshogun_1_1CSVMLight_1ac8cca3fe94a16b80eec1a9c8b8d00ee2)`(int32_t * docs,int32_t * label,int32_t totdoc,SHRINK_STATE * shrink_state,int32_t * inconsistent,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c,TIMING * timing_profile,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * maxdiff,int32_t heldout,int32_t retrain)` {#classshogun_1_1CSVMLight_1ac8cca3fe94a16b80eec1a9c8b8d00ee2}

optimize to convergence

#### Parameters
* `docs` the docs 

* `label` the label 

* `totdoc` the totdoc 

* `shrink_state` shrink state 

* `inconsistent` inconsistent 

* `a` a 

* `lin` lin 

* `c` c 

* `timing_profile` timing profile 

* `maxdiff` maximum diff 

* `heldout` held out 

* `retrain` retrain 

#### Returns
something inty

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_objective_function`](#classshogun_1_1CSVMLight_1a95f392856e00f734793d57e624aae909)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * eps,int32_t * label,int32_t totdoc)` {#classshogun_1_1CSVMLight_1a95f392856e00f734793d57e624aae909}

compute objective function

#### Parameters
* `a` a 

* `lin` lin 

* `c` c 

* `eps` epsilon 

* `label` label 

* `totdoc` totdoc 

#### Returns
something floaty

#### `public void `[`clear_index`](#classshogun_1_1CSVMLight_1a9be0210d565679fbf22cb1f39129f51f)`(int32_t * index)` {#classshogun_1_1CSVMLight_1a9be0210d565679fbf22cb1f39129f51f}

clear index

#### Parameters
* `index` index

#### `public void `[`add_to_index`](#classshogun_1_1CSVMLight_1ac00a77524973a39bf43a6ee1e06fc5b5)`(int32_t * index,int32_t elem)` {#classshogun_1_1CSVMLight_1ac00a77524973a39bf43a6ee1e06fc5b5}

add to index

#### Parameters
* `index` index 

* `elem` element at index

#### `public int32_t `[`compute_index`](#classshogun_1_1CSVMLight_1aacccc36ee508359a9ebc4c5e3764c682)`(int32_t * binfeature,int32_t range,int32_t * index)` {#classshogun_1_1CSVMLight_1aacccc36ee508359a9ebc4c5e3764c682}

compute index

#### Parameters
* `binfeature` binary feature 

* `range` range 

* `index` 

#### Returns
something inty

#### `public void `[`optimize_svm`](#classshogun_1_1CSVMLight_1a285ed34ec9a3667ec7926e101d0ce288)`(int32_t * docs,int32_t * label,int32_t * exclude_from_eq_const,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` eq_target,int32_t * chosen,int32_t * active2dnum,int32_t totdoc,int32_t * working2dnum,int32_t varnum,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * aicache,QP * qp,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * epsilon_crit_target)` {#classshogun_1_1CSVMLight_1a285ed34ec9a3667ec7926e101d0ce288}

optimise SVM

#### Parameters
* `docs` docs 

* `label` label 

* `exclude_from_eq_const` exclude from eq const 

* `eq_target` eq target 

* `chosen` chosen 

* `active2dnum` active 2D num 

* `totdoc` totdoc 

* `working2dnum` working 2D num 

* `varnum` var num 

* `a` a 

* `lin` lin 

* `c` c 

* `aicache` ai cache 

* `qp` QP 

* `epsilon_crit_target` epsilon crit target

#### `public void `[`compute_matrices_for_optimization`](#classshogun_1_1CSVMLight_1ade2f276226b2988e2b0b28499c656bbb)`(int32_t * docs,int32_t * label,int32_t * exclude_from_eq_const,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` eq_target,int32_t * chosen,int32_t * active2dnum,int32_t * key,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c,int32_t varnum,int32_t totdoc,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * aicache,QP * qp)` {#classshogun_1_1CSVMLight_1ade2f276226b2988e2b0b28499c656bbb}

compute matrices for optimization

#### Parameters
* `docs` docs 

* `label` label 

* `exclude_from_eq_const` exclude from eq const 

* `eq_target` eq target 

* `chosen` chosen 

* `active2dnum` active 2D num 

* `key` key 

* `a` a 

* `lin` lin 

* `c` c 

* `varnum` var num 

* `totdoc` totdoc 

* `aicache` ai cache 

* `qp` QP

#### `public void `[`compute_matrices_for_optimization_parallel`](#classshogun_1_1CSVMLight_1adf0e72fca21597df8081f09cf156299f)`(int32_t * docs,int32_t * label,int32_t * exclude_from_eq_const,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` eq_target,int32_t * chosen,int32_t * active2dnum,int32_t * key,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c,int32_t varnum,int32_t totdoc,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * aicache,QP * qp)` {#classshogun_1_1CSVMLight_1adf0e72fca21597df8081f09cf156299f}

compute matrices for optimization in parallel

#### Parameters
* `docs` docs 

* `label` label 

* `exclude_from_eq_const` exclude from eq const 

* `eq_target` eq target 

* `chosen` chosen 

* `active2dnum` active 2D num 

* `key` key 

* `a` a 

* `lin` lin 

* `c` c 

* `varnum` var num 

* `totdoc` totdoc 

* `aicache` ai cache 

* `qp` QP

#### `public int32_t `[`calculate_svm_model`](#classshogun_1_1CSVMLight_1a18b639ced2d4fcef76b8105031a59e0e)`(int32_t * docs,int32_t * label,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a_old,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c,int32_t * working2dnum,int32_t * active2dnum)` {#classshogun_1_1CSVMLight_1a18b639ced2d4fcef76b8105031a59e0e}

calculate SVM model

#### Parameters
* `docs` docs 

* `label` label 

* `lin` lin 

* `a` a 

* `a_old` old a 

* `c` c 

* `working2dnum` working 2D num 

* `active2dnum` active 2D num 

#### Returns
something inty

#### `public int32_t `[`check_optimality`](#classshogun_1_1CSVMLight_1ab0064451b453e29725e053ec1b73cc0c)`(int32_t * label,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c,int32_t totdoc,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * maxdiff,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` epsilon_crit_org,int32_t * misclassified,int32_t * inconsistent,int32_t * active2dnum,int32_t * last_suboptimal_at,int32_t iteration)` {#classshogun_1_1CSVMLight_1ab0064451b453e29725e053ec1b73cc0c}

check optimality

#### Parameters
* `label` label 

* `a` a 

* `lin` lin 

* `c` c 

* `totdoc` totdoc 

* `maxdiff` maximum diff 

* `epsilon_crit_org` epsilon crit org 

* `misclassified` misclassified 

* `inconsistent` inconsistent 

* `active2dnum` active 2D num 

* `last_suboptimal_at` last suboptimal at 

* `iteration` iteration 

#### Returns
something inty

#### `public virtual void `[`update_linear_component`](#classshogun_1_1CSVMLight_1acdba7d487d944c975f64dbf3b753a836)`(int32_t * docs,int32_t * label,int32_t * active2dnum,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a_old,int32_t * working2dnum,int32_t totdoc,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * aicache,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c)` {#classshogun_1_1CSVMLight_1acdba7d487d944c975f64dbf3b753a836}

update linear component

#### Parameters
* `docs` docs 

* `label` label 

* `active2dnum` active 2D num 

* `a` a 

* `a_old` old a 

* `working2dnum` working 2D num 

* `totdoc` totdoc 

* `lin` lin 

* `aicache` ai cache 

* `c` c

#### `public void `[`update_linear_component_mkl`](#classshogun_1_1CSVMLight_1ac10ac0f2e6835df436ffcfff2aac156b)`(int32_t * docs,int32_t * label,int32_t * active2dnum,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a_old,int32_t * working2dnum,int32_t totdoc,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * aicache)` {#classshogun_1_1CSVMLight_1ac10ac0f2e6835df436ffcfff2aac156b}

update linear component MKL

#### Parameters
* `docs` docs 

* `label` label 

* `active2dnum` active 2D num 

* `a` a 

* `a_old` old a 

* `working2dnum` working 2D num 

* `totdoc` totdoc 

* `lin` lin 

* `aicache` ai cache

#### `public void `[`update_linear_component_mkl_linadd`](#classshogun_1_1CSVMLight_1aad8b1708b6543ca04191adf7bf07b578)`(int32_t * docs,int32_t * label,int32_t * active2dnum,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a_old,int32_t * working2dnum,int32_t totdoc,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * aicache)` {#classshogun_1_1CSVMLight_1aad8b1708b6543ca04191adf7bf07b578}

update linear component MKL

#### Parameters
* `docs` docs 

* `label` label 

* `active2dnum` active 2D num 

* `a` a 

* `a_old` old a 

* `working2dnum` working 2D num 

* `totdoc` totdoc 

* `lin` lin 

* `aicache` ai cache

#### `public void `[`call_mkl_callback`](#classshogun_1_1CSVMLight_1a6d39c21fa2d09a8436508d7014f4cb82)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,int32_t * label,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin)` {#classshogun_1_1CSVMLight_1a6d39c21fa2d09a8436508d7014f4cb82}

#### `public int32_t `[`select_next_qp_subproblem_grad`](#classshogun_1_1CSVMLight_1ae17f95034c5a1c9d881a221176bf6eba)`(int32_t * label,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c,int32_t totdoc,int32_t qp_size,int32_t * inconsistent,int32_t * active2dnum,int32_t * working2dnum,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * selcrit,int32_t * select,int32_t cache_only,int32_t * key,int32_t * chosen)` {#classshogun_1_1CSVMLight_1ae17f95034c5a1c9d881a221176bf6eba}

select next qp subproblem grad

#### Parameters
* `label` label 

* `a` a 

* `lin` lin 

* `c` c 

* `totdoc` totdoc 

* `qp_size` size of qp 

* `inconsistent` inconsistent 

* `active2dnum` active 2D num 

* `working2dnum` working 2D num 

* `selcrit` selcrit 

* `select` select 

* `cache_only` cache only 

* `key` key 

* `chosen` chosen 

#### Returns
something inty

#### `public int32_t `[`select_next_qp_subproblem_rand`](#classshogun_1_1CSVMLight_1a4f837dbfa802997c6c3588aedab369d0)`(int32_t * label,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c,int32_t totdoc,int32_t qp_size,int32_t * inconsistent,int32_t * active2dnum,int32_t * working2dnum,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * selcrit,int32_t * select,int32_t * key,int32_t * chosen,int32_t iteration)` {#classshogun_1_1CSVMLight_1a4f837dbfa802997c6c3588aedab369d0}

select next qp subproblem rand

#### Parameters
* `label` label 

* `a` a 

* `lin` lin 

* `c` c 

* `totdoc` totdoc 

* `qp_size` size of qp 

* `inconsistent` inconsistent 

* `active2dnum` active 2D num 

* `working2dnum` working 2D num 

* `selcrit` selcrit 

* `select` select 

* `key` key 

* `chosen` chosen 

* `iteration` iteration 

#### Returns
something inty

#### `public void `[`select_top_n`](#classshogun_1_1CSVMLight_1abbbd32699279e7b8693c6e1c79e56418)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * selcrit,int32_t range,int32_t * select,int32_t n)` {#classshogun_1_1CSVMLight_1abbbd32699279e7b8693c6e1c79e56418}

select top n

#### Parameters
* `selcrit` selcrit 

* `range` range 

* `select` select 

* `n` n

#### `public void `[`init_shrink_state`](#classshogun_1_1CSVMLight_1abb11f6e852cfd459a68828be6689722a)`(SHRINK_STATE * shrink_state,int32_t totdoc,int32_t maxhistory)` {#classshogun_1_1CSVMLight_1abb11f6e852cfd459a68828be6689722a}

init shrink state

#### Parameters
* `shrink_state` shrink state 

* `totdoc` totdoc 

* `maxhistory` maximum history

#### `public void `[`shrink_state_cleanup`](#classshogun_1_1CSVMLight_1aefc3e1093bcb90cc4288079965a46152)`(SHRINK_STATE * shrink_state)` {#classshogun_1_1CSVMLight_1aefc3e1093bcb90cc4288079965a46152}

cleanup shrink state

#### Parameters
* `shrink_state` shrink state

#### `public int32_t `[`shrink_problem`](#classshogun_1_1CSVMLight_1a83fc7f196280febc0972f07e3bc37100)`(SHRINK_STATE * shrink_state,int32_t * active2dnum,int32_t * last_suboptimal_at,int32_t iteration,int32_t totdoc,int32_t minshrink,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,int32_t * inconsistent,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,int * label)` {#classshogun_1_1CSVMLight_1a83fc7f196280febc0972f07e3bc37100}

shrink problem

#### Parameters
* `shrink_state` shrink state 

* `active2dnum` active 2D num 

* `last_suboptimal_at` last suboptimal at 

* `iteration` iteration 

* `totdoc` totdoc 

* `minshrink` minimal shrink 

* `a` a 

* `inconsistent` inconsistent 

* `c` c 

* `lin` lin 

* `label` label 

#### Returns
something inty

#### `public virtual void `[`reactivate_inactive_examples`](#classshogun_1_1CSVMLight_1a9bb83012b8d9abd60f2ca0cca569cc7c)`(int32_t * label,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * a,SHRINK_STATE * shrink_state,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * lin,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * c,int32_t totdoc,int32_t iteration,int32_t * inconsistent,int32_t * docs,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * aicache,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * maxdiff)` {#classshogun_1_1CSVMLight_1a9bb83012b8d9abd60f2ca0cca569cc7c}

reactivate inactive examples

#### Parameters
* `label` label 

* `a` a 

* `shrink_state` shrink state 

* `lin` lin 

* `c` c 

* `totdoc` totdoc 

* `iteration` iteration 

* `inconsistent` inconsistent 

* `docs` docs 

* `aicache` ai cache 

* `maxdiff` maximum diff

#### `public  `[`MACHINE_PROBLEM_TYPE`](#classshogun_1_1CSVM_1aa2d22990d22f93916c7b9675db96f0ea)`(`[`PT_BINARY`](#namespaceshogun_1a0aa89aa872f89f6a174de2f45b7596d4a17ea40d0e25bb381c98ce350e05a66a6)`)` {#classshogun_1_1CSVM_1aa2d22990d22f93916c7b9675db96f0ea}

problem type

#### `public void `[`set_defaults`](#classshogun_1_1CSVM_1a682c4f9e58f769d5c1f052cd3ff83598)`(int32_t num_sv)` {#classshogun_1_1CSVM_1a682c4f9e58f769d5c1f052cd3ff83598}

set default values for members a SVM object

#### `public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_linear_term`](#classshogun_1_1CSVM_1a1fbcfd825ea31d6c8cf1434fcc39a050)`()` {#classshogun_1_1CSVM_1a1fbcfd825ea31d6c8cf1434fcc39a050}

get linear term

#### Returns
the linear term

#### `public virtual void `[`set_linear_term`](#classshogun_1_1CSVM_1a7db3d5c0ba0feac2d70a06e42b5d3ac4)`(const `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > linear_term)` {#classshogun_1_1CSVM_1a7db3d5c0ba0feac2d70a06e42b5d3ac4}

set linear term of the QP

#### Parameters
* `linear_term` the linear term

#### `public bool `[`load`](#classshogun_1_1CSVM_1a5330d46603b0a4d7b269341db92ad3a3)`(FILE * svm_file)` {#classshogun_1_1CSVM_1a5330d46603b0a4d7b269341db92ad3a3}

load a SVM from file 
#### Parameters
* `svm_file` the file handle

#### `public bool `[`save`](#classshogun_1_1CSVM_1a57adfb729db48725e1c9a30b52eae9a2)`(FILE * svm_file)` {#classshogun_1_1CSVM_1a57adfb729db48725e1c9a30b52eae9a2}

write a SVM to a file 
#### Parameters
* `svm_file` the file handle

#### `public inline void `[`set_nu`](#classshogun_1_1CSVM_1a95e04a495bfc9124526506b427b0fe53)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` nue)` {#classshogun_1_1CSVM_1a95e04a495bfc9124526506b427b0fe53}

set nu

#### Parameters
* `nue` new nu

#### `public inline void `[`set_C`](#classshogun_1_1CSVM_1a272a6477be80601077c22e17a530a460)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` c_neg,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` c_pos)` {#classshogun_1_1CSVM_1a272a6477be80601077c22e17a530a460}

set C

#### Parameters
* `c_neg` new C constant for negatively labeled examples 

* `c_pos` new C constant for positively labeled examples

Note that not all SVMs support this (however at least [CLibSVM](#classshogun_1_1CLibSVM) and [CSVMLight](#classshogun_1_1CSVMLight) do)

#### `public inline void `[`set_epsilon`](#classshogun_1_1CSVM_1ae3931ee9091f751d7584919fb92dde53)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` eps)` {#classshogun_1_1CSVM_1ae3931ee9091f751d7584919fb92dde53}

set epsilon

#### Parameters
* `eps` new epsilon

#### `public inline void `[`set_tube_epsilon`](#classshogun_1_1CSVM_1ad04af32292a7ea673ee2f4b935a68e2c)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` eps)` {#classshogun_1_1CSVM_1ad04af32292a7ea673ee2f4b935a68e2c}

set tube epsilon

#### Parameters
* `eps` new tube epsilon

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_tube_epsilon`](#classshogun_1_1CSVM_1a4aa0557a5bcf6c27002f90b7ac1ea6c1)`()` {#classshogun_1_1CSVM_1a4aa0557a5bcf6c27002f90b7ac1ea6c1}

get tube epsilon

#### Returns
tube epsilon

#### `public inline void `[`set_qpsize`](#classshogun_1_1CSVM_1a98c5fb91618fdc01a929ee41bff73f7d)`(int32_t qps)` {#classshogun_1_1CSVM_1a98c5fb91618fdc01a929ee41bff73f7d}

set qpsize

#### Parameters
* `qps` new qpsize

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_epsilon`](#classshogun_1_1CSVM_1acc649b6e3439428fe014ae45f8db19b0)`()` {#classshogun_1_1CSVM_1acc649b6e3439428fe014ae45f8db19b0}

get epsilon

#### Returns
epsilon

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_nu`](#classshogun_1_1CSVM_1af4a7fa8cd6386c1b7a26a67ca062c855)`()` {#classshogun_1_1CSVM_1af4a7fa8cd6386c1b7a26a67ca062c855}

get nu

#### Returns
nu

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_C1`](#classshogun_1_1CSVM_1a106ca4c7bad3e1779f80eae35c203144)`()` {#classshogun_1_1CSVM_1a106ca4c7bad3e1779f80eae35c203144}

get C1

#### Returns
C1

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_C2`](#classshogun_1_1CSVM_1a48b19829cbf87b2f540aa68db4ed50fa)`()` {#classshogun_1_1CSVM_1a48b19829cbf87b2f540aa68db4ed50fa}

get C2

#### Returns
C2

#### `public inline int32_t `[`get_qpsize`](#classshogun_1_1CSVM_1a6fd9f6edc2dd733f04ee069bebf653d3)`()` {#classshogun_1_1CSVM_1a6fd9f6edc2dd733f04ee069bebf653d3}

get qpsize

#### Returns
qpsize

#### `public inline void `[`set_shrinking_enabled`](#classshogun_1_1CSVM_1acd0ce5d50e27f8240c843777bfb6b033)`(bool enable)` {#classshogun_1_1CSVM_1acd0ce5d50e27f8240c843777bfb6b033}

set state of shrinking

#### Parameters
* `enable` if shrinking will be enabled

#### `public inline bool `[`get_shrinking_enabled`](#classshogun_1_1CSVM_1a5552ede75927d45cbb0165c676ac3045)`()` {#classshogun_1_1CSVM_1a5552ede75927d45cbb0165c676ac3045}

get state of shrinking

#### Returns
if shrinking is enabled

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_svm_dual_objective`](#classshogun_1_1CSVM_1a5b7f2bbc1d700ef7572ab1018cd2d57d)`()` {#classshogun_1_1CSVM_1a5b7f2bbc1d700ef7572ab1018cd2d57d}

compute svm dual objective

#### Returns
computed dual objective

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_svm_primal_objective`](#classshogun_1_1CSVM_1a92d7b51b534a0bc4c20afe7983ce1d53)`()` {#classshogun_1_1CSVM_1a92d7b51b534a0bc4c20afe7983ce1d53}

compute svm primal objective

#### Returns
computed svm primal objective

#### `public inline void `[`set_objective`](#classshogun_1_1CSVM_1a259ad42da9e35f1416836cd1d48a5aac)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` v)` {#classshogun_1_1CSVM_1a259ad42da9e35f1416836cd1d48a5aac}

set objective

#### Parameters
* `v` objective

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_objective`](#classshogun_1_1CSVM_1a35324625863981d4196336d7e7443f06)`()` {#classshogun_1_1CSVM_1a35324625863981d4196336d7e7443f06}

get objective

#### Returns
objective

#### `public inline bool `[`get_loaded_status`](#classshogun_1_1CSVM_1a68bd318899d05b99e815913f852e2316)`()` {#classshogun_1_1CSVM_1a68bd318899d05b99e815913f852e2316}

check if svm been loaded

#### Returns
if svm_loaded is true

#### `public inline void `[`set_loaded_status`](#classshogun_1_1CSVM_1a12cc58040ecd868bfe0e90836477c4f1)`(bool loaded)` {#classshogun_1_1CSVM_1a12cc58040ecd868bfe0e90836477c4f1}

set svm loaded status

if svm been loaded

#### `public void `[`set_callback_function`](#classshogun_1_1CSVM_1aa7077ff11811d1a54e61c16f7ea4c8e4)`(`[`CMKL`](#classshogun_1_1CMKL)` * m,bool(*)(`[`CMKL](#classshogun_1_1CMKL) *[mkl](#classshogun_1_1CSVM_1a061a27bdcf1516056edc1d229e80f140), const [float64_t](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4) *sumw, const [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4) suma)` cb)` {#classshogun_1_1CSVM_1aa7077ff11811d1a54e61c16f7ea4c8e4}

set callback function svm optimizers may call when they have a new (small) set of alphas

#### Parameters
* `m` pointer to mkl object 

* `cb` callback function

#### `public void `[`set_kernel`](#classshogun_1_1CKernelMachine_1aecb33756a13e8e25ee610fce65f48b99)`(`[`CKernel`](#classshogun_1_1CKernel)` * k)` {#classshogun_1_1CKernelMachine_1aecb33756a13e8e25ee610fce65f48b99}

set kernel

#### Parameters
* `k` kernel

#### `public `[`CKernel`](#classshogun_1_1CKernel)` * `[`get_kernel`](#classshogun_1_1CKernelMachine_1ab0da30c8a056a80cf85a9ea3638348d0)`()` {#classshogun_1_1CKernelMachine_1ab0da30c8a056a80cf85a9ea3638348d0}

get kernel

#### Returns
kernel

#### `public void `[`set_batch_computation_enabled`](#classshogun_1_1CKernelMachine_1a6c10d5b31beb22429fee7a17c4622c78)`(bool enable)` {#classshogun_1_1CKernelMachine_1a6c10d5b31beb22429fee7a17c4622c78}

set batch computation enabled

#### Parameters
* `enable` if batch computation shall be enabled

#### `public bool `[`get_batch_computation_enabled`](#classshogun_1_1CKernelMachine_1a3f68567b2b10d2ebfa7883da74c02285)`()` {#classshogun_1_1CKernelMachine_1a3f68567b2b10d2ebfa7883da74c02285}

check if batch computation is enabled

#### Returns
if batch computation is enabled

#### `public void `[`set_linadd_enabled`](#classshogun_1_1CKernelMachine_1ac68e75ba55a0286baab70d6a7de84f73)`(bool enable)` {#classshogun_1_1CKernelMachine_1ac68e75ba55a0286baab70d6a7de84f73}

set linadd enabled

#### Parameters
* `enable` if linadd shall be enabled

#### `public bool `[`get_linadd_enabled`](#classshogun_1_1CKernelMachine_1ae11f2c49e6b3ab6fcef5975c893e669b)`()` {#classshogun_1_1CKernelMachine_1ae11f2c49e6b3ab6fcef5975c893e669b}

check if linadd is enabled

#### Returns
if linadd is enabled

#### `public void `[`set_bias_enabled`](#classshogun_1_1CKernelMachine_1a5b773e2eeec54d607c1add0864a701ab)`(bool enable_bias)` {#classshogun_1_1CKernelMachine_1a5b773e2eeec54d607c1add0864a701ab}

set state of bias

#### Parameters
* `enable_bias` if bias shall be enabled

#### `public bool `[`get_bias_enabled`](#classshogun_1_1CKernelMachine_1a24209179a0e8592371857af993da1c51)`()` {#classshogun_1_1CKernelMachine_1a24209179a0e8592371857af993da1c51}

get state of bias

#### Returns
state of bias

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_bias`](#classshogun_1_1CKernelMachine_1a3abce3a0d07fad71b9acd49de0d00148)`()` {#classshogun_1_1CKernelMachine_1a3abce3a0d07fad71b9acd49de0d00148}

get bias

#### Returns
bias

#### `public void `[`set_bias`](#classshogun_1_1CKernelMachine_1a3e9f04b92a597096bcf3e10d472675d4)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` bias)` {#classshogun_1_1CKernelMachine_1a3e9f04b92a597096bcf3e10d472675d4}

set bias to given value

#### Parameters
* `bias` new bias

#### `public int32_t `[`get_support_vector`](#classshogun_1_1CKernelMachine_1acd4c009f894cc6df93812f75a3e69cfc)`(int32_t idx)` {#classshogun_1_1CKernelMachine_1acd4c009f894cc6df93812f75a3e69cfc}

get support vector at given index

#### Parameters
* `idx` index of support vector 

#### Returns
support vector

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_alpha`](#classshogun_1_1CKernelMachine_1ae0b6d34f42abd02ec4f0d830963a6608)`(int32_t idx)` {#classshogun_1_1CKernelMachine_1ae0b6d34f42abd02ec4f0d830963a6608}

get alpha at given index

#### Parameters
* `idx` index of alpha 

#### Returns
alpha

#### `public bool `[`set_support_vector`](#classshogun_1_1CKernelMachine_1af3b3665310b7ebff97e268276dd790be)`(int32_t idx,int32_t val)` {#classshogun_1_1CKernelMachine_1af3b3665310b7ebff97e268276dd790be}

set support vector at given index to given value

#### Parameters
* `idx` index of support vector 

* `val` new value of support vector 

#### Returns
if operation was successful

#### `public bool `[`set_alpha`](#classshogun_1_1CKernelMachine_1a5f93d1140f943f9a616712d1986d4926)`(int32_t idx,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` val)` {#classshogun_1_1CKernelMachine_1a5f93d1140f943f9a616712d1986d4926}

set alpha at given index to given value

#### Parameters
* `idx` index of alpha vector 

* `val` new value of alpha vector 

#### Returns
if operation was successful

#### `public int32_t `[`get_num_support_vectors`](#classshogun_1_1CKernelMachine_1ae0d36162db143622aecc5fe721ed8b14)`()` {#classshogun_1_1CKernelMachine_1ae0d36162db143622aecc5fe721ed8b14}

get number of support vectors

#### Returns
number of support vectors

#### `public void `[`set_alphas`](#classshogun_1_1CKernelMachine_1a560c1a5b57e2ca1ed5ba4aaa4334755f)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > alphas)` {#classshogun_1_1CKernelMachine_1a560c1a5b57e2ca1ed5ba4aaa4334755f}

set alphas to given values

#### Parameters
* `alphas` float vector with all alphas to set

#### `public void `[`set_support_vectors`](#classshogun_1_1CKernelMachine_1a2d82aa7e06239e34781ae33a3522f023)`(`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > svs)` {#classshogun_1_1CKernelMachine_1a2d82aa7e06239e34781ae33a3522f023}

set support vectors to given values

#### Parameters
* `svs` integer vector with all support vectors indexes to set

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`get_support_vectors`](#classshogun_1_1CKernelMachine_1ac04d4c9009462250851fdf99ce5255a0)`()` {#classshogun_1_1CKernelMachine_1ac04d4c9009462250851fdf99ce5255a0}

#### Returns
all support vectors

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_alphas`](#classshogun_1_1CKernelMachine_1a3c649a2215667a363360536155e263b8)`()` {#classshogun_1_1CKernelMachine_1a3c649a2215667a363360536155e263b8}

#### Returns
vector of alphas

#### `public bool `[`create_new_model`](#classshogun_1_1CKernelMachine_1a9fa06e8c87b376a4ce8a667bda094b5c)`(int32_t num)` {#classshogun_1_1CKernelMachine_1a9fa06e8c87b376a4ce8a667bda094b5c}

create new model

#### Parameters
* `num` number of alphas and support vectors in new model

#### `public bool `[`init_kernel_optimization`](#classshogun_1_1CKernelMachine_1ab60ed83e44c460fdac82ec0dfe839590)`()` {#classshogun_1_1CKernelMachine_1ab60ed83e44c460fdac82ec0dfe839590}

initialise kernel optimisation

#### Returns
if operation was successful

#### `public virtual `[`CRegressionLabels`](#classshogun_1_1CRegressionLabels)` * `[`apply_regression`](#classshogun_1_1CKernelMachine_1aaeea92e0e4795e7f63f067c16f162302)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CKernelMachine_1aaeea92e0e4795e7f63f067c16f162302}

apply kernel machine to data for regression task

#### Parameters
* `data` (test)data to be classified 

#### Returns
classified labels

#### `public virtual `[`CBinaryLabels`](#classshogun_1_1CBinaryLabels)` * `[`apply_binary`](#classshogun_1_1CKernelMachine_1a16a7dee83bb61aedc93792df578d4a77)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CKernelMachine_1a16a7dee83bb61aedc93792df578d4a77}

apply kernel machine to data for binary classification task

#### Parameters
* `data` (test)data to be classified 

#### Returns
classified labels

#### `public virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`apply_one`](#classshogun_1_1CKernelMachine_1a541d70682e317105112ba75d3d03624a)`(int32_t num)` {#classshogun_1_1CKernelMachine_1a541d70682e317105112ba75d3d03624a}

apply kernel machine to one example

#### Parameters
* `num` which example to apply to 

#### Returns
classified value

#### `public virtual bool `[`train_locked`](#classshogun_1_1CKernelMachine_1a5a69e66a9ea3f503dfbf7bc2d332d1b1)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CKernelMachine_1a5a69e66a9ea3f503dfbf7bc2d332d1b1}

This precomputes the kernel matrix and stores it

#### Parameters
* `indices` index vector (of locked features) that is used for + * training 

#### Returns
whether training was successful

#### `public virtual bool `[`train_locked`](#classshogun_1_1CMachine_1aab4927bdae8da7f0c85efdfce22c86c2)`()` {#classshogun_1_1CMachine_1aab4927bdae8da7f0c85efdfce22c86c2}

Trains a locked machine on a set of indices. Error if machine is not locked 
#### Returns
whether training was successful

#### `public virtual `[`CBinaryLabels`](#classshogun_1_1CBinaryLabels)` * `[`apply_locked_binary`](#classshogun_1_1CKernelMachine_1ac417f13423c17ebd9b0aa742f5e78c4c)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CKernelMachine_1ac417f13423c17ebd9b0aa742f5e78c4c}

Applies a locked machine on a set of indices. Error if machine is not locked. Binary case

#### Parameters
* `indices` index vector (of locked features) that is predicted 

#### Returns
resulting labels

#### `public virtual `[`CRegressionLabels`](#classshogun_1_1CRegressionLabels)` * `[`apply_locked_regression`](#classshogun_1_1CKernelMachine_1a764464fca138ac17692cb994824a1d93)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CKernelMachine_1a764464fca138ac17692cb994824a1d93}

Applies a locked machine on a set of indices. Error if machine is not locked. Binary case

#### Parameters
* `indices` index vector (of locked features) that is predicted 

#### Returns
resulting labels

#### `public virtual `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`apply_locked_get_output`](#classshogun_1_1CKernelMachine_1aa9db3cc5c76f3670c3726d03d49a2182)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CKernelMachine_1aa9db3cc5c76f3670c3726d03d49a2182}

Applies a locked machine on a set of indices. Error if machine is not locked

#### Parameters
* `indices` index vector (of locked features) that is predicted 

#### Returns
raw output of machine

#### `public virtual void `[`data_lock`](#classshogun_1_1CKernelMachine_1a420e18489602624aa97bf980b87491fc)`(`[`CLabels`](#classshogun_1_1CLabels)` * labs,`[`CFeatures`](#classshogun_1_1CFeatures)` * features)` {#classshogun_1_1CKernelMachine_1a420e18489602624aa97bf980b87491fc}

Locks the machine on given labels and data. After this call, only train_locked and apply_locked may be called.

Computes kernel matrix to speed up train/apply calls

#### Parameters
* `labs` labels used for locking 

* `features` features used for locking

#### `public virtual void `[`data_unlock`](#classshogun_1_1CKernelMachine_1a72933e4edad4e2daabeeafd9f1069e47)`()` {#classshogun_1_1CKernelMachine_1a72933e4edad4e2daabeeafd9f1069e47}

Unlocks a locked machine and restores previous state

#### `public virtual bool `[`supports_locking`](#classshogun_1_1CKernelMachine_1a9c45ac77f2e73467cd9e566d69dea83d)`() const` {#classshogun_1_1CKernelMachine_1a9c45ac77f2e73467cd9e566d69dea83d}

#### Returns
whether machine supports locking

#### `public virtual bool `[`train`](#classshogun_1_1CMachine_1aa0ece9fd14892c6dfed1bb8c78f3b3ed)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMachine_1aa0ece9fd14892c6dfed1bb8c78f3b3ed}

train machine

#### Parameters
* `data` training data (parameter can be avoided if distance or kernel-based classifiers are used and distance/kernels are initialized with train data). If flag is set, model features will be stored after training.

#### Returns
whether training was successful

#### `public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`apply`](#classshogun_1_1CMachine_1afd5d402257972c78456594234d13eb4c)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMachine_1afd5d402257972c78456594234d13eb4c}

apply machine to data if data is not specified apply to the current features

#### Parameters
* `data` (test)data to be classified 

#### Returns
classified labels

#### `public virtual `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * `[`apply_multiclass`](#classshogun_1_1CMachine_1a250aa566fff0edb31433db98f70a7f15)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMachine_1a250aa566fff0edb31433db98f70a7f15}

apply machine to data in means of multiclass classification problem

#### `public virtual `[`CStructuredLabels`](#classshogun_1_1CStructuredLabels)` * `[`apply_structured`](#classshogun_1_1CMachine_1a588efa92a0696e1d2a61a8cd21d8ebee)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMachine_1a588efa92a0696e1d2a61a8cd21d8ebee}

apply machine to data in means of SO classification problem

#### `public virtual `[`CLatentLabels`](#classshogun_1_1CLatentLabels)` * `[`apply_latent`](#classshogun_1_1CMachine_1a276d23b37202ecb31367df26a5600cf7)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CMachine_1a276d23b37202ecb31367df26a5600cf7}

apply machine to data in means of latent problem

#### `public virtual void `[`set_labels`](#classshogun_1_1CMachine_1a5f0cfd09e37bd5e793cacecb8d3c818b)`(`[`CLabels`](#classshogun_1_1CLabels)` * lab)` {#classshogun_1_1CMachine_1a5f0cfd09e37bd5e793cacecb8d3c818b}

set labels

#### Parameters
* `lab` labels

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

#### `public virtual `[`CLabels`](#classshogun_1_1CLabels)` * `[`apply_locked`](#classshogun_1_1CMachine_1add0cb383e34472fdc66db18b0a5a4bc5)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CMachine_1add0cb383e34472fdc66db18b0a5a4bc5}

Applies a locked machine on a set of indices. Error if machine is not locked

#### Parameters
* `indices` index vector (of locked features) that is predicted

#### `public virtual `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * `[`apply_locked_multiclass`](#classshogun_1_1CMachine_1a9a97b605764f96da5aaadda76a05d21d)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CMachine_1a9a97b605764f96da5aaadda76a05d21d}

applies a locked machine on a set of indices for multiclass problems

#### `public virtual `[`CStructuredLabels`](#classshogun_1_1CStructuredLabels)` * `[`apply_locked_structured`](#classshogun_1_1CMachine_1a8c63b6efbfe361a91794937f6fda544c)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CMachine_1a8c63b6efbfe361a91794937f6fda544c}

applies a locked machine on a set of indices for structured problems

#### `public virtual `[`CLatentLabels`](#classshogun_1_1CLatentLabels)` * `[`apply_locked_latent`](#classshogun_1_1CMachine_1ab4e951edb0bafda3d57fe80d648190d6)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CMachine_1ab4e951edb0bafda3d57fe80d648190d6}

applies a locked machine on a set of indices for latent problems

#### `public inline virtual void `[`post_lock`](#classshogun_1_1CMachine_1a0ad27205b36008a86beb4da016ceef0d)`(`[`CLabels`](#classshogun_1_1CLabels)` * labs,`[`CFeatures`](#classshogun_1_1CFeatures)` * features)` {#classshogun_1_1CMachine_1a0ad27205b36008a86beb4da016ceef0d}

post lock

#### `public inline bool `[`is_data_locked`](#classshogun_1_1CMachine_1a2996bc9c87fd16414792bca4aa0a14ec)`() const` {#classshogun_1_1CMachine_1a2996bc9c87fd16414792bca4aa0a14ec}

#### Returns
whether this machine is locked

#### `public inline virtual `[`EProblemType`](#namespaceshogun_1a0aa89aa872f89f6a174de2f45b7596d4)` `[`get_machine_problem_type`](#classshogun_1_1CMachine_1ac1c69755f623188143fc30188354a039)`() const` {#classshogun_1_1CMachine_1ac1c69755f623188143fc30188354a039}

returns type of problem machine solves

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

#### `protected MODEL * `[`model`](#classshogun_1_1CSVMLight_1a05b8d68085a6371c3f02933a2a007866) {#classshogun_1_1CSVMLight_1a05b8d68085a6371c3f02933a2a007866}

model

#### `protected LEARN_PARM * `[`learn_parm`](#classshogun_1_1CSVMLight_1ade6f4b01f7240261e6299d741fd702c8) {#classshogun_1_1CSVMLight_1ade6f4b01f7240261e6299d741fd702c8}

learn parameters

#### `protected int32_t `[`verbosity`](#classshogun_1_1CSVMLight_1ae58239b03e562b412748d74dece0fcc8) {#classshogun_1_1CSVMLight_1ae58239b03e562b412748d74dece0fcc8}

verbosity level (0-4)

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`init_margin`](#classshogun_1_1CSVMLight_1a807c081a57e3894502d85014ee1e1805) {#classshogun_1_1CSVMLight_1a807c081a57e3894502d85014ee1e1805}

init margin

#### `protected int32_t `[`init_iter`](#classshogun_1_1CSVMLight_1a2a2398dd614018ed5c642739b713b882) {#classshogun_1_1CSVMLight_1a2a2398dd614018ed5c642739b713b882}

init iter

#### `protected int32_t `[`precision_violations`](#classshogun_1_1CSVMLight_1a12425692bd8c9dd71dd13b938494bf32) {#classshogun_1_1CSVMLight_1a12425692bd8c9dd71dd13b938494bf32}

precision violations

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`model_b`](#classshogun_1_1CSVMLight_1a8b520a07895ec66cef773797f613d365) {#classshogun_1_1CSVMLight_1a8b520a07895ec66cef773797f613d365}

model b

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`opt_precision`](#classshogun_1_1CSVMLight_1a7a7eb2bf99e42732382c627140362f99) {#classshogun_1_1CSVMLight_1a7a7eb2bf99e42732382c627140362f99}

opt precision

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`primal`](#classshogun_1_1CSVMLight_1a85d406dfc47fb0241a5c5e881cf7ab5c) {#classshogun_1_1CSVMLight_1a85d406dfc47fb0241a5c5e881cf7ab5c}

primal

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`dual`](#classshogun_1_1CSVMLight_1adb28191abf363d70a92d349f948ffaf8) {#classshogun_1_1CSVMLight_1adb28191abf363d70a92d349f948ffaf8}

dual

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`W`](#classshogun_1_1CSVMLight_1af812e9640e548a405562e0a0bfd2fcc7) {#classshogun_1_1CSVMLight_1af812e9640e548a405562e0a0bfd2fcc7}

Matrix that stores the contribution by each kernel for each example (for current alphas)

#### `protected int32_t `[`count`](#classshogun_1_1CSVMLight_1a4858b400f708a13bd514376ab941b27d) {#classshogun_1_1CSVMLight_1a4858b400f708a13bd514376ab941b27d}

number of iteration

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`mymaxdiff`](#classshogun_1_1CSVMLight_1a6998ea7dc6695f4d9fb809582cc4ea49) {#classshogun_1_1CSVMLight_1a6998ea7dc6695f4d9fb809582cc4ea49}

current alpha gap

#### `protected bool `[`use_kernel_cache`](#classshogun_1_1CSVMLight_1a20a7b39356cb72dade90878c38536d06) {#classshogun_1_1CSVMLight_1a20a7b39356cb72dade90878c38536d06}

if kernel cache is used

#### `protected bool `[`mkl_converged`](#classshogun_1_1CSVMLight_1af9fce52acb3de0a68f2542026299f45d) {#classshogun_1_1CSVMLight_1af9fce52acb3de0a68f2542026299f45d}

mkl converged

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_linear_term`](#classshogun_1_1CSVM_1aa78e3d09ddcd620afb2ea0e0c39ebebe) {#classshogun_1_1CSVM_1aa78e3d09ddcd620afb2ea0e0c39ebebe}

linear term in qp

#### `protected bool `[`svm_loaded`](#classshogun_1_1CSVM_1adb059ae3d435ea174376872d3bc7e161) {#classshogun_1_1CSVM_1adb059ae3d435ea174376872d3bc7e161}

if SVM is loaded

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`epsilon`](#classshogun_1_1CSVM_1a0bde8d297e19e73b20b99110ba38f7bd) {#classshogun_1_1CSVM_1a0bde8d297e19e73b20b99110ba38f7bd}

epsilon

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`tube_epsilon`](#classshogun_1_1CSVM_1abba40bb38baeb174694a8d8968b79ae8) {#classshogun_1_1CSVM_1abba40bb38baeb174694a8d8968b79ae8}

tube epsilon for support vector regression

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`nu`](#classshogun_1_1CSVM_1a2772277c0052a522eb99d674f9ab5295) {#classshogun_1_1CSVM_1a2772277c0052a522eb99d674f9ab5295}

nu

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`C1`](#classshogun_1_1CSVM_1a1ecd274e8562cfd7010dffbe7af07054) {#classshogun_1_1CSVM_1a1ecd274e8562cfd7010dffbe7af07054}

C1 regularization const

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`C2`](#classshogun_1_1CSVM_1aadda42a3db2f58cc3a5e885d27053f4c) {#classshogun_1_1CSVM_1aadda42a3db2f58cc3a5e885d27053f4c}

C2

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`objective`](#classshogun_1_1CSVM_1af9f1d5f9e3e9539281cba7e48aa378cf) {#classshogun_1_1CSVM_1af9f1d5f9e3e9539281cba7e48aa378cf}

objective

#### `protected int32_t `[`qpsize`](#classshogun_1_1CSVM_1aaf97cb08dd99dbc61cf59a062ada056d) {#classshogun_1_1CSVM_1aaf97cb08dd99dbc61cf59a062ada056d}

qpsize

#### `protected bool `[`use_shrinking`](#classshogun_1_1CSVM_1aeb303ab18c98a2156c5bf4015335d6bb) {#classshogun_1_1CSVM_1aeb303ab18c98a2156c5bf4015335d6bb}

if shrinking shall be used

#### `protected bool(* `[`callback`](#classshogun_1_1CSVM_1a7dd862c5d7a9281712150ec671d62aed) {#classshogun_1_1CSVM_1a7dd862c5d7a9281712150ec671d62aed}

callback function svm optimizers may call when they have a new (small) set of alphas

#### `protected `[`CMKL`](#classshogun_1_1CMKL)` * `[`mkl`](#classshogun_1_1CSVM_1a061a27bdcf1516056edc1d229e80f140) {#classshogun_1_1CSVM_1a061a27bdcf1516056edc1d229e80f140}

mkl object that svm optimizers need to pass when calling the callback function

#### `protected `[`CKernel`](#classshogun_1_1CKernel)` * `[`kernel`](#classshogun_1_1CKernelMachine_1a4065c466d501ac67871c0f79e37b648a) {#classshogun_1_1CKernelMachine_1a4065c466d501ac67871c0f79e37b648a}

kernel

#### `protected `[`CCustomKernel`](#classshogun_1_1CCustomKernel)` * `[`m_custom_kernel`](#classshogun_1_1CKernelMachine_1a5d98aa6af45ac8633c825283b61ca675) {#classshogun_1_1CKernelMachine_1a5d98aa6af45ac8633c825283b61ca675}

is filled with pre-computed custom kernel on data lock

#### `protected `[`CKernel`](#classshogun_1_1CKernel)` * `[`m_kernel_backup`](#classshogun_1_1CKernelMachine_1a43ec85cf8d70c23f3a96d131431bd0a1) {#classshogun_1_1CKernelMachine_1a43ec85cf8d70c23f3a96d131431bd0a1}

old kernel is stored here on data lock

#### `protected bool `[`use_batch_computation`](#classshogun_1_1CKernelMachine_1a70d4cb83d11df3fe1db70c01253efcd8) {#classshogun_1_1CKernelMachine_1a70d4cb83d11df3fe1db70c01253efcd8}

if batch computation is enabled

#### `protected bool `[`use_linadd`](#classshogun_1_1CKernelMachine_1a7635719f5466cb6969a61b023657eb0e) {#classshogun_1_1CKernelMachine_1a7635719f5466cb6969a61b023657eb0e}

if linadd is enabled

#### `protected bool `[`use_bias`](#classshogun_1_1CKernelMachine_1a1c58e9e70ed28387a69429e81707f9ba) {#classshogun_1_1CKernelMachine_1a1c58e9e70ed28387a69429e81707f9ba}

if bias shall be used

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_bias`](#classshogun_1_1CKernelMachine_1ad72a1b71fbbc87f2a618539e2ecaa4fc) {#classshogun_1_1CKernelMachine_1ad72a1b71fbbc87f2a618539e2ecaa4fc}

bias term b

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`m_alpha`](#classshogun_1_1CKernelMachine_1adbf2e7c7892979cd2e78ba11b32855c6) {#classshogun_1_1CKernelMachine_1adbf2e7c7892979cd2e78ba11b32855c6}

coefficients alpha

#### `protected `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`m_svs`](#classshogun_1_1CKernelMachine_1a1fcca56d5cd66573cd0f074c03270620) {#classshogun_1_1CKernelMachine_1a1fcca56d5cd66573cd0f074c03270620}

array of ``support vectors'' (indices of feature objects)

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

#### `protected virtual bool `[`train_machine`](#classshogun_1_1CSVMLightOneClass_1ac6ad4326a1641cb16d8d74d2ac00e9d3)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CSVMLightOneClass_1ac6ad4326a1641cb16d8d74d2ac00e9d3}

train one class svm

#### Parameters
* `data` training data (parameter can be avoided if distance or kernel-based regressors are used and distance/kernels are initialized with train data)

#### Returns
whether training was successful

#### `protected inline virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_kernel`](#classshogun_1_1CSVMLight_1a5935f6eb0c3cb5363bcc7f507addd53a)`(int32_t i,int32_t j)` {#classshogun_1_1CSVMLight_1a5935f6eb0c3cb5363bcc7f507addd53a}

compute kernel

#### Parameters
* `i` at index i 

* `j` at index j 

#### Returns
computed kernel item at index i, j

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`optimize_qp`](#classshogun_1_1CSVMLight_1ad6763e9c0e35b1aac1a84978c1fb0932)`(QP * qp,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * epsilon_crit,int32_t nx,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * threshold,int32_t & svm_maxqpsize)` {#classshogun_1_1CSVMLight_1ad6763e9c0e35b1aac1a84978c1fb0932}

#### `protected virtual `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`get_linear_term_array`](#classshogun_1_1CSVM_1a5335a7ed982616a55579b4d441a9ff92)`()` {#classshogun_1_1CSVM_1a5335a7ed982616a55579b4d441a9ff92}

get linear term copy as dynamic array

#### Returns
linear term copied to a dynamic array

#### `protected `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`apply_get_outputs`](#classshogun_1_1CKernelMachine_1a4b696cdfb849ca73d178431c06ddf3ff)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CKernelMachine_1a4b696cdfb849ca73d178431c06ddf3ff}

apply get outputs

#### Parameters
* `data` features to compute outputs 

#### Returns
outputs

#### `protected virtual void `[`store_model_features`](#classshogun_1_1CKernelMachine_1a050a168495c7e63e3b77eea1a07c7c3b)`()` {#classshogun_1_1CKernelMachine_1a050a168495c7e63e3b77eea1a07c7c3b}

Stores feature data of the SV indices and sets it to the lhs of the underlying kernel. Then, all SV indices are set to identity.

May be overwritten by subclasses in case the model should be stored differently.

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

#### `protected inline virtual bool `[`is_label_valid`](#classshogun_1_1CMachine_1a6749b87bc09701b950e315b287f73e78)`(`[`CLabels`](#classshogun_1_1CLabels)` * lab) const` {#classshogun_1_1CMachine_1a6749b87bc09701b950e315b287f73e78}

check whether the labels is valid.

Subclasses can override this to implement their check of label types.

#### Parameters
* `lab` the labels being checked, guaranteed to be non-NULL

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

