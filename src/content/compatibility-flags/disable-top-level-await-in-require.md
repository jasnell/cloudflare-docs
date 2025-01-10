---
_build:
	publishResources: false
	render: never
	list: never

name: "Disable top-level await in require(...)"
sort_date: "2024-12-02"
enable_date: "2024-12-02"
enable_flag: "disable_top_level_await_in_require"
disable_flag: "enable_top_level_await_in_require"
---

Workers implements the ability to use the Node.js style `require(...)` method
to import modules in the worker bundle. Historically, this mechanism allowed
required modules to use top-level await. This, however, is not Node.js
compatible.

The `disable_top_level_await_in_require` compat flag will cause `require()`
to fail if the module uses a top-level await. This flag is default enabled
on or after compatibility date 2024-12-02.

To restore the original behavior allowing top-level await, use the
`enable_top_level_await_in_require` compatibility flag.
