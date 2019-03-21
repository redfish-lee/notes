# Complexity

分析演算法好壞取決於不同角度：

* 時間複雜度（Time Complexity ）
* 空間複雜度（Space Complexity）

## Magnitude order

當 n 越大的時候的函數趨勢：

 $$log_2n < n < n\ log_2 n < n^2 < 2^n < n!$$

### Polynomial Time

> An algorithm is said to be of polynomial time if its running time is **upper bounded by a polynomial expression** in the size of the input for the algorithm. ex, $$log_2n ,\  n ,\ n\ log_2 n,\ n^2$$

### Exponential Time

時間複雜度**不能**被 Polynomial function bound 住的， $$ex: 2^n,\ n!$$

#### Pitfall: 當有兩個演算法分別是 $$O(n^3)$$ 與 $$O(n)$$，則後者一定跑得比較快？

NO! 這個問題的關鍵在於 n 的大小，當 n 極大或是超過某個 n0 後，前者會呈指數上升，但是如果 n 極小的話， 前者是有可能較快的

example: $$Algo_1 = n^3,\ Algo_2=100n$$ ，則 $$n<10$$ 都是前者較快

## Notation

### Big-O

* 存在**正數**$$c,\ n_0$$，使得**對於所有**$$n ≥ n_0$$， 都符合 $$0 ≤ f(n) ≤ c\ g(n)$$的$$f(n)$$集合
* $$O(g(n))$$，includes all functions that are **upper bounded** by $$g(n)$$

一個演算法的 Upper-bound 取決於 worst case running time.

### Big-Omega

* 存在**正數**$$c,\ n_0$$，使得**對於所有**$$n ≥ n_0$$， 都符合 $$0 ≤  c\ g(n) ≤ f(n)$$的$$f(n)$$集合
* $$Ω(g(n))$$，includes all functions that are **lower bounded** by $$g(n)$$



Theory of Computation

f\(n\) = Ω\(g\(n\)\) &lt;-&gt; g\(n\) = O\(f\(n\)\)



