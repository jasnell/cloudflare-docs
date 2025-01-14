---
_build:
  publishResources: false
  render: never
  list: never

name: "Populate process.env from environment variables"
sort_date: "2025-01-31"
enable_flag: "nodejs_compat_populate_process_env"
disable_flag: "nodejs_compat_do_not_populate_process_env"
---

When the `nodejs_compat_populate_process_env` compatibility flag is used in conjunction with
the `nodejs_compat` compatibility flag, all environment variables configured for the worker
are added a string values to the `process.env` global.

Refer to the [environment variables](/workers/configuration/environment-variables/) docuemntation
for more detail.
