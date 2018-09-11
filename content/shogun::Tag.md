---
classname: "shogun::Tag"
type: "class"
parents:
   - BaseTag
---

# class `shogun::Tag` {#classshogun_1_1Tag}

```
class shogun::Tag
  : public BaseTag
```

Acts as an identifier for a shogun object. It contains type information and name of the object. Generally used to CSGObject::set() and [CSGObject::get()](#classshogun_1_1CSGObject_1a4de6e15966500093d2c04db29bbf4ac7) parameters of a class.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public inline  explicit `[`Tag`](#classshogun_1_1Tag_1aa8a761f0ce48d435ee759c394bef079e)`(const std::string & _name)` | Constructor 
`public inline  `[`Tag`](#classshogun_1_1Tag_1ab07dae39c064401b112836c7952a62cd)`(const `[`Tag`](#classshogun_1_1Tag)` & other)` | Copy constructor 
`public inline std::string `[`name`](#classshogun_1_1BaseTag_1a1d89c28bd42ba9a52da008bb69367171)`() const` | #### Returns
`public inline std::size_t `[`hash`](#classshogun_1_1BaseTag_1ada6d4b3c044384f0fa0f1d990c0dcd96)`() const` | #### Returns

## Members

#### `public inline  explicit `[`Tag`](#classshogun_1_1Tag_1aa8a761f0ce48d435ee759c394bef079e)`(const std::string & _name)` {#classshogun_1_1Tag_1aa8a761f0ce48d435ee759c394bef079e}

Constructor 
#### Parameters
* `_name` name of tag

#### `public inline  `[`Tag`](#classshogun_1_1Tag_1ab07dae39c064401b112836c7952a62cd)`(const `[`Tag`](#classshogun_1_1Tag)` & other)` {#classshogun_1_1Tag_1ab07dae39c064401b112836c7952a62cd}

Copy constructor 
#### Parameters
* `other` another tag object to copy

#### `public inline std::string `[`name`](#classshogun_1_1BaseTag_1a1d89c28bd42ba9a52da008bb69367171)`() const` {#classshogun_1_1BaseTag_1a1d89c28bd42ba9a52da008bb69367171}

#### Returns
name of [Tag](#classshogun_1_1Tag)

#### `public inline std::size_t `[`hash`](#classshogun_1_1BaseTag_1ada6d4b3c044384f0fa0f1d990c0dcd96)`() const` {#classshogun_1_1BaseTag_1ada6d4b3c044384f0fa0f1d990c0dcd96}

#### Returns
hash of [Tag](#classshogun_1_1Tag)

