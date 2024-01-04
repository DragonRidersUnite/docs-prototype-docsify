

  ```ruby
  # /10_advanced_debugging/03_unit_tests/input_emulation_tests.rb

  def test_keyboard args, assert
  args.inputs.keyboard.key_down.i = true
  assert.true! args.inputs.keyboard.truthy_keys.include?(:i)
end

  ```
  