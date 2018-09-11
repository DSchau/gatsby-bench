---
classname: "shogun::CTaxonomy"
type: "class"
---

# class `shogun::CTaxonomy` {#classshogun_1_1CTaxonomy}

[CTaxonomy](#classshogun_1_1CTaxonomy) is used to describe hierarchical structure between tasks.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public inline  `[`CTaxonomy`](#classshogun_1_1CTaxonomy_1a3ea76b903bb62b7cf99a0ef0ed38167a)`()` | default constructor
`public inline virtual  `[`~CTaxonomy`](#classshogun_1_1CTaxonomy_1a9097f7dd3db017f95c9abe7e4de3f924)`()` | 
`public inline `[`CNode`](#classshogun_1_1CNode)` * `[`get_node`](#classshogun_1_1CTaxonomy_1a53393b0c2e6280ae96d1f2fd30540a85)`(int32_t task_id)` | #### Parameters
`public inline void `[`set_root_beta`](#classshogun_1_1CTaxonomy_1a9b8e0b311dce16957f6742792ed359ff)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` beta)` | set root weight 
`public inline `[`CNode`](#classshogun_1_1CNode)` * `[`add_node`](#classshogun_1_1CTaxonomy_1a4211e6016ca1cd52073054b20f9c306b)`(std::string parent_name,std::string child_name,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` beta)` | inserts additional node into taxonomy 
`public inline int32_t `[`get_id`](#classshogun_1_1CTaxonomy_1a560c589915e169f8eb84c1b79510aff4)`(std::string name)` | translates name to id 
`public inline std::set< `[`CNode`](#classshogun_1_1CNode)` * > `[`intersect_root_path`](#classshogun_1_1CTaxonomy_1a8046a6bb98e3c47833d985a8c96909f4)`(`[`CNode`](#classshogun_1_1CNode)` * node_lhs,`[`CNode`](#classshogun_1_1CNode)` * node_rhs)` | given two nodes, compute the intersection of their ancestors 
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_node_similarity`](#classshogun_1_1CTaxonomy_1a03230572bf7dfb52d42365b06746ea2a)`(int32_t task_lhs,int32_t task_rhs)` | #### Parameters
`public inline void `[`update_task_histogram`](#classshogun_1_1CTaxonomy_1ab638b66978a9a512c7e9b590203c9507)`(std::vector< int32_t > task_vector_lhs)` | keep track of how many elements each task has 
`public inline int32_t `[`get_num_nodes`](#classshogun_1_1CTaxonomy_1a6e13225298fc2aff0c03240d906b7567)`()` | #### Returns
`public inline int32_t `[`get_num_leaves`](#classshogun_1_1CTaxonomy_1a56e2454dfd37f194b3dae1099fae8e87)`()` | #### Returns
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_node_weight`](#classshogun_1_1CTaxonomy_1a9fce7d1937501dcff9bb13888abbc28f)`(int32_t idx)` | #### Returns
`public inline void `[`set_node_weight`](#classshogun_1_1CTaxonomy_1ac1e79a4776f78b94d718d7179574a213)`(int32_t idx,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` weight)` | #### Parameters
`public inline virtual const char * `[`get_name`](#classshogun_1_1CTaxonomy_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` | #### Returns
`public inline std::map< std::string, int32_t > `[`get_name2id`](#classshogun_1_1CTaxonomy_1a026ebb458c69bf9770cdba5b85a0f4b3)`()` | #### Returns
`public inline int32_t `[`get_id_by_name`](#classshogun_1_1CTaxonomy_1a848c70b1868175c155da7b609f06e80f)`(std::string name)` | translate name to id 
`protected `[`CNode`](#classshogun_1_1CNode)` * `[`root`](#classshogun_1_1CTaxonomy_1a6a907739dfec790bf8aedc7794f20132) | root
`protected std::map< std::string, int32_t > `[`name2id`](#classshogun_1_1CTaxonomy_1a874a64f98fb6eaa1d979c9720cdfb162) | name 2 id
`protected std::vector< `[`CNode`](#classshogun_1_1CNode)` * > `[`nodes`](#classshogun_1_1CTaxonomy_1a45dc80d6a26f95151d9c61698e6f2d9b) | nodes
`protected std::map< int32_t, `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`task_histogram`](#classshogun_1_1CTaxonomy_1afc0b2abde30a34ddf2dd70b5285dd426) | task histogram

## Members

#### `public inline  `[`CTaxonomy`](#classshogun_1_1CTaxonomy_1a3ea76b903bb62b7cf99a0ef0ed38167a)`()` {#classshogun_1_1CTaxonomy_1a3ea76b903bb62b7cf99a0ef0ed38167a}

default constructor

#### `public inline virtual  `[`~CTaxonomy`](#classshogun_1_1CTaxonomy_1a9097f7dd3db017f95c9abe7e4de3f924)`()` {#classshogun_1_1CTaxonomy_1a9097f7dd3db017f95c9abe7e4de3f924}

#### `public inline `[`CNode`](#classshogun_1_1CNode)` * `[`get_node`](#classshogun_1_1CTaxonomy_1a53393b0c2e6280ae96d1f2fd30540a85)`(int32_t task_id)` {#classshogun_1_1CTaxonomy_1a53393b0c2e6280ae96d1f2fd30540a85}

#### Parameters
* `task_id` task identifier 

#### Returns
node with id task_id

#### `public inline void `[`set_root_beta`](#classshogun_1_1CTaxonomy_1a9b8e0b311dce16957f6742792ed359ff)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` beta)` {#classshogun_1_1CTaxonomy_1a9b8e0b311dce16957f6742792ed359ff}

set root weight 
#### Parameters
* `beta` weight

#### `public inline `[`CNode`](#classshogun_1_1CNode)` * `[`add_node`](#classshogun_1_1CTaxonomy_1a4211e6016ca1cd52073054b20f9c306b)`(std::string parent_name,std::string child_name,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` beta)` {#classshogun_1_1CTaxonomy_1a4211e6016ca1cd52073054b20f9c306b}

inserts additional node into taxonomy 
#### Parameters
* `parent_name` name of parent 

* `child_name` name of child 

* `beta` weight of child

#### `public inline int32_t `[`get_id`](#classshogun_1_1CTaxonomy_1a560c589915e169f8eb84c1b79510aff4)`(std::string name)` {#classshogun_1_1CTaxonomy_1a560c589915e169f8eb84c1b79510aff4}

translates name to id 
#### Parameters
* `name` name of task 

#### Returns
id

#### `public inline std::set< `[`CNode`](#classshogun_1_1CNode)` * > `[`intersect_root_path`](#classshogun_1_1CTaxonomy_1a8046a6bb98e3c47833d985a8c96909f4)`(`[`CNode`](#classshogun_1_1CNode)` * node_lhs,`[`CNode`](#classshogun_1_1CNode)` * node_rhs)` {#classshogun_1_1CTaxonomy_1a8046a6bb98e3c47833d985a8c96909f4}

given two nodes, compute the intersection of their ancestors 
#### Parameters
* `node_lhs` node of left hand side 

* `node_rhs` node of right hand side 

#### Returns
intersection of the two sets of ancestors

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`compute_node_similarity`](#classshogun_1_1CTaxonomy_1a03230572bf7dfb52d42365b06746ea2a)`(int32_t task_lhs,int32_t task_rhs)` {#classshogun_1_1CTaxonomy_1a03230572bf7dfb52d42365b06746ea2a}

#### Parameters
* `task_lhs` task_id on left hand side 

* `task_rhs` task_id on right hand side 

#### Returns
similarity between tasks

#### `public inline void `[`update_task_histogram`](#classshogun_1_1CTaxonomy_1ab638b66978a9a512c7e9b590203c9507)`(std::vector< int32_t > task_vector_lhs)` {#classshogun_1_1CTaxonomy_1ab638b66978a9a512c7e9b590203c9507}

keep track of how many elements each task has 
#### Parameters
* `task_vector_lhs` vector of task ids for examples

#### `public inline int32_t `[`get_num_nodes`](#classshogun_1_1CTaxonomy_1a6e13225298fc2aff0c03240d906b7567)`()` {#classshogun_1_1CTaxonomy_1a6e13225298fc2aff0c03240d906b7567}

#### Returns
number of nodes

#### `public inline int32_t `[`get_num_leaves`](#classshogun_1_1CTaxonomy_1a56e2454dfd37f194b3dae1099fae8e87)`()` {#classshogun_1_1CTaxonomy_1a56e2454dfd37f194b3dae1099fae8e87}

#### Returns
number of leaves

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_node_weight`](#classshogun_1_1CTaxonomy_1a9fce7d1937501dcff9bb13888abbc28f)`(int32_t idx)` {#classshogun_1_1CTaxonomy_1a9fce7d1937501dcff9bb13888abbc28f}

#### Returns
weight of node with identifier idx

#### `public inline void `[`set_node_weight`](#classshogun_1_1CTaxonomy_1ac1e79a4776f78b94d718d7179574a213)`(int32_t idx,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` weight)` {#classshogun_1_1CTaxonomy_1ac1e79a4776f78b94d718d7179574a213}

#### Parameters
* `idx` node id 

* `weight` weight to set

#### `public inline virtual const char * `[`get_name`](#classshogun_1_1CTaxonomy_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` {#classshogun_1_1CTaxonomy_1a9cb485686dd7a1e6f7103cf42e87717e}

#### Returns
object name

#### `public inline std::map< std::string, int32_t > `[`get_name2id`](#classshogun_1_1CTaxonomy_1a026ebb458c69bf9770cdba5b85a0f4b3)`()` {#classshogun_1_1CTaxonomy_1a026ebb458c69bf9770cdba5b85a0f4b3}

#### Returns
mapping from name to id

#### `public inline int32_t `[`get_id_by_name`](#classshogun_1_1CTaxonomy_1a848c70b1868175c155da7b609f06e80f)`(std::string name)` {#classshogun_1_1CTaxonomy_1a848c70b1868175c155da7b609f06e80f}

translate name to id 
#### Parameters
* `name` node name 

#### Returns
id

#### `protected `[`CNode`](#classshogun_1_1CNode)` * `[`root`](#classshogun_1_1CTaxonomy_1a6a907739dfec790bf8aedc7794f20132) {#classshogun_1_1CTaxonomy_1a6a907739dfec790bf8aedc7794f20132}

root

#### `protected std::map< std::string, int32_t > `[`name2id`](#classshogun_1_1CTaxonomy_1a874a64f98fb6eaa1d979c9720cdfb162) {#classshogun_1_1CTaxonomy_1a874a64f98fb6eaa1d979c9720cdfb162}

name 2 id

#### `protected std::vector< `[`CNode`](#classshogun_1_1CNode)` * > `[`nodes`](#classshogun_1_1CTaxonomy_1a45dc80d6a26f95151d9c61698e6f2d9b) {#classshogun_1_1CTaxonomy_1a45dc80d6a26f95151d9c61698e6f2d9b}

nodes

#### `protected std::map< int32_t, `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`task_histogram`](#classshogun_1_1CTaxonomy_1afc0b2abde30a34ddf2dd70b5285dd426) {#classshogun_1_1CTaxonomy_1afc0b2abde30a34ddf2dd70b5285dd426}

task histogram

