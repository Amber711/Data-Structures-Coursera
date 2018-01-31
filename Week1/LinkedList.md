# Linked List

![definition](../imgs/linkedlist.png)

head is a variable of type "point to node". It stores the address of the head node.
so head.next will be 10, since head point to 7.
 ## List API
 
|   |   |
|---|---|
|PushFront(Key) | add to front |
|Key TopFront() | return front item  |
| PopFront() | remove front item |
| PushBack(Key)  | add to back |
| Key TopBack()  | return back item |
| PopBack() | remove back item |
| Boolean Find(Key) | is key in list? |
| EraseKey) | remove key from list |
| Boolean Empty() | empty list?|
| AddBefore(Node, Key)| add key before node|
| AddAfter(Node, Key) | add key after node|

#### PopFront()    
    if head == nil:
        ERROR: Empty list
    head = head.next
    if head == nil //when there is only one node in the linked list, and has been poped up.
        tail = nil
        
#### PushFront(key)            
    node = new Node();
    node.key = key;
    node.next = head;
    head = node;
    
    if tail = nil; //Empty list, so tail will point to what head point to.
       tail = head 
       
### PopBack()       O(n)
    if head == nil;
       ERRORP Empty list
    if head = tail; //only one node
        head <- tail <- nil;
    p = head;
    while(p.next.next != nil){
        p = p.next
    }
    p.next = nil;
    tail = p;
       
### PushBack(key)  //1. without a tail
    node = new Node();
    node.key = key;
    node.next = nil
    
    if tail == nil:  //Empty list
       head <- tail <- node
    
    tail.next = node
    tail = node
    
### AddAfter(node, key)
    node2 = new Node();
    node2.key = key;
    node2.next = node.next;
    node.next = node2
    if tail == node;  //Only one node;
    tail = node2

### AddBefore(node, key)    O(n) 
       node2 = new node();
       node2.key = key;
       
       if tail == nil:
          head <- tail <- node2
       if head == node
          node2.next = node
          head = node2
        
       while(p.next.key != node.key) {
            p = p.next
       }
       
       node2.next = node;
       p.next = node2
   
### Time Complexity
![LinkedList](../imgs/linkedlist-timeCom.png)
     