---
classname: "shogun::Any"
type: "class"
---

# class `shogun::Any` {#classshogun_1_1Any}

Allows to store objects of arbitrary types by using a [BaseAnyPolicy](#classshogun_1_1BaseAnyPolicy) and provides a type agnostic API. See its usage in [CSGObject::Self](#classshogun_1_1CSGObject_1_1Self), CSGObject::set(), [CSGObject::get()](#classshogun_1_1CSGObject_1a4de6e15966500093d2c04db29bbf4ac7) and [CSGObject::has()](#classshogun_1_1CSGObject_1aa911ba3ef90e0b3179e0a8dc10586424).

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public inline  `[`Any`](#classshogun_1_1Any_1a07f7072608d83354a5eed8bbc94ce92b)`()` | [Empty](#structshogun_1_1Empty) value constructor
`public inline  `[`Any`](#classshogun_1_1Any_1a2b1fa787aa0010e977015ebcc744ead2)`(`[`BaseAnyPolicy`](#classshogun_1_1BaseAnyPolicy)` * the_policy,void * the_storage)` | Base constructor
`public template<>`  <br/>`inline  explicit `[`Any`](#classshogun_1_1Any_1afb533a0e5973b9273ec0d696e8cf7d91)`(const T & v)` | Constructor to copy value
`public inline  `[`Any`](#classshogun_1_1Any_1a91c4026dc28de330498ae8d94bc7b55a)`(const `[`Any`](#classshogun_1_1Any)` & other)` | Copy constructor
`public inline  `[`Any`](#classshogun_1_1Any_1a381b29f8be43c8900c54046d89b854fd)`(`[`Any`](#classshogun_1_1Any)` && other)` | Move constructor
`public inline `[`Any`](#classshogun_1_1Any)` & `[`operator=`](#classshogun_1_1Any_1a67a7d162cbd72dba19b0227d0c91d1ef)`(const `[`Any`](#classshogun_1_1Any)` & other)` | Assignment operator 
`public inline `[`Any`](#classshogun_1_1Any)` & `[`clone_from`](#classshogun_1_1Any_1a410b9b3085bbaad70867d284035ecc75)`(const `[`Any`](#classshogun_1_1Any)` & other)` | 
`public inline  `[`~Any`](#classshogun_1_1Any_1a74082a1daff91f56146e67cc4e5e7666)`()` | Destructor
`public template<>`  <br/>`inline T `[`as`](#classshogun_1_1Any_1a0a722d04cee6bf06b968660956d7ebc3)`() const` | Casts hidden value to provided type, fails otherwise. 
`public template<>`  <br/>`inline bool `[`has_type`](#classshogun_1_1Any_1ae3047fab975f854f3732892260f92f08)`() const` | #### Returns
`public template<>`  <br/>`inline bool `[`has_type_fallback`](#classshogun_1_1Any_1aacf89173620b4fd628b83d3bd1f219cb)`() const` | #### Returns
`public inline bool `[`empty`](#classshogun_1_1Any_1a644718bb2fb240de962dc3c9a1fdf0dc)`() const` | #### Returns
`public inline bool `[`cloneable`](#classshogun_1_1Any_1a30da34ff3314046d5ff0b172d2415a44)`() const` | #### Returns
`public inline bool `[`visitable`](#classshogun_1_1Any_1a4be6bc8666266476a54efb8122f8b9b4)`() const` | #### Returns
`public inline const std::type_info & `[`type_info`](#classshogun_1_1Any_1ac962891325aacc89ab430a23a86d5157)`() const` | 
`public inline std::string `[`type`](#classshogun_1_1Any_1a9d92a94608e07bd972d6eb7f64cf6871)`() const` | Returns type-name of policy as string. 
`public inline void `[`visit`](#classshogun_1_1Any_1ac3699ca4f34b5c24396f588cea3c22e3)`(`[`AnyVisitor`](#classshogun_1_1AnyVisitor)` * visitor) const` | Visitor pattern. Calls the appropriate 'on' method of [AnyVisitor](#classshogun_1_1AnyVisitor).

## Members

#### `public inline  `[`Any`](#classshogun_1_1Any_1a07f7072608d83354a5eed8bbc94ce92b)`()` {#classshogun_1_1Any_1a07f7072608d83354a5eed8bbc94ce92b}

[Empty](#structshogun_1_1Empty) value constructor

#### `public inline  `[`Any`](#classshogun_1_1Any_1a2b1fa787aa0010e977015ebcc744ead2)`(`[`BaseAnyPolicy`](#classshogun_1_1BaseAnyPolicy)` * the_policy,void * the_storage)` {#classshogun_1_1Any_1a2b1fa787aa0010e977015ebcc744ead2}

Base constructor

#### `public template<>`  <br/>`inline  explicit `[`Any`](#classshogun_1_1Any_1afb533a0e5973b9273ec0d696e8cf7d91)`(const T & v)` {#classshogun_1_1Any_1afb533a0e5973b9273ec0d696e8cf7d91}

Constructor to copy value

#### `public inline  `[`Any`](#classshogun_1_1Any_1a91c4026dc28de330498ae8d94bc7b55a)`(const `[`Any`](#classshogun_1_1Any)` & other)` {#classshogun_1_1Any_1a91c4026dc28de330498ae8d94bc7b55a}

Copy constructor

#### `public inline  `[`Any`](#classshogun_1_1Any_1a381b29f8be43c8900c54046d89b854fd)`(`[`Any`](#classshogun_1_1Any)` && other)` {#classshogun_1_1Any_1a381b29f8be43c8900c54046d89b854fd}

Move constructor

#### `public inline `[`Any`](#classshogun_1_1Any)` & `[`operator=`](#classshogun_1_1Any_1a67a7d162cbd72dba19b0227d0c91d1ef)`(const `[`Any`](#classshogun_1_1Any)` & other)` {#classshogun_1_1Any_1a67a7d162cbd72dba19b0227d0c91d1ef}

Assignment operator 
#### Parameters
* `other` another [Any](#classshogun_1_1Any) object 

#### Returns
[Any](#classshogun_1_1Any) object

#### `public inline `[`Any`](#classshogun_1_1Any)` & `[`clone_from`](#classshogun_1_1Any_1a410b9b3085bbaad70867d284035ecc75)`(const `[`Any`](#classshogun_1_1Any)` & other)` {#classshogun_1_1Any_1a410b9b3085bbaad70867d284035ecc75}

#### `public inline  `[`~Any`](#classshogun_1_1Any_1a74082a1daff91f56146e67cc4e5e7666)`()` {#classshogun_1_1Any_1a74082a1daff91f56146e67cc4e5e7666}

Destructor

#### `public template<>`  <br/>`inline T `[`as`](#classshogun_1_1Any_1a0a722d04cee6bf06b968660956d7ebc3)`() const` {#classshogun_1_1Any_1a0a722d04cee6bf06b968660956d7ebc3}

Casts hidden value to provided type, fails otherwise. 
#### Returns
type-casted value

#### `public template<>`  <br/>`inline bool `[`has_type`](#classshogun_1_1Any_1ae3047fab975f854f3732892260f92f08)`() const` {#classshogun_1_1Any_1ae3047fab975f854f3732892260f92f08}

#### Returns
true if type is same.

#### `public template<>`  <br/>`inline bool `[`has_type_fallback`](#classshogun_1_1Any_1aacf89173620b4fd628b83d3bd1f219cb)`() const` {#classshogun_1_1Any_1aacf89173620b4fd628b83d3bd1f219cb}

#### Returns
true if type-id is same.

#### `public inline bool `[`empty`](#classshogun_1_1Any_1a644718bb2fb240de962dc3c9a1fdf0dc)`() const` {#classshogun_1_1Any_1a644718bb2fb240de962dc3c9a1fdf0dc}

#### Returns
true if [Any](#classshogun_1_1Any) object is empty.

#### `public inline bool `[`cloneable`](#classshogun_1_1Any_1a30da34ff3314046d5ff0b172d2415a44)`() const` {#classshogun_1_1Any_1a30da34ff3314046d5ff0b172d2415a44}

#### Returns
true if [Any](#classshogun_1_1Any) object is cloneable.

#### `public inline bool `[`visitable`](#classshogun_1_1Any_1a4be6bc8666266476a54efb8122f8b9b4)`() const` {#classshogun_1_1Any_1a4be6bc8666266476a54efb8122f8b9b4}

#### Returns
true if [Any](#classshogun_1_1Any) object is visitable.

#### `public inline const std::type_info & `[`type_info`](#classshogun_1_1Any_1ac962891325aacc89ab430a23a86d5157)`() const` {#classshogun_1_1Any_1ac962891325aacc89ab430a23a86d5157}

#### `public inline std::string `[`type`](#classshogun_1_1Any_1a9d92a94608e07bd972d6eb7f64cf6871)`() const` {#classshogun_1_1Any_1a9d92a94608e07bd972d6eb7f64cf6871}

Returns type-name of policy as string. 
#### Returns
name of type class

#### `public inline void `[`visit`](#classshogun_1_1Any_1ac3699ca4f34b5c24396f588cea3c22e3)`(`[`AnyVisitor`](#classshogun_1_1AnyVisitor)` * visitor) const` {#classshogun_1_1Any_1ac3699ca4f34b5c24396f588cea3c22e3}

Visitor pattern. Calls the appropriate 'on' method of [AnyVisitor](#classshogun_1_1AnyVisitor).

#### Parameters
* `visitor` visitor object to use

