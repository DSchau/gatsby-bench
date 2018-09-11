---
classname: "shogun::GPUMemoryBase"
type: "struct"
---

# struct `shogun::GPUMemoryBase` {#structshogun_1_1GPUMemoryBase}

Interface for GPU memory libraries.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public inline  `[`GPUMemoryBase`](#structshogun_1_1GPUMemoryBase_1a5a173d01e39f9a117fa128177d35c6a6)`()` | Default constructor
`public `[`GPUMemoryBase`](#structshogun_1_1GPUMemoryBase)`< T > * `[`clone_vector`](#structshogun_1_1GPUMemoryBase_1a0404f6502d0b1107cd100b5107097ddc)`(`[`GPUMemoryBase`](#structshogun_1_1GPUMemoryBase)`< T > * gpu_ptr,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` vlen) const` | Clone GPU memory, i.e. vector or matrix

## Members

#### `public inline  `[`GPUMemoryBase`](#structshogun_1_1GPUMemoryBase_1a5a173d01e39f9a117fa128177d35c6a6)`()` {#structshogun_1_1GPUMemoryBase_1a5a173d01e39f9a117fa128177d35c6a6}

Default constructor

#### `public `[`GPUMemoryBase`](#structshogun_1_1GPUMemoryBase)`< T > * `[`clone_vector`](#structshogun_1_1GPUMemoryBase_1a0404f6502d0b1107cd100b5107097ddc)`(`[`GPUMemoryBase`](#structshogun_1_1GPUMemoryBase)`< T > * gpu_ptr,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` vlen) const` {#structshogun_1_1GPUMemoryBase_1a0404f6502d0b1107cd100b5107097ddc}

Clone GPU memory, i.e. vector or matrix

#### Parameters
* `gpu_ptr` [GPUMemoryBase](#structshogun_1_1GPUMemoryBase) structure pointer 

#### Returns
A deep-copy of [GPUMemoryBase](#structshogun_1_1GPUMemoryBase) structure pointer

