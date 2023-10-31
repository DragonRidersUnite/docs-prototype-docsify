# $gtk.console

This object represents the DragonRuby Console and allows you to interact with the console through your code.


## set_command String

Takes the String parameter and places it on the console commandline but does not execute it.  The following will place `puts "Hello DragonRuby!"` on the commandline.

```ruby
  $gtk.console.set_command 'puts "Hello DragonRuby!"'
```

## eval_the_set_command

Forces the execution of whatever command is on the DragonRuby console commandline.  If there is nothing on the commandline, it will return nil.

```ruby
$gtk.console.eval_the_set_command
```

## set_command_extended
## set_command_silent
## set_command_with_history
## set_command_with_history_silent
## set_system_command
