---
classname: "shogun::GCNode"
type: "struct"
---

# struct `shogun::GCNode` {#structshogun_1_1GCNode}

Graph cuts node.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public int32_t `[`id`](#structshogun_1_1GCNode_1a2708c0bbb6f926149707c2c61fe43c3e) | node id
`public `[`GCEdge`](#structshogun_1_1GCEdge)` * `[`first`](#structshogun_1_1GCNode_1a42cfdbade8fc1dd0df1c99c95c8c424e) | first outcoming edge
`public `[`GCEdge`](#structshogun_1_1GCEdge)` * `[`parent`](#structshogun_1_1GCNode_1a05d6357bcf7adbdf46f96474798e1350) | node's parent
`public `[`GCNode`](#structshogun_1_1GCNode)` * `[`next`](#structshogun_1_1GCNode_1a5966991b3612582b6f8961ce226270ad) | pointer to the next active node (or itself if it is the last node in the list)
`public int32_t `[`timestamp`](#structshogun_1_1GCNode_1af424c5c51376cd09eb214ebec28e933d) | timestamp showing when dist_to_terminal was computed
`public int32_t `[`dist_terminal`](#structshogun_1_1GCNode_1aa5910641dcc1367711517a84e2302dd6) | distance to the terminal
`public `[`ETerminalType`](#namespaceshogun_1aed1bf962e9ccb8a673943d0880920d24)` `[`type_tree`](#structshogun_1_1GCNode_1aa316fdd57419a45572bdbb2bbd438afc) | the type of the tree that the node belongs to
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`tree_cap`](#structshogun_1_1GCNode_1a5ac11fcf0583521c9e6a394465e67f16) | if tree_cap > 0 then tree_cap is residual capacity of the edge SOURCE->node otherwise -tree_cap is residual capacity of the edge node->SINK

## Members

#### `public int32_t `[`id`](#structshogun_1_1GCNode_1a2708c0bbb6f926149707c2c61fe43c3e) {#structshogun_1_1GCNode_1a2708c0bbb6f926149707c2c61fe43c3e}

node id

#### `public `[`GCEdge`](#structshogun_1_1GCEdge)` * `[`first`](#structshogun_1_1GCNode_1a42cfdbade8fc1dd0df1c99c95c8c424e) {#structshogun_1_1GCNode_1a42cfdbade8fc1dd0df1c99c95c8c424e}

first outcoming edge

#### `public `[`GCEdge`](#structshogun_1_1GCEdge)` * `[`parent`](#structshogun_1_1GCNode_1a05d6357bcf7adbdf46f96474798e1350) {#structshogun_1_1GCNode_1a05d6357bcf7adbdf46f96474798e1350}

node's parent

#### `public `[`GCNode`](#structshogun_1_1GCNode)` * `[`next`](#structshogun_1_1GCNode_1a5966991b3612582b6f8961ce226270ad) {#structshogun_1_1GCNode_1a5966991b3612582b6f8961ce226270ad}

pointer to the next active node (or itself if it is the last node in the list)

#### `public int32_t `[`timestamp`](#structshogun_1_1GCNode_1af424c5c51376cd09eb214ebec28e933d) {#structshogun_1_1GCNode_1af424c5c51376cd09eb214ebec28e933d}

timestamp showing when dist_to_terminal was computed

#### `public int32_t `[`dist_terminal`](#structshogun_1_1GCNode_1aa5910641dcc1367711517a84e2302dd6) {#structshogun_1_1GCNode_1aa5910641dcc1367711517a84e2302dd6}

distance to the terminal

#### `public `[`ETerminalType`](#namespaceshogun_1aed1bf962e9ccb8a673943d0880920d24)` `[`type_tree`](#structshogun_1_1GCNode_1aa316fdd57419a45572bdbb2bbd438afc) {#structshogun_1_1GCNode_1aa316fdd57419a45572bdbb2bbd438afc}

the type of the tree that the node belongs to

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`tree_cap`](#structshogun_1_1GCNode_1a5ac11fcf0583521c9e6a394465e67f16) {#structshogun_1_1GCNode_1a5ac11fcf0583521c9e6a394465e67f16}

if tree_cap > 0 then tree_cap is residual capacity of the edge SOURCE->node otherwise -tree_cap is residual capacity of the edge node->SINK

