## Ruby Style Guide


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
