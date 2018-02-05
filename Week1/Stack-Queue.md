# Stack LIFO

### Implementation
You can implement stack and queue with array and linked list

# Queue FIFO

### Operations

#### Enqueue(key): adds key to collection
#### Key Dequeue(): removes and returns first key
#### Boolean Empty(): are there any elements

### Implementation with Linked List with a tail pointer(so pushBack is cheap)
#### Enqueue: use List.PushBack
#### Dequeue: use List.TopFront and List.PopFront

### Implementation with Array ==> Circular Array to make Dequeue O(1)
 Pointer A point to the node that will be read.
 Pointer B point to the space that will be write.

### Problems

1. IsBalanced(str)
    Stack stack
    for char in str:
        if char in ['[', '(']:
            stack.push(char)
        else:
            if stack.Empty: return false
            top <- stack.pop()
            if(top == '[' and char != ']') or
            (top == '(' and char != ')'):
            return false
    return stack.Empty()

