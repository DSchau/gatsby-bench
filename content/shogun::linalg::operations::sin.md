---
classname: "shogun::linalg::operations::sin"
type: "struct"
parents:
   - ocl_operation
---

# struct `shogun::linalg::operations::sin` {#structshogun_1_1linalg_1_1operations_1_1sin}

```
struct shogun::linalg::operations::sin
  : public ocl_operation
```

Template struct sin for computing element-wise sin for matrices and vectors. The operator() is for NATIVE backend implementation. Methods compute_using_eigen3 are for computing element-wise sin using EIGEN3 backend.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public inline  `[`sin`](#structshogun_1_1linalg_1_1operations_1_1sin_1ac87d8aa2f8d991fa0aa633ddb5708d78)`()` | 
`public inline `[`return_type`](#structshogun_1_1linalg_1_1operations_1_1sin_1adcd3885e7ca42983ef8e08e77a1b695f)` `[`operator()`](#structshogun_1_1linalg_1_1operations_1_1sin_1a080f9da6a32688517a4012dd5b0b1618)`(T & val) const` | #### Parameters
`public inline `[`Eigen::MatrixXd`](#namespaceEigen_1a955270f233a3db6bd4db13f1930f16ce)` `[`compute_using_eigen3`](#structshogun_1_1linalg_1_1operations_1_1sin_1a568b44a99cd45ae23bc4f6af1d8991ee)`(`[`MapMatrixXt`](#structshogun_1_1linalg_1_1operations_1_1sin_1a01e7dd1c2e4fdbf73a4d77ec540b61dc)` m) const` | #### Parameters
`public inline Eigen::VectorXd `[`compute_using_eigen3`](#structshogun_1_1linalg_1_1operations_1_1sin_1af077dbb8528bba750923ac4de7a1ba37)`(`[`MapVectorXt`](#structshogun_1_1linalg_1_1operations_1_1sin_1a74847acc6545e85094ae6724f858205f)` v) const` | #### Parameters
`public inline std::string `[`get_operation`](#classshogun_1_1linalg_1_1operations_1_1ocl__operation_1ae87e57a8a0f00180233ca2e23eabf23a)`() const` | #### Returns
`typedef `[`return_type`](#structshogun_1_1linalg_1_1operations_1_1sin_1adcd3885e7ca42983ef8e08e77a1b695f) | The return type
`typedef `[`MatrixXt`](#structshogun_1_1linalg_1_1operations_1_1sin_1a57b0f426b424e3db52a64081ae74ee80) | Eigen3 matrix type
`typedef `[`VectorXt`](#structshogun_1_1linalg_1_1operations_1_1sin_1ad3e7902edab83a87dd1e501a43f80742) | Eigen3 vector type
`typedef `[`MapMatrixXt`](#structshogun_1_1linalg_1_1operations_1_1sin_1a01e7dd1c2e4fdbf73a4d77ec540b61dc) | Eigen3 matrix map type
`typedef `[`MapVectorXt`](#structshogun_1_1linalg_1_1operations_1_1sin_1a74847acc6545e85094ae6724f858205f) | Eigen3 vector map type

## Members

#### `public inline  `[`sin`](#structshogun_1_1linalg_1_1operations_1_1sin_1ac87d8aa2f8d991fa0aa633ddb5708d78)`()` {#structshogun_1_1linalg_1_1operations_1_1sin_1ac87d8aa2f8d991fa0aa633ddb5708d78}

#### `public inline `[`return_type`](#structshogun_1_1linalg_1_1operations_1_1sin_1adcd3885e7ca42983ef8e08e77a1b695f)` `[`operator()`](#structshogun_1_1linalg_1_1operations_1_1sin_1a080f9da6a32688517a4012dd5b0b1618)`(T & val) const` {#structshogun_1_1linalg_1_1operations_1_1sin_1a080f9da6a32688517a4012dd5b0b1618}

#### Parameters
* `val` The scalar value 

#### Returns
sin(val)

#### `public inline `[`Eigen::MatrixXd`](#namespaceEigen_1a955270f233a3db6bd4db13f1930f16ce)` `[`compute_using_eigen3`](#structshogun_1_1linalg_1_1operations_1_1sin_1a568b44a99cd45ae23bc4f6af1d8991ee)`(`[`MapMatrixXt`](#structshogun_1_1linalg_1_1operations_1_1sin_1a01e7dd1c2e4fdbf73a4d77ec540b61dc)` m) const` {#structshogun_1_1linalg_1_1operations_1_1sin_1a568b44a99cd45ae23bc4f6af1d8991ee}

#### Parameters
* `m` The Eigen3 matrix map of the operand 

#### Returns
Element-wise sin in a newly allocated matrix

#### `public inline Eigen::VectorXd `[`compute_using_eigen3`](#structshogun_1_1linalg_1_1operations_1_1sin_1af077dbb8528bba750923ac4de7a1ba37)`(`[`MapVectorXt`](#structshogun_1_1linalg_1_1operations_1_1sin_1a74847acc6545e85094ae6724f858205f)` v) const` {#structshogun_1_1linalg_1_1operations_1_1sin_1af077dbb8528bba750923ac4de7a1ba37}

#### Parameters
* `v` The Eigen3 vector map of the operand 

#### Returns
Element-wise sin in a newly allocated vector

#### `public inline std::string `[`get_operation`](#classshogun_1_1linalg_1_1operations_1_1ocl__operation_1ae87e57a8a0f00180233ca2e23eabf23a)`() const` {#classshogun_1_1linalg_1_1operations_1_1ocl__operation_1ae87e57a8a0f00180233ca2e23eabf23a}

#### Returns
The OpenCL operation to be used in a OpenCL kernel

#### `typedef `[`return_type`](#structshogun_1_1linalg_1_1operations_1_1sin_1adcd3885e7ca42983ef8e08e77a1b695f) {#structshogun_1_1linalg_1_1operations_1_1sin_1adcd3885e7ca42983ef8e08e77a1b695f}

The return type

#### `typedef `[`MatrixXt`](#structshogun_1_1linalg_1_1operations_1_1sin_1a57b0f426b424e3db52a64081ae74ee80) {#structshogun_1_1linalg_1_1operations_1_1sin_1a57b0f426b424e3db52a64081ae74ee80}

Eigen3 matrix type

#### `typedef `[`VectorXt`](#structshogun_1_1linalg_1_1operations_1_1sin_1ad3e7902edab83a87dd1e501a43f80742) {#structshogun_1_1linalg_1_1operations_1_1sin_1ad3e7902edab83a87dd1e501a43f80742}

Eigen3 vector type

#### `typedef `[`MapMatrixXt`](#structshogun_1_1linalg_1_1operations_1_1sin_1a01e7dd1c2e4fdbf73a4d77ec540b61dc) {#structshogun_1_1linalg_1_1operations_1_1sin_1a01e7dd1c2e4fdbf73a4d77ec540b61dc}

Eigen3 matrix map type

#### `typedef `[`MapVectorXt`](#structshogun_1_1linalg_1_1operations_1_1sin_1a74847acc6545e85094ae6724f858205f) {#structshogun_1_1linalg_1_1operations_1_1sin_1a74847acc6545e85094ae6724f858205f}

Eigen3 vector map type

