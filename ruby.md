## Ruby Style Guide


### Basics

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
