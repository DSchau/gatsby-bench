---
classname: "shogun::linalg::operations::ocl_operation"
type: "class"
---

# class `shogun::linalg::operations::ocl_operation` {#classshogun_1_1linalg_1_1operations_1_1ocl__operation}

class [ocl_operation](#classshogun_1_1linalg_1_1operations_1_1ocl__operation) for element-wise unary OpenCL operations for GPU-types (CGPUMatrix/CGPUVector).

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public inline  `[`ocl_operation`](#classshogun_1_1linalg_1_1operations_1_1ocl__operation_1a9a38d95f6f5debb52fc3de77dceb812b)`(std::string operation)` | Constructor 
`public inline std::string `[`get_operation`](#classshogun_1_1linalg_1_1operations_1_1ocl__operation_1ae87e57a8a0f00180233ca2e23eabf23a)`() const` | #### Returns

## Members

#### `public inline  `[`ocl_operation`](#classshogun_1_1linalg_1_1operations_1_1ocl__operation_1a9a38d95f6f5debb52fc3de77dceb812b)`(std::string operation)` {#classshogun_1_1linalg_1_1operations_1_1ocl__operation_1a9a38d95f6f5debb52fc3de77dceb812b}

Constructor 
#### Parameters
* `operation` The unary operation string. The current element has to be refered as "element".

#### `public inline std::string `[`get_operation`](#classshogun_1_1linalg_1_1operations_1_1ocl__operation_1ae87e57a8a0f00180233ca2e23eabf23a)`() const` {#classshogun_1_1linalg_1_1operations_1_1ocl__operation_1ae87e57a8a0f00180233ca2e23eabf23a}

#### Returns
The OpenCL operation to be used in a OpenCL kernel

