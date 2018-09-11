---
classname: "shogun::MixModelData"
type: "struct"
---

# struct `shogun::MixModelData` {#structshogun_1_1MixModelData}

This structure is used for storing data required for using the generic Expectation Maximization (EM) implemented by the template class [CEMBase](#classshogun_1_1CEMBase) for mixture models like gaussian mixture model, multinomial mixture model etc. The EM specialized for mixture models is implemented by the class [CEMMixtureModel](#classshogun_1_1CEMMixtureModel) which uses this [MixModelData](#structshogun_1_1MixModelData) structure.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`alpha`](#structshogun_1_1MixModelData_1afee45d2cb15d0a13e1516ef53c2cc97f) | allocated belongingness matrix
`public `[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` * `[`components`](#structshogun_1_1MixModelData_1a5c3ee698b95537e0978440a62f3989a9) | components of mixture
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`weights`](#structshogun_1_1MixModelData_1afb8fb3218650083b3c636dd12fdceacc) | weights of mixture
`public inline  `[`MixModelData`](#structshogun_1_1MixModelData_1ad8d72e0d2ff6af87c49c8ae8901dcc65)`()` | 

## Members

#### `public `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`alpha`](#structshogun_1_1MixModelData_1afee45d2cb15d0a13e1516ef53c2cc97f) {#structshogun_1_1MixModelData_1afee45d2cb15d0a13e1516ef53c2cc97f}

allocated belongingness matrix

#### `public `[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` * `[`components`](#structshogun_1_1MixModelData_1a5c3ee698b95537e0978440a62f3989a9) {#structshogun_1_1MixModelData_1a5c3ee698b95537e0978440a62f3989a9}

components of mixture

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`weights`](#structshogun_1_1MixModelData_1afb8fb3218650083b3c636dd12fdceacc) {#structshogun_1_1MixModelData_1afb8fb3218650083b3c636dd12fdceacc}

weights of mixture

#### `public inline  `[`MixModelData`](#structshogun_1_1MixModelData_1ad8d72e0d2ff6af87c49c8ae8901dcc65)`()` {#structshogun_1_1MixModelData_1ad8d72e0d2ff6af87c49c8ae8901dcc65}

