bool isValid(BinaryTreeNode<int> *root,int minVal,int maxVal){

if(root==NULL){

return true;

}

if(root->data>maxVal || root->data<minVal){

return false;

}

return (isValid(root->left, minVal, root->data)and isValid(root->right, root->data, maxVal));

 

}

bool validateBST(BinaryTreeNode<int> *root) {

// Write your code here

return isValid(root, INT_MIN, INT_MAX);

}
