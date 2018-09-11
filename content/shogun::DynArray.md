---
classname: "shogun::DynArray"
type: "class"
---

# class `shogun::DynArray` {#classshogun_1_1DynArray}

Template Dynamic array class that creates an array that can be used like a list or an array.

It grows and shrinks dynamically, while elements can be accessed via index. It is performance tuned for simple types like float etc. and for hi-level objects only stores pointers, which are not automagically SG_REF'd/deleted.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public inline  `[`DynArray`](#classshogun_1_1DynArray_1a71a4229f2ad5ba0e5df6e2ff91a24075)`(int32_t p_resize_granularity,bool tracable)` | constructor
`public inline  `[`DynArray`](#classshogun_1_1DynArray_1a67df257f06078cb7e395d7ff2b97b917)`(T * p_array,int32_t p_array_size,bool p_free_array,bool p_copy_array,bool tracable)` | constructor
`public inline  `[`DynArray`](#classshogun_1_1DynArray_1a220f2f64bae8f1c8135d33c42604ebf9)`(const T * p_array,int32_t p_array_size,bool tracable)` | constructor
`public inline virtual  `[`~DynArray`](#classshogun_1_1DynArray_1a4c913cf4d1e6f094d31a250b0e4feba4)`()` | destructor
`public inline int32_t `[`set_granularity`](#classshogun_1_1DynArray_1a2850663a352f44e69a6896fcd7f6bb76)`(int32_t g)` | set the resize granularity
`public inline int32_t `[`get_array_size`](#classshogun_1_1DynArray_1aac888c32bbbf9363b1c50d496132f780)`() const` | get array size (including granularity buffer)
`public inline int32_t `[`get_num_elements`](#classshogun_1_1DynArray_1aa1a8c34958f199dc0209b1ef9c23b72d)`() const` | get number of elements
`public inline T `[`get_element`](#classshogun_1_1DynArray_1a5ad6735bd3aad8601afb08fc4714359d)`(int32_t index) const` | get array element at index
`public inline T `[`get_last_element`](#classshogun_1_1DynArray_1a37e774af60d0206611fec17dd9f2661d)`() const` | gets last array element
`public inline T * `[`get_element_ptr`](#classshogun_1_1DynArray_1a0ea23ea07699503eef68fc87b81a1e7d)`(int32_t index)` | get array element at index as pointer
`public inline T `[`get_element_safe`](#classshogun_1_1DynArray_1af9d122a6aceb61900123f6a6aa673052)`(int32_t index) const` | get array element at index
`public inline bool `[`set_element`](#classshogun_1_1DynArray_1adf49331c5643dc4d1cf004375ca76001)`(T element,int32_t index)` | set array element at index
`public inline bool `[`insert_element`](#classshogun_1_1DynArray_1abcd77035c18bf0c7ddcc8c5be91532bc)`(T element,int32_t index)` | insert array element at index
`public inline bool `[`append_element`](#classshogun_1_1DynArray_1ad7980b73fe2e1b9695305017e111b72a)`(T element)` | append array element to the end of array
`public inline void `[`push_back`](#classshogun_1_1DynArray_1ab1f08be94f07c176a1e76c38b3f4051e)`(T element)` | STD VECTOR compatible. Append array element to the end of array.
`public inline void `[`pop_back`](#classshogun_1_1DynArray_1a058bda4957df6a97b1ea6c9fd783f672)`()` | STD VECTOR compatible. Delete array element at the end of array.
`public inline T `[`back`](#classshogun_1_1DynArray_1a993054173e187eb9f15011f9fd3e2ad0)`() const` | STD VECTOR compatible. Return array element at the end of array.
`public inline int32_t `[`find_element`](#classshogun_1_1DynArray_1ac17f4a00028014c41476c4616e7ce5c5)`(T element) const` | find first occurence of array element and return its index or -1 if not available
`public inline bool `[`delete_element`](#classshogun_1_1DynArray_1af1e028b3c9d27ca9cbf78ebec9e79b93)`(int32_t idx)` | delete array element at idx (does not call SG_FREE() or the like)
`public inline bool `[`resize_array`](#classshogun_1_1DynArray_1ab87b186ee33f8bc8b309a1d7e26c9226)`(int32_t n,bool exact_resize)` | resize the array
`public inline T * `[`get_array`](#classshogun_1_1DynArray_1ae5e97a64694ed7fd85475d6790e03014)`() const` | get the array call get_array just before messing with it DO NOT call any [],resize/delete functions after [get_array()](#classshogun_1_1DynArray_1ae5e97a64694ed7fd85475d6790e03014), the pointer may become invalid !
`public inline void `[`set_array`](#classshogun_1_1DynArray_1a639546225a9e65c593356d4094373c1b)`(T * p_array,int32_t p_num_elements,int32_t p_array_size,bool p_free_array,bool p_copy_array)` | set the array pointer and free previously allocated memory
`public inline void `[`set_array`](#classshogun_1_1DynArray_1a774b4a8eec6cdf7a8276cbfc4bd173af)`(const T * p_array,int32_t p_num_elements,int32_t p_array_size)` | set the array pointer and free previously allocated memory
`public inline void `[`clear_array`](#classshogun_1_1DynArray_1a402b94aecfa928ab094bb30e6eee362a)`(T value)` | clear the array (with e.g. zeros)
`public inline void `[`reset`](#classshogun_1_1DynArray_1a7d6ba3006015c7435c085ac716d147f0)`(T value)` | resets the array (as if it was just created), keeps granularity
`public inline void `[`shuffle`](#classshogun_1_1DynArray_1a1905fe84eb39f020b32c58baf7a76758)`()` | randomizes the array (not thread safe!)
`public inline void `[`shuffle`](#classshogun_1_1DynArray_1aab5aeea2dba53b2995b58f400be7db1a)`(`[`CRandom`](#classshogun_1_1CRandom)` * rand)` | randomizes the array with external random state
`public inline void `[`set_const`](#classshogun_1_1DynArray_1a9eaae66fe81b1044e644767c5871e0df)`(const T & const_element)` | set array with a constant
`public inline T `[`operator[]`](#classshogun_1_1DynArray_1afd0d0238c34b1c884ea601b11bf52114)`(int32_t index) const` | operator overload for array read only access use [set_element()](#classshogun_1_1DynArray_1adf49331c5643dc4d1cf004375ca76001) for write access (will also make the array dynamically grow)
`public inline `[`DynArray`](#classshogun_1_1DynArray)`< T > & `[`operator=`](#classshogun_1_1DynArray_1a96c0e6582aedead2042950ca170efc80)`(`[`DynArray`](#classshogun_1_1DynArray)`< T > & orig)` | operator overload for array assignment. Left array is resized if needed.
`public inline virtual const char * `[`get_name`](#classshogun_1_1DynArray_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` | #### Returns
`protected int32_t `[`resize_granularity`](#classshogun_1_1DynArray_1a364caf1df30c6dce6a711586c568be26) | shrink/grow step size
`protected T * `[`array`](#classshogun_1_1DynArray_1a189874643dd3d326549d72b097665049) | memory for dynamic array
`protected int32_t `[`num_elements`](#classshogun_1_1DynArray_1a481f2cd05e67d8830f548ec248ea1d92) | the number of potentially used elements in array
`protected int32_t `[`current_num_elements`](#classshogun_1_1DynArray_1ace070cc900bca005910d53f39ea6897c) | the number of currently used elements
`protected bool `[`use_sg_mallocs`](#classshogun_1_1DynArray_1ad358739efb565b48bd00586384106310) | whether SG_MALLOC or just malloc etc shall be used
`protected bool `[`free_array`](#classshogun_1_1DynArray_1a8523f3d4c8bf61a18c074aceaa8fddd3) | if array must be freed

## Members

#### `public inline  `[`DynArray`](#classshogun_1_1DynArray_1a71a4229f2ad5ba0e5df6e2ff91a24075)`(int32_t p_resize_granularity,bool tracable)` {#classshogun_1_1DynArray_1a71a4229f2ad5ba0e5df6e2ff91a24075}

constructor

#### Parameters
* `p_resize_granularity` resize granularity 

* `tracable`

#### `public inline  `[`DynArray`](#classshogun_1_1DynArray_1a67df257f06078cb7e395d7ff2b97b917)`(T * p_array,int32_t p_array_size,bool p_free_array,bool p_copy_array,bool tracable)` {#classshogun_1_1DynArray_1a67df257f06078cb7e395d7ff2b97b917}

constructor

#### Parameters
* `p_array` another array 

* `p_array_size` array's size 

* `p_free_array` if array must be freed 

* `p_copy_array` if array must be copied 

* `tracable`

#### `public inline  `[`DynArray`](#classshogun_1_1DynArray_1a220f2f64bae8f1c8135d33c42604ebf9)`(const T * p_array,int32_t p_array_size,bool tracable)` {#classshogun_1_1DynArray_1a220f2f64bae8f1c8135d33c42604ebf9}

constructor

#### Parameters
* `p_array` another array 

* `p_array_size` array's size 

* `tracable`

#### `public inline virtual  `[`~DynArray`](#classshogun_1_1DynArray_1a4c913cf4d1e6f094d31a250b0e4feba4)`()` {#classshogun_1_1DynArray_1a4c913cf4d1e6f094d31a250b0e4feba4}

destructor

#### `public inline int32_t `[`set_granularity`](#classshogun_1_1DynArray_1a2850663a352f44e69a6896fcd7f6bb76)`(int32_t g)` {#classshogun_1_1DynArray_1a2850663a352f44e69a6896fcd7f6bb76}

set the resize granularity

#### Parameters
* `g` new granularity 

#### Returns
what has been set (minimum is 128)

#### `public inline int32_t `[`get_array_size`](#classshogun_1_1DynArray_1aac888c32bbbf9363b1c50d496132f780)`() const` {#classshogun_1_1DynArray_1aac888c32bbbf9363b1c50d496132f780}

get array size (including granularity buffer)

#### Returns
total array size (including granularity buffer)

#### `public inline int32_t `[`get_num_elements`](#classshogun_1_1DynArray_1aa1a8c34958f199dc0209b1ef9c23b72d)`() const` {#classshogun_1_1DynArray_1aa1a8c34958f199dc0209b1ef9c23b72d}

get number of elements

#### Returns
number of elements

#### `public inline T `[`get_element`](#classshogun_1_1DynArray_1a5ad6735bd3aad8601afb08fc4714359d)`(int32_t index) const` {#classshogun_1_1DynArray_1a5ad6735bd3aad8601afb08fc4714359d}

get array element at index

(does NOT do bounds checking)

#### Parameters
* `index` index 

#### Returns
array element at index

#### `public inline T `[`get_last_element`](#classshogun_1_1DynArray_1a37e774af60d0206611fec17dd9f2661d)`() const` {#classshogun_1_1DynArray_1a37e774af60d0206611fec17dd9f2661d}

gets last array element

#### Returns
array element at last index

#### `public inline T * `[`get_element_ptr`](#classshogun_1_1DynArray_1a0ea23ea07699503eef68fc87b81a1e7d)`(int32_t index)` {#classshogun_1_1DynArray_1a0ea23ea07699503eef68fc87b81a1e7d}

get array element at index as pointer

(does NOT do bounds checking)

#### Parameters
* `index` index 

#### Returns
array element at index

#### `public inline T `[`get_element_safe`](#classshogun_1_1DynArray_1af9d122a6aceb61900123f6a6aa673052)`(int32_t index) const` {#classshogun_1_1DynArray_1af9d122a6aceb61900123f6a6aa673052}

get array element at index

(does bounds checking)

#### Parameters
* `index` index 

#### Returns
array element at index

#### `public inline bool `[`set_element`](#classshogun_1_1DynArray_1adf49331c5643dc4d1cf004375ca76001)`(T element,int32_t index)` {#classshogun_1_1DynArray_1adf49331c5643dc4d1cf004375ca76001}

set array element at index

#### Parameters
* `element` element to set 

* `index` index 

#### Returns
if setting was successful

#### `public inline bool `[`insert_element`](#classshogun_1_1DynArray_1abcd77035c18bf0c7ddcc8c5be91532bc)`(T element,int32_t index)` {#classshogun_1_1DynArray_1abcd77035c18bf0c7ddcc8c5be91532bc}

insert array element at index

#### Parameters
* `element` element to insert 

* `index` index 

#### Returns
if setting was successful

#### `public inline bool `[`append_element`](#classshogun_1_1DynArray_1ad7980b73fe2e1b9695305017e111b72a)`(T element)` {#classshogun_1_1DynArray_1ad7980b73fe2e1b9695305017e111b72a}

append array element to the end of array

#### Parameters
* `element` element to append 

#### Returns
if setting was successful

#### `public inline void `[`push_back`](#classshogun_1_1DynArray_1ab1f08be94f07c176a1e76c38b3f4051e)`(T element)` {#classshogun_1_1DynArray_1ab1f08be94f07c176a1e76c38b3f4051e}

STD VECTOR compatible. Append array element to the end of array.

#### Parameters
* `element` element to append

#### `public inline void `[`pop_back`](#classshogun_1_1DynArray_1a058bda4957df6a97b1ea6c9fd783f672)`()` {#classshogun_1_1DynArray_1a058bda4957df6a97b1ea6c9fd783f672}

STD VECTOR compatible. Delete array element at the end of array.

#### `public inline T `[`back`](#classshogun_1_1DynArray_1a993054173e187eb9f15011f9fd3e2ad0)`() const` {#classshogun_1_1DynArray_1a993054173e187eb9f15011f9fd3e2ad0}

STD VECTOR compatible. Return array element at the end of array.

#### Returns
element at the end of array

#### `public inline int32_t `[`find_element`](#classshogun_1_1DynArray_1ac17f4a00028014c41476c4616e7ce5c5)`(T element) const` {#classshogun_1_1DynArray_1ac17f4a00028014c41476c4616e7ce5c5}

find first occurence of array element and return its index or -1 if not available

#### Parameters
* `element` element to search for 

#### Returns
index of element or -1

#### `public inline bool `[`delete_element`](#classshogun_1_1DynArray_1af1e028b3c9d27ca9cbf78ebec9e79b93)`(int32_t idx)` {#classshogun_1_1DynArray_1af1e028b3c9d27ca9cbf78ebec9e79b93}

delete array element at idx (does not call SG_FREE() or the like)

#### Parameters
* `idx` index 

#### Returns
if deleting was successful

#### `public inline bool `[`resize_array`](#classshogun_1_1DynArray_1ab87b186ee33f8bc8b309a1d7e26c9226)`(int32_t n,bool exact_resize)` {#classshogun_1_1DynArray_1ab87b186ee33f8bc8b309a1d7e26c9226}

resize the array

#### Parameters
* `n` new size 

* `exact_resize` resize exactly to size n 

#### Returns
if resizing was successful

#### `public inline T * `[`get_array`](#classshogun_1_1DynArray_1ae5e97a64694ed7fd85475d6790e03014)`() const` {#classshogun_1_1DynArray_1ae5e97a64694ed7fd85475d6790e03014}

get the array call get_array just before messing with it DO NOT call any [],resize/delete functions after [get_array()](#classshogun_1_1DynArray_1ae5e97a64694ed7fd85475d6790e03014), the pointer may become invalid !

#### Returns
the array

#### `public inline void `[`set_array`](#classshogun_1_1DynArray_1a639546225a9e65c593356d4094373c1b)`(T * p_array,int32_t p_num_elements,int32_t p_array_size,bool p_free_array,bool p_copy_array)` {#classshogun_1_1DynArray_1a639546225a9e65c593356d4094373c1b}

set the array pointer and free previously allocated memory

#### Parameters
* `p_array` new array 

* `p_num_elements` last element index + 1 

* `p_array_size` number of elements in array 

* `p_free_array` if array must be freed 

* `p_copy_array` if array must be copied

#### `public inline void `[`set_array`](#classshogun_1_1DynArray_1a774b4a8eec6cdf7a8276cbfc4bd173af)`(const T * p_array,int32_t p_num_elements,int32_t p_array_size)` {#classshogun_1_1DynArray_1a774b4a8eec6cdf7a8276cbfc4bd173af}

set the array pointer and free previously allocated memory

#### Parameters
* `p_array` new array 

* `p_num_elements` last element index + 1 

* `p_array_size` number of elements in array

#### `public inline void `[`clear_array`](#classshogun_1_1DynArray_1a402b94aecfa928ab094bb30e6eee362a)`(T value)` {#classshogun_1_1DynArray_1a402b94aecfa928ab094bb30e6eee362a}

clear the array (with e.g. zeros)

#### `public inline void `[`reset`](#classshogun_1_1DynArray_1a7d6ba3006015c7435c085ac716d147f0)`(T value)` {#classshogun_1_1DynArray_1a7d6ba3006015c7435c085ac716d147f0}

resets the array (as if it was just created), keeps granularity

#### `public inline void `[`shuffle`](#classshogun_1_1DynArray_1a1905fe84eb39f020b32c58baf7a76758)`()` {#classshogun_1_1DynArray_1a1905fe84eb39f020b32c58baf7a76758}

randomizes the array (not thread safe!)

#### `public inline void `[`shuffle`](#classshogun_1_1DynArray_1aab5aeea2dba53b2995b58f400be7db1a)`(`[`CRandom`](#classshogun_1_1CRandom)` * rand)` {#classshogun_1_1DynArray_1aab5aeea2dba53b2995b58f400be7db1a}

randomizes the array with external random state

#### `public inline void `[`set_const`](#classshogun_1_1DynArray_1a9eaae66fe81b1044e644767c5871e0df)`(const T & const_element)` {#classshogun_1_1DynArray_1a9eaae66fe81b1044e644767c5871e0df}

set array with a constant

#### `public inline T `[`operator[]`](#classshogun_1_1DynArray_1afd0d0238c34b1c884ea601b11bf52114)`(int32_t index) const` {#classshogun_1_1DynArray_1afd0d0238c34b1c884ea601b11bf52114}

operator overload for array read only access use [set_element()](#classshogun_1_1DynArray_1adf49331c5643dc4d1cf004375ca76001) for write access (will also make the array dynamically grow)

DOES NOT DO ANY BOUNDS CHECKING

#### Parameters
* `index` index 

#### Returns
element at index

#### `public inline `[`DynArray`](#classshogun_1_1DynArray)`< T > & `[`operator=`](#classshogun_1_1DynArray_1a96c0e6582aedead2042950ca170efc80)`(`[`DynArray`](#classshogun_1_1DynArray)`< T > & orig)` {#classshogun_1_1DynArray_1a96c0e6582aedead2042950ca170efc80}

operator overload for array assignment. Left array is resized if needed.

#### Parameters
* `orig` original array 

#### Returns
new array

#### `public inline virtual const char * `[`get_name`](#classshogun_1_1DynArray_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` {#classshogun_1_1DynArray_1a9cb485686dd7a1e6f7103cf42e87717e}

#### Returns
object name

#### `protected int32_t `[`resize_granularity`](#classshogun_1_1DynArray_1a364caf1df30c6dce6a711586c568be26) {#classshogun_1_1DynArray_1a364caf1df30c6dce6a711586c568be26}

shrink/grow step size

#### `protected T * `[`array`](#classshogun_1_1DynArray_1a189874643dd3d326549d72b097665049) {#classshogun_1_1DynArray_1a189874643dd3d326549d72b097665049}

memory for dynamic array

#### `protected int32_t `[`num_elements`](#classshogun_1_1DynArray_1a481f2cd05e67d8830f548ec248ea1d92) {#classshogun_1_1DynArray_1a481f2cd05e67d8830f548ec248ea1d92}

the number of potentially used elements in array

#### `protected int32_t `[`current_num_elements`](#classshogun_1_1DynArray_1ace070cc900bca005910d53f39ea6897c) {#classshogun_1_1DynArray_1ace070cc900bca005910d53f39ea6897c}

the number of currently used elements

#### `protected bool `[`use_sg_mallocs`](#classshogun_1_1DynArray_1ad358739efb565b48bd00586384106310) {#classshogun_1_1DynArray_1ad358739efb565b48bd00586384106310}

whether SG_MALLOC or just malloc etc shall be used

#### `protected bool `[`free_array`](#classshogun_1_1DynArray_1a8523f3d4c8bf61a18c074aceaa8fddd3) {#classshogun_1_1DynArray_1a8523f3d4c8bf61a18c074aceaa8fddd3}

if array must be freed

