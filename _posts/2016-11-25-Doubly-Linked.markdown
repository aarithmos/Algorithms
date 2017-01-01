---
layout: post
title:  "Doubly Linked List"
author: "Doubly Linked List "
permalink: /Doubly-Linked-List/
---


* [Addition after the node](#addition-after-the-node)

* [Add before the node](#add-before-the-node)

* [Add item at the beginning](#add-item-at-the-beginning)

* [Add item at the end](#add-item-at-the-end)

* [Deleting a node inbetween](#deleting-a-node-inbetween)

* [Deleting a node at the end](#deleting-a-node-at-the-end)

* [Deleting a node at the beginning](#deleting-a-node-at-the-beginning)


### Addition after the node

```
Function Doubly_Linked_list_add_After( START , data , item)   //item is the data of the node after which we need to insert
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
13. end Doubly_Linked_list_add_After

```

### Add before the node

```
Function Doubly_Linked_list_add_before( START , data , item) 
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
13. end Doubly_Linked_list_add_before

```

### Add item at the beginning

```
1. Function doubly_linear_linked_list_add_begin( START , data )
2. new_node = new node
3. new_node.data = data
4. new_node.prev = NULL
5. new_node.next = NULL
6. if( START == NULL )
7.    START = new_node
8. else
9.    new_node.next = START
10.    START.prev = new_node
11.    START = new_node
12.    end else
13.  end doubly_linear_linked_list_add_begin

```

### Add item at the end

```
Function Doubly_Linked_list_add_end( START , data)
1. new_node = new node
2. new_node.data = data
3. if( START == NULL )
4.    START = new_node
5. else
6.    ptr = START
7.    while( ptr.NEXT != NULL )
8.       ptr = ptr.NEXT
9.       end while
10.    ptr.NEXT = new_node
11.    new_node.PREV = ptr
12.    end else
13. end Doubly_Linked_list_add_end

```

### Deleting a node inbetween

```
Function Doubly_Linked_list_delete_between(START , item)
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
14. end Doubly_Linked_list_delete_end

```

### Deleting a node at the end

```
Function Doubly_Linked_list_delete_end(START)
1. if( START == NULL)
2.    print( “List is empty” )
3. else  
4.    ptr = START
5.    while(ptr.NEXT != NULL )
6.       ptr = ptr.NEXT 
7.    delete ptr
8.    end else  
9. end Doubly_Linked_list_delete_end

```

### Deleting a node at the beginning

```
Function Doubly_Linked_list_delete_begin(START)
1. if( START == NULL)
2.    print( “List is empty” )
3. else  
4.    temp = START
5.    START = START.NEXT
6.    delete temp
7.    end else  
8. end Doubly_Linked_list_delete_begin

```

[BACK TO THE TOP](#top)

[![](/img/back.png)](/Search)