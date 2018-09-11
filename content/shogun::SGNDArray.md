---
classname: "shogun::SGNDArray"
type: "class"
parents:
   - SGReferencedData
---

# class `shogun::SGNDArray` {#classshogun_1_1SGNDArray}

```
class shogun::SGNDArray
  : public SGReferencedData
```

shogun n-dimensional array

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public T * `[`array`](#classshogun_1_1SGNDArray_1a189874643dd3d326549d72b097665049) | array
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * `[`dims`](#classshogun_1_1SGNDArray_1a3fc1cec95c3bb8c6d0b4a2abdf6d79ef) | dimension sizes
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`num_dims`](#classshogun_1_1SGNDArray_1a106ca2d70063bf85da5cb08fa1ec9f26) | number of dimensions
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`len_array`](#classshogun_1_1SGNDArray_1a5f4cfabc7d19206cd8f298e909362bb5) | the flatten length of the N-d array
`public  `[`SGNDArray`](#classshogun_1_1SGNDArray_1a30b8053061887942d0f4179d1dc0be8f)`()` | default constructor
`public  `[`SGNDArray`](#classshogun_1_1SGNDArray_1a109bd3d4a387c0c94fdd8c751f3cbc77)`(T * a,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * d,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` nd,bool ref_counting)` | constructor for setting params
`public  `[`SGNDArray`](#classshogun_1_1SGNDArray_1aaa727e63be90beea4e251229f19d42c0)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * d,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` nd,bool ref_counting)` | constructor to create new ndarray in memory
`public  `[`SGNDArray`](#classshogun_1_1SGNDArray_1af46de04a1edc057e3c433ab3aea117c6)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > d,bool ref_counting)` | constructor to create new ndarray of given bases
`public  `[`SGNDArray`](#classshogun_1_1SGNDArray_1aae0d01885912e5df9030ace3179e3123)`(const `[`SGNDArray`](#classshogun_1_1SGNDArray)` & orig)` | copy constructor
`public virtual  `[`~SGNDArray`](#classshogun_1_1SGNDArray_1a2ed772e51695d2a436cd87872fc72908)`()` | empty destructor
`public `[`SGNDArray`](#classshogun_1_1SGNDArray)`< T > `[`clone`](#classshogun_1_1SGNDArray_1ac8f6e6dca567578ce2f1307a0c7db484)`() const` | #### Returns
`public inline T * `[`get_matrix`](#classshogun_1_1SGNDArray_1a5ef1c26850517e2ec80b8e5c7453e93e)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` matIdx) const` | get a matrix formed by the two first dimensions
`public void `[`transpose_matrix`](#classshogun_1_1SGNDArray_1afc3d17c4bd5cb695dfa289771da59d87)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` matIdx) const` | transposes a matrix formed by the two first dimensions
`public inline const T & `[`operator[]`](#classshogun_1_1SGNDArray_1a1ba5350612032058f4c1e531b6f155a5)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index) const` | operator overload for ndarray read only access
`public inline T & `[`operator[]`](#classshogun_1_1SGNDArray_1abe0aa2d215384e9de7b5bf3163d15d9e)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index)` | operator overload for ndarray r/w access
`public `[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > `[`get_dimensions`](#classshogun_1_1SGNDArray_1a2ed20d046e754c85f939b0134ed7f1cd)`() const` | #### Returns
`public void `[`set_const`](#classshogun_1_1SGNDArray_1a8bce01a1fc41a734d9b5cf1533fd7a2a)`(T const_elem)` | set N-d array to a constant
`public `[`SGNDArray`](#classshogun_1_1SGNDArray)`< T > & `[`operator*=`](#classshogun_1_1SGNDArray_1a5058d8c51345ee9ee6cd99a41c74bc0c)`(T val)` | operator overload of multiplication assignment
`public `[`SGNDArray`](#classshogun_1_1SGNDArray)`< T > & `[`operator+=`](#classshogun_1_1SGNDArray_1a41ad1e2561a87fb31add3c711bc39f59)`(`[`SGNDArray`](#classshogun_1_1SGNDArray)` & ndarray)` | operator overload of addition assignment
`public `[`SGNDArray`](#classshogun_1_1SGNDArray)`< T > & `[`operator-=`](#classshogun_1_1SGNDArray_1a9a06f3762e040a6a8d72ea8fdd81c9d6)`(`[`SGNDArray`](#classshogun_1_1SGNDArray)` & ndarray)` | operator overload of subtruction assignment
`public T `[`max_element`](#classshogun_1_1SGNDArray_1a747ac360136411a831356f6a6c554e94)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` & max_at)` | find the maximum value of the elements
`public void `[`expand`](#classshogun_1_1SGNDArray_1aca087b638c8cbd881aa2369a24a690d9)`(`[`SGNDArray`](#classshogun_1_1SGNDArray)` & big_array,`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > & axes)` | expand to a big size array
`public T `[`get_value`](#classshogun_1_1SGNDArray_1a7f27ff9856085ab8b68721b1e7108b1d)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > index) const` | get the value at index
`public void `[`next_index`](#classshogun_1_1SGNDArray_1a2929dc8a2a72eedba0bbee7c6407449e)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > & curr_index) const` | get the next index from the current one
`public template<>`  <br/>[`SGNDArray`](#classshogun_1_1SGNDArray)`< bool > & `[`operator*=`](#classshogun_1_1SGNDArray_1ac1a1856287ec16b9308aba76f75a146e)`(bool val)` | 
`public template<>`  <br/>[`SGNDArray`](#classshogun_1_1SGNDArray)`< char > & `[`operator*=`](#classshogun_1_1SGNDArray_1a034041c51f798967dc844792614c7886)`(char val)` | 
`public template<>`  <br/>[`SGNDArray`](#classshogun_1_1SGNDArray)`< bool > & `[`operator+=`](#classshogun_1_1SGNDArray_1a04670b6240914a438c20f382d2ae1b2c)`(`[`SGNDArray`](#classshogun_1_1SGNDArray)` & ndarray)` | 
`public template<>`  <br/>[`SGNDArray`](#classshogun_1_1SGNDArray)`< char > & `[`operator+=`](#classshogun_1_1SGNDArray_1ae0752ce3e759f83ebf7261923f669ebf)`(`[`SGNDArray`](#classshogun_1_1SGNDArray)` & ndarray)` | 
`public template<>`  <br/>[`SGNDArray`](#classshogun_1_1SGNDArray)`< bool > & `[`operator-=`](#classshogun_1_1SGNDArray_1a931a630f3cbc6262362fd8de8bce0d75)`(`[`SGNDArray`](#classshogun_1_1SGNDArray)` & ndarray)` | 
`public template<>`  <br/>[`SGNDArray`](#classshogun_1_1SGNDArray)`< char > & `[`operator-=`](#classshogun_1_1SGNDArray_1acd7550f21024c8df54c044f39659840c)`(`[`SGNDArray`](#classshogun_1_1SGNDArray)` & ndarray)` | 
`public template<>`  <br/>`bool `[`max_element`](#classshogun_1_1SGNDArray_1a69746f6efb0ba22547da092e3e87f09a)`(int32_t & max_at)` | 
`public template<>`  <br/>`char `[`max_element`](#classshogun_1_1SGNDArray_1a81253e62b3a6a78102c51ede535d8643)`(int32_t & max_at)` | 
`public int32_t `[`ref_count`](#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d)`()` | display reference counter
`protected virtual void `[`copy_data`](#classshogun_1_1SGNDArray_1a6e8ddd37b0b245f7cca418642762e16b)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` | copy data
`protected virtual void `[`init_data`](#classshogun_1_1SGNDArray_1a3b42d3bd68c5200393c1f0809ed1facf)`()` | init data
`protected virtual void `[`free_data`](#classshogun_1_1SGNDArray_1ab340ce24b1c9d2b26ab2b46a7a64c346)`()` | free data
`protected void `[`copy_refcount`](#classshogun_1_1SGReferencedData_1a253175a13e8af17d4f2a2cfd9e14dd63)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` | copy refcount
`protected int32_t `[`ref`](#classshogun_1_1SGReferencedData_1ab8c24b912ee57d3f2c81ecccd083582a)`()` | increase reference counter
`protected int32_t `[`unref`](#classshogun_1_1SGReferencedData_1ad99bde1a142a1c07a963169123166e01)`()` | decrement reference counter and deallocate object if refcount is zero before or after decrementing it

## Members

#### `public T * `[`array`](#classshogun_1_1SGNDArray_1a189874643dd3d326549d72b097665049) {#classshogun_1_1SGNDArray_1a189874643dd3d326549d72b097665049}

array

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * `[`dims`](#classshogun_1_1SGNDArray_1a3fc1cec95c3bb8c6d0b4a2abdf6d79ef) {#classshogun_1_1SGNDArray_1a3fc1cec95c3bb8c6d0b4a2abdf6d79ef}

dimension sizes

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`num_dims`](#classshogun_1_1SGNDArray_1a106ca2d70063bf85da5cb08fa1ec9f26) {#classshogun_1_1SGNDArray_1a106ca2d70063bf85da5cb08fa1ec9f26}

number of dimensions

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`len_array`](#classshogun_1_1SGNDArray_1a5f4cfabc7d19206cd8f298e909362bb5) {#classshogun_1_1SGNDArray_1a5f4cfabc7d19206cd8f298e909362bb5}

the flatten length of the N-d array

#### `public  `[`SGNDArray`](#classshogun_1_1SGNDArray_1a30b8053061887942d0f4179d1dc0be8f)`()` {#classshogun_1_1SGNDArray_1a30b8053061887942d0f4179d1dc0be8f}

default constructor

#### `public  `[`SGNDArray`](#classshogun_1_1SGNDArray_1a109bd3d4a387c0c94fdd8c751f3cbc77)`(T * a,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * d,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` nd,bool ref_counting)` {#classshogun_1_1SGNDArray_1a109bd3d4a387c0c94fdd8c751f3cbc77}

constructor for setting params

#### Parameters
* `a` data of the array 

* `d` dimentions of the array 

* `nd` number of dimentions 

* `ref_counting` if true, count the reference

#### `public  `[`SGNDArray`](#classshogun_1_1SGNDArray_1aaa727e63be90beea4e251229f19d42c0)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * d,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` nd,bool ref_counting)` {#classshogun_1_1SGNDArray_1aaa727e63be90beea4e251229f19d42c0}

constructor to create new ndarray in memory

#### Parameters
* `d` dimentions of the array 

* `nd` number of dimentions 

* `ref_counting` if true, count the reference

#### `public  `[`SGNDArray`](#classshogun_1_1SGNDArray_1af46de04a1edc057e3c433ab3aea117c6)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > d,bool ref_counting)` {#classshogun_1_1SGNDArray_1af46de04a1edc057e3c433ab3aea117c6}

constructor to create new ndarray of given bases

#### Parameters
* `d` dimentions of the array 

* `ref_counting` if true, count the reference

#### `public  `[`SGNDArray`](#classshogun_1_1SGNDArray_1aae0d01885912e5df9030ace3179e3123)`(const `[`SGNDArray`](#classshogun_1_1SGNDArray)` & orig)` {#classshogun_1_1SGNDArray_1aae0d01885912e5df9030ace3179e3123}

copy constructor

#### Parameters
* `orig` the original N-d array

#### `public virtual  `[`~SGNDArray`](#classshogun_1_1SGNDArray_1a2ed772e51695d2a436cd87872fc72908)`()` {#classshogun_1_1SGNDArray_1a2ed772e51695d2a436cd87872fc72908}

empty destructor

#### `public `[`SGNDArray`](#classshogun_1_1SGNDArray)`< T > `[`clone`](#classshogun_1_1SGNDArray_1ac8f6e6dca567578ce2f1307a0c7db484)`() const` {#classshogun_1_1SGNDArray_1ac8f6e6dca567578ce2f1307a0c7db484}

#### Returns
the cloned N-d array

#### `public inline T * `[`get_matrix`](#classshogun_1_1SGNDArray_1a5ef1c26850517e2ec80b8e5c7453e93e)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` matIdx) const` {#classshogun_1_1SGNDArray_1a5ef1c26850517e2ec80b8e5c7453e93e}

get a matrix formed by the two first dimensions

#### Parameters
* `matIdx` matrix index 

#### Returns
pointer to the matrix

#### `public void `[`transpose_matrix`](#classshogun_1_1SGNDArray_1afc3d17c4bd5cb695dfa289771da59d87)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` matIdx) const` {#classshogun_1_1SGNDArray_1afc3d17c4bd5cb695dfa289771da59d87}

transposes a matrix formed by the two first dimensions

#### Parameters
* `matIdx` matrix index

#### `public inline const T & `[`operator[]`](#classshogun_1_1SGNDArray_1a1ba5350612032058f4c1e531b6f155a5)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index) const` {#classshogun_1_1SGNDArray_1a1ba5350612032058f4c1e531b6f155a5}

operator overload for ndarray read only access

#### Parameters
* `index` to access

#### `public inline T & `[`operator[]`](#classshogun_1_1SGNDArray_1abe0aa2d215384e9de7b5bf3163d15d9e)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index)` {#classshogun_1_1SGNDArray_1abe0aa2d215384e9de7b5bf3163d15d9e}

operator overload for ndarray r/w access

#### Parameters
* `index` to access

#### `public `[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > `[`get_dimensions`](#classshogun_1_1SGNDArray_1a2ed20d046e754c85f939b0134ed7f1cd)`() const` {#classshogun_1_1SGNDArray_1a2ed20d046e754c85f939b0134ed7f1cd}

#### Returns
dimentions of the N-d array

#### `public void `[`set_const`](#classshogun_1_1SGNDArray_1a8bce01a1fc41a734d9b5cf1533fd7a2a)`(T const_elem)` {#classshogun_1_1SGNDArray_1a8bce01a1fc41a734d9b5cf1533fd7a2a}

set N-d array to a constant

#### Parameters
* `const_elem` constant value to set N-d array to

#### `public `[`SGNDArray`](#classshogun_1_1SGNDArray)`< T > & `[`operator*=`](#classshogun_1_1SGNDArray_1a5058d8c51345ee9ee6cd99a41c74bc0c)`(T val)` {#classshogun_1_1SGNDArray_1a5058d8c51345ee9ee6cd99a41c74bc0c}

operator overload of multiplication assignment

#### Parameters
* `val` a scalar value to multiply 

#### Returns
the result N-d array

#### `public `[`SGNDArray`](#classshogun_1_1SGNDArray)`< T > & `[`operator+=`](#classshogun_1_1SGNDArray_1a41ad1e2561a87fb31add3c711bc39f59)`(`[`SGNDArray`](#classshogun_1_1SGNDArray)` & ndarray)` {#classshogun_1_1SGNDArray_1a41ad1e2561a87fb31add3c711bc39f59}

operator overload of addition assignment

#### Parameters
* `ndarray` N-d array to add 

#### Returns
the result N-d array

#### `public `[`SGNDArray`](#classshogun_1_1SGNDArray)`< T > & `[`operator-=`](#classshogun_1_1SGNDArray_1a9a06f3762e040a6a8d72ea8fdd81c9d6)`(`[`SGNDArray`](#classshogun_1_1SGNDArray)` & ndarray)` {#classshogun_1_1SGNDArray_1a9a06f3762e040a6a8d72ea8fdd81c9d6}

operator overload of subtruction assignment

#### Parameters
* `ndarray` N-d array to add 

#### Returns
the result N-d array

#### `public T `[`max_element`](#classshogun_1_1SGNDArray_1a747ac360136411a831356f6a6c554e94)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` & max_at)` {#classshogun_1_1SGNDArray_1a747ac360136411a831356f6a6c554e94}

find the maximum value of the elements

#### Parameters
* `max_at` the index of the maximum element, index is in 1-d flattend array. If there are multiple maximum element, return the last index. 

#### Returns
the maximum value

#### `public void `[`expand`](#classshogun_1_1SGNDArray_1aca087b638c8cbd881aa2369a24a690d9)`(`[`SGNDArray`](#classshogun_1_1SGNDArray)` & big_array,`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > & axes)` {#classshogun_1_1SGNDArray_1aca087b638c8cbd881aa2369a24a690d9}

expand to a big size array

#### Parameters
* `big_array` the target big size array 

* `axes` the axis where the current ndarray will be replicated

#### `public T `[`get_value`](#classshogun_1_1SGNDArray_1a7f27ff9856085ab8b68721b1e7108b1d)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > index) const` {#classshogun_1_1SGNDArray_1a7f27ff9856085ab8b68721b1e7108b1d}

get the value at index

#### Parameters
* `index` vector of indices where the value to retrieve of the array is located 

#### Returns
the value at index

#### `public void `[`next_index`](#classshogun_1_1SGNDArray_1a2929dc8a2a72eedba0bbee7c6407449e)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > & curr_index) const` {#classshogun_1_1SGNDArray_1a2929dc8a2a72eedba0bbee7c6407449e}

get the next index from the current one

#### Parameters
* `curr_index` the current index

#### `public template<>`  <br/>[`SGNDArray`](#classshogun_1_1SGNDArray)`< bool > & `[`operator*=`](#classshogun_1_1SGNDArray_1ac1a1856287ec16b9308aba76f75a146e)`(bool val)` {#classshogun_1_1SGNDArray_1ac1a1856287ec16b9308aba76f75a146e}

#### `public template<>`  <br/>[`SGNDArray`](#classshogun_1_1SGNDArray)`< char > & `[`operator*=`](#classshogun_1_1SGNDArray_1a034041c51f798967dc844792614c7886)`(char val)` {#classshogun_1_1SGNDArray_1a034041c51f798967dc844792614c7886}

#### `public template<>`  <br/>[`SGNDArray`](#classshogun_1_1SGNDArray)`< bool > & `[`operator+=`](#classshogun_1_1SGNDArray_1a04670b6240914a438c20f382d2ae1b2c)`(`[`SGNDArray`](#classshogun_1_1SGNDArray)` & ndarray)` {#classshogun_1_1SGNDArray_1a04670b6240914a438c20f382d2ae1b2c}

#### `public template<>`  <br/>[`SGNDArray`](#classshogun_1_1SGNDArray)`< char > & `[`operator+=`](#classshogun_1_1SGNDArray_1ae0752ce3e759f83ebf7261923f669ebf)`(`[`SGNDArray`](#classshogun_1_1SGNDArray)` & ndarray)` {#classshogun_1_1SGNDArray_1ae0752ce3e759f83ebf7261923f669ebf}

#### `public template<>`  <br/>[`SGNDArray`](#classshogun_1_1SGNDArray)`< bool > & `[`operator-=`](#classshogun_1_1SGNDArray_1a931a630f3cbc6262362fd8de8bce0d75)`(`[`SGNDArray`](#classshogun_1_1SGNDArray)` & ndarray)` {#classshogun_1_1SGNDArray_1a931a630f3cbc6262362fd8de8bce0d75}

#### `public template<>`  <br/>[`SGNDArray`](#classshogun_1_1SGNDArray)`< char > & `[`operator-=`](#classshogun_1_1SGNDArray_1acd7550f21024c8df54c044f39659840c)`(`[`SGNDArray`](#classshogun_1_1SGNDArray)` & ndarray)` {#classshogun_1_1SGNDArray_1acd7550f21024c8df54c044f39659840c}

#### `public template<>`  <br/>`bool `[`max_element`](#classshogun_1_1SGNDArray_1a69746f6efb0ba22547da092e3e87f09a)`(int32_t & max_at)` {#classshogun_1_1SGNDArray_1a69746f6efb0ba22547da092e3e87f09a}

#### `public template<>`  <br/>`char `[`max_element`](#classshogun_1_1SGNDArray_1a81253e62b3a6a78102c51ede535d8643)`(int32_t & max_at)` {#classshogun_1_1SGNDArray_1a81253e62b3a6a78102c51ede535d8643}

#### `public int32_t `[`ref_count`](#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d)`()` {#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d}

display reference counter

#### Returns
reference count

#### `protected virtual void `[`copy_data`](#classshogun_1_1SGNDArray_1a6e8ddd37b0b245f7cca418642762e16b)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` {#classshogun_1_1SGNDArray_1a6e8ddd37b0b245f7cca418642762e16b}

copy data

#### `protected virtual void `[`init_data`](#classshogun_1_1SGNDArray_1a3b42d3bd68c5200393c1f0809ed1facf)`()` {#classshogun_1_1SGNDArray_1a3b42d3bd68c5200393c1f0809ed1facf}

init data

#### `protected virtual void `[`free_data`](#classshogun_1_1SGNDArray_1ab340ce24b1c9d2b26ab2b46a7a64c346)`()` {#classshogun_1_1SGNDArray_1ab340ce24b1c9d2b26ab2b46a7a64c346}

free data

#### `protected void `[`copy_refcount`](#classshogun_1_1SGReferencedData_1a253175a13e8af17d4f2a2cfd9e14dd63)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` {#classshogun_1_1SGReferencedData_1a253175a13e8af17d4f2a2cfd9e14dd63}

copy refcount

#### `protected int32_t `[`ref`](#classshogun_1_1SGReferencedData_1ab8c24b912ee57d3f2c81ecccd083582a)`()` {#classshogun_1_1SGReferencedData_1ab8c24b912ee57d3f2c81ecccd083582a}

increase reference counter

#### Returns
reference count

#### `protected int32_t `[`unref`](#classshogun_1_1SGReferencedData_1ad99bde1a142a1c07a963169123166e01)`()` {#classshogun_1_1SGReferencedData_1ad99bde1a142a1c07a963169123166e01}

decrement reference counter and deallocate object if refcount is zero before or after decrementing it

#### Returns
reference count

