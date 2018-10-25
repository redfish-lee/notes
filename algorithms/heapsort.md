# Heapsort

## Heap

* heap \(binary heap\) 是一種 binary tree
* 符合 **Shape Property**
  * 除最底層外，每層須填滿 \(none-deepest layers must be fullyfilled\)
  * 填滿順序由左至右
* 符合 **Heap Property**
  * $$node\ 值\leq it's\ children\ 值$$
  * $$root's\ value\ (minimum)$$
  * 也叫做 min-heap

### Basic Operations

* `FindMin`，root 就是 min，$$O(1)$$ 
* `Extract-Min`，刪除並重選 root，$$O(log\ n)$$
  * 複製最後一個節點到 root
  * 刪除最後結點
  * 重新 locate root 到新位置 \(一直swap下去\)
    * 與 children 中較小的作交換，直到所有 children 均大於此 node
* `Insert`，加入一個點到 heap 中，$$O(log\ n)$$
  * 新增節點到最後
  * 與 parent 比較，較小就往上交換，直到比 parent node 大

### Advanced Operations

* Heapify

### Array Representation

![Max Heap](../.gitbook/assets/image%20%2815%29.png)

* heap index 由 1 ~ n
* node `x` ****的 **children node** 分別為 `2x`, `2x+1` 
* node `x` 的 **parent node** 是 $$\left \lfloor{\frac{x}{2}}\right \rfloor$$ 
* 不需要額外 tree pointer 即可用 index 定址

## Heapsort

* 用 heap 做 sorting
* 用上述 methods 可以得到一個 sorted array
* 時間複雜度： $$n\times O(log\ n) +n\times O(log\ n) = O(n\ log\ n)$$ 

```cpp
for i = 1 to n:
    heap.insert(i)
for i = 1 to n:
    heap.extract_min()
```

## Priority Queue

* heap 可以用來實作高效率 priority queue



