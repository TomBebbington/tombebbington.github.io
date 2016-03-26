---
published: true
title: D1.4 - Matchings
layout: post
category: further-maths
tags: D1
summary: Matchings involve allocating each and every worker to a single task, based on their preference.
---

We use **matchings** when we want to allocate each of something to a single of something else. To represent these, we use **bipartite graphs**, which have vertices either on the left or the right where they can connect if they are on opposite sides but not if they are on the same side.

# Algorithm
1. From initial matching, find a value on the left that hasn't been matched and connect this to a vertex on the right.
2. If the right vertex isn't in the matching, add it to the matching and repeat step 1. If it is, then go on to step 3.
3. Add the new edge to the matching and remove the edge connecting this to the left from the matching. Repeat step 1 with the verex that you removed.
4. Continue until you have either a full matching or there is nothing more you can do.

# Formatting your answer
1. Write down the initial matching, as just each left vertex and the right vertex it is connected to.
2. Write down the matching as you run the algorithm, using the notation:
    - A dash '\`-\`' between edges you have **joined**.
    - A crossed-out dash '/-' between edged you have **disconnected**.
3. Write down the final matching, as just each left vertex and the right vertex it is connected to.

```
Initial matching:
    A - X
    B - Z

Matching:
    C - X -/- A - Y

Final match:
    A - Y
    B - Z
    C - X
```


