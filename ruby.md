# Ruby

+ [Install Ruby](#install-ruby)
+ [Write the first Ruby script](#write-the-first-ruby-script)

## Install Ruby
`Ruby` can be installed on `macOS` using `Homebrew`. Once installed, the terminal can be used to display the version of `Ruby` installed:

```shell
$ brew install ruby

# Display the version of Ruby is installed
$ ruby -v
# Check which version of RubyGems are installed
$ gem -v
```

`RubyGems` is the package manager for `Ruby`. Libraries that are installed are called `gems`.

To install `Ruby on Rails` (`Rails`), the `Bundler` gem needs to be installed:

```shell
$ gem install bundler
# Check which version of the Bundler is installed
$ bundle -v
```

Once installed, install `Ruby on Rails`:

```shell
$ gem install rails
# Check which version of Rails is installed
$ rails -v
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
