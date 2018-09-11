---
classname: "shogun::linalg::ocl::Parameter"
type: "struct"
---

# struct `shogun::linalg::ocl::Parameter` {#structshogun_1_1linalg_1_1ocl_1_1Parameter}

Struct [Parameter](#structshogun_1_1linalg_1_1ocl_1_1Parameter) for wrapping up parameters to custom OpenCL operation strings. Supports string type, C-style string type and all basic types of parameters.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public std::function< std::string()> `[`to_string`](#structshogun_1_1linalg_1_1ocl_1_1Parameter_1a63dc2fe3f0a77a105d0dde59be6f2e64) | The method to_string which is initialized by the assignment operators based on the parameter value types. This method is invoked by the cast operator to std::string
`public std::string `[`m_name`](#structshogun_1_1linalg_1_1ocl_1_1Parameter_1adb41893ba19e889e56c559f25fc1a68a) | The name of the parameter
`public inline  `[`Parameter`](#structshogun_1_1linalg_1_1ocl_1_1Parameter_1a608b727ee99369a8e94a4744682cc964)`(const char * name)` | Constructor that initlializes the name of the parameter.
`public template<>`  <br/>`inline `[`Parameter`](#structshogun_1_1linalg_1_1ocl_1_1Parameter)` & `[`operator=`](#structshogun_1_1linalg_1_1ocl_1_1Parameter_1a9f69e730cf21e20c614ce149b7440fb4)`(const T & value)` | Template overloaded assignment operator for basic-types that initializes an internal to_string method which is invoked when the parameter is casted to std::string.
`public inline `[`Parameter`](#structshogun_1_1linalg_1_1ocl_1_1Parameter)` & `[`operator=`](#structshogun_1_1linalg_1_1ocl_1_1Parameter_1a9334e13701e525c1ae6f8a57baabd55d)`(const char * value)` | Overloaded assignment operator for C-style string-types that initializes an internal to_string method which is invoked when the parameter is casted to std::string.
`public inline `[`Parameter`](#structshogun_1_1linalg_1_1ocl_1_1Parameter)` & `[`operator=`](#structshogun_1_1linalg_1_1ocl_1_1Parameter_1a8af700a71da801e8954d283d9e06d89e)`(std::string value)` | Overloaded assignment operator for std::string that initializes an internal to_string method which is invoked when the parameter is casted to std::string.
`public inline  `[`operator std::string`](#structshogun_1_1linalg_1_1ocl_1_1Parameter_1a3888dcd59dd5acd1ca5b9bee4c2e252a)`() const` | Cast opetator to std::string

## Members

#### `public std::function< std::string()> `[`to_string`](#structshogun_1_1linalg_1_1ocl_1_1Parameter_1a63dc2fe3f0a77a105d0dde59be6f2e64) {#structshogun_1_1linalg_1_1ocl_1_1Parameter_1a63dc2fe3f0a77a105d0dde59be6f2e64}

The method to_string which is initialized by the assignment operators based on the parameter value types. This method is invoked by the cast operator to std::string

#### `public std::string `[`m_name`](#structshogun_1_1linalg_1_1ocl_1_1Parameter_1adb41893ba19e889e56c559f25fc1a68a) {#structshogun_1_1linalg_1_1ocl_1_1Parameter_1adb41893ba19e889e56c559f25fc1a68a}

The name of the parameter

#### `public inline  `[`Parameter`](#structshogun_1_1linalg_1_1ocl_1_1Parameter_1a608b727ee99369a8e94a4744682cc964)`(const char * name)` {#structshogun_1_1linalg_1_1ocl_1_1Parameter_1a608b727ee99369a8e94a4744682cc964}

Constructor that initlializes the name of the parameter.

#### Parameters
* `name` The name of the parameter.

#### `public template<>`  <br/>`inline `[`Parameter`](#structshogun_1_1linalg_1_1ocl_1_1Parameter)` & `[`operator=`](#structshogun_1_1linalg_1_1ocl_1_1Parameter_1a9f69e730cf21e20c614ce149b7440fb4)`(const T & value)` {#structshogun_1_1linalg_1_1ocl_1_1Parameter_1a9f69e730cf21e20c614ce149b7440fb4}

Template overloaded assignment operator for basic-types that initializes an internal to_string method which is invoked when the parameter is casted to std::string.

#### Parameters
* `value` The value of the parameter.

#### `public inline `[`Parameter`](#structshogun_1_1linalg_1_1ocl_1_1Parameter)` & `[`operator=`](#structshogun_1_1linalg_1_1ocl_1_1Parameter_1a9334e13701e525c1ae6f8a57baabd55d)`(const char * value)` {#structshogun_1_1linalg_1_1ocl_1_1Parameter_1a9334e13701e525c1ae6f8a57baabd55d}

Overloaded assignment operator for C-style string-types that initializes an internal to_string method which is invoked when the parameter is casted to std::string.

#### Parameters
* `value` The value of the parameter.

#### `public inline `[`Parameter`](#structshogun_1_1linalg_1_1ocl_1_1Parameter)` & `[`operator=`](#structshogun_1_1linalg_1_1ocl_1_1Parameter_1a8af700a71da801e8954d283d9e06d89e)`(std::string value)` {#structshogun_1_1linalg_1_1ocl_1_1Parameter_1a8af700a71da801e8954d283d9e06d89e}

Overloaded assignment operator for std::string that initializes an internal to_string method which is invoked when the parameter is casted to std::string.

#### Parameters
* `value` The value of the parameter.

#### `public inline  `[`operator std::string`](#structshogun_1_1linalg_1_1ocl_1_1Parameter_1a3888dcd59dd5acd1ca5b9bee4c2e252a)`() const` {#structshogun_1_1linalg_1_1ocl_1_1Parameter_1a3888dcd59dd5acd1ca5b9bee4c2e252a}

Cast opetator to std::string

