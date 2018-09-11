---
classname: "shogun::C45TreeNodeData"
type: "struct"
---

# struct `shogun::C45TreeNodeData` {#structshogun_1_1C45TreeNodeData}

structure to store data of a node of C4.5 tree. This can be used as a template type in TreeMachineNode class. Ex: C4.5 algorithm uses nodes of type [CTreeMachineNode<C45TreeNodeData>](#classshogun_1_1CTreeMachineNode)

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public int32_t `[`attribute_id`](#structshogun_1_1C45TreeNodeData_1a84d77d418084005e282778de4de04bd8) | classifying attribute
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`transit_if_feature_value`](#structshogun_1_1C45TreeNodeData_1a27d9d0ceb25ac0d43be0c85433ff01df) | feature value required to move into this node
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`class_label`](#structshogun_1_1C45TreeNodeData_1a3e6d33f238e61b366f07f678fd89c374) | class label of data (-1 for internal nodes)
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`total_weight`](#structshogun_1_1C45TreeNodeData_1a31b2f1779930baf8ebde64d4d8878d17) | weight of all samples present in the node during training
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`weight_minus`](#structshogun_1_1C45TreeNodeData_1a48ecc992bab19dcc840b10953c161886) | weight of all samples present in the node during training not belonging to class_label class
`public inline  `[`C45TreeNodeData`](#structshogun_1_1C45TreeNodeData_1a7ebe3a1292eab8270cdc499c68b621e7)`()` | constructor

## Members

#### `public int32_t `[`attribute_id`](#structshogun_1_1C45TreeNodeData_1a84d77d418084005e282778de4de04bd8) {#structshogun_1_1C45TreeNodeData_1a84d77d418084005e282778de4de04bd8}

classifying attribute

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`transit_if_feature_value`](#structshogun_1_1C45TreeNodeData_1a27d9d0ceb25ac0d43be0c85433ff01df) {#structshogun_1_1C45TreeNodeData_1a27d9d0ceb25ac0d43be0c85433ff01df}

feature value required to move into this node

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`class_label`](#structshogun_1_1C45TreeNodeData_1a3e6d33f238e61b366f07f678fd89c374) {#structshogun_1_1C45TreeNodeData_1a3e6d33f238e61b366f07f678fd89c374}

class label of data (-1 for internal nodes)

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`total_weight`](#structshogun_1_1C45TreeNodeData_1a31b2f1779930baf8ebde64d4d8878d17) {#structshogun_1_1C45TreeNodeData_1a31b2f1779930baf8ebde64d4d8878d17}

weight of all samples present in the node during training

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`weight_minus`](#structshogun_1_1C45TreeNodeData_1a48ecc992bab19dcc840b10953c161886) {#structshogun_1_1C45TreeNodeData_1a48ecc992bab19dcc840b10953c161886}

weight of all samples present in the node during training not belonging to class_label class

#### `public inline  `[`C45TreeNodeData`](#structshogun_1_1C45TreeNodeData_1a7ebe3a1292eab8270cdc499c68b621e7)`()` {#structshogun_1_1C45TreeNodeData_1a7ebe3a1292eab8270cdc499c68b621e7}

constructor

