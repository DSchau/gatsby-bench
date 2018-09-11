---
classname: "shogun::LDACanVarSolver"
type: "class"
parents:
   - shogun::LDASolver< T >
---

# class `shogun::LDACanVarSolver` {#classshogun_1_1LDACanVarSolver}

```
class shogun::LDACanVarSolver
  : public shogun::LDASolver< T >
```

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public inline  `[`LDACanVarSolver`](#classshogun_1_1LDACanVarSolver_1ac3b0f85fd07498fdf4900f3f996284ce)`(`[`CDenseFeatures`](#classshogun_1_1CDenseFeatures)`< T > * features,`[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * labels,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_dim,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` gamma,bool bdc_svd,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` threshold)` | 
`public `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`get_eigenvectors`](#classshogun_1_1LDACanVarSolver_1a0352e7a74e76e2040bbdf5ed22a92d30)`()` | #### Returns
`public `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`get_eigenvalues`](#classshogun_1_1LDACanVarSolver_1adc38a8fa90e215ea337eab097572be0b)`()` | #### Returns
`public std::vector< `[`SGVector`](#classshogun_1_1SGVector)`< T > > `[`get_class_mean`](#classshogun_1_1LDASolver_1a5269554ce5171cfd086f5312766f52b8)`()` | #### Returns
`public std::vector< `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > `[`get_class_count`](#classshogun_1_1LDASolver_1aef5019dd5d184b284f528a230ca70170)`()` | #### Returns
`public `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`get_mean`](#classshogun_1_1LDASolver_1afb9f86821ffa75bc2eaf7875e6b5b7f9)`()` | #### Returns
`public `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`get_within_cov`](#classshogun_1_1LDASolver_1a05572cae9351fac0ae1f664ad74dba84)`()` | #### Returns
`protected `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`m_between_cov`](#classshogun_1_1LDACanVarSolver_1a1dd23ac68076b5510814878aac7cfea4) | Between covariance matrix
`protected `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`m_num_dim`](#classshogun_1_1LDACanVarSolver_1aa15d7128085ed3e7edf608a1448a20c5) | Number of dimensions in the projected space
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_threshold`](#classshogun_1_1LDACanVarSolver_1af64d35f034939b007842051d4a0caf08) | Singular values threshold in svd
`protected `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`m_eigenvectors`](#classshogun_1_1LDACanVarSolver_1a4a391687808ad3e136b95f7c4779f639) | eigenvectors matrix
`protected `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`m_eigenvalues`](#classshogun_1_1LDACanVarSolver_1aee432b60602d9d75941e2d7473539c36) | eigenvalues vector
`protected bool `[`m_bdc_svd`](#classshogun_1_1LDACanVarSolver_1a379500608d9abfac5e8a3eb21f0ac7a8) | use bdc-svd algorithm
`protected `[`CDenseFeatures`](#classshogun_1_1CDenseFeatures)`< T > * `[`m_features`](#classshogun_1_1LDASolver_1a20bff9c7bcea127d06216632ac5c92a2) | 
`protected `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * `[`m_labels`](#classshogun_1_1LDASolver_1a8dbff20aba35514bdbbabc1ec901db29) | 
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_gamma`](#classshogun_1_1LDASolver_1ad47b73a03e3cfe4dbccb7867c38d295e) | 
`protected std::vector< `[`SGVector`](#classshogun_1_1SGVector)`< T > > `[`m_class_mean`](#classshogun_1_1LDASolver_1a8f8aa0edc9ae0ab348b4c6edd34622d3) | 
`protected std::vector< `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > `[`m_class_count`](#classshogun_1_1LDASolver_1ac7f7926135a614131af074567423a563) | 
`protected `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`m_mean`](#classshogun_1_1LDASolver_1a629cd79e74e5f693caa33377557a0002) | 
`protected `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`m_within_cov`](#classshogun_1_1LDASolver_1a373ee2cf98ac06d6c400c50516cbd138) | 
`protected virtual void `[`compute_between_cov`](#classshogun_1_1LDACanVarSolver_1a3cda6bfea4d9c84dfe8069883c4a2d08)`()` | Compute between class covariance matrix.
`protected virtual void `[`canvar`](#classshogun_1_1LDACanVarSolver_1a69d3ae567918824f7f960201dd90891b)`()` | Compute the eigenvectors through the canonical variates algorithm.
`protected virtual void `[`compute_means`](#classshogun_1_1LDASolver_1ab33878b42ea7b78453fd484300fa7477)`()` | Compute the total mean and for each class the number of data points and its mean.
`protected virtual void `[`compute_within_cov`](#classshogun_1_1LDASolver_1adda6d3510fa50a6f27cf2904ede40602)`()` | Compute within class covariance matrix.

## Members

#### `public inline  `[`LDACanVarSolver`](#classshogun_1_1LDACanVarSolver_1ac3b0f85fd07498fdf4900f3f996284ce)`(`[`CDenseFeatures`](#classshogun_1_1CDenseFeatures)`< T > * features,`[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * labels,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` num_dim,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` gamma,bool bdc_svd,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` threshold)` {#classshogun_1_1LDACanVarSolver_1ac3b0f85fd07498fdf4900f3f996284ce}

#### `public `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`get_eigenvectors`](#classshogun_1_1LDACanVarSolver_1a0352e7a74e76e2040bbdf5ed22a92d30)`()` {#classshogun_1_1LDACanVarSolver_1a0352e7a74e76e2040bbdf5ed22a92d30}

#### Returns
eigenvectors to project features into the transformed space

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`get_eigenvalues`](#classshogun_1_1LDACanVarSolver_1adc38a8fa90e215ea337eab097572be0b)`()` {#classshogun_1_1LDACanVarSolver_1adc38a8fa90e215ea337eab097572be0b}

#### Returns
eigenvalues

#### `public std::vector< `[`SGVector`](#classshogun_1_1SGVector)`< T > > `[`get_class_mean`](#classshogun_1_1LDASolver_1a5269554ce5171cfd086f5312766f52b8)`()` {#classshogun_1_1LDASolver_1a5269554ce5171cfd086f5312766f52b8}

#### Returns
the vector of classes' mean

#### `public std::vector< `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > `[`get_class_count`](#classshogun_1_1LDASolver_1aef5019dd5d184b284f528a230ca70170)`()` {#classshogun_1_1LDASolver_1aef5019dd5d184b284f528a230ca70170}

#### Returns
the number of data points of each class

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`get_mean`](#classshogun_1_1LDASolver_1afb9f86821ffa75bc2eaf7875e6b5b7f9)`()` {#classshogun_1_1LDASolver_1afb9f86821ffa75bc2eaf7875e6b5b7f9}

#### Returns
the total mean

#### `public `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`get_within_cov`](#classshogun_1_1LDASolver_1a05572cae9351fac0ae1f664ad74dba84)`()` {#classshogun_1_1LDASolver_1a05572cae9351fac0ae1f664ad74dba84}

#### Returns
the within covariance matrix

#### `protected `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`m_between_cov`](#classshogun_1_1LDACanVarSolver_1a1dd23ac68076b5510814878aac7cfea4) {#classshogun_1_1LDACanVarSolver_1a1dd23ac68076b5510814878aac7cfea4}

Between covariance matrix

#### `protected `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`m_num_dim`](#classshogun_1_1LDACanVarSolver_1aa15d7128085ed3e7edf608a1448a20c5) {#classshogun_1_1LDACanVarSolver_1aa15d7128085ed3e7edf608a1448a20c5}

Number of dimensions in the projected space

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_threshold`](#classshogun_1_1LDACanVarSolver_1af64d35f034939b007842051d4a0caf08) {#classshogun_1_1LDACanVarSolver_1af64d35f034939b007842051d4a0caf08}

Singular values threshold in svd

#### `protected `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`m_eigenvectors`](#classshogun_1_1LDACanVarSolver_1a4a391687808ad3e136b95f7c4779f639) {#classshogun_1_1LDACanVarSolver_1a4a391687808ad3e136b95f7c4779f639}

eigenvectors matrix

#### `protected `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`m_eigenvalues`](#classshogun_1_1LDACanVarSolver_1aee432b60602d9d75941e2d7473539c36) {#classshogun_1_1LDACanVarSolver_1aee432b60602d9d75941e2d7473539c36}

eigenvalues vector

#### `protected bool `[`m_bdc_svd`](#classshogun_1_1LDACanVarSolver_1a379500608d9abfac5e8a3eb21f0ac7a8) {#classshogun_1_1LDACanVarSolver_1a379500608d9abfac5e8a3eb21f0ac7a8}

use bdc-svd algorithm

#### `protected `[`CDenseFeatures`](#classshogun_1_1CDenseFeatures)`< T > * `[`m_features`](#classshogun_1_1LDASolver_1a20bff9c7bcea127d06216632ac5c92a2) {#classshogun_1_1LDASolver_1a20bff9c7bcea127d06216632ac5c92a2}

#### `protected `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * `[`m_labels`](#classshogun_1_1LDASolver_1a8dbff20aba35514bdbbabc1ec901db29) {#classshogun_1_1LDASolver_1a8dbff20aba35514bdbbabc1ec901db29}

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_gamma`](#classshogun_1_1LDASolver_1ad47b73a03e3cfe4dbccb7867c38d295e) {#classshogun_1_1LDASolver_1ad47b73a03e3cfe4dbccb7867c38d295e}

#### `protected std::vector< `[`SGVector`](#classshogun_1_1SGVector)`< T > > `[`m_class_mean`](#classshogun_1_1LDASolver_1a8f8aa0edc9ae0ab348b4c6edd34622d3) {#classshogun_1_1LDASolver_1a8f8aa0edc9ae0ab348b4c6edd34622d3}

#### `protected std::vector< `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > `[`m_class_count`](#classshogun_1_1LDASolver_1ac7f7926135a614131af074567423a563) {#classshogun_1_1LDASolver_1ac7f7926135a614131af074567423a563}

#### `protected `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`m_mean`](#classshogun_1_1LDASolver_1a629cd79e74e5f693caa33377557a0002) {#classshogun_1_1LDASolver_1a629cd79e74e5f693caa33377557a0002}

#### `protected `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`m_within_cov`](#classshogun_1_1LDASolver_1a373ee2cf98ac06d6c400c50516cbd138) {#classshogun_1_1LDASolver_1a373ee2cf98ac06d6c400c50516cbd138}

#### `protected virtual void `[`compute_between_cov`](#classshogun_1_1LDACanVarSolver_1a3cda6bfea4d9c84dfe8069883c4a2d08)`()` {#classshogun_1_1LDACanVarSolver_1a3cda6bfea4d9c84dfe8069883c4a2d08}

Compute between class covariance matrix.

#### `protected virtual void `[`canvar`](#classshogun_1_1LDACanVarSolver_1a69d3ae567918824f7f960201dd90891b)`()` {#classshogun_1_1LDACanVarSolver_1a69d3ae567918824f7f960201dd90891b}

Compute the eigenvectors through the canonical variates algorithm.

#### `protected virtual void `[`compute_means`](#classshogun_1_1LDASolver_1ab33878b42ea7b78453fd484300fa7477)`()` {#classshogun_1_1LDASolver_1ab33878b42ea7b78453fd484300fa7477}

Compute the total mean and for each class the number of data points and its mean.

#### `protected virtual void `[`compute_within_cov`](#classshogun_1_1LDASolver_1adda6d3510fa50a6f27cf2904ede40602)`()` {#classshogun_1_1LDASolver_1adda6d3510fa50a6f27cf2904ede40602}

Compute within class covariance matrix.

