
# Data Structures
- Definition:
	- Are ways to store and organize data, resulting in various levels of efficiency depending on use.
	- An example of data structures are Python's collections, like list arrays, refer to collections for more info.
- Python lists
	- Definition:
		- Lists are defined by square brackets _[ ]_.
	- Syntax:
		```
		<list_name>: list = [<values>]
		#> or
		<list_name>: list[<data_type>] = [<values>]
		```
	- Example:
		```
		my_list: list[int] = [1, 2, 3, 4]
		```
	- Methods:
		- Definition:
			- There are various built-in methods that are used for operations, like _.append()_ or _.sort()_, refer to functions for more info
- Stacks
	- Definition:
		- A stack is a linear structure that follows the LIFO principle, being the Last-In-First-Out rule which means, the last value added will the first value to be removed.
		- Stacks are data structures that can hold many variables:
		- Basic operations of stacks:
			- push
				- Add elements to the stack (like appending).
			- pop
				- Removes and returns the top element from the stack.
			- peek
				- Returns the top (logically last) element on the stack.
			- is empty
				- Queries if the stack is empty.
			- size
				- Queries the current size of the stack
	- Note:
		- Stacks in Python are usually implemented using lists or linked lists, which can also be implemented to have undo mechanisms like reverting to previous states used to create algorithms for depth_first search or for back-tracing.
	- Stacks using lists
		- Definition:
			- Why stacks using lists or arrays?
				- Memory efficiency
					- Arrays do not hold the next elements' address unlike linked lists.
				- Implementation
					- Stacks using arrays requires less code as opposed to linked lists, as it is easier to use lists than linked lists.
		- Stack implementation using Python's lists:
			```
			#> start with an empty stack
			stack: list = []
			
			#> push elements to the end of the stack
			stack.append('A')
			stack.append('B')
			stack.append('C')
			
			#> peek at the last element on the stack
			stack[-1]
			
			#> pops the element at the top of the stack
			stack.pop
			
			#> checks is the stack is empty
			not bool(stack) #> empty elements return a false
			
			#> checks the size of the stack
			len(stack)
			```
		- Note:
			- It is recommended to create a dedicated stack class, such that the methods are a bit more straight forward.
				- Sample code:
					```
					class Stack:
						#> creates an empty stack
						def __init__(self) -> None:
							self.stack: list = []
						
						#> method to check if the stack is empty
						def is_empty(self) -> bool:
							if len(self.stack):
								return False
							return True
						
						#> method to push elements to the end of the stack
						def push(self, value) -> None:
							self.stack.append(value)
						
						#> method to pop elements from the end of the stack and return it
						def pop(self) -> int | None:
							#> checks if the stack is empty
							if self.is_empty():
								print("stack is empty")
								return None
							return self.stack.pop()
						
						#> method to return the element at the top of the stack
						def peek(self) -> int | None:
							#> checks if the stack is empty
							if self.is_empty():
								print("stack is empty")
								return None
							return self.stack[-1]
						
						#> method to return the size of the stack
						def size(self) -> int:
							return len(self.stack)
					```
	- Stacks using linked lists
		- Definition:
			- Why stacks using linked lists?
				- Unlike normal lists, linked lists are able to be stored where there is free space in memory where linked lists do not have to be stored contiguously in memory.
				- Unlike lists when an element is removed (popped), the rest of the nodes in the linked list do not have to be shifted.
		- Note:
			- Even though linked lists are better when dealing with a scattered memory space, this type of list will use more memory space due to having to also store the node addresses.
				- The code is also more complex, making it a bit hard to understand or interpret.
		- Stack implementation using Python's linked lists:
			```
			#> handles the node logic
			class Node:
				def __init__(self, value) -> None:
					self.value: int = value                 #> takes in the value provided
					self.next: Node = None
			
			#> handles the linked stack logic
			class Stack:
				#> creates an empty stack
				def __init__(self) -> None:
					self.head: Node = None                  #> is the pointer to the first node
					self.size: int = 0                      #> represents the size of the list
			
				#> method to check if the linked list is empty
				def is_empty(self) -> bool:
					return self.sze == 0                    #> returns True if the stack is empty
			
				#> method to push new values to the stack
				def push(self, value) -> None:
					new_node = None(value)                  #> creates a new node for the new value
					if self.head:                           #> runs if the head is not empty
						new_node.next = self.head           #> gives the current head to the new node (value head)
					self.head = new_node                    #> gives the new node object to the head of the list
					self.size += 1                          #> increases the size by 1
			
				#> method to pop values from the stack
				def pop(self) -> int | None:
					if is_empty:                            #> checks if the stack is empty
						print("stack is empty")
						return None                         #> returns if True
					popped_node = self.head                 #> popped_head gets the self.head object
					self.head = self.head.next              #> the new head beomes the _.next attrubute_
					#> or the pointer to the next item in the stack
					#> from the top down
					self.size -= 1                          #> decreases the size by 1
					return popped_node.value                #> returns the value that the removed node holds
			
				#> method to look at the latest value in the stack
				def peek(self) -> int | None:
					if is_empty:                            #> checks if the stack is empty
						print("stack is empty")
						return None                         #> returns if True
					return self.head.value                  #> returns the current value at the top of the stack
			
				#> method to return the current size of the stack
				def size(self) -> int:
					return self.size                        #> returns the current size
			
				#> method to print the nodes in order
				def traverse(self) -> None:
					current_node = self.head                #> current_node gets a copy of self.head
					while current_node:                     #> loops current_node until it results to None
					#> which is the beginning of the stack
						print(current_node.value, end="- ") #> prints the value of the current node it is at
						current_node = current_node.next    #> changes the pointer to the next value in the stack
					print()                                 #> adds a new line
			```
- Queues
	- Definition:
		- This concept follows the FIFO principle, First-In-First-Out.
			- Where the first element in would be the first element to be removed which the exact opposite of the LIFO principle
		- Basic Operations of Queues:
			- enqueue
				- Adds an element to the end of the queue.
			- dequeue
				- Removes the first element on the queue.
			- peek
				- Returns the first element on the queue
			- is_empty
				- Returns a boolean if queue is empty.
			- size
				- Returns an integer corresponding to the current size of the queue.
	- Note:
		- Queues in Python are usually implemented using lists or linked lists, being used for scheduling, order processing, or message queuing or even be used for algorithms like breadth search in graphs.
	- Queue using lists
		- Queue implementation in Python's list
			```
			#> start with an empty queue
			queue: list = []
			
			#> enqueue items in the queue
			queue.append('A')
			queue.append('B')
			queue.append('C')
			
			#> peek at the first item in the queue
			queue[0]
			
			#> dequeue items from the queue
			queue.pop(0)
			
			#> checks if the queue is empty
			not bool(queue)
			
			#> queries the size of the queue
			len(queue)
			```
		- Note:
			- Unlike stacks, de-queuing items from a queue is generally inefficient, as it shifts the position of all items in the queue and even more so for large queues.
		- Queue implemented as a class:
			```
			class Queue:
				#> creates an empty queue
				def __init__(self) -> None:
					self.queue: list = []
			
				#> method to check if the queue is empty
				def is_empty(self) -> None:
					return len(self.queue) == 0
			
				#> method to enqueue items from the queue
				def enqueue(self, value) -> None:
					self.queue.append(value)
			
				#> method to dequeue items from the queue
				def dequeue(self) -> int | None:
					if self.is_empty():
						print("queue is empty")
						return None
					return self.queue.pop(0)
			
				#> method to return the first element in the queue
				def peek(self) -> None:
					if self.is_empty():
						print("queue is empty")
						return None
					return self.queue[0]
			
				#> method to return the current size of the queue
				def size(self) -> int:
					return len(self.queue)
			```
	- Queue using linked lists
		- Definition:
			- Why queues using linked lists?
				- Unlike normal lists, linked lists are able to be stored where there is free space in memory, 
					- Where linked lists do not have to be stored contiguously in memory.
				- Linked lists also don't shift the elements in current queue, unlike lists which shift items when items are removed inside the list.
				- Unlike lists when an element is removed (popped), the rest of the nodes in the linked list do not have to be shifted
		- Note:
			- Even though linked lists are better when dealing with a scattered memory space, this type of list will use more memory space due to having to also store the node addresses.
			- The code is also more complex, making it a bit hard to understand or interpret
		- Queue implementation using Python's linked lists
			```
			#> handles the node logic
			class Node:
				def __init__(self, value) -> None:
					self.value: int = value                 #> takes in the value provided
					self.next: Node = None                  #> presumably the next node address(?)
			
			#> handles the linked queue logic
			class Queue:
				#> creates an empty queue
				def __init__(self) -> None:
					self.front: Node = None                 #> represents the first in line
					self.rear: Node = None                  #> represents the last in line
					self.size: int = 0                      #> represents the size of the queue
			
				#> method to check if the linked queue is empty
				def is_empty(self) -> bool:
					return self.size == 0                   #> returns True if the queue is empty
			
				#> method to enqueue items to the queue
				def enqueue(self, value) -> None:
					new_node = Node(value)                  #> creates a new node for the new value
					if self.rear is None:                   #> if the queue is currently empty
						self.front = self.rear = new_node   #> sets the value of self.front and self.rear to the new_node object
						self.size += 1                      #> increases the size by 1
						return                              #> exits the function call
					self.rear.next = new_node               #> if the queue is not empty, this code runs and sets the last in the queue to the new node
					self.size += 1                          #> increases the size by 1
			
				#> method to dequeue items from the queue
				def dequeue(self) -> int | None:
					if is_empty:                            #> checks if the queue is empty
						print("queue is empty")             
						return None                         #> returns if True
					dequeued = self.front                   #> dequeued gets the value of self.front
					self.front = self.front.next            #> the new front becomes the next element in the queue or the pointer to the next node
					#> from the bottom up
					self.size -= 1                          #> decreases the size by 1
					if self.front is None:                   #> checks if the front of the queue is empty
						self.rear = None                    #> sets the rear of the queue to None if the queue is now empty
			
				#> method to look at the front value in the queue
				def peek(self) -> int | None:
					if is_empty:                            #> checks if the queue is empty
						print("queue is empty")             
						return None                         #> returns if True
					return self.front.ValueError            #> returns the current value at the front of the queue
			
				#> method to return the current size of the queue
				def size(self) -> int:
					return self.size                        #> retunr the current size
			
				#> method to print the nodes in order
				def traverse(self) -> None:
					current_node = self.front               #> current_node gets a copy of self.front
					while current_node:                     #> loops current_node until it results to None which is the end of the queue
						print(current_node.value, end="- ") #> prints the value of the current node it is at
						current_node = current_node.next    #> changes the pointer to the next value in the stack
					print()                                 #> adds a new line
			```
- Linked Lists
	- Definition:
		- Is a list where the nodes are linked together, each node contains both a data and a pointer.
			- The data it stores are able to be any value
		- Like normal arrays, the pointer it holds is a pointer to another node.
		- The elements in this list is linked together such that each node points to where in memory the other node is placed.
		- Figure:
			```
			|────────|     |────────|     |────────|
			|  DATA  |   ->|  DATA  |   ->|  DATA  |
			|────────|  /  |────────|  /  |────────|
			|  NEXT -|-/   |  NEXT -|-/   |  NEXT -|
			|────────|     |────────|     |────────|
			```
		- Linked lists vs arrays (Python)
			- Unlike linked lists, arrays are a existing data structure where linked lists which has to be implemented.
			- In arrays, elements are stored together right next to each other (contiguous).
				- this is more memory efficient unlike linked lists wherein it has to accommodate nodes as well.
			- While in linked lists, they are store separately in their own part in memory.
			- In linked lists, elements are not able to be accessed directly (random access), while in arrays, this is not the case.
			- Elements are able to be removed or added without any shifting in linked lists.
				- This is not the case in arrays, due to each element shifting every time the array is modified
			- Implementing linked lists is way more complicated unlike built-in arrays, this is due to the logic required to efficiently traverse linked lists
		- Time complexities in Linked Lists Operations
			- Linear search works the same as normal lists, due to the algorithm searching through each node (element) one after the other.
			- Binary search however, is impractical in linked lists due to the algorithm needing to jump to specific nodes.
				- It is technically possible, but the performance penalty makes it impractical to use.
			- Sorting algorithms that goes through each node sequentially is possible in linked lists, but algorithms that requires to jump through each other nodes (or based on an index) are unlikely to work in linked lists.
		- Basic operation of Linked Lists:
			- traversal
				- Traverses from one node to another.
				- Sample code:
					```
					#> singly linked lists
					class Node:
					def __init__(self, value) -> None:
						self.data: int = data
						self.next: Node = None
					
					#> logic
					def traverse(head) -> None:
						current_node: Node = head
						while current_node:
							print(current_node.data, end=" > ")
							current_node = current_node.next
						print("null")
					```
			- deletion
				- Nodes are able to be removed at a constant performance penalty.
				- Like removing a certain node, this comes at a constant performance penalty.
			- sort
				- This type of operation is more complicated but has the same penalties.
	- Types of linked lists:
		- Singly linked lists
			- Definition:
				- This type of list are the simplest kind of linked lists.
				- It takes up less memory space than other types, due to each node only being linked to one other node.
			- Figure:
				```
				|────────|     |────────|     |────────|
				|  DATA  |   ->|  DATA  |   ->|  DATA  |
				|────────|  /  |────────|  /  |────────|
				|  NEXT -|-/   |  NEXT -|-/   |  NEXT -|
				|────────|     |────────|     |────────|
				```
		- Doubly linked lists.
			- Definition:
				- This type of linked list has both the address of the next node, but also has the address of the previous node.
				- This type of list takes up more memory space than single linked nodes, due to having an additional memory address to store
			- Figure:
				```
				|────────|<----|────────|<----|────────|
				|  PREV  |   ->|  PREV  |   ->|  PREV  |
				|────────|   | |────────|   | |────────|
				|  DATA  |  /  |  DATA  |  /  |  DATA  |
				|────────|  |  |────────|  |  |────────|
				|  NEXT -|-/   |  NEXT -|-/   |  NEXT -|
				|────────|     |────────|     |────────|
				```
		- Circular linked lists
			- Definition:
				- This type of linked lists mostly stays the same as doubly linked lists, but the "head" and "tail" nodes are connected.
				- Even though this types of linked lists mostly take the same memory doubly linked lists, it is a lot more complicated to implement.
					- The trade off is that this type of linked lists are "contiguous", the elements inside are able to be cycled through.
					- Though it is required to run checks every time a new node is created or removed, to check if there are no links that points to null.
			- Types of circular linked lists:
				- Circular Singly Linked Lists
					- Definition:
						- A circular singly linked list only points to the next node, it cannot do so to the previous node.
					- Figure:
						```
						  |────────|     |────────|     |────────|
						->|  DATA  |   ->|  DATA  |   ->|  DATA  |
						| |────────|  /  |────────|  /  |────────|
						| |  NEXT -|-/   |  NEXT -|-/   |  NEXT -|-\
						| |────────|     |────────|     |────────| |
						\------------------------------------------/
						```
				- Doubly Circular Linked Lists
					- Definition:
						- A circular doubly linked list can point both at the next node and also to the previous node.
					- Figure:
						```
						/------------------------------------------\
						| |────────|<----|────────|<----|────────| |
						\-|  PREV  |   ->|  PREV  |   ->|  PREV  |</
                    > |────────|   | |────────|   | |────────|
						| |  DATA  |  /  |  DATA  |  /  |  DATA  |
						| |────────|  |  |────────|  |  |────────|
						| |  NEXT -|-/   |  NEXT -|-/   |  NEXT -|-\
						| |────────|     |────────|     |────────| |
						\------------------------------------------/
						```
- Hash Tables
	- Definition:
		- A data structure that is designed to be fast to work with.
		- Why Hash Tables?
			- This type of data structure is sometime more preferred instead of arrays, due to being faster when searching, adding, and removing data even with large amounts of data.
			- Hash tables are useful when using a container that is easy to:
				- Find something, like a book in a library.
				- Store and find elements quickly.
				- Connecting values to keys, the keys are tied to their values.
		- Hash tables vs lists
			- In linked lists
				- Finding an element will take since each node must be checked, only halting when the element has been found, taking _O(n)_ time.
			- In normal lists
				- Even though the element to be found is known, the index is unknown, taking the same amount of time as linked lists due to this.
			- In hash tables
				- The element can be easily found since there is a way to go to the element directly, through the use of a "hash function".
				- On average, hash tables table about O(1) time.
		- A hash table is able to be made using 5 key points:
			- It requires an empty list.
			- It requires a hash function.
			- Inserting an element using a hash function.
			- Looking up an element using a hash function.
			- Handling collisions.
		- Sample code:
			```
			#> create an empty list (can be a set or a dictionary)
			my_list: list[list = [[], [], [], [], []] #> stores 5 elements
			#> also called "buckets"
			#> nested arrays prevent collisions
			#> also called "chaining"   
			
			#> create a hash function
			def hash_function(value) -> int:
				hash_sum = 0                                 #> stores the value of the has
				for char in value:                           #> loops through every single character
					hash_sum += ord(char)                    #> converts a character into a unicode code number
				return hash_sum % 5                          #> uses a modulo to dictate where the value is stored in
																	#> different text will result into different hash codes
																	#> using a modulo will make storing a bit easier
			#> create an add function
			def add(value) -> None:
				index = hash_function(value)             #> calls the hash_function to return an index
																#> where the new value is going to be stored in 
				my_list[index].append(value)             #> appends the new value to the corresponding index
			
			#> create a loopup function
			def lookup(value) -> None:
				index = hash_function(value)             #> calls the hash_function to return an index
																#> looks up where the value might be stored in
				print(f"{value} is at {index}")          #> returns the index wherein the valus is stored at
			```
- Trees
	- Definition:
		- A hierarchical data structure consisting of nodes connected by edges, as each node contains a value and references to its child nodes.
		- Similar to linked lists, each node consists of both data and a reference to other nodes.
		- Unlike other data structures, in trees, a single element can have multiple 'next' elements which allows data to branch out in various directions,
		- Use cases:
			- Hierachical data
				- Like file systems, organizational models, etc.
			- Databases
				- Quick data retrieval.
			- Routing tables
				- Used for routing data in network algorithms
			- Sorting or searching
				- Used for sorting data or searching for data
		- Priority queues
			- Priority queues are commonly implemented using trees, such as binary heaps
		- Trees vs Lists
			- Arrays (lists)
				- Are fast when accessing data directly, only when the index is known.
				- Inserting and deleting elements requires other elements to shift in memory, in order to take place for the new element of to take the place of the deleted element.
					- This process is very time consuming for very big data sets
		- Linked lists
			- Are fast when inserting and deleting nodes, as it does not require any memory shifting.
			- Accessing an element in a linked lists is slow, as the list must first be traversed to access the element.
		- Trees
			- In Binary Trees, Binary Search Tree and AVL trees.
			- Trees are better due to it being better in accessing and modifying each node, as it does not need to shift memory.
	- Types of Trees:
		- Binary Trees
			- Definition:
				- Each node has up to two children, the left and right child node
				- This structure is the foundation for more complex tree types, like Binary Search Trees, and AVL Trees.
		- Binary Search Trees (BSTs)
			- A type of a Binary Tree where for each node, the left child node has a lower value and the right child node has a higher value.
		- AVL Trees
			- Named after Adelson-Velsky and Landis.
			- A type of Binary Search Tree that self-balances so that for every node.
			- The difference between the left and right sub-trees is at most one, 1.
				- The balance is maintained through rotations where nodes are inserted or deleted

	- Binary Trees
		- Definition:
			- It a type of a tree data structure where each node an have up to two child nodes, a left child node and right child node.
			- Why Binary Trees?
				- Algorithms that traverse, search, inserts and deletes element are simpler.
				- It is easier to implement and runs faster.
				- Keeping data in a Binary Search Tree is very efficient when searching for elements.
				- Balancing trees are easier to do with a limited number of child nodes, e.g. using an AVL Binary Tree.
				- Binary Trees can be represented as arrays, making the tree more memory efficient.
		- Types of Binary Trees
			- Balanced trees
				- Definition:
					- At most, only one difference between is left and right sub-tree heights, for each node in the tree
				- Figure:
					```
					                |---| 
					          _---->| R |<----_
					         |      |---|      |
					         |                 |
					       |---|              |---|
				      _-->| A |<--_      _-->| B |
					  |    |---|    |    |    |---|
					  |             |    |
					|---|         |---||---|
					| C |         | D || E |
					|---|         |---||---|
					```
			- Complete trees
				- Definition:
					- Has all levels of full nodes, except the last level which can be full, or filled from left to right.
					- It has the properties of a binary tree, which means it is also balanced.
				- Figure:
					```
					                     |---| 
					              _----->| R |<-----_
					             |       |---|       |
					             |                   |
					           |---|               |---|
					       _-->| A |<--_       _-->| B |<--_
					      |    |---|    |     |    |---|    |
					      |             |     |             |
					    |---|         |---| |---|        |---|
					  _>| C |<_     _>| D | | E |        | F |
					  ? |---| ?     ? |---| |---|        |---|
					  |       |     |
					|---|   |---| |---|
					| G |   | H | | I |
					|---|   |---| |---|
					```
			- Full tree
				- Definition:
					- Is a kind of tree where each node either has 0 or 2 nodes, and there cannot be a node with a single child node.
				- Figure:
					```
					                    |---| 
					              _---->| R |<----_
					             |      |---|      |
					             |                 |
					           |---|              |---|
					       _-->| A |<--_          | B |
					      |    |---|    |         |---|
					      |             |    
					    |---|         |---|
					  _>| C |<_       | D |
					  ? |---| ?       |---|
					  |       |
					|---|   |---|
					| E |   | F |
					|---|   |---|
					```
			- Perfect tree
				- Definition:
					- It has all leaf nodes on the same level meaning, all levels are full of nodes.
					- All internal nodes have two child nodes and it is also perfect, balanced and complete.
				- Figure:
					```
					                |---| 
					          _---->| R |<----_
					         |      |---|      |
					         |                 |
					       |---|              |---|
					   _-->| A |<--_      _-->| B |<--_
					  |    |---|    |    |    |---|    |
					  |             |    |             |
					|---|         |---||---|        |---|
					| C |         | D || E |        | F |
					|---|         |---||---|        |---|
					```
		- Tree implementation in Python
			- Definition:
				- Similar to Linked Lists, implementing Trees is the same to it
			- Binary tree implementation in Python:
				```
				class TreeNode:
					def __init__(self, data) -> None:
						self.data: str = data 
						self.left: TreeNode = None
						self.right: TreeNode = None
				
				#> binary tree with a depth of two (root and two children)
				class Tree:
					def __init__(self, value) -> None:
						self.tree: TreeNode = TreeNode(value)
				
					def add_right(self, value) -> None:
						self.tree.right = value
				
					def add_left(self, value) -> None:
						self.tree.left
				
				#> implementation without the Tree class
				root_node: TreeNode = TreeNode('R')
				node_a: TreeNode = TreeNode('A')
				node_b: TreeNode = TreeNode('B')
				
				root_node.left = node_a
				root_node.right = node_b
				```
		- Binary Tree Traversal
			- Definition:
				- Going from node to node is called "traversal".
				- Unlike linked lists, since they are linear data structures it is only traversable in one of two ways at the start of the first node (element) and go forwards or backwards.
				- Since trees can branch out to different directions, which is non-linear, there are different ways of traversing Trees.
			- Two main categories of Tree traversal methods
				- Breadth First Search (BFS)
					- Is when the nodes on the same level are visited all before going to the next level in the tree .
					- Meaning, that the three is explored in a more sideways direction.
				- Depth First Search (DFS)
					- Is when the traversal moves down the tree all to the leaf nodes (external), exploring the tree branch by branch in a downwards direction.
					- There are three different types of DFS traversals:
						- Pre-order
						- In-order
						- Post-order
					- Pre-order Traversal
						- Definition:
							- Is a type of DFS, where each node is visited in a certain order.
							- Done by visiting the root node first, then recursively do a pre-order traversal of the left sub-tree followed by a recursive pre-order traversal of the right sub-tree.
							- Used for creating a cope of the tree, prefix notation of an expression tree, etc.
							- It is called "pre" due to each node is printed before the recursion of the left and right sub-trees.
						- Implementation of pre-order traversal of trees
							```
							def pre_order_traversal(node) -> None:
								if node is None:
									return
								print(node.data, end=", ")
								pre_order_traversal(node.left)
							```
						- Note:
							- In the function implementation, the first node to be printed is the root node, the first node to be traversed before calling the left node and then the right node.
								- The function keeps traversing the left sub-tree before going to the right sub-tree.
								- It will switch to the other node once the node becomes None, indicating that the node has no child nodes after both left and right nodes return None.
								- The recursive function ends and returns to the parent recursion, the function ends its propagation until the rightmost node is reached.
					- In-order Traversal
						- Definition:
							- Is a type of DFS, where each node is visited in a certain order, done by a visiting the leftmost node first, recursively searching for the leftmost node.
							- After which, visits the root node and then visits the right node until the rightmost nodes.
							- It is called "in" due to the node being printed in between recursion calls, the node gets printed after the left sub-tree and before the right sub-tree.
						- Implementation of in-order traversal of trees
							```
							def in_order_traversal(node) -> None:
								if node is Node:
									return
								in_order_traversal(node.left)
								print(node.data, end=", ")
								in_order_traversal(node.right)
							```
						- Note:
							- In the function implementation, the first node to be printed is the leftmost node, calling itself until the child with the most leftmost node is printed.
								- Once the node becomes None. it indicates that there is no left child node.
								- After that, moves to the parent of the child node and then, the right node before moving a node backwards.
								- The function recursively runs through the tree until the rightmost three is printed.
					- Post-order Traversal
						- Definition:
							- Is a type of DFS, where each node is visited in a certain order.
							- Done visiting the leftmost node first recursively searching for the leftmost node.
							- After which, recursively searches for the rightmost nodes, and then finally printing the data of the node.
							- It is called "post" due to it visiting a node, after the left and right child nodes are called recursively.
						- Implementation of post-order traversal of trees
							```
							def post_order_traversal(node) -> None:
								if node is None:
									return
								post_order_traversal(node.left)
								post_order_traversal(node.right)
								print(node.data, end=", ")
							```
						- Note:
							- In the function implementation, the first node to be printed is the leftmost child node, printing the node and the going to the right child of the same parent node.
								- Once the node becomes None, it indicates that the leftmost child node is empty then moves on to the right child node.
								- After which bot child nodes becomes None, prints the data.
								- The function recursively runs through the tree until all nodes is printed.
		
	- Binary Search Trees
		- Definition:
			- BST is a type of Binary Tree data structure.
			- The following properties must be true for a node in the tree:
				- The node's left child and all of it's descendants, like its children, children's children, etc.
				- It must have lower values than the original node's value.
				- the node's right child and all of its descendants must have higher values than the original node's value.
				- the left and right sub-trees must also be BSTs
			- These properties makes it faster to search, add, and delete values than a regular Binary Tree.
			- Assuming all values in a BST are unique, the size of a tree and the number of nodes in it is _n_.
			- A sub-tree starts with one of the nodes in the tree as a local root, consisting of that node and all of its descendants.
				- The descendants of a node are all the child nodes of that node and their child nodes, and that child's child nodes, and so on.
				- And the descendants will be all nodes that are connected below that node.
			- The node's height is the maximum number of edges between that node and a leaf node.
			- A node's in-order successor is the node that comes after it if the in-order traversal is used.
			- An in-order traversals of the BST would result in node 13 coming before node 14 and so, the successor of node 13 would be node 14.
		- Binary Search Tree Traversal
			- Definition:
				- The primary way to check if the tree is a BST, is to check if the tree posses the properties of BSTs.
				- Another way is to use in-order traversal, printing out if the nodes are in order from lowest to highest.
			- Implementation of Binary Search Trees in Python:
				```
				class TreeNode:
					def __init__(self, data) -> None:
						self.data: int = data
						self.left: TreeNode = None
						self.right: TreeNode = None
			
					def in_order_traversal(node) -> None:
						if node is None:
							return
						in_order_traversal(node.left)
						print(node.data, end=', ')
						in_order_traversal(node.right)
				
				#> example
				root: TreeNode = TreeNode('10')
				node_a: TreeNode = TreeNode('7')
				node_b: TreeNode = TreeNode('13')
				node_c: TreeNode = TreeNode('6')
				node_d: TreeNode = TreeNode('8')
				node_e: TreeNode = TreeNode('12')
				node_f: TreeNode = TreeNode('14')
				
				root.left = node_a
				root.right = node_b
				
				node_a.left = node_c
				node_a.right = node_d
				node_b.left = node_e
				node_b.right = node_f
				```
		- BST value searching
			- Definition:
				- Finding a value in a BST is similar to using Binary Search on an array.
				- Rules:
					- Start at the root node
					- If the in that node is equal to the target value,
						- Then return.
					- If the target value is higher than the value at that node,
						- Continue searching to the right sub-tree.
					- If the target value is lower than the value at that node,
						- Continue searching to the left sub-tree.
					- If the node returns None, and there are no more sub-trees,
						- The target value is not present inside the BST.
			- Sample Code:
				```
				def binary_search(node, target) -> int | None:
					if node is None:
						return None
					elif node.data == target:
						return node
					elif node > node.data:
						return binary_search(node.left, target)
					else:
						return binary_search(node.right, target)
				```
			- Note:
				- Using a Binary Search algorithm on an array, it must be first sorted.
				- Since BSTs are already ordered from highest to lowest, using the same algorithm as Binary Search is very efficient.
				- In order to find the lowest value or the highest value in a BST, go as far left or as far right as possible, respectively
					- Sample Code:
						```
						def get_lowest_node(node) -> TreeNode:
							current: TreeNode = node
							while current.left is not None:
								current = current.left
							return current
							
						def get_highest_node(node) -> TreeNode:
							current: TreeNode = node
							while current.right is not None:
								current = current.right
							return current
						```
		- BST value insertion
			- Definition:
				- Inserting a value in a BST is similar to searching a value.
				- Rules:
					- Start at the root node.
					- If the value is higher than the node.
						- Go to the right sub-tree.
					- If the value is lower than the node,
						- Go to the left sub-tree.
					- If there are no more sub-trees to go to,
						- Then insert the value as a new node.
			- Note
				- All nodes in are unique and if the value to insert is the same value as a node, then the new value is discarded.
			- Sample Code:
				```
				def insert_node(node, value) -> TreeNode:
					if node is Node:
						return TreeNode(value)
					else:
						if value > node.data:
							node.right = insert_node(node.right, value)
						elif value < node.data:
							node.left = insert_node(node.left, value)
						return node
				```
		- BST value deleting
			- Definition:
				- In order to delete a node, the node must first be searched.
					- After which, if found, there are three cases that can be done.
				- Rules:
					- If the node is a lead node (external),
						- It can be removed by removing the link to it.
					- If the node is not a leaf node and only has one child node,
						- It can be removed by connecting its child node to the current node's parent node.
					- If the node has both a left and right child node,
						- Then find the node's in order successor, change the values with that node and then delete it.
			- Sample Code:
				```
				#> the function in which enables deleting specific nodes
				#> note that the "node" perimeter enables recursion
				def delete_node(node, value) -> TreeNode | None:
					# these lines searches for the node with the correct value to delete
					if not node:
						return None
					if node < node.data:
						node.left = delete(node.left, data)
					elif data > node.data:
						node.right = delete(node.right, data)
					#> runs when the corrent node to delete has been found
					else:
						#> if there is no child nodes
						#> None is returned
						#> if there is either a left child or right child node
						#> then those child nodes beomes the parent of the current node's left or right child node
						#> if the node has both child nodes
						#> the in-order successor is found using the get_lowest_node() function
						#> keeping the successor's value by seeting it as the value of the node to delete, and then it is now possible to delete the successor node
						if not node.left:
							temp: TreeNode = node.right
							node = None
							return temp
						elif not node.right:
							temp: TreeNode = node.left
							node = None
							return temp
						node.data = get_lowest_node(node.right).data
						node.right = delete(node.right, node.data)
						return node
				```
		- Time complexity
			- Definition:
				- The time complexity for finding a value inside a sub-tree is _O(h)_.
					- Where h is the height of the tree, only if the BST is a balanced tree.
			- Figure:
				```
								 |---| 
						  _----->| 5 |<-----_
						 |       |---|       |
						 |                   |
					   |---|               |---|
				   _-->| 3 |<--_       _-->| 7 |
				  |    |---|    |     |    |---|
				  |             |     |
				|---|         |---| |---|
				| 1 |         | 4 | | 6 |
				|---|         |---| |---|
				```
			- Note:
				- If a BST contains the most nodes in the left sub-tree, the worst case search will take longer.
					- These types of trees are called unbalanced trees.
					- Figure:
						```
											|---| 
									  _---->| 5 |<----_
									 |      |---|      |
									 |                 |
								   |---|              |---|
							   _-->| 3 |<--_          | 7 |
							  |    |---|    |         |---|
							  |             |    
							|---|         |---|
						  _>| 1 |         | 4 |
						  ? |---|         |---|
						  |        
						|---|
						| 0 |
						|---|
						```
			- BST time complexity compared to other Data Structures
				- Comparing to sorted arrays and linked lists.
					- Sorted arrays
						- _O(log n)_
					- Linked lists
						- __O(n)__
					- BSTs
						- _O(log n)_
				- Note 
					- Searching a BST is just as fast as Binary Search on an array, with the same _O(log n)_ time complexity.
						- Add on to the fact that items don't have to be shifted in memory, when inserting or deleting elements like Linked Lists.
					- When inserting, deleting or searching for a node, the time complexity is actually _O(h)_, wherein h is the right.
						- Meaning, the higher (or taller) the tree, the longer the operation will take.
					- The reason why the time complexity compared to other Data Structures is _O(log n)_, is only true if the tree is balanced.
						- Refer to types of Binary Trees
					- For a balanced BST, with a large number of nodes (n), the height becomes _h ≈ log n_.
						- Therefore, the time complexity becomed _O(h)_ = _O(log n)_
					- In the case of BSTs being unbalanced, the height of the tree is approximately the same as the number of nodes.
						- _h ≈ n_
						- Therefore, the time complexity becomes _O(h)_ = _O(n)_.
					- In order to optimize a BST, the height of the the tree must be minimized.
						- for that, the tree must become balanced, AVL trees solves this problem.
	- Adelson-Velsky and Landis Trees
		- Definition:
			- Commonly known as AVL Trees, invented by Georgy Adelson-Velsky and Evgenii Landis in 1962.
			- It is a type of Binary Search Tree, and are self-balancing.
				- Meaning, that the tree height is kept to a minimum so that fast runtime is guaranteed searching, inserting and delete nodes with the time complexity of _O(log n)_.
			- The only difference it and a regular Binary Search Tree, is that an AVL Tree do rotation operations in addition, keeping the tree balanced.
			- In return, AVL trees ensures that it always have a minimum tree height.
				- Meaning, searching, inserting, and deleting operations can be very fast.
		- Figure:
			```
			    Unbalanced Binary Search Tree                   Self-balancing AVL Tree
			             Height: 5                                      Height: 2
			                        |---|                                |---|
			                  _---->| 5 |<----_                   _----->| 3 |<-----_
			                 |      |---|      |                 |       |---|       |
			                 |                 |                 |                   |
                         |---|              |---|            |---|               |---|
			           _-->| 3 |<--_          | 7 |        _-->| 0 |<--_       _-->| 5 |<--_
			          |    |---|    |         |---|       |    |---|    |     |    |---|    |
			          |             |                   |---|         |---| |---|         |---|
			        |---|         |---|                 |-1 |         | 1 | | 4 |         | 7 |
			      _>| 1 |         | 4 |                 |---|         |---| |---|         |---|
			      ? |---|         |---|
			      |        
			    |---|
             >| 0 |
			  / |---|
			  ?
			|---|
			|-1 |
			|---|
			```
		- Note
			- The two trees above are both Binary Search Trees, having the same nodes and the same in-order traversal.
				- The height is very different due to AVL Trees being always balanced/
			- To restore the balance of an AVL Tree, left or right rotations are done, or a combination of left and right rotations.
				- Sub-trees change parents during rotation to maintain in-order traversal and to maintain the BST property.
				- Such that the left child is left than the right child, for all nodes in the tree.
		- The Balance Factor
			- Definition:
				- A node's balance factor is he difference in sub-tree heights.
				- The sub-tree heights are stored to each node for all nodes in an AVL tree.
				- The balance factor is calculated based on its sub-tree heights.
				- To check if the tree has become out of balance, the height of a sub-tree is the number of the edges between the root node of the sub-tree and the leaf nodes farthest down in that sub-tree.
				- The balance factor (BF) for a node (X), is the difference between its right and left sub-trees.
			- Formula
				$BF(X) = height(right_sub-tree(X)) - height(left_sub-tree(X)))$
				- When
					- 0
						- The node is in balance.
					- > 0
						- The node is right-heavy.
					- < 0
						- The node is left-heavy
			- Note
				- If the balance factor is less than 0, or more than 1 for one or more node in the tree, then the tree is not considered balanced and a rotation is needed to restore balance.
			- Out-of-balance cases:
				- Left-Left (LL)
					- The unbalanced node and its left child node are both left-heavy.
					- A single right rotation is required to restore balance.
				- Right-Right (RR)
					- The unbalanced node and its right child node are both left-heavy.
					- A single left rotation is required to restore balance.
				- Left-Right (LR)
					- the unbalanced node is left-heavy and its left node is right heavy.
					- To restore balance, a left rotation on the left child, then the a right rotation on the unbalanced node.
				- Right-Left (RL)
					- The unbalanced node is right-heavy and its left node is left heavy.
					- To restore balance, a right rotation on the left child, then the a left rotation on the unbalanced node.
			- Left-Left Case
				- Definition:
					- A node where the unbalance is discovered to be left heavy, so is the left child node, also being left heavy.
					- In this case, a single right rotation on the unbalanced node is enough to restore balance
				- Figure:
					```
					   Left-Left Case              Right Rotation
					                 |---|              |---|
					          _----->| 5 |       _----->| 3 |<-----_
					         |       |---|      |       |---|       |
					         |       -2 BF      |       00 BF       |
					       |---|              |---|               |---|
					   _-->| 3 |              | 1 |               | 5 |
					  |    |---|              |---|               |---|
					  |    -1 BF              00 BF               00 BF
					|---|
					| 1 |
					|---|
					00 BF
					```
					- Note:
						- In the figure above, when '1' is added, the balance factor of '5' becomes -2.
							- Meaning the tree is unbalanced.
							- This becomes an LL case due to both the unbalanced node '5', and its left child node '3' are left node heavy which is a negative balance factor.
							- A single right rotation at node '5' restores the balance of the tree
				- Figure:
					```
					         Left-Left Case                            Right Rotation
					                     |---|                               |---|
					              _----->| 3 |<-----_                 _----->| 1 |<-----_
					             |       |---|       |               |       |---|       |
					             |       -2 BF       |               |       00 BF       |
					           |---|               |---|           |---|               |---| 
					       _-->| 1 |<--_           | 5 |       _-->| 0 |           _-->| 3 |<--_
					      |    |---|    |          |---|      |    |---|          |    |---|    |
					      |             |          00 BF      |    -1 BF          |    00 BF    |
					    |---|  -1 BF  |---|                 |---|               |---|         |---|
					  _>| 0 |         | 2 |                 |-1 |               | 2 |         | 5 |
					  ? |---|         |---|                 |---|               |---|         |---|
					  | -1 BF         00 BF                 00 BF               00 BF         00 BF
					|---|
					|-1 |
					|---|
					00 BF
					```
					- Note:
						- In the figure above, as nodes '2', '0' and '-1' are added, the balance factor of '3' becomes -1.
							- Meaning, the tree is out of balance
							- This is also a LL case due to both the unbalanced '3' node, and its left child node '1' are left heavy.
							- A single right rotation at node '3' restores the balance.
			- Right-Right Case
				- Definition:
					- A node where the unbalance is discovered to be right heavy, so it the left child node, also being right heavy.
					- In this case, a single left rotation on the unbalanced node is enough to restore balance.
				- Figure:
					```
					  Right-Right Case             Left Rotation
					|---|                               |---|
					| 1 |<-----_                 _----->| 3 |<-----_
					|---|       |               |       |---|       |
					-2 BF     |---|             |       00 BF       |
					          | 3 |<--_       |---|               |---|
					          |---|   ?       | 1 |               | 5 |
				              -1 BF  |       |---|               |---|
					                |---|     00 BF               00 BF
					                | 5 |
					                |---|
					                00 BF
					```
					- Note:
						- In the figure above, when '5' is added, the balance factor of '1' becomes -2.
							- Meaning, the tree is unbalanced.
							- This becomes an RR case due to both the unbalanced node '1', and its left child node '3' are right node heavy which is a negative balance factor.
							- A single left rotation at node '1' restores the balance of the tree
				- Figure:
					```
					         Right-Right Case                      Left Rotation
					          |---|                                     |---|
					   _----->| 3 |<-----_                       _----->| 5 |<-----_
					  |       |---|       |                     |       |---|       |
					  |       +2 BF       |                     |       00 BF       |
					|---|               |---|                 |---|               |---| 
					| 1 |           _-->| 5 |<--_         _-->| 3 |<--_           | 7 |<--_
					|---|          |    |---|    |       |    |---|    |          |---|    |
					00 BF          |    +1 BF    |       |    00 BF    |          +1 BF    |
					             |---|         |---|   |---|         |---|               |---|
					             | 4 |         | 7 |<_ | 1 |         | 4 |               | 8 |
					             |---|         |---| ? |---|         |---|               |---|
					             00 BF         +1 BF | 00 BF         00 BF               00 BF
					                               |---|
					                               | 8 |
					                               |---|
					                               00 BF
					```
					- Note:
						- In the figure above, as nodes '4', '7' and '8' are added, the balance factor of '3' becomes +2.
							- Meaning, the tree is out of balance.
							- This is also a RR case due to both the unbalanced '3' node and its left child node '5' are right heavy.
							- In this case, a single left rotation on the unbalanced node is enough to restore balance
			- Left-Right Case
				- Definition:
					- A node where the unbalance is discovered to be left heavy and the left child node, is right heavy.
					- A left rotation on the unbalanced child node and a right rotation on the main node restores balance.
				- Figure:
					```
					 Left-Right Case         Left Rotation             Right Rotation
					          |---|                      |---|              |---|
					   _----->| 9 |               _----->| 9 |       _----->| 8 |<-----_
					  |       |---|              |       |---|      |       |---|       |
					  |       -2 BF              |       -2 BF      |       00 BF       |
					|---|                      |---|              |---|               |---|
					| 5 |<--_              _-->| 8 |              | 5 |               | 9 |
					|---|    |            |    |---|              |---|               |---|
					+1 BF    |            |    -1 BF              00 BF               00 BF
					       |---|        |---|
					       | 8 |        | 5 |
					       |---|        |---|
					       00 BF        00 BF
					```
					- Note:
						- In the figure above, when '4' is added, the balance factor of '5' becomes -2.
							- Meaning the tree is unbalanced.
							- This becomes an LR case due to both the unbalanced node '5' being left heavy, and its left child node '3' is right node heavy which is a negative balance factor.
							- A left rotation at node '3', swapping with node '4', and a right rotation at node '5' restores balance in the tree.
				- Figure:
					```
					        Left-Right Case                      Left Rotation                        Right Rotation
					                 |---|                                |---|                            |---|
					          _----->| 8 |<-----_                  _----->| 8 |<-----_              _----->| 6 |<-----_
					         |       |---|       |                |       |---|       |            |       |---|       |
					         |       -2 BF       |                |       -2 BF       |            |       00 BF       |    
					       |---|               |---|            |---|               |---|        |---|               |---|
					   _-->| 5 |<--_           | 9 |        _-->| 6 |<--_           | 9 |    _-->| 5 |           _-->| 8 |<--_
					  |    |---|    |          |---|       |    |---|    |          |---|   |    |---|          |    |---|    |
					  |    +1 BF    |          00 BF       |    -1 BF    |          00 BF   |    -1 BF          |    00 BF    |
					|---|         |---|                  |---|         |---|              |---|               |---|         |---|
					| 4 |         | 6 |<_              _>| 5 |         | 7 |              | 4 |               | 7 |         | 9 |
					|---|         |---| ?              ? |---|         |---|              |---|               |---|         |---|
					00 BF         +1 BF |              | -1 BF         00 BF              00 BF               00 BF         00 BF
					                  |---|          |---|
					                  | 7 |          | 4 |
					                  |---|          |---|
					                  00 BF          00 BF
					```
					- Note
						- In the figure above. as nodes '4', '6' and '7' are added, the balance factor of '8' becomes -2, and its child node, '5' becomes unbalanced with a balance factor of +1.
							- Meaning, the tree is out of balance.
							- This is also a LR case due to both the unbalanced '3' node being left heavy, and its left child node '5' is right heavy.
							- A left rotation on its child node and a right rotation on the main node restores balance to the Tree.
			- Right-Left Case
				- Definition:
					- A node where the unbalance is discovered to be right heavy, and the right child node is left heavy.
					- A right rotation on the unbalanced child node and a left rotation on the main node restores balance.
				- Figure:
					```
					Right-Left Case        Right Rotation             Left Rotation
					|---|               |---|                             |---|
					| 9 |<-----_        | 9 |<-----_               _----->|10 |<-----_
					|---|       |       |---|       |             |       |---|       |
					+2 BF       |       +2 BF       |             |       00 BF       |
					          |---|               |---|         |---|               |---|
					      _-->|13 |               |10 |<--_     | 9 |               |13 |
					     |    |---|               |---|    |    |---|               |---|
					     |    -1 BF               +1 BF    |    00 BF               00 BF
					   |---|                             |---|
					   |10 |                             |13 |
					   |---|                             |---|
					   00 BF                             00 BF
					```
					- Note:
						- In the figure above, when '4' is added, the balance factor of '5' becomes -2.
							- Meaning the tree is unbalanced.
							- This becomes an RL case due to both the unbalanced node '5' being left heavy and its left child node '3' is right node heavy which is a negative balance factor.
							- A left rotation at node '3', swapping with node '4' and a right rotation at node '5' restores balance in the tree.
				- Figure:
					```
					      Left-Right Case                   Left Rotation                          Right Rotation
					          |---|                            |---|                                     |---|
					   _----->|10 |<-----_              _----->|10 |<-----_                       _----->|12 |<-----_
					  |       |---|       |            |       |---|       |                     |       |---|       |
					  |       +2 BF       |            |       +2 BF       |                     |       00 BF       |    
					|---|               |---|        |---|               |---|                 |---|               |---|
					| 9 |           _-->|13 |<--_    | 9 |           _-->|12 |<--_         _-->|10 | --_           |13 |<--_
					|---|          |    |---|    |   |---|          |    |---|    |       |    |---|    |          |---|    |
					00 BF          |    -1 BF    |   00 BF          |    +1 BF    |       |    -1 BF    |          +1 BF    |
					             |---|         |---|              |---|         |---|   |---|         |---|               |---|
					           _>|12 |         |14 |              |11 |         |13 |<_ | 9 |         |11 |               |14 |
					           ? |---|         |---|              |---|         |---| ? |---|         |---|               |---|
					           | -1 BF         00 BF              00 BF         +1 BF | 00 BF         00 BF               00 BF
					         |---|                                                  |---|
					         |11 |                                                  |14 |
					         |---|                                                  |---|
					         00 BF                                                  00 BF
					```
					- Note:
						- In the figure above, as nodes '14', '12' and '11' are added, the balance factor of '10' becomes +2 and its child node, '13' becomes unbalanced with a balance factor of -1.
							- Meaning, the tree is out of balance.
							- This is also a RL case due to both the unbalanced '3\10' node being right heavy, and its left child node '13' is left heavy.
							- A right rotation on its child node and a left rotation on the main node restores balance to the Tree
		- Retracing in AVL Trees
			- Definition:
				- When inserting or deleting nodes, the tree may become unbalanced.
				- In order to know if the tree is unbalanced, the heights must be updated and the balance factors of each ancestor node must be recalculated.
					- This process, is called "retracing" and is done through recursion as the recursive calls propagate back to the root after an insertion and deletion.
					- If any ancestor node is found to have a balance factor outside of the range of -1 to 1, a rotation is performed at that node to restore the tree's balance.
			- Figure:
				```
				           Unbalanced Tree                              Retracing
				                 |---|                                     |---|
				          _----->|10 |<-----_                       _----->|10 |<-----_
				         |       |---|       |                     |       |---|       |
				         |       +1 BF       |                     |       +1 BF       |
				       |---|               |---|                 |---|               |---|
				   _-->| 9 |           _-->|14 |<--_         _-->| 9 |           _-->|14 |<--_
				  |    |---|          |    |---|    |       |    |---|          |    |---|    |
				  |    -1 BF          |    -1 BF    |       |    -1 BF          |    -1 BF    |
				|---|               |---|         |---|   |---|               |---|         |---|
				| 8 |             _>|13 |         |15 |   | 8 |             _>|12 |<_       |15 |
				|---|             ? |---|         |---|   |---|             ? |---| ?       |---|
				00 BF             | -2 BF         00 BF   00 BF             | 00 BF |       00 BF 
				                |---|                                     |---|   |---|
				              _>|12 |                                     |11 |   |13 |
				              ? |---|                                     |---|   |---|
				              | -1 BF                                     00 BF   00 BF
				            |---|
				            |11 |
				            |---|
				            00 BF
				```
				- Note:
					- In the figure above, after node '11' is inserted, the code will retrace, calculating balance factors as it propagates back up towards the root node.
						- When node '13' is reached and the balancing factor of that node became -2, a right rotation is done.
						- Only after a rotation is done, the code will continue to retrace, calculating balancing factors further up on ancestor '14' and '10'.
						- Due to the balancing factors of node '14' and '10' remaining unchanged, they are unaffected by the rotation.
			- Implementation of AVL Trees in Python:
				```
				class TreeNode:
					def __init__(self, data) -> None:
						self.data: int = data
						self.left: TreeNode = None
						self.right: TreeNode = None
						self.height: int = 1
				
					def get_height(node) -> int:
						if not node:
							return 0
						return node.height
	
					def get_balance(node) -> int:
						if not node:
							return 0
						return get_height(node.left) - get_height(node.right)
				
					def right_rotate(y) -> TreeNode:
						x: TreeNode = y.left
						T2: TreeNode = x.right
						x.right = y
						y.left = T2
						y.height = 1 + max(get_height(y.left), get_height(y.right))
						x.height = 1 + max(get_height(x.left), get_height(x.right))
						return x
				
					def left_rotate(y) -> TreeNode:
						y: TreeNode = x.right
						T2: TreeNode = y.left
						y.left = x
						x.right = T2
						x.height = 1 + max(get_height(x.left), get_height(x.right))
						y.height = 1 + max(get_height(y.left), get_height(y.right))
						return y
				
					def insert_node(node, value) -> TreeNode | int:
						if not node:
							return TreeNode(value)
				
						if value < node.data:
							node.left = insert_node(node.left, value)
						elif value > node.data:
							node.right = insert_node(node.right, value)
				
						node.height = 1 + max(get_height(node.left), get_height(node.right))
						balance: int = get_balance(node)
				
						if balance > 1 and get_balance(node.left) >= 0:
							return right_rotate(node)
							
						if balance > 1 and get_balance(node.left) < 0:
							node.left = left_rotate(node.left)
							return right_node(node)
							
						if balance < -1 and get_balance(node.right) <= 0:
							return left_rotate(node)
							
						if balance < -1 and get_balance(node.right) > 0:
							node.left = right_rotate(node.right)
							return rleft_node(node)
							
						return node
				```
				
		- AVL node deleting
			- Definition:
				- When deleting a node that is not a leaf node, the AVL Tree requires the least value in the node, queried through the get_lowest_node() function or found through using in-order traversal.
				- This process is similar to deleting a node in a BST.
				- Deleting a node in a AVL Tree, the same code to restore balance is needed.
			- Sample code:
				```
				def get_lowest_node(node) -> TreeNode:
					current: TreeNode = node
					while current is not None:
						current = current.left
					return current
				
				def delete_node(node, value) -> TreeNode:
					if not node:
						return node
						
					if value < node.data:
						node.left = delete_node(node.left, value)
					elif value > node.data:
						node.right = delete_node(node.right, value)
					else:
						if node.left is None:
							temp: TreeNode = node.right
							node = None
							return temp
						elif node.right is None:
							temp: TreeNode = node.left 
							node = None
							return temp
	
						temp: TreeNode = get_lowest_node(node.right)
						node.data = temp.data
						node.right = delete(node.right, temp.data)
						return node
				```
		
		- Time Complexity in AVL Trees
			- Definition:
				- When looking through an unbalanced BST, the worst case scenario is _O(n)_.
				- But when searching in an AVL Tree, the worst case scenario becomes a constant _O(log n)_.
				- When deleting, searching or inserting, the algorithm will only run through the whole height of the tree.
				- Meaning, by keeping the height of the tree low, algorithms will only have a lower runtime.
				- AVL Trees vs BSTs
					- A BST is not self-balancing, leading to it can becoming very unbalanced.
						- Where the height is nearly the same as the number of nodes, making operations like inserting, deleting or searching very slow,
						- With a time complexity of _O(h)_ = _O(n)_.
					- An AVL Tree however, is self-balancing.
						- Meaning, the height of the tree is kept to a minimum such that operations like inserting, deleting or searching takes only a time complexity of _O(h)_ = _O(log n)_.
				- _O(log n)_
					- In a perfect binary tree, with a height of 4, the number of nodes becomes 1, 2, 4, 8 or 15.
						- The same as 2^0, 2^1, 2^2. 2^3.
					- To get the number of nodes n in a perfect binary tree with a height of 5, it is possible to add the number of nodes together.
						- 2^0 + 2^1 + 2^2 + 2^3 + 2^4 + 2^5 = 63
						- Which is the same as 2^6 - 1 = 63.
					- In general, the formula for the relationship between the height and number of nodes is
						- $2^(h + 1) - 1$
					- Relationship between the height of a Tree and the number of nodes:
						```
									 n = 2(h + 1) - 1
								n + 1 = 2(h + 1)
						log_2(n + 1) = log_2(2^(h + 1))
						log_2(n + 1) = h + 1
									 h = log_2(n + 1) - 1
									 h = log n            #> note that the +1 and -1 are dropped
														     #> due to being insignificant in Computer Science
														     #> when tackling time complexity
						```