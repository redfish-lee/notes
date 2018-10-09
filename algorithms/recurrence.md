# Recurrence

### Basic

### Example: Hanoi Tower 

#### 3 rules: 

* 由某個栓子移到另一個栓上
* 一次只能移動一個 disk
* 符合**小的必須在大的上方**

![](https://www.dropbox.com/s/bqpx6jipwdey8xc/Screenshot%202018-09-30%2000.52.40.png?dl=0)

![Mathematics for Computer Science, Eric Lehman](../.gitbook/assets/image%20%286%29.png)

* **3** pegs \(**A, B, C**\) and **N** disks \(on **A**\)，定義`T(N-1, start, aux, end)`
  * 先移動最大塊的到目標 \(end\)：
    * `T(N-1, start, end, aux)`
    * `T(1, start, aux, end)`
  *  再把剩下 N-1 個 disks 移到目標 \(end\)
    * `T(N-1, start, end, aux)`
* 複雜度

![](../.gitbook/assets/image%20%289%29.png)

