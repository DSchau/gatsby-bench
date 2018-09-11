---
classname: "shogun::BaseTag"
type: "class"
---

# class `shogun::BaseTag` {#classshogun_1_1BaseTag}

Base class for all tags. This class stores name and not the type information for a shogun object. It can be used as an identifier for a shogun object where type information is not known. One application of this can be found in CSGObject::set_param_with_btag().

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public inline  explicit `[`BaseTag`](#classshogun_1_1BaseTag_1a380546dcef5507b408254b97f6cbe288)`(const std::string & _name)` | Constructor to initialize hash from name 
`public inline  `[`BaseTag`](#classshogun_1_1BaseTag_1a05dc89cfe03bce80f616caf64417d087)`(const `[`BaseTag`](#classshogun_1_1BaseTag)` & other)` | Copy constructor 
`public inline `[`BaseTag`](#classshogun_1_1BaseTag)` & `[`operator=`](#classshogun_1_1BaseTag_1a5727dd20cbc3f28a301466f660583e04)`(const `[`BaseTag`](#classshogun_1_1BaseTag)` & other)` | Class Assignment operator 
`public inline std::string `[`name`](#classshogun_1_1BaseTag_1a1d89c28bd42ba9a52da008bb69367171)`() const` | #### Returns
`public inline std::size_t `[`hash`](#classshogun_1_1BaseTag_1ada6d4b3c044384f0fa0f1d990c0dcd96)`() const` | #### Returns

## Members

#### `public inline  explicit `[`BaseTag`](#classshogun_1_1BaseTag_1a380546dcef5507b408254b97f6cbe288)`(const std::string & _name)` {#classshogun_1_1BaseTag_1a380546dcef5507b408254b97f6cbe288}

Constructor to initialize hash from name 
#### Parameters
* `_name` name for tag

#### `public inline  `[`BaseTag`](#classshogun_1_1BaseTag_1a05dc89cfe03bce80f616caf64417d087)`(const `[`BaseTag`](#classshogun_1_1BaseTag)` & other)` {#classshogun_1_1BaseTag_1a05dc89cfe03bce80f616caf64417d087}

Copy constructor 
#### Parameters
* `other` basetag object to be copied

#### `public inline `[`BaseTag`](#classshogun_1_1BaseTag)` & `[`operator=`](#classshogun_1_1BaseTag_1a5727dd20cbc3f28a301466f660583e04)`(const `[`BaseTag`](#classshogun_1_1BaseTag)` & other)` {#classshogun_1_1BaseTag_1a5727dd20cbc3f28a301466f660583e04}

Class Assignment operator 
#### Parameters
* `other` basetag object to be assigned

#### `public inline std::string `[`name`](#classshogun_1_1BaseTag_1a1d89c28bd42ba9a52da008bb69367171)`() const` {#classshogun_1_1BaseTag_1a1d89c28bd42ba9a52da008bb69367171}

#### Returns
name of [Tag](#classshogun_1_1Tag)

#### `public inline std::size_t `[`hash`](#classshogun_1_1BaseTag_1ada6d4b3c044384f0fa0f1d990c0dcd96)`() const` {#classshogun_1_1BaseTag_1ada6d4b3c044384f0fa0f1d990c0dcd96}

#### Returns
hash of [Tag](#classshogun_1_1Tag)

