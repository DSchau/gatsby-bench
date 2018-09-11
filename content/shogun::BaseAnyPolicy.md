---
classname: "shogun::BaseAnyPolicy"
type: "class"
---

# class `shogun::BaseAnyPolicy` {#classshogun_1_1BaseAnyPolicy}

An interface for a policy to store a value. Value can be any data like primitive data-types, shogun objects, etc. Policy defines how to handle this data. It works with a provided memory region and is able to set value, clear it and return the type-name as string.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public void `[`set`](#classshogun_1_1BaseAnyPolicy_1ae4072acb0fe4128427f186db1639b40e)`(void ** storage,const void * v) const` | Puts provided value pointed by v (untyped to be generic) to storage. 
`public void `[`clone`](#classshogun_1_1BaseAnyPolicy_1a000df864c1aa7c7f9971a6f9004b7695)`(void ** storage,const void * from) const` | Clones value provided by from into storage 
`public void `[`clear`](#classshogun_1_1BaseAnyPolicy_1ada6d4def7769eb6994f068f278876286)`(void ** storage) const` | Clears storage. 
`public std::string `[`type`](#classshogun_1_1BaseAnyPolicy_1ae89eb7d1fb1f2d4594b941749205de4e)`() const` | Returns type-name as string. 
`public const std::type_info & `[`type_info`](#classshogun_1_1BaseAnyPolicy_1a4e287a4a2d7d6da577c8b6b57ac5624e)`() const` | Returns type info 
`public bool `[`matches_type`](#classshogun_1_1BaseAnyPolicy_1aa87d2bd37f52c949f563e7c40abd4903)`(const std::type_info & ti) const` | Compares type. 
`public bool `[`matches_policy`](#classshogun_1_1BaseAnyPolicy_1a6519ce6e7df5e2536884d8abf9876c75)`(`[`BaseAnyPolicy`](#classshogun_1_1BaseAnyPolicy)` * other) const` | Checks if policies are compatible. 
`public bool `[`equals`](#classshogun_1_1BaseAnyPolicy_1a83ff4385897a45c9b96b6db64716922c)`(const void * storage,const void * other_storage) const` | Compares two storages. 
`public `[`PolicyType`](#namespaceshogun_1a0d954142616a43643b0df76caa6f75e5)` `[`policy_type`](#classshogun_1_1BaseAnyPolicy_1a1c814be00c112d396da835076ed52dd1)`() const` | Returns the type of policy. 
`public void `[`visit`](#classshogun_1_1BaseAnyPolicy_1a6f98ff144e7dc588464c1b330c05fb98)`(void * storage,`[`AnyVisitor`](#classshogun_1_1AnyVisitor)` * visitor) const` | Visitor pattern. Calls the appropriate 'on' method of [AnyVisitor](#classshogun_1_1AnyVisitor).
`public bool `[`is_functional`](#classshogun_1_1BaseAnyPolicy_1a4fff660bed9b2a6346c5716c1b0d44ef)`() const` | 

## Members

#### `public void `[`set`](#classshogun_1_1BaseAnyPolicy_1ae4072acb0fe4128427f186db1639b40e)`(void ** storage,const void * v) const` {#classshogun_1_1BaseAnyPolicy_1ae4072acb0fe4128427f186db1639b40e}

Puts provided value pointed by v (untyped to be generic) to storage. 
#### Parameters
* `storage` pointer to a pointer to storage 

* `v` pointer to value

#### `public void `[`clone`](#classshogun_1_1BaseAnyPolicy_1a000df864c1aa7c7f9971a6f9004b7695)`(void ** storage,const void * from) const` {#classshogun_1_1BaseAnyPolicy_1a000df864c1aa7c7f9971a6f9004b7695}

Clones value provided by from into storage 
#### Parameters
* `storage` pointer to a pointer to storage 

* `from` pointer to value to clone

#### `public void `[`clear`](#classshogun_1_1BaseAnyPolicy_1ada6d4def7769eb6994f068f278876286)`(void ** storage) const` {#classshogun_1_1BaseAnyPolicy_1ada6d4def7769eb6994f068f278876286}

Clears storage. 
#### Parameters
* `storage` pointer to a pointer to storage

#### `public std::string `[`type`](#classshogun_1_1BaseAnyPolicy_1ae89eb7d1fb1f2d4594b941749205de4e)`() const` {#classshogun_1_1BaseAnyPolicy_1ae89eb7d1fb1f2d4594b941749205de4e}

Returns type-name as string. 
#### Returns
name of type class

#### `public const std::type_info & `[`type_info`](#classshogun_1_1BaseAnyPolicy_1a4e287a4a2d7d6da577c8b6b57ac5624e)`() const` {#classshogun_1_1BaseAnyPolicy_1a4e287a4a2d7d6da577c8b6b57ac5624e}

Returns type info 
#### Returns
type info of value's type

#### `public bool `[`matches_type`](#classshogun_1_1BaseAnyPolicy_1aa87d2bd37f52c949f563e7c40abd4903)`(const std::type_info & ti) const` {#classshogun_1_1BaseAnyPolicy_1aa87d2bd37f52c949f563e7c40abd4903}

Compares type. 
#### Parameters
* `ti` type information 

#### Returns
true if type matches

#### `public bool `[`matches_policy`](#classshogun_1_1BaseAnyPolicy_1a6519ce6e7df5e2536884d8abf9876c75)`(`[`BaseAnyPolicy`](#classshogun_1_1BaseAnyPolicy)` * other) const` {#classshogun_1_1BaseAnyPolicy_1a6519ce6e7df5e2536884d8abf9876c75}

Checks if policies are compatible. 
#### Parameters
* `other` other policy 

#### Returns
true if policies do match

#### `public bool `[`equals`](#classshogun_1_1BaseAnyPolicy_1a83ff4385897a45c9b96b6db64716922c)`(const void * storage,const void * other_storage) const` {#classshogun_1_1BaseAnyPolicy_1a83ff4385897a45c9b96b6db64716922c}

Compares two storages. 
#### Parameters
* `storage` pointer to a pointer to storage 

* `other_storage` pointer to a pointer to another storage 

#### Returns
true if both storages have same value

#### `public `[`PolicyType`](#namespaceshogun_1a0d954142616a43643b0df76caa6f75e5)` `[`policy_type`](#classshogun_1_1BaseAnyPolicy_1a1c814be00c112d396da835076ed52dd1)`() const` {#classshogun_1_1BaseAnyPolicy_1a1c814be00c112d396da835076ed52dd1}

Returns the type of policy. 
#### Returns
type of policy

#### `public void `[`visit`](#classshogun_1_1BaseAnyPolicy_1a6f98ff144e7dc588464c1b330c05fb98)`(void * storage,`[`AnyVisitor`](#classshogun_1_1AnyVisitor)` * visitor) const` {#classshogun_1_1BaseAnyPolicy_1a6f98ff144e7dc588464c1b330c05fb98}

Visitor pattern. Calls the appropriate 'on' method of [AnyVisitor](#classshogun_1_1AnyVisitor).

#### Parameters
* `storage` pointer to storage 

* `visitor` abstract visitor to use

#### `public bool `[`is_functional`](#classshogun_1_1BaseAnyPolicy_1a4fff660bed9b2a6346c5716c1b0d44ef)`() const` {#classshogun_1_1BaseAnyPolicy_1a4fff660bed9b2a6346c5716c1b0d44ef}

