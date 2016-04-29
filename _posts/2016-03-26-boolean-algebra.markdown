---
published: true
code: 5
title: Boolean Algebra
layout: post
tags: CS3.6
category: computing
summary: Boolean algebra lets us express operations on true / false numbers with a mathemetical syntax.
---

Boolean algebra is a way of expressing operations on `true` / `false` booleans with a mathematical syntax. It can be simplified just like any other kind of mathematics, and this simplifies the underlying circuit, thus reducing how many components the circuit requires. This causes the ciruit to be:

+ Cheaper
+ More efficient
+ With less gates: more reliable.

# Truth tables

**Truth tables** are tables used to model each possible value of a boolean expression to calculate its possible values.

# Operations

## NOT

$$ \overline{A} $$

| A | NOT A |
|---|--------------|
| 0 | 1            |
| 1 | 0            |

## OR

$$ A + B $$

| A | B | A OR B |
|---|---|-------|
| 0 | 0 | 0     |
| 0 | 1 | 1     |
| 1 | 0 | 1     |
| 1 | 1 | 1     |

## NOR

$$ \overline{A + B} $$

| A | B | A OR B |
|---|---|-------|
| 0 | 0 | 1     |
| 0 | 1 | 0     |
| 1 | 0 | 0     |
| 1 | 1 | 0     |

## AND

$$ A . B $$

| A | B | A AND B |
|---|---|-------|
| 0 | 0 | 0     |
| 0 | 1 | 0     |
| 1 | 0 | 0     |
| 1 | 1 | 1     |

## NAND

$$ \overline{A . B} $$

| A | B | A NAND B |
|---|---|-------|
| 0 | 0 | 1     |
| 0 | 1 | 1     |
| 1 | 0 | 1     |
| 1 | 1 | 0     |


## XOR

$$ A \oplus B $$

| A | B | A XOR B |
|---|---|-------|
| 0 | 0 | 0     |
| 0 | 1 | 1     |
| 1 | 0 | 1     |
| 1 | 1 | 0     |


# Laws

## The Identity law

These are self-explanatory key laws.

$$ A + 0 = A $$

$$ A + A = A $$

$$ A + \overline{A} = 1 $$

$$ A \cdot 0 = 0 $$

$$ A \cdot 1 = 1 $$

$$ A \cdot A = A $$

$$ A \cdot \overline{A} = 0 $$

## The Absorption Law

$$ A + (A \cdot B) = A $$

$$ A \cdot (A + B) = A $$

## The Null Law

$$ A + 1 = 1 $$

## The Commutative law

This states that in an **AND** or **OR** operation, the operands can be swapped without affecting the result of the operation.

$$ A + B = B + A $$

## The Associative law

This states that the order you group operands in for **OR** and **AND** operations doesn't matter, so long as the original order is preserved:

$$ (A + B) + C = A + (B + C) $$

## The Distributive law

This states that in an **AND** operation, if one of the operands is an **OR** operation, it can be expanded by **OR**ing the results of **AND**ng the value outside the brackets and the ones inside:

$$ A \cdot (B + C) = A \cdot B + A \cdot C $$

## The Negation law

This states that double negatives cancel out:

$$ \overline{\overline{A}} = A $$

## The Redundancy law

This states that in an **OR** operation, the second value is redundant if it is **AND**ed into the first value:

$$ A + A \cdot B = A $$

$$ A \cdot (A + B) = A $$

## De Morgan's laws

These state that in **AND** / **OR** expressions that are all negative, you can 'break the bar' by splitting it and changing the operation to **OR** / **AND**:

$$\overline{A \cdot B} = \overline{A} + \overline{B}$$

$$\overline{A + B} = \overline{A} \cdot \overline{B}$$
