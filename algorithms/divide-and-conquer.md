# Divide-and-Conquer

## Introduction:

* 一種將大問題**拆分**成小問題**遞迴**求解的演算法
* 主要分成 3 個步驟：

  1. **Divide**, 把一個問題切成數個子問題（subproblem與原問題是同類型問題，只是較小）
  2. **Conquer**, 用遞迴方式分別對 subproblem 求解，直到遞迴到子問題夠小，可直接解決
  3. **Combine**, 把子問題的解法帶進原問題得出所求

* 
## Example

### Max-subarray problem

給一含有正負數的 list，找到一 subarray（連續）有最大的數字和

#### 暴力法：

* 有 $$n \choose 2$$ 個可能性，分別為$$S\ [\ i,\ j\ ]$$ 
* 每個 subarray 要相加需要 $$O(n)$$，共需要 $$O(n^3)$$ 
* 因為有重複的計算： $$S[i,\ j+1] = S[i,\ j] + A[j+1]$$，所以可縮減至 $$O(n^2)$$ 

#### 遞迴法：

* `max(leftSubarrMax(), rightSubarrMax(), crossmidMax()`
* $$T(n) = O(n\ log\ n)$$ 

## Strassen's Matrix Multiplication

利用「2個2x2矩陣相乘，至少需要 7 個 multiplications \([reference](https://ccjou.wordpress.com/2013/06/04/%E5%88%86%E6%B2%BB%E7%9F%A9%E9%99%A3%E4%B9%98%E6%B3%95%E2%94%80%E2%94%80strassen-%E6%BC%94%E7%AE%97%E6%B3%95/)\)，所以時間上

$$
T(n) = 7\ T(\frac{n}{2}) + \Theta(n^2)=\Theta(n^{lg\ 7})=\Theta (n^{2.81}) <\Theta(n^3)
$$

推廣到 kxk 矩陣，最佳 upperbound $$O(n^{2.376})$$

