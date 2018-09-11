---
classname: "shogun::GCEdge"
type: "struct"
---

# struct `shogun::GCEdge` {#structshogun_1_1GCEdge}

Graph cuts edge.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public int32_t `[`id`](#structshogun_1_1GCEdge_1a2708c0bbb6f926149707c2c61fe43c3e) | edge id
`public `[`GCNode`](#structshogun_1_1GCNode)` * `[`head`](#structshogun_1_1GCEdge_1a45f203c73bd047a34a26cc167badb6be) | node the edge point to
`public `[`GCEdge`](#structshogun_1_1GCEdge)` * `[`next`](#structshogun_1_1GCEdge_1abb1b314dccba7fbdd86296139cb1a1d9) | next edge with the same originated node
`public `[`GCEdge`](#structshogun_1_1GCEdge)` * `[`reverse`](#structshogun_1_1GCEdge_1a3360cde9944076d5222d93c62498bd51) | reverse edge
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`residual_capacity`](#structshogun_1_1GCEdge_1ad5bae1a0ba60c04407f8bac5b09e6f47) | residual capacity

## Members

#### `public int32_t `[`id`](#structshogun_1_1GCEdge_1a2708c0bbb6f926149707c2c61fe43c3e) {#structshogun_1_1GCEdge_1a2708c0bbb6f926149707c2c61fe43c3e}

edge id

#### `public `[`GCNode`](#structshogun_1_1GCNode)` * `[`head`](#structshogun_1_1GCEdge_1a45f203c73bd047a34a26cc167badb6be) {#structshogun_1_1GCEdge_1a45f203c73bd047a34a26cc167badb6be}

node the edge point to

#### `public `[`GCEdge`](#structshogun_1_1GCEdge)` * `[`next`](#structshogun_1_1GCEdge_1abb1b314dccba7fbdd86296139cb1a1d9) {#structshogun_1_1GCEdge_1abb1b314dccba7fbdd86296139cb1a1d9}

next edge with the same originated node

#### `public `[`GCEdge`](#structshogun_1_1GCEdge)` * `[`reverse`](#structshogun_1_1GCEdge_1a3360cde9944076d5222d93c62498bd51) {#structshogun_1_1GCEdge_1a3360cde9944076d5222d93c62498bd51}

reverse edge

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`residual_capacity`](#structshogun_1_1GCEdge_1ad5bae1a0ba60c04407f8bac5b09e6f47) {#structshogun_1_1GCEdge_1ad5bae1a0ba60c04407f8bac5b09e6f47}

residual capacity

