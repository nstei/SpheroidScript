# Basic Syntax

From this document you'll learn the basics of Spheroid Script. You can run the examples by creating 
a simple [Hello world](../examples/HelloWorld/README.md) app and replacing the code in the 
"Client.spheroid" file with the code from the examples.

Try it out!

If you have encountered any problems, please let us know by 
[submitting an issue](https://github.com/SpheroidUniverse/SpheroidScript/issues/new), 
we will make sure to help you find the solution.
See our [recommendations](issues.md) on how to submit an issue.

## Program entry point

An entry point of an application is the `main` function.

```
fun main() {
    println("Hello world!")
}
```

[TODO: скриншот с нижней панели с логами]

## Functions

Function that takes two parameters and returns a value:

```
fun sum(a, b) {
    return a + b
}

fun main() {
    print("sum of 4 and 7 is ")
    println(sum(4, 7))
}
```

Function returning no value:

```
fun printSum(a, b) {
    println("Sum of $a and $b is ${a + b}.")
}

fun main() {
    printSum(10, 20)
}
```

## Variables

Read-only local variables are defined using the keyword `val`. They can be assigned a value only once.

```
fun main() {
    val a = 1
    println("a = $a")
}
```

Variables that can be reassigned use the `var` keyword:

```
fun main() {
    var x = 5
    x = x + 1
    println("x = $x")
}
```

Top-level variables:

```
val a = "Foo"
var b = 0

fun incrementB() { 
    b += 1 
}

fun main() {
    println("a = $a; b = $b")
    incrementB()
    println("incrementB()")
    println("a = $a; b = $b")
}
```

## Comments

Spheroid Script supports single-line (or _end-of-line_) and multi-line (_block_) comments.

```
// This is an end-of-line comment

/* This is a block comment
   on multiple lines. */
```


## String templates

String literals may contain template expressions, i.e. pieces of code that are evaluated and whose results are concatenated into the string. A template expression starts with a dollar sign ($) and consists of either a simple name:

```
fun main() {
    val i = 10
    println("i = $i") // prints "i = 10"
}
```

or an arbitrary expression in curly braces:

```
fun main() {
    val s = "abc"
    println("$s.length is ${s.length}") // prints "abc.length is 3"
}
```

## Conditional expressions

```
fun maxOf(a, b) {
    if (a > b) {
        return a
    } else {
        return b
    }
}

fun main() {
    println("max of 0 and 42 is ${maxOf(0, 42)}")
}
```

`if` can also be used as an expression:

```
fun maxOf(a, b) {
    return if (a > b) a else b
}

fun main() {
    println("max of 0 and 42 is ${maxOf(0, 42)}")
}
```

## `for` loop

```
fun main() {
    val items = listOf("1st item", "2nd item", "3rd item")
    for (item in items) {
        println(item)
    }
}
```

## Ranges

Iterating over a range:

```
fun main() {
    for (x in 1..100) {
        print(x)
    }
}
```

## Collections

Iterating over a collection:

```
fun main() {
    val items = listOf("1st item", "2nd item", "3rd item")
    for (item in items) {
        println(item)
    }
}
```
