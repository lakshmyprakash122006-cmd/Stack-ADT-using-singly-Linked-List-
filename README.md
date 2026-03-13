# Stack-ADT-using-singly-Linked-List-
Data structure practical program 
# Stack using Singly Linked List

class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

top = None

# Push operation
def push():
    global top
    x = int(input("Enter element: "))
    newnode = Node(x)
    newnode.next = top
    top = newnode
    print("Element pushed")

# Pop operation
def pop():
    global top
    if top is None:
        print("Stack is empty")
    else:
        print("Popped element:", top.data)
        top = top.next

# Display stack
def display():
    temp = top
    if temp is None:
        print("Stack is empty")
    else:
        print("Stack elements:")
        while temp:
            print(temp.data)
            temp = temp.next

while True:
    print("\n1.Push 2.Pop 3.Display 4.Exit")
    ch = int(input("Enter choice: "))

    if ch == 1:
        push()
    elif ch == 2:
        pop()
    elif ch == 3:
        display()
    elif ch == 4:
        break
    else:
        print("Invalid choice")
  output:
  1.Push 2.Pop 3.Display 4.Exit
Enter choice: 1
Enter element: 10
Element pushed

Enter choice: 1
Enter element: 20
Element pushed

Enter choice: 3
Stack elements:
20
10
