---
layout: post
title:  "Backtracking Algorithms"
author: "N-Queen Problem Sum of subset "
permalink: /Backtracking Algorithms/
---


[N-Queen Problem](#n-queen-problem)


[Sum of subset Problem](#sum-of-subset-problem)

### N-Queen Problem

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

 [![](/img/back.png)](/search/)
