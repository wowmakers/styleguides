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
* Use literal array syntax for arrays of strings.

    ```ruby
    VALID_STATUSES = ['new', 'approved', 'rejected'] # bad
    VALID_STATUSES = %w(new approved rejected)       # good
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
