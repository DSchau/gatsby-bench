---
classname: "shogun::internal::NextSamples"
type: "class"
---

# class `shogun::internal::NextSamples` {#classshogun_1_1internal_1_1NextSamples}

class [NextSamples](#classshogun_1_1internal_1_1NextSamples) is the return type for next() call in [DataManager](#classshogun_1_1internal_1_1DataManager). If there are no more samples (from any one of the distributions), an empty instance of [NextSamples](#classshogun_1_1internal_1_1NextSamples) is supposed to be returned. This can be verified from the caller by calling the [empty()](#classshogun_1_1internal_1_1NextSamples_1a8c6573cb2ef47dafba7caaa30085b78c) method. Otherwise, always a get() call with appropriate index would give the samples from that distribution. If an inappropriate index is provided, e.g. get(2) for a two-sample test, a runtime exception is thrown.

[Example](#classshogun_1_1Example) usage: 
```cpp
NextSamples next_samples(2);
next_samples[0] = fetchers[0].next();
next_samples[1] = fetchers[1].next();
if (!next_samples.empty())
{
    auto first = next_samples[0];
    auto second = next_samples[1];
    auto third = next_samples[2]; / Runtime Error
}
```

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public `[`NextSamples`](#classshogun_1_1internal_1_1NextSamples)` & `[`operator=`](#classshogun_1_1internal_1_1NextSamples_1a8c9169d6d40ee9a6d5e5065f51199950)`(const `[`NextSamples`](#classshogun_1_1internal_1_1NextSamples)` & other)` | Assignment operator. Clears the current blocks.
`public  `[`~NextSamples`](#classshogun_1_1internal_1_1NextSamples_1a42325676828c895a907511d74f50a689)`()` | Destructor
`public std::vector< `[`Block`](#classshogun_1_1internal_1_1Block)` > & `[`operator[]`](#classshogun_1_1internal_1_1NextSamples_1ad6cdf4daf94e46a1a0bb0513dca263d9)`(size_t i)` | Contains a number of blocks (of samples) fetched in the current burst from a specified distribution.
`public const std::vector< `[`Block`](#classshogun_1_1internal_1_1Block)` > & `[`operator[]`](#classshogun_1_1internal_1_1NextSamples_1a0c623d45a1847c4175e67f63dcdfc612)`(size_t i) const` | Const version of the above. This is called when a const instance of [NextSamples](#classshogun_1_1internal_1_1NextSamples) is returned.
`public const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`num_blocks`](#classshogun_1_1internal_1_1NextSamples_1a4548c14012124578e6857042e4689188)`() const` | #### Returns
`public const bool `[`empty`](#classshogun_1_1internal_1_1NextSamples_1a8c6573cb2ef47dafba7caaa30085b78c)`() const` | This returns true if any of the distribution fetched 0 blocks (checked from the size of the vector for that distribution)
`public void `[`clear`](#classshogun_1_1internal_1_1NextSamples_1ac8bb3912a3ce86b15842e79d0b421204)`()` | Method that clears the memory occupied by the feature objects inside.

## Members

#### `public `[`NextSamples`](#classshogun_1_1internal_1_1NextSamples)` & `[`operator=`](#classshogun_1_1internal_1_1NextSamples_1a8c9169d6d40ee9a6d5e5065f51199950)`(const `[`NextSamples`](#classshogun_1_1internal_1_1NextSamples)` & other)` {#classshogun_1_1internal_1_1NextSamples_1a8c9169d6d40ee9a6d5e5065f51199950}

Assignment operator. Clears the current blocks.

#### `public  `[`~NextSamples`](#classshogun_1_1internal_1_1NextSamples_1a42325676828c895a907511d74f50a689)`()` {#classshogun_1_1internal_1_1NextSamples_1a42325676828c895a907511d74f50a689}

Destructor

#### `public std::vector< `[`Block`](#classshogun_1_1internal_1_1Block)` > & `[`operator[]`](#classshogun_1_1internal_1_1NextSamples_1ad6cdf4daf94e46a1a0bb0513dca263d9)`(size_t i)` {#classshogun_1_1internal_1_1NextSamples_1ad6cdf4daf94e46a1a0bb0513dca263d9}

Contains a number of blocks (of samples) fetched in the current burst from a specified distribution.

#### Parameters
* `i` determines samples from which distribution 

#### Returns
a vector of fetched blocks of features from the specified distribution

#### `public const std::vector< `[`Block`](#classshogun_1_1internal_1_1Block)` > & `[`operator[]`](#classshogun_1_1internal_1_1NextSamples_1a0c623d45a1847c4175e67f63dcdfc612)`(size_t i) const` {#classshogun_1_1internal_1_1NextSamples_1a0c623d45a1847c4175e67f63dcdfc612}

Const version of the above. This is called when a const instance of [NextSamples](#classshogun_1_1internal_1_1NextSamples) is returned.

#### `public const `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`num_blocks`](#classshogun_1_1internal_1_1NextSamples_1a4548c14012124578e6857042e4689188)`() const` {#classshogun_1_1internal_1_1NextSamples_1a4548c14012124578e6857042e4689188}

#### Returns
number of blocks fetched from each of the distribution. It is assumed that this number is same for all the distributions.

#### `public const bool `[`empty`](#classshogun_1_1internal_1_1NextSamples_1a8c6573cb2ef47dafba7caaa30085b78c)`() const` {#classshogun_1_1internal_1_1NextSamples_1a8c6573cb2ef47dafba7caaa30085b78c}

This returns true if any of the distribution fetched 0 blocks (checked from the size of the vector for that distribution)

#### Returns
whether this instance does not contain any blocks of samples from any of the distribution

#### `public void `[`clear`](#classshogun_1_1internal_1_1NextSamples_1ac8bb3912a3ce86b15842e79d0b421204)`()` {#classshogun_1_1internal_1_1NextSamples_1ac8bb3912a3ce86b15842e79d0b421204}

Method that clears the memory occupied by the feature objects inside.

