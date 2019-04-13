# The Assignment Expression

## Learning Goals

* Define the _Assignment Expression_
* Define Mutability / Immutability
* Constant versus "Symbolic Constants" and "Values"
* Return Value of an _Assignment Expression_

## Introduction

So you've seen the first of our **essential three expressions**, the _constant
expression_ which gives Python some constant fact about the world: `2` is `2`.

It's really useful (we'll see why in a minute) to associate an _expression's_
_evaluated_ result (or, _return value_)  with a 'name'. We call those names
that we associate with the _expression's_ result, _variables_.

We use the second of our **essential three expressions** to do this: the
_assignment expression_.  Other programming books and guides call using the
assignment expression "assigning a variable."

In terms of conversation, learning the _assignment expression_ is what babies
are demonstrating when they perform the miracle of ***LEARNING TO TALK***.

Let's dig into this amazing mystery of existence.

## Define the _Assignment Expression_

In Python, the assignment expression is represented as the following:

```Python
lhs = rhs
```

We have a name, which we call `lhs` for "left-hand side."; an `=` sign which is
the _assignment operator_; and then an expression or a constant, which we call
`rhs` for "right-hand side."

Here's an example:

```Python
height_in_centimeters = 180
```

The left-hand side is a name. Often, programmers call it the "variable name."
The "LHS" **can never** be an expression. It is called a "bare word." Bare
words (also: "barewords") are not data like `180`, nor are they expressions
like `1 + 1`, nor are they words that are special to Python. They're words that
***we*** introduce. For Python, `height_in_centimeters` is a bare word. For a
human baby, `Ma-Ma` is a bare word.

These bare word names are made to "point" to the RHS. This operator is known as
the _assignment operator_. The _assignment operator_ should not be confused
with `=` which we know from daily life and arithmetic which means "is equal
to."

> **ASIDE**: Some programming language authors find "`=` means assignment" to
> be very confusing.  The Go programming language from Google uses `:=` to mean
> assignment as does the Pascal programming language.

The RHS should be an _expression_, even if it's our friend the lowly _constant
expression_. To associate this to learning to speak:

```text
ma-ma = <this person in front of me>
```

That's the basics of the assignment expression!

## Define Mutability / Immutability

A variable is said to be mutable. We can apply multiple assignment expressions
to it.

Many years ago I was:

```Python
height_in_centimeters = 50
```

But today I am:

```Python
height_in_centimeters = 180
```

We can try these out in the Python interpreter:

(animation)

In some programming languages, we might want to make a variable name permanent;
that is, we only want it to be assigned ONCE. In Python, **all variables are
mutable**. There is no way to prevent a variable from being changed without
some additional, complicated code.

Now, we _can_ imply that a variable should not be changed. One way we do this is
by writing the variable name in all caps:

```Python
SPEED_OF_LIGHT = 180000
```

If, after this you try to set `SPEED_OF_LIGHT` to something else, it will
still change:

```Python
SPEED_OF_LIGHT = 0
```

## Constant versus "Symbolic Constants" and "Values"

We need to clear up some vocabulary.

We've been calling `23` and `255` _constants_, because that's what the
definition of _expression_ called them. And this is absolutely true and
correct.

**But** programmers have come to say, "constant" is short for "symbolic
constant" &mdash; like we just learned. What _we_ have been calling _constants_
many programmers call "values" or "scalar values."

## Return Value of an _Assignment Expression_

It's interesting, but the return value of an _assignment expression_ is the
evaluated result of the RHS.

Let's do a table again:

|Expession|Action|Notes|
|---------|------|-----|
|`x = 2 * (y = 3 * 2)`| Evaluate innermost expression in `()`| PEMDAS rules|
|`y = 3 * 2`|Zoom in to evaluate expression `3 * 2` and assign to y||
|`y = 6`| Assignment expression taking a constant expression to assign| y now points to `6`|
|6|Return value of `y = 6`|Remember: Assignment expressions have a return value; insert in outer expression|
|x = 2 * 6 |Evaluate expression|PEMDAS rules|
|x = 12| A bare word and a constant| `x` now points to `12` |

That first line is a little bit tricky. You might be thinking "Hey, that's not
math!" You're right. This is evaluating expressions in Python, so things are a
bit more interesting.

> **FURTHER GROWTH**: When you learn the _variable lookup expression_ in two
> lessons, come back to this lesson and use the _variable lookup expression_ to
> see what's inside `x` and `y` after Python evaluates the expression:
`x = 2 * (y = 3 * 2)`.

## Conclusion

Think about a baby, sitting back. Before it stands a parent saying their name
over and over (...and over) again. They wave towards their body and say their
name again and again. What the parent is trying to do is teach the baby to
assign to the bare word "Mama" or "Papa" or "Dada" _to their face_.

While neither the baby or the (average) adult is aware of it, they're trying to
teach the baby the second of the _three essential expessions_: the assignment
expression.

With Python, it's much easier. We simply type a bare word, an `=` and an
expression.

Since we now how to get a constant for the purpose of assigning (_constant
expression_) and we know how to assign it (_assignment expression_) we have
only one more vital expression to learn of the _essential three_: the variable
lookup expression!
