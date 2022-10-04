# 题型总结笔记
###### tags: `Leetcode`
**Leetcode数据规模和时间复杂度对照**
![](https://i.imgur.com/T2w2aQi.png)
## Two Pointers
[0392. Is Subsequence](https://leetcode.com/problems/is-subsequence/)\
[0611. Valid Triangle Number](https://hackmd.io/0K3tNOyPQcCkRxZZQUvD8A)\
[0360. Sort Transformed Array](https://hackmd.io/VIjmADEcT4agS3ZiY7s5zg)\
[1793. Maximum Score of a Good Subarray](https://hackmd.io/ulPJ8HGcQEu7FhX_jrQYpA)(经典)\
[2337. Move Pieces to Obtain a String](https://hackmd.io/PhWeQn2_SjSyIYg7L2iuWg)\
[0777. Swap Adjacent in LR String](https://hackmd.io/L9wvI1fuSsqwKi6FcPwI6g)
### Two Sum(经典)
[1885. Count Pairs in Two Arrays](https://hackmd.io/JJb56E1kTviOjH2qQcEE6A)
### Unfamiliar
[1989. Maximum Number of People That Can Be Caught in Tag](https://hackmd.io/jVv97NtYShW7sWhHjV7jMw)
### Merge Intervals
#### base: 
给两个array list，找出交集
先排序然后双指针 注意退出回圈的条件是两个指针都到头还是一个到头即可\
[1229. Meeting Scheduler](https://hackmd.io/V7zW3AraQ9CIANAhGv2HkQ)\
[0986. Interval List Intersections](https://hackmd.io/1oCvBXRuRsSWPuKUItw3Gg)
#### more general:
两个sequence 两个指针一个个跑\
[2098. Subsequence of Size K With the Largest Even Sum](https://)
### Sliding Window
- 看到substring就应该想到sliding window
- 如果我们依次递增地枚举子串的起始位置，那么子串的结束位置也是递增的！那么就可以使用「滑动窗口」来解决这个问题了
- 如何计算subarray sum小于某个数的subarray个数: 只要当前的l和r满足条件 ```cnt+=r-l+1``` 相当于每次是算以r为右边界的满足条件的subarray数量 ([1918. Kth Smallest Subarray Sum](https://hackmd.io/jyl8yjzlRFOLeg1_ctbjAg))
#### Fixed Length Sliding Window
用for回圈遍历 先加上新的值 如果已经超过长度再减去最左边的值 最后更新答案\
    [1052. Grumpy Bookstore Owner](https://hackmd.io/O8aCAsHdTFuhSo6Ikuvk5A)\
    [0438. Find All Anagrams in a String](https://hackmd.io/MvGWdMIxQZ26uuetxx6l_g)
#### Unfixed Length Sliding Window
while回圈遍历 先加上新的值 如果window里面的value invalid 跑**while**回圈挪left pointer一直到valid为止 **(在回圈外面)** 更新答案\
    [2024. Maximize the Confusion of an Exam](https://hackmd.io/fQOTPNnqT-SfFNKxzOpCag)
##### Sliding Window for Number Sequence
大部分时候不需要用prefixsum 还比较节省空间\
[1004. Max Consecutive Ones III](https://hackmd.io/LbO10-8UTDWGIJX2A4cEfA)\
[0209. Minimum Size Subarray Sum](https://hackmd.io/WyUTJHs1S7WjYBfNeuB37A)
##### Sliding Window for Distinct Characters
[0003. Longest Substring Without Repeating Characters](https://hackmd.io/-bC_ZG1BR2isaDfCleju6Q)\
[0076. Minimum Window Substring](https://hackmd.io/z50NoPGOTlOtJcP9sBE5nw)
#### Unfamiliar
[0930. Binary Subarrays With Sum](https://hackmd.io/wHpz7ueHSeyRa9d9hQBIdw)\
[1658. Minimum Operations to Reduce X to Zero](https://hackmd.io/sSVu2nTaT3mIxUfVX337PQ)\
[2271. Maximum White Tiles Covered by a Carpet](https://hackmd.io/7FnX3SCASZyuEec1uVk90w)
#### 形似sliding window但是不完全用sliding window解
[1156. Swap For Longest Repeated Character Substring](https://hackmd.io/R4opMwT2Qg-a-PnLmsS59g)\
[1763. Longest Nice Substring](https://hackmd.io/cIMdRw03R_iRQtFsbS7kNA)
## HashMap
考虑特殊情况
2sum问题和[0532. K-diff Pairs in an Array](https://hackmd.io/u9NqEI8aRV6-nCSd0VCRVw)和[2131. Longest Palindrome by Concatenating Two Letter Words](https://hackmd.io/mOO7zW3vQmqlS-HZNFr2tg) 如果diff=0，或者target sum减完当下数字还等于当下数字，那么这时候就要**重复使用同一个entry** 所以要特别讨论
还有[1573. Number of Ways to Split a String](https://hackmd.io/zf8Tv_oOT7WQ1jNGMJRBag) 如果total sum是0的时候
**注意subsequence和subarray的区别**
[0594. Longest Harmonious Subsequence](https://hackmd.io/EzxIF4I_Q3mBgZFa4u9c4w)

[0532. K-diff Pairs in an Array](https://hackmd.io/u9NqEI8aRV6-nCSd0VCRVw)\
[2131. Longest Palindrome by Concatenating Two Letter Words](https://hackmd.io/mOO7zW3vQmqlS-HZNFr2tg)\
[0170. Two Sum III - Data structure design](https://hackmd.io/cX8JgC3tSgeGhDgZX-mKww)\
[0409. Longest Palindrome](https://hackmd.io/ugAR5vc4R4OoCqZkH9SooA)\
[1573. Number of Ways to Split a String](https://hackmd.io/zf8Tv_oOT7WQ1jNGMJRBag)\
[0594. Longest Harmonious Subsequence](https://hackmd.io/EzxIF4I_Q3mBgZFa4u9c4w)
### 变式
[0890. Find and Replace Pattern](https://hackmd.io/q5X-Wx7nRlW9lCF0PtLeyQ)\
[0128. Longest Consecutive Sequence](https://hackmd.io/xQ0F7nSeRUqZ3CabQjFQxg)\
[0438. Find All Anagrams in a String](https://hackmd.io/MvGWdMIxQZ26uuetxx6l_g)
### HashMap + Prefix
**做法: 先建map 然后遍历 如果现在的值在map里面遇到过 更新答案
跟sliding window的场景其实有点像 都是找满足条件的subarray
但这个是通过'-'来得到的 这个value前面出现过一次 这次又出现了 那么中间的就是答案
但sliding window的就是两个指针一个往右挪了 另一个只能往右挪 不可能需要往左**

想好是不是固定size 是的话用array 否的话用map
map建好之后跑回圈之前 通常要先放一个值 **如果是算substring prefixSum通常放(0,-1)** (因为还没开始遍历array的时候值是0), **如果是算count 通常放(0,0)**
详见下面几题

[1524. Number of Sub-arrays With Odd Sum](https://leetcode.com/problems/number-of-sub-arrays-with-odd-sum/)\
[0974. Subarray Sums Divisible by K](https://hackmd.io/kqI87VXXQ-6je55xfvQzPw)\
[1658. Minimum Operations to Reduce X to Zero](https://hackmd.io/sSVu2nTaT3mIxUfVX337PQ)\
[0325. Maximum Size Subarray Sum Equals k](https://hackmd.io/9tY6qpjqQrCaw0E2mlr9ZA)
#### 变式
##### 看到array只有1和0, 就把0变成-1
[0525. Contiguous Array](https://hackmd.io/gvM6GJYHStmB-OH0bKr8sQ)\
[1983. Widest Pair of Indices With Equal Range Sum](https://hackmd.io/NvYEEEPfTIup5ztyaBM4qw)\
[1915. Number of Wonderful Substrings](https://hackmd.io/0NLt0f9ZQnicvBhDgaKRIg)\
[1371. Find the Longest Substring Containing Vowels in Even Counts](https://hackmd.io/vqzHHM8YQhyHFc1m21Ja3g)\
[1542. Find Longest Awesome Substring](https://hackmd.io/rSECrNhOTt28MGEvqBhksw)
前两题是同一个类型 后三题是同一个类型

## Binary Search
**万事不决用binary search**
- 判断一道题能不能用binary search解: 如果找到一个无效解，是不是后面的或者前面的解都可以抛弃
- 如果while里面用<= if和else的判断里面就一个是mid+1一个是mid-1
因为最极限的条件是 start==end 如果不这样写就会一直卡在start=end
- 如果while里面用< if和else里面就一个是```l=mid+1``` 一个是```r=mid```,因为极限的条件是start==end-1，这时候mid会等于start
- 考虑```end = nums.length-1```还是```end = nums.length```([0034. Find First and Last Position of Element in Sorted Array](https://hackmd.io/o124knmVT7KGKOjTPFUCAg))
- 考虑```if(nums[mid]<target)```还是```if(nums[mid]<=target)```([0034. Find First and Last Position of Element in Sorted Array](https://hackmd.io/o124knmVT7KGKOjTPFUCAg)) 如果是后者那么搜索的end不能是nums.length而要是nums.length+1
- ```mid = start+(end-start)/2```
- 如果是找minimum就找满足条件的第一个, 如果是找maximum就```if(nums[mid]<=target)```找大于target的第一个，然后再看start-1是否满足条件([1552. Magnetic Force Between Two Balls](https://hackmd.io/9umUWs4TTpyJCtBqrxkm-Q))\

[0033. Search in Rotated Sorted Array](https://hackmd.io/-HbelXktSrWIauaJrmoYsg)(经典)\
[0081. Search in Rotated Sorted Array II](https://hackmd.io/ppsp0g2ERh2wXE2dlxoQzQ)(经典)\
[0153. Find Minimum in Rotated Sorted Array](https://hackmd.io/YowIFBGsR3Couqh759r3lg)\
[0034. Find First and Last Position of Element in Sorted Array](https://hackmd.io/o124knmVT7KGKOjTPFUCAg)\
[1533. Find the Index of the Large Integer](https://hackmd.io/tIGKI9WWSlax9KtRX2_TyQ)\
[0302. Smallest Rectangle Enclosing Black Pixels](https://hackmd.io/P2FTEvAIQgeF_rYLoV7ylg)\
[0300. Longest Increasing Subsequence](https://hackmd.io/oPc5yL1oRhGtGP8UdRd3_g)\
[2389. Longest Subsequence With Limited Sum](https://hackmd.io/l5hF6FN6T66hno-ndYrvsw)\
[2426. Number of Pairs Satisfying Inequality](https://hackmd.io/ngD98TVUSXOEOUP66nF-lQ)
### Binary Search by Value
[1011. Capacity To Ship Packages Within D Days](https://hackmd.io/w9w2BtjpSsiVqhx9rhPGkQ)\
[1231. Divide Chocolate](https://hackmd.io/gB-3GUnbTzK2u0WNO6Yzxw)\
[1482. Minimum Number of Days to Make m Bouquets](https://hackmd.io/AEdtJ2k3TV-eQFe2cSo-UA)\
[1552. Magnetic Force Between Two Balls](https://hackmd.io/9umUWs4TTpyJCtBqrxkm-Q)\
[1870. Minimum Speed to Arrive on Time](https://hackmd.io/Lnohx5RtSya88dF3AL669w)\
[1891. Cutting Ribbons](https://hackmd.io/PlElcBsiTKSfWsxtn67wfA)
#### 重点复习
[1802. Maximum Value at a Given Index in a Bounded Array](https://hackmd.io/iLs1pcNwRm-KAwBQH_dMVA)\
[1608. Special Array With X Elements Greater Than or Equal X](https://hackmd.io/MjTGRGldSjKggKI-WXKzlw)\
[1300. Sum of Mutated Array Closest to Target](https://hackmd.io/AmhQgOSXQxuiuYJeTOymSQ)\
[2141. Maximum Running Time of N Computers](https://hackmd.io/A9EfBVIaSpm7SSmh07AeIQ)\
[1508. Range Sum of Sorted Subarray Sums](https://hackmd.io/1a4nVnUrR-WYq4H9jTHX4w)
[2250. Count Number of Rectangles Containing Each Point](https://hackmd.io/YVGJtsfjQwOcriojK3gErQ)
### K-th Element
[1918. Kth Smallest Subarray Sum](https://hackmd.io/jyl8yjzlRFOLeg1_ctbjAg)

## TreeMap
treemap 要确保key不会重复才能用
当你需要给特定值找已经存在的值里面最接近的值的时候需要用到heap
当用到ceiling或者floor的函数的时候并且把结果赋给某一个变量的时候用Integer/Long 定义变量 因为ceiling和floor函数有可能传null回来

TreeMap 
```ceilingKey()/floorKey()``` 是找高于或等于自己的key 
```higherKey()/lowerKey()``` 是找高于/低于自己的key(不包含等于)

[1296. Divide Array in Sets of K Consecutive Numbers](https://hackmd.io/uG7m4jX7QK6TAVd1wOYvoQ)\
[0220. Contains Duplicate III](https://hackmd.io/tCC_eBr4Rc-XKqia8Cz9xA)\
[1488. Avoid Flood in The City](https://hackmd.io/gKFb3WZtR3eNxikpO1CJpw)\
[1606. Find Servers That Handled Most Number of Requests](https://hackmd.io/y7AOPFnTRgymeyjvmtiwgw)\
[0729. My Calendar I](https://hackmd.io/am3vFQC-TeuImofwjISHjQ)\
[0870. Advantage Shuffle](https://hackmd.io/w0INiSnmSJOkU2puietlOw)\
[0975. Odd Even Jump](https://hackmd.io/OjMVidnIS_6qXPD7UctFsQ)
## Priority Queue
常规模版:（以时间顺序为例）
1. 先排序array
2. 然后for回圈遍历array
    a. 遍历时首先把离开时间比当前array到达时间早的从pq里面拿走
    b. 处理当前array
### 基本型
[1942. The Number of the Smallest Unoccupied Chair](https://hackmd.io/n9Rv-wxdTSKJl3yIWP4PaA)\
[1705. Maximum Number of Eaten Apples](https://hackmd.io/hVhh2RqqQ7yNlfdOkQMqIQ)\
[1834. Single-Threaded CPU](https://hackmd.io/1JHCWsJhQWKUnM5K90N1OA)\
[0502. IPO](https://hackmd.io/Af42eXaAQRWOGaUvFKj_tA)
### 变式
[0295. Find Median from Data Stream](https://hackmd.io/3lwAk5mCSp-4Hb_1osocdg)\
[1792. Maximum Average Pass Ratio](https://hackmd.io/BbRp_dzORMCJsamRv-Ys4w)\
[1801. Number of Orders in the Backlog](https://hackmd.io/iKDFgeW4Q3CuNdp_2JFHiA)
### Greedy Algorithm+Priority Queue
[1705. Maximum Number of Eaten Apples](https://hackmd.io/hVhh2RqqQ7yNlfdOkQMqIQ)\
[1792. Maximum Average Pass Ratio](https://hackmd.io/BbRp_dzORMCJsamRv-Ys4w)\
[0502. IPO](https://hackmd.io/Af42eXaAQRWOGaUvFKj_tA)
#### 区间最值* 区间总和
[1383. Maximum Performance of a Team](https://hackmd.io/bKCHp-8yTLi42s5emUM0WQ)\
[0857. Minimum Cost to Hire K Workers](https://hackmd.io/Ssaze_deSyi6x6qnHjWwHw)
### Priority Queue+TreeMap
[1488. Avoid Flood in The City](https://hackmd.io/gKFb3WZtR3eNxikpO1CJpw)\
[1606. Find Servers That Handled Most Number of Requests](https://hackmd.io/y7AOPFnTRgymeyjvmtiwgw)
### Task Scheduler
都是借用了priority queue的idea 但是用了桶排序 因为元素个数都是有限的
如果不能有repeat pattern 那么先排出现次数最多的再排别的(前三题)
[0767. Reorganize String](https://hackmd.io/Cs2YBT2RQHOFLNcLLFBPOQ)\
[1054. Distant Barcodes](https://hackmd.io/5RbR4Q9pRBKgIMKYQjgxQg)\
[1953. Maximum Number of Weeks for Which You Can Work](https://hackmd.io/d3qZmsx9SPGPnFdA_pMmHA)\
[0984. String Without AAA or BBB](https://hackmd.io/126E-vGIQQ25yC6GA8kgxg)

## Stack
[0341. Flatten Nested List Iterator](https://leetcode.com/problems/flatten-nested-list-iterator/)\
[0388. Longest Absolute File Path](https://hackmd.io/ZRs4b2URSx2lUMuYX7uMdA)
### Monotonic Stack
可以**解决一些subarray问题** 但解决的不全都是subarray问题
找next biger/smaller
"**window max**" 可以简化成next smaller item
"**window min**" 可以简化成next bigger item
**next bigger item** -> monotonic **decreasing** stack
**next smaller item** -> monotonic **increasing** stack
**prev bigger item** ->monotonic **decreasing** stack
**prev smaller item** -> monotonic **increasing** stack
[1019. Next Greater Node In Linked List](https://hackmd.io/OZOq7H72T5m_AFULsw5Keg)\
[1856. Maximum Subarray Min-Product](https://hackmd.io/rExGf0PFSy6pQxyJtyGvtQ) (Window题)(可以和[1383. Maximum Performance of a Team](https://hackmd.io/bKCHp-8yTLi42s5emUM0WQ)以及[0857. Minimum Cost to Hire K Workers](https://hackmd.io/Ssaze_deSyi6x6qnHjWwHw)对比)\
[1063. Number of Valid Subarrays](https://hackmd.io/wkf9N1CaSWW5hIU-kUKRdA)\
[1966. Binary Searchable Numbers in an Unsorted Array](https://hackmd.io/6ibIKe8mS6CLGc2L6c9NWw)\
[1063. Number of Valid Subarrays](https://hackmd.io/wkf9N1CaSWW5hIU-kUKRd)
#### Rectangle 问题
[1504. Count Submatrices With All Ones](https://hackmd.io/86AP-3gOTmeWP2XtzCr1bg)\
[0084. Largest Rectangle in Histogram](https://leetcode.com/problems/largest-rectangle-in-histogram/)\
[0085. Maximal Rectangle](https://hackmd.io/fMmT7YdPSs-VEYCIM3l5RA)
#### 变式
[2334. Subarray With Elements Greater Than Varying Threshold](https://hackmd.io/J7te9Rc7TOmTGz840T33UA)(Window题)
### Form Smallest Subsequence
[1081. Smallest Subsequence of Distinct Characters](https://hackmd.io/uZ9YopCBTDGfS8ZQr3pFIQ)\
[1673. Find the Most Competitive Subsequence](https://hackmd.io/bRx7W6cxS6u4vEUHdCPu8g)\
[0402. Remove K Digits](https://hackmd.io/sgShdZ1FTqC0ub_yodHsbw)
### 双栈
[0155. Min Stack](https://hackmd.io/YE_lfAhhTTu2hd6DL22-wg)\
[1209. Remove All Adjacent Duplicates in String II](https://hackmd.io/DOeKtFMuSZydHPXVbKsYyA)
### 处理字符串
StringBuilder也可以看成stack
[1209. Remove All Adjacent Duplicates in String II](https://hackmd.io/DOeKtFMuSZydHPXVbKsYyA)\
[0856. Score of Parentheses](https://hackmd.io/X4dO8hpbSPyyZxmQJsIHvg)\
[0536. Construct Binary Tree from String](https://hackmd.io/m2_jgwwmS_iaxJ3Md55TKQ)\
[2296. Design a Text Editor](https://hackmd.io/5plBCFBITgSgW3uYFd9KoQ)
### Parse Expression
[0071. Simplify Path](https://hackmd.io/H8c-FO0TTOqNL5dacNZexA)\
[0224. Basic Calculator](https://hackmd.io/vwa99ktZThW6SxLy8R1kBQ)\
[0227. Basic Calculator II](https://hackmd.io/qV1I9kI-SMOLDSTyy744Ag)\
[0772. Basic Calculator III](https://hackmd.io/KNnsw05_QaGBO_nSjA-SSQ)

## DFS
如果recursion里面不同分支只要有一个true 别的分支都不用看的话 就不需要记录每个node的结果([1306. Jump Game III](https://hackmd.io/DXDGFRc1SR2nttSNOosUYQ))
否则就需要记录每个node的结果
[1306. Jump Game III](https://hackmd.io/DXDGFRc1SR2nttSNOosUYQ)\
[0200. Number Of Islands](https://hackmd.io/qbl68ROHQEObty3jQK_ItA)\
[0417. Pacific Atlantic Water Flow](https://hackmd.io/J7U3OUnKRkqjNbp2Pmjy_Q)

### Backtracking
backtracking 模版:
1. backtracking函数通常不用返回任何值
2. 先写什么时候把答案加进result里面(通常是```start==nums.length```)
3. 什么时候这条分支不需要再往下遍历(直接return)
4. 最后写处理过程(用for回圈遍历所有可能值)

需要注意的是
1. 每次为了形成一个新的分支 call recursion 改了哪个变量都一定要改回来(不论是map还是set)
2. 把答案加进result里时如果result的形式是```List<List<Integer>> result``` 要写成```result.add(new ArrayList<>(curr))``` 不然curr在backtracking过程中改变也会改变result
3. 如果答案最后都装进list里面 那么这个list不用设成全域变量 只要设成backtracking的参数就好， 但如果答案是一个数(例如max number)那么就需要用到全域变量 不然一个分支的更新 另一个分支不会知道（因为function的参数没有改变）[2065. Maximum Path Quality of a Graph](https://hackmd.io/UDM6SdAcT4Guenxlh0uDyw)
4. 涉及到abbreviation类型的backtracking一定要小心 因为不确定abbreviation的数字长度 所以不能像其他题目一样dfs之后直接把最后一个element删掉就可以了 而是需要在末尾加上```curr.setLength(len);```([0320. Generalized Abbreviation](https://hackmd.io/b9bB2QFORuKd1-H3IFa1qg))

[0291. Word Pattern II](https://hackmd.io/q2HesIT7QYGgCs9af25H-Q)\
[2065. Maximum Path Quality of a Graph](https://hackmd.io/UDM6SdAcT4Guenxlh0uDyw)\
[0051. N-Queens](https://hackmd.io/6tGOdEXDT8GTeS9bRC8sbQ)\
[0131. Palindrome Partitioning](https://hackmd.io/iVZUy1SGQTKW8yTExda_Gw)(经典)\
[1593. Split a String Into the Max Number of Unique Substrings](https://hackmd.io/vV6OznDKRX2Gdcu6oBYkmw)\
[0320. Generalized Abbreviation](https://hackmd.io/b9bB2QFORuKd1-H3IFa1qg)\
[2277. Closest Node to Path in Tree](https://hackmd.io/l_H1yuFdQnG6gajhmXgPKA)\
[1240. Tiling a Rectangle with the Fewest Squares](https://hackmd.io/agLq_D4QS5aSiQkNGyjmpw)
#### Find Distinct Subset
[0090. Subsets II](https://hackmd.io/x0yhje8TSeWaIkIZf8NqHQ)\
[0040. Combination Sum II](https://hackmd.io/cOOug_AXSUeBnJKIjdF2IA)\
[0491. Increasing Subsequences](https://hackmd.io/zwyfgwfRQ0CKEFtYcMDiXQ)

### DFS + Memorization
**一般能用memo就用memo, 但是如果要把所有结果列出来通常就不需要memo了 浪费空间**

[0329. Longest Increasing Path in a Matrix](https://hackmd.io/4xn_ebSBSLufvgqkyA_ZcA)\
[2328. Number of Increasing Paths in a Grid](https://hackmd.io/nsHcqQhPTOCJE32B2RX5vA)\
[1986. Minimum Number of Work Sessions to Finish the Tasks](https://hackmd.io/69G6kfsHTLaMOO2GrBx7vw)\
[0638. Shopping Offers](https://hackmd.io/WtskTj8rRk6YWArb7av6ow)(经典)\
[0139. Word Break](https://hackmd.io/_c6UcaDWT9mWEQHdB3_XXQ)(经典)\
[0140. Word Break II](https://hackmd.io/nVBOAkUWR_OjK3NHME9cNQ)\
[0546. Remove Boxes](https://hackmd.io/T7eZJ9ZhQ9ayxS2ZVXdhKQ)(非常难想 没时间就跳过)
[0756. Pyramid Transition Matrix](https://hackmd.io/e3HHCquFQpu8yG7RXpJHvg)

### Min-max Strategy
需要memo记录之前算出的结果
根据题意定义memo的每一个state
如果是判断谁拿的多 就先算第一个拿的人能拿多少 再用减法算第二个人能拿多少

[1140. Stone Game II](https://hackmd.io/IoZ6byoxQeaeYyh8_KyJMg)\
[1510. Stone Game IV](https://hackmd.io/jhylOmfmSCOoZo3651za5A)\
[0464. Can I Win](https://hackmd.io/P3CBpte7Qx-dqoveApIuQg)\
[0877. Stone Game](https://hackmd.io/rj7ykKzAQgKOWaNOTOmArA)\
[1406. Stone Game III](https://hackmd.io/FmssWbuUSteq2qypavv7fw)
### Hidden Matrix
[1810. Minimum Path Cost in a Hidden Grid](https://hackmd.io/QXJ1rUebQCqcr0ukhsWqRg)
[0489. Robot Room Cleaner](https://hackmd.io/_C03LNMcRlmcmXRbL6l_BQ)
## BFS
- 层序遍历
  把检查有没有到target点放到```q.poll()```之后, 然后直接```return step``` step的初始值设成0
- 放入初始值的时候 记得把它设成visited 
- 不可以把visited和原来array合并的条件1: 一个点如果visited过 再碰到它这个branch就可以消灭了(反例：[0490. The Maze](https://hackmd.io/W1DGV3ZyRUWbzP7PQvYELw))
- 不可以把visited和原来array合并的条件2: 有多个起点 不能改变原本的值([2101. Detonate the Maximum Bombs](https://hackmd.io/rOk3kJMDTVmKA78Qi5Sxtw))
- 不可以把visited和原来array合并的条件3: array里面有0, 这样如果visited的值变成负的，还是会重复visit 值是0的地方([1102. Path With Maximum Minimum Value](https://hackmd.io/QjOZ8IEyRTOJiMtn94A1FQ))

[0490. The Maze](https://hackmd.io/W1DGV3ZyRUWbzP7PQvYELw)\
[0675. Cut Off Trees for Golf Event](https://hackmd.io/OMXUHlozQciKtoJAGyIYSA)\
[0637. Average of Levels in Binary Tree](https://hackmd.io/O02hytr6Sw6JqxXaVsh7Bg)\
[1311. Get Watched Videos by Your Friends](https://hackmd.io/evsplVXwSlKp9PMdpIoyfw)\
[1559. Detect Cycles in 2D Grid](https://leetcode.com/problems/detect-cycles-in-2d-grid/submissions/)
### 变式
[2290. Minimum Obstacle Removal to Reach Corner](https://hackmd.io/epsGYhK_RiyTjMBkNVjjbQ)\
[1345. Jump Game IV](https://hackmd.io/t815A4bBS7afy4tuNF_WqQ)\
[1905. Count Sub Islands](https://hackmd.io/Oc7KNiYpTvmDMssvniGlUg)\
[2101. Detonate the Maximum Bombs](https://hackmd.io/rOk3kJMDTVmKA78Qi5Sxtw)\
[0815. Bus Routes](https://hackmd.io/xIIdHbVeQw-PoiUYXnSv_A)\
[0785. Is Graph Bipartite?](https://hackmd.io/JhGlMsDdQB2981MMMjP-fQ)\
[1298. Maximum Candies You Can Get from Boxes](https://hackmd.io/8IPQAF1kSp-O8J_-KiiI1A)\
[0694. Number of Distinct Islands](https://hackmd.io/uEUuiD4sQpy-8RAc535uRg)\
[0529. Minesweeper](https://hackmd.io/pnoapkn9Teua5aUxxUemSw)\
[0127. Word Ladder](https://hackmd.io/2F_Qo1tWSH2QKrMp6USYEw)\
[0126. Word Ladder II](https://hackmd.io/v-B5QbO9Qk25KsytZOgaiw)\
[0838. Push Dominoes](https://hackmd.io/RpV2rwrSQiKg4YLc1erpYQ)
### Topological Sort
一个list of list的graph 一个int array记录每个点的degree
先把degree=0的加进queue里面 然后一点点bfs

[0210. Course Schedule II](https://hackmd.io/EzKnR3KLQayEp_SAYuXaYQ)\
[1136. Parallel Courses](https://hackmd.io/hP5U3AvSSwaPiBB4ch6Uaw)\
[2115. Find All Possible Recipes from Given Supplies](https://hackmd.io/Ksjixl-GS4i8IPUFVhLY0A)\
[2392. Build a Matrix With Conditions](https://hackmd.io/SSDkZWo3SKqk7RY65Yh7vQ)\
[2277. Closest Node to Path in Tree](https://hackmd.io/l_H1yuFdQnG6gajhmXgPKA)
#### 找到每个node的所有ancestor
再加一个list of set存每个node的所有ancestor
在做bfs的时候构建这个list of set\
[1462. Course Schedule IV](https://hackmd.io/QrubTV-KT9CEUdjsdvd7lw)\
[2192. All Ancestors of a Node in a Directed Acyclic Graph](https://hackmd.io/7kXmx7PKR7eZDMvhBWw5Bg)
#### undirected graph
每条边的两个方向都要加进graph里面 并且degree=1就可以加进queue\
[2204. Distance to a Cycle in Undirected Graph](https://hackmd.io/QScP4DXkT9GjyVku0oPLEA)
### Dijkstra (BFS+Priority Queue)
[1786. Number of Restricted Paths From First to Last Node](https://hackmd.io/AmqYoI20Rk-ea6Li25EmsA)\
[1810. Minimum Path Cost in a Hidden Grid](https://hackmd.io/QXJ1rUebQCqcr0ukhsWqRg)\
[1631. Path With Minimum Effort](https://hackmd.io/lWn1ryikSgOnvho6uAYZEw)\
[1976. Number of Ways to Arrive at Destination](https://hackmd.io/xxg1ck5lRmSDnAIrA0ZiCA)\
[1514. Path with Maximum Probability](https://hackmd.io/B7M8f6PUSdqHzZry7hDpSA)
#### 变式
找从起点到终点路径的最大的最小值或者最小的最大值
区别在于这里的题目：不需要记录从起点到现在点的最优解\
[1102. Path With Maximum Minimum Value](https://hackmd.io/QjOZ8IEyRTOJiMtn94A1FQ)\
[0778. Swim in Rising Water](https://hackmd.io/0P3Zi0RZQ1Stxj3pDvXciQ)
## Greedy Algorithm
### 典型题
[0055. Jump Game](https://leetcode.com/problems/jump-game/)\
[0045. Jump Game II](https://hackmd.io/eBarqjRNTIOUYBMU64wLKg)\
[0870. Advantage Shuffle](https://hackmd.io/w0INiSnmSJOkU2puietlOw)\
[2242. Maximum Score of a Node Sequence](https://hackmd.io/6XBAA7e4Sz2ttK3iSCFgwQ)\
[0910. Smallest Range II](https://hackmd.io/l0fVPqkiQG2vzFG1vErCNg)
#### Greedy+Sliding Window
[2271. Maximum White Tiles Covered by a Carpet](https://hackmd.io/7FnX3SCASZyuEec1uVk90w)
### 常规题
[0624. Maximum Distance in Arrays](https://hackmd.io/fWyuLHf9SK6RAiHQvWwU4w)\
[1578. Minimum Time to Make Rope Colorful](https://leetcode.com/problems/minimum-time-to-make-rope-colorful/)\
[1253. Reconstruct a 2-Row Binary Matrix](https://hackmd.io/50KYfhv-RdWejdAouFnyIQ)\
[2216. Minimum Deletions to Make Array Beautiful](https://hackmd.io/m7GV8k3IQsCLqiBz69_q5g)\
[2182. Construct String With Repeat Limit](https://hackmd.io/PR6JPID5RKeJ3-W7q8JMKw)\
[0670. Maximum Swap](https://hackmd.io/BRg5nV6yTJqspaUdaxQdSQ)\
[1727. Largest Submatrix With Rearrangements](https://leetcode.com/problems/largest-submatrix-with-rearrangements/)\
[1546. Maximum Number of Non-Overlapping Subarrays With Sum Equals Target](https://hackmd.io/hFLJpsHMT_2D499XIWuyYQ)\
[2311. Longest Binary Subsequence Less Than or Equal to K](https://hackmd.io/hm8hjl3tSLWBc0d3ttOUsg)\
**总结算长方形面积题目**
## Tree
[0572. Subtree of Another Tree](https://hackmd.io/oFMek64ETdCGrC_0NIR4rQ)\
[0958. Check Completeness of a Binary Tree](https://hackmd.io/EVLsEc5iTWCNbG3T710TgA)\
[1104. Path In Zigzag Labelled Binary Tree](https://hackmd.io/EVA8Pu5xSpWObcu4cf3uJw)\
[0226. Invert Binary Tree](https://hackmd.io/aaQaRXvoTXuEMxpnF9jU3Q)
### Binary Search Tree
[0098. Validate Binary Search Tree](https://hackmd.io/lTUSAW2EQVaTim1feD1YrA)\
[0285. Inorder Successor in BST](https://hackmd.io/nFez6sm8TD-eLu6PshxUfw)(经典)\
[0173. Binary Search Tree Iterator](https://hackmd.io/7BSUG7MBQ7mpEnKGhYW1YQ)\
[0235. Lowest Common Ancestor of a Binary Search Tree](https://hackmd.io/irC3SlpLSda4ljtH_iIVxg)
### dfs + Tree
[0110. Balanced Binary Tree](https://hackmd.io/qytkvtqYQQSKtQq8QP1x9g)(经典)
#### Path in a tree
需要一个global variable来存答案
因为每次dfs都只会找包含left/right child的subtree里的最优值(注意：一定是包含left/right tree)
但path需要把left subtree和right subtree的解加在一起\
[0543. Diameter of Binary Tree](https://hackmd.io/FPZpR3NBQuCV_u2vTZaEvQ)(经典)\
[0124. Binary Tree Maximum Path Sum](https://hackmd.io/mi68cm-8Sb6V2g0ZXwCy3Q)(经典)\
[1522. Diameter of N-Ary Tree](https://hackmd.io/lu9uAfWDSS6V8yUnGRSBgw)\
[0687. Longest Univalue Path](https://hackmd.io/yr5bIriNQ3ahO_D6ah679Q)(经典)\
[2049. Count Nodes With the Highest Score](https://hackmd.io/tTfQSMKxRoKh7xAlV3PwHA)\
[2246. Longest Path With Different Adjacent Characters](https://hackmd.io/CxJftNNbS9CyGJTXJ2j8Pg)
### LCA
除了235和1650之外，基本上所有的题都按照236的模版写 (核心思想：如果一个node 左右两边的subtree都有target node那么就返回他本身 否则就返回左边subtree或者右边subtree的LCA)\
[0235. Lowest Common Ancestor of a Binary Search Tree](https://hackmd.io/irC3SlpLSda4ljtH_iIVxg)(经典)\
[1650. Lowest Common Ancestor of a Binary Tree III](https://hackmd.io/3sL7H1qZQKCkIIWNG19JTQ)(经典)(给了每个node的parent)\
[0236. Lowest Common Ancestor of a Binary Tree](https://hackmd.io/8Sj0WCYbRFadYo4hDTXcyg)(经典)\
[1123. Lowest Common Ancestor of Deepest Leaves](https://hackmd.io/mZdc39MCT0CVggkkbYX0_g)\
[1644. Lowest Common Ancestor of a Binary Tree II](https://hackmd.io/ZQcxIr0ATdGsU7OHP3NTdg)\
[1676. Lowest Common Ancestor of a Binary Tree IV](https://hackmd.io/rfFxWl_vSpmNuuDBZnDChQ)
#### 变式
[2096. Step-By-Step Directions From a Binary Tree Node to Another](https://hackmd.io/oXIR5v6GRhSm7fSuZ-Cn4Q)\
[1740. Find Distance in a Binary Tree](https://hackmd.io/Afgf3V6lR4yMvEzy1I7PnA)\
[0785. Is Graph Bipartite?](https://hackmd.io/JhGlMsDdQB2981MMMjP-fQ)(两种解法)
## Union Find
记得初始化fa和size array
union find的很多题也可以用dfs bfs做
union find *find father*:
```java
public int find(int a){
    if(fa[a] == a) return a;
    return fa[a] = find(fa[a]);
}
```
union find *combine*: 
```java
public int combine(int a, int b){
    a = find(a);
    b = find(b);
    if(a==b) return 0;
    else{
        if(size[a]<size[b]){
            size[b] += size[a];
            fa[a] = b;
        }
        else{
            size[a] += size[b];
            fa[b] = a;
        }
        return 1;
    }
}
```
union find 计算group数量: 
- 如果两个端点的father是一样的，那么说明这两个点之前已经合并起来了，group数量不变
- 如果两个端点的father不一样，则需要合并这两个点，group-1

[0547. Number of Provinces](https://hackmd.io/Qs8Or2S2Q3Ok8qlT5JN7xw)\
[1061. Lexicographically Smallest Equivalent String](https://hackmd.io/U9BQ6T44QQmzzhmw3V_DUA)\
[0684. Redundant Connection](https://hackmd.io/erqNEw7vRMiFzbOAX8qCAg)\
[1319. Number of Operations to Make Network Connected](https://hackmd.io/sav7-nr0Qw2G0kse3c1d_A)\
[1101. The Earliest Moment When Everyone Become Friends](https://hackmd.io/wPYXfO1uThWhC_ZxLBZY9g)
### 变式
[1202. Smallest String With Swaps](https://hackmd.io/eSIiROjkS4yq6QI1RhjmQg)\
[1722. Minimize Hamming Distance After Swap Operations](https://hackmd.io/Dr9cQU9NRPqvspNUPb1XZg)\
[0721. Accounts Merge](https://hackmd.io/E2AEXy2RSy6718CqqOLhNA)\
[0947. Most Stones Removed with Same Row or Column](https://hackmd.io/S7lrCKT0QKSPqvteahktDw)\
[0990. Satisfiability of Equality Equations](https://hackmd.io/zsQmaUycR--KoeZktOk5zw)\
[0785. Is Graph Bipartite?](https://hackmd.io/JhGlMsDdQB2981MMMjP-fQ)(两种解法)\
[0839. Similar String Groups](https://hackmd.io/MB4hkOjqQ16o7pUkG3rKrg)
[2092. Find All People With Secret](https://hackmd.io/hwFbv3adRDulvBhoD1YzqQ)
### Union by an Order
[1697. Checking Existence of Edge Length Limited Paths](https://hackmd.io/pFeiq6JLSmSzs26pBw-L3Q)\
[2421. Number of Good Paths](https://hackmd.io/fiQDv27nQ7e-Rx86uMdL6w)
### Minimum Spanning Tree
[1135. Connecting Cities With Minimum Cost](https://hackmd.io/Fo-g8osYTGOAsqcF18Ljxw)
### Factors
[1627. Graph Connectivity With Threshold](https://hackmd.io/P2s41S2FSxm2_0SF2HirgQ)
## Bit Manipulation
[0318. Maximum Product of Word Lengths](https://hackmd.io/6dKXgpkzQ6-NDUr0P9frbw)\
[1356. Sort Integers by The Number of 1 Bits](https://hackmd.io/-mnod4xZTfakGIyNTc_-jQ)\
[2275. Largest Combination With Bitwise AND Greater Than Zero](https://hackmd.io/Vwz7huQQS-CYWuAsOvUv_A)

### XOR
异或运算的性质
![](https://i.imgur.com/0FMV1XI.png)
```(a1^a2) & (b1^b2) = (a1&b1) ^ (a1&b2) ^ (a2&b1) ^ (a2&b2)```([1835. Find XOR Sum of All Pairs Bitwise AND](https://hackmd.io/c8rLPqfATzOhU8c7yzNk_w))
异或运算
- 可以用来消除重复
- 不用比较运算符来比较两个数 直接```A^B==0```就可以判断```A==B```
- 实现不用其他空间就交换两个变量
```java
a = a^b
b = a^b //a^b^b = a^0 = a
a = a^b //a^b^a = b
```
[0136. Single Number](https://hackmd.io/c01pAAvZRG2QvNYapiov0g)\
[0268. Missing Number](https://hackmd.io/5HobPwZuTcWtBKj3bqPVpA)\
[1310. XOR Queries of a Subarray](https://hackmd.io/z39CKNF3R4qtyc8WG68iWg)\
[1835. Find XOR Sum of All Pairs Bitwise AND](https://hackmd.io/c8rLPqfATzOhU8c7yzNk_w)\
[1506. Find Root of N-Ary Tree](https://hackmd.io/zoOb_2tpTxazJJiQ8DT_cg)\
[1442. Count Triplets That Can Form Two Arrays of Equal XOR](https://hackmd.io/Kx1k88R3S0u2WqaqAvoxmw)\
[1734. Decode XORed Permutation](https://hackmd.io/B1pHZvzpSISZE8DgKl-zjw)\
[2425. Bitwise XOR of All Pairings](https://hackmd.io/vuI0ILbJSmeR6QV9aOHRyw)\
[2429. Minimize XOR](https://hackmd.io/LXIg8NoKTVGW91_uLnttRA)
### Bitmask
[0320. Generalized Abbreviation](https://hackmd.io/b9bB2QFORuKd1-H3IFa1qg)\
[1774. Closest Dessert Cost](https://hackmd.io/MC1wn6lhSPeHdvyJT5EQKg)(三进制)\
[2002. Maximum Product of the Length of Two Palindromic Subsequences](https://hackmd.io/I_cQd8R3QcyF9k4t3EP4ig)\
[1239. Maximum Length of a Concatenated String with Unique Characters](https://hackmd.io/awaBJbC1TlWNQ49kgWgNqg)\
[2135. Count Words Obtained After Adding a Letter](https://hackmd.io/4HXcFkyvTJ6EYYohz0lDkg)
## Deque
Sliding Window Maximum模版:
```
Deque<int[]> q = new ArrayDeque<>();
for(int i=0; i<nums.length; i++){
    超出范围的部分先pollFirst()弄掉
    计算当前的max (不能调换位置)
    把queue里面小于当前值的部分都pollLast()弄掉 (因为他们又老又旧，之后不会用到)
    q.add() 加入当前值
}
```
[1499. Max Value of Equation](https://hackmd.io/JT-L6xehRFCuBUsqJGXd8w)\
[1696. Jump Game VI](https://hackmd.io/PkwAF5OZRUKwbtJZpNJMKQ)
## Trie
Trie 模版:
```
class TrieNode{
    TrieNode[] children = new TrieNode[26];
    boolean isWord = false;
    int countPrefix = 0;
    int countWord = 0;
    int score = 0;
    (上面四个不一定用哪个)
}
```
各个function的写法可以看[0208. Implement Trie (Prefix Tree)](https://hackmd.io/ExDA-j4YSZ-YymHS75TmRg)

[1858. Longest Word With All Prefixes](https://hackmd.io/WUh7DnbYTsagOyLTHtJPaw)\
[0677. Map Sum Pairs](https://hackmd.io/FluIFqvmQb28p5-jcMxrUQ)\
[0208. Implement Trie (Prefix Tree)](https://hackmd.io/ExDA-j4YSZ-YymHS75TmRg)\
[1804. Implement Trie II (Prefix Tree)](https://hackmd.io/3ZIAA-kMTEyD3Fxz1QK9-w)\
[2416. Sum of Prefix Scores of Strings](https://hackmd.io/I4owiG_-RgGlvbAtyXamfg)
## Linked List
[0061. Rotate List](https://hackmd.io/fNN_O2qPT2OjcYV8VaQ4Nw)\
[0086. Partition List](https://hackmd.io/qbiIN4s2Rkyk-Fs_QsGK5Q)\
[0109. Convert Sorted List to Binary Search Tree](https://hackmd.io/xGmhY4bSQ7ewSkjhKZfDDA)\
[0369. Plus One Linked List](https://hackmd.io/z67xI6jmTVWpEcD8GhOM8Q)\
[1474. Delete N Nodes After M Nodes of a Linked List](https://hackmd.io/SIxTI8hHTAKkbl2rNbMorQ)\
[0082. Remove Duplicates from Sorted List II](https://hackmd.io/VA1lmVyUQlOzeOLqI3mTlg)\
[0092. Reverse Linked List II](https://hackmd.io/98PAuvfURuiUW_5X_bEbKw)\
[0142. Linked List Cycle II](https://hackmd.io/iiXmhYCfR32eRwFxjl876Q)\
[1836. Remove Duplicates From an Unsorted Linked List](https://hackmd.io/8tLNzrYPTdWe3ssvqeg0tA)
##  DP
[讲解](https://blog.csdn.net/u013309870/article/details/75193592)
[套路讲解](https://www.youtube.com/watch?app=desktop&v=FLbqgyJ-70I&t=6554s)
[套路ppt](https://docs.google.com/presentation/d/1F_Qp3kzw7jZkPpb7ll7J6-02285bCA3Z9nmU1e7a2rk/edit#slide=id.g82af7adac0_0_675)
简单来说就是用已经解决过了的子问题的解去解新的问题
经典问题：
1. 找string里面subsequence的最长回文字符串 ([2002. Maximum Product of the Length of Two Palindromic Subsequences](https://hackmd.io/I_cQd8R3QcyF9k4t3EP4ig))
### 基本型 I (时间序列型) $O(N)$
**今天状态只取决于昨天状态**
![](https://i.imgur.com/A9P6CmD.png)
初始条件的设定: 
1. 如果不是subarray题目，如果初始值显而易见，那么就直接设 (例如[2320. Count Number of Ways to Place Houses](https://hackmd.io/DjBBHzHBSIiuhhgC1iLymg), [0801. Minimum Swaps To Make Sequences Increasing](https://hackmd.io/56SvCwGORzywqiIe789vjA), [1824. Minimum Sideway Jumps](https://hackmd.io/izenODQoRUuC4rEWpNDt6Q))
2. 如果实在有变量不知道怎么设初始值，并且也不需要把arr[0]拿来当初始值，看题目问min还是max，就把初始值设成相反的max(min)
3. 如果以上方法都不能体现不同状态的差异, 初始值直接用arr[0]的值 (例如有一些subarray题目 [1186. Maximum Subarray Sum with One Deletion](https://hackmd.io/mEeqqUmARlmmtyQR_chxVQ), [1746. Maximum Subarray Sum After One Operation](https://hackmd.io/qN2Bh6RxQAO7Xkv_oNGwdg))

总而言之就是需要**初始值的设定也能满足不同状态的差异和要求**(思考的时候就思考当下这一天的设定是否满足条件)

subarray最值dp
subarray题目状态定义：**包含**nums[i]的最值，然后**在过程中记录最值**([2036. Maximum Alternating Subarray Sum](https://hackmd.io/50hUosjQT_W7xhFPjtIurQ))

求min的题通常每一轮开始要设一个极值([0801. Minimum Swaps To Make Sequences Increasing](https://hackmd.io/56SvCwGORzywqiIe789vjA))

[0198. House Robber](https://hackmd.io/2t7kWFk_TVmewlzltG_Qaw)\
[0213. House Robber II](https://hackmd.io/Ug-8ugwETsmu9DF73ZEigg)\
[0123. Best Time to Buy and Sell Stock III](https://hackmd.io/EMMrQEFTSKyo5sxnrqkx7Q)\
[0309. Best Time to Buy and Sell Stock with Cooldown](https://hackmd.io/qst4ueCwToKBy3ZwoHo2Yg)\
[0376. Wiggle Subsequence](https://hackmd.io/7Iu_kRQBQueLEXufCv8fyg)\
[0256. Paint House](https://hackmd.io/IH85BfuSQAyObMZxbUAcPQ)\
[1289. Minimum Falling Path Sum II](https://hackmd.io/3trxUuWbQnybTTNZTPwjuw)\
[0714. Best Time to Buy and Sell Stock with Transaction Fee](https://hackmd.io/DiQ804bqTLii1h0wo8SlMA)\
[2320. Count Number of Ways to Place Houses](https://hackmd.io/DjBBHzHBSIiuhhgC1iLymg)\
[0801. Minimum Swaps To Make Sequences Increasing](https://hackmd.io/56SvCwGORzywqiIe789vjA)\
[2036. Maximum Alternating Subarray Sum](https://hackmd.io/50hUosjQT_W7xhFPjtIurQ)\
[1824. Minimum Sideway Jumps](https://hackmd.io/izenODQoRUuC4rEWpNDt6Q)\
[1262. Greatest Sum Divisible by Three](https://hackmd.io/JtDP1Kh7Se-F6Rj5hjLFLA)\
[2400. Number of Ways to Reach a Position After Exactly k Steps](https://hackmd.io/wER00MrASZil427NsqQ44Q)

#### 变式 (把"权利"写进状态)
[0487. Max Consecutive Ones II](https://hackmd.io/8lcD9MH8RAqKwz7DVjNtGg)\
[1186. Maximum Subarray Sum with One Deletion](https://hackmd.io/mEeqqUmARlmmtyQR_chxVQ)\
[1746. Maximum Subarray Sum After One Operation](https://hackmd.io/qN2Bh6RxQAO7Xkv_oNGwdg)
[0552. Student Attendance Record II](https://hackmd.io/_1beCVHnTjuoJjSgzfgV4Q)
### 基本型 II (时间序列加强版) $O(N^2)$
![](https://i.imgur.com/vEITlRV.png)
由于某些题需要设置初始值当作dp[0], 也就是需要让nums[0]对应到dp[1], 相比基本型I, 这里考虑这种情况会比较麻烦, 所以通常情况下会在前面加一个凑数的num或者char (例如[1043. Partition Array for Maximum Sum](https://hackmd.io/sSjKhGdcQrmWNvAvq0s6bw), [1105. Filling Bookcase Shelves](https://hackmd.io/SStKMDA2S2OdA5X256a7KA), [1416. Restore The Array](https://hackmd.io/6PmS-oOITbqSovcqAbppVw))

[0300. Longest Increasing Subsequence](https://hackmd.io/oPc5yL1oRhGtGP8UdRd3_g)\
[0673. Number of Longest Increasing Subsequence](https://hackmd.io/ggEUM5vIS36_nrs5h0VGMQ)\
[0368. Largest Divisible Subset](https://hackmd.io/T9YlpxKmRjOCKFFdyiWDsg)\
[1626. Best Team With No Conflicts](https://hackmd.io/SIztzm-uQ2yzVNtop0zoxw)

[2209. Minimum White Tiles After Covering With Carpets](https://hackmd.io/UEAOe9NtRSSb7fQkrmefhw)(Good)\
[0983. Minimum Cost For Tickets](https://hackmd.io/9G_ZvJRARB6gUpo1ob1JCw)

#### 分组题
找到前一个group的最后一个元素
[1105. Filling Bookcase Shelves](https://hackmd.io/SStKMDA2S2OdA5X256a7KA)\
[1043. Partition Array for Maximum Sum](https://hackmd.io/sSjKhGdcQrmWNvAvq0s6bw)\
[1416. Restore The Array](https://hackmd.io/6PmS-oOITbqSovcqAbppVw)

### 双序列型
![](https://i.imgur.com/PZB4aKV.png)
**通常```dp[i][j]```的取值是分情况讨论: 看```s.charAt(i)==t.charAt(j)```是否成立**
![](https://i.imgur.com/xOsvG02.png)
注意subarray问题定义dp的时候要写成**包含```nums[i]```** 的subarray的最值, subsequence问题写成以nums[i]结尾的subsequnce的subarray的最值

[1143. Longest Common Subsequence](https://hackmd.io/bO7KsaWYS4iKJnjgeCz5gA)(经典)\
[1092. Shortest Common Supersequence](https://hackmd.io/jlauVPUGShKqo6HzbeZbKA)\
[0072. Edit Distance](https://hackmd.io/Q8Ih3bdASK6cZiwFNV3IDQ)\
[0115. Distinct Subsequences](https://hackmd.io/ELuDI85BSwqf4o8QSalxYg)\
[0727. Minimum Window Subsequence](https://hackmd.io/5URINcb3Q76siuGQ9xJWMA)\
[0718. Maximum Length of Repeated Subarray](https://hackmd.io/RpH7XazXSxamHXn-T5d-sw)\
[1458. Max Dot Product of Two Subsequences](https://hackmd.io/5goxddf9QMmUo9YXwmBxig)
#### LCS SCS变式
[0583. Delete Operation for Two Strings](https://hackmd.io/TGyjylNgRmqHjVLMTDnVgw)\
[1035. Uncrossed Lines](https://hackmd.io/msbmGiOTTpaJ5hnJqD14xg)\
[1312. Minimum Insertion Steps to Make a String Palindrome](https://hackmd.io/9iF5-hs4TyGh1jK-_J0nKQ)\
[1216. Valid Palindrome III](https://hackmd.io/fRam7uIYT0OhEPXUMC10iQ)\
[2430. Maximum Deletions on a String](https://hackmd.io/QetLsZKSRP2U3c-6rt-h9Q)
### 第I类区间型DP
和基本型II的分组题区分开 一个指定了要分几组一个没有指定
![](https://i.imgur.com/rfsC6Gb.png)
举例: **注意回圈边界**
![](https://i.imgur.com/QIGDkih.png)


[1278. Palindrome Partitioning III](https://hackmd.io/Igc7yQalTeWaCyrJArjm4A)\
[0813. Largest Sum of Averages](https://hackmd.io/W9qUmvnoSIOt58Ylr6qKVQ)\
[1335. Minimum Difficulty of a Job Schedule](https://hackmd.io/8PIlmv0IRJOOXJS3WF2bRg)\
[0410. Split Array Largest Sum](https://hackmd.io/nNeGw-FeSyWghLf5ZB2C-Q)
### 第II类区间型DP
![](https://i.imgur.com/NgM2IvV.png)
- 注意**第一层循环是区间大小；第二层循环是起始点**
- 建议len的起始写成2 再单独定义len=1的时候的dp值 比较不容易出错
- 需要注意当i>j的时候dp值的定义 通常情况下都是等于0
- 如果回圈里面出现了k-1 k+1这种 如果担心越界 就把dp的size变大 例如从```n*n``` 扩大到```(n+2)*(n+2)```([0312. Burst Balloons](https://leetcode.com/problems/burst-balloons/))
- 考虑对于一个小区间来说到底从哪切第一刀

[0516. Longest Palindromic Subsequence](https://hackmd.io/KGqTZxWWQCeKT3ptY4LWBw)(经典)\
[0312. Burst Balloons](https://leetcode.com/problems/burst-balloons/)\
[0375. Guess Number Higher or Lower II](https://hackmd.io/pJ9pUaq_SwmtPxn6vIhCvw)\
[1745. Palindrome Partitioning IV](https://hackmd.io/Lhdh2BOsTnScQZJFcDHUDg)\
[1547. Minimum Cost to Cut a Stick](https://hackmd.io/_OImj0R1R_KXRYmxhIp0Pg)\
[1246. Palindrome Removal](https://hackmd.io/v4DhCetNQ96TIsEWlwg63Q)\
[1130. Minimum Cost Tree From Leaf Values](https://hackmd.io/7M8-WsJfRuq7mjHclMToyA)
### 背包问题
![](https://i.imgur.com/vbETTQv.png)
![](https://i.imgur.com/K3aHXJE.png)
[0474. Ones and Zeroes](https://hackmd.io/A71TsrJ_RIGo-0jIczcCNw)\
[0494. Target Sum](https://hackmd.io/BBt3Z9T0Tx-vNuZzFlZpGg)\
[0416. Partition Equal Subset Sum](https://hackmd.io/18plVWdQSjutpHD_ownwSg)\
[2291. Maximum Profit From Trading Stocks](https://hackmd.io/4xQawwDKS2mDMhinroeCnw)\
[0956. Tallest Billboard](https://hackmd.io/6Tv_k3eGSyqIcgKd5MDx7w)\
[1049. Last Stone Weight II](https://hackmd.io/yWIIxo5BQoSW_hZOX_fE-A)\
[1155. Number of Dice Rolls With Target Sum](https://hackmd.io/Ggss6gIST_iJbvuQZ6kNyA)
#### 需要优化的背包问题
[1981. Minimize the Difference Between Target and Chosen Elements](https://hackmd.io/O_ABik1mTem5D5LSaq0ITA)\
[0879. Profitable Schemes](https://leetcode.com/problems/profitable-schemes/)\
[0956. Tallest Billboard](https://hackmd.io/6Tv_k3eGSyqIcgKd5MDx7w)\
#### 每个物品可以用无限多次
外层遍历状态 里层遍历coin
[0322. Coin Change](https://hackmd.io/4FjJq5P_Sc6miBP0IwKc6A)(经典)\
[0518. Coin Change 2](https://hackmd.io/azimrNJRRUK0CBaC2d0Ivg)(经典)\
[0691. Stickers to Spell Word](https://hackmd.io/g6-O9OjCRiqSgbKVNXC2Ig)\
### 状态压缩
[1125. Smallest Sufficient Team](https://hackmd.io/iziZ5qIEQjeGGCX5Aj_p3g)\
[0691. Stickers to Spell Word](https://hackmd.io/g6-O9OjCRiqSgbKVNXC2Ig)\
[1349. Maximum Students Taking Exam](https://hackmd.io/pIRFwFXgQGWTbTNDPwrYDg)\
[1411. Number of Ways to Paint N × 3 Grid](https://hackmd.io/AKffexhVRtGqAo1_PAqr2Q)\
[1931. Painting a Grid With Three Different Colors](https://hackmd.io/9pdSzNvwR6-_64BhTSQWKg)\
[2184. Number of Ways to Build Sturdy Brick Wall](https://hackmd.io/1R8nFxZ3T4uThpurkQVXgw)\
### 键盘型
[0650. 2 Keys Keyboard](https://hackmd.io/S0C7B2ILSraGq3J_-ZSCnw)\
[0651. 4 Keys Keyboard](https://hackmd.io/8A_iOI6ER4i0IssTkC1d0Q)\
[0935. Knight Dialer](https://hackmd.io/mVFRorYKTsWa5I6QLgUnfA)
### Maximum Subarray
[0053. Maximum Subarray](https://hackmd.io/qpgZUbERQVOXcw9DSBI1Mw)\
[0152. Maximum Product Subarray](https://hackmd.io/qpgZUbERQVOXcw9DSBI1Mw)
#### 枚举集合的子集
枚举子集的模板：
```
for (int state=1; state<(1<<n); state++){ 
    for (int subset=state; subset>0; subset=(subset-1)&state){
        dp[state] = DoSomething(dp[subset]);
    }
}
``` 
[1986. Minimum Number of Work Sessions to Finish the Tasks](https://hackmd.io/69G6kfsHTLaMOO2GrBx7vw)
### 迷宫型
给一个图让你找从某个点到某个点maximum score的一条路径的score
(会规定走法)
[0120. Triangle](https://hackmd.io/_q9inK24Tma2gcF58FSASQ)\
[0931. Minimum Falling Path Sum](https://hackmd.io/6OEUfm0SS-eeHlADFNXKGQ)\
[1289. Minimum Falling Path Sum II](https://hackmd.io/3trxUuWbQnybTTNZTPwjuw)\
[1594. Maximum Non Negative Product in a Matrix](https://hackmd.io/zTSVD5RrTvyViPnpFN_EVw)\
[1463. Cherry Pickup II](https://hackmd.io/l58Hy-YaSKiaZvJb-R-9Pw)\
[1301. Number of Paths with Max Score](https://hackmd.io/kApGbvmOTPeKpxkaxO5rfg)
## Recursion
[0427. Construct Quad Tree](https://hackmd.io/Egf4XnCPRRqBzU8O4ZhB_g)
## Simulation
[2257. Count Unguarded Cells in the Grid](https://hackmd.io/ZmQOPyHORVmk081ZLgbjfw)
## Math
[0781. Rabbits in Forest](https://hackmd.io/GoToVbu1QYmhXOZJh3dlVw)\
[0780. Reaching Points](https://hackmd.io/Cv7T9O2NR3yxHnzgNzujmQ)\
Greatest Common Divisor
[2427. Number of Common Factors](https://hackmd.io/eitQmChnRaGw_OhNPbOQSA)\
距离所有点直线距离最近的点
[0296. Best Meeting Point](https://hackmd.io/iSJUkTnTTKu2AnB8iPowrA)
## Sweep Line & 差分法
[0252. Meeting Rooms](https://hackmd.io/IEBJKDJMQKifMm502z5jiw)\
[1094. Car Pooling](https://hackmd.io/-FSHYs9DSYWKJW5TIUBTBg)(经典)\
[1893. Check if All the Integers in a Range Are Covered](https://hackmd.io/cbM9HQCNSNaPJUHKU1eccw)\
[1109. Corporate Flight Bookings](https://hackmd.io/dfft8CmbSxKdy9KbhJigXQ)\
[1589. Maximum Sum Obtained of Any Permutation](https://hackmd.io/RCXOpd_GQUOxbJwVjpfDBw)\
[2237. Count Positions on Street With Required](https://hackmd.io/H3qwtlMYTGeTlTpUNbqeJQ)\
[0056. Merge Intervals](https://hackmd.io/-Me1s3AUQCi4IPU8FslHyw)\
[0057. Insert Interval](https://hackmd.io/7Xg-MSxbQza--3rY_Um3cA)(重点复习 看笔记)
### TreeMap+Sweep Line
[2251. Number of Flowers in Full Bloom](https://hackmd.io/SlEo8THMSG2IQFjEy0qXKQ)(经典)\
[0732. My Calendar III](https://hackmd.io/v3_I8Np7RPSadXz9Z8D0ig)\
[0759. Employee Free Time](https://hackmd.io/HpHsgFsyTCK1kB_sUq2i2g)\
[1871. Jump Game VII](https://hackmd.io/cb46t-RNRTqyDQ3X8aiP_A)(经典)
## Design
[1352. Product of the Last K Numbers](https://hackmd.io/I6C-0C1RRhCc43bQVjnmqQ)\
[0642. Design Search Autocomplete System](https://hackmd.io/SCAbjINTS9mp7W8s7MtPlw)
## 不常见语法整理
- 比较两个array ```Arrays.equals()```
- 比较两个String ```a.compareTo(b)```
- ```TreeMap.lowerKey()``` The lowerKey() method is used to return the greatest key strictly less than to given key, passed as the parameter. [0729. My Calendar I](https://hackmd.io/am3vFQC-TeuImofwjISHjQ)
- ```TreeMap.firstKey() TreeMap.lastKey()``` 最小最大的key
- ```TreeMap.ceilingKey()/floorKey()``` 是找高于或等于自己的key, ```TreeMap.higherKey()/lowerKey()``` 是找高于/低于自己的key (不包含等于)
- ```map.entrySet().removeIf(e -> e.getValue() <= currentTime)```如果需要在遍历mapkey时删掉某些key可以直接用这个替代 [1797. Design Authentication Manager](https://hackmd.io/GTCQB10lQZqW_UWWPTbpuA)
- 对于一个priority queue, 我们可以不需要把queue的peek()拿出来就可以给它赋值 for example, ```buy.peek()[1] -= k;```[1801. Number of Orders in the Backlog](https://hackmd.io/iKDFgeW4Q3CuNdp_2JFHiA)
- PriorityQueue如果queue里面item的type和lambda表达式里面的结果不一样会报error
    for example, 
    ```java
    Queue<int[]> pq = new PriorityQueue<>((a,b)->((double)(a[0]+1)/(a[1]+1)-(double)(b[0]+1)/(b[1]+1))
    ```
    需要写成
    ```java
    Queue<int[]> pq = new PriorityQueue<>((a,b)->{
        double diff1 = (double)(a[0]+1)/(a[1]+1) - (double)a[0]/a[1];
        double diff2 = (double)(b[0]+1)/(b[1]+1) - (double)b[0]/b[1];
        if(diff1<diff2) return 1;
        if(diff1<diff2) return 0;
        else return -1;
    });
    ```
    [1792. Maximum Average Pass Ratio](https://hackmd.io/BbRp_dzORMCJsamRv-Ys4w)
- ```Arrays.asList``` vs ```new ArrayList(Arrays.asList())```([1253. Reconstruct a 2-Row Binary Matrix](https://hackmd.io/50KYfhv-RdWejdAouFnyIQ))
    - Using ```Arrays.asList()```, we can convert from an array to a fixed-size List object. This List is just a wrapper that makes the array available as a list. No data is copied or created.
    - ```new ArrayList(Arrays.asList())``` creates an independent copy of the array, which means that modifying the new list won't affect the original array. 
- 遇到需要把数字拆成一位一位，然后处理，再合起来的，可以不用自己慢慢取余数，直接用String和Integer之间的变换(```String.valueOf(num)```和```Integer.parseInt(s)```)([0670. Maximum Swap](https://hackmd.io/BRg5nV6yTJqspaUdaxQdSQ))
- charArray可以直接通过```String(charArray)```或者```String.valueOf()```变成string 不能直接像StringBuilder一样用```toString()``` ([0670. Maximum Swap](https://hackmd.io/BRg5nV6yTJqspaUdaxQdSQ))
- List[int[]]转换成int[][]的方法(下面例子中res是list)
```res.toArray(new int[res.size()][])```或者```res.toArray(new int[0][])```
- ```Arrays.copyOf(arr, arr.length);``` copy array([1331. Rank Transform of an Array](https://hackmd.io/-wkbEfZaTSeGdFSdm4B8cQ))
- copy array 如果用```int[] temp = forces``` temp指向forces的位置 所以temp变forces也会变 用```int[] temp = forces.clone()```就不会有这个问题([0838. Push Dominoes](https://hackmd.io/RpV2rwrSQiKg4YLc1erpYQ))
- 可以把整个list通过toString转换成string it will be like "[1,2,3]"([0638. Shopping Offers](https://hackmd.io/WtskTj8rRk6YWArb7av6ow
- Array sort 自定义comparator([1626. Best Team With No Conflicts](https://hackmd.io/SIztzm-uQ2yzVNtop0zoxw))
```
Arrays.sort(players, new Comparator<int[]>() {
    public int compare(int[] o1, int[] o2) {
        if(o1[1]!=o2[1]) return o1[1]-o2[1];
        else return o1[0]-o2[0];
    }
});
```
- ```int[] temp = dp``` 如果dp改了temp也会跟着改 因为temp存的是dp的指针 如果希望dp改了但是temp保持不变 就要用```int[] temp = dp.clone()``` ([1411. Number of Ways to Paint N × 3 Grid](https://hackmd.io/AKffexhVRtGqAo1_PAqr2Q)) 但是如果dp是2d的话 ```int[][] temp = dp.clone()``` temp 存的还是dp的指针 这时候就要一行一行copy ([1463. Cherry Pickup II](https://hackmd.io/l58Hy-YaSKiaZvJb-R-9Pw))
- ```Integer.bitCount()```可以算出每个数字的the number of 1 bits([1356. Sort Integers by The Number of 1 Bits](https://hackmd.io/-mnod4xZTfakGIyNTc_-jQ))
- ```text.split(" ")```只能split by一个空格, ```text.split("\\s+")```才能去除单词间的连续空格([1592. Rearrange Spaces Between Words](https://hackmd.io/UW7hOOBbS_WYrQch0DMiMw))
- ```String.join()```和```" ".repeat()```的用法([1592. Rearrange Spaces Between Words](https://hackmd.io/UW7hOOBbS_WYrQch0DMiMw))
## 注意事项
- 如果res是long，题目要求你return res%1000000007 
    ```(int)res%mod``` wrong ```(int)(res%mod)``` correct 前面一种方法会先把res变成int然后再算
- 如果index是一个int array(例如它是一个array的所有index的集合，我们不想排序array本身，而转而排序它的index)那我们不能写```Arrays.sort(index, (a,b)->(nums2[b]-nums2[a]))```而是要写成```Arrays.sort(index, (a,b)->Integer.compare(nums2[b], nums2[a])``` 同时index的数据类型还要设成Integer([0870. Advantage Shuffle](https://hackmd.io/w0INiSnmSJOkU2puietlOw))
- ```Arrays.sort(nums, Collections.reverseOrder())```的```nums```不能是int array，而要是Integer array
- 如果priority queue里面存的是integer，但是比较的是double，所以它自带的compare函数的参数应该是integer，而不是double，因此要写成```Queue<Integer> pq = new PriorityQueue<Integer>(Comparator.comparingDouble(i -> -prob[i]));```([1514. Path with Maximum Probability](https://hackmd.io/B7M8f6PUSdqHzZry7hDpSA)
- 考虑装进priority queue里面的元素会不会动([1514. Path with Maximum Probability](https://hackmd.io/B7M8f6PUSdqHzZry7hDpSA)