---
classname: "shogun::SGLinalg"
type: "class"
---

# class `shogun::SGLinalg` {#classshogun_1_1SGLinalg}

linalg library backend

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public `[`CLock`](#classshogun_1_1CLock)` `[`m_gpu_transfer`](#classshogun_1_1SGLinalg_1a39c31dd6e00e61c2d2d4158d08fadc67) | Mutex of GPU transfer methods
`public inline  `[`SGLinalg`](#classshogun_1_1SGLinalg_1abb57d5130962bce865ae22b995e859fc)`()` | Default constructor
`public inline  `[`~SGLinalg`](#classshogun_1_1SGLinalg_1a8aeffd83f07754b88c018313a2957558)`()` | Default destructor
`public inline void `[`set_cpu_backend`](#classshogun_1_1SGLinalg_1a2323506e08e4ecba514fa44929731da2)`(`[`LinalgBackendBase`](#classshogun_1_1LinalgBackendBase)` * backend)` | Set CPU backend The default CPU backend is EIGEN3
`public inline `[`LinalgBackendBase`](#classshogun_1_1LinalgBackendBase)` *const `[`get_cpu_backend`](#classshogun_1_1SGLinalg_1a2b9be31e3ba4a75e172150185d1aa1c9)`() const` | Set CPU backend
`public inline void `[`set_gpu_backend`](#classshogun_1_1SGLinalg_1a83c8b81085e21d9c795e8063c71cb44b)`(`[`LinalgBackendBase`](#classshogun_1_1LinalgBackendBase)` * backend)` | Set GPU backend The default GPU backend is NULL
`public inline `[`LinalgBackendBase`](#classshogun_1_1LinalgBackendBase)` *const `[`get_gpu_backend`](#classshogun_1_1SGLinalg_1a947956d40a53afa59a2c7f3e8cdd2c2b)`() const` | Set GPU backend
`public inline void `[`set_linalg_warnings`](#classshogun_1_1SGLinalg_1abf67062e8811691f4b7e4422127d0b3c)`(bool enable_warnings)` | Set linalg library warnings display option The warnings are default on.
`public inline bool const `[`get_linalg_warnings`](#classshogun_1_1SGLinalg_1a9fcf6d4614ca4c747b10fec46aa5141c)`() const` | Get linalg library warnings display option

## Members

#### `public `[`CLock`](#classshogun_1_1CLock)` `[`m_gpu_transfer`](#classshogun_1_1SGLinalg_1a39c31dd6e00e61c2d2d4158d08fadc67) {#classshogun_1_1SGLinalg_1a39c31dd6e00e61c2d2d4158d08fadc67}

Mutex of GPU transfer methods

#### `public inline  `[`SGLinalg`](#classshogun_1_1SGLinalg_1abb57d5130962bce865ae22b995e859fc)`()` {#classshogun_1_1SGLinalg_1abb57d5130962bce865ae22b995e859fc}

Default constructor

#### `public inline  `[`~SGLinalg`](#classshogun_1_1SGLinalg_1a8aeffd83f07754b88c018313a2957558)`()` {#classshogun_1_1SGLinalg_1a8aeffd83f07754b88c018313a2957558}

Default destructor

#### `public inline void `[`set_cpu_backend`](#classshogun_1_1SGLinalg_1a2323506e08e4ecba514fa44929731da2)`(`[`LinalgBackendBase`](#classshogun_1_1LinalgBackendBase)` * backend)` {#classshogun_1_1SGLinalg_1a2323506e08e4ecba514fa44929731da2}

Set CPU backend The default CPU backend is EIGEN3

#### `public inline `[`LinalgBackendBase`](#classshogun_1_1LinalgBackendBase)` *const `[`get_cpu_backend`](#classshogun_1_1SGLinalg_1a2b9be31e3ba4a75e172150185d1aa1c9)`() const` {#classshogun_1_1SGLinalg_1a2b9be31e3ba4a75e172150185d1aa1c9}

Set CPU backend

#### Returns
Pointer of [LinalgBackendBase](#classshogun_1_1LinalgBackendBase) type

#### `public inline void `[`set_gpu_backend`](#classshogun_1_1SGLinalg_1a83c8b81085e21d9c795e8063c71cb44b)`(`[`LinalgBackendBase`](#classshogun_1_1LinalgBackendBase)` * backend)` {#classshogun_1_1SGLinalg_1a83c8b81085e21d9c795e8063c71cb44b}

Set GPU backend The default GPU backend is NULL

#### `public inline `[`LinalgBackendBase`](#classshogun_1_1LinalgBackendBase)` *const `[`get_gpu_backend`](#classshogun_1_1SGLinalg_1a947956d40a53afa59a2c7f3e8cdd2c2b)`() const` {#classshogun_1_1SGLinalg_1a947956d40a53afa59a2c7f3e8cdd2c2b}

Set GPU backend

#### Returns
Pointer of [LinalgBackendBase](#classshogun_1_1LinalgBackendBase) type

#### `public inline void `[`set_linalg_warnings`](#classshogun_1_1SGLinalg_1abf67062e8811691f4b7e4422127d0b3c)`(bool enable_warnings)` {#classshogun_1_1SGLinalg_1abf67062e8811691f4b7e4422127d0b3c}

Set linalg library warnings display option The warnings are default on.

#### `public inline bool const `[`get_linalg_warnings`](#classshogun_1_1SGLinalg_1a9fcf6d4614ca4c747b10fec46aa5141c)`() const` {#classshogun_1_1SGLinalg_1a9fcf6d4614ca4c747b10fec46aa5141c}

Get linalg library warnings display option

#### Returns
Whether to display linalg library warnings

