---
layout: post
title:  "Circular Doubly Linked List"
author: "Circular Doubly Linked List "
permalink: /Circular-Doubly-Linked-List/
---

A linked list is a linear collection of data elements called nodes(data and address) each pointing to the next node by means of a pointer(variable which contains the address of next node). It is a data structure consisting of a group of nodes which together represent a sequence.A Circular Doubly linked list has a previous pointer in the node in addition with the features of single linked list. This previous node pointes to node preceding the current node.Moreover the next pointer of the last node of the list points to the first node of the list and the previous pointer(pointer that has the address of previous element) of the first element points to the last element.


* [Addition after the node](#addition-after-the-node)

* [Add before the node](#add-before-the-node)

* [Add item at the beginning](#add-item-at-the-beginning)

* [Add item at the end](#add-item-at-the-end)

* [Deleting a node in between](#deleting-a-node-in-between)

* [Deleting a node at the end](#deleting-a-node-at-the-end)

* [Deleting a node at the beginning](#deleting-a-node-at-the-beginning)


### Addition after the node

Time complexity: __O(n)__

Space complexity: __O(1)__

```
Function Circular_Doubly_Linked_list_add_After( START , data , item)   //item is the data of the node after which we need to insert
1. new_node = new node
2. new_node.data = data
3. ptr = START
4. preptr = START
5. while(preptr.data != item)
6.    preptr = ptr
7.    ptr = ptr.NEXT
8.    end while
9. preptr.NEXT = new_node
10. new_node.prev = preptr
11. new_node.NEXT = ptr 
12. ptr.prev = new_node
13. end Circular_Doubly_Linked_list_add_After

```

### Add before the node

Time complexity: __O(n)__

Space complexity: __O(1)__

```
Function Circular_Doubly_Linked_list_add_before( START , data , item) 
1. new_node = new node
2. new_node.data = data
3. ptr = START
4. preptr = START
5. while(ptr.data != item)
6.    preptr = ptr
7.    ptr = ptr.NEXT
8.    end while
9. preptr.NEXT = new_node
10. new_node.PREV = preptr
11. new_node.NEXT = ptr 
12. ptr.PREV = new_node
13. end Circular_Doubly_Linked_list_add_before


```

### Add item at the beginning

Time complexity: __O(1)__

Space complexity: __O(1)__

```
1. Function doubly_circular_linked_list_add_begin( START , data )
2. new_node = new node
3. new_node.data = data
4. new_node.prev = NULL
5. new_node.next = NULL
6. if( START == NULL )
7.    START = new_node
8. else
9.    new_node.next = START
10.    new_node.prev = START.prev
11.    START.prev.next = new_node 
12.    START.prev = new_node
13.    START = new_node
14.    end else
15.  end doubly_circular_linked_list_add_begin

```

### Add item at the end

Time complexity: __O(n)__

Space complexity: __O(1)__

```
Function Doubly_Circular_Linked_list_add_end( START , data)
1. new_node = new node
2. new_node.data = data
3. if( START == NULL )
4.    START = new_node
5. else
6.    ptr = START
7.    while( ptr.NEXT != START )
8.       ptr = ptr.NEXT
9.       end while
10.    ptr.NEXT = new_node
11.    new_node.PREV = ptr
12.    new_node.NEXT = START
13.    START.prev = new_node
14.    end else
15. end Doubly_Circular_Linked_list_add_end

```

### Deleting a node in between

Time complexity: __O(n)__

Space complexity: __O(1)__

```
Function Circular_Doubly_Linked_list_delete_between(START , item)
1. if( START == NULL)
2.    print( “List is empty” )
3. else  
4.    ptr = START
5.    preptr = START
6.    while(ptr.data != item )
7.       preptr = ptr
8.       ptr = ptr.NEXT 
9.       end while
10.     preptr.NEXT = ptr.NEXT
11.     ptr.NEXT.PREV = preptr
12.    delete ptr
13.    end else  
14. end Circular_Doubly_Linked_list_delete_end

```

### Deleting a node at the end

Time complexity: __O(n)__

Space complexity: __O(1)__

```
Function Doubly_Circular_Linked_list_delete_end(START)
1. if( START == NULL)
2.    print( “List is empty” )
3. else  
4.    ptr = START
5.    preptr = START
6.    while(ptr.NEXT != START )
7.       preptr = ptr
8.       ptr = ptr.NEXT
9.       end while
10.   preptr.NEXT = START
11.   START.PREV = preptr  
12.   delete ptr
13.   end else  
14. end Doubly_Circular_Linked_list_delete_end

```

### Deleting a node at the beginning

Time complexity: __O(1)__

Space complexity: __O(1)__

```
Function Doubly_Cirucular_Linked_list_delete_begin(START)
1. if( START == NULL)
2.    print( “List is empty” )
3. else  
4.    temp = START
5.    ptr = START
6.    while( ptr.NEXT != START )
7.       ptr = ptr.NEXT
8.       end while
9.     ptr.NEXT = START.NEXT
10.   START.NEXT.PREV = ptr 
11.   START = START.NEXT
12.   delete temp
13.   end else  
14. end Doubly_Circular_Linked_list_delete_begin

```

[BACK TO THE TOP](#top)

[![](/img/back.png)](/Search)
