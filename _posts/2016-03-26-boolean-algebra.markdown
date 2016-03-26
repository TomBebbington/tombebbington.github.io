---
published: true
title: 3.6.5 - Boolean Algebra
layout: post
tags: CS3.6
category: computing
summary: Boolean algebra lets us express operations on true / false numbers with a mathemetical syntax.
---

Boolean algebra is a way of expressing operations on true / false numbers with a mathematical syntax. The following are the laws of Boolean algebra:

## The Commutative law

This states that in an **AND** or **OR** operation, the operands can be swapped without affecting the result of the operation.

\`A + B = B + A\`

## The Associate law

This states that the order you group operands in for **OR** and **AND** operations doesn't matter, so long as the original order is preserved:

\`(A + B) + C = A + (B + C)\`

## The Distributive law

This states that in an **AND** operation, if one of the operands is an **OR** operation, it can be expanded by **OR**ing the results of **AND**ng the value outside the brackets and the ones inside:

\`A(B + C) = AB + AC\`

## The Identity law

This states that **OR** or **AND** operations on the same number yield that number.

\`A + A = A\`

\`A . A = A\`

## The Negation law

This states that double negatives cancel out:

\`\overline{\overline{A}} = A\`

## The Redundancy law

This states that in an **OR** operation, the second value is redundant if it is **OR**ed into the first value:

\`A + AB = A\`

\`A(A + B) = A\`

## De Morgan's laws

These state that in **AND** / **OR** expressions that are all negative, you can 'break the bar' by splitting it and changing the operation to **OR** / **AND**.
