---
  layout: post
  title: Exploring Linked Lists:A Beginner's Guide
  subtitle: All you need to know to get started with Linked lists.
  categories: Programming, Data Structures, Algorithms
  tags: [Linked Lists, Singly Linked Lists, Doubly Linked Lists, Circular Linked Lists]
  author: Krishna Sharma S
  banner:
      image: assets/images/banners/linked-list.png
      heading_style: "font-size: 4.25em; font-weight: bold; text-decoration: underline"
      subheading_style: "color: gold"
---
# Intoduction
A linked list is a daaata structure where the elements (nodes) are stoerd in non contiguous memory locations and are linked using pointers.
A node in a linked list typically consists of two components:
* Data: It holds the actual value or data associated with the node.
* Next Pointer: It stores the memory address (reference) of the next node in the sequence.
The first node in a linked list is the head node. The last node in the list points to NULL or nullptr, indicating the end of the list. This node is known as the tail node.
Linked lists can be singly linked, doubly linked and there are also circular linked lists.

# Singly Linked Lists
Singly linked lists are the simplest among the three mentioned above. It has a simple structure where each node consists of the data and next pointer. The head node is the beginning of the list and the tail points to the null pointer indicating the end of the list. It is notable that you can only traverse from the head to the tail, not the other way around.

### Python Code
```
class Node:
  def __init__(self, data):
    self.data = data
    self.next = None
 
class SinglyLinkedList:
  def __init__(self):
    self.head = None
     
  def add_node(self, data):
    new_node = Node(data)
    new_node.next = self.head
    self.head = new_node

```

### Inserting a node
Inserting to a Singly Linked list after a node involves checking if the previous node exists and then making the newly created node's next pointer point to the previous node's next pointer. The prevoious node's next pointer points to the newly created node.

### Deleting a node
To delete a node from the linked list, we need to do the following steps:

* Find the previous node of the node to be deleted. 
* Change the next of the previous node. 
* Free memory for the node to be deleted.


# Doubly Linked Lists
Doubly Linked lists are quite similar to Singly linked lists but here, traversall can be done both ways. It uses an extra pointer to do so. Again, the head node is the beginning of the list and the tail points to the null pointer indicating the end of the list. In addition to the <b>Next Pointer</b>, each node also has a <b>Prev Pointer</b> which points to the previous node. The head's previous node points to null pointer and all other nodes in the list have their prev pointer pointing to the previous node.

### Python Code
```
class Node:
  def __init__(self, data):
    self.data = data
    self.next = None
    self.prev = None
 
class DoublyLinkedList:
  def __init__(self):
    self.head = None
     
  def add_node(self, data):
    new_node = Node(data)
    new_node.next = self.head
    if self.head is not None:
      self.head.prev = new_node
    self.head = new_node

```

### Inserting a node

Assuming previous node is prev_node and the node we want to insert is new_node,
* First, create a new node.
* Now insert the data in the new node.
* Point the next of new_node to the next of prev_node.
* Point the next of prev_node to new_node.
* Point the previous of new_node to prev_node.
* Change the pointer of the new node’s previous pointer to new_node.

### Deleting a node
Assume that node to be dleted is del_node and it has prev_node as the previous node and next_node as the next node. To delete a node from the linked list, we need to do the following steps:

* Find the previous node of the node to be deleted (del_node). 
* Change the next of the prev_node. Make it point to next_node.
* Change the prev of the next_node. Make it point to the prev_node.
* Free memory for the node to be deleted (del_node).


# Circular Linked Lists
This linked list is similar to Singly linked lists meaning that it is unidirectional but in this list, the tail node points to  the head node and hence it becomes circular in nature.

### Python Code
```
class Node:
  def __init__(self, data):
    self.data = data
    self.next = None
 
class CircularLinkedList:
  def __init__(self):
    self.head = None
     
  def add_node(self, data):
    new_node = Node(data)
    if self.head is None:
      self.head = new_node
      new_node.next = self.head
      return
    current = self.head
    while current.next != self.head:
      current = current.next
    current.next = new_node
    new_node.next = self.head

```

### Inserting a node
To insert a node in between the two nodes, follow these steps: 

* Create a node, say N. 
* Search for the node after which N needs to be inserted, say that node is prev. 
* Make N -> next = prev -> next; 
* prev -> next = N.

### Deleting a node

* If the list is not empty then we define two pointers curr and prev and initialize the pointer curr with the head node. If it is empty, simply return.
* Traverse the list using curr to find the node to be deleted and before moving to curr to the next node, every time set prev = curr.
* If the node is found, check if it is the only node in the list. If yes, set head = NULL and free(curr).
* If the list has more than one node, check if it is the first node of the list. Condition to check this( curr == head). If yes, then move prev until it reaches the last node. After prev reaches the last node, set head = head -> next and prev -> next = head. Delete curr.
* If curr is not the first node, we check if it is the last node in the list. Condition to check this is (curr -> next == head).
* If curr is the last node. Set prev -> next = head and delete the node curr.
* If the node to be deleted is neither the first node nor the last node, then set prev -> next = curr -> next and delete curr.
* If the node is not present in the list return head and don’t do anything.



# Applications
Linked lists are useful for music players, for web browsers to keep track of next and previous pages, for image galleries to go to previous and next image and so on. Even the undo operation can be modeled using linked lists.