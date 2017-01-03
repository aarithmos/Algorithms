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

A palindrome String is a string which has same character position for each character of a string when compared with its reverse form , in other words when a palindrome string is reversed then it is identical to its parent string .
For instance :-  

‘NAMAN’ is a palindrome as its reverse is also ‘NAMAN’ whereas word ‘PROG’ is not a palindrome as its reverse is ‘GORP’ which is not same as its parent string

Complexity:-

Time complexity:  __O(n/2)__

Space complexity:  __O(1)__


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

A Function which takes String and character as input and returns the position of the character in the string and returns -1 if the character is not present in the string.

For instance :-

Input : String = ‘Rohan’ , Character = ‘h’

Output: 2

Note: Answer is not 3 and 2 because indexing in an array(String array in this case) 
begins from 0 & not 1

Complexity:-

Time complexity:  __O(n)__   where ‘n’ is the number of elements in the string 

Space complexity:  __O(1)__ 

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

A function which returns the number of characters present in the string (also popularly referred as length of string)

For instance :-

Input: String = ‘Algorithm’

Output : 9

Complexity:- O(n) where ‘n’ is the number of elements in the string

Time complexity: __O(n)__

Space complexity:  __O(1)__

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

A function which returns the character at a particular position and also determines if the position enquired for is within the boundary of the String of not (0<=pos<String_length).

For instance :-

Input : String = ‘Algorithm’ pos = 3

Output : ‘o’

Note : Indexing of a String character begins from 0

Complexity:-

Time complexity:  __O(1)__

Space complexity:  __O(1)__

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
