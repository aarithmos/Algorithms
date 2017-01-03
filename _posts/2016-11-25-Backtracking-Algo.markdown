---
layout: post
title:  "Backtracking Algorithms"
author: "N-Queen Problem Sum of subset "
permalink: /Backtracking Algorithms/
---


In backtracking algorithms you try to build a solution one step at a time. If at some step it become clear that the current path that you are on cannot lead to a solution you go back to the previous step (backtrack) and choose a different path. Basically once you exhaust all your options at a certain step you go back.

* [N-Queen Problem](#n-queen-problem)


* [Sum of subset Problem](#sum-of-subset-problem)

### N-Queen Problem

The eight queens puzzle is the problem of placing eight chess queens on an 8×8 chessboard so that no two queens threaten each other. Thus, a solution requires that no two queens share the same row, column, or diagonal.

```
Function N-queen ( row , num )        //num is the number of queens to be inserted at row
1. column = 1
2. while( column <= num )
3.    if( place(row , column ) )
4.       board[row] = column
5.       if( row == num )
6.          print board[1,num]
7.       else
8.          N_queen( row+1 , num)
9.       end if
10.    column++
11.    end while
12.  end N_queen

Function Place( row , column )
1. i = 1
2. while( i < row-1 ) 
3.    if( board[i] == column )
4.       return false
5.    else if( abs|board[i] - column| == abs| i - row |)
6.       return false
7.    end while 
8. return true
9. end Place   

```

### Sum of subset Problem

Is there a possible subset of the given set of elements whose sum is x? This problem is refered to as sum of subset problem.
For Instance:-

Array = {1,2,3,4,5}

Input: 7

Output: Yes 

__Note__: 3 possible subsets exists whose sum of all elements of set is 7

{1,2,4}

{3,4}

{2,5} 

Input: 20

Output: No (no possible combination exist of the given elements whos sum is 20) 


```
Function Sum_of_subset( array[] , size , sum)
1. if( sum == 0 )
2.    return true
3. if( size==0 && sum!=0 )
4.    return false
5. if( a[n-1] > sum )
6.    return Sum_of_subset( array[] , size-1 , sum )
7. return Sum_of_subset( array[] , size-1 , sum ) || Sum_of_subset( array[] , size-1 , sum-a[n-1] )
8. end Sum_of_subset 

```

[BACK TO THE TOP](#top)                                           

 [![](/img/back.png)](/search)
