---
classname: "shogun::CARTreeNodeData"
type: "struct"
---

# struct `shogun::CARTreeNodeData` {#structshogun_1_1CARTreeNodeData}

structure to store data of a node of CART. This can be used as a template type in TreeMachineNode class. CART algorithm uses nodes of type [CTreeMachineNode<CARTreeNodeData>](#classshogun_1_1CTreeMachineNode)

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public int32_t `[`attribute_id`](#structshogun_1_1CARTreeNodeData_1a84d77d418084005e282778de4de04bd8) | classifying attribute
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`transit_into_values`](#structshogun_1_1CARTreeNodeData_1a12887d93e55d494ba036a61e879b4346) | feature value(s) required to move into this node
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`node_label`](#structshogun_1_1CARTreeNodeData_1adb89927da98a86dec0b928f02d38c65c) | classification/regression label of data
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`total_weight`](#structshogun_1_1CARTreeNodeData_1a31b2f1779930baf8ebde64d4d8878d17) | total weight of training samples passing through this node
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`weight_minus_node`](#structshogun_1_1CARTreeNodeData_1afe27c215da765359e02f0a2e0024a631) | total weight of misclassified samples in node/ weighted sum of squared deviation in case of regression
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`weight_minus_branch`](#structshogun_1_1CARTreeNodeData_1a12c9a7328ab728574161028dab894ad1) | total weight of misclassified samples in subtree/ weighted sum of squared deviation in case of regression
`public int32_t `[`num_leaves`](#structshogun_1_1CARTreeNodeData_1ac3b8bfb47f8997d551e4ba818baf894c) | number of leaves in the subtree beginning at this node
`public inline  `[`CARTreeNodeData`](#structshogun_1_1CARTreeNodeData_1a203abcfcb75517d9c3c75c828b958a21)`()` | constructor

## Members

#### `public int32_t `[`attribute_id`](#structshogun_1_1CARTreeNodeData_1a84d77d418084005e282778de4de04bd8) {#structshogun_1_1CARTreeNodeData_1a84d77d418084005e282778de4de04bd8}

classifying attribute

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`transit_into_values`](#structshogun_1_1CARTreeNodeData_1a12887d93e55d494ba036a61e879b4346) {#structshogun_1_1CARTreeNodeData_1a12887d93e55d494ba036a61e879b4346}

feature value(s) required to move into this node

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`node_label`](#structshogun_1_1CARTreeNodeData_1adb89927da98a86dec0b928f02d38c65c) {#structshogun_1_1CARTreeNodeData_1adb89927da98a86dec0b928f02d38c65c}

classification/regression label of data

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`total_weight`](#structshogun_1_1CARTreeNodeData_1a31b2f1779930baf8ebde64d4d8878d17) {#structshogun_1_1CARTreeNodeData_1a31b2f1779930baf8ebde64d4d8878d17}

total weight of training samples passing through this node

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`weight_minus_node`](#structshogun_1_1CARTreeNodeData_1afe27c215da765359e02f0a2e0024a631) {#structshogun_1_1CARTreeNodeData_1afe27c215da765359e02f0a2e0024a631}

total weight of misclassified samples in node/ weighted sum of squared deviation in case of regression

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`weight_minus_branch`](#structshogun_1_1CARTreeNodeData_1a12c9a7328ab728574161028dab894ad1) {#structshogun_1_1CARTreeNodeData_1a12c9a7328ab728574161028dab894ad1}

total weight of misclassified samples in subtree/ weighted sum of squared deviation in case of regression

#### `public int32_t `[`num_leaves`](#structshogun_1_1CARTreeNodeData_1ac3b8bfb47f8997d551e4ba818baf894c) {#structshogun_1_1CARTreeNodeData_1ac3b8bfb47f8997d551e4ba818baf894c}

number of leaves in the subtree beginning at this node

#### `public inline  `[`CARTreeNodeData`](#structshogun_1_1CARTreeNodeData_1a203abcfcb75517d9c3c75c828b958a21)`()` {#structshogun_1_1CARTreeNodeData_1a203abcfcb75517d9c3c75c828b958a21}

constructor

