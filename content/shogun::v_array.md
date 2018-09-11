---
classname: "shogun::v_array"
type: "class"
---

# class `shogun::v_array` {#classshogun_1_1v__array}

Class [v_array](#classshogun_1_1v__array) is a templated class used to store variable length arrays. Memory locations are stored as 'extents', i.e., address of the first memory location and address after the last member.

`begin', `end' and `end_array' handle the extent of the array. `end_array' is the address at the end of the space allocated for the array while `end' is the address at the end of the space actually filled with elements.

The class should be instantiated on the basis of the data type of the contained array, eg. v_array<float32_t> if one wants to store a float32_t* array.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public T * `[`begin`](#classshogun_1_1v__array_1a28880d9a30422b761311492b8926f5fa) | Pointer to first element of the array.
`public T * `[`end`](#classshogun_1_1v__array_1a43676dcfa5af1d75e64292537feacc64) | Pointer to last set element in the array.
`public T * `[`end_array`](#classshogun_1_1v__array_1af47a9b2e17e99ee25c7121cda9af3237) | Pointer to end of array, based on memory reserved.
`public inline  `[`v_array`](#classshogun_1_1v__array_1a3a6711573514af16ceed89c75e40151c)`()` | Constructor. Sets begin and end pointers to NULL.
`public inline  `[`~v_array`](#classshogun_1_1v__array_1a2a824fcbe9e36d0115c66218130c61d1)`()` | Destructor
`public inline T & `[`operator[]`](#classshogun_1_1v__array_1acc931891ae9e3bb537e3a0a78ff87d8f)`(unsigned int i)` | Operator [] overloaded to return the i-th element of the stored array.
`public inline T `[`last`](#classshogun_1_1v__array_1a4fe9d3fee79bdf854302cfbf6707c729)`()` | Return the last element.
`public inline T `[`pop`](#classshogun_1_1v__array_1ad702374ab51a03308e76cc7305f42582)`()` | Pop from the array.
`public inline bool `[`empty`](#classshogun_1_1v__array_1a3f37b042a1e7cd4bd38fc564de81f0da)`()` | Check if array is empty or not.
`public inline void `[`decr`](#classshogun_1_1v__array_1a431939dbd3f0ff43a3aef0c4731459e4)`()` | Decrement the 'end' pointer.
`public inline unsigned int `[`index`](#classshogun_1_1v__array_1a871c37f0ffc7ee7785874f1bbc7dd095)`()` | Get number of elements in array.
`public inline void `[`erase`](#classshogun_1_1v__array_1af139f30d28b7dc61f5051c0d595af368)`()` | [Empty](#structshogun_1_1Empty) the array.
`public inline void `[`push`](#classshogun_1_1v__array_1a44a9956c5f9a96b4a5e7b5969cc67c8a)`(const T & new_elem)` | Push an element into the array.
`public inline void `[`push_many`](#classshogun_1_1v__array_1a05d735e3b05f1a6e14ed4cce4de173b6)`(const T * new_elem,size_t num)` | Push multiple elements into the array.
`public inline void `[`reserve`](#classshogun_1_1v__array_1afedb87504d3eed69bf507724983ed313)`(size_t length)` | Reserve space for specified number of elements. Reallocate, keeping the elements currently in the array.
`public inline void `[`calloc_reserve`](#classshogun_1_1v__array_1a2b992cd573bbe87697c93244c486cb84)`(size_t length)` | Reserve space for specified number of elements. No reallocation is done, array is replaced.
`public inline `[`v_array`](#classshogun_1_1v__array)`< T > `[`pop`](#classshogun_1_1v__array_1a4a96c4f56e1f4ae0785ad3766a2d0b22)`(`[`v_array](#classshogun_1_1v__array)< [v_array`](#classshogun_1_1v__array)`< T > > & stack)` | Pop an array from a list of arrays.

## Members

#### `public T * `[`begin`](#classshogun_1_1v__array_1a28880d9a30422b761311492b8926f5fa) {#classshogun_1_1v__array_1a28880d9a30422b761311492b8926f5fa}

Pointer to first element of the array.

#### `public T * `[`end`](#classshogun_1_1v__array_1a43676dcfa5af1d75e64292537feacc64) {#classshogun_1_1v__array_1a43676dcfa5af1d75e64292537feacc64}

Pointer to last set element in the array.

#### `public T * `[`end_array`](#classshogun_1_1v__array_1af47a9b2e17e99ee25c7121cda9af3237) {#classshogun_1_1v__array_1af47a9b2e17e99ee25c7121cda9af3237}

Pointer to end of array, based on memory reserved.

#### `public inline  `[`v_array`](#classshogun_1_1v__array_1a3a6711573514af16ceed89c75e40151c)`()` {#classshogun_1_1v__array_1a3a6711573514af16ceed89c75e40151c}

Constructor. Sets begin and end pointers to NULL.

#### `public inline  `[`~v_array`](#classshogun_1_1v__array_1a2a824fcbe9e36d0115c66218130c61d1)`()` {#classshogun_1_1v__array_1a2a824fcbe9e36d0115c66218130c61d1}

Destructor

will only free the array not the ptrs it contains

#### `public inline T & `[`operator[]`](#classshogun_1_1v__array_1acc931891ae9e3bb537e3a0a78ff87d8f)`(unsigned int i)` {#classshogun_1_1v__array_1acc931891ae9e3bb537e3a0a78ff87d8f}

Operator [] overloaded to return the i-th element of the stored array.

#### Parameters
* `i` index of the element, starting at 0

#### Returns
element at position i

#### `public inline T `[`last`](#classshogun_1_1v__array_1a4fe9d3fee79bdf854302cfbf6707c729)`()` {#classshogun_1_1v__array_1a4fe9d3fee79bdf854302cfbf6707c729}

Return the last element.

#### Returns
Last element of array

#### `public inline T `[`pop`](#classshogun_1_1v__array_1ad702374ab51a03308e76cc7305f42582)`()` {#classshogun_1_1v__array_1ad702374ab51a03308e76cc7305f42582}

Pop from the array.

#### Returns
Popped element

#### `public inline bool `[`empty`](#classshogun_1_1v__array_1a3f37b042a1e7cd4bd38fc564de81f0da)`()` {#classshogun_1_1v__array_1a3f37b042a1e7cd4bd38fc564de81f0da}

Check if array is empty or not.

#### Returns
whether array is empty

#### `public inline void `[`decr`](#classshogun_1_1v__array_1a431939dbd3f0ff43a3aef0c4731459e4)`()` {#classshogun_1_1v__array_1a431939dbd3f0ff43a3aef0c4731459e4}

Decrement the 'end' pointer.

#### `public inline unsigned int `[`index`](#classshogun_1_1v__array_1a871c37f0ffc7ee7785874f1bbc7dd095)`()` {#classshogun_1_1v__array_1a871c37f0ffc7ee7785874f1bbc7dd095}

Get number of elements in array.

#### Returns
number of array elements

#### `public inline void `[`erase`](#classshogun_1_1v__array_1af139f30d28b7dc61f5051c0d595af368)`()` {#classshogun_1_1v__array_1af139f30d28b7dc61f5051c0d595af368}

[Empty](#structshogun_1_1Empty) the array.

#### `public inline void `[`push`](#classshogun_1_1v__array_1a44a9956c5f9a96b4a5e7b5969cc67c8a)`(const T & new_elem)` {#classshogun_1_1v__array_1a44a9956c5f9a96b4a5e7b5969cc67c8a}

Push an element into the array.

#### Parameters
* `new_elem` element to be pushed

#### `public inline void `[`push_many`](#classshogun_1_1v__array_1a05d735e3b05f1a6e14ed4cce4de173b6)`(const T * new_elem,size_t num)` {#classshogun_1_1v__array_1a05d735e3b05f1a6e14ed4cce4de173b6}

Push multiple elements into the array.

#### Parameters
* `new_elem` pointer to first element 

* `num` number of elements

#### `public inline void `[`reserve`](#classshogun_1_1v__array_1afedb87504d3eed69bf507724983ed313)`(size_t length)` {#classshogun_1_1v__array_1afedb87504d3eed69bf507724983ed313}

Reserve space for specified number of elements. Reallocate, keeping the elements currently in the array.

#### Parameters
* `length` number of elements to accommodate

#### `public inline void `[`calloc_reserve`](#classshogun_1_1v__array_1a2b992cd573bbe87697c93244c486cb84)`(size_t length)` {#classshogun_1_1v__array_1a2b992cd573bbe87697c93244c486cb84}

Reserve space for specified number of elements. No reallocation is done, array is replaced.

#### Parameters
* `length`

#### `public inline `[`v_array`](#classshogun_1_1v__array)`< T > `[`pop`](#classshogun_1_1v__array_1a4a96c4f56e1f4ae0785ad3766a2d0b22)`(`[`v_array](#classshogun_1_1v__array)< [v_array`](#classshogun_1_1v__array)`< T > > & stack)` {#classshogun_1_1v__array_1a4a96c4f56e1f4ae0785ad3766a2d0b22}

Pop an array from a list of arrays.

#### Parameters
* `stack` array of arrays 

#### Returns
popped array

