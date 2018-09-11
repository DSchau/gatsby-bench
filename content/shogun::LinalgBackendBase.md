---
classname: "shogun::LinalgBackendBase"
type: "class"
---

# class `shogun::LinalgBackendBase` {#classshogun_1_1LinalgBackendBase}

Base interface of generic linalg methods and generic memory transfer methods.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public  `[`DEFINE_FOR_ALL_PTYPE`](#classshogun_1_1LinalgBackendBase_1a261e66c21283cc37de965565a3c9f52b)`(`[`BACKEND_GENERIC_ADD_DIAG`](#LinalgBackendEigen_8h_1a87832a810fda33d3dbdb38a63b55cfbb)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` | 
`public  `[`DEFINE_FOR_ALL_PTYPE`](#classshogun_1_1LinalgBackendBase_1a2254641e8daa408e79cdd199cc8ae3a0)`(`[`BACKEND_GENERIC_ADD_RIDGE`](#LinalgBackendEigen_8h_1a933cb2066b0f13442c6cdcfc9a1111f9)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` | 
`public  `[`DEFINE_FOR_NON_INTEGER_PTYPE`](#classshogun_1_1LinalgBackendBase_1a2c0c95141ff102f773fefdf52a56c855)`(`[`BACKEND_GENERIC_EIGEN_SOLVER_SYMMETRIC`](#LinalgBackendEigen_8h_1a552da5c11cf37943b028d1b144348bb5)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` | [Wrapper](#classWrapper) method of in-place vector elementwise product.
`public  `[`DEFINE_FOR_ALL_PTYPE`](#classshogun_1_1LinalgBackendBase_1a7279fddb01a18ea5460deba07aca208a)`(`[`BACKEND_GENERIC_IN_PLACE_MATRIX_ELEMENT_PROD`](#LinalgBackendEigen_8h_1acc37c92fcd41745a264c0bed8f2dbc39)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` | [Wrapper](#classWrapper) method of in-place matrix block elementwise product.
`public  `[`DEFINE_FOR_ALL_PTYPE`](#classshogun_1_1LinalgBackendBase_1adeee2ca24d7cf6627c7d7e92feee88c5)`(`[`BACKEND_GENERIC_MULTIPLY_BY_LOGISTIC_DERIV`](#LinalgBackendEigen_8h_1acf6e1f42783459111138470543074067)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` | [Wrapper](#classWrapper) method of multiply_by_rectified_linear_derivative
`public  `[`DEFINE_FOR_NON_INTEGER_PTYPE`](#classshogun_1_1LinalgBackendBase_1afa5189ae572a610cc569755121d0def7)`(`[`BACKEND_GENERIC_TRIANGULAR_SOLVER`](#LinalgBackendEigen_8h_1aa485a2f1c1369303b2e5a4e5d62bb978)`,`[`SGVector`](#classshogun_1_1SGVector)`)` | 

## Members

#### `public  `[`DEFINE_FOR_ALL_PTYPE`](#classshogun_1_1LinalgBackendBase_1a261e66c21283cc37de965565a3c9f52b)`(`[`BACKEND_GENERIC_ADD_DIAG`](#LinalgBackendEigen_8h_1a87832a810fda33d3dbdb38a63b55cfbb)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` {#classshogun_1_1LinalgBackendBase_1a261e66c21283cc37de965565a3c9f52b}

#### `public  `[`DEFINE_FOR_ALL_PTYPE`](#classshogun_1_1LinalgBackendBase_1a2254641e8daa408e79cdd199cc8ae3a0)`(`[`BACKEND_GENERIC_ADD_RIDGE`](#LinalgBackendEigen_8h_1a933cb2066b0f13442c6cdcfc9a1111f9)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` {#classshogun_1_1LinalgBackendBase_1a2254641e8daa408e79cdd199cc8ae3a0}

#### `public  `[`DEFINE_FOR_NON_INTEGER_PTYPE`](#classshogun_1_1LinalgBackendBase_1a2c0c95141ff102f773fefdf52a56c855)`(`[`BACKEND_GENERIC_EIGEN_SOLVER_SYMMETRIC`](#LinalgBackendEigen_8h_1a552da5c11cf37943b028d1b144348bb5)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` {#classshogun_1_1LinalgBackendBase_1a2c0c95141ff102f773fefdf52a56c855}

[Wrapper](#classWrapper) method of in-place vector elementwise product.

**See also**: [linalg::element_prod](#namespaceshogun_1_1linalg_1a0fb476f802c6ae03c6927ec6bfad695b)

#### `public  `[`DEFINE_FOR_ALL_PTYPE`](#classshogun_1_1LinalgBackendBase_1a7279fddb01a18ea5460deba07aca208a)`(`[`BACKEND_GENERIC_IN_PLACE_MATRIX_ELEMENT_PROD`](#LinalgBackendEigen_8h_1acc37c92fcd41745a264c0bed8f2dbc39)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` {#classshogun_1_1LinalgBackendBase_1a7279fddb01a18ea5460deba07aca208a}

[Wrapper](#classWrapper) method of in-place matrix block elementwise product.

**See also**: [linalg::element_prod](#namespaceshogun_1_1linalg_1a0fb476f802c6ae03c6927ec6bfad695b)

#### `public  `[`DEFINE_FOR_ALL_PTYPE`](#classshogun_1_1LinalgBackendBase_1adeee2ca24d7cf6627c7d7e92feee88c5)`(`[`BACKEND_GENERIC_MULTIPLY_BY_LOGISTIC_DERIV`](#LinalgBackendEigen_8h_1acf6e1f42783459111138470543074067)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` {#classshogun_1_1LinalgBackendBase_1adeee2ca24d7cf6627c7d7e92feee88c5}

[Wrapper](#classWrapper) method of multiply_by_rectified_linear_derivative

**See also**: [linalg::multiply_by_rectified_linear_derivative](#namespaceshogun_1_1linalg_1ae5bb06ce8c045e1ba15656aa51188b61)

#### `public  `[`DEFINE_FOR_NON_INTEGER_PTYPE`](#classshogun_1_1LinalgBackendBase_1afa5189ae572a610cc569755121d0def7)`(`[`BACKEND_GENERIC_TRIANGULAR_SOLVER`](#LinalgBackendEigen_8h_1aa485a2f1c1369303b2e5a4e5d62bb978)`,`[`SGVector`](#classshogun_1_1SGVector)`)` {#classshogun_1_1LinalgBackendBase_1afa5189ae572a610cc569755121d0def7}

