---
layout: page
permalink: /Pollard’s-Rho-Algorithm/
---
<html>
<head>
	  <link href="https://fonts.googleapis.com/css?family=Raleway" rel="stylesheet">
<style>
body{
font-family: 'Raleway', sans-serif;
}
table {
    width:100%;
}
table, th, td {
    border: 1px solid black;
    border-collapse: collapse;
}
th, td {
    padding: 5px;
    text-align: left;
}
table#t01 tr:nth-child(even) {
    background-color: #eee;
}
table#t01 tr:nth-child(odd) {
   background-color:#fff;
}
table#t01 th {
    background-color: black;
    color: white;
}
</style>
</head>
</html>
<h1><u>Pollard’s Rho Algorithm for Prime Factorization</u></h1>

This algorithm allows you to find prime factors for a composite number, particularly fast for large numbers with small prime factors.

The __Rho algorithm’s__ most remarkable success was the factorization of eighth Fermat number(__i.e 2<sup>2<sup>n</sup></sup>+1__): _115,792,089,237,316,195,423,570,985,008,687,907,853,
269,984,665,640,564,039,457,584,007,913,129,
639,937 (78 digits)_

__Example:__

```
Input: n = 10;
Output: 2 [OR 5]

Input: n = 187;
Output: 11 [OR 17]

```

### Algorithm

```

1.Start with random x and c. Take y equal to x and f(x) = x2 + c.
2.While a divisor isn’t obtained
    a.Update x to f(x) (modulo n) [Tortoise Move]
    b.Update y to f(f(y)) (modulo n) [Hare Move]
    c.Calculate GCD of |x-y| and n
    d.If GCD is not unity
       i)If GCD is n, repeat from step 2 with another set of x, y and c
       ii)Else GCD is our answer

```

### Illustration:

Let us suppose n = 187 and consider different cases for different random values.

1) An Example of random values such that algorithm finds result:<br>
y = x = 2 and c = 1, Hence, our f(x) = x2 + 1.

<table>
  <tr>
    <th>x<sub>i+1</sub> = f(x<sub>i</sub>)</th>
    <th>y<sub>i+1</sub> = f(f(y<sub>i</sub>))</th>
     <th>c</th>
     <th>d = GCD(|x-y|,n)</th>
  </tr>
  <tr>
    <td>5</td>
    <td>26</td>
    <td>1</td>
    <td>1</td>
  </tr>
  <tr>
 <td>26</td>
    <td>180</td>
    <td>1</td>
    <td>11</td>
  </tr>
</table>
<br>
2) An Example of random values such that algorithm __finds result faster__:<br>
y = x = 110 and ‘c’ = 183. Hence, our f(x) = x2 + 183.

<table>
  <tr>
    <th>x<sub>i+1</sub> = f(x<sub>i</sub>)</th>
    <th>y<sub>i+1</sub> = f(f(y<sub>i</sub>))</th>
     <th>c</th>
     <th>d = GCD(|x-y|,n)</th>
  </tr>
  <tr>
    <td>128</td>
    <td>111</td>
    <td>183</td>
    <td>17</td>
  </tr>
</table>
<br>

3) An Example of random values such that algorithm __doesn’t find result__:<br>
x = y = 147 and c = 67. Hence, our f(x) = x2 + 67.

<table>
  <tr>
    <th>x<sub>i+1</sub> = f(x<sub>i</sub>)</th>
    <th>y<sub>i+1</sub> = f(f(y<sub>i</sub>))</th>
     <th>c</th>
     <th>d = GCD(|x-y|,n)</th>
  </tr>
  <tr>
    <td>32</td>
    <td>156</td>
    <td>67</td>
    <td>1</td>
  </tr>
    <tr>
    <td>156</td>
    <td>114</td>
    <td>67</td>
    <td>1</td>
  </tr>
    <tr>
    <td>93</td>
    <td>48</td>
    <td>67</td>
    <td>1</td>
  </tr>
    <tr>
    <td>114</td>
    <td>114</td>
    <td>67</td>
    <td>187</td>
  </tr>
</table>
<br>

### Time Complexity Analysis:

The algorithm offers a trade-off between its running time and the probability that it finds a factor. A prime divisor can be achieved with a probability around __0.5, in O(√d) <= O(n1/4) iterations__. This is a heuristic claim, and rigorous analysis of the algorithm remains open.


[BACK TO THE TOP](#top)                                           

 [![](/img/back.png)](/Our-Picks)

 