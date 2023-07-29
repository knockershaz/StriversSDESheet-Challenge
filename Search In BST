void inorder(BinaryTreeNode<int> *root,vector<int>&v)

{

    if(root)

    {

        inorder(root->left,v);

        v.push_back(root->data);

        inorder(root->right,v);

    }

}

bool searchInBST(BinaryTreeNode<int> *root, int x) {

    // Write your code here.

    vector<int>v;

    inorder(root,v);

    int low=0,high=v.size()-1;

    while(low<=high)

    {

        int mid=(low+high)/2;

        if(x==v[mid])

        {

            return true;

        }

        if(x>v[mid])

        {

            low=mid+1;

        }

        else

        {

            high=mid-1;

        }

    }

    return false;

}
