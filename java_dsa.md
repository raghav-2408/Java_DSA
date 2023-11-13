## Here's the Basic syntax and operations for  Data Structures in Java :

## Syntax :
### 1. Arrays:
```java
// Declaration and Initialization
int[] numbers = {1, 2, 3, 4, 5};

// Accessing Elements
int firstElement = numbers[0];

// Array Length
int length = numbers.length;
```

### 2. LinkedList:

```java
// Node Definition
class Node {
    int data;
    Node next;

    public Node(int data) {
        this.data = data;
        this.next = null;
    }
}

// Creating a LinkedList
Node head = new Node(1);
head.next = new Node(2);
```

### 3. Stacks:

```java
// Using Java's Stack Class
import java.util.Stack;

Stack<Integer> stack = new Stack<>();
stack.push(1);
int topElement = stack.pop();
```
### 4. Queues:

```java
// Using Java's Queue Interface
import java.util.LinkedList;
import java.util.Queue;

Queue<Integer> queue = new LinkedList<>();
queue.offer(1);
int frontElement = queue.poll();

```
### 5. Trees (Binary Tree):

```java
// Node Definition
class TreeNode {
    int data;
    TreeNode left, right;

    public TreeNode(int data) {
        this.data = data;
        this.left = this.right = null;
    }
}

// Creating a Binary Tree
TreeNode root = new TreeNode(1);
root.left = new TreeNode(2);
root.right = new TreeNode(3);
```
### 6. HashMap:
```java
// Declaration and Initialization
import java.util.HashMap;

HashMap<String, Integer> map = new HashMap<>();
map.put("key", 1);
int value = map.get("key");
```
### 7. HashSet:

```java
// Using Java's HashSet Class
import java.util.HashSet;

HashSet<Integer> set = new HashSet<>();
set.add(1);
boolean contains = set.contains(1);
```

###  8. Priority Queue:

```java
// Using Java's PriorityQueue Class
import java.util.PriorityQueue;

PriorityQueue<Integer> pq = new PriorityQueue<>();
pq.offer(3);
int smallest = pq.poll();
```
### 9. Doubly Linked List:
```java
// Node Definition
class DoublyNode {
    int data;
    DoublyNode prev, next;

    public DoublyNode(int data) {
        this.data = data;
        this.prev = this.next = null;
    }
}

// Creating a Doubly LinkedList
DoublyNode head = new DoublyNode(1);
head.next = new DoublyNode(2);
head.next.prev = head;
```

## Operations :
### 10. Single Linked List Operations:

```java
// Single Linked List Node Definition
class ListNode {
    int val;
    ListNode next;

    public ListNode(int val) {
        this.val = val;
        this.next = null;
    }
}

// Insertion at the end of a Linked List
ListNode insertAtEnd(ListNode head, int val) {
    ListNode newNode = new ListNode(val);
    if (head == null) {
        return newNode;
    }
    ListNode current = head;
    while (current.next != null) {
        current = current.next;
    }
    current.next = newNode;
    return head;
}

// Deletion by Value from a Linked List
ListNode deleteNode(ListNode head, int val) {
    if (head == null) {
        return null;
    }
    if (head.val == val) {
        return head.next;
    }
    ListNode current = head;
    while (current.next != null && current.next.val != val) {
        current = current.next;
    }
    if (current.next != null) {
        current.next = current.next.next;
    }
    return head;
}
```

### 11. Circular List:
```java
// Circular Linked List Node Definition
class CircularListNode {
    int data;
    CircularListNode next;

    public CircularListNode(int data) {
        this.data = data;
        this.next = null;
    }
}

// Insertion into a Circular Linked List
CircularListNode insertIntoCircularList(CircularListNode head, int data) {
    CircularListNode newNode = new CircularListNode(data);
    if (head == null) {
        newNode.next = newNode;
        return newNode;
    }
    CircularListNode last = head;
    while (last.next != head) {
        last = last.next;
    }
    last.next = newNode;
    newNode.next = head;
    return head;
}
```

### 12. Tree Traversals Operations:

```java
// Tree Node Definition
class TreeNode {
    int data;
    TreeNode left, right;

    public TreeNode(int data) {
        this.data = data;
        this.left = this.right = null;
    }
}

// Preorder Traversal
void preorderTraversal(TreeNode root) {
    if (root != null) {
        System.out.print(root.data + " ");
        preorderTraversal(root.left);
        preorderTraversal(root.right);
    }
}

// Inorder Traversal
void inorderTraversal(TreeNode root) {
    if (root != null) {
        inorderTraversal(root.left);
        System.out.print(root.data + " ");
        inorderTraversal(root.right);
    }
}

// Postorder Traversal
void postorderTraversal(TreeNode root) {
    if (root != null) {
        postorderTraversal(root.left);
        postorderTraversal(root.right);
        System.out.print(root.data + " ");
    }
}
```

### 13. Push, Pop, and Append Operations:

```java
// Stack Implementation (Push and Pop)
import java.util.Stack;

Stack<Integer> stack = new Stack<>();
stack.push(1);
int poppedElement = stack.pop();

// Queue Implementation (Enqueue and Dequeue)
import java.util.LinkedList;
import java.util.Queue;

Queue<Integer> queue = new LinkedList<>();
queue.offer(1);
int dequeuedElement = queue.poll();

// Append Operation in LinkedList
void appendToLinkedList(ListNode head, int val) {
    ListNode newNode = new ListNode(val);
    if (head == null) {
        head = newNode;
        return;
    }
    ListNode current = head;
    while (current.next != null) {
        current = current.next;
    }
    current.next = newNode;
}
```