# args.state

Store your game data inside of this state. Properties with arbitrary nesting is allowed and a backing Entity will be created on your behalf.

```ruby
def tick args
  args.state.player.x ||= 0
  args.state.player.y ||= 0
end
```
| Properties | Descriptions |
| --- | --- |
| entity_id | Entities automatically receive an entity_id of type Fixnum.|
| entity_type | Entities can have an entity_type which is represented as a Symbol.|
| created_at | Entities have created_at set to args.state.tick_count when they are created.|
| created_at_elapsed | Returns the elapsed number of ticks since creation. |
| global_created_at | Entities have global_created_at set to Kernel.global_tick_count when they are created.|
| global_created_at_elapsed | Returns the elapsed number of global ticks since creation. |
| tick_count | Returns the current tick of the game. args.state.tick_count is 0 when the game is first started or if the game is reset via $gtk.reset. |

## Methods

### as_hash

Entity cast to a Hash so you can update values as if you were updating a Hash.

### new_entity

Creates a new Entity with a type, and initial properties. An optional block can be passed to change the newly created entity:

```ruby
def tick args
  args.state.player ||= args.state.new_entity :player, x: 0, y: 0 do |e|
    e.max_hp = 100
    e.hp     = e.max_hp * rand
  end
end
```

## new_entity_strict

Creates a new Strict Entity. While Entities created via `args.state.new_entity` can have new properties added later on, Entities created using `args.state.new_entity_strict` must define all properties that are allowed during its initialization. Attempting to add new properties after initialization will result in an exception.


