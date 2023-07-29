TreeNode<int>* help(vector<int> &pre,int &i,int bound){
    if(i>=pre.size() || pre[i]>=bound)return NULL;
    TreeNode<int>* root=new TreeNode<int>(pre[i++]);
    root->left=help(pre,i,root->data);
    root->right=help(pre,i,bound);
    return root;
}
TreeNode<int>* preOrderTree(vector<int> &pre){
    // Write your code here.
    int i=0;
    return help(pre,i,INT_MAX);
}
