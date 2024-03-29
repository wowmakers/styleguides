## Ruby Style Guide

Borrowed heavily from the [Github Ruby Styleguide](github.com/styleguide/ruby).

### Basic formatting

* Use 2 space indentation (no hard tabs)
* No trailing whitespace
* Avoid exceeding 80 characters per line

### Strings

* Use single quotes, unless you need interpolation.

    ```ruby
    "foobar" # bad
    'foobar' # good
    ```

* When using string intepolation, don't use spaces before/after { and }.

    ```ruby
    "foo{ bar }" # bad
    "foo{bar}"   # good
    ```
* Use double quotes if the string contains single quotes.

    ```ruby
    'Don\'t use single quotes here' # bad
    "Don't use single quotes here"  # good
    ```

### Arrays and hashes

* Use Ruby 1.9 hash syntax.

    ```ruby
    numbers = { 'one' => 1, 'two' => 2, 'three' => 3 }     # bad
    numbers = { one: 1, two: 2, three: 3 }                 # good
    ```

* Use literal array syntax for arrays of strings.

    ```ruby
    STATES = ['new', 'approved', 'rejected'] # bad
    STATES = %w(new approved rejected)       # good
    ```

### Conditions

* Leave blank lines between if blocks.

    ```ruby
    # Bad
    if some_condition?
      do_something
    if some_other_condition?
      do_something_else
    
    # Good
    if some_condition?
      do_something
    
    if some_other_condition?
      do_something_else
    ```
* Use `unless condition?` instead of `if !condition?`.
* Never use unless-else conditions. Replace it with if-else.

    ```ruby
    # Bad
    unless success?
      puts 'failure'
    else
      puts 'success'
    end
    
    # Good
    if success?
      puts 'success'
    else
      puts 'failure'
    end
    ```

### Blocks

* Use `{ ... }` blocks instead of single line `do ... end` blocks.

    ```ruby
    # Bad
    manipulate! do |img|
      img.auto_orient!
    end

    # Good
    manipulate! { |img| img.auto_orient! }
    ```

### Methods

* Use parentheses around arguments in method definition.

    ```ruby
    def foo bar   # bad
    def foo(bar)  # good
    ```
* Don't use parentheses when there are no arguments.

    ```ruby
    def foo()   # bad
    def foo     # good
    ```

* Always use parentheses in method calls when there is a condition after it.

    ```ruby
    foo(bar) if baz?  # good
    foo bar if baz?   # bad
    ```
