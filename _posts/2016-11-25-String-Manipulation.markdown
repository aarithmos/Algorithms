---
layout: post
title:  "String Manipulation"
author: "Palindrome String Index of char length Character At position"
permalink: /String Manipulation/
---

* [Palindrome](#palindrome)


* [String Index of char](#index-of-character-in-string)


* [String length](#string-length)


* [Character At position](#character-position)


### Palindrome 

```
Palindrome character

Function Palindrome_char( char[] , n )      //char[] is character array & n is length of string
1. i = 0 
2. j = n-1
3. while( i < n/2 )
4.    if(c[i] != c[j] )
5.       return false
6.    i++
7.    j—
8.    end while
9. return true
10. end Palindrome_char

```

### Index of Character in String

```
String Index of char
1. Function Index_of( char[] , ch ) // ch is the character who’s index is needed
2. i = 0
3. pos = -1
4. while( char[i] != ‘/0’ )
5.    if( char[] == ch )
6.       pos = i
7.       break   // breaks out of the loop as the position is found
8.       end if 
9.    i++
10.    end while 
11. return  pos
12. end Index_of

```

### String Length

```
String length
1. Function String_length( char[] )
2. count = 0
3. while( char[count] != ‘/0’ )
4.    count++
5. return count+1
6. end String_length  

```

### Character Position

```
Character At position
1. Function Char_At( char[] , pos )          //character present at a particular index
2. if( pos < 0 || pos > n)
3.    print( “index is outside the array bounds” )
4. else
5.     return char[pos]
6. end Char_At 

```

[BACK TO THE TOP](#top)                                           

 [![](/img/back.png)](/search)
