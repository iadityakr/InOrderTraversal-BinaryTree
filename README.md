# InOrderTraversal-BinaryTree

# Recursive-Code

```
public static void inOrderRecursive(TreeNode root){
        if(root == null) return;  // base case
        
        inOrderRecursive(root.left);
        System.out.println(root.data);
        inOrderRecursive(root.right);
        
    }
 ```
 
 # Iterative-Code
 
 ```
 public static void inOrderIterative(TreeNode root){
        if(root == null) return;
        
        Stack<TreeNode> s = new Stack<>();
        TreeNode curr = root;
        
        while(curr != null || s.size() > 0){
            if(curr != null){
                s.push(curr);
                curr = curr.left;
            }
            else{
                curr = s.pop();
                System.out.print(curr.data+" ");
                curr = curr.right;
            }
        }
    }
 ```
 
 # Whole code
 
 ```
 import java.util.Stack;

class TreeNode{
    TreeNode left, right;
    int data;
    public TreeNode(int data){
        this.data = data;
    }
}



public class BinaryTree {
    
    public static void inOrderRecursive(TreeNode root){
        if(root == null) return;  // base case
        
        inOrderRecursive(root.left);
        System.out.println(root.data);
        inOrderRecursive(root.right);
        
    }
    
    public static void inOrderIterative(TreeNode root){
        if(root == null) return;
        
        Stack<TreeNode> s = new Stack<>();
        TreeNode curr = root;
        
        while(curr != null || s.size() > 0){
            if(curr != null){
                s.push(curr);
                curr = curr.left;
            }
            else{
                curr = s.pop();
                System.out.print(curr.data+" ");
                curr = curr.right;
            }
        }
    }
    
    public static void main(String[] args) {
        TreeNode root = new TreeNode(10);
        root.left = new TreeNode(20);
        root.right = new TreeNode(30);
        root.right.left = new TreeNode(40);
        root.right.right = new TreeNode(50);
//        inOrderRecursive(root);
        inOrderIterative(root);
    }
}
 ```
