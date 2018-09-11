---
classname: "shogun::LinalgBackendEigen"
type: "class"
parents:
   - LinalgBackendBase
---

# class `shogun::LinalgBackendEigen` {#classshogun_1_1LinalgBackendEigen}

```
class shogun::LinalgBackendEigen
  : public LinalgBackendBase
```

Linalg methods with Eigen3 backend.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public  `[`DEFINE_FOR_NON_INTEGER_REAL_PTYPE`](#classshogun_1_1LinalgBackendEigen_1a213a2e7805a540945f8c8bd8192f2ebc)`(`[`BACKEND_GENERIC_CROSS_ENTROPY`](#LinalgBackendEigen_8h_1aa7b3e948a36e479ad371961761903afe)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` | Implementation of 
`public  `[`DEFINE_FOR_ALL_PTYPE`](#classshogun_1_1LinalgBackendEigen_1aea8ad4fe5003ad25b724105d41e83afd)`(`[`BACKEND_GENERIC_IN_PLACE_VECTOR_ELEMENT_PROD`](#LinalgBackendEigen_8h_1a8606892f97c92561af77d9f550526896)`,`[`SGVector`](#classshogun_1_1SGVector)`)` | Implementation of 
`public  `[`DEFINE_FOR_ALL_PTYPE`](#classshogun_1_1LinalgBackendEigen_1af32010393a803f16550aef5bed3d2bfc)`(`[`BACKEND_GENERIC_IN_PLACE_BLOCK_ELEMENT_PROD`](#LinalgBackendEigen_8h_1ae0596c15f4a7ae99bc6fda07e41599de)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` | Implementation of 
`public  `[`DEFINE_FOR_NON_INTEGER_REAL_PTYPE`](#classshogun_1_1LinalgBackendEigen_1a4f898d142078cbfbb2972cb33bcbd1df)`(`[`BACKEND_GENERIC_MULTIPLY_BY_RECTIFIED_LINEAR_DERIV`](#LinalgBackendEigen_8h_1a43f2ca68a06dd140c02f5b4ae5fe1d55)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` | Implementation of 
`public  `[`DEFINE_FOR_NON_INTEGER_PTYPE`](#classshogun_1_1LinalgBackendEigen_1afa5189ae572a610cc569755121d0def7)`(`[`BACKEND_GENERIC_TRIANGULAR_SOLVER`](#LinalgBackendEigen_8h_1aa485a2f1c1369303b2e5a4e5d62bb978)`,`[`SGVector`](#classshogun_1_1SGVector)`)` | 
`public  `[`DEFINE_FOR_ALL_PTYPE`](#classshogun_1_1LinalgBackendBase_1a261e66c21283cc37de965565a3c9f52b)`(`[`BACKEND_GENERIC_ADD_DIAG`](#LinalgBackendEigen_8h_1a87832a810fda33d3dbdb38a63b55cfbb)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` | 
`public  `[`DEFINE_FOR_ALL_PTYPE`](#classshogun_1_1LinalgBackendBase_1a2254641e8daa408e79cdd199cc8ae3a0)`(`[`BACKEND_GENERIC_ADD_RIDGE`](#LinalgBackendEigen_8h_1a933cb2066b0f13442c6cdcfc9a1111f9)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` | 
`public  `[`DEFINE_FOR_ALL_PTYPE`](#classshogun_1_1LinalgBackendBase_1a7279fddb01a18ea5460deba07aca208a)`(`[`BACKEND_GENERIC_IN_PLACE_MATRIX_ELEMENT_PROD`](#LinalgBackendEigen_8h_1acc37c92fcd41745a264c0bed8f2dbc39)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` | [Wrapper](#classWrapper) method of in-place matrix block elementwise product.
`public  `[`DEFINE_FOR_ALL_PTYPE`](#classshogun_1_1LinalgBackendBase_1adeee2ca24d7cf6627c7d7e92feee88c5)`(`[`BACKEND_GENERIC_MULTIPLY_BY_LOGISTIC_DERIV`](#LinalgBackendEigen_8h_1acf6e1f42783459111138470543074067)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` | [Wrapper](#classWrapper) method of multiply_by_rectified_linear_derivative
`public  `[`DEFINE_FOR_NON_INTEGER_PTYPE`](#classshogun_1_1LinalgBackendBase_1a2c0c95141ff102f773fefdf52a56c855)`(`[`BACKEND_GENERIC_EIGEN_SOLVER_SYMMETRIC`](#LinalgBackendEigen_8h_1a552da5c11cf37943b028d1b144348bb5)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` | [Wrapper](#classWrapper) method of in-place vector elementwise product.

## Members

#### `public  `[`DEFINE_FOR_NON_INTEGER_REAL_PTYPE`](#classshogun_1_1LinalgBackendEigen_1a213a2e7805a540945f8c8bd8192f2ebc)`(`[`BACKEND_GENERIC_CROSS_ENTROPY`](#LinalgBackendEigen_8h_1aa7b3e948a36e479ad371961761903afe)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` {#classshogun_1_1LinalgBackendEigen_1a213a2e7805a540945f8c8bd8192f2ebc}

Implementation of 
**See also**: LinalgBackendBase::dot Implementation of 

**See also**: LinalgBackendBase::eigen_solver Implementation of 

**See also**: LinalgBackendBase::eigen_solver_symmetric

#### `public  `[`DEFINE_FOR_ALL_PTYPE`](#classshogun_1_1LinalgBackendEigen_1aea8ad4fe5003ad25b724105d41e83afd)`(`[`BACKEND_GENERIC_IN_PLACE_VECTOR_ELEMENT_PROD`](#LinalgBackendEigen_8h_1a8606892f97c92561af77d9f550526896)`,`[`SGVector`](#classshogun_1_1SGVector)`)` {#classshogun_1_1LinalgBackendEigen_1aea8ad4fe5003ad25b724105d41e83afd}

Implementation of 
**See also**: LinalgBackendBase::element_prod

#### `public  `[`DEFINE_FOR_ALL_PTYPE`](#classshogun_1_1LinalgBackendEigen_1af32010393a803f16550aef5bed3d2bfc)`(`[`BACKEND_GENERIC_IN_PLACE_BLOCK_ELEMENT_PROD`](#LinalgBackendEigen_8h_1ae0596c15f4a7ae99bc6fda07e41599de)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` {#classshogun_1_1LinalgBackendEigen_1af32010393a803f16550aef5bed3d2bfc}

Implementation of 
**See also**: [linalg::exponent](#namespaceshogun_1_1linalg_1a75791b8e6af73823b814e2e2e1bc81ea) Implementation of 

**See also**: LinalgBackendBase::identity Implementation of 

**See also**: LinalgBackendBase::logistic Implementation of 

**See also**: LinalgBackendBase::matrix_prod Implementation of 

**See also**: LinalgBackendBase::max Implementation of 

**See also**: LinalgBackendBase::mean Implementation of 

**See also**: LinalgBackendBase::mean Implementation of 

**See also**: [linalg::multiply_by_logistic_derivative](#namespaceshogun_1_1linalg_1afbd5f881304c4b0b31174a37744138c3)

#### `public  `[`DEFINE_FOR_NON_INTEGER_REAL_PTYPE`](#classshogun_1_1LinalgBackendEigen_1a4f898d142078cbfbb2972cb33bcbd1df)`(`[`BACKEND_GENERIC_MULTIPLY_BY_RECTIFIED_LINEAR_DERIV`](#LinalgBackendEigen_8h_1a43f2ca68a06dd140c02f5b4ae5fe1d55)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` {#classshogun_1_1LinalgBackendEigen_1a4f898d142078cbfbb2972cb33bcbd1df}

Implementation of 
**See also**: LinalgBackendBase::qr_solver Implementation of 

**See also**: LinalgBackendBase::range_fill Implementation of 

**See also**: [linalg::rectified_linear](#namespaceshogun_1_1linalg_1a7e5ae33effbb01bb7f07846dee8a8580) Implementation of 

**See also**: [linalg::scale](#namespaceshogun_1_1linalg_1aad80c8710edc3edaf37de5273202fdcf) Implementation of 

**See also**: LinalgBackendBase::set_const Implementation of 

**See also**: [linalg::softmax](#namespaceshogun_1_1linalg_1ad43e523e54cb1fc01d3950c9272a7b9d) Implementation of 

**See also**: [linalg::squared_error](#namespaceshogun_1_1linalg_1aa3cbc453a341eb505aff0a114ceb1c1d)

#### `public  `[`DEFINE_FOR_NON_INTEGER_PTYPE`](#classshogun_1_1LinalgBackendEigen_1afa5189ae572a610cc569755121d0def7)`(`[`BACKEND_GENERIC_TRIANGULAR_SOLVER`](#LinalgBackendEigen_8h_1aa485a2f1c1369303b2e5a4e5d62bb978)`,`[`SGVector`](#classshogun_1_1SGVector)`)` {#classshogun_1_1LinalgBackendEigen_1afa5189ae572a610cc569755121d0def7}

#### `public  `[`DEFINE_FOR_ALL_PTYPE`](#classshogun_1_1LinalgBackendBase_1a261e66c21283cc37de965565a3c9f52b)`(`[`BACKEND_GENERIC_ADD_DIAG`](#LinalgBackendEigen_8h_1a87832a810fda33d3dbdb38a63b55cfbb)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` {#classshogun_1_1LinalgBackendBase_1a261e66c21283cc37de965565a3c9f52b}

#### `public  `[`DEFINE_FOR_ALL_PTYPE`](#classshogun_1_1LinalgBackendBase_1a2254641e8daa408e79cdd199cc8ae3a0)`(`[`BACKEND_GENERIC_ADD_RIDGE`](#LinalgBackendEigen_8h_1a933cb2066b0f13442c6cdcfc9a1111f9)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` {#classshogun_1_1LinalgBackendBase_1a2254641e8daa408e79cdd199cc8ae3a0}

#### `public  `[`DEFINE_FOR_ALL_PTYPE`](#classshogun_1_1LinalgBackendBase_1a7279fddb01a18ea5460deba07aca208a)`(`[`BACKEND_GENERIC_IN_PLACE_MATRIX_ELEMENT_PROD`](#LinalgBackendEigen_8h_1acc37c92fcd41745a264c0bed8f2dbc39)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` {#classshogun_1_1LinalgBackendBase_1a7279fddb01a18ea5460deba07aca208a}

[Wrapper](#classWrapper) method of in-place matrix block elementwise product.

**See also**: [linalg::element_prod](#namespaceshogun_1_1linalg_1a0fb476f802c6ae03c6927ec6bfad695b)

#### `public  `[`DEFINE_FOR_ALL_PTYPE`](#classshogun_1_1LinalgBackendBase_1adeee2ca24d7cf6627c7d7e92feee88c5)`(`[`BACKEND_GENERIC_MULTIPLY_BY_LOGISTIC_DERIV`](#LinalgBackendEigen_8h_1acf6e1f42783459111138470543074067)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` {#classshogun_1_1LinalgBackendBase_1adeee2ca24d7cf6627c7d7e92feee88c5}

[Wrapper](#classWrapper) method of multiply_by_rectified_linear_derivative

**See also**: [linalg::multiply_by_rectified_linear_derivative](#namespaceshogun_1_1linalg_1ae5bb06ce8c045e1ba15656aa51188b61)

#### `public  `[`DEFINE_FOR_NON_INTEGER_PTYPE`](#classshogun_1_1LinalgBackendBase_1a2c0c95141ff102f773fefdf52a56c855)`(`[`BACKEND_GENERIC_EIGEN_SOLVER_SYMMETRIC`](#LinalgBackendEigen_8h_1a552da5c11cf37943b028d1b144348bb5)`,`[`SGMatrix`](#classshogun_1_1SGMatrix)`)` {#classshogun_1_1LinalgBackendBase_1a2c0c95141ff102f773fefdf52a56c855}

[Wrapper](#classWrapper) method of in-place vector elementwise product.

**See also**: [linalg::element_prod](#namespaceshogun_1_1linalg_1a0fb476f802c6ae03c6927ec6bfad695b)

