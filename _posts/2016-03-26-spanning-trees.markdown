---
published: true
title: D1.3 - Spanning Tree Problems
layout: post
category: further-maths
tags: D1
summary: Spanning tree problems involve connecting vertices so there is a path between all the vertices.
---
**Minimum spanning trees** are the minimum way to connect each vertex in a graph so each vertex has a path to every other vertex. There are 2 algorithms for finding these: **Prim's** and **Kruskal's**. These both find the same minimum spanning tree, just in different orders.

# Kruskal's algorithm

In **Kruskal's**, the lowest edge in the whole network is added each time.

To find a minimum spanning tree for a network with \`n\` vertices:

1. Find the unused edge of the lowest value.
2. Add this edge into your tree.
3. If there are \`n - 1\` edges in your tree, stop. If not, go back to Step 1.

# Prim's algorithm

In **Prim's**, the lowest edge connected to the tree is added each time.

To find a minimum spanning tree for a network with \`n\` vertices:

1. From a start vertex, add the connected edge of the lowest value to start your tree. This will *always* be given in an exam question.
2. From any vertex contained in your tree, add the edge of the lowest value.
3. If there are \`n - 1\` edges in your tree, stop. If not, go back to Step 2.