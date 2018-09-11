---
classname: "shogun::PointerValueAnyPolicy"
type: "class"
parents:
   - shogun::TypedAnyPolicy< T >
---

# class `shogun::PointerValueAnyPolicy` {#classshogun_1_1PointerValueAnyPolicy}

```
class shogun::PointerValueAnyPolicy
  : public shogun::TypedAnyPolicy< T >
```

This is one concrete implementation of policy that uses void pointers to store values.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public inline virtual void `[`set`](#classshogun_1_1PointerValueAnyPolicy_1ae63f3242418a2e70a626f9c8c2c4e460)`(void ** storage,const void * v) const` | Puts provided value pointed by v (untyped to be generic) to storage. 
`public inline virtual void `[`clone`](#classshogun_1_1PointerValueAnyPolicy_1aa08402782418ba4157121427e7f56c54)`(void ** storage,const void * from) const` | Clones value provided by from into storage 
`public inline virtual void `[`clear`](#classshogun_1_1PointerValueAnyPolicy_1acd831686f4adff0e520ff878103fef71)`(void ** storage) const` | Clears storage. 
`public virtual bool `[`matches_policy`](#classshogun_1_1PointerValueAnyPolicy_1a70bc26b73b0fd18f7c42101876a82139)`(`[`BaseAnyPolicy`](#classshogun_1_1BaseAnyPolicy)` * other) const` | Checks if policies are compatible. 
`public inline virtual bool `[`equals`](#classshogun_1_1PointerValueAnyPolicy_1a21b1427248e33f98ad7de4a824e8f563)`(const void * storage,const void * other_storage) const` | Compares two storages. 
`public inline virtual `[`PolicyType`](#namespaceshogun_1a0d954142616a43643b0df76caa6f75e5)` `[`policy_type`](#classshogun_1_1PointerValueAnyPolicy_1a255740fd8004fc9aab62e194192c96ca)`() const` | Returns the type of policy. 
`public inline virtual void `[`visit`](#classshogun_1_1PointerValueAnyPolicy_1a2a6700d5b62d01db9d7ebef3665c6bc4)`(void * storage,`[`AnyVisitor`](#classshogun_1_1AnyVisitor)` * visitor) const` | Visitor pattern. Calls the appropriate 'on' method of [AnyVisitor](#classshogun_1_1AnyVisitor).
`public inline virtual std::string `[`type`](#classshogun_1_1TypedAnyPolicy_1a5f7e89e020a940e8b05ccb171cfbc8b8)`() const` | Returns type-name as string. 
`public inline virtual const std::type_info & `[`type_info`](#classshogun_1_1TypedAnyPolicy_1aad68a099433abcc00997566f82c1761d)`() const` | Returns type info 
`public inline virtual bool `[`matches_type`](#classshogun_1_1TypedAnyPolicy_1a28c97d7aa8df5d70e5ccecbdead59b26)`(const std::type_info & ti) const` | Compares type. 
`public inline virtual bool `[`is_functional`](#classshogun_1_1TypedAnyPolicy_1a4b94a60e31ec465631edcd793b2ee924)`() const` | 

## Members

#### `public inline virtual void `[`set`](#classshogun_1_1PointerValueAnyPolicy_1ae63f3242418a2e70a626f9c8c2c4e460)`(void ** storage,const void * v) const` {#classshogun_1_1PointerValueAnyPolicy_1ae63f3242418a2e70a626f9c8c2c4e460}

Puts provided value pointed by v (untyped to be generic) to storage. 
#### Parameters
* `storage` pointer to a pointer to storage 

* `v` pointer to value

#### `public inline virtual void `[`clone`](#classshogun_1_1PointerValueAnyPolicy_1aa08402782418ba4157121427e7f56c54)`(void ** storage,const void * from) const` {#classshogun_1_1PointerValueAnyPolicy_1aa08402782418ba4157121427e7f56c54}

Clones value provided by from into storage 
#### Parameters
* `storage` pointer to a pointer to storage 

* `from` pointer to value to clone

#### `public inline virtual void `[`clear`](#classshogun_1_1PointerValueAnyPolicy_1acd831686f4adff0e520ff878103fef71)`(void ** storage) const` {#classshogun_1_1PointerValueAnyPolicy_1acd831686f4adff0e520ff878103fef71}

Clears storage. 
#### Parameters
* `storage` pointer to a pointer to storage

#### `public virtual bool `[`matches_policy`](#classshogun_1_1PointerValueAnyPolicy_1a70bc26b73b0fd18f7c42101876a82139)`(`[`BaseAnyPolicy`](#classshogun_1_1BaseAnyPolicy)` * other) const` {#classshogun_1_1PointerValueAnyPolicy_1a70bc26b73b0fd18f7c42101876a82139}

Checks if policies are compatible. 
#### Parameters
* `other` other policy 

#### Returns
true if policies do match

#### `public inline virtual bool `[`equals`](#classshogun_1_1PointerValueAnyPolicy_1a21b1427248e33f98ad7de4a824e8f563)`(const void * storage,const void * other_storage) const` {#classshogun_1_1PointerValueAnyPolicy_1a21b1427248e33f98ad7de4a824e8f563}

Compares two storages. 
#### Parameters
* `storage` pointer to a pointer to storage 

* `other_storage` pointer to a pointer to another storage 

#### Returns
true if both storages have same value

#### `public inline virtual `[`PolicyType`](#namespaceshogun_1a0d954142616a43643b0df76caa6f75e5)` `[`policy_type`](#classshogun_1_1PointerValueAnyPolicy_1a255740fd8004fc9aab62e194192c96ca)`() const` {#classshogun_1_1PointerValueAnyPolicy_1a255740fd8004fc9aab62e194192c96ca}

Returns the type of policy. 
#### Returns
type of policy

#### `public inline virtual void `[`visit`](#classshogun_1_1PointerValueAnyPolicy_1a2a6700d5b62d01db9d7ebef3665c6bc4)`(void * storage,`[`AnyVisitor`](#classshogun_1_1AnyVisitor)` * visitor) const` {#classshogun_1_1PointerValueAnyPolicy_1a2a6700d5b62d01db9d7ebef3665c6bc4}

Visitor pattern. Calls the appropriate 'on' method of [AnyVisitor](#classshogun_1_1AnyVisitor).

#### Parameters
* `storage` pointer to a pointer to storage 

* `visitor` abstract visitor to use

#### `public inline virtual std::string `[`type`](#classshogun_1_1TypedAnyPolicy_1a5f7e89e020a940e8b05ccb171cfbc8b8)`() const` {#classshogun_1_1TypedAnyPolicy_1a5f7e89e020a940e8b05ccb171cfbc8b8}

Returns type-name as string. 
#### Returns
name of type class

#### `public inline virtual const std::type_info & `[`type_info`](#classshogun_1_1TypedAnyPolicy_1aad68a099433abcc00997566f82c1761d)`() const` {#classshogun_1_1TypedAnyPolicy_1aad68a099433abcc00997566f82c1761d}

Returns type info 
#### Returns
type info of value's type

#### `public inline virtual bool `[`matches_type`](#classshogun_1_1TypedAnyPolicy_1a28c97d7aa8df5d70e5ccecbdead59b26)`(const std::type_info & ti) const` {#classshogun_1_1TypedAnyPolicy_1a28c97d7aa8df5d70e5ccecbdead59b26}

Compares type. 
#### Parameters
* `ti` type information 

#### Returns
true if type matches

#### `public inline virtual bool `[`is_functional`](#classshogun_1_1TypedAnyPolicy_1a4b94a60e31ec465631edcd793b2ee924)`() const` {#classshogun_1_1TypedAnyPolicy_1a4b94a60e31ec465631edcd793b2ee924}

