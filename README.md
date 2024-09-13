# BinaryTree_methods
applying various methods in binary tree through  python list
class BinaryTree:
    def __init__(self, size):
        self.customList = size * [None]
        self.lastUsedIndex = 0
        self.maxSize = size
