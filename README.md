# BinaryTree_methods
applying various methods in binary tree through  python list
# creating an empty binary tree
class BinaryTree:
    def __init__(self, size):
        self.customList = size * [None]
        self.lastUsedIndex = 0
        self.maxSize = size
#inserting node
    def insertNode(self, value):
        if self.lastUsedIndex + 1 == self.maxSize:
            return " THe binary tree is full"
        self.customList[self.lastUsedIndex+1] = value
        self.lastUsedIndex += 1
        return "The value has been inserted"

#Searching a node
    def searchNode(self, noddeValue):
        for i in range(len(self.customList)):
            if self.customList[i] == noddeValue:
                return "success"
        return "NOT found"

#PreorderTraversal 
    def preOrderTraversal(self, index):
        if index > self.lastUsedIndex:
            return
        print(self.customList[index])
        self.preOrderTraversal(index*2)
        self.preOrderTraversal(index*2 + 1)

#inOrderTrversal
    def inOrderTraversal(self, index):
        if index > self.lastUsedIndex:
            return
        self.inOrderTraversal(index*2)
        print(self.customList[index])
        self.inOrderTraversal(index*2+1)   
        

