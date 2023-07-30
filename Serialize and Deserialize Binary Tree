#include<bits/stdc++.h>
string serializeTree(TreeNode<int> *root)
{
 //    Write your code here for serializing the tree
 string s;
 if(root==NULL)return "";
 queue<TreeNode<int>*>q;
 q.push(root);
 while(!q.empty()){
     TreeNode<int>*cur=q.front();
     q.pop();
     if(cur==NULL){
        s.append("#,");
     } else {
       s.append(to_string(cur->data) + ',');
     }
     if (cur != NULL) {
       q.push(cur->left);
       q.push(cur->right);
     }
  }
return s;
}

TreeNode<int>* deserializeTree(string &data)
{
  if(data.size()==0)return NULL;
  stringstream s(data);
  string str;
  getline(s,str,',');
  TreeNode<int>* root=new TreeNode<int>(stoi(str));
  queue<TreeNode<int>*>q;
  q.push(root);
  while(!q.empty()){
      TreeNode<int>* cur=q.front();
      q.pop();
      getline(s,str,',');
      if(str=="#"){
          cur->left=NULL;
      }else{
          TreeNode<int>* l=new TreeNode<int>(stoi(str));
          cur->left=l;
          q.push(l);
      }
      getline(s,str,',');
      if(str=="#"){
          cur->right=NULL;
      }else{
          TreeNode<int>* r=new TreeNode<int>(stoi(str));
          cur->right=r;
          q.push(r);
      }
  }
  return root;
}
