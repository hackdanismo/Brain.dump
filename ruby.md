# Ruby

+ [Install Ruby](#install-ruby)
+ [Write the first Ruby script](#write-the-first-ruby-script)

## Install Ruby
`Ruby` can be installed on `macOS` using `Homebrew`. Once installed, the terminal can be used to display the version of `Ruby` installed:

```shell
$ brew install ruby

# Display the version of Ruby installed
$ ruby -v
```

## Write the first Ruby script
Once `Ruby` is installed, write the first script. `Ruby` files have the file extension of: `.rb`. Create a file named `hello.rb`:

```ruby
puts "Hello, World"

# Using print
print "Hello, World"
# Using p
p "Hello, World"
```

The `puts` keyword is shorthand for `"put string"` and is Ruby's built-in method for printing output to the console followed by a newline.

We can also use `print` and `p` as keywords.

+ `puts`: adds a newline at the end of the string (e.g. `Hello, World\n`).
+ `print`: prints the string without a newline (e.g. `Hello, World`).
+ `p`: prints the string without a newline but uses `inspect` to print with debug information (e.g. `Hello, World`).

Run it:

```shell
$ ruby hello.rb
```
