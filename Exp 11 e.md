### EX: 11.d e.Doubly Linked List (Insertion at specific Node)

### Aim:

To Type a python function to insert elements after the specific node in doubly linked list.

### Algorithm:

 1. Create node with data, next, prev
 2. Insert front:
    - new_node.next = head
    - if head exists, head.prev = new_node
    - head = new_node
 3. Insert after node:
    - new_node.next = prev_node.next
    - prev_node.next = new_node
    - new_node.prev = prev_node
    - if new_node.next exists, new_node.next.prev = new_node
 4. Traverse and print nodes from head

### Program:

```python

# Name: Nidhish B
# Reg.No: 212223050032

class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None

class DoublyLinkedList:
    def __init__(self):
        self.head = None
    
    def insert_front(self, data):
        new_node = Node(data)
        new_node.next = self.head
        if self.head is not None:
            self.head.prev = new_node
        self.head = new_node
    
    def insert_after(self, prev_node, data):
        if prev_node is None:
            print("previous node cannot be null")
            return
        newnode=Node(data)
        newnode.next=prev_node.next
        prev_node.next=newnode
        newnode=prev_node
        if newnode.next:
            newnode.next.prev=newnode
        
            
    def display_list(self, node):
        while node:
            print(node.data, end="->")
            last = node
            node = node.next
            
d_linked_list = DoublyLinkedList()

d_linked_list.insert_front(7)
d_linked_list.insert_front(2)
d_linked_list.insert_front(1)
d_linked_list.insert_front(6)

d_linked_list.insert_after(d_linked_list.head, 11)

d_linked_list.insert_after(d_linked_list.head.next, 15)

d_linked_list.display_list(d_linked_list.head)

```
### Output:

![image](https://github.com/user-attachments/assets/826f6d53-0640-4766-92b5-0b5e0e51df61)


### Result:

Thus, the given program is implemented and executed successfully.
