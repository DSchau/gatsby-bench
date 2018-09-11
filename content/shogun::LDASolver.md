---
classname: "shogun::LDASolver"
type: "class"
---

# class `shogun::LDASolver` {#classshogun_1_1LDASolver}

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public inline  `[`LDASolver`](#classshogun_1_1LDASolver_1a2d2bda0de1d32fa43d11878adb12bc1f)`(`[`CDenseFeatures`](#classshogun_1_1CDenseFeatures)`< T > * features,`[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * labels,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` gamma)` | 
`public inline  `[`~LDASolver`](#classshogun_1_1LDASolver_1ad5ac2aa3eade68f3c1a43b522957260a)`()` | 
`public std::vector< `[`SGVector`](#classshogun_1_1SGVector)`< T > > `[`get_class_mean`](#classshogun_1_1LDASolver_1a5269554ce5171cfd086f5312766f52b8)`()` | #### Returns
`public std::vector< `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > `[`get_class_count`](#classshogun_1_1LDASolver_1aef5019dd5d184b284f528a230ca70170)`()` | #### Returns
`public `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`get_mean`](#classshogun_1_1LDASolver_1afb9f86821ffa75bc2eaf7875e6b5b7f9)`()` | #### Returns
`public `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`get_within_cov`](#classshogun_1_1LDASolver_1a05572cae9351fac0ae1f664ad74dba84)`()` | #### Returns
`protected `[`CDenseFeatures`](#classshogun_1_1CDenseFeatures)`< T > * `[`m_features`](#classshogun_1_1LDASolver_1a20bff9c7bcea127d06216632ac5c92a2) | 
`protected `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * `[`m_labels`](#classshogun_1_1LDASolver_1a8dbff20aba35514bdbbabc1ec901db29) | 
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_gamma`](#classshogun_1_1LDASolver_1ad47b73a03e3cfe4dbccb7867c38d295e) | 
`protected std::vector< `[`SGVector`](#classshogun_1_1SGVector)`< T > > `[`m_class_mean`](#classshogun_1_1LDASolver_1a8f8aa0edc9ae0ab348b4c6edd34622d3) | 
`protected std::vector< `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > `[`m_class_count`](#classshogun_1_1LDASolver_1ac7f7926135a614131af074567423a563) | 
`protected `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`m_mean`](#classshogun_1_1LDASolver_1a629cd79e74e5f693caa33377557a0002) | 
`protected `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`m_within_cov`](#classshogun_1_1LDASolver_1a373ee2cf98ac06d6c400c50516cbd138) | 
`protected virtual void `[`compute_means`](#classshogun_1_1LDASolver_1ab33878b42ea7b78453fd484300fa7477)`()` | Compute the total mean and for each class the number of data points and its mean.
`protected virtual void `[`compute_within_cov`](#classshogun_1_1LDASolver_1adda6d3510fa50a6f27cf2904ede40602)`()` | Compute within class covariance matrix.

## Members

#### `public inline  `[`LDASolver`](#classshogun_1_1LDASolver_1a2d2bda0de1d32fa43d11878adb12bc1f)`(`[`CDenseFeatures`](#classshogun_1_1CDenseFeatures)`< T > * features,`[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * labels,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` gamma)` {#classshogun_1_1LDASolver_1a2d2bda0de1d32fa43d11878adb12bc1f}

#### `public inline  `[`~LDASolver`](#classshogun_1_1LDASolver_1ad5ac2aa3eade68f3c1a43b522957260a)`()` {#classshogun_1_1LDASolver_1ad5ac2aa3eade68f3c1a43b522957260a}

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

#### `protected `[`CDenseFeatures`](#classshogun_1_1CDenseFeatures)`< T > * `[`m_features`](#classshogun_1_1LDASolver_1a20bff9c7bcea127d06216632ac5c92a2) {#classshogun_1_1LDASolver_1a20bff9c7bcea127d06216632ac5c92a2}

#### `protected `[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * `[`m_labels`](#classshogun_1_1LDASolver_1a8dbff20aba35514bdbbabc1ec901db29) {#classshogun_1_1LDASolver_1a8dbff20aba35514bdbbabc1ec901db29}

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`m_gamma`](#classshogun_1_1LDASolver_1ad47b73a03e3cfe4dbccb7867c38d295e) {#classshogun_1_1LDASolver_1ad47b73a03e3cfe4dbccb7867c38d295e}

#### `protected std::vector< `[`SGVector`](#classshogun_1_1SGVector)`< T > > `[`m_class_mean`](#classshogun_1_1LDASolver_1a8f8aa0edc9ae0ab348b4c6edd34622d3) {#classshogun_1_1LDASolver_1a8f8aa0edc9ae0ab348b4c6edd34622d3}

#### `protected std::vector< `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > `[`m_class_count`](#classshogun_1_1LDASolver_1ac7f7926135a614131af074567423a563) {#classshogun_1_1LDASolver_1ac7f7926135a614131af074567423a563}

#### `protected `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`m_mean`](#classshogun_1_1LDASolver_1a629cd79e74e5f693caa33377557a0002) {#classshogun_1_1LDASolver_1a629cd79e74e5f693caa33377557a0002}

#### `protected `[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > `[`m_within_cov`](#classshogun_1_1LDASolver_1a373ee2cf98ac06d6c400c50516cbd138) {#classshogun_1_1LDASolver_1a373ee2cf98ac06d6c400c50516cbd138}

#### `protected virtual void `[`compute_means`](#classshogun_1_1LDASolver_1ab33878b42ea7b78453fd484300fa7477)`()` {#classshogun_1_1LDASolver_1ab33878b42ea7b78453fd484300fa7477}

Compute the total mean and for each class the number of data points and its mean.

#### `protected virtual void `[`compute_within_cov`](#classshogun_1_1LDASolver_1adda6d3510fa50a6f27cf2904ede40602)`()` {#classshogun_1_1LDASolver_1adda6d3510fa50a6f27cf2904ede40602}

Compute within class covariance matrix.

