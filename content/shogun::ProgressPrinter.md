---
classname: "shogun::ProgressPrinter"
type: "class"
---

# class `shogun::ProgressPrinter` {#classshogun_1_1ProgressPrinter}

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public inline  `[`ProgressPrinter`](#classshogun_1_1ProgressPrinter_1ae652216322b5e5d8c2516aa7d476f51b)`(const `[`SGIO`](#classshogun_1_1SGIO)` & io,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` max_value,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` min_value,const std::string & prefix,const `[`SG_PRG_MODE`](#namespaceshogun_1a2d152916e795a22fa2b10bbf840b09a6)` mode)` | Creates a [ProgressPrinter](#classshogun_1_1ProgressPrinter) instance. 
`public inline  `[`~ProgressPrinter`](#classshogun_1_1ProgressPrinter_1abb98c0bb76229677ffefefa68c70fb68)`()` | 
`public inline void `[`print_progress`](#classshogun_1_1ProgressPrinter_1a6e48dbe7de14d07c909f0d92302f19e8)`() const` | Increment and print the progress bar. Everything is locked to prevent race conditions or characters overlapping (especially within multi threaded environments).
`public inline void `[`print_progress_absolute`](#classshogun_1_1ProgressPrinter_1a31badb9234f6c720ac3c97a796b7cbe3)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` current_val,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` val,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` min_val,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` max_val)` | 
`public inline void `[`premature_end`](#classshogun_1_1ProgressPrinter_1a09e0611fecb041e784913e39499d0997)`()` | Manually increment to max size the current value to print a complete progress bar.
`public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_current_progress`](#classshogun_1_1ProgressPrinter_1adca5330e0fa343586b94be938c06ca36)`() const` | #### Returns

## Members

#### `public inline  `[`ProgressPrinter`](#classshogun_1_1ProgressPrinter_1ae652216322b5e5d8c2516aa7d476f51b)`(const `[`SGIO`](#classshogun_1_1SGIO)` & io,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` max_value,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` min_value,const std::string & prefix,const `[`SG_PRG_MODE`](#namespaceshogun_1a2d152916e795a22fa2b10bbf840b09a6)` mode)` {#classshogun_1_1ProgressPrinter_1ae652216322b5e5d8c2516aa7d476f51b}

Creates a [ProgressPrinter](#classshogun_1_1ProgressPrinter) instance. 
#### Parameters
* `io` [SGIO](#classshogun_1_1SGIO) object which will be used to print the progress bar. 

* `max_value` interval maximum value. 

* `min_value` interval minimum value. 

* `prefix` string which will be printed before the progress bar. 

* `mode` char mode (UTF8, ASCII etc.).

#### `public inline  `[`~ProgressPrinter`](#classshogun_1_1ProgressPrinter_1abb98c0bb76229677ffefefa68c70fb68)`()` {#classshogun_1_1ProgressPrinter_1abb98c0bb76229677ffefefa68c70fb68}

#### `public inline void `[`print_progress`](#classshogun_1_1ProgressPrinter_1a6e48dbe7de14d07c909f0d92302f19e8)`() const` {#classshogun_1_1ProgressPrinter_1a6e48dbe7de14d07c909f0d92302f19e8}

Increment and print the progress bar. Everything is locked to prevent race conditions or characters overlapping (especially within multi threaded environments).

#### `public inline void `[`print_progress_absolute`](#classshogun_1_1ProgressPrinter_1a31badb9234f6c720ac3c97a796b7cbe3)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` current_val,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` val,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` min_val,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` max_val)` {#classshogun_1_1ProgressPrinter_1a31badb9234f6c720ac3c97a796b7cbe3}

#### `public inline void `[`premature_end`](#classshogun_1_1ProgressPrinter_1a09e0611fecb041e784913e39499d0997)`()` {#classshogun_1_1ProgressPrinter_1a09e0611fecb041e784913e39499d0997}

Manually increment to max size the current value to print a complete progress bar.

#### `public inline `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_current_progress`](#classshogun_1_1ProgressPrinter_1adca5330e0fa343586b94be938c06ca36)`() const` {#classshogun_1_1ProgressPrinter_1adca5330e0fa343586b94be938c06ca36}

#### Returns
last progress as a percentage.

