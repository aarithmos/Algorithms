---
layout: s-layout
permalink: /Johnson's-Algorithm/
---
<html>
<head>
  <link href="https://fonts.googleapis.com/css?family=Raleway" rel="stylesheet">
<style> 
h1.ab{
font-family: 'Raleway', sans-serif;
}
</style>
</head>
</html>

<h1><u>Johnson’s algorithm for shortest paths between all pairs of vertices in a Graph</u></h1>

If we apply [Dijkstra’s Single Source]() shortest path algorithm for every vertex, considering every vertex as source, we can find all pair shortest paths in O(V*VLogV) time. So using Dijkstra’s single source shortest path seems to be a better option than Floyd Warshell, but the problem with Dijkstra’s algorithm is, it doesn’t work for negative weight edge.<br>
<br>
<i>The idea of <b>Johnson’s algorithm</b> is to re-weight all edges and make them all positive, then apply Dijkstra’s algorithm for every vertex.</i>

### Algorithm:

```
JOHNSON(G)
 1  compute G′, where V[G′] = V[G] ∪ {s},
           E[G′] = E[G] ∪ {(s, v) : v ∈ V[G]}, and
           w(s, v) = 0 for all v ∈ V[G]
 2  if BELLMAN-FORD(G′, w, s) = FALSE
 3     then print "the input graph contains a negative-weight cycle"
 4     else for each vertex v ∈ V[G′]
 5              do set h(v) to the value of δ(s, v)
                           computed by the Bellman-Ford algorithm
 6          for each edge (u, v) ∈ E[G′]
 7              do 
 8          for each vertex u ∈ V[G]
 9              do run DIJKSTRA(G, , u) to compute  for all v ∈ V[G]
10                 for each vertex v ∈ V[G]
11                     do 
12          return D

```
__Time Complexity:__ The main steps in algorithm are [Bellman Ford Algorithm]() called once and [Dijkstra]() called V times. Time complexity of Bellman Ford is O(VE) and time complexity of Dijkstra is __O(VLogV)__. So overall time complexity is __O(V2log V + VE)__.

[BACK TO THE TOP](#top)                                           

 [![](/img/back.png)](/Our-Picks)
