---
classname: "shogun::internal::Block"
type: "class"
---

# class `shogun::internal::Block` {#classshogun_1_1internal_1_1Block}

Class that holds a block feature. A block feature is a shallow copy of an underlying (non-owning) feature object. In its constructor, it increases the refcount of the original object (since it has to be alive as long as the block is alive) and it decreases the refcount of the original object in destructor.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public  `[`Block`](#classshogun_1_1internal_1_1Block_1a48fc8795b60efac1ef421f1c0e5141b8)`(const `[`Block`](#classshogun_1_1internal_1_1Block)` & other)` | Copy constructor. Every time a block is copied or assigned, the underlying feature object is SG_REF'd.
`public `[`Block`](#classshogun_1_1internal_1_1Block)` & `[`operator=`](#classshogun_1_1internal_1_1Block_1a8a3f8788002e123f11e5a1c72075a075)`(const `[`Block`](#classshogun_1_1internal_1_1Block)` & other)` | Assignment operator. Every time a block is copied or assigned, the underlying feature object is SG_REF'd.
`public  `[`~Block`](#classshogun_1_1internal_1_1Block_1a06b6fb79eca9133ea0d036865de71e1f)`()` | Destructor. Decreases the reference count of the underlying feature object.
`public inline  `[`operator CFeatures *`](#classshogun_1_1internal_1_1Block_1a406c4aba5b119d321261fd58fe9bd072)`()` | Operator overloading for getting the block object as a naked ptr (non-const, unsafe).

## Members

#### `public  `[`Block`](#classshogun_1_1internal_1_1Block_1a48fc8795b60efac1ef421f1c0e5141b8)`(const `[`Block`](#classshogun_1_1internal_1_1Block)` & other)` {#classshogun_1_1internal_1_1Block_1a48fc8795b60efac1ef421f1c0e5141b8}

Copy constructor. Every time a block is copied or assigned, the underlying feature object is SG_REF'd.

#### `public `[`Block`](#classshogun_1_1internal_1_1Block)` & `[`operator=`](#classshogun_1_1internal_1_1Block_1a8a3f8788002e123f11e5a1c72075a075)`(const `[`Block`](#classshogun_1_1internal_1_1Block)` & other)` {#classshogun_1_1internal_1_1Block_1a8a3f8788002e123f11e5a1c72075a075}

Assignment operator. Every time a block is copied or assigned, the underlying feature object is SG_REF'd.

#### `public  `[`~Block`](#classshogun_1_1internal_1_1Block_1a06b6fb79eca9133ea0d036865de71e1f)`()` {#classshogun_1_1internal_1_1Block_1a06b6fb79eca9133ea0d036865de71e1f}

Destructor. Decreases the reference count of the underlying feature object.

#### `public inline  `[`operator CFeatures *`](#classshogun_1_1internal_1_1Block_1a406c4aba5b119d321261fd58fe9bd072)`()` {#classshogun_1_1internal_1_1Block_1a406c4aba5b119d321261fd58fe9bd072}

Operator overloading for getting the block object as a naked ptr (non-const, unsafe).

