# 19CS301-Module11

### EX: 11 a Singly Linked List (Traversal, Search and Delete)

### Aim: 

Write a function to traverse the linked list and display it in the following format.

### Algorithm:

STEP 1: Start.

STEP 2: Create a node class and object of the node.

STEP 3: Create another class to use the node object.

STEP 4 : Using data traversing traverse from first to last data element.

STEP 5 : Print the data.

STEP 6 : Stop.

### Program:

```python
# Name: Nidhish B
# Reg.No: 212223050032

class Node:
   def __init__(self, data=None):
      self.data = data
      self.next = None

class SLinkedList:
   def __init__(self):
      self.head = None

   def listprint(self):
       cur = self.head 
       while cur:
           print(cur.data)
           cur = cur.next

list = SLinkedList()
list.head = Node("Mon")
e2 = Node("Tue")
e3 = Node("Wed")

list.head.next = e2

e2.next = e3

list.listprint()

```

### Output:

![image](https://github.com/user-attachments/assets/cdf05566-077d-409f-b5f6-1c85a237e560)

### Result:

Thus,the given program is implemented and executed successfully.
 


