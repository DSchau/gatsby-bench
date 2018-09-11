---
classname: "shogun::CIndirectObject"
type: "class"
---

# class `shogun::CIndirectObject` {#classshogun_1_1CIndirectObject}

an array class that accesses elements indirectly via an index array.

It does not store the objects itself, but only indices to objects. This conveniently allows e.g. sorting the array without changing the order of objects (but only the order of their indices).

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public inline  `[`CIndirectObject`](#classshogun_1_1CIndirectObject_1a9401305a8fdec2aee14768e8c82e5611)`()` | default constructor (initializes index with -1)
`public inline  `[`CIndirectObject`](#classshogun_1_1CIndirectObject_1abbdafa53e8db07b1694b00c1d1a2606e)`(int32_t idx)` | constructor 
`public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator=`](#classshogun_1_1CIndirectObject_1a3ea7bf05b8d6aa7210ed8875572a56bf)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x)` | overload = operator 
`public inline T `[`operator\|`](#classshogun_1_1CIndirectObject_1a954439b14ebae3e93cbfed59339d864d)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` | overload \| operator and return x \| y
`public inline const T `[`operator &`](#classshogun_1_1CIndirectObject_1a607f9ba654c39f6d629bd59a7eb05862)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` | overload & operator and return x & y
`public inline T `[`operator<<`](#classshogun_1_1CIndirectObject_1a6473dd30b32d66632ef11590eeaa00b5)`(int shift)` | overload << operator
`public inline T `[`operator>>`](#classshogun_1_1CIndirectObject_1a416a53d007b21c8a69e020167e7099f7)`(int shift)` | overload >> operator
`public inline T `[`operator^`](#classshogun_1_1CIndirectObject_1af1a92e04b5cc7ba6b4f2d95842459252)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` | overload ^ operator and return x ^ y
`public inline T `[`operator+`](#classshogun_1_1CIndirectObject_1aa9d364aeaa7dde09c97b016b2c0a5de6)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` | overload + operator and return x + y
`public inline T `[`operator-`](#classshogun_1_1CIndirectObject_1ad4bd1709062a5fd3aa35fe40b9504e58)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` | overload - operator and return x - y
`public inline T `[`operator/`](#classshogun_1_1CIndirectObject_1a54d0849b303f6905c1be7968d913370c)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` | overload / operator and return x / y
`public inline T `[`operator*`](#classshogun_1_1CIndirectObject_1a0ef54713ae3b9f7cc273031e982f0556)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` | overload * operator and return x * y
`public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator+=`](#classshogun_1_1CIndirectObject_1a73173a6b881fdff4a84b9df7a14ab1ac)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x)` | overload += operator; add x to current element
`public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator-=`](#classshogun_1_1CIndirectObject_1a3ac217b1ba9358fda56ac26d6fca976f)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x)` | overload -= operator; substract x from current element
`public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator*=`](#classshogun_1_1CIndirectObject_1a9391f50ecd28def64849ed4424551024)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x)` | overload *= operator; multiple x to with current element
`public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator/=`](#classshogun_1_1CIndirectObject_1a986d8b1ccfb0084f0220ad9de1111f68)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x)` | overload /= operator; divide current object by x
`public inline bool `[`operator==`](#classshogun_1_1CIndirectObject_1aa660da2ad26f990000528e72d778fc6c)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` | overload == operator; test if current object equals x
`public inline bool `[`operator>=`](#classshogun_1_1CIndirectObject_1a2d35ed455319f4316139affb0f972711)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` | overload >= operator; test if current object greater equal x
`public inline bool `[`operator<=`](#classshogun_1_1CIndirectObject_1a239485bea6b7d0842d122017d781b8d8)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` | overload <= operator; test if current object lower equal x
`public inline bool `[`operator>`](#classshogun_1_1CIndirectObject_1a5b0e80b8f6162b44a0a826edf36ef1e5)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` | overload > operator; test if current object is bigger than x
`public inline bool `[`operator<`](#classshogun_1_1CIndirectObject_1a5a461a7f62c808ed997bdcb5dbb08bb3)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` | overload < operator; test if current object is smaller than x
`public inline bool `[`operator!=`](#classshogun_1_1CIndirectObject_1a21f4c5836c2ec30323b67fe509db6760)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` | overload ! operator; test if current object is not equal to x
`public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator\|=`](#classshogun_1_1CIndirectObject_1af2a8201e900a98958c47c1ead5320ca0)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x)` | overload \|= operator
`public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator &=`](#classshogun_1_1CIndirectObject_1ae2c650d66d157e1e714916f091898381)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x)` | overload &= operator
`public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator^=`](#classshogun_1_1CIndirectObject_1a3d77b6c0db966e88af040e981bf388f9)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x)` | overload ^= operator
`public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator<<=`](#classshogun_1_1CIndirectObject_1a9947bf2ae38c56b45380dfb7988964e4)`(int shift)` | overload <<= operator
`public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator>>=`](#classshogun_1_1CIndirectObject_1a2ef68c39d01969cf908ab2d43c2cc340)`(int shift)` | overload >>= operator
`public inline T `[`operator~`](#classshogun_1_1CIndirectObject_1a65a4e88748487508cc4efb0474c71cd8)`()` | negate element
`public inline  `[`operator T`](#classshogun_1_1CIndirectObject_1a54724b9dd792a6022b918eae2f393734)`() const` | return array element
`public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator--`](#classshogun_1_1CIndirectObject_1a48bcb20952c73bffd08eb5a3f0a8c27e)`()` | decrement element by one
`public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator++`](#classshogun_1_1CIndirectObject_1a375af2d553aaf5377baa32bdfac603cf)`()` | increment element by one
`protected int32_t `[`index`](#classshogun_1_1CIndirectObject_1ae1b9103978b8e0c475d68564bb2e3a2f) | index into array

## Members

#### `public inline  `[`CIndirectObject`](#classshogun_1_1CIndirectObject_1a9401305a8fdec2aee14768e8c82e5611)`()` {#classshogun_1_1CIndirectObject_1a9401305a8fdec2aee14768e8c82e5611}

default constructor (initializes index with -1)

#### `public inline  `[`CIndirectObject`](#classshogun_1_1CIndirectObject_1abbdafa53e8db07b1694b00c1d1a2606e)`(int32_t idx)` {#classshogun_1_1CIndirectObject_1abbdafa53e8db07b1694b00c1d1a2606e}

constructor 
#### Parameters
* `idx` index

#### `public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator=`](#classshogun_1_1CIndirectObject_1a3ea7bf05b8d6aa7210ed8875572a56bf)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x)` {#classshogun_1_1CIndirectObject_1a3ea7bf05b8d6aa7210ed8875572a56bf}

overload = operator 
#### Parameters
* `x` assign elements from x

#### `public inline T `[`operator|`](#classshogun_1_1CIndirectObject_1a954439b14ebae3e93cbfed59339d864d)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` {#classshogun_1_1CIndirectObject_1a954439b14ebae3e93cbfed59339d864d}

overload | operator and return x | y

#### Parameters
* `x` x

#### `public inline const T `[`operator &`](#classshogun_1_1CIndirectObject_1a607f9ba654c39f6d629bd59a7eb05862)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` {#classshogun_1_1CIndirectObject_1a607f9ba654c39f6d629bd59a7eb05862}

overload & operator and return x & y

#### Parameters
* `x` x

#### `public inline T `[`operator<<`](#classshogun_1_1CIndirectObject_1a6473dd30b32d66632ef11590eeaa00b5)`(int shift)` {#classshogun_1_1CIndirectObject_1a6473dd30b32d66632ef11590eeaa00b5}

overload << operator

perform bit shift to the left

#### Parameters
* `shift` shift by this amount

#### `public inline T `[`operator>>`](#classshogun_1_1CIndirectObject_1a416a53d007b21c8a69e020167e7099f7)`(int shift)` {#classshogun_1_1CIndirectObject_1a416a53d007b21c8a69e020167e7099f7}

overload >> operator

perform bit shift to the right

#### Parameters
* `shift` shift by this amount

#### `public inline T `[`operator^`](#classshogun_1_1CIndirectObject_1af1a92e04b5cc7ba6b4f2d95842459252)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` {#classshogun_1_1CIndirectObject_1af1a92e04b5cc7ba6b4f2d95842459252}

overload ^ operator and return x ^ y

#### Parameters
* `x` x

#### `public inline T `[`operator+`](#classshogun_1_1CIndirectObject_1aa9d364aeaa7dde09c97b016b2c0a5de6)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` {#classshogun_1_1CIndirectObject_1aa9d364aeaa7dde09c97b016b2c0a5de6}

overload + operator and return x + y

#### Parameters
* `x` x

#### `public inline T `[`operator-`](#classshogun_1_1CIndirectObject_1ad4bd1709062a5fd3aa35fe40b9504e58)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` {#classshogun_1_1CIndirectObject_1ad4bd1709062a5fd3aa35fe40b9504e58}

overload - operator and return x - y

#### Parameters
* `x` x

#### `public inline T `[`operator/`](#classshogun_1_1CIndirectObject_1a54d0849b303f6905c1be7968d913370c)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` {#classshogun_1_1CIndirectObject_1a54d0849b303f6905c1be7968d913370c}

overload / operator and return x / y

#### Parameters
* `x` x

#### `public inline T `[`operator*`](#classshogun_1_1CIndirectObject_1a0ef54713ae3b9f7cc273031e982f0556)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` {#classshogun_1_1CIndirectObject_1a0ef54713ae3b9f7cc273031e982f0556}

overload * operator and return x * y

#### Parameters
* `x` x

#### `public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator+=`](#classshogun_1_1CIndirectObject_1a73173a6b881fdff4a84b9df7a14ab1ac)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x)` {#classshogun_1_1CIndirectObject_1a73173a6b881fdff4a84b9df7a14ab1ac}

overload += operator; add x to current element

#### Parameters
* `x` x

#### `public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator-=`](#classshogun_1_1CIndirectObject_1a3ac217b1ba9358fda56ac26d6fca976f)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x)` {#classshogun_1_1CIndirectObject_1a3ac217b1ba9358fda56ac26d6fca976f}

overload -= operator; substract x from current element

#### Parameters
* `x` x

#### `public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator*=`](#classshogun_1_1CIndirectObject_1a9391f50ecd28def64849ed4424551024)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x)` {#classshogun_1_1CIndirectObject_1a9391f50ecd28def64849ed4424551024}

overload *= operator; multiple x to with current element

#### Parameters
* `x` x

#### `public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator/=`](#classshogun_1_1CIndirectObject_1a986d8b1ccfb0084f0220ad9de1111f68)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x)` {#classshogun_1_1CIndirectObject_1a986d8b1ccfb0084f0220ad9de1111f68}

overload /= operator; divide current object by x

#### Parameters
* `x` x

#### `public inline bool `[`operator==`](#classshogun_1_1CIndirectObject_1aa660da2ad26f990000528e72d778fc6c)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` {#classshogun_1_1CIndirectObject_1aa660da2ad26f990000528e72d778fc6c}

overload == operator; test if current object equals x

#### Parameters
* `x` x

#### `public inline bool `[`operator>=`](#classshogun_1_1CIndirectObject_1a2d35ed455319f4316139affb0f972711)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` {#classshogun_1_1CIndirectObject_1a2d35ed455319f4316139affb0f972711}

overload >= operator; test if current object greater equal x

#### Parameters
* `x` x

#### `public inline bool `[`operator<=`](#classshogun_1_1CIndirectObject_1a239485bea6b7d0842d122017d781b8d8)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` {#classshogun_1_1CIndirectObject_1a239485bea6b7d0842d122017d781b8d8}

overload <= operator; test if current object lower equal x

#### Parameters
* `x` x

#### `public inline bool `[`operator>`](#classshogun_1_1CIndirectObject_1a5b0e80b8f6162b44a0a826edf36ef1e5)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` {#classshogun_1_1CIndirectObject_1a5b0e80b8f6162b44a0a826edf36ef1e5}

overload > operator; test if current object is bigger than x

#### Parameters
* `x` x

#### `public inline bool `[`operator<`](#classshogun_1_1CIndirectObject_1a5a461a7f62c808ed997bdcb5dbb08bb3)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` {#classshogun_1_1CIndirectObject_1a5a461a7f62c808ed997bdcb5dbb08bb3}

overload < operator; test if current object is smaller than x

#### Parameters
* `x` x

#### `public inline bool `[`operator!=`](#classshogun_1_1CIndirectObject_1a21f4c5836c2ec30323b67fe509db6760)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x) const` {#classshogun_1_1CIndirectObject_1a21f4c5836c2ec30323b67fe509db6760}

overload ! operator; test if current object is not equal to x

#### Parameters
* `x` x

#### `public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator|=`](#classshogun_1_1CIndirectObject_1af2a8201e900a98958c47c1ead5320ca0)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x)` {#classshogun_1_1CIndirectObject_1af2a8201e900a98958c47c1ead5320ca0}

overload |= operator

perform bitwise or with current element and x

#### Parameters
* `x` x

#### `public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator &=`](#classshogun_1_1CIndirectObject_1ae2c650d66d157e1e714916f091898381)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x)` {#classshogun_1_1CIndirectObject_1ae2c650d66d157e1e714916f091898381}

overload &= operator

perform bitwise and with current element and x

#### Parameters
* `x` x

#### `public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator^=`](#classshogun_1_1CIndirectObject_1a3d77b6c0db966e88af040e981bf388f9)`(const `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & x)` {#classshogun_1_1CIndirectObject_1a3d77b6c0db966e88af040e981bf388f9}

overload ^= operator

perform bitwise xor with current element and x

#### Parameters
* `x` x

#### `public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator<<=`](#classshogun_1_1CIndirectObject_1a9947bf2ae38c56b45380dfb7988964e4)`(int shift)` {#classshogun_1_1CIndirectObject_1a9947bf2ae38c56b45380dfb7988964e4}

overload <<= operator

perform bit shift to the left

#### Parameters
* `shift` shift by this amount

#### `public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator>>=`](#classshogun_1_1CIndirectObject_1a2ef68c39d01969cf908ab2d43c2cc340)`(int shift)` {#classshogun_1_1CIndirectObject_1a2ef68c39d01969cf908ab2d43c2cc340}

overload >>= operator

perform bit shift to the right

#### Parameters
* `shift` shift by this amount

#### `public inline T `[`operator~`](#classshogun_1_1CIndirectObject_1a65a4e88748487508cc4efb0474c71cd8)`()` {#classshogun_1_1CIndirectObject_1a65a4e88748487508cc4efb0474c71cd8}

negate element

#### `public inline  `[`operator T`](#classshogun_1_1CIndirectObject_1a54724b9dd792a6022b918eae2f393734)`() const` {#classshogun_1_1CIndirectObject_1a54724b9dd792a6022b918eae2f393734}

return array element

#### `public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator--`](#classshogun_1_1CIndirectObject_1a48bcb20952c73bffd08eb5a3f0a8c27e)`()` {#classshogun_1_1CIndirectObject_1a48bcb20952c73bffd08eb5a3f0a8c27e}

decrement element by one

#### `public inline `[`CIndirectObject`](#classshogun_1_1CIndirectObject)`< T, P > & `[`operator++`](#classshogun_1_1CIndirectObject_1a375af2d553aaf5377baa32bdfac603cf)`()` {#classshogun_1_1CIndirectObject_1a375af2d553aaf5377baa32bdfac603cf}

increment element by one

#### `protected int32_t `[`index`](#classshogun_1_1CIndirectObject_1ae1b9103978b8e0c475d68564bb2e3a2f) {#classshogun_1_1CIndirectObject_1ae1b9103978b8e0c475d68564bb2e3a2f}

index into array

