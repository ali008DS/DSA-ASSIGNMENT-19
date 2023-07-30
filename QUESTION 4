class TreeNode:
    def __init__(self, val):
        self.val = val
        self.left = None
        self.right = None
        self.next = None

def connect_nodes_at_same_level(root):
    if not root:
        return

    queue = [root]

    while queue:
        level_size = len(queue)
        for i in range(level_size):
            node = queue.pop(0)
            if i < level_size - 1:
                node.next = queue[0]
            if node.left:
                queue.append(node.left)
            if node.right:
                queue.append(node.right)

# Example input binary tree
root = TreeNode(1)
root.left = TreeNode(2)
root.right = TreeNode(3)
root.left.left = TreeNode(4)
root.left.right = TreeNode(5)
root.right.left = TreeNode(6)
root.right.right = TreeNode(7)

# Connect nodes at the same level
connect_nodes_at_same_level(root)

# Function to print the next pointers at the same level
def print_next_pointers(root):
    while root:
        print(root.val, end=" -> ")
        root = root.next
    print("-1")

# Test case
print_next_pointers(root)  # Output: 1 -> -1, 2 -> 3 -> -1, 4 -> 5 -> 6 -> 7 -> -1
