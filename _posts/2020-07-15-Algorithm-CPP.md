### Storage and basic operation of binary tree
**storage structure**

```C++
struct node
{
  typename data; 
  node* lchild;
  node* rchild;
}

// create root
node* root = NULL;

// create new node
node* newNode(int v)
{
  node* Node = new node;
  Node->data = v;
  Node->lchild = Node->rchild = NULL;
  return Node;
}
```

**2. seraching and revising of the node in binary tree**
```C++
void search(node* root, int x, int newdata)
{
  if(root = NULL)
  {
    return null; // empty tree
  }
  if(root->data == x) 
  {
    root->data = newdata;
  }
  search(root->lchild, x, newdata);
  search(root->rchild, x, newdata);
}
```

**3. inseart**
```C++
void insert(node* &root, int x)
{
  if(root == NULL)
  {
    root = newNode(x);
    return;
  }
  if( ...)
  {
    insert(root->lchild, x);
  }
  else
  {
    insert(root->rchild, x);
  }

}
```


***4. creation*
```C++
node* Create(int data[], int n)
{
  node* root = NULL;
  for(int i = 0; i < n; i++)
  {
    insert(root, data[i]);
  }
  return root;
}
```
