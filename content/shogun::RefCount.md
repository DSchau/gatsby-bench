---
classname: "shogun::RefCount"
type: "class"
---

# class `shogun::RefCount` {#classshogun_1_1RefCount}

brief This class implements a thread-safe counter used for reference counting.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public inline  `[`RefCount`](#classshogun_1_1RefCount_1a6f534ac346d6c95b6baaa4d875f55248)`(int32_t ref_start)` | Constructor
`public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` int32_t `[`ref`](#classshogun_1_1RefCount_1a97e45dc180821dcc7ba9af2baea2f5a6)`()` | Increase ref count
`public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` int32_t `[`unref`](#classshogun_1_1RefCount_1af5a4d3881ec3903901db95e6041ca068)`()` | Decrease reference count
`public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` int32_t `[`ref_count`](#classshogun_1_1RefCount_1a87036a4f569f90fe1f367e445166170b)`()` | Get the reference count

## Members

#### `public inline  `[`RefCount`](#classshogun_1_1RefCount_1a6f534ac346d6c95b6baaa4d875f55248)`(int32_t ref_start)` {#classshogun_1_1RefCount_1a6f534ac346d6c95b6baaa4d875f55248}

Constructor

#### Parameters
* `ref_start` starting value for counter

#### `public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` int32_t `[`ref`](#classshogun_1_1RefCount_1a97e45dc180821dcc7ba9af2baea2f5a6)`()` {#classshogun_1_1RefCount_1a97e45dc180821dcc7ba9af2baea2f5a6}

Increase ref count

#### Returns
the new reference count

#### `public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` int32_t `[`unref`](#classshogun_1_1RefCount_1af5a4d3881ec3903901db95e6041ca068)`()` {#classshogun_1_1RefCount_1af5a4d3881ec3903901db95e6041ca068}

Decrease reference count

#### Returns
the new reference count

#### `public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` int32_t `[`ref_count`](#classshogun_1_1RefCount_1a87036a4f569f90fe1f367e445166170b)`()` {#classshogun_1_1RefCount_1a87036a4f569f90fe1f367e445166170b}

Get the reference count

#### Returns
the reference count

