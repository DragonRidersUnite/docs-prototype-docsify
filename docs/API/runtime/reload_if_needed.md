# reload_if_needed

Given a file name, this function will queue the file for reload if it's been modified. An optional second parameter can be passed in to signify if the file should be forced loaded regardless of modified time (true means to force load, false means to load only if the file has been modified). This function should be used for development/debugging purposes only.

## Related Functions

[production?](production.md), [reload_history_pending](reload_history_pending.md), [reload_history](reload_history.md)
