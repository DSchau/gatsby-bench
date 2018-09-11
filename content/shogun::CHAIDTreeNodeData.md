---
classname: "shogun::CHAIDTreeNodeData"
type: "struct"
---

# struct `shogun::CHAIDTreeNodeData` {#structshogun_1_1CHAIDTreeNodeData}

structure to store data of a node of CHAID. This can be used as a template type in TreeMachineNode class. CHAID algorithm uses nodes of type [CTreeMachineNode<CHAIDTreeNodeData>](#classshogun_1_1CTreeMachineNode)

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public int32_t `[`attribute_id`](#structshogun_1_1CHAIDTreeNodeData_1a84d77d418084005e282778de4de04bd8) | classifying attribute
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`distinct_features`](#structshogun_1_1CHAIDTreeNodeData_1a0fb69af1770aee9c7097d2ed4107b23e) | distinct feature values possible for attribute_id
`public `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`feature_class`](#structshogun_1_1CHAIDTreeNodeData_1a3efa908c236bc759a558023b567a6331) | class to which each distinct feature type is assigned
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`node_label`](#structshogun_1_1CHAIDTreeNodeData_1adb89927da98a86dec0b928f02d38c65c) | label representative of data in node
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`total_weight`](#structshogun_1_1CHAIDTreeNodeData_1a31b2f1779930baf8ebde64d4d8878d17) | total weight of training samples passing through this node
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`weight_minus_node`](#structshogun_1_1CHAIDTreeNodeData_1afe27c215da765359e02f0a2e0024a631) | total weight of misclassified samples in node
`public inline  `[`CHAIDTreeNodeData`](#structshogun_1_1CHAIDTreeNodeData_1a47266a87fd5e7527c9411906907c47c2)`()` | constructor

## Members

#### `public int32_t `[`attribute_id`](#structshogun_1_1CHAIDTreeNodeData_1a84d77d418084005e282778de4de04bd8) {#structshogun_1_1CHAIDTreeNodeData_1a84d77d418084005e282778de4de04bd8}

classifying attribute

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`distinct_features`](#structshogun_1_1CHAIDTreeNodeData_1a0fb69af1770aee9c7097d2ed4107b23e) {#structshogun_1_1CHAIDTreeNodeData_1a0fb69af1770aee9c7097d2ed4107b23e}

distinct feature values possible for attribute_id

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< int32_t > `[`feature_class`](#structshogun_1_1CHAIDTreeNodeData_1a3efa908c236bc759a558023b567a6331) {#structshogun_1_1CHAIDTreeNodeData_1a3efa908c236bc759a558023b567a6331}

class to which each distinct feature type is assigned

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`node_label`](#structshogun_1_1CHAIDTreeNodeData_1adb89927da98a86dec0b928f02d38c65c) {#structshogun_1_1CHAIDTreeNodeData_1adb89927da98a86dec0b928f02d38c65c}

label representative of data in node

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`total_weight`](#structshogun_1_1CHAIDTreeNodeData_1a31b2f1779930baf8ebde64d4d8878d17) {#structshogun_1_1CHAIDTreeNodeData_1a31b2f1779930baf8ebde64d4d8878d17}

total weight of training samples passing through this node

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`weight_minus_node`](#structshogun_1_1CHAIDTreeNodeData_1afe27c215da765359e02f0a2e0024a631) {#structshogun_1_1CHAIDTreeNodeData_1afe27c215da765359e02f0a2e0024a631}

total weight of misclassified samples in node

#### `public inline  `[`CHAIDTreeNodeData`](#structshogun_1_1CHAIDTreeNodeData_1a47266a87fd5e7527c9411906907c47c2)`()` {#structshogun_1_1CHAIDTreeNodeData_1a47266a87fd5e7527c9411906907c47c2}

constructor

