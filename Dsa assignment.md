# DSA-assignment- 
//1- Write a program to declare and initialize a 1D array.

#include <stdio.h>



int main() {

    int arr[5] = {10, 20, 30, 40, 50}; // declaration + initialization

    int i;

    printf("Array elements:\n");

    for (i = 0; i < 5;i++)

        printf("%d ", arr[i]);

    printf("\n");

    return 0;

}



// Output: Array elements:

//10 20 30 40 50



//2. Input and display elements of a 1D array.

#include<stdio.h>

int main() {

    int n, i;

    printf("Enter number of elements: ");

    if (scanf("%d", &n) != 1 || n <= 0) return 0;

    int arr[n];

    printf("Enter %d elements:\n", n);

    for (i = 0; i < n; i++) scanf("%d", &arr[i]);

    printf("You entered:\n");

    for (i = 0; i < n; i++) printf("%d ", arr[i]);

    printf("\n");

    return 0;

}

// Output:Enter number of elements: 5

//Enter 5 elements:

//1

//2

//3

//4

//5

//You entered:

//1 2 3 4 5

// 3. Find the largest and smallest element in an array.

#include <stdio.h>



int main() {

    int n, i;

    printf("Enter number of elements: ");

    if (scanf("%d", &n) != 1 || n <= 0) return 0;

    int arr[n];

    for (i = 0; i < n; i++) scanf("%d", &arr[i]);

    int max = arr[0], min = arr[0];

    for (i = 1; i < n; i++) {

        if (arr[i] > max) max = arr[i];

        if (arr[i] < min) min = arr[i];

    }

    printf("Largest = %d\nSmallest = %d\n", max, min);

    return 0;

}

//Output: Enter number of elements: 5

//10

//20

//55

//65

//25

//Largest = 65

//Smallest = 10

// 4.Calculate sum and average of elements in an array.

#include <stdio.h>



Int main() {

    Int n, i;

    Printf(“Enter number of elements: “);

    If (scanf(“%d”, &n) != 1 || n <= 0) return 0;

    Int arr[n];

    Long long sum = 0;

    For (i = 0; i < n; i++) {

        Scanf(“%d”, &arr[i]);

        Sum += arr[i];

    }

    Double avg = (double)sum / n;

    Printf(“Sum = %lld\nAverage = %.2f\n”, sum, avg);

    Return 0;

}

//Output:Enter number of elements: 5

//10

//20

//30

//40

//50

//Sum = 150

//Average = 30.00 



// 5. Insert an element at a given position in an array.

#include <stdio.h>



Int main() {

    Int n, pos, x, i;

    Printf(“Enter number of elements: “);

    If (scanf(“%d”, &n) != 1 || n < 0) return 0;

    Int arr[n+1]; // allow one extra

    Printf(“Enter %d elements:\n”, n);

    For (i = 0; i < n; i++) scanf(“%d”, &arr[i]);

    Printf(“Enter element to insert: “);

    Scanf(“%d”, &x);

    Printf(“Enter position (0 to %d): “, n);

    Scanf(“%d”, &pos);

    If (pos < 0 || pos > n) {

        Printf(“Invalid position\n”);

        Return 0;

    }

    For (i = n; i > pos; i--) arr[i] = arr[i-1];

    Arr[pos] = x;

    N = n + 1;

    Printf(“Array after insertion:\n”);

    For (i = 0; i < n; i++) printf(“%d “, arr[i]);

    Printf(“\n”);

    Return 0;

}

//OutputEnter number of elements: 5

//Enter 5 elements:

//10

//20

//30

//40

//50

//Enter element to insert: 78

//Enter position (0 to 5): 4

//Array after insertion:

//10 20 30 40 78 50 



// 6. Delete an element from an array.

#include <stdio.h>



Int main() {

    Int n, pos, i;

    Printf(“Enter number of elements: “);

    If (scanf(“%d”, &n) != 1 || n <= 0) return 0;

    Int arr[n];

    Printf(“Enter %d elements:\n”, n);

    For (i = 0; i < n; i++) scanf(“%d”, &arr[i]);

    Printf(“Enter position to delete (0 to %d): “, n-1);

    Scanf(“%d”, &pos);

    If (pos < 0 || pos >= n) {

        Printf(“Invalid position\n”);

        Return 0;

    }

    For (i = pos; i < n-1; i++) arr[i] = arr[i+1];

    N = n – 1;

    Printf(“Array after deletion:\n”);

    For (i = 0; i < n; i++) printf(“%d “, arr[i]);

    Printf(“\n”);

    Return 0;

}



//OutputEnter number of elements: 5

//Enter 5 elements:

//10

//20

//30

//40

//50

//Enter position to delete (0 to 4): 4

//Array after deletion:

//10 20 30 40 

// 7. Merge two arrays into one.

#include <stdio.h>



int main() {

    int n1, n2, i;

    printf("Enter size of first array: ");

    if (scanf("%d", &n1) != 1 || n1 < 0) return 0;

    int a[n1];

    printf("Enter %d elements for first array:\n", n1);

    for (i = 0; i < n1; i++) scanf("%d", &a[i]);



    printf("Enter size of second array: ");

    if (scanf("%d", &n2) != 1 || n2 < 0) return 0;

    int b[n2];

    printf("Enter %d elements for second array:\n", n2);

    for (i = 0; i < n2; i++) scanf("%d", &b[i]);



    int merged[n1 + n2];

    for (i = 0; i < n1; i++) merged[i] = a[i];

    for (i = 0; i < n2; i++) merged[n1 + i] = b[i];



    printf("Merged array:\n");

    for (i = 0; i < n1 + n2; i++) printf("%d ", merged[i]);

    printf("\n");

    return 0;

}

//Output:Enter size of first array: 5

//Enter 5 elements for first array:

//10

//20

//30

//40

//50

//Enter size of second array: 5

//Enter 5 elements for second array:

//60

//70

//80

//90

//100

//Merged array:

//10 20 30 40 50 60 70 80 90 100

// 8. Add two matrices.

#include <stdio.h>



int main() {

    int r, c, i, j;

    printf("Enter rows and columns: ");

    if (scanf("%d %d", &r, &c) != 2 || r <= 0 || c <= 0) return 0;

    int A[r][c], B[r][c], C[r][c];

    printf("Enter elements of matrix A:\n");

    for (i = 0; i < r; i++)

        for (j = 0; j < c; j++)

            scanf("%d", &A[i][j]);

    printf("Enter elements of matrix B:\n");

    for (i = 0; i < r; i++)

        for (j = 0; j < c; j++)

            scanf("%d", &B[i][j]);

    for (i = 0; i < r; i++)

        for (j = 0; j < c; j++)

            C[i][j] = A[i][j] + B[i][j];

    printf("Sum matrix:\n");

    for (i = 0; i < r; i++) {

        for (j = 0; j < c; j++) printf("%d ", C[i][j]);

        printf("\n");

    }

    return 0;

}

// Output:Enter rows and columns: 2

//2

//Enter elements of matrix A:

//10

//20

//30

//40

//Enter elements of matrix B:

//40

//30

//20

//10

//Sum matrix:

//50 50 

//50 50

//9. Subtract two matrices.

#include <stdio.h>



int main() {

    int r, c, i, j;

    printf("Enter rows and columns: ");

    if (scanf("%d %d", &r, &c) != 2 || r <= 0 || c <= 0) return 0;

    int A[r][c], B[r][c], C[r][c];

    printf("Enter elements of matrix A:\n");

    for (i = 0; i < r; i++)

        for (j = 0; j < c; j++)

            scanf("%d", &A[i][j]);

    printf("Enter elements of matrix B:\n");

    for (i = 0; i < r; i++)

        for (j = 0; j < c; j++)

            scanf("%d", &B[i][j]);

    for (i = 0; i < r; i++)

        for (j = 0; j < c; j++)

            C[i][j] = A[i][j] - B[i][j];

    printf("Difference matrix (A - B):\n");

    for (i = 0; i < r; i++) {

        for (j = 0; j < c; j++) printf("%d ", C[i][j]);

        printf("\n");

    }

    return 0;

}

// Output:Enter rows and columns: 2

//2

//Enter elements of matrix A:

//10

//20

//30

//40

//Enter elements of matrix B:

//10

//20

//30

//40

//Difference matrix (A - B):

//0 0 

//0 0 



//10. Multiply two matrices.

#include <stdio.h>

int main() {

    int r1, c1, r2, c2, i, j, k;

    printf("Enter rows and columns of matrix A: ");

    if (scanf("%d %d", &r1, &c1) != 2) return 0;

    printf("Enter rows and columns of matrix B: ");

    if (scanf("%d %d", &r2, &c2) != 2) return 0;

    if (c1 != r2) {

        printf("Matrices cannot be multiplied (c1 != r2)\n");

        return 0;

    }

    int A[r1][c1], B[r2][c2], C[r1][c2];

    printf("Enter elements of A (%dx%d):\n", r1, c1);

    for (i = 0; i < r1; i++)

        for (j = 0; j < c1; j++)

            scanf("%d", &A[i][j]);



    printf("Enter elements of B (%dx%d):\n", r2, c2);

    for (i = 0; i < r2; i++)

        for (j = 0; j < c2; j++)

            scanf("%d", &B[i][j]);



    // initialize C

    for (i = 0; i < r1; i++)

        for (j = 0; j < c2; j++)

            C[i][j] = 0;



    for (i = 0; i < r1; i++) {

        for (j = 0; j < c2; j++) {

            for (k = 0; k < c1; k++)

                C[i][j] += A[i][k] * B[k][j];

        }

    }



    printf("Product matrix (%dx%d):\n", r1, c2);

    for (i = 0; i < r1; i++) {

        for (j = 0; j < c2; j++) printf("%d ", C[i][j]);

        printf("\n");

    }

    return 0;

}

// Output:Enter rows and columns of matrix A: 2

//2

//Enter rows and columns of matrix B: 2

//2

//Enter elements of A (2x2):

//1

//2

//3

//4

//Enter elements of B (2x2):

//4

//3

//2

//1

//Product matrix (2x2):

//8 5 

//20 13 

//11. Define stack structure and demonstrate push/pop operations

#include <stdio.h>

#define MAX 5



Struct Stack {

    Int items[MAX];

    Int top;

};



Void push(struct Stack *s, int value) {

    If (s->top == MAX – 1)

        Printf(“Stack Overflow!\n”);

    Else

        s->items[++(s->top)] = value;

}



Int pop(struct Stack *s) {

    If (s->top == -1) {

        Printf(“Stack Underflow!\n”);

        Return -1;

    }

    Return s->items[(s->top)--];

}



Int main() {

    Struct Stack s;

    s.top = -1;

    push(&s, 10);

    push(&s, 20);

    push(&s, 30);

    printf(“Popped element: %d\n”, pop(&s));

    printf(“Current Stack:\n”);

    for (int i = s.top; i >= 0; i--)

        printf(“%d\n”, s.items[i]);

    return 0;

}

//Output:Popped element: 30

//Current Stack:

//20

//10 



//12. Implement stack using array.

#include <stdio.h>

#define MAX 5



int stack[MAX], top = -1;



void push(int val) {

    if (top == MAX - 1)

        printf("Stack Overflow!\n");

    else

        stack[++top] = val;

}



void pop() {

    if (top == -1)

        printf("Stack Underflow!\n");

    else

        printf("Popped: %d\n", stack[top--]);

}



void display() {

    if (top == -1)

        printf("Stack is empty.\n");

    else {

        printf("Stack elements:\n");

        for (int i = top; i >= 0; i--)

            printf("%d\n", stack[i]);

    }

}



int main() {

    push(10);

    push(20);

    push(30);

    display();

    pop();

    display();

    return 0;

}

//Stack elements:

//30

//20

//10

//Popped: 30

//Stack elements:

//20

//10

//13. Implement stack using linked list.

#include <stdio.h>

#include <stdlib.h>



Struct Node {

    Int data;

    Struct Node *next;

};



Struct Node *top = NULL;



Void push(int val) {

    Struct Node *newNode = (struct Node *)malloc(sizeof(struct Node));

    newNode->data = val;

    newNode->next = top;

    top = newNode;

}



Void pop() {

    If (top == NULL)

        Printf(“Stack Underflow!\n”);

    Else {

        Printf(“Popped: %d\n”, top->data);

        Struct Node *temp = top;

        Top = top->next;

        Free(temp);

    }

}



Void display() {

    Struct Node *ptr = top;

    If (ptr == NULL)

        Printf(“Stack is empty.\n”);

    Else {

        Printf(“Stack elements:\n”);

        While (ptr != NULL) {

            Printf(“%d\n”, ptr->data);

            Ptr = ptr->next;

        }

    }

}



Int main() {

    Push(10);

    Push(20);

    Push(30);

    Display();

    Pop();

    Display();

    Return 0;

}

//Output:Stack elements:

//30

//20

//10

//Popped: 30

//Stack elements:

//20

//10

//14. Check stack overflow and underflow conditions.



#include <stdio.h>

#define MAX 3



int stack[MAX], top = -1;



void push(int val) {

    if (top == MAX - 1)

        printf("Overflow: Stack is full!\n");

    else

        stack[++top] = val;

}



void pop() {

    if (top == -1)

        printf("Underflow: Stack is empty!\n");

    else

        printf("Popped: %d\n", stack[top--]);

}



int main() {

    pop(); // underflow

    push(10);

    push(20);

    push(30);

    push(40); // overflow

    return 0;

}

//output: Underflow: Stack is empty!

//Overflow: Stack is full! 



//15. Reverse a string using stack.



#include <stdio.h>

#include <string.h>

#define MAX 100



Int main() {

    Char str[MAX], stack[MAX];

    Int top = -1;

    Printf(“Enter a string: “);

    Scanf(“%s”, str);

    Int n = strlen(str);

    For (int i = 0; i < n; i++)

        Stack[++top] = str[i];

    Printf(“Reversed string: “);

    While (top != -1)

        Printf(“%c”, stack[top--]);

    Printf(“\n”);

    Return 0;

}

//Output:Enter a string: DSA

//Reversed string: ASD

//16. Define and demonstrate basic queue operations (enqueue/dequeue).

#include <stdio.h>

#define MAX 5



int queue[MAX], front = -1, rear = -1;



void enqueue(int val) {

    if (rear == MAX - 1)

        printf("Queue Overflow!\n");

    else {

        if (front == -1) front = 0;

        queue[++rear] = val;

    }

}



void dequeue() {

    if (front == -1 || front > rear)

        printf("Queue Underflow!\n");

    else

        printf("Dequeued: %d\n", queue[front++]);

}



void display() {

    if (front == -1 || front > rear)

        printf("Queue is empty.\n");

    else {

        printf("Queue elements: ");

        for (int i = front; i <= rear; i++)

            printf("%d ", queue[i]);

        printf("\n");

    }

}



int main() {

    enqueue(10);

    enqueue(20);

    enqueue(30);

    display();

    dequeue();

    display();

    return 0;

}

// Output: Queue elements: 10 20 30 

//Dequeued: 10

//Queue elements: 20 30 



//17. Implement queue using array.

#include <stdio.h>

#define MAX 5



Int queue[MAX], front = -1, rear = -1;



Void enqueue(int val) {

    If (rear == MAX – 1)

        Printf(“Overflow!\n”);

    Else {

        If (front == -1) front = 0;

        Queue[++rear] = val;

    }

}



Int dequeue() {

    If (front == -1 || front > rear) {

        Printf(“Underflow!\n”);

        Return -1;

    }

    Return queue[front++];

}



Void display() {

    If (front == -1 || front > rear)

        Printf(“Queue is empty.\n”);

    Else {

        Printf(“Queue: “);

        For (int i = front; i <= rear; i++)

            Printf(“%d “, queue[i]);

        Printf(“\n”);

    }

}



Int main() {

    Enqueue(5);

    Enqueue(10);

    Enqueue(15);

    Display();

    Printf(“Dequeued: %d\n”, dequeue());

    Display();

    Return 0;

}

//Queue: 5 10 15 

//Dequeued: 5

//Queue: 10 15 



//18. Implement queue using linked

#include <stdio.h>

#include <stdlib.h>



struct Node {

    int data;

    struct Node *next;

};

struct Node *front = NULL, *rear = NULL;



void enqueue(int val) {

    struct Node *newNode = (struct Node *)malloc(sizeof(struct Node));

    newNode->data = val;

    newNode->next = NULL;

    if (rear == NULL)

        front = rear = newNode;

    else {

        rear->next = newNode;

        rear = newNode;

    }

}



void dequeue() {

    if (front == NULL)

        printf("Queue Underflow!\n");

    else {

        printf("Dequeued: %d\n", front->data);

        struct Node *temp = front;

        front = front->next;

        if (front == NULL) rear = NULL;

        free(temp);

    }

}



void display() {

    struct Node *ptr = front;

    if (ptr == NULL)

        printf("Queue is empty.\n");

    else {

        printf("Queue elements: ");

        while (ptr != NULL) {

            printf("%d ", ptr->data);

            ptr = ptr->next;

        }

        printf("\n");

    }

}



int main() {

    enqueue(10);

    enqueue(20);

    enqueue(30);

    display();

    dequeue();

    display();

    return 0;

}

//Output:Queue elements: 10 20 30 

//Dequeued: 10

//Queue elements: 20 30

//19. Implement circular queue using array.



#include <stdio.h>

#define MAX 5



Int queue[MAX];

Int front = -1, rear = -1;



Void enqueue(int val) {

    If ((rear + 1) % MAX == front)

        Printf(“Circular Queue Overflow!\n”);

    Else {

        If (front == -1) front = 0;

        Rear = (rear + 1) % MAX;

        Queue[rear] = val;

    }

}



Void dequeue() {

    If (front == -1)

        Printf(“Circular Queue Underflow!\n”);

    Else if (front == rear)

        Front = rear = -1;

    Else

        Front = (front + 1) % MAX;

}



Void display() {

    If (front == -1) {

        Printf(“Queue is empty.\n”);

        Return;

    }

    Printf(“Circular Queue: “);

    Int i = front;

    While (1) {

        Printf(“%d “, queue[i]);

        If (i == rear) break;

        I = (i + 1) % MAX;

    }

    Printf(“\n”);

}



Int main() {

    Enqueue(10);

    Enqueue(20);

    Enqueue(30);

    Enqueue(40);

    Display();

    Dequeue();

    Display();

    Enqueue(50);

    Display();

    Return 0;

}

//output:Circular Queue: 10 20 30 40 

//Circular Queue: 20 30 40 

//Circular Queue: 20 30 40 50 

//20. Implement double-ended queue (Deque).



#include <stdio.h>

#define MAX 5



int deque[MAX];

int front = -1, rear = -1;



void insertFront(int val) {

    if ((front == 0 && rear == MAX - 1) || (front == rear + 1))

        printf("Deque Overflow!\n");

    else if (front == -1)

        front = rear = 0;

    else if (front == 0)

        front = MAX - 1;

    else

        front--;

    deque[front] = val;

}



void insertRear(int val) {

    if ((front == 0 && rear == MAX - 1) || (front == rear + 1))

        printf("Deque Overflow!\n");

    else if (rear == -1)

        front = rear = 0;

    else if (rear == MAX - 1)

        rear = 0;

    else

        rear++;

    deque[rear] = val;

}



void deleteFront() {

    if (front == -1)

        printf("Deque Underflow!\n");

    else if (front == rear)

        front = rear = -1;

    else if (front == MAX - 1)

        front = 0;

    else

        front++;

}



void deleteRear() {

    if (rear == -1)

        printf("Deque Underflow!\n");

    else if (front == rear)

        front = rear = -1;

    else if (rear == 0)

        rear = MAX - 1;

    else

        rear--;

}



void display() {

    if (front == -1) {

        printf("Deque is empty.\n");

        return;

    }

    printf("Deque elements: ");

    int i = front;

    while (1) {

        printf("%d ", deque[i]);

        if (i == rear) break;

        i = (i + 1) % MAX;

    }

    printf("\n");

}



int main() {

    insertRear(10);

    insertRear(20);

    insertFront(5);

    display();

    deleteRear();

    display();

    deleteFront();

    display();

    return 0;

}

//Output  Deque elements: 5 10 20 

//Deque elements: 5 10 

//Deque elements: 10 

//21. Implement a Priority Queue using an array.

#include <stdio.h>

#define MAX 10



struct {

    int data;

    int priority;

} pq[MAX];



int size = 0;



void enqueue(int data, int priority) {

    if (size == MAX) {

        printf("Priority Queue Overflow!\n");

        return;

    }

    pq[size].data = data;

    pq[size].priority = priority;

    size++;

}



void dequeue() {

    if (size == 0) {

        printf("Priority Queue Underflow!\n");

        return;

    }

    int highest = 0;

    for (int i = 1; i < size; i++) {

        if (pq[i].priority < pq[highest].priority)

            highest = i;

    }

    printf("Dequeued element: %d (Priority: %d)\n", pq[highest].data, pq[highest].priority);

    for (int i = highest; i < size - 1; i++)

        pq[i] = pq[i + 1];

    size--;

}



void display() {

    if (size == 0) {

        printf("Queue empty!\n");

        return;

    }

    printf("Priority Queue elements:\n");

    for (int i = 0; i < size; i++)

        printf("Data: %d | Priority: %d\n", pq[i].data, pq[i].priority);

}



int main() {

    enqueue(10, 2);

    enqueue(5, 1);

    enqueue(15, 3);

    display();

    dequeue();

    display();

    return 0;

}

//Output:Priority Queue elements:

//Data: 10 | Priority: 2

//Data: 5 | Priority: 1

//Data: 15 | Priority: 3

//Dequeued element: 5 (Priority: 1)

//Priority Queue elements:

//Data: 10 | Priority: 2

//Data: 15 | Priority: 3

//22. Simulate Queue using two Stacks.



#include <stdio.h>

#define MAX 10



int stack1[MAX], stack2[MAX];

int top1 = -1, top2 = -1;



void push1(int val) { stack1[++top1] = val; }

void push2(int val) { stack2[++top2] = val; }

int pop1() { return stack1[top1--]; }

int pop2() { return stack2[top2--]; }



void enqueue(int val) {

    push1(val);

    printf("%d enqueued\n", val);

}



void dequeue() {

    if (top1 == -1 && top2 == -1) {

        printf("Queue Empty!\n");

        return;

    }

    if (top2 == -1) {

        while (top1 != -1)

            push2(pop1());

    }

    printf("%d dequeued\n", pop2());

}



int main() {

    enqueue(10);

    enqueue(20);

    enqueue(30);

    dequeue();

    dequeue();

    enqueue(40);

    dequeue();

    return 0;

}

//output:10 enqueued

//20 enqueued

//30 enqueued

//10 dequeued

//20 dequeued

//40 enqueued

//30 dequeued 



//23. Implement Overflow and Underflow in Queue.



#include <stdio.h>

#define MAX 3



Int queue[MAX], front = -1, rear = -1;



Void enqueue(int val) {

    If (rear == MAX – 1)

        Printf(“Overflow! Queue full.\n”);

    Else {

        If (front == -1) front = 0;

        Queue[++rear] = val;

    }

}



Void dequeue() {

    If (front == -1 || front > rear)

        Printf(“Underflow! Queue empty.\n”);

    Else

        Printf(“Dequeued: %d\n”, queue[front++]);

}



Int main() {

    Dequeue();

    Enqueue(10);

    Enqueue(20);

    Enqueue(30);

    Enqueue(40);

    Dequeue();

    Return 0;

}

// Output:Underflow! Queue empty.

//Overflow! Queue full.

//Dequeued: 10



//24. Create and display a singly linked list.



#include <stdio.h>

#include <stdlib.h>



Struct Node {

    Int data;

    Struct Node *next;

};



Int main() {

    Struct Node *head = NULL, *temp, *newNode;

    Int n, data;



    Printf(“Enter number of nodes: “);

    Scanf(“%d”, &n);



    For (int i = 0; i < n; i++) {

        newNode = (struct Node *)malloc(sizeof(struct Node));

        printf(“Enter data for node %d: “, i + 1);

        scanf(“%d”, &data);

        newNode->data = data;

        newNode->next = NULL;

        if (head == NULL)

            head = temp = newNode;

        else {

            temp->next = newNode;

            temp = newNode;

        }

    }



    Printf(“Linked List: “);

    Temp = head;

    While (temp != NULL) {

        Printf(“%d -> “, temp->data);

        Temp = temp->next;

    }

    Printf(“NULL\n”);

    Return 0;

}

//Output: Enter number of nodes: 2

//Enter data for node 1: 56

//Enter data for node 2: 54

//Linked List: 56 -> 54 -> NULL

//25. Insert a node at the beginning of a linked list.



#include <stdio.h>

#include <stdlib.h>



struct Node {

    int data;

    struct Node *next;

};



void insertAtBeginning(struct Node **head, int data) {

    struct Node *newNode = (struct Node *)malloc(sizeof(struct Node));

    newNode->data = data;

    newNode->next = *head;

    *head = newNode;

}



void display(struct Node *head) {

    while (head != NULL) {

        printf("%d -> ", head->data);

        head = head->next;

    }

    printf("NULL\n");

}



int main() {

    struct Node *head = NULL;

    insertAtBeginning(&head, 10);

    insertAtBeginning(&head, 20);

    insertAtBeginning(&head, 30);

    display(head);

    return 0;

}

//Output:30 -> 20 -> 10 -> NULL 

//26. Insert a node at the end of a linked list.



#include <stdio.h>

#include <stdlib.h>



Struct Node {

    Int data;

    Struct Node *next;

};



Void insertAtEnd(struct Node **head, int data) {

    Struct Node *newNode = (struct Node *)malloc(sizeof(struct Node));

    newNode->data = data;

    newNode->next = NULL;

    if (*head == NULL)

        *head = newNode;

    Else {

        Struct Node *temp = *head;

        While (temp->next != NULL)

            Temp = temp->next;

        Temp->next = newNode;

    }

}



Void display(struct Node *head) {

    While (head != NULL) {

        Printf(“%d -> “, head->data);

        Head = head->next;

    }

    Printf(“NULL\n”);

}



Int main() {

    Struct Node *head = NULL;

    insertAtEnd(&head, 10);

    insertAtEnd(&head, 20);

    insertAtEnd(&head, 30);

    display(head);

    return 0;

}

//Output: 10 -> 20 -> 30 -> NULL



//27. Insert a node at any position in a linked list.



#include <stdio.h>

#include <stdlib.h>



Struct Node {

    Int data;

    Struct Node *next;

};



Void insertAtPosition(struct Node **head, int data, int pos) {

    Struct Node *newNode = (struct Node *)malloc(sizeof(struct Node));

    newNode->data = data;



    if (pos == 1) {

        newNode->next = *head;

        *head = newNode;

        Return;

    }



    Struct Node *temp = *head;

    For (int i = 1; temp != NULL && i < pos – 1; i++)

        Temp = temp->next;



    If (temp == NULL) {

        Printf(“Invalid position!\n”);

        Return;

    }



    newNode->next = temp->next;

    temp->next = newNode;

}



Void display(struct Node *head) {

    While (head != NULL) {

        Printf(“%d -> “, head->data);

        Head = head->next;

    }

    Printf(“NULL\n”);

}



Int main() {

    Struct Node *head = NULL;

    insertAtPosition(&head, 10, 1);

    insertAtPosition(&head, 20, 2);

    insertAtPosition(&head, 15, 2);

    display(head);

    return 0;

}

//output:10 -> 15 -> 20 -> NULL



//28. Delete a node from the beginning of a linked list.



#include <stdio.h>

#include <stdlib.h>



Struct Node {

    Int data;

    Struct Node *next;

};



Void deleteFromBeginning(struct Node **head) {

    If (*head == NULL) {

        Printf(“List is empty.\n”);

        Return;

    }

    Struct Node *temp = *head;

    *head = (*head)->next;

    Free(temp);

}



Void display(struct Node *head) {

    While (head != NULL) {

        Printf(“%d -> “, head->data);

        Head = head->next;

    }

    Printf(“NULL\n”);

}



Int main() {

    Struct Node *head = NULL;

    Head = malloc(sizeof(struct Node));

    Head->data = 10;

    Head->next = malloc(sizeof(struct Node));

    Head->next->data = 20;

    Head->next->next = NULL;



    Display(head);

    deleteFromBeginning(&head);

    display(head);

    return 0;

}

//Output:10 -> 20 -> NULL

//20 -> NULL

//29. Delete a node from the end of a linked list.



#include <stdio.h>

#include <stdlib.h>



Struct Node {

    Int data;

    Struct Node *next;

};



Void deleteFromEnd(struct Node **head) {

    If (*head == NULL)

        Printf(“List empty.\n”);

    Else if ((*head)->next == NULL) {

        Free(*head);

        *head = NULL;

    } else {

        Struct Node *temp = *head;

        While (temp->next->next != NULL)

            Temp = temp->next;

        Free(temp->next);

        Temp->next = NULL;

    }

}



Void display(struct Node *head) {

    While (head != NULL) {

        Printf(“%d -> “, head->data);

        Head = head->next;

    }

    Printf(“NULL\n”);

}



Int main() {

    Struct Node *head = NULL;

    Head = malloc(sizeof(struct Node));

    Head->data = 10;

    Head->next = malloc(sizeof(struct Node));

    Head->next->data = 20;

    Head->next->next = NULL;



    Display(head);

    deleteFromEnd(&head);

    display(head);

    return 0;

}

//10 -> 20 -> NULL

//10 -> NULL

//30. Delete a node from any position in a linked list.



#include <stdio.h>

#include <stdlib.h>



Struct Node {

    Int data;

    Struct Node *next;

};



Void deleteAtPosition(struct Node **head, int pos) {

    If (*head == NULL) {

        Printf(“List empty.\n”);

        Return;

    }

    Struct Node *temp = *head;



    If (pos == 1) {

        *head = temp->next;

        Free(temp);

        Return;

    }



    For (int i = 1; temp != NULL && i < pos – 1; i++)

        Temp = temp->next;



    If (temp == NULL || temp->next == NULL) {

        Printf(“Invalid position!\n”);

        Return;

    }



    Struct Node *del = temp->next;

    Temp->next = del->next;

    Free(del);

}



Void display(struct Node *head) {

    While (head != NULL) {

        Printf(“%d -> “, head->data);

        Head = head->next;

    }

    Printf(“NULL\n”);

}



Int main() {

    Struct Node *head = NULL;

    Struct Node *node1 = malloc(sizeof(struct Node));

    Struct Node *node2 = malloc(sizeof(struct Node));

    Struct Node *node3 = malloc(sizeof(struct Node));



    Node1->data = 10; node1->next = node2;

    Node2->data = 20; node2->next = node3;

    Node3->data = 30; node3->next = NULL;

    Head = node1;



    Display(head);

    deleteAtPosition(&head, 2);

    display(head);

    return 0;

}

// Output: 10 -> 20 -> 30 -> NULL

//10 -> 30 -> NULL

//31. Search an element in a linked list



#include <stdio.h>

#include <stdlib.h>



Struct Node {

    Int data;

    Struct Node *next;

};



Void search(struct Node *head, int key) {

    Int pos = 1;

    While (head != NULL) {

        If (head->data == key) {

            Printf(“Element %d found at position %d\n”, key, pos);

            Return;

        }

        Head = head->next;

        Pos++;

    }

    Printf(“Element %d not found in the list.\n”, key);

}



Int main() {

    Struct Node *head = NULL, *node1, *node2, *node3;



    Node1 = malloc(sizeof(struct Node));

    Node2 = malloc(sizeof(struct Node));

    Node3 = malloc(sizeof(struct Node));



    Node1->data = 10; node1->next = node2;

    Node2->data = 20; node2->next = node3;

    Node3->data = 30; node3->next = NULL;

    Head = node1;



    Search(head, 20);

    Search(head, 40);

    Return 0;

}

// Output: Element 20 found at position 2

//Element 40 not found in the list.

//32. Count the number of nodes in a linked list



#include <stdio.h>

#include <stdlib.h>



Struct Node {

    Int data;

    Struct Node *next;

};



Int countNodes(struct Node *head) {

    Int count = 0;

    While (head != NULL) {

        Count++;

        Head = head->next;

    }

    Return count;

}



Int main() {

    Struct Node *head = NULL, *node1, *node2, *node3;

    Node1 = malloc(sizeof(struct Node));

    Node2 = malloc(sizeof(struct Node));

    Node3 = malloc(sizeof(struct Node));



    Node1->data = 10; node1->next = node2;

    Node2->data = 20; node2->next = node3;

    Node3->data = 30; node3->next = NULL;

    Head = node1;



    Printf(“Total nodes: %d\n”, countNodes(head));

    Return 0;

}

//Output:Total nodes: 3



//33. Reverse a linked list



#include <stdio.h>

#include <stdlib.h>



struct Node {

    int data;

    struct Node *next;

};



void reverse(struct Node **head) {

    struct Node *prev = NULL, *current = *head, *next = NULL;

    while (current != NULL) {

        next = current->next;

        current->next = prev;

        prev = current;

        current = next;

    }

    *head = prev;

}



void display(struct Node *head) {

    while (head != NULL) {

        printf("%d -> ", head->data);

        head = head->next;

    }

    printf("NULL\n");

}



int main() {

    struct Node *head = NULL, *node1, *node2, *node3;

    node1 = malloc(sizeof(struct Node));

    node2 = malloc(sizeof(struct Node));

    node3 = malloc(sizeof(struct Node));



    node1->data = 10; node1->next = node2;

    node2->data = 20; node2->next = node3;

    node3->data = 30; node3->next = NULL;

    head = node1;



    printf("Original List: ");

    display(head);



    reverse(&head);

    printf("Reversed List: ");

    display(head);

    return 0;

}

//Output: Original List: 10 -> 20 -> 30 -> NULL

//Reversed List: 30 -> 20 -> 10 -> NULL 



//34. Create a doubly linked list and display it



#include <stdio.h>

#include <stdlib.h>



Struct Node {

    Int data;

    Struct Node *prev;

    Struct Node *next;

};



Void display(struct Node *head) {

    Struct Node *temp = head;

    Printf(“Doubly Linked List: “);

    While (temp != NULL) {

        Printf(“%d <-> “, temp->data);

        Temp = temp->next;

    }

    Printf(“NULL\n”);

}



Int main() {

    Struct Node *head = NULL, *node1, *node2, *node3;



    Node1 = malloc(sizeof(struct Node));

    Node2 = malloc(sizeof(struct Node));

    Node3 = malloc(sizeof(struct Node));



    Node1->data = 10; node1->prev = NULL; node1->next = node2;

    Node2->data = 20; node2->prev = node1; node2->next = node3;

    Node3->data = 30; node3->prev = node2; node3->next = NULL;



    Head = node1;

    Display(head);

    Return 0;

}

//output: Doubly Linked List: 10 <-> 20 <-> 30 <-> NULL

//35. Insert a node at the beginning of a doubly linked list



#include <stdio.h>

#include <stdlib.h>



Struct Node {

    Int data;

    Struct Node *prev;

    Struct Node *next;

};



Void insertAtBeginning(struct Node **head, int data) {

    Struct Node *newNode = malloc(sizeof(struct Node));

    newNode->data = data;

    newNode->prev = NULL;

    newNode->next = *head;



    if (*head != NULL)

        (*head)->prev = newNode;



    *head = newNode;

}



Void display(struct Node *head) {

    While (head != NULL) {

        Printf(“%d <-> “, head->data);

        Head = head->next;

    }

    Printf(“NULL\n”);

}



Int main() {

    Struct Node *head = NULL;

    insertAtBeginning(&head, 10);

    insertAtBeginning(&head, 20);

    insertAtBeginning(&head, 30);

    display(head);

    return 0;

}

//Output:30 <-> 20 <-> 10 <-> NULL



//36. Insert a node at the end of a doubly linked list



#include <stdio.h>

#include <stdlib.h>



Struct Node {

    Int data;

    Struct Node *prev;

    Struct Node *next;

};



Void insertAtEnd(struct Node **head, int data) {

    Struct Node *newNode = malloc(sizeof(struct Node));

    newNode->data = data;

    newNode->next = NULL;



    if (*head == NULL) {

        newNode->prev = NULL;

        *head = newNode;

        Return;

    }



    Struct Node *temp = *head;

    While (temp->next != NULL)

        Temp = temp->next;



    Temp->next = newNode;

    newNode->prev = temp;

}



Void display(struct Node *head) {

    While (head != NULL) {

        Printf(“%d <-> “, head->data);

        Head = head->next;

    }

    Printf(“NULL\n”);

}



Int main() {

    Struct Node *head = NULL;

    insertAtEnd(&head, 10);

    insertAtEnd(&head, 20);

    insertAtEnd(&head, 30);

    display(head);

    return 0;

}

//output:10 <-> 20 <-> 30 <-> NULL



//37. Delete a node from the beginning of a doubly linked list



#include <stdio.h>

#include <stdlib.h>



struct Node {

    int data;

    struct Node *prev;

    struct Node *next;

};



void deleteFromBeginning(struct Node **head) {

    if (*head == NULL) {

        printf("List empty.\n");

        return;

    }

    struct Node *temp = *head;

    *head = (*head)->next;

    if (*head != NULL)

        (*head)->prev = NULL;

    free(temp);

}



void display(struct Node *head) {

    while (head != NULL) {

        printf("%d <-> ", head->data);

        head = head->next;

    }

    printf("NULL\n");

}



int main() {

    struct Node *head = NULL;

    struct Node *node1 = malloc(sizeof(struct Node));

    struct Node *node2 = malloc(sizeof(struct Node));



    node1->data = 10; node1->prev = NULL; node1->next = node2;

    node2->data = 20; node2->prev = node1; node2->next = NULL;

    head = node1;



    display(head);

    deleteFromBeginning(&head);

    display(head);

    return 0;

}

//Output:10 <-> 20 <-> NULL

//20 <-> NULL 

//38. Delete a node from the end of a doubly linked list



#include <stdio.h>

#include <stdlib.h>



struct Node {

    int data;

    struct Node *prev;

    struct Node *next;

};



void deleteFromEnd(struct Node **head) {

    if (*head == NULL) {

        printf("List empty.\n");

        return;

    }

    struct Node *temp = *head;

    if (temp->next == NULL) {

        free(temp);

        *head = NULL;

        return;

    }



    while (temp->next != NULL)

        temp = temp->next;



    temp->prev->next = NULL;

    free(temp);

}



void display(struct Node *head) {

    while (head != NULL) {

        printf("%d <-> ", head->data);

        head = head->next;

    }

    printf("NULL\n");

}



int main() {

    struct Node *head = NULL;

    struct Node *n1 = malloc(sizeof(struct Node));

    struct Node *n2 = malloc(sizeof(struct Node));



    n1->data = 10; n1->prev = NULL; n1->next = n2;

    n2->data = 20; n2->prev = n1; n2->next = NULL;

    head = n1;



    display(head);

    deleteFromEnd(&head);

    display(head);

    return 0;

}

//output: 10 <-> 20 <-> NULL

//10 <-> NULL 

//39. Create a binary tree and traverse it (Inorder, Preorder, Postorder)



#include <stdio.h>

#include <stdlib.h>



Struct Node {

    Int data;

    Struct Node *left;

    Struct Node *right;

};



Struct Node* createNode(int data) {

    Struct Node* newNode = malloc(sizeof(struct Node));

    newNode->data = data;

    newNode->left = newNode->right = NULL;

    return newNode;

}



Void inorder(struct Node *root) {

    If (root == NULL) return;

    Inorder(root->left);

    Printf(“%d “, root->data);

    Inorder(root->right);

}



Void preorder(struct Node *root) {

    If (root == NULL) return;

    Printf(“%d “, root->data);

    Preorder(root->left);

    Preorder(root->right);

}



Void postorder(struct Node *root) {

    If (root == NULL) return;

    Postorder(root->left);

    Postorder(root->right);

    Printf(“%d “, root->data);

}



Int main() {

    Struct Node *root = createNode(1);

    Root->left = createNode(2);

    Root->right = createNode(3);

    Root->left->left = createNode(4);

    Root->left->right = createNode(5);



    Printf(“Inorder Traversal: “);

    Inorder(root);

    Printf(“\nPreorder Traversal: “);

    Preorder(root);

    Printf(“\nPostorder Traversal: “);

    Postorder(root);

    Return 0;

}



//Output:Inorder Traversal: 4 2 5 1 3 

//Preorder Traversal: 1 2 4 5 3 

//Postorder Traversal: 4 5 2 3 1 


//40. Insert a node into a Binary Search Tree (BST)



#include <stdio.h>

#include <stdlib.h>



Struct Node {

    Int data;

    Struct Node *left, *right;

};



Struct Node* createNode(int data) {

    Struct Node* newNode = malloc(sizeof(struct Node));

    newNode->data = data;

    newNode->left = newNode->right = NULL;

    return newNode;

}



Struct Node* insert(struct Node* root, int data) {

    If (root == NULL)

        Return createNode(data);

    If (data < root->data)

        Root->left = insert(root->left, data);

    Else if (data > root->data)

        Root->right = insert(root->right, data);

    Return root;

}



Void inorder(struct Node* root) {

    If (root != NULL) {

        Inorder(root->left);

        Printf(“%d “, root->data);

        Inorder(root->right);

    }

}



Int main() {

    Struct Node* root = NULL;

    Root = insert(root, 50);

    Insert(root, 30);

    Insert(root, 70);

    Insert(root, 20);

    Insert(root, 40);

    Insert(root, 60);

    Insert(root, 80);



    Printf(“Inorder traversal of BST: “);

    Inorder(root);

    Return 0;

}

//Output: Inorder traversal of BST: 20 30 40 50 60 70 80

//41. Delete a node from a Binary Search Tree (BST)



#include <stdio.h>

#include <stdlib.h>



struct Node {

    int data;

    struct Node *left, *right;

};



struct Node* createNode(int data) {

    struct Node* newNode = malloc(sizeof(struct Node));

    newNode->data = data;

    newNode->left = newNode->right = NULL;

    return newNode;

}



struct Node* insert(struct Node* root, int data) {

    if (root == NULL)

        return createNode(data);

    if (data < root->data)

        root->left = insert(root->left, data);

    else if (data > root->data)

        root->right = insert(root->right, data);

    return root;

}



struct Node* minValueNode(struct Node* node) {

    struct Node* current = node;

    while (current && current->left != NULL)

        current = current->left;

    return current;

}



struct Node* deleteNode(struct Node* root, int key) {

    if (root == NULL) return root;

    if (key < root->data)

        root->left = deleteNode(root->left, key);

    else if (key > root->data)

        root->right = deleteNode(root->right, key);

    else {

        if (root->left == NULL) {

            struct Node* temp = root->right;

            free(root);

            return temp;

        } else if (root->right == NULL) {

            struct Node* temp = root->left;

            free(root);

            return temp;

        }

        struct Node* temp = minValueNode(root->right);

        root->data = temp->data;

        root->right = deleteNode(root->right, temp->data);

    }

    return root;

}



void inorder(struct Node* root) {

    if (root != NULL) {

        inorder(root->left);

        printf("%d ", root->data);

        inorder(root->right);

    }

}



int main() {

    struct Node* root = NULL;

    root = insert(root, 50);

    insert(root, 30);

    insert(root, 70);

    insert(root, 20);

    insert(root, 40);

    insert(root, 60);

    insert(root, 80);



    printf("Inorder before deletion: ");

    inorder(root);



    root = deleteNode(root, 20);

    root = deleteNode(root, 30);



    printf("\nInorder after deletion: ");

    inorder(root);

    return 0;

}

// Output: Inorder before deletion: 20 30 40 50 60 70 80 

//Inorder after deletion: 40 50 60 70 80

//42. Find the minimum and maximum value in a BST



#include <stdio.h>

#include <stdlib.h>



struct Node {

    int data;

    struct Node *left, *right;

};



struct Node* createNode(int data) {

    struct Node* node = malloc(sizeof(struct Node));

    node->data = data;

    node->left = node->right = NULL;

    return node;

}



struct Node* insert(struct Node* root, int data) {

    if (root == NULL) return createNode(data);

    if (data < root->data)

        root->left = insert(root->left, data);

    else if (data > root->data)

        root->right = insert(root->right, data);

    return root;

}



int findMin(struct Node* root) {

    while (root->left != NULL)

        root = root->left;

    return root->data;

}



int findMax(struct Node* root) {

    while (root->right != NULL)

        root = root->right;

    return root->data;

}



int main() {

    struct Node* root = NULL;

    root = insert(root, 50);

    insert(root, 30);

    insert(root, 70);

    insert(root, 20);

    insert(root, 90);



    printf("Minimum value: %d\n", findMin(root));

    printf("Maximum value: %d\n", findMax(root));

    return 0;

}

//Output: Minimum value: 20

//Maximum value: 90 

//43. Implement a stack using a linked list



#include <stdio.h>

#include <stdlib.h>



Struct Node {

    Int data;

    Struct Node* next;

};



Struct Node* top = NULL;



Void push(int data) {

    Struct Node* newNode = malloc(sizeof(struct Node));

    newNode->data = data;

    newNode->next = top;

    top = newNode;

    printf(“%d pushed to stack\n”, data);

}



Void pop() {

    If (top == NULL) {

        Printf(“Stack Underflow\n”);

        Return;

    }

    Printf(“%d popped from stack\n”, top->data);

    Struct Node* temp = top;

    Top = top->next;

    Free(temp);

}



Void display() {

    Struct Node* temp = top;

    Printf(“Stack elements: “);

    While (temp) {

        Printf(“%d “, temp->data);

        Temp = temp->next;

    }

    Printf(“\n”);

}



Int main() {

    Push(10);

    Push(20);

    Push(30);

    Display();

    Pop();

    Display();

    Return 0;

}

//Output:10 pushed to stack

//20 pushed to stack

//30 pushed to stack

//Stack elements: 30 20 10 

//30 popped from stack

//Stack elements: 20 10 

//44. Implement a queue using a linked list



#include <stdio.h>

#include <stdlib.h>



Struct Node {

    Int data;

    Struct Node* next;

};



Struct Node *front = NULL, *rear = NULL;



Void enqueue(int data) {

    Struct Node* newNode = malloc(sizeof(struct Node));

    newNode->data = data;

    newNode->next = NULL;

    if (rear == NULL)

        front = rear = newNode;

    else {

        rear->next = newNode;

        rear = newNode;

    }

    Printf(“%d enqueued\n”, data);

}



Void dequeue() {

    If (front == NULL) {

        Printf(“Queue Underflow\n”);

        Return;

    }

    Printf(“%d dequeued\n”, front->data);

    Struct Node* temp = front;

    Front = front->next;

    If (front == NULL)

        Rear = NULL;

    Free(temp);

}



Void display() {

    Struct Node* temp = front;

    Printf(“Queue elements: “);

    While (temp) {

        Printf(“%d “, temp->data);

        Temp = temp->next;

    }

    Printf(“\n”);

}



Int main() {

    Enqueue(10);

    Enqueue(20);

    Enqueue(30);

    Display();

    Dequeue();

    Display();

    Return 0;

}

//10 enqueued

//20 enqueued

//30 enqueued

//Queue elements: 10 20 30 

//10 dequeued 

//45. Create and display a circular linked list



#include <stdio.h>

#include <stdlib.h>



Struct Node {

    Int data;

    Struct Node* next;

};



Void display(struct Node* head) {

    Struct Node* temp = head;

    If (head == NULL) return;

    Do {

        Printf(“%d -> “, temp->data);

        Temp = temp->next;

    } while (temp != head);

    Printf(“(back to head)\n”);

}



Int main() {

    Struct Node *head = NULL, *n1, *n2, *n3;

    N1 = malloc(sizeof(struct Node));

    N2 = malloc(sizeof(struct Node));

    N3 = malloc(sizeof(struct Node));



    N1->data = 10; n2->data = 20; n3->data = 30;

    N1->next = n2; n2->next = n3; n3->next = n1;

    Head = n1;



    Display(head);

    Return 0;

}

// Output:10 -> 20 -> 30 -> (back to head)

//46. Add two polynomials using linked list



#include <stdio.h>

#include <stdlib.h>



struct Node {

    int coeff, exp;

    struct Node* next;

};



struct Node* createNode(int c, int e) {

    struct Node* newNode = malloc(sizeof(struct Node));

    newNode->coeff = c;

    newNode->exp = e;

    newNode->next = NULL;

    return newNode;

}



struct Node* addPolynomials(struct Node* p1, struct Node* p2) {

    struct Node* result = NULL, *tail = NULL;

    while (p1 && p2) {

        struct Node* temp;

        if (p1->exp == p2->exp) {

            temp = createNode(p1->coeff + p2->coeff, p1->exp);

            p1 = p1->next; p2 = p2->next;

        } else if (p1->exp > p2->exp) {

            temp = createNode(p1->coeff, p1->exp);

            p1 = p1->next;

        } else {

            temp = createNode(p2->coeff, p2->exp);

            p2 = p2->next;

        }

        if (!result)

            result = tail = temp;

        else {

            tail->next = temp;

            tail = temp;

        }

    }

    while (p1) {

        tail->next = createNode(p1->coeff, p1->exp);

        p1 = p1->next;

        tail = tail->next;

    }

    while (p2) {

        tail->next = createNode(p2->coeff, p2->exp);

        p2 = p2->next;

        tail = tail->next;

    }

    return result;

}



void display(struct Node* poly) {

    while (poly) {

        printf("%dx^%d ", poly->coeff, poly->exp);

        if (poly->next) printf("+ ");

        poly = poly->next;

    }

    printf("\n");

}



int main() {

    struct Node *p1 = NULL, *p2 = NULL, *res = NULL;

    p1 = createNode(5, 2);

    p1->next = createNode(4, 1);

    p1->next->next = createNode(2, 0);



    p2 = createNode(5, 1);

    p2->next = createNode(5, 0);



    printf("Polynomial 1: "); display(p1);

    printf("Polynomial 2: "); display(p2);



    res = addPolynomials(p1, p2);

    printf("Sum: "); display(res);

    return 0;

}

//Output:Polynomial 1: 5x^2 + 4x^1 + 2x^0 

//Polynomial 2: 5x^1 + 5x^0 

//Sum: 5x^2 + 9x^1 + 7x^0 



//48. Bubble Sort



#include <stdio.h>



Int main() {

    Int n, i, j, temp;

    Printf(“Enter number of elements: “);

    Scanf(“%d”, &n);

    Int a[n];

    Printf(“Enter elements: “);

    For(i = 0; i < n; i++)

        Scanf(“%d”, &a[i]);



    For(i = 0; i < n-1; i++)

        For(j = 0; j < n-i-1; j++)

            If(a[j] > a[j+1]) {

                Temp = a[j];

                A[j] = a[j+1];

                A[j+1] = temp;

            }



    Printf(“Sorted array: “);

    For(i = 0; i < n; i++)

        Printf(“%d “, a[i]);

    Return 0;

}

// Output: Enter number of elements: 4

//Enter elements: 55

//78

//23

//54

//Sorted array: 23 54 55 78 



//49. Insertion Sort



#include <stdio.h>



Int main() {

    Int n, i, j, key;

    Printf(“Enter number of elements: “);

    Scanf(“%d”, &n);

    Int a[n];

    Printf(“Enter elements: “);

    For(i = 0; i < n; i++)

        Scanf(“%d”, &a[i]);



    For(i = 1; i < n; i++) {

        Key = a[i];

        J = i – 1;

        While(j >= 0 && a[j] > key) {

            A[j+1] = a[j];

            j--;

        }

        A[j+1] = key;

    }



    Printf(“Sorted array: “);

    For(i = 0; i < n; i++)

        Printf(“%d “, a[i]);

    Return 0;

}

// Output: Enter number of elements: 4

//Enter elements: 45

//65

//55

//23

//Sorted array: 23 45 55 65

//50. Quick Sort



#include <stdio.h>



void swap(int *a, int *b) {

    int temp = *a; *a = *b; *b = temp;

}



int partition(int arr[], int low, int high) {

    int pivot = arr[high];

    int i = low - 1;

    for(int j = low; j < high; j++) {

        if(arr[j] < pivot) {

            i++;

            swap(&arr[i], &arr[j]);

        }

    }

    swap(&arr[i + 1], &arr[high]);

    return i + 1;

}



void quickSort(int arr[], int low, int high) {

    if(low < high) {

        int pi = partition(arr, low, high);

        quickSort(arr, low, pi - 1);

        quickSort(arr, pi + 1, high);

    }

}



int main() {

    int n;

    printf("Enter number of elements: ");

    scanf("%d", &n);

    int arr[n];

    printf("Enter elements: ");

    for(int i = 0; i < n; i++)

        scanf("%d", &arr[i]);



    quickSort(arr, 0, n - 1);



    printf("Sorted array: ");

    for(int i = 0; i < n; i++)

        printf("%d ", arr[i]);

    return 0;

}

// Output: Enter number of elements: 4

//Enter elements: 23

//45

//65

//44

//Sorted array: 23 44 45 65 




