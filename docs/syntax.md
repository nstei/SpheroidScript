# Basic Syntax

В этом документе мы научим вас писать скрипты на языке программирования Spheroid sCript.
Тут будут вставки кода, вы их можете запускать 
(дать инструкцию как запускать -- ссылка на Tutorial "Hello World").
Пробуйте! 
Если будут проблемы -- пиши в issues 
(ссылка на инстуркцию и рекомендации как писать issue)


## Program entry point

An entry point of a Kotlin application is the `main` function.

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
fun main() {
    println("Hello world!")
}
```

</div>

## Functions

Function having two `Int` parameters with `Int` return type:

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
//sampleStart
fun sum(a: Int, b: Int): Int {
    return a + b
}
//sampleEnd

fun main() {
    print("sum of 3 and 5 is ")
    println(sum(3, 5))
}
```

</div>

Function with an expression body and inferred return type:

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
//sampleStart
fun sum(a: Int, b: Int) = a + b
//sampleEnd

fun main() {
    println("sum of 19 and 23 is ${sum(19, 23)}")
}
```

</div>

Function returning no meaningful value:

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
//sampleStart
fun printSum(a: Int, b: Int): Unit {
    println("sum of $a and $b is ${a + b}")
}
//sampleEnd

fun main() {
    printSum(-1, 8)
}
```

</div>

`Unit` return type can be omitted:

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
//sampleStart
fun printSum(a: Int, b: Int) {
    println("sum of $a and $b is ${a + b}")
}
//sampleEnd

fun main() {
    printSum(-1, 8)
}
```

</div>

{:#defining-variables}

## Variables

Read-only local variables are defined using the keyword `val`. They can be assigned a value only once.

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
fun main() {
//sampleStart
    val a: Int = 1  // immediate assignment
    val b = 2   // `Int` type is inferred
    val c: Int  // Type required when no initializer is provided
    c = 3       // deferred assignment
//sampleEnd
    println("a = $a, b = $b, c = $c")
}
```

</div>

Variables that can be reassigned use the `var` keyword:

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
fun main() {
//sampleStart
    var x = 5 // `Int` type is inferred
    x += 1
//sampleEnd
    println("x = $x")
}
```

</div>

Top-level variables:

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
//sampleStart
val PI = 3.14
var x = 0

fun incrementX() { 
    x += 1 
}
//sampleEnd

fun main() {
    println("x = $x; PI = $PI")
    incrementX()
    println("incrementX()")
    println("x = $x; PI = $PI")
}
```

</div>


## Comments

Just like most modern languages, Kotlin supports single-line (or _end-of-line_) and multi-line (_block_) comments.

<div class="sample" markdown="1" theme="idea" data-highlight-only>

```
// This is an end-of-line comment

/* This is a block comment
   on multiple lines. */
```

</div>

Block comments in Kotlin can be nested.

<div class="sample" markdown="1" theme="idea" data-highlight-only>

```
/* The comment starts here
/* contains a nested comment */     
and ends here. */
```

</div>

See [Documenting Kotlin Code](kotlin-doc.html) for information on the documentation comment syntax.

{:#using-string-templates}

## String templates

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
fun main() {
//sampleStart
    var a = 1
    // simple name in template:
    val s1 = "a is $a" 
    
    a = 2
    // arbitrary expression in template:
    val s2 = "${s1.replace("is", "was")}, but now is $a"
//sampleEnd
    println(s2)
}
```

</div>

See [String templates](basic-types.html#string-templates) for details.

{:#using-conditional-expressions}

## Conditional expressions

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
//sampleStart
fun maxOf(a: Int, b: Int): Int {
    if (a > b) {
        return a
    } else {
        return b
    }
}
//sampleEnd

fun main() {
    println("max of 0 and 42 is ${maxOf(0, 42)}")
}
```

</div>


In Kotlin, *if*{: .keyword } can also be used as an expression:

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
//sampleStart
fun maxOf(a: Int, b: Int) = if (a > b) a else b
//sampleEnd

fun main() {
    println("max of 0 and 42 is ${maxOf(0, 42)}")
}
```

</div>

See [*if*{: .keyword }-expressions](control-flow.html#if-expression).

{:#using-a-for-loop}

## `for` loop

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
fun main() {
//sampleStart
    val items = listOf("apple", "banana", "kiwifruit")
    for (item in items) {
        println(item)
    }
//sampleEnd
}
```

</div>

{:#using-ranges}

## Ranges

Check if a number is within a range using *in*{: .keyword } operator:

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
fun main() {
//sampleStart
    val x = 10
    val y = 9
    if (x in 1..y+1) {
        println("fits in range")
    }
//sampleEnd
}
```

</div>


Iterating over a range:

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
fun main() {
//sampleStart
    for (x in 1..5) {
        print(x)
    }
//sampleEnd
}
```

</div>

{:#using-collections}

## Collections

Iterating over a collection:

<div class="sample" markdown="1" theme="idea" data-min-compiler-version="1.3">

```
fun main() {
    val items = listOf("apple", "banana", "kiwifruit")
//sampleStart
    for (item in items) {
        println(item)
    }
//sampleEnd
}
```

</div>