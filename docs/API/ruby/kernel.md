# Module Kernel

The Kernel module is included by class Object, so its methods are available in every Ruby object.  Kernel in the DragonRuby Runtime has patches for how `standard out` is handled and also contains a unit of time in games called a `tick`.

## tick_count

Returns the current `tick` of the game. This value is reset if you call `$gtk.reset`.

## global_tick_count

Returns the current `tick` of the application from the point it was started. This value is **never** reset.

