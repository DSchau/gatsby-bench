---
classname: "shogun::PRange"
type: "class"
---

# class `shogun::PRange` {#classshogun_1_1PRange}

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public inline  `[`PRange`](#classshogun_1_1PRange_1a93d64ee4a2a495fc365c74302e5122fe)`(`[`Range`](#classshogun_1_1Range)`< T > range,const `[`SGIO`](#classshogun_1_1SGIO)` & io,const std::string prefix,const `[`SG_PRG_MODE`](#namespaceshogun_1a2d152916e795a22fa2b10bbf840b09a6)` mode,std::function< bool()> condition)` | Constructor, initialize the progress bar manager.
`public inline `[`PIterator`](#classshogun_1_1PRange_1_1PIterator)` `[`begin`](#classshogun_1_1PRange_1a43a92fb1c1d745fa5a435b01f1ff2c82)`() const` | Create the iterator that corresponds to the start of the range. Used within the range-based loop version of the progress bar.
`public inline `[`PIterator`](#classshogun_1_1PRange_1_1PIterator)` `[`end`](#classshogun_1_1PRange_1a8f22bb5b04f0e9351f23c205ce9ca609)`() const` | Create the iterator that corresponds to the end of the range. Used within the range-based loop version of the progress bar.
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_current_progress`](#classshogun_1_1PRange_1adca5330e0fa343586b94be938c06ca36)`() const` | Return the current progress bar value. Used for testing purposes. 
`public inline void `[`print_progress`](#classshogun_1_1PRange_1a6e48dbe7de14d07c909f0d92302f19e8)`() const` | Print the progress bar. This method must be called each time we want the progress bar to be updated. 
`public inline void `[`print_absolute`](#classshogun_1_1PRange_1a4bb17ef2c53d38bb4997357bd7085ded)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` current_val,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` val,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` min_value,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` max_value) const` | Print the absolute progress bar. This method must be called each time we want the progress bar to be updated.
`public inline void `[`complete`](#classshogun_1_1PRange_1a5c23dc5dc0f68d251db743dbde10988c)`() const` | Print the progress bar end. This method must be called one time, after the loop. 
`public inline void `[`complete_absolute`](#classshogun_1_1PRange_1a4d889a29f78e822c605f03240a57f3cc)`() const` | Print the progress bar end. This method must be called one time, after the loop. 

## Members

#### `public inline  `[`PRange`](#classshogun_1_1PRange_1a93d64ee4a2a495fc365c74302e5122fe)`(`[`Range`](#classshogun_1_1Range)`< T > range,const `[`SGIO`](#classshogun_1_1SGIO)` & io,const std::string prefix,const `[`SG_PRG_MODE`](#namespaceshogun_1a2d152916e795a22fa2b10bbf840b09a6)` mode,std::function< bool()> condition)` {#classshogun_1_1PRange_1a93d64ee4a2a495fc365c74302e5122fe}

Constructor, initialize the progress bar manager.

#### Parameters
* `range` the range to loop over 

* `io` the [SGIO](#classshogun_1_1SGIO) object which will be used to print the progress bar 

* `prefix` the string prefix which will be printed before the progress bar 

* `mode` the char mode used to print the progress bar (ASCII, UTF8 etc.) 

* `condition` premature stop condition for the loop

#### `public inline `[`PIterator`](#classshogun_1_1PRange_1_1PIterator)` `[`begin`](#classshogun_1_1PRange_1a43a92fb1c1d745fa5a435b01f1ff2c82)`() const` {#classshogun_1_1PRange_1a43a92fb1c1d745fa5a435b01f1ff2c82}

Create the iterator that corresponds to the start of the range. Used within the range-based loop version of the progress bar.

```cpp
for (auto i: progress(range(0, 10), io, ASCII))
{
    //Do stuff
}
```

#### Returns
[PIterator](#classshogun_1_1PRange_1_1PIterator) that represents the start of the range

#### `public inline `[`PIterator`](#classshogun_1_1PRange_1_1PIterator)` `[`end`](#classshogun_1_1PRange_1a8f22bb5b04f0e9351f23c205ce9ca609)`() const` {#classshogun_1_1PRange_1a8f22bb5b04f0e9351f23c205ce9ca609}

Create the iterator that corresponds to the end of the range. Used within the range-based loop version of the progress bar.

```cpp
for (auto i: progress(range(0, 10), io, ASCII))
{
    //Do stuff
}
```

#### Returns
[PIterator](#classshogun_1_1PRange_1_1PIterator) that represent the end of the range.

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_current_progress`](#classshogun_1_1PRange_1adca5330e0fa343586b94be938c06ca36)`() const` {#classshogun_1_1PRange_1adca5330e0fa343586b94be938c06ca36}

Return the current progress bar value. Used for testing purposes. 
#### Returns
current progress bar value.

#### `public inline void `[`print_progress`](#classshogun_1_1PRange_1a6e48dbe7de14d07c909f0d92302f19e8)`() const` {#classshogun_1_1PRange_1a6e48dbe7de14d07c909f0d92302f19e8}

Print the progress bar. This method must be called each time we want the progress bar to be updated. 
```cpp
auto pr = progress(range(0,10), ASCII);
for (int i=0; i<10; i++)
{
    // Do stuff
    pr.print_progress();
}
pr.complete();
```

#### `public inline void `[`print_absolute`](#classshogun_1_1PRange_1a4bb17ef2c53d38bb4997357bd7085ded)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` current_val,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` val,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` min_value,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` max_value) const` {#classshogun_1_1PRange_1a4bb17ef2c53d38bb4997357bd7085ded}

Print the absolute progress bar. This method must be called each time we want the progress bar to be updated.

#### Parameters
* `current_val` current value 

* `val` value 

* `min_val` minimum value 

* `max_val` maximum value

#### `public inline void `[`complete`](#classshogun_1_1PRange_1a5c23dc5dc0f68d251db743dbde10988c)`() const` {#classshogun_1_1PRange_1a5c23dc5dc0f68d251db743dbde10988c}

Print the progress bar end. This method must be called one time, after the loop. 
```cpp
auto pr = progress(range(0,10), ASCII);
for (int i=0; i<10; i++)
{
    // Do stuff
    pr.print_progress();
}
pr.complete();
```

#### `public inline void `[`complete_absolute`](#classshogun_1_1PRange_1a4d889a29f78e822c605f03240a57f3cc)`() const` {#classshogun_1_1PRange_1a4d889a29f78e822c605f03240a57f3cc}

Print the progress bar end. This method must be called one time, after the loop. 
```cpp
auto pr = progress(range(0,10), ASCII);
for (int i=0; i<10; i++)
{
    // Do stuff
    pr.print_absolute();
}
pr.complete_absolute();
```

