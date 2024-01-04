

  ```ruby
  # /14_vr/05_draw_a_cube/app/main.rb

  require 'app/tick.rb'

def tick args
  args.gtk.start_server! port: 9001, enable_in_prod: true
  tick_game args
end

  ```
  