# Basic Syntax

From this document you'll learn the basics of how to create code 
in SpheroidScript programming language. You can run the examples by creating 
a simple [Hello world](../examples/HelloWorld/README.md) app and replacing the code in the 
"Client.spheroid" file with the code from the examples.

Try in out!

If you have encountered any problems, please let us know by 
[submitting an issue](https://github.com/SpheroidUniverse/SpheroidScript/issues/new), 
we will make sure to help you find the solution.
See our [recommendations](issues.md) on how to write an issue.

## Program entry point

An entry point of an application is the `main` function.

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
fun main() {
    println("Hello world!")
}
```

[TODO: скриншот с нижней панели с логами]

</div>

## Functions

Here is an example of a function that has two parameters and returns a value:

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
fun sum(a, b) {
    return a + b
}

fun main() {
    print("sum of 4 and 7 is ")
    println(sum(4, 7))
}
```

</div>

Function with an expression body and inferred return type:

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
fun sum(a, b) = a + b

fun main() {
    println("sum of 5 and 8 is ${sum(5, 8)}")
}
```

</div>

Function returning no meaningful value:

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
fun printSum(a, b) {
    println("Sum of $a and $b is ${a + b}.")
}

fun main() {
    printSum(10, 20)
}
```

</div>

## Variables

Read-only local variables are defined using the keyword `val`. They can be assigned a value only once.

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
fun main() {
    val a = 1
    println("a = $a")
}
```

</div>

Variables that can be reassigned use the `var` keyword:

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
fun main() {
    var x = 5 // `Int` type is inferred
    x += 1
    println("x = $x")
}
```

</div>

Top-level variables:

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
val PI = 3.14
var x = 0

fun incrementX() { 
    x += 1 
}

fun main() {
    println("x = $x; PI = $PI")
    incrementX()
    println("incrementX()")
    println("x = $x; PI = $PI")
}
```

</div>

## Comments

SpheroidScript supports single-line (or _end-of-line_) and multi-line (_block_) comments.

<div class="sample" markdown="1" theme="idea" data-highlight-only>

```
// This is an end-of-line comment

/* This is a block comment
   on multiple lines. */
```

</div>

## String templates

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
fun main() {
    var a = 1
    // simple name in template:
    val s1 = "a is $a" 
    
    a = 2
    // arbitrary expression in template:
    val s2 = "${s1.replace("is", "was")}, but now is $a"

    println(s2)
}
```

</div>

## Conditional expressions

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

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

</div>

`if` can also be used as an expression:

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
fun maxOf(a, b) = if (a > b) a else b

fun main() {
    println("max of 0 and 42 is ${maxOf(0, 42)}")
}
```

</div>

## `for` loop

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
fun main() {
    val items = listOf("1st item", "2nd item", "3rd item")
    for (item in items) {
        println(item)
    }
}
```

</div>

## Ranges

Checking if a number is within a range using `in` operator:

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
fun main() {
    val x = 10
    val y = 9
    if (x in 1..y+1) {
        println("fits in range")
    }
}
```

</div>


Iterating over a range:

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
fun main() {
    for (x in 1..100) {
        print(x)
    }
}
```

</div>

## Collections

Iterating over a collection:

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
fun main() {
    val items = listOf("1st item", "2nd item", "3rd item")
    for (item in items) {
        println(item)
    }
}
```

</div>