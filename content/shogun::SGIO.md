---
classname: "shogun::SGIO"
type: "class"
---

# class `shogun::SGIO` {#classshogun_1_1SGIO}

Class [SGIO](#classshogun_1_1SGIO), used to do input output operations throughout shogun.

[Any](#classshogun_1_1Any) debug or error or progress message is passed through the functions of this class to be in the end written to the screen. Note that messages don't have to be written to stdout or stderr, but can be redirected to a file.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public  `[`SGIO`](#classshogun_1_1SGIO_1a23d6be2bdff660559d8b04e172e55b7e)`()` | default constructor
`public  `[`SGIO`](#classshogun_1_1SGIO_1a5fc417982acdccc63439d46d75885fbf)`(const `[`SGIO`](#classshogun_1_1SGIO)` & orig)` | copy constructor
`public virtual  `[`~SGIO`](#classshogun_1_1SGIO_1ad05548e845b6795cfeb0766f510d183c)`()` | destructor
`public void `[`set_loglevel`](#classshogun_1_1SGIO_1ae60ea3b09ede583a595882fee796eef6)`(`[`EMessageType`](#namespaceshogun_1ad2ca0a3c84404274f8bfaa618869fdf9)` level)` | set loglevel
`public `[`EMessageType`](#namespaceshogun_1ad2ca0a3c84404274f8bfaa618869fdf9)` `[`get_loglevel`](#classshogun_1_1SGIO_1a4a9f37d731966e9e06d21f85997a7b83)`() const` | get loglevel
`public inline bool `[`loglevel_above`](#classshogun_1_1SGIO_1a79c41034139b19a6352ca0817165c4ee)`(`[`EMessageType`](#namespaceshogun_1ad2ca0a3c84404274f8bfaa618869fdf9)` type) const` | loglevel above
`public inline bool `[`get_show_progress`](#classshogun_1_1SGIO_1a49a976eb222f367687883c3f4e6d332c)`() const` | get show_progress
`public inline `[`EMessageLocation`](#namespaceshogun_1a3f1ebc445f249f73946c88739f9cecaf)` `[`get_location_info`](#classshogun_1_1SGIO_1a9b9441ab5c985f06d6e7a0490a0fbd53)`() const` | show location where printing occurs
`public inline bool `[`get_syntax_highlight`](#classshogun_1_1SGIO_1ad7309e7740d15aad403d3f2b45600286)`() const` | get syntax highlight
`public std::string `[`format`](#classshogun_1_1SGIO_1a63baba7a0bed404229180bda6fbcce6b)`(`[`EMessageType`](#namespaceshogun_1ad2ca0a3c84404274f8bfaa618869fdf9)` prio,const char * function,const char * file,int32_t line,const char * fmt,...) const` | format a message
`public template<>`  <br/>`void `[`message`](#classshogun_1_1SGIO_1acccdf68a00153d74800e3917b1cf8fe1)`(`[`EMessageType`](#namespaceshogun_1ad2ca0a3c84404274f8bfaa618869fdf9)` prio,Args &&... args) const` | format and print a message 
`public template<>`  <br/>`void `[`error`](#classshogun_1_1SGIO_1ae9f59ca666db039ca83d9cdfd139280b)`(`[`EMessageType`](#namespaceshogun_1ad2ca0a3c84404274f8bfaa618869fdf9)` prio,Args &&... args) const` | format and print a message, and then throw an exception 
`public void `[`print`](#classshogun_1_1SGIO_1a1adca398600c25faefec74c78f4e33cc)`(`[`EMessageType`](#namespaceshogun_1ad2ca0a3c84404274f8bfaa618869fdf9)` prio,const std::string & msg) const` | print a message with the print function decided by priority
`public void `[`done`](#classshogun_1_1SGIO_1ab650651e4cda2869f73100c6fd2c821a)`()` | print 'done' with priority INFO, but only if progress bar is enabled
`public inline void `[`not_implemented`](#classshogun_1_1SGIO_1ad87d5fb588746e2b1db85cb0f96d64c1)`(const char * function,const char * file,int32_t line) const` | print error message 'not implemented'
`public inline void `[`gpl_only`](#classshogun_1_1SGIO_1a415ddf52c5b4e7b821b9c8a14e898426)`(const char * function,const char * file,int32_t line) const` | print error message 'Only available with GPL parts.'
`public inline void `[`deprecated`](#classshogun_1_1SGIO_1a3da0e8c997c4d4a1fb84e7d161e31f93)`(const char * function,const char * file,int32_t line) const` | print warning message 'function deprecated'
`public void `[`buffered_message`](#classshogun_1_1SGIO_1a983c170dc338817b6722059060230c92)`(`[`EMessageType`](#namespaceshogun_1ad2ca0a3c84404274f8bfaa618869fdf9)` prio,const char * fmt,...) const` | print a buffered message
`public inline FILE * `[`get_target`](#classshogun_1_1SGIO_1a8ada04984ab591095fec0487dccbf08f)`() const` | get target
`public void `[`set_target`](#classshogun_1_1SGIO_1afe1055340162ba2f54182720cc4ca374)`(FILE * target)` | set target
`public inline void `[`set_target_to_stderr`](#classshogun_1_1SGIO_1aa0578e8c240ab6bbbc96985881235877)`()` | set target to stderr
`public inline void `[`set_target_to_stdout`](#classshogun_1_1SGIO_1a165e95b72849a1088b045d2e1a42e52e)`()` | set target to stdout
`public inline void `[`enable_progress`](#classshogun_1_1SGIO_1aa5617560c8e2708095f1b99132627d19)`()` | enable progress bar
`public inline void `[`disable_progress`](#classshogun_1_1SGIO_1a20b1769e56458e2e57a61b03c55df5c7)`()` | disable progress bar
`public inline void `[`set_location_info`](#classshogun_1_1SGIO_1aaf908d02218769186b03dafcf62aca7b)`(`[`EMessageLocation`](#namespaceshogun_1a3f1ebc445f249f73946c88739f9cecaf)` location)` | enable displaying of file and line when printing messages etc
`public inline void `[`enable_syntax_highlighting`](#classshogun_1_1SGIO_1aac409d70061f7e137a2f6fcfd1dbc71e)`()` | enable syntax highlighting
`public inline void `[`disable_syntax_highlighting`](#classshogun_1_1SGIO_1afe44e95f4e5982f14372045a0dd38a0a)`()` | disable syntax highlighting
`public int32_t `[`ref`](#classshogun_1_1SGIO_1ab8c24b912ee57d3f2c81ecccd083582a)`()` | increase reference counter
`public int32_t `[`ref_count`](#classshogun_1_1SGIO_1a7682f1bc33b51f8f0b9340c6f4df4237)`() const` | display reference counter
`public int32_t `[`unref`](#classshogun_1_1SGIO_1ad99bde1a142a1c07a963169123166e01)`()` | decrement reference counter and deallocate object if refcount is zero before or after decrementing it
`public inline const char * `[`get_name`](#classshogun_1_1SGIO_1aa37ab6a2f004bfa2c956115231072736)`()` | #### Returns
`protected FILE * `[`target`](#classshogun_1_1SGIO_1a64f36225f1f832409928275a0e7f947f) | target file
`protected bool `[`show_progress`](#classshogun_1_1SGIO_1ab66c7076b4bef3e236b8415b239dcbc0) | if progress bar shall be shown
`protected `[`EMessageLocation`](#namespaceshogun_1a3f1ebc445f249f73946c88739f9cecaf)` `[`location_info`](#classshogun_1_1SGIO_1a18b856ff8f1964efcf8c02ddf5618db6) | if each print function should append filename and linenumber of where the print occurs etc
`protected bool `[`syntax_highlight`](#classshogun_1_1SGIO_1a2809fd43237d869be614bd02c6367a48) | whether syntax highlighting is enabled
`protected `[`EMessageType`](#namespaceshogun_1ad2ca0a3c84404274f8bfaa618869fdf9)` `[`loglevel`](#classshogun_1_1SGIO_1a63a97c658e984dcd95219291d7af26aa) | log level
`protected const char * `[`get_msg_intro`](#classshogun_1_1SGIO_1a25aec05ef972ffeb541fed761c6408b5)`(`[`EMessageType`](#namespaceshogun_1ad2ca0a3c84404274f8bfaa618869fdf9)` prio) const` | get message intro

## Members

#### `public  `[`SGIO`](#classshogun_1_1SGIO_1a23d6be2bdff660559d8b04e172e55b7e)`()` {#classshogun_1_1SGIO_1a23d6be2bdff660559d8b04e172e55b7e}

default constructor

#### `public  `[`SGIO`](#classshogun_1_1SGIO_1a5fc417982acdccc63439d46d75885fbf)`(const `[`SGIO`](#classshogun_1_1SGIO)` & orig)` {#classshogun_1_1SGIO_1a5fc417982acdccc63439d46d75885fbf}

copy constructor

#### `public virtual  `[`~SGIO`](#classshogun_1_1SGIO_1ad05548e845b6795cfeb0766f510d183c)`()` {#classshogun_1_1SGIO_1ad05548e845b6795cfeb0766f510d183c}

destructor

#### `public void `[`set_loglevel`](#classshogun_1_1SGIO_1ae60ea3b09ede583a595882fee796eef6)`(`[`EMessageType`](#namespaceshogun_1ad2ca0a3c84404274f8bfaa618869fdf9)` level)` {#classshogun_1_1SGIO_1ae60ea3b09ede583a595882fee796eef6}

set loglevel

#### Parameters
* `level` level of log messages

#### `public `[`EMessageType`](#namespaceshogun_1ad2ca0a3c84404274f8bfaa618869fdf9)` `[`get_loglevel`](#classshogun_1_1SGIO_1a4a9f37d731966e9e06d21f85997a7b83)`() const` {#classshogun_1_1SGIO_1a4a9f37d731966e9e06d21f85997a7b83}

get loglevel

#### Returns
level of log messages

#### `public inline bool `[`loglevel_above`](#classshogun_1_1SGIO_1a79c41034139b19a6352ca0817165c4ee)`(`[`EMessageType`](#namespaceshogun_1ad2ca0a3c84404274f8bfaa618869fdf9)` type) const` {#classshogun_1_1SGIO_1a79c41034139b19a6352ca0817165c4ee}

loglevel above

#### Returns
whether loglevel is above specified level and thus the message should be printed

#### `public inline bool `[`get_show_progress`](#classshogun_1_1SGIO_1a49a976eb222f367687883c3f4e6d332c)`() const` {#classshogun_1_1SGIO_1a49a976eb222f367687883c3f4e6d332c}

get show_progress

#### Returns
if progress bar is shown

#### `public inline `[`EMessageLocation`](#namespaceshogun_1a3f1ebc445f249f73946c88739f9cecaf)` `[`get_location_info`](#classshogun_1_1SGIO_1a9b9441ab5c985f06d6e7a0490a0fbd53)`() const` {#classshogun_1_1SGIO_1a9b9441ab5c985f06d6e7a0490a0fbd53}

show location where printing occurs

#### `public inline bool `[`get_syntax_highlight`](#classshogun_1_1SGIO_1ad7309e7740d15aad403d3f2b45600286)`() const` {#classshogun_1_1SGIO_1ad7309e7740d15aad403d3f2b45600286}

get syntax highlight

#### Returns
if syntax highlighting is enabled

#### `public std::string `[`format`](#classshogun_1_1SGIO_1a63baba7a0bed404229180bda6fbcce6b)`(`[`EMessageType`](#namespaceshogun_1ad2ca0a3c84404274f8bfaa618869fdf9)` prio,const char * function,const char * file,int32_t line,const char * fmt,...) const` {#classshogun_1_1SGIO_1a63baba7a0bed404229180bda6fbcce6b}

format a message

optionally prefixed with file name and line number from (use -1 in line to disable this)

#### Parameters
* `prio` message priority 

* `function` the function name from where the message is called 

* `file` file name from where the message is called 

* `line` line number from where the message is called 

* `fmt` format string

#### `public template<>`  <br/>`void `[`message`](#classshogun_1_1SGIO_1acccdf68a00153d74800e3917b1cf8fe1)`(`[`EMessageType`](#namespaceshogun_1ad2ca0a3c84404274f8bfaa618869fdf9)` prio,Args &&... args) const` {#classshogun_1_1SGIO_1acccdf68a00153d74800e3917b1cf8fe1}

format and print a message 
#### Parameters
* `prio` message priority 

* `args` arguments for formatting message

#### `public template<>`  <br/>`void `[`error`](#classshogun_1_1SGIO_1ae9f59ca666db039ca83d9cdfd139280b)`(`[`EMessageType`](#namespaceshogun_1ad2ca0a3c84404274f8bfaa618869fdf9)` prio,Args &&... args) const` {#classshogun_1_1SGIO_1ae9f59ca666db039ca83d9cdfd139280b}

format and print a message, and then throw an exception 
#### Parameters
* `ExceptionType` type of the exception to throw 

#### Parameters
* `prio` message priority 

* `args` arguments for formatting message

#### `public void `[`print`](#classshogun_1_1SGIO_1a1adca398600c25faefec74c78f4e33cc)`(`[`EMessageType`](#namespaceshogun_1ad2ca0a3c84404274f8bfaa618869fdf9)` prio,const std::string & msg) const` {#classshogun_1_1SGIO_1a1adca398600c25faefec74c78f4e33cc}

print a message with the print function decided by priority

#### Parameters
* `prio` message priority 

* `msg` message

#### `public void `[`done`](#classshogun_1_1SGIO_1ab650651e4cda2869f73100c6fd2c821a)`()` {#classshogun_1_1SGIO_1ab650651e4cda2869f73100c6fd2c821a}

print 'done' with priority INFO, but only if progress bar is enabled

#### `public inline void `[`not_implemented`](#classshogun_1_1SGIO_1ad87d5fb588746e2b1db85cb0f96d64c1)`(const char * function,const char * file,int32_t line) const` {#classshogun_1_1SGIO_1ad87d5fb588746e2b1db85cb0f96d64c1}

print error message 'not implemented'

#### `public inline void `[`gpl_only`](#classshogun_1_1SGIO_1a415ddf52c5b4e7b821b9c8a14e898426)`(const char * function,const char * file,int32_t line) const` {#classshogun_1_1SGIO_1a415ddf52c5b4e7b821b9c8a14e898426}

print error message 'Only available with GPL parts.'

#### `public inline void `[`deprecated`](#classshogun_1_1SGIO_1a3da0e8c997c4d4a1fb84e7d161e31f93)`(const char * function,const char * file,int32_t line) const` {#classshogun_1_1SGIO_1a3da0e8c997c4d4a1fb84e7d161e31f93}

print warning message 'function deprecated'

#### `public void `[`buffered_message`](#classshogun_1_1SGIO_1a983c170dc338817b6722059060230c92)`(`[`EMessageType`](#namespaceshogun_1ad2ca0a3c84404274f8bfaa618869fdf9)` prio,const char * fmt,...) const` {#classshogun_1_1SGIO_1a983c170dc338817b6722059060230c92}

print a buffered message

#### Parameters
* `prio` message priority 

* `fmt` format string

#### `public inline FILE * `[`get_target`](#classshogun_1_1SGIO_1a8ada04984ab591095fec0487dccbf08f)`() const` {#classshogun_1_1SGIO_1a8ada04984ab591095fec0487dccbf08f}

get target

#### Returns
file descriptor for target

#### `public void `[`set_target`](#classshogun_1_1SGIO_1afe1055340162ba2f54182720cc4ca374)`(FILE * target)` {#classshogun_1_1SGIO_1afe1055340162ba2f54182720cc4ca374}

set target

#### Parameters
* `target` file descriptor for target

#### `public inline void `[`set_target_to_stderr`](#classshogun_1_1SGIO_1aa0578e8c240ab6bbbc96985881235877)`()` {#classshogun_1_1SGIO_1aa0578e8c240ab6bbbc96985881235877}

set target to stderr

#### `public inline void `[`set_target_to_stdout`](#classshogun_1_1SGIO_1a165e95b72849a1088b045d2e1a42e52e)`()` {#classshogun_1_1SGIO_1a165e95b72849a1088b045d2e1a42e52e}

set target to stdout

#### `public inline void `[`enable_progress`](#classshogun_1_1SGIO_1aa5617560c8e2708095f1b99132627d19)`()` {#classshogun_1_1SGIO_1aa5617560c8e2708095f1b99132627d19}

enable progress bar

#### `public inline void `[`disable_progress`](#classshogun_1_1SGIO_1a20b1769e56458e2e57a61b03c55df5c7)`()` {#classshogun_1_1SGIO_1a20b1769e56458e2e57a61b03c55df5c7}

disable progress bar

#### `public inline void `[`set_location_info`](#classshogun_1_1SGIO_1aaf908d02218769186b03dafcf62aca7b)`(`[`EMessageLocation`](#namespaceshogun_1a3f1ebc445f249f73946c88739f9cecaf)` location)` {#classshogun_1_1SGIO_1aaf908d02218769186b03dafcf62aca7b}

enable displaying of file and line when printing messages etc

#### Parameters
* `location` location info (none, function, ...)

#### `public inline void `[`enable_syntax_highlighting`](#classshogun_1_1SGIO_1aac409d70061f7e137a2f6fcfd1dbc71e)`()` {#classshogun_1_1SGIO_1aac409d70061f7e137a2f6fcfd1dbc71e}

enable syntax highlighting

#### `public inline void `[`disable_syntax_highlighting`](#classshogun_1_1SGIO_1afe44e95f4e5982f14372045a0dd38a0a)`()` {#classshogun_1_1SGIO_1afe44e95f4e5982f14372045a0dd38a0a}

disable syntax highlighting

#### `public int32_t `[`ref`](#classshogun_1_1SGIO_1ab8c24b912ee57d3f2c81ecccd083582a)`()` {#classshogun_1_1SGIO_1ab8c24b912ee57d3f2c81ecccd083582a}

increase reference counter

#### Returns
reference count

#### `public int32_t `[`ref_count`](#classshogun_1_1SGIO_1a7682f1bc33b51f8f0b9340c6f4df4237)`() const` {#classshogun_1_1SGIO_1a7682f1bc33b51f8f0b9340c6f4df4237}

display reference counter

#### Returns
reference count

#### `public int32_t `[`unref`](#classshogun_1_1SGIO_1ad99bde1a142a1c07a963169123166e01)`()` {#classshogun_1_1SGIO_1ad99bde1a142a1c07a963169123166e01}

decrement reference counter and deallocate object if refcount is zero before or after decrementing it

#### Returns
reference count

#### `public inline const char * `[`get_name`](#classshogun_1_1SGIO_1aa37ab6a2f004bfa2c956115231072736)`()` {#classshogun_1_1SGIO_1aa37ab6a2f004bfa2c956115231072736}

#### Returns
object name

#### `protected FILE * `[`target`](#classshogun_1_1SGIO_1a64f36225f1f832409928275a0e7f947f) {#classshogun_1_1SGIO_1a64f36225f1f832409928275a0e7f947f}

target file

#### `protected bool `[`show_progress`](#classshogun_1_1SGIO_1ab66c7076b4bef3e236b8415b239dcbc0) {#classshogun_1_1SGIO_1ab66c7076b4bef3e236b8415b239dcbc0}

if progress bar shall be shown

#### `protected `[`EMessageLocation`](#namespaceshogun_1a3f1ebc445f249f73946c88739f9cecaf)` `[`location_info`](#classshogun_1_1SGIO_1a18b856ff8f1964efcf8c02ddf5618db6) {#classshogun_1_1SGIO_1a18b856ff8f1964efcf8c02ddf5618db6}

if each print function should append filename and linenumber of where the print occurs etc

#### `protected bool `[`syntax_highlight`](#classshogun_1_1SGIO_1a2809fd43237d869be614bd02c6367a48) {#classshogun_1_1SGIO_1a2809fd43237d869be614bd02c6367a48}

whether syntax highlighting is enabled

#### `protected `[`EMessageType`](#namespaceshogun_1ad2ca0a3c84404274f8bfaa618869fdf9)` `[`loglevel`](#classshogun_1_1SGIO_1a63a97c658e984dcd95219291d7af26aa) {#classshogun_1_1SGIO_1a63a97c658e984dcd95219291d7af26aa}

log level

#### `protected const char * `[`get_msg_intro`](#classshogun_1_1SGIO_1a25aec05ef972ffeb541fed761c6408b5)`(`[`EMessageType`](#namespaceshogun_1ad2ca0a3c84404274f8bfaa618869fdf9)` prio) const` {#classshogun_1_1SGIO_1a25aec05ef972ffeb541fed761c6408b5}

get message intro

#### Parameters
* `prio` message priority 

#### Returns
message intro or NULL if message is not to be printed

