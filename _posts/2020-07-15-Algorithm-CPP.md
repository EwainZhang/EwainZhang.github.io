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
    return null;
  }
}
```
