---
layout: post
title:  "Circular Linked List"
author: "Circular Linked List "
permalink: /Circular-Linked-List/
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
Function Circular_Linked_list_add_After( START , data , item)   //item is the data of the node after which we need to insert
1. new_node = new node
2. new_node.data = data
3. ptr = START
4. preptr = START
5. while(preptr.data != item)
6.    preptr = ptr
7.    ptr = ptr.NEXT
8.    end while
9. preptr.NEXT = new_node
10. new_node.NEXT = ptr 
11. end Circular_Linked_list_add_After

```

### Add before the node

```
Function Circular_Linked_list_add_before( START , data , item) 
1. new_node = new node
2. new_node.data = data
3. ptr = START
4. preptr = START
5. while(ptr.data != item)
6.    preptr = ptr
7.    ptr = ptr.NEXT
8.    end while
9. preptr.NEXT = new_node
10. new_node.NEXT = ptr 
11. end Circular_Linked_list_add_before

```

### Add item at the beginning

```
1. Function circular_linked_list_add_begin( START , data )
2. new_node = new node
3. new_node.data = data
4. new_node.next = NULL
5. if( START == NULL )
6.    START = new_node
7. else
8.    new_node.next = START
9.    ptr = START
10.    while( ptr.next != START )
11.       ptr = ptr.next
12.       end while
13.    ptr.next = new_node  
14.    START = new_node
15.    end else
16.  end circular_linked_list_add_begin

```

### Add item at the end

```
Function Circular_Linked_list_add_end( START , data)
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
11.    new_node.NEXT = START
11.    end else
12. end Circular_Linked_list_add_end

```

### Deleting a node inbetween

```
Function Circular_Linked_list_delete_between(START , item)
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
11.    delete ptr
12.    end else  
13. end Circular_Linked_list_delete_end

```

### Deleting a node at the end

```
Function Circular_Linked_list_delete_end(START)
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
11.   delete ptr
12.   end else  
13. end Circular_Linked_list_delete_end

```

### Deleting a node at the beginning

```
Function Cirucular_Linked_list_delete_begin(START)
1. if( START == NULL)
2.    print( “List is empty” )
3. else  
4.    temp = START
5.    ptr = START
6.    while( ptr.NEXT != START )
7.       ptr = ptr.NEXT
8.       end while
9.    ptr.NEXT = START.NEXT   
10.   START = START.NEXT
11.   delete temp
12.   end else  
13. end Circular_Linked_list_delete_begin

```


[BACK TO THE TOP](#top)

[![](/img/back.png)](/Search)