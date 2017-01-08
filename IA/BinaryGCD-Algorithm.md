---
layout: page
permalink: /BinaryGCD-Algorithm/
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

<h1><u>Binary GCD</u></h1>

This algorithm allows you to compute the [greatest common divisor](#bottom) of two integers u and v expressed in binary. 

### Algorithm:

```
1.g = 1
2.while u is even and v is even
      u = u/2 (right shift)
      v = v/2
      g = 2*g (left shift)
  now u or v (or both) are odd
3.while u > 0
     if u is even, u = u/2
     else if v is even, v = v/2
     else
       t = |u-v|/2
       if u < v, then v = t else u = t
4.return v*g

```
__Time Complexity:__  O((log<sub>2</sub>uv)<sup>2</sup>) 


<a id="bottom"></a>
__NOTE__:
```
Greatest common divisor (gcd) of two or more integers, when at least one of them is not zero, 
is the largest positive integer that divides the numbers without a remainder. 

For example, the GCD of 8 and 12 is 4.

```                                         

 [![](/img/back.png)](/Our-Picks)
