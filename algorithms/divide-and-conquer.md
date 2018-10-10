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



