---
_build:
	publishResources: false
	render: never
	list: never

name: "Automatically set the Symbol.toStringTag for Workers API objects"
sort_date: "2024-09-26"
enable_date: "2024-09-26"
enable_flag: "set_tostring_tag"
disable_flag: "do_not_set_tostring_tag"
---

A change was made that set the Symbol.toStringTag on all Workers API objects
in order to fix several spec compliance bugs. Unfortunately it turns out
that was more breaking than expected. The `do_not_set_tostring_tag`  compat
flag restores the original behavior for compat dates before 2024-09-26
