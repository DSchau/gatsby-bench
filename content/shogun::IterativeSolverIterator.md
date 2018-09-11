---
classname: "shogun::IterativeSolverIterator"
type: "class"
---

# class `shogun::IterativeSolverIterator` {#classshogun_1_1IterativeSolverIterator}

template class that is used as an iterator for an iterative linear solver. In the iteration of solving phase, each solver initializes the iteration with a maximum number of iteration limit, and relative/ absolute tolerence. They then call begin with the residual vector and continue until its end returns true, i.e. either it has converged or iteration count reached maximum limit.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public inline  `[`IterativeSolverIterator`](#classshogun_1_1IterativeSolverIterator_1a367b9cc0323afaec8124d0f7312867ff)`(const `[`VectorXt`](#classEigen_1_1Matrix)` & b,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` max_iteration_limit,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` relative_tolerence,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` absolute_tolerence)` | constructor
`public inline void `[`begin`](#classshogun_1_1IterativeSolverIterator_1a5d6eb442bc6374e57dac6c0d191c341f)`(const `[`VectorXt`](#classEigen_1_1Matrix)` & residual)` | assign operator from an IterInfo
`public inline const bool `[`end`](#classshogun_1_1IterativeSolverIterator_1acae14e719e91bcdeda7fce7eab9db6a0)`(const `[`VectorXt`](#classEigen_1_1Matrix)` & residual)` | #### Returns
`public inline const `[`IterInfo`](#namespaceshogun_1ae37add856d1ce95f9f351987da38a82c)` `[`get_iter_info`](#classshogun_1_1IterativeSolverIterator_1a925cc234488a993cac2071be454a105a)`() const` | #### Returns
`public inline const bool `[`succeeded`](#classshogun_1_1IterativeSolverIterator_1a0bf51d376d642e5116b7d491921af146)`(const `[`VectorXt`](#classEigen_1_1Matrix)` & residual)` | #### Returns
`public inline void `[`operator++`](#classshogun_1_1IterativeSolverIterator_1a00f008b80917746917b874d00abd02a9)`()` | increment operator

## Members

#### `public inline  `[`IterativeSolverIterator`](#classshogun_1_1IterativeSolverIterator_1a367b9cc0323afaec8124d0f7312867ff)`(const `[`VectorXt`](#classEigen_1_1Matrix)` & b,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` max_iteration_limit,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` relative_tolerence,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` absolute_tolerence)` {#classshogun_1_1IterativeSolverIterator_1a367b9cc0323afaec8124d0f7312867ff}

constructor

tolerence of the solver is absolute_tolerence + relative_tolerence * ||b||

#### Parameters
* `b` the vector of the linear system Ax=b 

* `max_iteration_limit` maximum iteration limit 

* `relative_tolerence` relative tolerence of the iterative method 

* `absolute_tolerence` absolute tolerence of the iterative method

#### `public inline void `[`begin`](#classshogun_1_1IterativeSolverIterator_1a5d6eb442bc6374e57dac6c0d191c341f)`(const `[`VectorXt`](#classEigen_1_1Matrix)` & residual)` {#classshogun_1_1IterativeSolverIterator_1a5d6eb442bc6374e57dac6c0d191c341f}

assign operator from an IterInfo

#### `public inline const bool `[`end`](#classshogun_1_1IterativeSolverIterator_1acae14e719e91bcdeda7fce7eab9db6a0)`(const `[`VectorXt`](#classEigen_1_1Matrix)` & residual)` {#classshogun_1_1IterativeSolverIterator_1acae14e719e91bcdeda7fce7eab9db6a0}

#### Returns
true if converged or maximum iteration limit crossed

#### `public inline const `[`IterInfo`](#namespaceshogun_1ae37add856d1ce95f9f351987da38a82c)` `[`get_iter_info`](#classshogun_1_1IterativeSolverIterator_1a925cc234488a993cac2071be454a105a)`() const` {#classshogun_1_1IterativeSolverIterator_1a925cc234488a993cac2071be454a105a}

#### Returns
current iteration info

#### `public inline const bool `[`succeeded`](#classshogun_1_1IterativeSolverIterator_1a0bf51d376d642e5116b7d491921af146)`(const `[`VectorXt`](#classEigen_1_1Matrix)` & residual)` {#classshogun_1_1IterativeSolverIterator_1a0bf51d376d642e5116b7d491921af146}

#### Returns
success status

#### `public inline void `[`operator++`](#classshogun_1_1IterativeSolverIterator_1a00f008b80917746917b874d00abd02a9)`()` {#classshogun_1_1IterativeSolverIterator_1a00f008b80917746917b874d00abd02a9}

increment operator

