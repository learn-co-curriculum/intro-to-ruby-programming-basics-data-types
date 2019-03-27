# Data Types

## Learning Goals

- Identify the six data types in Ruby

## Introduction

Just like the English language has different types of data or ways of representing
information––words, numbers, lists––Ruby has several different data types,
which are also known as classes. These six classes are built in and always
available for programmers to use.

In Ruby, we use data types to store information in our code. That information
could be a person's name, a specific number, maybe a list of numbers, etc. The
specific ways in which we can use and manipulate these data types will become
clearer as we build more Ruby applications, but it is useful to have a baseline
understanding of what these data types are.

## Identify the Six Data Types in Ruby

### Strings

#### What is a String?

A _string_ is a data type that represents textual data. In Ruby, a string is a
sequence of characters enclosed in double or single quotes.

For example:

```ruby
"hello"
```

`"hello"` is a string!

The above string is an instance of Ruby's String class. In other words, the
`"hello"` string is made based on the String template that is a part of Ruby.
This means that every string we make has certain behaviors or attributes, just
by virtue of it being a string.

#### Creating Strings

There are two ways to create a string. In fact, we've already created a string
just by typing `"hello"`.

Try it out by opening up IRB, and typing `"hello".class`. You should see a
return value of `=> String`.

> We can actually call `.class` on any object to find out what type of data,
> i.e. what class, it is.

**The Literal Constructor:** This is the method through which we created our
`"hello"` string.

**The Class Constructor:** You can also create a string with `String.new`. This
will create an empty string.

`String.new("hello")` on the other hand, will create this string: `"hello"`. For
the most part, you will create strings using the first method discussed
here––simply by enclosing whatever text you want in double or single quotes.

#### Operating on Strings

Because every string is an instance of, or is based on, Ruby's String class,
there are certain behaviors, or methods, available to us for operating on them.
You can learn more about the many String methods by reading the [Ruby
documentation on Strings][string]. For now, we'll just take a look at a few
examples.

```ruby
"hello".size
   => 5
"hello".upcase
   => "HELLO"
"hello".reverse
   => "olleh"
```

### Booleans

There are only two values of the Boolean data type: `true` and `false`. In Ruby,
however, there is no such thing as a Boolean class. Instead, every appearance,
or instance, of `true` and `false` in your program are instances of TrueClass
and FalseClass respectively.

#### Creating Booleans

Unlike strings, there is not a way to create a Boolean value, other than to
explicitly write `true` or `false`. Later, we will see that we can write lines
of code that _evaluate to_ or return `true` and `false`, but we won't worry
about that for now.

#### Operating on Booleans

We don't! They just... are.

### Numbers

In Ruby, there are two types of numbers, Integers and Floats.

**Integers** are whole numbers, like `7`.

**Floats** are decimal numbers, like `7.3`.

> In earlier versions of Ruby, Integers were split into two classes, Fixnum and
> Bignum, but these data types are deprecated as of Ruby 2.4

#### Creating Numbers

Once again, there is no special magic to creating numbers. Simply declare them
by typing then out like `9000123` or `2.42331`. Ruby will treat the number as
an Integer or Float accordingly.

#### Operating on Integers and Floats

There are a number of methods available to you for operating on or manipulating
integers. You can read more about [Integers][integer] and [Floats][float], but for
now, we'll just check out a few examples:

```ruby
# .floor will round a float down to the nearest integer
7.5.floor
  => 7
# .cail will round a float up to the nearest integer
7.5.ceil
  => 8

# .next will increment an integer by one
10.next
  => 11
```

### Symbols

A symbol is a representation of a piece of data. Symbols look like this
`:my_symbol`. If I make a symbol, `:my_symbol`, and then use that symbol later
on in my code, my program will refer to the same area of memory in both cases.
This is different from, for example, strings, which take up new areas of memory
every time they are used.

#### Creating Symbols

You write symbols by placing a `:` in front of the symbol name.

`:this_is_a_symbol`

The usefulness of symbols will become more apparent later on, so that's all on
symbols for now.

### Arrays

Arrays are collections of Ruby objects. You can store any type of data in an
array.

#### Creating Arrays

There are a number of ways to create an array. Just like with creating strings,
you can use the literal constructor or the class constructor.

##### The Array Literal Constructor

```ruby
[1, 3, 400, 7]
```

The above code snippet is an array of integers (Fixnums). Any set of comma
separated data enclosed in brackets is an array. So, by simply writing
something like the above, you can create an array.

##### The Array Class Constructor

```ruby
Array.new
# => []
```

You can also create an array using `Array.new`. Just typing `Array.new` will
create an empty array (`=> []`). We can also provide arguments to set the amount
of starting values and what those values are:

```ruby
Array.new(4, false)
# => [false, false, false, false]
```

#### Operating on Arrays

There are many ways to operate on arrays and on each individual item, or
element, within an array. Later on in the course, we'll learn about
iteration––the process of operating on each successive item in an array. For
now, we'll preview a few array methods, and you can check out more
[here][array].

```ruby
[5, 100, 234, 7, 2].sort

  => [2, 5, 7, 100, 234]

[1, 2, 3].reverse
  => [3, 2, 1]
```

### Hashes

Hashes also store objects in Ruby. However, they differ from arrays in that they
function like dictionaries, rather than a list. Instead of a simple comma
separated list, hashes are composed of key/value pairs. Each key points to a
specific value––just like a word and a definition in a regular dictionary.

Hashes look like this:

```ruby
{"i'm a key" => "i'm a value!", "key2" => "value2"}
```

The curly brackets wrapped around indicate that this is a hash. We see in this
hash contains two key/value pairs, separated by a comma.

Keys and values can be _any_ data type, but keys are commonly set as strings or
symbols.

#### Creating Hashes

Just like arrays, hashes can be created with literal constructors and class
constructors.

**The Literal Constructor:** You can create a hash by simply writing key/value
pairs enclosed in curly braces. If you, for instance, wanted to create a key
using the symbol `:name`, and give it a value, `"Frank"`, we could write that
like so:

```ruby
{:name => "Frank"}
# => {:name => "Frank"}
```

**The Class Constructor:** You can also use the `Hash.new` syntax, which would
create an empty hash, `{}`.

```ruby
Hash.new
# => {}
```

#### Operating on Hashes

There are many methods for operating on hashes and their individual key/value
pairs. We will learn much more about them later, but you can preview some
methods [here][hash].

## Conclusion

Strings, booleans, numbers, symbols, arrays, and hashes make up the core data
types of Ruby. When we're building complex Ruby programs, we will frequently
need to store bits of information for use later. It might be the result of a
calculation, a custom message, or a list of numbers. With these data types,
we can store and access data as needed.

## Resources

- [Intro to Data Types](https://www.youtube.com/embed/iaz3dojT9ew?rel=0&showinfo=0)
- [Strings][string]
- [Integers][integer]
- [Floats][float]
- [Arrays][array]
- [Hashes][hash]

[string]: https://ruby-doc.org/core-2.4.0/String.html
[integer]: http://ruby-doc.org/core-2.5.0/Integer.html
[float]: http://ruby-doc.org/core-2.5.0/Float.html
[array]: http://ruby-doc.org/core-2.5.0/Array.html
[hash]: http://ruby-doc.org/core-2.5.0/Hash.html

<p class='util--hide'>View <a href='https://learn.co/lessons/data-types-readme'>Ruby Data Types</a> on Learn.co and start learning to code for free.</p>
