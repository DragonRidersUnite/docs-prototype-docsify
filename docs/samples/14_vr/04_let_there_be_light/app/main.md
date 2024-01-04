

  ```ruby
  # /14_vr/04_let_there_be_light/app/main.rb

  require 'app/tick.rb'

def tick args
  args.gtk.start_server! port: 9001, enable_in_prod: true
  tick_game args
end

  ```
  