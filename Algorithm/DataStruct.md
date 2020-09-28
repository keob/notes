### 前言

常见的数据结构分为 [线性数据结构] 与 [非线性数据结构]

- 线性数据结构
    1. 数组 (Array)
    2. 表 (Linked List)
    3. 栈 (Stack)
    4. 队列 (Queue)

- 非线性数据结构
    1. 树 (Tree)
    2. 堆 (Heap)
    3. 散列表 (Hashing)
    4. 图 (Graph)

#### 链表

链表以节点为单位，每个元素都是一个独立对象，在内存空间是非连续的。链表的节点对象具有连个成员变量: [值 val], [后继节点引用 next]

```go
type ListNode {
    val int
    next *ListNode
}
```

#### 栈

栈是一种具有 [后进先出] 特点的抽象数据结构，可以使用数组或者链表实现。

```go
type Stack struct {
    data int
    next *Stack
}
```

#### 队列

队列是一种具有 [先进先出] 特点的抽象数据结构，可使用链表实现。

```go
type Queue struct {
    data int
    next *Queue
}
```

#### 树

树是一种非线性数据结构，根据子节点的数量可分为 [二叉树] 和 [多叉树]，最顶层的节点成为 [根节点 root]。以二叉树为例，每个节点包含三个成员变量：[值 val]、[左子节点 left]、[右子节点 right]。

```go
type TreeNode struct {
    val int
    left *TreeNode
    right *TreeNode
}
```

#### 图

图是一种非线性数据结构，由 [节点(顶点) vertex] 和 [边 edge] 组成，每条边连接一对顶点。根据边的方向有无，图可分为 [有向图] 和 [无向图]。

```go
type Node struct {
    Val int
}

type Graph struct {
    nodes []*Node
    edges map[Node][]*Node
}
```

#### 散列表

散列表是一种非线数据结构，通过 Hash 函数将指定的 [键 key] 映射至对应的 [值 value]，以实现高效的元素查找。

```go
type Hash struct {
    key interface{}
    val interface{}
    next *Hash
}
```

#### 堆

堆是一种基于「完全二叉树」的数据结构，可使用数组实现。以堆为原理的排序算法称为「堆排序」，基于堆实现的数据结构为「优先队列」。堆分为「大顶堆」和「小顶堆」，大（小）顶堆：任意节点的值不大于（小于）其父节点的值。

```go
type Heap struct {
    val []int
}
```
