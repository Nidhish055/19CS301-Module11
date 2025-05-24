### EX: 11.d Doubly Linked List (Insertion and all operation)

### Aim:

To Type a python function to insert elements at the beginning of the doubly linked list.

### Algorithm:

STEP 1: Start.

STEP 2: Create a node class and object of the node.

STEP 3: Create another class to use the node object.

STEP 4: The new node is always added before the head of the given Linked List. And newly added node becomes the new head of the Linked List.

STEP 5: Print the data.

STEP 6: Stop.

### Program:

```python

# Name: Nidhish B
# Reg.No: 212223050032

class Node:
    def __init__(self, data):
        self.item = data
        self.nref = None
        self.pref = None

class DoublyLinkedList:
    def __init__(self):
        self.start_node = None

    def insert_in_emptylist(self, data):
        if self.start_node is None:
            new_node = Node(data)
            self.start_node = new_node
        else:
            print("list is not empty")
            
    def insert_at_start(self, data):
    
        n=Node(data)
        temp=self.start_node
        temp.pref = n
        n.nref=temp
        self.start_node = n
        
        
    def traverse_list(self):
        if self.start_node is None:
            print("List has no element")
            return
        else:
            n = self.start_node
            while n is not None:
                print(n.item , " ")
                n = n.nref
                
new_linked_list = DoublyLinkedList()
new_linked_list.insert_in_emptylist(40)
new_linked_list.insert_at_start(30)
new_linked_list.insert_at_start(20)
new_linked_list.insert_at_start(10)
new_linked_list.traverse_list()

```
### Output:

![image](https://github.com/user-attachments/assets/5bb48327-69de-440c-8a1a-2602a302e779)

### Result:

Thus, the given program is implemented and executed successfully.
