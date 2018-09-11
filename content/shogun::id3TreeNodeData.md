---
classname: "shogun::id3TreeNodeData"
type: "struct"
---

# struct `shogun::id3TreeNodeData` {#structshogun_1_1id3TreeNodeData}

structure to store data of a node of id3 tree. This can be used as a template type in TreeMachineNode class. Ex: id3 algorithm uses nodes of type [CTreeMachineNode<id3TreeNodeData>](#classshogun_1_1CTreeMachineNode)

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public int32_t `[`attribute_id`](#structshogun_1_1id3TreeNodeData_1a84d77d418084005e282778de4de04bd8) | classifying attribute
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`transit_if_feature_value`](#structshogun_1_1id3TreeNodeData_1a27d9d0ceb25ac0d43be0c85433ff01df) | feature value required to move into this node
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`class_label`](#structshogun_1_1id3TreeNodeData_1a3e6d33f238e61b366f07f678fd89c374) | class label of data (-1 for internal nodes)
`public inline  `[`id3TreeNodeData`](#structshogun_1_1id3TreeNodeData_1aa8d6f64605c039e2673dc33b8172602f)`()` | constructor

## Members

#### `public int32_t `[`attribute_id`](#structshogun_1_1id3TreeNodeData_1a84d77d418084005e282778de4de04bd8) {#structshogun_1_1id3TreeNodeData_1a84d77d418084005e282778de4de04bd8}

classifying attribute

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`transit_if_feature_value`](#structshogun_1_1id3TreeNodeData_1a27d9d0ceb25ac0d43be0c85433ff01df) {#structshogun_1_1id3TreeNodeData_1a27d9d0ceb25ac0d43be0c85433ff01df}

feature value required to move into this node

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`class_label`](#structshogun_1_1id3TreeNodeData_1a3e6d33f238e61b366f07f678fd89c374) {#structshogun_1_1id3TreeNodeData_1a3e6d33f238e61b366f07f678fd89c374}

class label of data (-1 for internal nodes)

#### `public inline  `[`id3TreeNodeData`](#structshogun_1_1id3TreeNodeData_1aa8d6f64605c039e2673dc33b8172602f)`()` {#structshogun_1_1id3TreeNodeData_1aa8d6f64605c039e2673dc33b8172602f}

constructor

