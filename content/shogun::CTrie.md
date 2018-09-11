---
classname: "shogun::CTrie"
type: "class"
parents:
   - CSGObject
---

# class `shogun::CTrie` {#classshogun_1_1CTrie}

```
class shogun::CTrie
  : public CSGObject
```

Template class Trie implements a suffix trie, i.e. a tree in which all suffixes up to a certain length are stored.

It is excessively used in the [CWeightedDegreeStringKernel](#classshogun_1_1CWeightedDegreeStringKernel) and [CWeightedDegreePositionStringKernel](#classshogun_1_1CWeightedDegreePositionStringKernel) to construct the whole features space $\Phi(x)$ and enormously helps here to speed up SVM training and evaluation.

Note that depending on the underlying structure used, a single symbol in the tree requires 20 bytes (DNATrie). It is also used to do the efficient recursion in computing positional oligomer importance matrices (POIMs) where the structure requires * 20+3*8 (POIMTrie) bytes.

Finally note that this tree may use compact internal nodes (for strings that appear without modifications, thus not requiring further branches), which may save a lot of memory on higher degree tries.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public int32_t `[`NUM_SYMS`](#classshogun_1_1CTrie_1a367f311f57ff46ddfcff220c732809d1) | number of symbols
`public `[`SGIO`](#classshogun_1_1SGIO)` * `[`io`](#classshogun_1_1CSGObject_1ab3ff22f724961ace985100941ba0364d) | io
`public `[`Parallel`](#classshogun_1_1Parallel)` * `[`parallel`](#classshogun_1_1CSGObject_1a1401044636b5c2353226b974526302e9) | parallel
`public `[`Version`](#classshogun_1_1Version)` * `[`version`](#classshogun_1_1CSGObject_1afc25f30ab1a6d04798c360a2ce70b87d) | version
`public `[`Parameter`](#classshogun_1_1Parameter)` * `[`m_parameters`](#classshogun_1_1CSGObject_1a70e59038292e669701bad2af7715aa1e) | parameters
`public `[`Parameter`](#classshogun_1_1Parameter)` * `[`m_model_selection_parameters`](#classshogun_1_1CSGObject_1a113f5ae82840ac3f354f94456c10f59b) | model selection parameters
`public `[`Parameter`](#classshogun_1_1Parameter)` * `[`m_gradient_parameters`](#classshogun_1_1CSGObject_1ac3f51364b93830b9c9d991cb2d5801f4) | parameters wrt which we can compute gradients
`public uint32_t `[`m_hash`](#classshogun_1_1CSGObject_1a170f14be9561242f924939c56b372a41) | Hash of parameter values
`public  `[`CTrie`](#classshogun_1_1CTrie_1acb656e4df14990e12c644f7f765d4e70)`()` | default constructor
`public  `[`CTrie`](#classshogun_1_1CTrie_1afe7da49a0cf5e88049593a2dfb8f59c5)`(int32_t d,bool p_use_compact_terminal_nodes)` | constructor
`public  `[`CTrie`](#classshogun_1_1CTrie_1a7c884abf96e7d54fc560e9dadd8b5417)`(const `[`CTrie`](#classshogun_1_1CTrie)` & to_copy)` | copy constructor
`public virtual  `[`~CTrie`](#classshogun_1_1CTrie_1ae16e12e97bb824101497d34ae703c6af)`()` | 
`public const `[`CTrie`](#classshogun_1_1CTrie)` & `[`operator=`](#classshogun_1_1CTrie_1a24057cda3beb74e9f557315568b195f0)`(const `[`CTrie`](#classshogun_1_1CTrie)` & to_copy)` | overload operator =
`public bool `[`compare_traverse`](#classshogun_1_1CTrie_1abbf2cdd2f2dfcd67226a950af3427acc)`(int32_t node,const `[`CTrie`](#classshogun_1_1CTrie)` & other,int32_t other_node)` | compare traverse
`public bool `[`compare`](#classshogun_1_1CTrie_1a59b522b096f0b2447d6dea8968ac5f13)`(const `[`CTrie`](#classshogun_1_1CTrie)` & other)` | compare
`public bool `[`find_node`](#classshogun_1_1CTrie_1addb01cfaa7c8ef7a3a749fe535970a25)`(int32_t node,int32_t * trace,int32_t & trace_len) const` | find node
`public int32_t `[`find_deepest_node`](#classshogun_1_1CTrie_1a162f0e205789b36a4e94e1eeb0084959)`(int32_t start_node,int32_t & deepest_node) const` | find deepest node
`public void `[`display_node`](#classshogun_1_1CTrie_1a6279de7ce8d659ce4df208aeaabb260d)`(int32_t node) const` | display node
`public void `[`destroy`](#classshogun_1_1CTrie_1a3a80b6032f86a56bec74609034b3246f)`()` | destroy
`public void `[`set_degree`](#classshogun_1_1CTrie_1aff130acb80db0400e19fb9b8ebf8c6be)`(int32_t d)` | set degree
`public void `[`create`](#classshogun_1_1CTrie_1acb3093b3ab5bb131c66b9e6635652532)`(int32_t len,bool p_use_compact_terminal_nodes)` | create
`public void `[`delete_trees`](#classshogun_1_1CTrie_1aa3f635620663d41fab43979edf504626)`(bool p_use_compact_terminal_nodes)` | delete trees
`public void `[`add_to_trie`](#classshogun_1_1CTrie_1a6447af48e9eb83a8f9eb1677b2e13aee)`(int32_t i,int32_t seq_offset,int32_t * vec,`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` alpha,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * weights,bool degree_times_position_weights)` | add to trie
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_abs_weights_tree`](#classshogun_1_1CTrie_1a76da10d9fc9f58e7c64b62fda82a831b)`(int32_t tree,int32_t depth)` | compute absolute weights tree
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`compute_abs_weights`](#classshogun_1_1CTrie_1a0070e4f2032a9e17ba315d0ae7a97020)`(int32_t & len)` | compute absolute weights
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_by_tree_helper`](#classshogun_1_1CTrie_1a13e180ba0e7674cd7af488b9bd47f77d)`(int32_t * vec,int32_t len,int32_t seq_pos,int32_t tree_pos,int32_t weight_pos,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * weights,bool degree_times_position_weights)` | compute by tree helper
`public void `[`compute_by_tree_helper`](#classshogun_1_1CTrie_1a5e0261d23720f9323007e5b2e058e4a1)`(int32_t * vec,int32_t len,int32_t seq_pos,int32_t tree_pos,int32_t weight_pos,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * LevelContrib,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` factor,int32_t mkl_stepsize,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * weights,bool degree_times_position_weights)` | compute by tree helper
`public void `[`compute_scoring_helper`](#classshogun_1_1CTrie_1a1f5af9f3a878cb2cd54faeb9890bad9f)`(int32_t tree,int32_t i,int32_t j,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` weight,int32_t d,int32_t max_degree,int32_t num_feat,int32_t num_sym,int32_t sym_offset,int32_t offs,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * result)` | compute scoring helper
`public void `[`add_example_to_tree_mismatch_recursion`](#classshogun_1_1CTrie_1a27d9a51d58eb2756f305339783b60e58)`(int32_t tree,int32_t i,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` alpha,int32_t * vec,int32_t len_rem,int32_t degree_rec,int32_t mismatch_rec,int32_t max_mismatch,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * weights)` | add example to tree mismatch recursion
`public void `[`traverse`](#classshogun_1_1CTrie_1a84099b370e7382a42fd264692b01be85)`(int32_t tree,const int32_t p,struct TreeParseInfo info,const int32_t depth,int32_t *const x,const int32_t k)` | traverse
`public void `[`count`](#classshogun_1_1CTrie_1a53672616226b245d4315fb2cbd163db9)`(const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` w,const int32_t depth,const struct TreeParseInfo info,const int32_t p,int32_t * x,const int32_t k)` | count
`public int32_t `[`compact_nodes`](#classshogun_1_1CTrie_1a5eb6f79f4e34a06748fccc7e31ec0659)`(int32_t start_node,int32_t depth,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * weights)` | compact nodes
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_cumulative_score`](#classshogun_1_1CTrie_1aea9b1756b0ffb1288560bc66e4a42134)`(int32_t pos,uint64_t seq,int32_t deg,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * weights)` | get cumulative score
`public void `[`fill_backtracking_table_recursion`](#classshogun_1_1CTrie_1ab27beb809be6dd85d9d155c741660bf8)`(Trie * tree,int32_t depth,uint64_t seq,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` value,`[`DynArray`](#classshogun_1_1DynArray)`< ConsensusEntry > * table,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * weights)` | fill backtracking table recursion
`public void `[`fill_backtracking_table`](#classshogun_1_1CTrie_1ac1270d3ff755ad5db6b862959979f383)`(int32_t pos,`[`DynArray`](#classshogun_1_1DynArray)`< ConsensusEntry > * prev,`[`DynArray`](#classshogun_1_1DynArray)`< ConsensusEntry > * cur,bool cumulative,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * weights)` | fill backtracking table
`public void `[`POIMs_extract_W`](#classshogun_1_1CTrie_1ad89ad1795f95ce536dc4cbbb1961e5d0)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const *const W,const int32_t K)` | POIMs extract W
`public void `[`POIMs_precalc_SLR`](#classshogun_1_1CTrie_1a0688b5d1c2bc37c7f5ab033df12efb9e)`(const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const distrib)` | POIMs precalc SLR
`public void `[`POIMs_get_SLR`](#classshogun_1_1CTrie_1a7cc2906f58a5ab4ddcfc5c65f8a95bb4)`(const int32_t parentIdx,const int32_t sym,const int32_t depth,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * S,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * L,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * R)` | POIMs get SLR
`public void `[`POIMs_add_SLR`](#classshogun_1_1CTrie_1a23bce2214ddc13cfedcc8c445a4aef5f)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const *const poims,const int32_t K,const int32_t debug)` | POIMs add SLR
`public inline bool `[`get_use_compact_terminal_nodes`](#classshogun_1_1CTrie_1a48adcbe1c20e63966a6dd92970dd1b71)`()` | get use compact terminal nodes
`public inline void `[`set_use_compact_terminal_nodes`](#classshogun_1_1CTrie_1a1aa2ca12a24716a58836ea4030bb8e28)`(bool p_use_compact_terminal_nodes)` | set use compact terminal nodes
`public inline int32_t `[`get_num_used_nodes`](#classshogun_1_1CTrie_1a9550979ff4901166b9ff47bc541e9607)`()` | get number of used nodes
`public inline void `[`set_position_weights`](#classshogun_1_1CTrie_1a9978eb1ce2f85db90e47dc08426e1360)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * p_position_weights)` | set position weights
`public inline int32_t `[`get_node`](#classshogun_1_1CTrie_1ae4976b23f96483d8782a76cfbb5b2c48)`(bool last_node)` | get node
`public inline void `[`check_treemem`](#classshogun_1_1CTrie_1a1ab2dc1655e50542b1bbda382ca83859)`()` | check tree memory usage
`public inline void `[`set_weights_in_tree`](#classshogun_1_1CTrie_1a09da45f2aa8a07f1464583256b477dbf)`(bool weights_in_tree_)` | set weights in tree
`public inline bool `[`get_weights_in_tree`](#classshogun_1_1CTrie_1a65eef2046f9670a9f140ba490eb897c3)`()` | get weights in tree
`public void `[`POIMs_extract_W_helper`](#classshogun_1_1CTrie_1a248b966f71431d01148ba5d5103f374d)`(const int32_t nodeIdx,const int32_t depth,const int32_t offset,const int32_t y0,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const *const W,const int32_t K)` | POIMs extract W helper
`public void `[`POIMs_calc_SLR_helper1`](#classshogun_1_1CTrie_1a90be23e61c82a83502be8b363631e289)`(const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const distrib,const int32_t i,const int32_t nodeIdx,int32_t left_tries_idx,const int32_t depth,int32_t const lastSym,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * S,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * L,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * R)` | POIMs calc SLR helper
`public void `[`POIMs_calc_SLR_helper2`](#classshogun_1_1CTrie_1a5b28095369e632966e0b171f0b52749f)`(const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const distrib,const int32_t i,const int32_t nodeIdx,int32_t left_tries_idx,const int32_t depth,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * S,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * L,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * R)` | POIMs calc SLR helper 2 
`public void `[`POIMs_add_SLR_helper1`](#classshogun_1_1CTrie_1aeed343b271faec052a5fc478d2b47e71)`(const int32_t nodeIdx,const int32_t depth,const int32_t i,const int32_t y0,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const *const poims,const int32_t K,const int32_t debug)` | POIMs add SLR helper 1
`public void `[`POIMs_add_SLR_helper2`](#classshogun_1_1CTrie_1a823bbe778810e5c8fe0dca4b170d88ad)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const *const poims,const int32_t K,const int32_t k,const int32_t i,const int32_t y,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` valW,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` valS,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` valL,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` valR,const int32_t debug)` | POIMs add SLR helper 2
`public inline virtual const char * `[`get_name`](#classshogun_1_1CTrie_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` | #### Returns
`public template<>`  <br/>`void `[`POIMs_extract_W_helper`](#classshogun_1_1CTrie_1a28bfeb71bcf6048d087d8e65110e591d)`(const int32_t nodeIdx,const int32_t depth,const int32_t offset,const int32_t y0,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const *const W,const int32_t K)` | 
`public template<>`  <br/>`void `[`POIMs_extract_W`](#classshogun_1_1CTrie_1ab38fffa2d8aa27360d7e029e67f01e83)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const *const W,const int32_t K)` | 
`public template<>`  <br/>`void `[`POIMs_calc_SLR_helper1`](#classshogun_1_1CTrie_1a49ad1011cab4e042c1ccd84042f1fa79)`(const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const distrib,const int32_t i,const int32_t nodeIdx,int32_t left_tries_idx,const int32_t depth,int32_t const lastSym,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * S,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * L,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * R)` | 
`public template<>`  <br/>`void `[`POIMs_calc_SLR_helper2`](#classshogun_1_1CTrie_1a2286269429b159c00f2b8a1186b43454)`(const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const distrib,const int32_t i,const int32_t nodeIdx,int32_t left_tries_idx,const int32_t depth,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * S,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * L,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * R)` | 
`public template<>`  <br/>`void `[`POIMs_precalc_SLR`](#classshogun_1_1CTrie_1a827691bb2efdeed3c7a1326dc9c3c6c6)`(const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const distrib)` | 
`public template<>`  <br/>`void `[`POIMs_get_SLR`](#classshogun_1_1CTrie_1a8b184d76faf9026a0e0a4f7069463c02)`(const int32_t parentIdx,const int32_t sym,const int32_t depth,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * S,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * L,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * R)` | 
`public template<>`  <br/>`void `[`POIMs_add_SLR_helper2`](#classshogun_1_1CTrie_1ad392481f528265b599b38ac4e8748cd4)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const *const poims,const int32_t K,const int32_t k,const int32_t i,const int32_t y,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` valW,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` valS,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` valL,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` valR,const int32_t debug)` | 
`public template<>`  <br/>`void `[`POIMs_add_SLR_helper1`](#classshogun_1_1CTrie_1a30c0e30f4625c437903d0a83705246e6)`(const int32_t nodeIdx,const int32_t depth,const int32_t i,const int32_t y0,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const *const poims,const int32_t K,const int32_t debug)` | 
`public template<>`  <br/>`void `[`POIMs_add_SLR`](#classshogun_1_1CTrie_1a063ffffc29b1968a8c312a3729007b40)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const *const poims,const int32_t K,const int32_t debug)` | 
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
`protected int32_t `[`length`](#classshogun_1_1CTrie_1a5ae5048776b1de2d7dce124f78dc300f) | length
`protected int32_t * `[`trees`](#classshogun_1_1CTrie_1ae0079cae9635c82aa95e9b29f50b9193) | trees
`protected int32_t `[`degree`](#classshogun_1_1CTrie_1a192432a474907a70b37aa10ddabc0c97) | degree
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`position_weights`](#classshogun_1_1CTrie_1a3db9cfc85326a0471076c3ca57e68e28) | position weights
`protected Trie * `[`TreeMem`](#classshogun_1_1CTrie_1a80f3cea09ce6343de93bdeb2bd5e03a6) | tree memory
`protected int32_t `[`TreeMemPtr`](#classshogun_1_1CTrie_1a13d2b8afd8463f10d9a1f1b3266cd73b) | tree memory pointer
`protected int32_t `[`TreeMemPtrMax`](#classshogun_1_1CTrie_1a7832defb495918167ecdfa892d1ffe2a) | tree memory pointer maximum
`protected bool `[`use_compact_terminal_nodes`](#classshogun_1_1CTrie_1a9c8f4fae95027f1551b763a62f404cdb) | if compact terminal nodes are used
`protected bool `[`weights_in_tree`](#classshogun_1_1CTrie_1ad3901a594bb455678f820fe476e3d4a6) | if weights are in tree
`protected int32_t * `[`nofsKmers`](#classshogun_1_1CTrie_1ada368866267ab1a41b1c643090dbf38f) | nofsKmers
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

#### `public int32_t `[`NUM_SYMS`](#classshogun_1_1CTrie_1a367f311f57ff46ddfcff220c732809d1) {#classshogun_1_1CTrie_1a367f311f57ff46ddfcff220c732809d1}

number of symbols

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

#### `public  `[`CTrie`](#classshogun_1_1CTrie_1acb656e4df14990e12c644f7f765d4e70)`()` {#classshogun_1_1CTrie_1acb656e4df14990e12c644f7f765d4e70}

default constructor

#### `public  `[`CTrie`](#classshogun_1_1CTrie_1afe7da49a0cf5e88049593a2dfb8f59c5)`(int32_t d,bool p_use_compact_terminal_nodes)` {#classshogun_1_1CTrie_1afe7da49a0cf5e88049593a2dfb8f59c5}

constructor

#### Parameters
* `d` degree 

* `p_use_compact_terminal_nodes` if compact terminal nodes shall be used

#### `public  `[`CTrie`](#classshogun_1_1CTrie_1a7c884abf96e7d54fc560e9dadd8b5417)`(const `[`CTrie`](#classshogun_1_1CTrie)` & to_copy)` {#classshogun_1_1CTrie_1a7c884abf96e7d54fc560e9dadd8b5417}

copy constructor

#### `public virtual  `[`~CTrie`](#classshogun_1_1CTrie_1ae16e12e97bb824101497d34ae703c6af)`()` {#classshogun_1_1CTrie_1ae16e12e97bb824101497d34ae703c6af}

#### `public const `[`CTrie`](#classshogun_1_1CTrie)` & `[`operator=`](#classshogun_1_1CTrie_1a24057cda3beb74e9f557315568b195f0)`(const `[`CTrie`](#classshogun_1_1CTrie)` & to_copy)` {#classshogun_1_1CTrie_1a24057cda3beb74e9f557315568b195f0}

overload operator =

#### `public bool `[`compare_traverse`](#classshogun_1_1CTrie_1abbf2cdd2f2dfcd67226a950af3427acc)`(int32_t node,const `[`CTrie`](#classshogun_1_1CTrie)` & other,int32_t other_node)` {#classshogun_1_1CTrie_1abbf2cdd2f2dfcd67226a950af3427acc}

compare traverse

#### Parameters
* `node` node 

* `other` other trie 

* `other_node` other node 

#### Returns
if comparison was successful

#### `public bool `[`compare`](#classshogun_1_1CTrie_1a59b522b096f0b2447d6dea8968ac5f13)`(const `[`CTrie`](#classshogun_1_1CTrie)` & other)` {#classshogun_1_1CTrie_1a59b522b096f0b2447d6dea8968ac5f13}

compare

#### Parameters
* `other` other trie 

#### Returns
if comparison was successful

#### `public bool `[`find_node`](#classshogun_1_1CTrie_1addb01cfaa7c8ef7a3a749fe535970a25)`(int32_t node,int32_t * trace,int32_t & trace_len) const` {#classshogun_1_1CTrie_1addb01cfaa7c8ef7a3a749fe535970a25}

find node

#### Parameters
* `node` node to find 

* `trace` trace 

* `trace_len` length of trace

#### `public int32_t `[`find_deepest_node`](#classshogun_1_1CTrie_1a162f0e205789b36a4e94e1eeb0084959)`(int32_t start_node,int32_t & deepest_node) const` {#classshogun_1_1CTrie_1a162f0e205789b36a4e94e1eeb0084959}

find deepest node

#### Parameters
* `start_node` start node 

* `deepest_node` deepest node will be stored in here 

#### Returns
depth of deepest node

#### `public void `[`display_node`](#classshogun_1_1CTrie_1a6279de7ce8d659ce4df208aeaabb260d)`(int32_t node) const` {#classshogun_1_1CTrie_1a6279de7ce8d659ce4df208aeaabb260d}

display node

#### Parameters
* `node` node to display

#### `public void `[`destroy`](#classshogun_1_1CTrie_1a3a80b6032f86a56bec74609034b3246f)`()` {#classshogun_1_1CTrie_1a3a80b6032f86a56bec74609034b3246f}

destroy

#### `public void `[`set_degree`](#classshogun_1_1CTrie_1aff130acb80db0400e19fb9b8ebf8c6be)`(int32_t d)` {#classshogun_1_1CTrie_1aff130acb80db0400e19fb9b8ebf8c6be}

set degree

#### Parameters
* `d` new degree

#### `public void `[`create`](#classshogun_1_1CTrie_1acb3093b3ab5bb131c66b9e6635652532)`(int32_t len,bool p_use_compact_terminal_nodes)` {#classshogun_1_1CTrie_1acb3093b3ab5bb131c66b9e6635652532}

create

#### Parameters
* `len` length of new trie 

* `p_use_compact_terminal_nodes` if compact terminal nodes shall be used

#### `public void `[`delete_trees`](#classshogun_1_1CTrie_1aa3f635620663d41fab43979edf504626)`(bool p_use_compact_terminal_nodes)` {#classshogun_1_1CTrie_1aa3f635620663d41fab43979edf504626}

delete trees

#### Parameters
* `p_use_compact_terminal_nodes` if compact terminal nodes shall be used

#### `public void `[`add_to_trie`](#classshogun_1_1CTrie_1a6447af48e9eb83a8f9eb1677b2e13aee)`(int32_t i,int32_t seq_offset,int32_t * vec,`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` alpha,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * weights,bool degree_times_position_weights)` {#classshogun_1_1CTrie_1a6447af48e9eb83a8f9eb1677b2e13aee}

add to trie

#### Parameters
* `i` i 

* `seq_offset` sequence offset 

* `vec` vector 

* `alpha` alpha 

* `weights` weights 

* `degree_times_position_weights` if degree times position weights shall be applied

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_abs_weights_tree`](#classshogun_1_1CTrie_1a76da10d9fc9f58e7c64b62fda82a831b)`(int32_t tree,int32_t depth)` {#classshogun_1_1CTrie_1a76da10d9fc9f58e7c64b62fda82a831b}

compute absolute weights tree

#### Parameters
* `tree` tree to compute for 

* `depth` depth 

#### Returns
computed absolute weights tree

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`compute_abs_weights`](#classshogun_1_1CTrie_1a0070e4f2032a9e17ba315d0ae7a97020)`(int32_t & len)` {#classshogun_1_1CTrie_1a0070e4f2032a9e17ba315d0ae7a97020}

compute absolute weights

#### Parameters
* `len` length 

#### Returns
computed absolute weights

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_by_tree_helper`](#classshogun_1_1CTrie_1a13e180ba0e7674cd7af488b9bd47f77d)`(int32_t * vec,int32_t len,int32_t seq_pos,int32_t tree_pos,int32_t weight_pos,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * weights,bool degree_times_position_weights)` {#classshogun_1_1CTrie_1a13e180ba0e7674cd7af488b9bd47f77d}

compute by tree helper

#### Parameters
* `vec` vector 

* `len` length 

* `seq_pos` sequence position 

* `tree_pos` tree position 

* `weight_pos` weight position 

* `weights` 

* `degree_times_position_weights` if degree times position weights shall be applied 

#### Returns
a computed value

#### `public void `[`compute_by_tree_helper`](#classshogun_1_1CTrie_1a5e0261d23720f9323007e5b2e058e4a1)`(int32_t * vec,int32_t len,int32_t seq_pos,int32_t tree_pos,int32_t weight_pos,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * LevelContrib,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` factor,int32_t mkl_stepsize,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * weights,bool degree_times_position_weights)` {#classshogun_1_1CTrie_1a5e0261d23720f9323007e5b2e058e4a1}

compute by tree helper

#### Parameters
* `vec` vector 

* `len` length 

* `seq_pos` sequence position 

* `tree_pos` tree position 

* `weight_pos` weight position 

* `LevelContrib` level contribution 

* `factor` factor 

* `mkl_stepsize` MKL stepsize 

* `weights` 

* `degree_times_position_weights` if degree times position weights shall be applied

#### `public void `[`compute_scoring_helper`](#classshogun_1_1CTrie_1a1f5af9f3a878cb2cd54faeb9890bad9f)`(int32_t tree,int32_t i,int32_t j,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` weight,int32_t d,int32_t max_degree,int32_t num_feat,int32_t num_sym,int32_t sym_offset,int32_t offs,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * result)` {#classshogun_1_1CTrie_1a1f5af9f3a878cb2cd54faeb9890bad9f}

compute scoring helper

#### Parameters
* `tree` tree 

* `i` i 

* `j` j 

* `weight` weight 

* `d` degree 

* `max_degree` maximum degree 

* `num_feat` number of features 

* `num_sym` number of symbols 

* `sym_offset` symbol offset 

* `offs` offsets 

* `result` result

#### `public void `[`add_example_to_tree_mismatch_recursion`](#classshogun_1_1CTrie_1a27d9a51d58eb2756f305339783b60e58)`(int32_t tree,int32_t i,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` alpha,int32_t * vec,int32_t len_rem,int32_t degree_rec,int32_t mismatch_rec,int32_t max_mismatch,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * weights)` {#classshogun_1_1CTrie_1a27d9a51d58eb2756f305339783b60e58}

add example to tree mismatch recursion

#### Parameters
* `tree` tree 

* `i` i 

* `alpha` alpha 

* `vec` vector 

* `len_rem` length of rem 

* `degree_rec` degree rec 

* `mismatch_rec` mismatch rec 

* `max_mismatch` maximum mismatch 

* `weights` weights

#### `public void `[`traverse`](#classshogun_1_1CTrie_1a84099b370e7382a42fd264692b01be85)`(int32_t tree,const int32_t p,struct TreeParseInfo info,const int32_t depth,int32_t *const x,const int32_t k)` {#classshogun_1_1CTrie_1a84099b370e7382a42fd264692b01be85}

traverse

#### Parameters
* `tree` tree 

* `p` p 

* `info` tree parse info 

* `depth` depth 

* `x` x 

* `k` k

#### `public void `[`count`](#classshogun_1_1CTrie_1a53672616226b245d4315fb2cbd163db9)`(const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` w,const int32_t depth,const struct TreeParseInfo info,const int32_t p,int32_t * x,const int32_t k)` {#classshogun_1_1CTrie_1a53672616226b245d4315fb2cbd163db9}

count

#### Parameters
* `w` w 

* `depth` depth 

* `info` tree parse info 

* `p` p 

* `x` x 

* `k`

#### `public int32_t `[`compact_nodes`](#classshogun_1_1CTrie_1a5eb6f79f4e34a06748fccc7e31ec0659)`(int32_t start_node,int32_t depth,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * weights)` {#classshogun_1_1CTrie_1a5eb6f79f4e34a06748fccc7e31ec0659}

compact nodes

#### Parameters
* `start_node` start node 

* `depth` depth 

* `weights` weights

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_cumulative_score`](#classshogun_1_1CTrie_1aea9b1756b0ffb1288560bc66e4a42134)`(int32_t pos,uint64_t seq,int32_t deg,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * weights)` {#classshogun_1_1CTrie_1aea9b1756b0ffb1288560bc66e4a42134}

get cumulative score

#### Parameters
* `pos` position 

* `seq` sequence 

* `deg` degree 

* `weights` weights 

#### Returns
cumulative score

#### `public void `[`fill_backtracking_table_recursion`](#classshogun_1_1CTrie_1ab27beb809be6dd85d9d155c741660bf8)`(Trie * tree,int32_t depth,uint64_t seq,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` value,`[`DynArray`](#classshogun_1_1DynArray)`< ConsensusEntry > * table,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * weights)` {#classshogun_1_1CTrie_1ab27beb809be6dd85d9d155c741660bf8}

fill backtracking table recursion

#### Parameters
* `tree` tree 

* `depth` depth 

* `seq` sequence 

* `value` value 

* `table` table of concensus entries 

* `weights` weights

#### `public void `[`fill_backtracking_table`](#classshogun_1_1CTrie_1ac1270d3ff755ad5db6b862959979f383)`(int32_t pos,`[`DynArray`](#classshogun_1_1DynArray)`< ConsensusEntry > * prev,`[`DynArray`](#classshogun_1_1DynArray)`< ConsensusEntry > * cur,bool cumulative,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * weights)` {#classshogun_1_1CTrie_1ac1270d3ff755ad5db6b862959979f383}

fill backtracking table

#### Parameters
* `pos` position 

* `prev` previous concencus entry 

* `cur` current concensus entry 

* `cumulative` if is cumulative 

* `weights` weights

#### `public void `[`POIMs_extract_W`](#classshogun_1_1CTrie_1ad89ad1795f95ce536dc4cbbb1961e5d0)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const *const W,const int32_t K)` {#classshogun_1_1CTrie_1ad89ad1795f95ce536dc4cbbb1961e5d0}

POIMs extract W

#### Parameters
* `W` W 

* `K` K

#### `public void `[`POIMs_precalc_SLR`](#classshogun_1_1CTrie_1a0688b5d1c2bc37c7f5ab033df12efb9e)`(const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const distrib)` {#classshogun_1_1CTrie_1a0688b5d1c2bc37c7f5ab033df12efb9e}

POIMs precalc SLR

#### Parameters
* `distrib` distribution

#### `public void `[`POIMs_get_SLR`](#classshogun_1_1CTrie_1a7cc2906f58a5ab4ddcfc5c65f8a95bb4)`(const int32_t parentIdx,const int32_t sym,const int32_t depth,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * S,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * L,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * R)` {#classshogun_1_1CTrie_1a7cc2906f58a5ab4ddcfc5c65f8a95bb4}

POIMs get SLR

#### Parameters
* `parentIdx` parent index 

* `sym` symbol 

* `depth` depth 

* `S` will point to S 

* `L` will point to L 

* `R` will point to R

#### `public void `[`POIMs_add_SLR`](#classshogun_1_1CTrie_1a23bce2214ddc13cfedcc8c445a4aef5f)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const *const poims,const int32_t K,const int32_t debug)` {#classshogun_1_1CTrie_1a23bce2214ddc13cfedcc8c445a4aef5f}

POIMs add SLR

#### Parameters
* `poims` POIMs 

* `K` K 

* `debug` debug level

#### `public inline bool `[`get_use_compact_terminal_nodes`](#classshogun_1_1CTrie_1a48adcbe1c20e63966a6dd92970dd1b71)`()` {#classshogun_1_1CTrie_1a48adcbe1c20e63966a6dd92970dd1b71}

get use compact terminal nodes

#### Returns
if compact terminal nodes are used

#### `public inline void `[`set_use_compact_terminal_nodes`](#classshogun_1_1CTrie_1a1aa2ca12a24716a58836ea4030bb8e28)`(bool p_use_compact_terminal_nodes)` {#classshogun_1_1CTrie_1a1aa2ca12a24716a58836ea4030bb8e28}

set use compact terminal nodes

#### Parameters
* `p_use_compact_terminal_nodes` if compact terminal nodes shall be used

#### `public inline int32_t `[`get_num_used_nodes`](#classshogun_1_1CTrie_1a9550979ff4901166b9ff47bc541e9607)`()` {#classshogun_1_1CTrie_1a9550979ff4901166b9ff47bc541e9607}

get number of used nodes

#### Returns
number of used nodes

#### `public inline void `[`set_position_weights`](#classshogun_1_1CTrie_1a9978eb1ce2f85db90e47dc08426e1360)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * p_position_weights)` {#classshogun_1_1CTrie_1a9978eb1ce2f85db90e47dc08426e1360}

set position weights

#### Parameters
* `p_position_weights` new position weights

#### `public inline int32_t `[`get_node`](#classshogun_1_1CTrie_1ae4976b23f96483d8782a76cfbb5b2c48)`(bool last_node)` {#classshogun_1_1CTrie_1ae4976b23f96483d8782a76cfbb5b2c48}

get node

#### Returns
node

#### `public inline void `[`check_treemem`](#classshogun_1_1CTrie_1a1ab2dc1655e50542b1bbda382ca83859)`()` {#classshogun_1_1CTrie_1a1ab2dc1655e50542b1bbda382ca83859}

check tree memory usage

#### `public inline void `[`set_weights_in_tree`](#classshogun_1_1CTrie_1a09da45f2aa8a07f1464583256b477dbf)`(bool weights_in_tree_)` {#classshogun_1_1CTrie_1a09da45f2aa8a07f1464583256b477dbf}

set weights in tree

#### Parameters
* `weights_in_tree_` if weights shall be in tree

#### `public inline bool `[`get_weights_in_tree`](#classshogun_1_1CTrie_1a65eef2046f9670a9f140ba490eb897c3)`()` {#classshogun_1_1CTrie_1a65eef2046f9670a9f140ba490eb897c3}

get weights in tree

#### Returns
if weights are in tree

#### `public void `[`POIMs_extract_W_helper`](#classshogun_1_1CTrie_1a248b966f71431d01148ba5d5103f374d)`(const int32_t nodeIdx,const int32_t depth,const int32_t offset,const int32_t y0,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const *const W,const int32_t K)` {#classshogun_1_1CTrie_1a248b966f71431d01148ba5d5103f374d}

POIMs extract W helper

#### Parameters
* `nodeIdx` node index 

* `depth` depth 

* `offset` offset 

* `y0` y0 

* `W` W 

* `K` K

#### `public void `[`POIMs_calc_SLR_helper1`](#classshogun_1_1CTrie_1a90be23e61c82a83502be8b363631e289)`(const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const distrib,const int32_t i,const int32_t nodeIdx,int32_t left_tries_idx,const int32_t depth,int32_t const lastSym,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * S,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * L,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * R)` {#classshogun_1_1CTrie_1a90be23e61c82a83502be8b363631e289}

POIMs calc SLR helper

#### Parameters
* `distrib` distribution 

* `i` i 

* `nodeIdx` node index 

* `left_tries_idx` left tries index 

* `depth` depth 

* `lastSym` last symbol 

* `S` S 

* `L` L 

* `R` R

#### `public void `[`POIMs_calc_SLR_helper2`](#classshogun_1_1CTrie_1a5b28095369e632966e0b171f0b52749f)`(const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const distrib,const int32_t i,const int32_t nodeIdx,int32_t left_tries_idx,const int32_t depth,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * S,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * L,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * R)` {#classshogun_1_1CTrie_1a5b28095369e632966e0b171f0b52749f}

POIMs calc SLR helper 2 
#### Parameters
* `distrib` distribution 

* `i` i 

* `nodeIdx` node index 

* `left_tries_idx` left tries index 

* `depth` depth 

* `S` S 

* `L` L 

* `R` R

#### `public void `[`POIMs_add_SLR_helper1`](#classshogun_1_1CTrie_1aeed343b271faec052a5fc478d2b47e71)`(const int32_t nodeIdx,const int32_t depth,const int32_t i,const int32_t y0,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const *const poims,const int32_t K,const int32_t debug)` {#classshogun_1_1CTrie_1aeed343b271faec052a5fc478d2b47e71}

POIMs add SLR helper 1

#### Parameters
* `nodeIdx` node index 

* `depth` depth 

* `i` i 

* `y0` y0 

* `poims` POIMs 

* `K` K 

* `debug` debug level

#### `public void `[`POIMs_add_SLR_helper2`](#classshogun_1_1CTrie_1a823bbe778810e5c8fe0dca4b170d88ad)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const *const poims,const int32_t K,const int32_t k,const int32_t i,const int32_t y,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` valW,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` valS,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` valL,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` valR,const int32_t debug)` {#classshogun_1_1CTrie_1a823bbe778810e5c8fe0dca4b170d88ad}

POIMs add SLR helper 2

#### Parameters
* `poims` POIMs 

* `K` K 

* `k` k 

* `i` i 

* `y` y 

* `valW` value W 

* `valS` value S 

* `valL` value L 

* `valR` value R 

* `debug` debug level

#### `public inline virtual const char * `[`get_name`](#classshogun_1_1CTrie_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` {#classshogun_1_1CTrie_1a9cb485686dd7a1e6f7103cf42e87717e}

#### Returns
object name

#### `public template<>`  <br/>`void `[`POIMs_extract_W_helper`](#classshogun_1_1CTrie_1a28bfeb71bcf6048d087d8e65110e591d)`(const int32_t nodeIdx,const int32_t depth,const int32_t offset,const int32_t y0,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const *const W,const int32_t K)` {#classshogun_1_1CTrie_1a28bfeb71bcf6048d087d8e65110e591d}

#### `public template<>`  <br/>`void `[`POIMs_extract_W`](#classshogun_1_1CTrie_1ab38fffa2d8aa27360d7e029e67f01e83)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const *const W,const int32_t K)` {#classshogun_1_1CTrie_1ab38fffa2d8aa27360d7e029e67f01e83}

#### `public template<>`  <br/>`void `[`POIMs_calc_SLR_helper1`](#classshogun_1_1CTrie_1a49ad1011cab4e042c1ccd84042f1fa79)`(const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const distrib,const int32_t i,const int32_t nodeIdx,int32_t left_tries_idx,const int32_t depth,int32_t const lastSym,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * S,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * L,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * R)` {#classshogun_1_1CTrie_1a49ad1011cab4e042c1ccd84042f1fa79}

#### `public template<>`  <br/>`void `[`POIMs_calc_SLR_helper2`](#classshogun_1_1CTrie_1a2286269429b159c00f2b8a1186b43454)`(const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const distrib,const int32_t i,const int32_t nodeIdx,int32_t left_tries_idx,const int32_t depth,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * S,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * L,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * R)` {#classshogun_1_1CTrie_1a2286269429b159c00f2b8a1186b43454}

#### `public template<>`  <br/>`void `[`POIMs_precalc_SLR`](#classshogun_1_1CTrie_1a827691bb2efdeed3c7a1326dc9c3c6c6)`(const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const distrib)` {#classshogun_1_1CTrie_1a827691bb2efdeed3c7a1326dc9c3c6c6}

#### `public template<>`  <br/>`void `[`POIMs_get_SLR`](#classshogun_1_1CTrie_1a8b184d76faf9026a0e0a4f7069463c02)`(const int32_t parentIdx,const int32_t sym,const int32_t depth,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * S,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * L,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * R)` {#classshogun_1_1CTrie_1a8b184d76faf9026a0e0a4f7069463c02}

#### `public template<>`  <br/>`void `[`POIMs_add_SLR_helper2`](#classshogun_1_1CTrie_1ad392481f528265b599b38ac4e8748cd4)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const *const poims,const int32_t K,const int32_t k,const int32_t i,const int32_t y,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` valW,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` valS,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` valL,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` valR,const int32_t debug)` {#classshogun_1_1CTrie_1ad392481f528265b599b38ac4e8748cd4}

#### `public template<>`  <br/>`void `[`POIMs_add_SLR_helper1`](#classshogun_1_1CTrie_1a30c0e30f4625c437903d0a83705246e6)`(const int32_t nodeIdx,const int32_t depth,const int32_t i,const int32_t y0,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const *const poims,const int32_t K,const int32_t debug)` {#classshogun_1_1CTrie_1a30c0e30f4625c437903d0a83705246e6}

#### `public template<>`  <br/>`void `[`POIMs_add_SLR`](#classshogun_1_1CTrie_1a063ffffc29b1968a8c312a3729007b40)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` *const *const poims,const int32_t K,const int32_t debug)` {#classshogun_1_1CTrie_1a063ffffc29b1968a8c312a3729007b40}

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

#### `protected int32_t `[`length`](#classshogun_1_1CTrie_1a5ae5048776b1de2d7dce124f78dc300f) {#classshogun_1_1CTrie_1a5ae5048776b1de2d7dce124f78dc300f}

length

#### `protected int32_t * `[`trees`](#classshogun_1_1CTrie_1ae0079cae9635c82aa95e9b29f50b9193) {#classshogun_1_1CTrie_1ae0079cae9635c82aa95e9b29f50b9193}

trees

#### `protected int32_t `[`degree`](#classshogun_1_1CTrie_1a192432a474907a70b37aa10ddabc0c97) {#classshogun_1_1CTrie_1a192432a474907a70b37aa10ddabc0c97}

degree

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * `[`position_weights`](#classshogun_1_1CTrie_1a3db9cfc85326a0471076c3ca57e68e28) {#classshogun_1_1CTrie_1a3db9cfc85326a0471076c3ca57e68e28}

position weights

#### `protected Trie * `[`TreeMem`](#classshogun_1_1CTrie_1a80f3cea09ce6343de93bdeb2bd5e03a6) {#classshogun_1_1CTrie_1a80f3cea09ce6343de93bdeb2bd5e03a6}

tree memory

#### `protected int32_t `[`TreeMemPtr`](#classshogun_1_1CTrie_1a13d2b8afd8463f10d9a1f1b3266cd73b) {#classshogun_1_1CTrie_1a13d2b8afd8463f10d9a1f1b3266cd73b}

tree memory pointer

#### `protected int32_t `[`TreeMemPtrMax`](#classshogun_1_1CTrie_1a7832defb495918167ecdfa892d1ffe2a) {#classshogun_1_1CTrie_1a7832defb495918167ecdfa892d1ffe2a}

tree memory pointer maximum

#### `protected bool `[`use_compact_terminal_nodes`](#classshogun_1_1CTrie_1a9c8f4fae95027f1551b763a62f404cdb) {#classshogun_1_1CTrie_1a9c8f4fae95027f1551b763a62f404cdb}

if compact terminal nodes are used

#### `protected bool `[`weights_in_tree`](#classshogun_1_1CTrie_1ad3901a594bb455678f820fe476e3d4a6) {#classshogun_1_1CTrie_1ad3901a594bb455678f820fe476e3d4a6}

if weights are in tree

#### `protected int32_t * `[`nofsKmers`](#classshogun_1_1CTrie_1ada368866267ab1a41b1c643090dbf38f) {#classshogun_1_1CTrie_1ada368866267ab1a41b1c643090dbf38f}

nofsKmers

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

