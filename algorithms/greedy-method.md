# Greedy Method

* 在一連串的選擇中做 local optimal decision 會在最終產生 global optimal solution
* 只有少數 optimization problem 可以使用 Greedy
* 但大部分問題仍可以用 Greedy 找到近似解 \(acceptable solution\)

## Minimum Spanning Tree

A minimum spanning tree of _**G**_ is a spanning tree of _**G**_ with the smallest total weight.

* 假設 $$G=(V,E),\ |V|=n,\ |E|=m$$
* 邊數： $$|E'|=|V|-1$$
* * 滿足 spanning tree \(點之間連通 connected\)

### Brute-force method:

* $$n^{n-2} $$ possible spanning trees for $$n$$ points
* **Exponential** time complexity

### Greedy method:

* **Kruskal’s** algorithm: $$O(m\ log\ m)$$
* **Prim’s** algorithm: $$O(n^2)$$

