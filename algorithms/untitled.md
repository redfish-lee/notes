# Sorting

> **Defn: Sorting 是把一序列值由小到大排列**

* sorting 會影響 search 的速度，sorted 會比較快

### Insertion Sort

![Algorithm: Insertion Sort](../.gitbook/assets/image%20%281%29.png)

#### 說明

* 想成撲克牌由小排到大，每抽一張新牌都會與前面的牌作比較，若比前一個小就一直往前順移
* `i`是前一張牌的 index，若新牌比 `A[i]`還大，所在位置就會在`A[i+1]`

#### 分析

* 時間複雜度： $$T(n) = O(n^2)$$

### **Selection sort**

![Algorithm: Selection Sort](../.gitbook/assets/image%20%283%29.png)

#### 說明

* 找到最小的值與`A[1]`交換，再找第二小的值與`A[2]`交換，以此類推

#### 分析

* 時間複雜度： $$T(n) = O()$$

### Merge Sort

![Algorithm: Merge Sort](../.gitbook/assets/image%20%286%29.png)

#### 說明

* **Divide and Conquer**
  * Split 成兩個 list 分別做 sorting
  * **Merge** 兩個 **sorted** **list**
  * \*\*\*\*
* 需要一個新的 list 空間

#### 分析

* 時間複雜度： $$T(n) = 2T(n/2) + c_1n = c_1 n\ log\ n + c_2 n =O(n\ log\ n)$$
* Merge Sort is **asymptotically** faster than Insertion Sort

