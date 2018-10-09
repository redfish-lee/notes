# Growth Functions

分析演算法好壞會用到

* 時間複雜度（Time Complexity ）
* 空間複雜度（Space Complexity）

Worst case running time --&gt; Upper bound of running time

時間複雜度在 n 很大的時候差別更明顯：

* **Dominating term**，當 n 越大時，成長最快項
  * ex., $$n^2+c_1n+c_2$$的決定項為 $$n^2$$

### Big-O

* 存在**正數**$$c,\ n_0$$，使得**對於所有**$$n ≥ n_0$$， 都符合 $$0 ≤ f(n) ≤ c\ g(n)$$的$$f(n)$$集合
* $$O(g(n))$$，includes all functions that are **upper bounded** by $$g(n)$$



### Big-Omega

* 存在**正數**$$c,\ n_0$$，使得**對於所有**$$n ≥ n_0$$， 都符合 $$0 ≤  c\ g(n) ≤ f(n)$$的$$f(n)$$集合
* $$Ω(g(n))$$，includes all functions that are **lower bounded** by $$g(n)$$



Theory of Computation

f\(n\) = Ω\(g\(n\)\) &lt;-&gt; g\(n\) = O\(f\(n\)\)

