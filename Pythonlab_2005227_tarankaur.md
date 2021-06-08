******Python program to print the elements of an array***

#Initialize array  
arr = [0,1, 2, 3, 4, 5]; 
print("Elements of given array: "); 
print("Access all items individually");
print"1st element:",arr[0];

print"2nd element:",arr[1];
print"3rd element:",arr[2];
print"4th element:",arr[3];
print"5th element:",arr[4];
print"6th element:",arr[5];

output:![py1](https://user-images.githubusercontent.com/79211429/121027166-5fd14600-c7c4-11eb-9f72-c3311119ea95.png)




***write a python program to reverse the order of the items in the array.***

#The original array

arr = [11, 22, 33, 44, 55]
print("Before reversal Array is :",arr)

#Reverse of array

arr.reverse() #reversing using reverse()
print("After reversing Array:",arr)

output:![py2](https://user-images.githubusercontent.com/79211429/121026567-e174a400-c7c3-11eb-9f55-291f03e1f409.png)




***Write a Python program to append a new item to the end of the array.***

my_input = ['Engineering', 'Medical'] 
my_input.append('Science') 
print(my_input)

output:![c](https://user-images.githubusercontent.com/79211429/121028510-86dc4780-c7c5-11eb-9ff6-a397b50fab21.png)




***write a python program to remove a specified item using the index from an array.***

# Original array
arr= [1,2,3,4,5,6]

# Remove element with index= 1
arr.remove(1)

# Printing the array
print(arr)

# Remove element with index = 4
arr.remove(4)

# Printing the array
print(arr)

output:![d](https://user-images.githubusercontent.com/79211429/121028368-64e2c500-c7c5-11eb-8ea8-517e266715b5.png)





***Write a Python program to get the length of an array.***

import array 
arr = [1,2,3,4,'PYTHON']
print("Array elements: ",arr)
print("Length of array:",len(arr))

output: ![e](https://user-images.githubusercontent.com/79211429/121028801-bc813080-c7c5-11eb-96f9-e0ed63cb0aa5.png)





***write a program for binary search***

def binary_search(arr, low, high, x):
 
    # Check base case
    if high >= low:
 
        mid = (high + low) // 2
 
        # If element is present at the middle itself
        if arr[mid] == x:
            return mid
 
        # If element is smaller than mid, then it can only
        # be present in left subarray
        elif arr[mid] > x:
            return binary_search(arr, low, mid - 1, x)
 
        # Else the element can only be present in right subarray
        else:
            return binary_search(arr, mid + 1, high, x)
 
    else:
        # Element is not present in the array
        return -1
 
# Test array
arr = [ 2, 3, 4, 10, 40 ]
x = 10
 
# Function call
result = binary_search(arr, 0, len(arr)-1, x)
 
if result != -1:
    print("Element is present at index", str(result))
else:
    print("Element is not present in array")
    
 output:![expt6](https://user-images.githubusercontent.com/79211429/121030128-d3745280-c7c6-11eb-9bff-037dfc4396bb.png)





***write a python program for sequential or linear search***

def linearsearch(arr, x):
   for i in range(len(arr)):
      if arr[i] == x:
         return i
   return -1
arr = ['t','u','t','o','r','i','a','l']
x = 'a'
print("element found at index "+str(linearsearch(arr,x)))

output:![exp7](https://user-images.githubusercontent.com/79211429/121031490-023ef880-c7c8-11eb-882c-fa87519b384e.png)






***write a python program to sort list of elements using bubble sort algorithm***

def bubbleSort(nlist):
    for passnum in range(len(nlist)-1,0,-1):
        for i in range(passnum):
            if nlist[i]>nlist[i+1]:
                temp = nlist[i]
                nlist[i] = nlist[i+1]
                nlist[i+1] = temp

nlist = [14,46,43,27,57,41,45,21,70]
bubbleSort(nlist)
print(nlist)

output:![expt8](https://user-images.githubusercontent.com/79211429/121034871-ff91d280-c7ca-11eb-8455-1ad6a8162369.png)





***write a python program to sort list of elements using selection sort algorithm***

def selectionSort( itemsList ):
    n = len( itemsList )
    for i in range( n - 1 ):
        minValueIndex = i

        for j in range( i + 1, n ):
            if itemsList[j] < itemsList[minValueIndex] :
                minValueIndex = j

        if minValueIndex != i :
            temp = itemsList[i]
            itemsList[i] = itemsList[minValueIndex]
            itemsList[minValueIndex] = temp

    return itemsList


el = [21,6,9,33,3]

print(selectionSort(el))

output: ![python9](https://user-images.githubusercontent.com/79211429/120997984-466cd180-c7a5-11eb-934c-95c42f6cb833.jpeg)



***write a python program to sort list of elements using insertion sort algorithm***

arr = [12, 11, 13, 5, 6]
insertionSort(arr)
print ("Sorted array is:")
for i in range(len(arr)):
    print ("%d" %arr[i])
    
    output:![python10](https://user-images.githubusercontent.com/79211429/120999629-f8f16400-c7a6-11eb-8d7c-ddd29c40c48d.jpeg)
    
    
    
    


***write a python program to sort list of elements using quick sort algorithm***

def quicksort(x):
    if len(x) == 1 or len(x) == 0:
        return x
    else:
        pivot = x[0]
        i = 0
        for j in range(len(x)-1):
            if x[j+1] < pivot:
                x[j+1],x[i+1] = x[i+1], x[j+1]
                i += 1
        x[0],x[i] = x[i],x[0]
        first_part = quicksort(x[:i])
        second_part = quicksort(x[i+1:])
        first_part.append(x[i])
        return first_part + second_part

alist = [54,26,93,17,77,31,44,55,20]
quicksort(alist)
print(alist)

output: ![python11](https://user-images.githubusercontent.com/79211429/121000060-6dc49e00-c7a7-11eb-8dba-4a86df06cacb.jpeg)






***write a python program to search a specific item in a singly linked list and return true if the item is found otherwise false***
class Node:
    def _init_(self, data=None):
        self.data = data
        self.next = None
class singly_linked_list:
    def _init_(self):
        self.tail = None
        self.head = None
        self.count = 0

    def iterate_item(self):
        current_item = self.tail
        while current_item:
            val = current_item.data
            current_item = current_item.next
            yield val

    def append_item(self, data):
        node = Node(data)
        if self.head:
            self.head.next = node
            self.head = node
        else:
            self.tail = node
            self.head = node
        self.count += 1

items = singly_linked_list()
items.append_item('PHP')
items.append_item('Python')
items.append_item('C#')
items.append_item('C++')
items.append_item('Java')

for val in items.iterate_item():
    print(val)
    
    output:![python12](https://user-images.githubusercontent.com/79211429/121000364-c1cf8280-c7a7-11eb-9793-1be5e0f31e66.jpeg)






***write a python program to find the size of singly linked list***

class Node:
    # Singly linked node
    def _init_(self, data=None):
        self.data = data
        self.next = None
class singly_linked_list:
    def _init_(self):
        # Createe an empty list
        self.tail = None
        self.head = None
        self.count = 0
	
    def append_item(self, data):
        #Append items on the list
        node = Node(data)
        if self.head:
            self.head.next = node
            self.head = node
        else:
            self.tail = node
            self.head = node
        self.count += 1
    
    def iterate_item(self):
        # Iterate the list.
        current_item = self.tail
        while current_item:
            val = current_item.data
            current_item = current_item.next
            yield val

items = singly_linked_list()
items.append_item('PHP')
items.append_item('Python')
items.append_item('C#')
items.append_item('C++')
items.append_item('Java')

print("Original list:")
for val in items.iterate_item():
    print(val)

print("\nSize of the list:",items.count)

output: ![python13](https://user-images.githubusercontent.com/79211429/121002577-1e33a180-c7aa-11eb-8131-b63e3e411183.jpeg)







***write a program to search specific item in a singly linked list and return the item if the item is found otherwise return false***

class Node:
    # Singly linked node
    def _init_(self, data=None):
        self.data = data
        self.next = None
class singly_linked_list:
    def _init_(self):
        # Createe an empty list
        self.tail = None
        self.head = None
        self.count = 0

    def append_item(self, data):
        #Append items on the list
        node = Node(data)
        if self.head:
            self.head.next = node
            self.head = node
        else:
            self.tail = node
            self.head = node
        self.count += 1

    def iterate_item(self):
        # Iterate the list.
        current_item = self.tail
        while current_item:
            val = current_item.data
            current_item = current_item.next
            yield val

    def search_item(self, val):
         # Search the list
         for node in self.iterate_item():
             if val == node:
                 return True
         return False

items = singly_linked_list()
items.append_item('PHP')
items.append_item('Python')
items.append_item('C#')
items.append_item('C++')
items.append_item('Java')

if items.search_item('SQL'):
    print("True")
else:
    print("False")

if items.search_item('C++'):
    print("True")
else:
    print("False")
    
 output:![python14](https://user-images.githubusercontent.com/79211429/121002879-77033a00-c7aa-11eb-933a-0f24a6a57299.jpeg)
 
 
 

 
 ***write a python program to delete the first item from singly linked list***
 
 class Node:
    # Singly linked node
    def _init_(self, data=None):
        self.data = data
        self.next = None
class singly_linked_list:
    def _init_(self):
        # Createe an empty list
        self.tail = None
        self.head = None
        self.count = 0

    def append_item(self, data):
        #Append items on the list
        node = Node(data)
        if self.head:
            self.head.next = node
            self.head = node
        else:
            self.tail = node
            self.head = node
        self.count += 1

    def delete_item(self, data):
        # Delete an item from the list
        current = self.tail
        prev = self.tail
        while current:
            if current.data == data:
                if current == self.tail:
                    self.tail = current.next
                else:
                    prev.next = current.next
                self.count -= 1
                return
            prev = current
            current = current.next
    def iterate_item(self):
        # Iterate the list.
        current_item = self.tail
        while current_item:
            val = current_item.data
            current_item = current_item.next
            yield val

items = singly_linked_list()
items.append_item('PHP')
items.append_item('Python')
items.append_item('C#')
items.append_item('C++')
items.append_item('Java')

print("Original list:")
for val in items.iterate_item():
    print(val)

print("\nAfter removing the first item from the list:")
items.delete_item('PHP')
for val in items.iterate_item():
    print(val)
    
    output: ![python15](https://user-images.githubusercontent.com/79211429/121003167-d7927700-c7aa-11eb-85a7-f35ff7c2c569.jpeg)






***write a python program to create circular linked list***
class Node:
     
    # Constructor to create  a new node
    def __init__(self, data):
        self.data = data
        self.next = None
 
class CircularLinkedList:
     
    # Constructor to create a empty circular linked list
    def __init__(self):
        self.head = None
 
    # Function to insert a node at the beginning of a
    # circular linked list
    def push(self, data):
        ptr1 = Node(data)
        temp = self.head
         
        ptr1.next = self.head
 
        # If linked list is not None then set the next of
        # last node
        if self.head is not None:
            while(temp.next != self.head):
                temp = temp.next
            temp.next = ptr1
 
        else:
            ptr1.next = ptr1 # For the first node
 
        self.head = ptr1
 
    # Function to print nodes in a given circular linked list
    def printList(self):
        temp = self.head
        if self.head is not None:
            while(True):
                print "%d" %(temp.data),
                temp = temp.next
                if (temp == self.head):
                    break
 
# Driver program to test above function
 
# Initialize list as empty
cllist = CircularLinkedList()
 
# Created linked list will be 11->2->56->12
cllist.push(12)
cllist.push(56)
cllist.push(2)
cllist.push(11)
 
print "Contents of circular Linked List"
cllist.printList()


 output:![ex16](https://user-images.githubusercontent.com/79211429/121030456-1df5cf00-c7c7-11eb-971b-f82ff75c9797.png)
 
 
 

***write a python program to implement stack and its operations using list***

stack = []
 
# append() function to push
# element in the stack
stack.append('a')
stack.append('b')
stack.append('c')
 
print('Initial stack')
print(stack)
 
# pop() fucntion to pop
# element from stack in
# LIFO order
print('\nElements poped from stack:')
print(stack.pop())
print(stack.pop())
print(stack.pop())
 
print('\nStack after elements are poped:')
print(stack)

output:![expt17](https://user-images.githubusercontent.com/79211429/121029213-0c5ff780-c7c6-11eb-9668-d45fc9370082.png)





***write python program to implement queue and its operations using list***


Initializing a queue
queue = []

# Adding elements to the queue
queue.append('a')
queue.append('b')
queue.append('c')

print("Initial queue")
print(queue)

# Removing elements from the queue
print("\nElements dequeued from queue")
print(queue.pop(0))
print(queue.pop(0))
print(queue.pop(0))

print("\nQueue after removing elements")
print(queue)

# Uncommenting print(queue.pop(0))
# will raise and IndexError
# as the queue is now empty

output:![python18](https://user-images.githubusercontent.com/79211429/121021352-ec790580-c7be-11eb-9667-451997d5936e.jpeg)



****write a program to create a balanced binary search tree (bst) using an array (given) elements where array elements are stored in ascending order***

class TreeNode(object):
    def __init__(self, x):
        self.val = x
        self.left = None
        self.right = None

def sorted_array_to_bst(nums):
    
    if not nums:
        return None
    mid_val = len(nums)//2
    node = TreeNode(nums[mid_val])
    node.left = sorted_array_to_bst(nums[:mid_val])
    node.right = sorted_array_to_bst(nums[mid_val+1:])
    return node

def preOrder(node): 
    if not node: 
        return      
    print(node.val)
    preOrder(node.left) 
    preOrder(node.right)   
    
result = sorted_array_to_bst([1, 2, 3, 4, 5, 6, 7])
preOrder(result)


output:![expt19](https://user-images.githubusercontent.com/79211429/121033383-c60c9780-c7c9-11eb-8809-e98e53d20ace.png)





****write a python program to find kth smallest element in a given binary search tree***

class TreeNode(object):
    def __init__(self, x):
        self.val = x
        self.left = None
        self.right = None

def kth_smallest(root, k):
    stack = []
    while root or stack:
        while root:
            stack.append(root)
            root = root.left
        root = stack.pop()
        k -= 1
        if k == 0:
            break
        root = root.right
    return root.val

root = TreeNode(8)  
root.left = TreeNode(5)  
root.right = TreeNode(14) 
root.left.left = TreeNode(4)  
root.left.right = TreeNode(6) 
root.left.right.left = TreeNode(8)  
root.left.right.right = TreeNode(7)  
root.right.right = TreeNode(24) 
root.right.right.left = TreeNode(22)  

print(kth_smallest(root, 2))
print(kth_smallest(root, 3))

output:![expt20](https://user-images.githubusercontent.com/79211429/121034404-a0cc5900-c7ca-11eb-81dd-9f6b4eef8367.png)


