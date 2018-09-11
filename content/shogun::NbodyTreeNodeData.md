---
classname: "shogun::NbodyTreeNodeData"
type: "struct"
---

# struct `shogun::NbodyTreeNodeData` {#structshogun_1_1NbodyTreeNodeData}

structure to store data of a node of N-Body tree. This can be used as a template type in TreeMachineNode class. N-Body tree building algorithm uses nodes of type CBinaryTreeMachineNode<NbodyTreeNodeData>

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`start_idx`](#structshogun_1_1NbodyTreeNodeData_1aecfc88c392561f70c1a074ee626bec6d) | start index
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`end_idx`](#structshogun_1_1NbodyTreeNodeData_1ad78afe33896205f618297cf54646312c) | end index
`public bool `[`is_leaf`](#structshogun_1_1NbodyTreeNodeData_1ab10fefeff0f06c67fe931f011449e3e5) | is leaf
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`bbox_upper`](#structshogun_1_1NbodyTreeNodeData_1abcf32504ec567d8fed3aee070b9c9c29) | bounding box upper bounds (in ball tree used only for fast calculation of max spread dimension)
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`bbox_lower`](#structshogun_1_1NbodyTreeNodeData_1acca0b509857d1dd170c3748a2fa82159) | bounding box lower bounds (in ball tree used only for fast calculation of max spread dimension)
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`radius`](#structshogun_1_1NbodyTreeNodeData_1aa033ea50999cc30efb5f00d65a685eba) | radius of point cloud in node
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`center`](#structshogun_1_1NbodyTreeNodeData_1aff41673ced693c954847467382114f80) | node center - used only in ball tree
`public inline  `[`NbodyTreeNodeData`](#structshogun_1_1NbodyTreeNodeData_1a3fbcda564f0d673dbaeeb162e7f28a25)`()` | constructor

## Members

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`start_idx`](#structshogun_1_1NbodyTreeNodeData_1aecfc88c392561f70c1a074ee626bec6d) {#structshogun_1_1NbodyTreeNodeData_1aecfc88c392561f70c1a074ee626bec6d}

start index

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`end_idx`](#structshogun_1_1NbodyTreeNodeData_1ad78afe33896205f618297cf54646312c) {#structshogun_1_1NbodyTreeNodeData_1ad78afe33896205f618297cf54646312c}

end index

#### `public bool `[`is_leaf`](#structshogun_1_1NbodyTreeNodeData_1ab10fefeff0f06c67fe931f011449e3e5) {#structshogun_1_1NbodyTreeNodeData_1ab10fefeff0f06c67fe931f011449e3e5}

is leaf

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`bbox_upper`](#structshogun_1_1NbodyTreeNodeData_1abcf32504ec567d8fed3aee070b9c9c29) {#structshogun_1_1NbodyTreeNodeData_1abcf32504ec567d8fed3aee070b9c9c29}

bounding box upper bounds (in ball tree used only for fast calculation of max spread dimension)

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`bbox_lower`](#structshogun_1_1NbodyTreeNodeData_1acca0b509857d1dd170c3748a2fa82159) {#structshogun_1_1NbodyTreeNodeData_1acca0b509857d1dd170c3748a2fa82159}

bounding box lower bounds (in ball tree used only for fast calculation of max spread dimension)

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`radius`](#structshogun_1_1NbodyTreeNodeData_1aa033ea50999cc30efb5f00d65a685eba) {#structshogun_1_1NbodyTreeNodeData_1aa033ea50999cc30efb5f00d65a685eba}

radius of point cloud in node

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`center`](#structshogun_1_1NbodyTreeNodeData_1aff41673ced693c954847467382114f80) {#structshogun_1_1NbodyTreeNodeData_1aff41673ced693c954847467382114f80}

node center - used only in ball tree

#### `public inline  `[`NbodyTreeNodeData`](#structshogun_1_1NbodyTreeNodeData_1a3fbcda564f0d673dbaeeb162e7f28a25)`()` {#structshogun_1_1NbodyTreeNodeData_1a3fbcda564f0d673dbaeeb162e7f28a25}

constructor

