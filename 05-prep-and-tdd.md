# Read04
* Big O: Analysis of Algorithm Efficiency.
* Linked Lists.
* What’s a Linked List, Anyway.

### *Big O: Analysis of Algorithm Efficiency*
- Big O(oh) notation is used to describe the efficiency of an algorithm or function(the Worst Case).
- This efficiency evaluated based on 2 factors:
   1) Running Time . 2) Memory Space.
- Four Key Areas for analysis:
- 1)Input Size(n):Input Size refers to the size of the parameter values that are read by the algorithm.The higher this n, the more likely there will be an increase to Running Time and Memory.
- 2)Units of Measurement:To evaluate a function for Time and Space complexity.
- 3)Orders of Growth:We can describe overall efficiency by using (n) and measuring the overall Units of Space and Time required for the given (n). As the value of (n) grows, the Order of Growth represents the increase in Running Time or Memory Space.
- 4)best Case, Worst Case, and Average Case: 
* *Worst Case: The efficiency for the worst possible (n).
* *Best Case: The efficiency for the best possible (n).
* *Average Case: The efficiency for a “typical” or “random”(n).
- Asymptotic Notations:
- Big O(oh): This notation describes the Worst Case for an algorithm. The Order of Growth used represents the upper bounds of Time and Space.
- Big Omega: This notation describes the Best Case for a given algorithm. The Order of Growth used represents the lower bounds of Time and Space.
- Big Theta: This notation describes the Average Case. The Order of Growth used represents the tight bound of Time and Space.

For more details see [Big O: Analysis of Algorithm Efficiency](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/big_oh.html).

### *Linked Lists*
A Linked List is a sequence of Nodes that are connected/linked to each other.
- There are two types of Linked List - Singly and Doubly.
- Singly - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.
- Doubly - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.

For more details [Linked Lists](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html).

### *What’s a Linked List.*
Linked list is linear data structures.which means that there is a sequence and an order to how they are 
constructed and traversed.
- Linear vs non-linear data structures: 
linear :the items in the list in order, or sequentially ,non-linear:items don’t have to be arranged in 
order,non-sequentially.
- Linked list vs Array:
The fundamental difference between arrays and linked lists is that arrays are static data structures, 
while linked lists are dynamic data structures.
- Parts of a linked list:
![part of linked list](https://miro.medium.com/max/1400/1*K0_eV07tJtKQSVGKfP18bw.jpeg)

- Lists for all shapes: 
* Singly linked lists are the simplest type of linked list, based solely on the fact that they only go 
in one direction. There is a single track that we can traverse the list in; we start at the head node, 
and traverse from the root until the last node, which will end at an empty null value.
* Doubly linked lists :there are two references contained within each node: a reference to the next 
node, as well as the previous node.
* Circular linked list :is a little odd in that it doesn’t end with a node pointing to a null value. 
Instead, it has a node that acts as the tail of the list (rather than the conventional head node), and 
the node after the tail node is the beginning of the list. 
- Basic Big O Notation Equations
![Basic Big O Notation Equations](https://miro.medium.com/max/1400/1*FC0XX0-9Vx7yCS0dTS2Zrw.jpeg)
- Inserting elements at the beginning and end of a linked list
![Inserting elements](https://miro.medium.com/max/1400/1*Jy5tjwrMdtpGl2ceq4f94A.jpeg)
- When to use an array versus a linked list
![When to use an array versus a linked list](https://miro.medium.com/max/1400/1*cUehR5S18XSoVLaPNfNzlA.jpeg)

For more details see [What’s a Linked List #1](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d).
and [What’s a Linked List #2](https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996).
