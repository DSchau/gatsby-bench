---
classname: "shogun::SGString"
type: "class"
---

# class `shogun::SGString` {#classshogun_1_1SGString}

shogun string

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public T * `[`string`](#classshogun_1_1SGString_1a7f28c1633d065aba666a84f225c64466) | string
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`slen`](#classshogun_1_1SGString_1a9ec8aec3193f1d40fa7c6b9c551b34f3) | length of string
`public bool `[`do_free`](#classshogun_1_1SGString_1a3a57b448bad8ae10decd6afe54acc14c) | whether string needs to be freed
`public  `[`SGString`](#classshogun_1_1SGString_1a5ac4f3039c80231994e73a12e77b788d)`()` | default constructor
`public  `[`SGString`](#classshogun_1_1SGString_1a4769e7c76409352c8cca808f88be0d69)`(T * s,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` l,bool free_s)` | constructor for setting params
`public  `[`SGString`](#classshogun_1_1SGString_1adea83baf47acdd3ced32ebbfbb46cdb9)`(`[`SGVector`](#classshogun_1_1SGVector)`< T > v)` | constructor for setting params from a [SGVector](#classshogun_1_1SGVector)
`public  `[`SGString`](#classshogun_1_1SGString_1aa1c818d5ff58290fb152549380cbacc2)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` len,bool free_s)` | constructor to create new string in memory
`public  `[`SGString`](#classshogun_1_1SGString_1a702c2e4e87ad1bbe837ef561821adb14)`(const `[`SGString`](#classshogun_1_1SGString)` & orig)` | copy constructor
`public bool `[`operator==`](#classshogun_1_1SGString_1ac68dfce016b4771a1bb81f4cc9d11af6)`(const `[`SGString`](#classshogun_1_1SGString)` & other) const` | #### Returns
`public bool `[`equals`](#classshogun_1_1SGString_1aa6dc1102fb7f967c44b7702e20aeea7c)`(const `[`SGString`](#classshogun_1_1SGString)` & other) const` | #### Returns
`public `[`SGString`](#classshogun_1_1SGString)`< T > `[`clone`](#classshogun_1_1SGString_1a15c0d78ba7b346ee5671147618bd6ae5)`() const` | Clone string
`public void `[`free_string`](#classshogun_1_1SGString_1a4dad796f544cc7cfa5647391959a70e9)`()` | free string
`public void `[`destroy_string`](#classshogun_1_1SGString_1a3b5af31c10539b4e195b4faa43379eee)`()` | destroy string
`public inline `[`SGString`](#classshogun_1_1SGString)`< T > `[`get`](#classshogun_1_1SGString_1ad4dcf0ba30523bf0f3e9b7efa7142772)`()` | get the string (no copying is done here)
`public void `[`load`](#classshogun_1_1SGString_1a5d33ec59a4be25056cca1f3b6691ad00)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` | load string from file
`public void `[`save`](#classshogun_1_1SGString_1aff4d5355fe0d9b68bc8c71cd331c082e)`(`[`CFile`](#classshogun_1_1CFile)` * saver)` | save string to file

## Members

#### `public T * `[`string`](#classshogun_1_1SGString_1a7f28c1633d065aba666a84f225c64466) {#classshogun_1_1SGString_1a7f28c1633d065aba666a84f225c64466}

string

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`slen`](#classshogun_1_1SGString_1a9ec8aec3193f1d40fa7c6b9c551b34f3) {#classshogun_1_1SGString_1a9ec8aec3193f1d40fa7c6b9c551b34f3}

length of string

#### `public bool `[`do_free`](#classshogun_1_1SGString_1a3a57b448bad8ae10decd6afe54acc14c) {#classshogun_1_1SGString_1a3a57b448bad8ae10decd6afe54acc14c}

whether string needs to be freed

#### `public  `[`SGString`](#classshogun_1_1SGString_1a5ac4f3039c80231994e73a12e77b788d)`()` {#classshogun_1_1SGString_1a5ac4f3039c80231994e73a12e77b788d}

default constructor

#### `public  `[`SGString`](#classshogun_1_1SGString_1a4769e7c76409352c8cca808f88be0d69)`(T * s,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` l,bool free_s)` {#classshogun_1_1SGString_1a4769e7c76409352c8cca808f88be0d69}

constructor for setting params

#### `public  `[`SGString`](#classshogun_1_1SGString_1adea83baf47acdd3ced32ebbfbb46cdb9)`(`[`SGVector`](#classshogun_1_1SGVector)`< T > v)` {#classshogun_1_1SGString_1adea83baf47acdd3ced32ebbfbb46cdb9}

constructor for setting params from a [SGVector](#classshogun_1_1SGVector)

#### `public  `[`SGString`](#classshogun_1_1SGString_1aa1c818d5ff58290fb152549380cbacc2)`(`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` len,bool free_s)` {#classshogun_1_1SGString_1aa1c818d5ff58290fb152549380cbacc2}

constructor to create new string in memory

#### `public  `[`SGString`](#classshogun_1_1SGString_1a702c2e4e87ad1bbe837ef561821adb14)`(const `[`SGString`](#classshogun_1_1SGString)` & orig)` {#classshogun_1_1SGString_1a702c2e4e87ad1bbe837ef561821adb14}

copy constructor

#### `public bool `[`operator==`](#classshogun_1_1SGString_1ac68dfce016b4771a1bb81f4cc9d11af6)`(const `[`SGString`](#classshogun_1_1SGString)` & other) const` {#classshogun_1_1SGString_1ac68dfce016b4771a1bb81f4cc9d11af6}

#### Returns
true iff pointer and size are equal

#### `public bool `[`equals`](#classshogun_1_1SGString_1aa6dc1102fb7f967c44b7702e20aeea7c)`(const `[`SGString`](#classshogun_1_1SGString)` & other) const` {#classshogun_1_1SGString_1aa6dc1102fb7f967c44b7702e20aeea7c}

#### Returns
true iff content is equal

#### `public `[`SGString`](#classshogun_1_1SGString)`< T > `[`clone`](#classshogun_1_1SGString_1a15c0d78ba7b346ee5671147618bd6ae5)`() const` {#classshogun_1_1SGString_1a15c0d78ba7b346ee5671147618bd6ae5}

Clone string

#### `public void `[`free_string`](#classshogun_1_1SGString_1a4dad796f544cc7cfa5647391959a70e9)`()` {#classshogun_1_1SGString_1a4dad796f544cc7cfa5647391959a70e9}

free string

#### `public void `[`destroy_string`](#classshogun_1_1SGString_1a3b5af31c10539b4e195b4faa43379eee)`()` {#classshogun_1_1SGString_1a3b5af31c10539b4e195b4faa43379eee}

destroy string

#### `public inline `[`SGString`](#classshogun_1_1SGString)`< T > `[`get`](#classshogun_1_1SGString_1ad4dcf0ba30523bf0f3e9b7efa7142772)`()` {#classshogun_1_1SGString_1ad4dcf0ba30523bf0f3e9b7efa7142772}

get the string (no copying is done here)

#### Returns
the refcount increased string

#### `public void `[`load`](#classshogun_1_1SGString_1a5d33ec59a4be25056cca1f3b6691ad00)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` {#classshogun_1_1SGString_1a5d33ec59a4be25056cca1f3b6691ad00}

load string from file

#### Parameters
* `loader` File object via which to load data

#### `public void `[`save`](#classshogun_1_1SGString_1aff4d5355fe0d9b68bc8c71cd331c082e)`(`[`CFile`](#classshogun_1_1CFile)` * saver)` {#classshogun_1_1SGString_1aff4d5355fe0d9b68bc8c71cd331c082e}

save string to file

#### Parameters
* `saver` File object via which to save data

