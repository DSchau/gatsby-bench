---
classname: "shogun::SGVector"
type: "class"
parents:
   - SGReferencedData
---

# class `shogun::SGVector` {#classshogun_1_1SGVector}

```
class shogun::SGVector
  : public SGReferencedData
```

shogun vector

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public T * `[`vector`](#classshogun_1_1SGVector_1a905c8bc77954df48218ead2e733588a2) | Pointer to memory where vector data is stored
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`vlen`](#classshogun_1_1SGVector_1a1337b82cd4f21b627937dd9032e0fddf) | Length of vector
`public std::shared_ptr< `[`GPUMemoryBase`](#structshogun_1_1GPUMemoryBase)`< T > > `[`gpu_ptr`](#classshogun_1_1SGVector_1af119f089106467dfd9eb1ecf6c50d36e) | GPU Vector structure. Stores pointer to the data on GPU.
`public  `[`SGVector`](#classshogun_1_1SGVector_1a500ad9eaca65225e132519b295fb8a30)`()` | Default constructor
`public  `[`SGVector`](#classshogun_1_1SGVector_1aadea20eac5565637f1c91ba566806ecc)`(T * v,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` len,bool ref_counting)` | Constructor for setting params
`public  `[`SGVector`](#classshogun_1_1SGVector_1a994c01488abc14175f054b175ec1c26a)`(T * m,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` len,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` offset)` | Wraps a vector around an existing memory segment with an offset
`public  `[`SGVector`](#classshogun_1_1SGVector_1a35fab3f50fb002918edc729b07c88795)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` len,bool ref_counting)` | Constructor to create new vector in memory
`public  `[`SGVector`](#classshogun_1_1SGVector_1a7c5a0abf31545d49450a4c685888f365)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > matrix)` | Constructor to create new vector from a [SGMatrix](#classshogun_1_1SGMatrix)
`public  `[`SGVector`](#classshogun_1_1SGVector_1ad5be3f2746de4a83e606965df9e156a6)`(`[`GPUMemoryBase`](#structshogun_1_1GPUMemoryBase)`< T > * vector,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` len)` | Construct [SGVector](#classshogun_1_1SGVector) from GPU memory.
`public  `[`SGVector`](#classshogun_1_1SGVector_1a4ed8072c7fe2e0866e4b1ae6e536ed5c)`(const `[`SGVector`](#classshogun_1_1SGVector)` & orig)` | Copy constructor
`public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` bool `[`on_gpu`](#classshogun_1_1SGVector_1a544d60c4a40021806165381020ea7d49)`() const` | Check whether data is stored on GPU
`public template<>`  <br/>`inline  `[`SGVector`](#classshogun_1_1SGVector_1a624c442bf7a7a4a7167376a791ee8aec)`(InputIt beginIt,InputIt endIt)` | Construct [SGVector](#classshogun_1_1SGVector) from InputIterator list
`public  `[`SGVector`](#classshogun_1_1SGVector_1a39e91472fabff989ff8b6a962edc570f)`(std::initializer_list< T > il)` | Construct [SGVector](#classshogun_1_1SGVector) from initializer list
`public  `[`SGVector`](#classshogun_1_1SGVector_1ab85bd639cf67c8be088f5f973f03ca9f)`(`[`EigenVectorXt`](#classshogun_1_1SGVector_1aa375779ac932b2c2e5460d5c90ea4560)` & vec)` | Wraps a matrix around the data of an Eigen3 column vector
`public  `[`SGVector`](#classshogun_1_1SGVector_1a018c03a0d0c33c6e05193ccf1cd2bf43)`(`[`EigenRowVectorXt`](#classshogun_1_1SGVector_1abd19ffc32ed839e3291975a2c6de019c)` & vec)` | Wraps a matrix around the data of an Eigen3 row vector
`public  `[`operator EigenVectorXtMap`](#classshogun_1_1SGVector_1acf96ae8cc160517b73fb359fc8f01032)`() const` | Wraps an Eigen3 column vector around the data of this matrix
`public  `[`operator EigenRowVectorXtMap`](#classshogun_1_1SGVector_1a31463522561a228104f4a483b9aea763)`() const` | Wraps an Eigen3 row vector around the data of this matrix
`public template<>`  <br/>`inline `[`SGVector`](#classshogun_1_1SGVector)`< X > `[`as`](#classshogun_1_1SGVector_1ac4af18bd5ed67b691d19bab86943f766)`() const` | #### Returns
`public void `[`set_const`](#classshogun_1_1SGVector_1a8bce01a1fc41a734d9b5cf1533fd7a2a)`(T const_elem)` | Set vector to a constant
`public inline `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`get`](#classshogun_1_1SGVector_1abd42845babdeb77fb02544720672ad55)`()` | Get the vector (no copying is done here)
`public void `[`set`](#classshogun_1_1SGVector_1a69169ab99ab307a13c834a3dc8b145f3)`(`[`SGVector`](#classshogun_1_1SGVector)`< T > orig)` | [Wrapper](#classWrapper) for the copy constructor useful for SWIG interfaces
`public virtual  `[`~SGVector`](#classshogun_1_1SGVector_1a872738a61edf5bb223f62385620e414e)`()` | [Empty](#structshogun_1_1Empty) destructor
`public inline int32_t `[`size`](#classshogun_1_1SGVector_1aa74e951f7370eb093717d70852a96981)`() const` | Size
`public inline T * `[`data`](#classshogun_1_1SGVector_1a2a1c4b452e7e2523397112c12e53554d)`() const` | Data pointer
`public inline `[`iterator`](#classshogun_1_1SGVector_1a88be8e03f7fa96234ccab7620a598fc0)` `[`begin`](#classshogun_1_1SGVector_1a979556eb331ec35eb33472a90a160f99)`() noexcept` | Returns an iterator to the first element of the container.
`public inline `[`iterator`](#classshogun_1_1SGVector_1a88be8e03f7fa96234ccab7620a598fc0)` `[`end`](#classshogun_1_1SGVector_1afc5380afa64b233d0df01a147616974b)`() noexcept` | Returns an iterator to the element following the last element of the container.
`public `[`SGVector`](#classshogun_1_1SGVector)`< T > & `[`operator=`](#classshogun_1_1SGVector_1aef82a5b8c4bdb525b1914f9a7d87603c)`(const `[`SGVector`](#classshogun_1_1SGVector)`< T > &)` | 
`public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` bool `[`operator==`](#classshogun_1_1SGVector_1a893af62a5fd79f330602eea8ff7620a9)`(const `[`SGVector`](#classshogun_1_1SGVector)`< T > & other) const` | Check for pointer identity
`public inline  `[`operator T*`](#classshogun_1_1SGVector_1adec4d6e4697fff19761dfb957ab203f2)`()` | Cast to pointer
`public void `[`zero`](#classshogun_1_1SGVector_1a0c4493a5d4723940d60164428f11adc3)`()` | Fill vector with zeros
`public void `[`range_fill`](#classshogun_1_1SGVector_1a11b4c18177e9a7dede674f8fe17d7423)`(T start)` | [Range](#classshogun_1_1Range) fill a vector with start...start+len-1
`public void `[`random`](#classshogun_1_1SGVector_1ad1e32b145eab46d794beb9e843b6e75f)`(T min_value,T max_value)` | Create random vector
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`find_position_to_insert`](#classshogun_1_1SGVector_1a54864150f4afaae2b3c296c09cb959cf)`(T element)` | For a sorted (ascending) vector, gets the index after the first element that is smaller than the given one
`public `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`clone`](#classshogun_1_1SGVector_1a8c70cf9bddee5ff6f539440bcae8f588)`() const` | Clone vector
`public inline const T & `[`get_element`](#classshogun_1_1SGVector_1a6b164abcccd9703be8251fe2c15b8d52)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index)` | Get element at index
`public inline void `[`set_element`](#classshogun_1_1SGVector_1a69ccf7020114a13dab3c6c9328fa1ee9)`(const T & el,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index)` | Set element at index
`public void `[`resize_vector`](#classshogun_1_1SGVector_1aae00e2f4717f097787912c6154618d85)`(int32_t n)` | Resize vector, with zero padding
`public inline const T & `[`operator[]`](#classshogun_1_1SGVector_1a424c205cae88bebdda365c021d53aef3)`(uint64_t index) const` | Operator overload for vector read only access
`public inline const T & `[`operator[]`](#classshogun_1_1SGVector_1a073cf2868548922ab9413557a5ccc440)`(int64_t index) const` | Operator overload for vector read only access
`public inline const T & `[`operator[]`](#classshogun_1_1SGVector_1a0d1658a24941329c21d6c745836b53fc)`(uint32_t index) const` | Operator overload for vector read only access
`public inline const T & `[`operator[]`](#classshogun_1_1SGVector_1a7b3d713784d21d55dbf1dac4971e1e22)`(int32_t index) const` | Operator overload for vector read only access
`public inline T & `[`operator[]`](#classshogun_1_1SGVector_1afaea7e9ab8a70823710f1dda292e8f1d)`(uint64_t index)` | Operator overload for vector r/w access
`public inline T & `[`operator[]`](#classshogun_1_1SGVector_1adb496a4681a6577d8806fe898df655bc)`(int64_t index)` | Operator overload for vector r/w access
`public inline T & `[`operator[]`](#classshogun_1_1SGVector_1a30ccb7f0b69f16a83ea29fdf35af05b9)`(uint32_t index)` | Operator overload for vector r/w access
`public inline T & `[`operator[]`](#classshogun_1_1SGVector_1a9d1c553ca2a17db6b21dffc39fd76faa)`(int32_t index)` | Operator overload for vector r/w access
`public void `[`add`](#classshogun_1_1SGVector_1a60459a3d1df1b36e24553d9be628df39)`(const `[`SGVector`](#classshogun_1_1SGVector)`< T > x)` | Add vector to current vector
`public void `[`add`](#classshogun_1_1SGVector_1a6eca3993c68f7593ccb7eaca39791698)`(const `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< T > & x)` | Add sparse vector to current vector
`public void `[`add`](#classshogun_1_1SGVector_1a96054b9b2e36b780302f1ba4ef356e13)`(const T x)` | Add scalar to current vector
`public `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`operator+`](#classshogun_1_1SGVector_1ae6073f121e7989ca0da8c902e103bf11)`(`[`SGVector`](#classshogun_1_1SGVector)`< T > x)` | Addition operator
`public inline `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`operator+=`](#classshogun_1_1SGVector_1ae00ea426fb9fc39942321bb8d70173dc)`(`[`SGVector`](#classshogun_1_1SGVector)`< T > x)` | Inplace addition operator
`public inline `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`operator+=`](#classshogun_1_1SGVector_1a3c822178319cc502d469e64737eca247)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< T > & x)` | Inplace addition operator for sparse vector
`public bool `[`equals`](#classshogun_1_1SGVector_1a2e383a8551e463625d36c971c7fb4253)`(const `[`SGVector`](#classshogun_1_1SGVector)`< T > & other) const` | Equals method up to precision for vectors (element-wise) 
`public inline T `[`product`](#classshogun_1_1SGVector_1a170fcfdaca76669b6dace97b687ee6b9)`()` | Return product(vec)
`public `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`unique`](#classshogun_1_1SGVector_1a63cbc3d40ec664e6e30f4e06aaae40b2)`()` | Returns new vector with sorted unique elements of current
`public void `[`display_size`](#classshogun_1_1SGVector_1a525360b36eff026a5d3d61d163c45695)`() const` | Display array size
`public void `[`display_vector`](#classshogun_1_1SGVector_1ad2f0f71a9a20cd8747a4657ed6a76c64)`(const char * name,const char * prefix) const` | Display vector
`public `[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > `[`find`](#classshogun_1_1SGVector_1a1b644c84c08aa4ab8357c246a33f3d30)`(T elem)` | Find index for occurance of an element 
`public template<>`  <br/>`inline `[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > `[`find_if`](#classshogun_1_1SGVector_1a159412b7e46c731f4bd321c7450eb66e)`(Predicate p)` | Find index for elements where the predicate returns true 
`public void `[`scale`](#classshogun_1_1SGVector_1a21b3ad2091f6b9df71afed0efe9a7e62)`(T alpha)` | Scale vector inplace.
`public void `[`load`](#classshogun_1_1SGVector_1a5d33ec59a4be25056cca1f3b6691ad00)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` | Load vector from file
`public void `[`save`](#classshogun_1_1SGVector_1aff4d5355fe0d9b68bc8c71cd331c082e)`(`[`CFile`](#classshogun_1_1CFile)` * saver)` | Save vector to file
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_real`](#classshogun_1_1SGVector_1adda3bcff402b917a950e9022265f4f86)`()` | Real part of a complex128_t vector
`public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_imag`](#classshogun_1_1SGVector_1a7ab9a2f31b17d19e82cb4df9a20f9038)`()` | Imag part of a complex128_t vector
`public template<>`  <br/>`void `[`zero`](#classshogun_1_1SGVector_1ae9deeaac2eaad960a9cdddf810d29a35)`()` | 
`public template<>`  <br/>[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`find_position_to_insert`](#classshogun_1_1SGVector_1a5fd8069abc9898d45f142a53e51a1b28)`(`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` element)` | 
`public template<>`  <br/>`void `[`range_fill_vector`](#classshogun_1_1SGVector_1a482d503acdb8406697a73f08d37dfb31)`(`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` * vec,int32_t len,`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` start)` | 
`public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1aeece7ae9714fd9050479fb1d073312b2)`(const bool * vector,int32_t n,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1a8bc0638eccb42a7071f2ca7a26136a3e)`(const char * vector,int32_t n,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1a2dc56de234c0ffa70ee47d459ff57763)`(const uint8_t * vector,int32_t n,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1a0d4234c5c0ff73b315077796be0cbc9e)`(const int8_t * vector,int32_t n,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1afbb42c6b622c615d09eaab971f684a7d)`(const uint16_t * vector,int32_t n,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1a60a1866268a275f2c70fa170b5ed6c3f)`(const int16_t * vector,int32_t n,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1aef457ae0881aec468ac5fd8ab8fffffb)`(const int32_t * vector,int32_t n,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1a8382b955e2c95ee3e8d5018391072b8a)`(const uint32_t * vector,int32_t n,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1a1e665cb9ac8faa06ec8375d399c42637)`(const int64_t * vector,int32_t n,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1a4a5c7af3725445fa15a1e985236587b7)`(const uint64_t * vector,int32_t n,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1a4a5181e1b039c341f82d4f29dba2de9c)`(const `[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * vector,int32_t n,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1aa287361aca72c80ba56f1813bf0b2813)`(const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * vector,int32_t n,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1a7a2d7e819ccc3a3a3d2778e24a87af9f)`(const `[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` * vector,int32_t n,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1a1524864ebffbae5c88ee5bec78cc46ef)`(const `[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` * vector,int32_t n,const char * name,const char * prefix)` | 
`public template<>`  <br/>`void `[`vec1_plus_scalar_times_vec2`](#classshogun_1_1SGVector_1a723c55c5e11122a930396a92a5be8a6e)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * vec1,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` scalar,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * vec2,int32_t n)` | 
`public template<>`  <br/>`void `[`vec1_plus_scalar_times_vec2`](#classshogun_1_1SGVector_1aacd4fa660389283c7a1fc06006f215cf)`(`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * vec1,`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` scalar,const `[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * vec2,int32_t n)` | 
`public template<>`  <br/>`void `[`random_vector`](#classshogun_1_1SGVector_1af0ff9f1f4614e711f3177c41cdd05072)`(`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` * vec,int32_t len,`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` min_value,`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` max_value)` | 
`public template<>`  <br/>`bool `[`twonorm`](#classshogun_1_1SGVector_1ae227f8a6f1d174b92b4ae27c8c3f2b34)`(const bool * x,int32_t len)` | 
`public template<>`  <br/>`char `[`twonorm`](#classshogun_1_1SGVector_1a1f173951785f09b16b77044a00fc2919)`(const char * x,int32_t len)` | 
`public template<>`  <br/>`int8_t `[`twonorm`](#classshogun_1_1SGVector_1a3d1a57721943f087a46fc7d075ae05d2)`(const int8_t * x,int32_t len)` | 
`public template<>`  <br/>`uint8_t `[`twonorm`](#classshogun_1_1SGVector_1a7e09aace4224b135fb24f22f20623482)`(const uint8_t * x,int32_t len)` | 
`public template<>`  <br/>`int16_t `[`twonorm`](#classshogun_1_1SGVector_1a4e7b4ca02a6196112d9c79acf39e82ce)`(const int16_t * x,int32_t len)` | 
`public template<>`  <br/>`uint16_t `[`twonorm`](#classshogun_1_1SGVector_1a36e23200f86373f7b0421a01bb65d7b4)`(const uint16_t * x,int32_t len)` | 
`public template<>`  <br/>`int32_t `[`twonorm`](#classshogun_1_1SGVector_1ad3b22897ff6555a9ce71566e7f021efd)`(const int32_t * x,int32_t len)` | 
`public template<>`  <br/>`uint32_t `[`twonorm`](#classshogun_1_1SGVector_1a1e6d0ceb402793ae771251d2f2b6065b)`(const uint32_t * x,int32_t len)` | 
`public template<>`  <br/>`int64_t `[`twonorm`](#classshogun_1_1SGVector_1a6572308404ccad5f9e3068b2be1166ec)`(const int64_t * x,int32_t len)` | 
`public template<>`  <br/>`uint64_t `[`twonorm`](#classshogun_1_1SGVector_1a649aa558a5b5ff02da794629c0394e52)`(const uint64_t * x,int32_t len)` | 
`public template<>`  <br/>[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` `[`twonorm`](#classshogun_1_1SGVector_1a6a7328a5016619cae11f70ae1e9fc35f)`(const `[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * x,int32_t len)` | 
`public template<>`  <br/>[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`twonorm`](#classshogun_1_1SGVector_1af983afee23a79cf2637746dfe4f508d1)`(const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * v,int32_t n)` | 
`public template<>`  <br/>[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` `[`twonorm`](#classshogun_1_1SGVector_1a8c1c05aceeeeb3fcfbe3abd21270a62d)`(const `[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` * x,int32_t len)` | 
`public template<>`  <br/>[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` `[`twonorm`](#classshogun_1_1SGVector_1a6b96c38f04f9814b50507799fc67acbc)`(const `[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` * x,int32_t len)` | 
`public template<>`  <br/>[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` `[`qsq`](#classshogun_1_1SGVector_1a7884f1d515470f498f222f8d60635b72)`(`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` * x,int32_t len,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` q)` | 
`public template<>`  <br/>[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` `[`qnorm`](#classshogun_1_1SGVector_1a6766ea3fa31ff852f335dda7fded9fc8)`(`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` * x,int32_t len,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` q)` | 
`public template<>`  <br/>[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`sum_abs`](#classshogun_1_1SGVector_1af9e9603dd32c7d6c7f68aa0e4b933c98)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * vec,int32_t len)` | 
`public template<>`  <br/>[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` `[`sum_abs`](#classshogun_1_1SGVector_1a730a93fc7384fc0b36d3f13fc196ef1e)`(`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * vec,int32_t len)` | 
`public template<>`  <br/>`int32_t `[`unique`](#classshogun_1_1SGVector_1a24bf23298af779be67f7c67d33fbecba)`(`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` * output,int32_t size)` | 
`public template<>`  <br/>[`SGVector](#classshogun_1_1SGVector)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > `[`unique`](#classshogun_1_1SGVector_1aae255ad261dab440c1622f3630d0499e)`()` | 
`public template<>`  <br/>`void `[`scale_vector`](#classshogun_1_1SGVector_1a3a9df99976a9712a893d161688b6da0e)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` alpha,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * vec,int32_t len)` | 
`public template<>`  <br/>`void `[`scale_vector`](#classshogun_1_1SGVector_1a96ddba4d36874313750da8667ee19a6f)`(`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` alpha,`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * vec,int32_t len)` | 
`public template<>`  <br/>`void `[`load`](#classshogun_1_1SGVector_1a17763c63f0719b10922bc4ed6f392ec4)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` | 
`public template<>`  <br/>`void `[`save`](#classshogun_1_1SGVector_1aa61bf55fa90bee7cd7e92beaebe38774)`(`[`CFile`](#classshogun_1_1CFile)` * saver)` | 
`public int32_t `[`ref_count`](#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d)`()` | display reference counter
`protected virtual void `[`copy_data`](#classshogun_1_1SGVector_1a6e8ddd37b0b245f7cca418642762e16b)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` | needs to be overridden to copy data
`protected virtual void `[`init_data`](#classshogun_1_1SGVector_1a3b42d3bd68c5200393c1f0809ed1facf)`()` | needs to be overridden to initialize empty data
`protected virtual void `[`free_data`](#classshogun_1_1SGVector_1ab340ce24b1c9d2b26ab2b46a7a64c346)`()` | needs to be overridden to free data
`protected void `[`copy_refcount`](#classshogun_1_1SGReferencedData_1a253175a13e8af17d4f2a2cfd9e14dd63)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` | copy refcount
`protected int32_t `[`ref`](#classshogun_1_1SGReferencedData_1ab8c24b912ee57d3f2c81ecccd083582a)`()` | increase reference counter
`protected int32_t `[`unref`](#classshogun_1_1SGReferencedData_1ad99bde1a142a1c07a963169123166e01)`()` | decrement reference counter and deallocate object if refcount is zero before or after decrementing it
`typedef `[`iterator`](#classshogun_1_1SGVector_1a88be8e03f7fa96234ccab7620a598fc0) | 
`typedef `[`EigenVectorXt`](#classshogun_1_1SGVector_1aa375779ac932b2c2e5460d5c90ea4560) | 
`typedef `[`EigenRowVectorXt`](#classshogun_1_1SGVector_1abd19ffc32ed839e3291975a2c6de019c) | 
`typedef `[`EigenVectorXtMap`](#classshogun_1_1SGVector_1a228edb14803d0d1b9307af0439719b9b) | 
`typedef `[`EigenRowVectorXtMap`](#classshogun_1_1SGVector_1afa6ac3dbae224e01be833e7e2bc1c43c) | 
`typedef `[`Scalar`](#classshogun_1_1SGVector_1a47fdf58368a1d22e91e658ab30bfcda8) | The scalar type of the vector
`typedef `[`container_type`](#classshogun_1_1SGVector_1a5a578ed7540440e16d3f8bd5f7d1992b) | The container type for a given template argument

## Members

#### `public T * `[`vector`](#classshogun_1_1SGVector_1a905c8bc77954df48218ead2e733588a2) {#classshogun_1_1SGVector_1a905c8bc77954df48218ead2e733588a2}

Pointer to memory where vector data is stored

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`vlen`](#classshogun_1_1SGVector_1a1337b82cd4f21b627937dd9032e0fddf) {#classshogun_1_1SGVector_1a1337b82cd4f21b627937dd9032e0fddf}

Length of vector

#### `public std::shared_ptr< `[`GPUMemoryBase`](#structshogun_1_1GPUMemoryBase)`< T > > `[`gpu_ptr`](#classshogun_1_1SGVector_1af119f089106467dfd9eb1ecf6c50d36e) {#classshogun_1_1SGVector_1af119f089106467dfd9eb1ecf6c50d36e}

GPU Vector structure. Stores pointer to the data on GPU.

#### `public  `[`SGVector`](#classshogun_1_1SGVector_1a500ad9eaca65225e132519b295fb8a30)`()` {#classshogun_1_1SGVector_1a500ad9eaca65225e132519b295fb8a30}

Default constructor

#### `public  `[`SGVector`](#classshogun_1_1SGVector_1aadea20eac5565637f1c91ba566806ecc)`(T * v,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` len,bool ref_counting)` {#classshogun_1_1SGVector_1aadea20eac5565637f1c91ba566806ecc}

Constructor for setting params

#### `public  `[`SGVector`](#classshogun_1_1SGVector_1a994c01488abc14175f054b175ec1c26a)`(T * m,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` len,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` offset)` {#classshogun_1_1SGVector_1a994c01488abc14175f054b175ec1c26a}

Wraps a vector around an existing memory segment with an offset

#### `public  `[`SGVector`](#classshogun_1_1SGVector_1a35fab3f50fb002918edc729b07c88795)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` len,bool ref_counting)` {#classshogun_1_1SGVector_1a35fab3f50fb002918edc729b07c88795}

Constructor to create new vector in memory

#### `public  `[`SGVector`](#classshogun_1_1SGVector_1a7c5a0abf31545d49450a4c685888f365)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< T > matrix)` {#classshogun_1_1SGVector_1a7c5a0abf31545d49450a4c685888f365}

Constructor to create new vector from a [SGMatrix](#classshogun_1_1SGMatrix)

#### `public  `[`SGVector`](#classshogun_1_1SGVector_1ad5be3f2746de4a83e606965df9e156a6)`(`[`GPUMemoryBase`](#structshogun_1_1GPUMemoryBase)`< T > * vector,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` len)` {#classshogun_1_1SGVector_1ad5be3f2746de4a83e606965df9e156a6}

Construct [SGVector](#classshogun_1_1SGVector) from GPU memory.

#### Parameters
* `vector` [GPUMemoryBase](#structshogun_1_1GPUMemoryBase) pointer 

* `len` length of the data in vector 

**See also**: [GPUMemoryBase](#structshogun_1_1GPUMemoryBase)

#### `public  `[`SGVector`](#classshogun_1_1SGVector_1a4ed8072c7fe2e0866e4b1ae6e536ed5c)`(const `[`SGVector`](#classshogun_1_1SGVector)` & orig)` {#classshogun_1_1SGVector_1a4ed8072c7fe2e0866e4b1ae6e536ed5c}

Copy constructor

#### `public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` bool `[`on_gpu`](#classshogun_1_1SGVector_1a544d60c4a40021806165381020ea7d49)`() const` {#classshogun_1_1SGVector_1a544d60c4a40021806165381020ea7d49}

Check whether data is stored on GPU

#### Returns
true if vector is on GPU

#### `public template<>`  <br/>`inline  `[`SGVector`](#classshogun_1_1SGVector_1a624c442bf7a7a4a7167376a791ee8aec)`(InputIt beginIt,InputIt endIt)` {#classshogun_1_1SGVector_1a624c442bf7a7a4a7167376a791ee8aec}

Construct [SGVector](#classshogun_1_1SGVector) from InputIterator list

#### `public  `[`SGVector`](#classshogun_1_1SGVector_1a39e91472fabff989ff8b6a962edc570f)`(std::initializer_list< T > il)` {#classshogun_1_1SGVector_1a39e91472fabff989ff8b6a962edc570f}

Construct [SGVector](#classshogun_1_1SGVector) from initializer list

#### `public  `[`SGVector`](#classshogun_1_1SGVector_1ab85bd639cf67c8be088f5f973f03ca9f)`(`[`EigenVectorXt`](#classshogun_1_1SGVector_1aa375779ac932b2c2e5460d5c90ea4560)` & vec)` {#classshogun_1_1SGVector_1ab85bd639cf67c8be088f5f973f03ca9f}

Wraps a matrix around the data of an Eigen3 column vector

#### `public  `[`SGVector`](#classshogun_1_1SGVector_1a018c03a0d0c33c6e05193ccf1cd2bf43)`(`[`EigenRowVectorXt`](#classshogun_1_1SGVector_1abd19ffc32ed839e3291975a2c6de019c)` & vec)` {#classshogun_1_1SGVector_1a018c03a0d0c33c6e05193ccf1cd2bf43}

Wraps a matrix around the data of an Eigen3 row vector

#### `public  `[`operator EigenVectorXtMap`](#classshogun_1_1SGVector_1acf96ae8cc160517b73fb359fc8f01032)`() const` {#classshogun_1_1SGVector_1acf96ae8cc160517b73fb359fc8f01032}

Wraps an Eigen3 column vector around the data of this matrix

#### `public  `[`operator EigenRowVectorXtMap`](#classshogun_1_1SGVector_1a31463522561a228104f4a483b9aea763)`() const` {#classshogun_1_1SGVector_1a31463522561a228104f4a483b9aea763}

Wraps an Eigen3 row vector around the data of this matrix

#### `public template<>`  <br/>`inline `[`SGVector`](#classshogun_1_1SGVector)`< X > `[`as`](#classshogun_1_1SGVector_1ac4af18bd5ed67b691d19bab86943f766)`() const` {#classshogun_1_1SGVector_1ac4af18bd5ed67b691d19bab86943f766}

#### Returns
a (copied) typed vector with same content

#### `public void `[`set_const`](#classshogun_1_1SGVector_1a8bce01a1fc41a734d9b5cf1533fd7a2a)`(T const_elem)` {#classshogun_1_1SGVector_1a8bce01a1fc41a734d9b5cf1533fd7a2a}

Set vector to a constant

#### Parameters
* `const_elem` - value to set vector to

#### `public inline `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`get`](#classshogun_1_1SGVector_1abd42845babdeb77fb02544720672ad55)`()` {#classshogun_1_1SGVector_1abd42845babdeb77fb02544720672ad55}

Get the vector (no copying is done here)

#### Returns
the refcount increased vector

#### `public void `[`set`](#classshogun_1_1SGVector_1a69169ab99ab307a13c834a3dc8b145f3)`(`[`SGVector`](#classshogun_1_1SGVector)`< T > orig)` {#classshogun_1_1SGVector_1a69169ab99ab307a13c834a3dc8b145f3}

[Wrapper](#classWrapper) for the copy constructor useful for SWIG interfaces

#### Parameters
* `orig` vector to set

#### `public virtual  `[`~SGVector`](#classshogun_1_1SGVector_1a872738a61edf5bb223f62385620e414e)`()` {#classshogun_1_1SGVector_1a872738a61edf5bb223f62385620e414e}

[Empty](#structshogun_1_1Empty) destructor

#### `public inline int32_t `[`size`](#classshogun_1_1SGVector_1aa74e951f7370eb093717d70852a96981)`() const` {#classshogun_1_1SGVector_1aa74e951f7370eb093717d70852a96981}

Size

#### `public inline T * `[`data`](#classshogun_1_1SGVector_1a2a1c4b452e7e2523397112c12e53554d)`() const` {#classshogun_1_1SGVector_1a2a1c4b452e7e2523397112c12e53554d}

Data pointer

#### `public inline `[`iterator`](#classshogun_1_1SGVector_1a88be8e03f7fa96234ccab7620a598fc0)` `[`begin`](#classshogun_1_1SGVector_1a979556eb331ec35eb33472a90a160f99)`() noexcept` {#classshogun_1_1SGVector_1a979556eb331ec35eb33472a90a160f99}

Returns an iterator to the first element of the container.

#### `public inline `[`iterator`](#classshogun_1_1SGVector_1a88be8e03f7fa96234ccab7620a598fc0)` `[`end`](#classshogun_1_1SGVector_1afc5380afa64b233d0df01a147616974b)`() noexcept` {#classshogun_1_1SGVector_1afc5380afa64b233d0df01a147616974b}

Returns an iterator to the element following the last element of the container.

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< T > & `[`operator=`](#classshogun_1_1SGVector_1aef82a5b8c4bdb525b1914f9a7d87603c)`(const `[`SGVector`](#classshogun_1_1SGVector)`< T > &)` {#classshogun_1_1SGVector_1aef82a5b8c4bdb525b1914f9a7d87603c}

#### `public inline `[`SG_FORCED_INLINE`](#macros_8h_1ac5e77ba4f8dacf9698c0fd975f68e9ba)` bool `[`operator==`](#classshogun_1_1SGVector_1a893af62a5fd79f330602eea8ff7620a9)`(const `[`SGVector`](#classshogun_1_1SGVector)`< T > & other) const` {#classshogun_1_1SGVector_1a893af62a5fd79f330602eea8ff7620a9}

Check for pointer identity

#### `public inline  `[`operator T*`](#classshogun_1_1SGVector_1adec4d6e4697fff19761dfb957ab203f2)`()` {#classshogun_1_1SGVector_1adec4d6e4697fff19761dfb957ab203f2}

Cast to pointer

#### `public void `[`zero`](#classshogun_1_1SGVector_1a0c4493a5d4723940d60164428f11adc3)`()` {#classshogun_1_1SGVector_1a0c4493a5d4723940d60164428f11adc3}

Fill vector with zeros

#### `public void `[`range_fill`](#classshogun_1_1SGVector_1a11b4c18177e9a7dede674f8fe17d7423)`(T start)` {#classshogun_1_1SGVector_1a11b4c18177e9a7dede674f8fe17d7423}

[Range](#classshogun_1_1Range) fill a vector with start...start+len-1

#### Parameters
* `start` - value to be assigned to first element of vector

#### `public void `[`random`](#classshogun_1_1SGVector_1ad1e32b145eab46d794beb9e843b6e75f)`(T min_value,T max_value)` {#classshogun_1_1SGVector_1ad1e32b145eab46d794beb9e843b6e75f}

Create random vector

#### Parameters
* `min_value` [min_value,max_value] 

* `max_value`

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`find_position_to_insert`](#classshogun_1_1SGVector_1a54864150f4afaae2b3c296c09cb959cf)`(T element)` {#classshogun_1_1SGVector_1a54864150f4afaae2b3c296c09cb959cf}

For a sorted (ascending) vector, gets the index after the first element that is smaller than the given one

#### Parameters
* `element` element to find index for 

#### Returns
index of the first element greater than given one

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`clone`](#classshogun_1_1SGVector_1a8c70cf9bddee5ff6f539440bcae8f588)`() const` {#classshogun_1_1SGVector_1a8c70cf9bddee5ff6f539440bcae8f588}

Clone vector

#### `public inline const T & `[`get_element`](#classshogun_1_1SGVector_1a6b164abcccd9703be8251fe2c15b8d52)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index)` {#classshogun_1_1SGVector_1a6b164abcccd9703be8251fe2c15b8d52}

Get element at index

#### Parameters
* `index` index 

#### Returns
element at index

#### `public inline void `[`set_element`](#classshogun_1_1SGVector_1a69ccf7020114a13dab3c6c9328fa1ee9)`(const T & el,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` index)` {#classshogun_1_1SGVector_1a69ccf7020114a13dab3c6c9328fa1ee9}

Set element at index

#### Parameters
* `el` element to set 

* `index` index

#### `public void `[`resize_vector`](#classshogun_1_1SGVector_1aae00e2f4717f097787912c6154618d85)`(int32_t n)` {#classshogun_1_1SGVector_1aae00e2f4717f097787912c6154618d85}

Resize vector, with zero padding

#### Parameters
* `n` new size

#### `public inline const T & `[`operator[]`](#classshogun_1_1SGVector_1a424c205cae88bebdda365c021d53aef3)`(uint64_t index) const` {#classshogun_1_1SGVector_1a424c205cae88bebdda365c021d53aef3}

Operator overload for vector read only access

#### Parameters
* `index` dimension to access

#### `public inline const T & `[`operator[]`](#classshogun_1_1SGVector_1a073cf2868548922ab9413557a5ccc440)`(int64_t index) const` {#classshogun_1_1SGVector_1a073cf2868548922ab9413557a5ccc440}

Operator overload for vector read only access

#### Parameters
* `index` dimension to access

#### `public inline const T & `[`operator[]`](#classshogun_1_1SGVector_1a0d1658a24941329c21d6c745836b53fc)`(uint32_t index) const` {#classshogun_1_1SGVector_1a0d1658a24941329c21d6c745836b53fc}

Operator overload for vector read only access

#### Parameters
* `index` dimension to access

#### `public inline const T & `[`operator[]`](#classshogun_1_1SGVector_1a7b3d713784d21d55dbf1dac4971e1e22)`(int32_t index) const` {#classshogun_1_1SGVector_1a7b3d713784d21d55dbf1dac4971e1e22}

Operator overload for vector read only access

#### Parameters
* `index` dimension to access

#### `public inline T & `[`operator[]`](#classshogun_1_1SGVector_1afaea7e9ab8a70823710f1dda292e8f1d)`(uint64_t index)` {#classshogun_1_1SGVector_1afaea7e9ab8a70823710f1dda292e8f1d}

Operator overload for vector r/w access

#### Parameters
* `index` dimension to access

#### `public inline T & `[`operator[]`](#classshogun_1_1SGVector_1adb496a4681a6577d8806fe898df655bc)`(int64_t index)` {#classshogun_1_1SGVector_1adb496a4681a6577d8806fe898df655bc}

Operator overload for vector r/w access

#### Parameters
* `index` dimension to access

#### `public inline T & `[`operator[]`](#classshogun_1_1SGVector_1a30ccb7f0b69f16a83ea29fdf35af05b9)`(uint32_t index)` {#classshogun_1_1SGVector_1a30ccb7f0b69f16a83ea29fdf35af05b9}

Operator overload for vector r/w access

#### Parameters
* `index` dimension to access

#### `public inline T & `[`operator[]`](#classshogun_1_1SGVector_1a9d1c553ca2a17db6b21dffc39fd76faa)`(int32_t index)` {#classshogun_1_1SGVector_1a9d1c553ca2a17db6b21dffc39fd76faa}

Operator overload for vector r/w access

#### Parameters
* `index` dimension to access

#### `public void `[`add`](#classshogun_1_1SGVector_1a60459a3d1df1b36e24553d9be628df39)`(const `[`SGVector`](#classshogun_1_1SGVector)`< T > x)` {#classshogun_1_1SGVector_1a60459a3d1df1b36e24553d9be628df39}

Add vector to current vector

#### Parameters
* `x` add vector x to current vector

#### `public void `[`add`](#classshogun_1_1SGVector_1a6eca3993c68f7593ccb7eaca39791698)`(const `[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< T > & x)` {#classshogun_1_1SGVector_1a6eca3993c68f7593ccb7eaca39791698}

Add sparse vector to current vector

#### Parameters
* `x` add sparse vector x to current vector

#### `public void `[`add`](#classshogun_1_1SGVector_1a96054b9b2e36b780302f1ba4ef356e13)`(const T x)` {#classshogun_1_1SGVector_1a96054b9b2e36b780302f1ba4ef356e13}

Add scalar to current vector

#### Parameters
* `x` add vector x to current vector

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`operator+`](#classshogun_1_1SGVector_1ae6073f121e7989ca0da8c902e103bf11)`(`[`SGVector`](#classshogun_1_1SGVector)`< T > x)` {#classshogun_1_1SGVector_1ae6073f121e7989ca0da8c902e103bf11}

Addition operator

addition operator

#### `public inline `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`operator+=`](#classshogun_1_1SGVector_1ae00ea426fb9fc39942321bb8d70173dc)`(`[`SGVector`](#classshogun_1_1SGVector)`< T > x)` {#classshogun_1_1SGVector_1ae00ea426fb9fc39942321bb8d70173dc}

Inplace addition operator

#### `public inline `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`operator+=`](#classshogun_1_1SGVector_1a3c822178319cc502d469e64737eca247)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< T > & x)` {#classshogun_1_1SGVector_1a3c822178319cc502d469e64737eca247}

Inplace addition operator for sparse vector

#### `public bool `[`equals`](#classshogun_1_1SGVector_1a2e383a8551e463625d36c971c7fb4253)`(const `[`SGVector`](#classshogun_1_1SGVector)`< T > & other) const` {#classshogun_1_1SGVector_1a2e383a8551e463625d36c971c7fb4253}

Equals method up to precision for vectors (element-wise) 
#### Parameters
* `other` vector to compare with 

#### Returns
false if any element differs or if sizes are different, true otherwise

#### `public inline T `[`product`](#classshogun_1_1SGVector_1a170fcfdaca76669b6dace97b687ee6b9)`()` {#classshogun_1_1SGVector_1a170fcfdaca76669b6dace97b687ee6b9}

Return product(vec)

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< T > `[`unique`](#classshogun_1_1SGVector_1a63cbc3d40ec664e6e30f4e06aaae40b2)`()` {#classshogun_1_1SGVector_1a63cbc3d40ec664e6e30f4e06aaae40b2}

Returns new vector with sorted unique elements of current

#### `public void `[`display_size`](#classshogun_1_1SGVector_1a525360b36eff026a5d3d61d163c45695)`() const` {#classshogun_1_1SGVector_1a525360b36eff026a5d3d61d163c45695}

Display array size

#### `public void `[`display_vector`](#classshogun_1_1SGVector_1ad2f0f71a9a20cd8747a4657ed6a76c64)`(const char * name,const char * prefix) const` {#classshogun_1_1SGVector_1ad2f0f71a9a20cd8747a4657ed6a76c64}

Display vector

#### `public `[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > `[`find`](#classshogun_1_1SGVector_1a1b644c84c08aa4ab8357c246a33f3d30)`(T elem)` {#classshogun_1_1SGVector_1a1b644c84c08aa4ab8357c246a33f3d30}

Find index for occurance of an element 
#### Parameters
* `elem` the element to find

#### `public template<>`  <br/>`inline `[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > `[`find_if`](#classshogun_1_1SGVector_1a159412b7e46c731f4bd321c7450eb66e)`(Predicate p)` {#classshogun_1_1SGVector_1a159412b7e46c731f4bd321c7450eb66e}

Find index for elements where the predicate returns true 
#### Parameters
* `p` the predicate, it should accept the value of the element and return a bool

#### `public void `[`scale`](#classshogun_1_1SGVector_1a21b3ad2091f6b9df71afed0efe9a7e62)`(T alpha)` {#classshogun_1_1SGVector_1a21b3ad2091f6b9df71afed0efe9a7e62}

Scale vector inplace.

#### `public void `[`load`](#classshogun_1_1SGVector_1a5d33ec59a4be25056cca1f3b6691ad00)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` {#classshogun_1_1SGVector_1a5d33ec59a4be25056cca1f3b6691ad00}

Load vector from file

#### Parameters
* `loader` File object via which to load data

#### `public void `[`save`](#classshogun_1_1SGVector_1aff4d5355fe0d9b68bc8c71cd331c082e)`(`[`CFile`](#classshogun_1_1CFile)` * saver)` {#classshogun_1_1SGVector_1aff4d5355fe0d9b68bc8c71cd331c082e}

Save vector to file

#### Parameters
* `saver` File object via which to save data

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_real`](#classshogun_1_1SGVector_1adda3bcff402b917a950e9022265f4f86)`()` {#classshogun_1_1SGVector_1adda3bcff402b917a950e9022265f4f86}

Real part of a complex128_t vector

#### `public `[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`get_imag`](#classshogun_1_1SGVector_1a7ab9a2f31b17d19e82cb4df9a20f9038)`()` {#classshogun_1_1SGVector_1a7ab9a2f31b17d19e82cb4df9a20f9038}

Imag part of a complex128_t vector

#### `public template<>`  <br/>`void `[`zero`](#classshogun_1_1SGVector_1ae9deeaac2eaad960a9cdddf810d29a35)`()` {#classshogun_1_1SGVector_1ae9deeaac2eaad960a9cdddf810d29a35}

#### `public template<>`  <br/>[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`find_position_to_insert`](#classshogun_1_1SGVector_1a5fd8069abc9898d45f142a53e51a1b28)`(`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` element)` {#classshogun_1_1SGVector_1a5fd8069abc9898d45f142a53e51a1b28}

#### `public template<>`  <br/>`void `[`range_fill_vector`](#classshogun_1_1SGVector_1a482d503acdb8406697a73f08d37dfb31)`(`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` * vec,int32_t len,`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` start)` {#classshogun_1_1SGVector_1a482d503acdb8406697a73f08d37dfb31}

#### `public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1aeece7ae9714fd9050479fb1d073312b2)`(const bool * vector,int32_t n,const char * name,const char * prefix)` {#classshogun_1_1SGVector_1aeece7ae9714fd9050479fb1d073312b2}

#### `public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1a8bc0638eccb42a7071f2ca7a26136a3e)`(const char * vector,int32_t n,const char * name,const char * prefix)` {#classshogun_1_1SGVector_1a8bc0638eccb42a7071f2ca7a26136a3e}

#### `public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1a2dc56de234c0ffa70ee47d459ff57763)`(const uint8_t * vector,int32_t n,const char * name,const char * prefix)` {#classshogun_1_1SGVector_1a2dc56de234c0ffa70ee47d459ff57763}

#### `public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1a0d4234c5c0ff73b315077796be0cbc9e)`(const int8_t * vector,int32_t n,const char * name,const char * prefix)` {#classshogun_1_1SGVector_1a0d4234c5c0ff73b315077796be0cbc9e}

#### `public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1afbb42c6b622c615d09eaab971f684a7d)`(const uint16_t * vector,int32_t n,const char * name,const char * prefix)` {#classshogun_1_1SGVector_1afbb42c6b622c615d09eaab971f684a7d}

#### `public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1a60a1866268a275f2c70fa170b5ed6c3f)`(const int16_t * vector,int32_t n,const char * name,const char * prefix)` {#classshogun_1_1SGVector_1a60a1866268a275f2c70fa170b5ed6c3f}

#### `public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1aef457ae0881aec468ac5fd8ab8fffffb)`(const int32_t * vector,int32_t n,const char * name,const char * prefix)` {#classshogun_1_1SGVector_1aef457ae0881aec468ac5fd8ab8fffffb}

#### `public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1a8382b955e2c95ee3e8d5018391072b8a)`(const uint32_t * vector,int32_t n,const char * name,const char * prefix)` {#classshogun_1_1SGVector_1a8382b955e2c95ee3e8d5018391072b8a}

#### `public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1a1e665cb9ac8faa06ec8375d399c42637)`(const int64_t * vector,int32_t n,const char * name,const char * prefix)` {#classshogun_1_1SGVector_1a1e665cb9ac8faa06ec8375d399c42637}

#### `public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1a4a5c7af3725445fa15a1e985236587b7)`(const uint64_t * vector,int32_t n,const char * name,const char * prefix)` {#classshogun_1_1SGVector_1a4a5c7af3725445fa15a1e985236587b7}

#### `public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1a4a5181e1b039c341f82d4f29dba2de9c)`(const `[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * vector,int32_t n,const char * name,const char * prefix)` {#classshogun_1_1SGVector_1a4a5181e1b039c341f82d4f29dba2de9c}

#### `public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1aa287361aca72c80ba56f1813bf0b2813)`(const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * vector,int32_t n,const char * name,const char * prefix)` {#classshogun_1_1SGVector_1aa287361aca72c80ba56f1813bf0b2813}

#### `public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1a7a2d7e819ccc3a3a3d2778e24a87af9f)`(const `[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` * vector,int32_t n,const char * name,const char * prefix)` {#classshogun_1_1SGVector_1a7a2d7e819ccc3a3a3d2778e24a87af9f}

#### `public template<>`  <br/>`void `[`display_vector`](#classshogun_1_1SGVector_1a1524864ebffbae5c88ee5bec78cc46ef)`(const `[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` * vector,int32_t n,const char * name,const char * prefix)` {#classshogun_1_1SGVector_1a1524864ebffbae5c88ee5bec78cc46ef}

#### `public template<>`  <br/>`void `[`vec1_plus_scalar_times_vec2`](#classshogun_1_1SGVector_1a723c55c5e11122a930396a92a5be8a6e)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * vec1,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` scalar,const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * vec2,int32_t n)` {#classshogun_1_1SGVector_1a723c55c5e11122a930396a92a5be8a6e}

#### `public template<>`  <br/>`void `[`vec1_plus_scalar_times_vec2`](#classshogun_1_1SGVector_1aacd4fa660389283c7a1fc06006f215cf)`(`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * vec1,`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` scalar,const `[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * vec2,int32_t n)` {#classshogun_1_1SGVector_1aacd4fa660389283c7a1fc06006f215cf}

#### `public template<>`  <br/>`void `[`random_vector`](#classshogun_1_1SGVector_1af0ff9f1f4614e711f3177c41cdd05072)`(`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` * vec,int32_t len,`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` min_value,`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` max_value)` {#classshogun_1_1SGVector_1af0ff9f1f4614e711f3177c41cdd05072}

#### `public template<>`  <br/>`bool `[`twonorm`](#classshogun_1_1SGVector_1ae227f8a6f1d174b92b4ae27c8c3f2b34)`(const bool * x,int32_t len)` {#classshogun_1_1SGVector_1ae227f8a6f1d174b92b4ae27c8c3f2b34}

#### `public template<>`  <br/>`char `[`twonorm`](#classshogun_1_1SGVector_1a1f173951785f09b16b77044a00fc2919)`(const char * x,int32_t len)` {#classshogun_1_1SGVector_1a1f173951785f09b16b77044a00fc2919}

#### `public template<>`  <br/>`int8_t `[`twonorm`](#classshogun_1_1SGVector_1a3d1a57721943f087a46fc7d075ae05d2)`(const int8_t * x,int32_t len)` {#classshogun_1_1SGVector_1a3d1a57721943f087a46fc7d075ae05d2}

#### `public template<>`  <br/>`uint8_t `[`twonorm`](#classshogun_1_1SGVector_1a7e09aace4224b135fb24f22f20623482)`(const uint8_t * x,int32_t len)` {#classshogun_1_1SGVector_1a7e09aace4224b135fb24f22f20623482}

#### `public template<>`  <br/>`int16_t `[`twonorm`](#classshogun_1_1SGVector_1a4e7b4ca02a6196112d9c79acf39e82ce)`(const int16_t * x,int32_t len)` {#classshogun_1_1SGVector_1a4e7b4ca02a6196112d9c79acf39e82ce}

#### `public template<>`  <br/>`uint16_t `[`twonorm`](#classshogun_1_1SGVector_1a36e23200f86373f7b0421a01bb65d7b4)`(const uint16_t * x,int32_t len)` {#classshogun_1_1SGVector_1a36e23200f86373f7b0421a01bb65d7b4}

#### `public template<>`  <br/>`int32_t `[`twonorm`](#classshogun_1_1SGVector_1ad3b22897ff6555a9ce71566e7f021efd)`(const int32_t * x,int32_t len)` {#classshogun_1_1SGVector_1ad3b22897ff6555a9ce71566e7f021efd}

#### `public template<>`  <br/>`uint32_t `[`twonorm`](#classshogun_1_1SGVector_1a1e6d0ceb402793ae771251d2f2b6065b)`(const uint32_t * x,int32_t len)` {#classshogun_1_1SGVector_1a1e6d0ceb402793ae771251d2f2b6065b}

#### `public template<>`  <br/>`int64_t `[`twonorm`](#classshogun_1_1SGVector_1a6572308404ccad5f9e3068b2be1166ec)`(const int64_t * x,int32_t len)` {#classshogun_1_1SGVector_1a6572308404ccad5f9e3068b2be1166ec}

#### `public template<>`  <br/>`uint64_t `[`twonorm`](#classshogun_1_1SGVector_1a649aa558a5b5ff02da794629c0394e52)`(const uint64_t * x,int32_t len)` {#classshogun_1_1SGVector_1a649aa558a5b5ff02da794629c0394e52}

#### `public template<>`  <br/>[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` `[`twonorm`](#classshogun_1_1SGVector_1a6a7328a5016619cae11f70ae1e9fc35f)`(const `[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * x,int32_t len)` {#classshogun_1_1SGVector_1a6a7328a5016619cae11f70ae1e9fc35f}

#### `public template<>`  <br/>[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`twonorm`](#classshogun_1_1SGVector_1af983afee23a79cf2637746dfe4f508d1)`(const `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * v,int32_t n)` {#classshogun_1_1SGVector_1af983afee23a79cf2637746dfe4f508d1}

#### `public template<>`  <br/>[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` `[`twonorm`](#classshogun_1_1SGVector_1a8c1c05aceeeeb3fcfbe3abd21270a62d)`(const `[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` * x,int32_t len)` {#classshogun_1_1SGVector_1a8c1c05aceeeeb3fcfbe3abd21270a62d}

#### `public template<>`  <br/>[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` `[`twonorm`](#classshogun_1_1SGVector_1a6b96c38f04f9814b50507799fc67acbc)`(const `[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` * x,int32_t len)` {#classshogun_1_1SGVector_1a6b96c38f04f9814b50507799fc67acbc}

#### `public template<>`  <br/>[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` `[`qsq`](#classshogun_1_1SGVector_1a7884f1d515470f498f222f8d60635b72)`(`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` * x,int32_t len,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` q)` {#classshogun_1_1SGVector_1a7884f1d515470f498f222f8d60635b72}

#### `public template<>`  <br/>[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` `[`qnorm`](#classshogun_1_1SGVector_1a6766ea3fa31ff852f335dda7fded9fc8)`(`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` * x,int32_t len,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` q)` {#classshogun_1_1SGVector_1a6766ea3fa31ff852f335dda7fded9fc8}

#### `public template<>`  <br/>[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`sum_abs`](#classshogun_1_1SGVector_1af9e9603dd32c7d6c7f68aa0e4b933c98)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * vec,int32_t len)` {#classshogun_1_1SGVector_1af9e9603dd32c7d6c7f68aa0e4b933c98}

#### `public template<>`  <br/>[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` `[`sum_abs`](#classshogun_1_1SGVector_1a730a93fc7384fc0b36d3f13fc196ef1e)`(`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * vec,int32_t len)` {#classshogun_1_1SGVector_1a730a93fc7384fc0b36d3f13fc196ef1e}

#### `public template<>`  <br/>`int32_t `[`unique`](#classshogun_1_1SGVector_1a24bf23298af779be67f7c67d33fbecba)`(`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` * output,int32_t size)` {#classshogun_1_1SGVector_1a24bf23298af779be67f7c67d33fbecba}

#### `public template<>`  <br/>[`SGVector](#classshogun_1_1SGVector)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > `[`unique`](#classshogun_1_1SGVector_1aae255ad261dab440c1622f3630d0499e)`()` {#classshogun_1_1SGVector_1aae255ad261dab440c1622f3630d0499e}

#### `public template<>`  <br/>`void `[`scale_vector`](#classshogun_1_1SGVector_1a3a9df99976a9712a893d161688b6da0e)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` alpha,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * vec,int32_t len)` {#classshogun_1_1SGVector_1a3a9df99976a9712a893d161688b6da0e}

#### `public template<>`  <br/>`void `[`scale_vector`](#classshogun_1_1SGVector_1a96ddba4d36874313750da8667ee19a6f)`(`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` alpha,`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * vec,int32_t len)` {#classshogun_1_1SGVector_1a96ddba4d36874313750da8667ee19a6f}

#### `public template<>`  <br/>`void `[`load`](#classshogun_1_1SGVector_1a17763c63f0719b10922bc4ed6f392ec4)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` {#classshogun_1_1SGVector_1a17763c63f0719b10922bc4ed6f392ec4}

#### `public template<>`  <br/>`void `[`save`](#classshogun_1_1SGVector_1aa61bf55fa90bee7cd7e92beaebe38774)`(`[`CFile`](#classshogun_1_1CFile)` * saver)` {#classshogun_1_1SGVector_1aa61bf55fa90bee7cd7e92beaebe38774}

#### `public int32_t `[`ref_count`](#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d)`()` {#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d}

display reference counter

#### Returns
reference count

#### `protected virtual void `[`copy_data`](#classshogun_1_1SGVector_1a6e8ddd37b0b245f7cca418642762e16b)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` {#classshogun_1_1SGVector_1a6e8ddd37b0b245f7cca418642762e16b}

needs to be overridden to copy data

#### `protected virtual void `[`init_data`](#classshogun_1_1SGVector_1a3b42d3bd68c5200393c1f0809ed1facf)`()` {#classshogun_1_1SGVector_1a3b42d3bd68c5200393c1f0809ed1facf}

needs to be overridden to initialize empty data

#### `protected virtual void `[`free_data`](#classshogun_1_1SGVector_1ab340ce24b1c9d2b26ab2b46a7a64c346)`()` {#classshogun_1_1SGVector_1ab340ce24b1c9d2b26ab2b46a7a64c346}

needs to be overridden to free data

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

#### `typedef `[`iterator`](#classshogun_1_1SGVector_1a88be8e03f7fa96234ccab7620a598fc0) {#classshogun_1_1SGVector_1a88be8e03f7fa96234ccab7620a598fc0}

#### `typedef `[`EigenVectorXt`](#classshogun_1_1SGVector_1aa375779ac932b2c2e5460d5c90ea4560) {#classshogun_1_1SGVector_1aa375779ac932b2c2e5460d5c90ea4560}

#### `typedef `[`EigenRowVectorXt`](#classshogun_1_1SGVector_1abd19ffc32ed839e3291975a2c6de019c) {#classshogun_1_1SGVector_1abd19ffc32ed839e3291975a2c6de019c}

#### `typedef `[`EigenVectorXtMap`](#classshogun_1_1SGVector_1a228edb14803d0d1b9307af0439719b9b) {#classshogun_1_1SGVector_1a228edb14803d0d1b9307af0439719b9b}

#### `typedef `[`EigenRowVectorXtMap`](#classshogun_1_1SGVector_1afa6ac3dbae224e01be833e7e2bc1c43c) {#classshogun_1_1SGVector_1afa6ac3dbae224e01be833e7e2bc1c43c}

#### `typedef `[`Scalar`](#classshogun_1_1SGVector_1a47fdf58368a1d22e91e658ab30bfcda8) {#classshogun_1_1SGVector_1a47fdf58368a1d22e91e658ab30bfcda8}

The scalar type of the vector

#### `typedef `[`container_type`](#classshogun_1_1SGVector_1a5a578ed7540440e16d3f8bd5f7d1992b) {#classshogun_1_1SGVector_1a5a578ed7540440e16d3f8bd5f7d1992b}

The container type for a given template argument

