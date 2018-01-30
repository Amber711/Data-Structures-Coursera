#Array#
###Definition
Contiguous area of memory consisting of equal-size elements indexed by contiguous integers.
    
###What's Special About Arrray?
    
Constant-time access: array_address + elem_size x (index - first_index)
###Multi-Dimensional Array
1. Row-major: Element changes most rapidly in row.
2. Column-major: Element changes mostly rapidly in column
    
###Times for common operations

|   |Add | Remove  |
|---|---|---|
| Beginning  | O(n)  | O(n)  | 
| End  | O(1)  |O(1)   |
|  Middle | O(n)   | O(n)   |

O(n): linear time