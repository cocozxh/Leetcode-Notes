# 题型总结笔记
###### tags: `Leetcode`
**Leetcode数据规模和时间复杂度对照**
![](https://i.imgur.com/T2w2aQi.png)
## 面试思路[参考](https://leetcode.com/problems/guess-the-word/solutions/556075/how-to-explain-to-interviewer-843-guess-the-word/)
## Two Pointers
[0392. Is Subsequence](https://hackmd.io/r78hzXqUSaWUeo-OqSzDeg)\
[0611. Valid Triangle Number](https://hackmd.io/0K3tNOyPQcCkRxZZQUvD8A)\
[0360. Sort Transformed Array](https://hackmd.io/VIjmADEcT4agS3ZiY7s5zg)\
[1793. Maximum Score of a Good Subarray](https://hackmd.io/ulPJ8HGcQEu7FhX_jrQYpA)(经典)\
[2337. Move Pieces to Obtain a String](https://hackmd.io/PhWeQn2_SjSyIYg7L2iuWg)\
[0777. Swap Adjacent in LR String](https://hackmd.io/L9wvI1fuSsqwKi6FcPwI6g)\
[2414. Length of the Longest Alphabetical Continuous Substring](https://hackmd.io/FQq8G6EbReu5fIVazrPang)\
[2410. Maximum Matching of Players With Trainers](https://hackmd.io/V02t5DH0RNCZCV747NS_zA)\
[2462. Total Cost to Hire K Workers](https://hackmd.io/L9V_AMNFQley0-UKFStLww)\
[2465. Number of Distinct Averages](https://hackmd.io/6gRGN3FbRkas7AVixGABTA)\
[2486. Append Characters to String to Make Subsequence](https://hackmd.io/-J-1D7WiSLSprPZdRspnQw)\
[2330. Valid Palindrome IV](https://hackmd.io/0gKxHf8lSBWpHnBzwoQ6MQ)\
[1712. Ways to Split Array Into Three Subarrays](https://hackmd.io/VyYwo5xuTAaCcCokB-6BTw)\
[2511. Maximum Enemy Forts That Can Be Captured](https://hackmd.io/fVQiW2HNReOO_kc1i1JdTQ)\
[1910. Remove All Occurrences of a Substring](https://hackmd.io/w9HB2xbSR_G8DH2TRHsjhg)\
[0345. Reverse Vowels of a String](https://hackmd.io/JELlDncUR7KgwzlMZJAB1w)\
[2070. Most Beautiful Item for Each Query](https://hackmd.io/obySHWqFScamlS-PShAxOg)\
[2109. Adding Spaces to a String](https://hackmd.io/IQiTZiAHTI2VhcYgPmJM4A)\
[2565. Subsequence With the Minimum Score](https://hackmd.io/OATYkbLdSgaNkHynbjS3Eg)\
[2570. Merge Two 2D Arrays by Summing Values](https://hackmd.io/rMkJoQ0kRwy3olg7mPY6PA)\
[2422. Merge Operations to Turn Array Into a Palindrome](https://hackmd.io/aXpLXKgRQ1KIHS9G76gifQ)\
[2592. Maximize Greatness of an Array](https://hackmd.io/QtBFzz-NTpKu2rwCZSyqDw)
### Two Sum(经典)
Two Sum 找相等 用map; 找小于/大于某个数 用sort+two pointers\
[1885. Count Pairs in Two Arrays](https://hackmd.io/JJb56E1kTviOjH2qQcEE6A)\
[2491. Divide Players Into Teams of Equal Skill](https://hackmd.io/7q4BQgOoTlaOPHe5PpcnZw)\
[2563. Count the Number of Fair Pairs](https://hackmd.io/FneNxcLbTO-H1jMqRYx-6A)\
[1711. Count Good Meals](https://hackmd.io/DH4xwaUXSAO_u8LAPUlm1Q)
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
[2098. Subsequence of Size K With the Largest Even Sum](https://hackmd.io/jU92j-qxSrulIKhfradL-w)
### Sliding Window
- 看到substring就应该想到sliding window
- 如果我们依次递增地枚举子串的起始位置，那么子串的结束位置也是递增的！那么就可以使用「滑动窗口」来解决这个问题了
- 如何计算subarray sum小于某个数的subarray个数: 只要当前的l和r满足条件 ```cnt+=r-l+1``` 相当于每次是算以r为右边界的满足条件的subarray数量 ([1918. Kth Smallest Subarray Sum](https://hackmd.io/jyl8yjzlRFOLeg1_ctbjAg))
#### Fixed Length Sliding Window
用for回圈遍历 先加上新的值 如果已经超过长度再减去最左边的值 最后更新答案\
[1052. Grumpy Bookstore Owner](https://hackmd.io/O8aCAsHdTFuhSo6Ikuvk5A)\
[0438. Find All Anagrams in a String](https://hackmd.io/MvGWdMIxQZ26uuetxx6l_g)\
[0567. Permutation in String](https://hackmd.io/6X-IxcbATymBez07eXRr6g)
[2379. Minimum Recolors to Get K Consecutive Black Blocks](https://hackmd.io/lqKln8EoSWO9ra_VECSsZQ)\
[1031. Maximum Sum of Two Non-Overlapping Subarrays](https://hackmd.io/hSLeqvRvTSWn3kDV72XEIg)\
[2134. Minimum Swaps to Group All 1's Together II](https://hackmd.io/bHmVkah-TTCvJD8_6It_pA)\
[2107. Number of Unique Flavors After Sharing K Candies](https://hackmd.io/5jNUdj9EQDyHdp8OgXCAzw)\
[2653. Sliding Subarray Beauty](https://hackmd.io/s8pdv210Qh-s8aQvQS7YtA)\
[2747. Count Zero Request Servers](https://hackmd.io/1u2xKxOcSrWw_La9rNp3BQ)
##### Distinct Subarray
[2461. Maximum Sum of Distinct Subarrays With Length K](https://hackmd.io/8kM45sHuQhq-aHejy2B7ZQ)
#### Unfixed Length Sliding Window
while回圈遍历 先加上新的值 如果window里面的value invalid 跑**while**回圈挪left pointer一直到valid为止 **(在回圈外面)** 更新答案\
[2024. Maximize the Confusion of an Exam](https://hackmd.io/fQOTPNnqT-SfFNKxzOpCag)\
[2444. Count Subarrays With Fixed Bounds](https://hackmd.io/5TbKxlSMQPKLK6J6_3S6Ig)\
[2516. Take K of Each Character From Left and Right](https://hackmd.io/2tjy5JpkS0iDajyrZGHkbQ)\
[2765. Longest Alternating Subarray](https://hackmd.io/9jJC0ACyT5a7p5KEikiRiA)
##### Sliding Window for Number Sequence
大部分时候不需要用prefixsum 还比较节省空间\
[1004. Max Consecutive Ones III](https://hackmd.io/LbO10-8UTDWGIJX2A4cEfA)\
[0209. Minimum Size Subarray Sum](https://hackmd.io/WyUTJHs1S7WjYBfNeuB37A)\
[2537. Count the Number of Good Subarrays](https://hackmd.io/cQejiWaTS4qBD8-afQjRxg)
##### Sliding Window for Distinct Characters
[0003. Longest Substring Without Repeating Characters](https://hackmd.io/-bC_ZG1BR2isaDfCleju6Q)\
[0076. Minimum Window Substring](https://hackmd.io/z50NoPGOTlOtJcP9sBE5nw)
#### Sliding Window + Greedy
[2271. Maximum White Tiles Covered by a Carpet](https://hackmd.io/7FnX3SCASZyuEec1uVk90w)
#### Sliding Window + DP
[2555. Maximize Win From Two Segments](https://hackmd.io/HKJMbIInThiVNpzZHnf_og)
#### Longest Sliding Window
[2779. Maximum Beauty of an Array After Applying Operation](https://hackmd.io/Qsl7RpgxTreTZglXwmSySg)
#### 变式
[0930. Binary Subarrays With Sum](https://hackmd.io/wHpz7ueHSeyRa9d9hQBIdw)\
[1658. Minimum Operations to Reduce X to Zero](https://hackmd.io/sSVu2nTaT3mIxUfVX337PQ)\
[1888. Minimum Number of Flips to Make the Binary String Alternating](https://hackmd.io/OKCVg7UFR3qUdjzoHN7J5w)


#### 形似sliding window但是不完全用sliding window解
[1156. Swap For Longest Repeated Character Substring](https://hackmd.io/R4opMwT2Qg-a-PnLmsS59g)\
[1763. Longest Nice Substring](https://hackmd.io/cIMdRw03R_iRQtFsbS7kNA)

## Sort
[0147. Insertion Sort List](https://hackmd.io/iJKi2XW9SBC7oVAmXsrJ3A)\
[2545. Sort the Students by Their Kth Score](https://hackmd.io/4JKjhA9tTse0Ulk1PD-rUw)

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
[0594. Longest Harmonious Subsequence](https://hackmd.io/EzxIF4I_Q3mBgZFa4u9c4w)\
[2342. Max Sum of a Pair With Equal Sum of Digits](https://hackmd.io/IXV48qcIR4aU5jrIcc-TiQ)\
[1814. Count Nice Pairs in an Array](https://hackmd.io/c8Ipq2IPRyiaZqYRaz69yw)\
[2364. Count Number of Bad Pairs](https://hackmd.io/v9Qr8EE6ShmouCNoSZq00w)\
[2365. Task Scheduler II](https://leetcode.com/problems/task-scheduler-ii/description/)\
[2488. Count Subarrays With Median K](https://hackmd.io/nodjb7ZcRK6zi0cXJxAcGA)\
[2506. Count Pairs Of Similar Strings](https://hackmd.io/WmpUVmyYQNyh4jq8xI0qMw)\
[2006. Count Number of Pairs With Absolute Difference K](https://hackmd.io/0EzOD00wQJOZ-KebRVGKKg)\
[2083. Substrings That Begin and End With the Same Letter](https://hackmd.io/kdyHWh97Rm-YqKS6PJ1YUg)\
[2150. Find All Lonely Numbers in the Array](https://hackmd.io/XKuF25mYSr-LH--8C_UhdA)\
[2657. Find the Prefix Common Array of Two Arrays](https://hackmd.io/hrwdN54ETjWn5jEtPOzkNw)
### 变式
[0890. Find and Replace Pattern](https://hackmd.io/q5X-Wx7nRlW9lCF0PtLeyQ)\
[0128. Longest Consecutive Sequence](https://hackmd.io/xQ0F7nSeRUqZ3CabQjFQxg)
### HashMap + Prefix
**做法: 先建map 然后遍历 如果现在的值在map里面遇到过 更新答案
跟sliding window的场景其实有点像 都是找满足条件的subarray
但这个是通过'-'来得到的 这个value前面出现过一次 这次又出现了 那么中间的就是答案
但sliding window的就是两个指针一个往右挪了 另一个只能往右挪 不可能需要往左**

想好是不是固定size 是的话用array 否的话用map
map建好之后跑回圈之前 通常要先放一个值 **如果是算substring prefixSum通常放(0,-1)** (因为还没开始遍历array的时候值是0), **如果是算count 通常放(0,0)**
详见下面几题

[1524. Number of Sub-arrays With Odd Sum](https://hackmd.io/yyWTzutqS_GYvUZY83Sjrg)\
[0974. Subarray Sums Divisible by K](https://hackmd.io/kqI87VXXQ-6je55xfvQzPw)\
[1658. Minimum Operations to Reduce X to Zero](https://hackmd.io/sSVu2nTaT3mIxUfVX337PQ)\
[0325. Maximum Size Subarray Sum Equals k](https://hackmd.io/9tY6qpjqQrCaw0E2mlr9ZA)\
[1124. Longest Well-Performing Interval](https://hackmd.io/VmIhbESGTgCDiFRB2dnRFg)\
[2489. Number of Substrings With Fixed Ratio](https://hackmd.io/BF-5UMALQQqPnLuMUgOYJg)
#### 变式
##### 看到array只有1和0, 就把0变成-1
[0525. Contiguous Array](https://hackmd.io/gvM6GJYHStmB-OH0bKr8sQ)\
[1983. Widest Pair of Indices With Equal Range Sum](https://hackmd.io/NvYEEEPfTIup5ztyaBM4qw)\
[1915. Number of Wonderful Substrings](https://hackmd.io/0NLt0f9ZQnicvBhDgaKRIg)\
[1371. Find the Longest Substring Containing Vowels in Even Counts](https://hackmd.io/vqzHHM8YQhyHFc1m21Ja3g)\
[1542. Find Longest Awesome Substring](https://hackmd.io/rSECrNhOTt28MGEvqBhksw)
前两题是同一个类型 后三题是同一个类型

### 连续变化
乍看之下需要找大于或者小于一个数的所有entry\
但仔细观察会发现只要找这个数即可\
因为变化是连续的 所以一定是这个数先出去 然后大于/小于它的entry才可能出现\
[2120. Execution of All Suffix Instructions Staying in a Grid](https://hackmd.io/vZadj8YgS66je8F2taAD5w)\
[1124. Longest Well-Performing Interval](https://hackmd.io/VmIhbESGTgCDiFRB2dnRFg)
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
[0154. Find Minimum in Rotated Sorted Array II](https://hackmd.io/7Ht9rietQa6YtJqaqT4H0w)\
[0034. Find First and Last Position of Element in Sorted Array](https://hackmd.io/o124knmVT7KGKOjTPFUCAg)\
[1533. Find the Index of the Large Integer](https://hackmd.io/tIGKI9WWSlax9KtRX2_TyQ)\
[2529. Maximum Count of Positive Integer and Negative Integer](https://hackmd.io/qPgV7hLOTrqbSzlRGFRCQw)\
[0302. Smallest Rectangle Enclosing Black Pixels](https://hackmd.io/P2FTEvAIQgeF_rYLoV7ylg)\
[0300. Longest Increasing Subsequence](https://hackmd.io/oPc5yL1oRhGtGP8UdRd3_g)\
[2389. Longest Subsequence With Limited Sum](https://hackmd.io/l5hF6FN6T66hno-ndYrvsw)\
[2426. Number of Pairs Satisfying Inequality](https://hackmd.io/ngD98TVUSXOEOUP66nF-lQ)\
[0852. Peak Index in a Mountain Array](https://hackmd.io/EQOMpC6lSBapVJ6PSnP2MA)\
[1712. Ways to Split Array Into Three Subarrays](https://hackmd.io/VyYwo5xuTAaCcCokB-6BTw)\
[2602. Minimum Operations to Make All Array Elements Equal](https://hackmd.io/ZXR1h6CER96MrOgxtoRo3w)
### Binary Search by Value
[1011. Capacity To Ship Packages Within D Days](https://hackmd.io/w9w2BtjpSsiVqhx9rhPGkQ)\
[1231. Divide Chocolate](https://hackmd.io/gB-3GUnbTzK2u0WNO6Yzxw)\
[1482. Minimum Number of Days to Make m Bouquets](https://hackmd.io/AEdtJ2k3TV-eQFe2cSo-UA)\
[1552. Magnetic Force Between Two Balls](https://hackmd.io/9umUWs4TTpyJCtBqrxkm-Q)\
[1870. Minimum Speed to Arrive on Time](https://hackmd.io/Lnohx5RtSya88dF3AL669w)\
[1891. Cutting Ribbons](https://hackmd.io/PlElcBsiTKSfWsxtn67wfA)\
[0275. H-Index II](https://hackmd.io/GIwOUjTPTx2S44anPZGMew)\
[2448. Minimum Cost to Make Array Equal](https://hackmd.io/DXfGz3FPTjygDK3q55Xnig)\
[2517. Maximum Tastiness of Candy Basket](https://hackmd.io/YYgWe4SBS9ScXBkxjp0SCA)\
[2528. Maximize the Minimum Powered City](https://hackmd.io/GsUUhcO-RyCfYtY8vnRQRQ)\
[1898. Maximum Number of Removable Characters](https://hackmd.io/kE3zJF-tSuWG3zWS6hxAtg)\
[2187. Minimum Time to Complete Trips](https://hackmd.io/VBlJPcDYSLSCPL8Z17el3w)\
[2560. House Robber IV](https://hackmd.io/QHqY5ENiR3ig9GsnoCFSMQ)\
[2594. Minimum Time to Repair Cars](https://hackmd.io/sPvgmc1GRmaKTAy6M6m_xA)
#### 重点复习
[1802. Maximum Value at a Given Index in a Bounded Array](https://hackmd.io/iLs1pcNwRm-KAwBQH_dMVA)\
[1608. Special Array With X Elements Greater Than or Equal X](https://hackmd.io/MjTGRGldSjKggKI-WXKzlw)\
[1300. Sum of Mutated Array Closest to Target](https://hackmd.io/AmhQgOSXQxuiuYJeTOymSQ)\
[2141. Maximum Running Time of N Computers](https://hackmd.io/A9EfBVIaSpm7SSmh07AeIQ)\
[1508. Range Sum of Sorted Subarray Sums](https://hackmd.io/1a4nVnUrR-WYq4H9jTHX4w)\
[2250. Count Number of Rectangles Containing Each Point](https://hackmd.io/YVGJtsfjQwOcriojK3gErQ)\
[2616. Minimize the Maximum Difference of Pairs](https://hackmd.io/DvZPao7xSMewDofJ6sC4xA)
### K-th Element
[1918. Kth Smallest Subarray Sum](https://hackmd.io/jyl8yjzlRFOLeg1_ctbjAg)

## TreeMap
treemap 要确保key不会重复才能用
当你需要给特定值找已经存在的值里面最接近的值的时候需要用到heap
当用到ceiling或者floor的函数的时候并且把结果赋给某一个变量的时候用Integer/Long 定义变量 因为ceiling和floor函数有可能传null回来

TreeMap 
```ceilingKey()/floorKey()``` 是找高于或等于自己的key 
```higherKey()/lowerKey()``` 是找高于/低于自己的key(不包含等于)

[2363. Merge Similar Items](https://hackmd.io/J08G-hkbQH2HO0TezEzJjQ)\
[1296. Divide Array in Sets of K Consecutive Numbers](https://hackmd.io/uG7m4jX7QK6TAVd1wOYvoQ)\
[0220. Contains Duplicate III](https://hackmd.io/tCC_eBr4Rc-XKqia8Cz9xA)\
[1488. Avoid Flood in The City](https://hackmd.io/gKFb3WZtR3eNxikpO1CJpw)\
[1606. Find Servers That Handled Most Number of Requests](https://hackmd.io/y7AOPFnTRgymeyjvmtiwgw)\
[0729. My Calendar I](https://hackmd.io/am3vFQC-TeuImofwjISHjQ)\
[0870. Advantage Shuffle](https://hackmd.io/w0INiSnmSJOkU2puietlOw)\
[0975. Odd Even Jump](https://hackmd.io/OjMVidnIS_6qXPD7UctFsQ)\
[1146. Snapshot Array](https://hackmd.io/NzBcZBxlSuKh0icF7E3bmg)\
[0715. Range Module](https://hackmd.io/6rfFcVTBTUmDiK3KlaaOmQ)\
[2070. Most Beautiful Item for Each Query](https://hackmd.io/obySHWqFScamlS-PShAxOg)
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
#### 区间最值* 区间总和
[1383. Maximum Performance of a Team](https://hackmd.io/bKCHp-8yTLi42s5emUM0WQ)\
[0857. Minimum Cost to Hire K Workers](https://hackmd.io/Ssaze_deSyi6x6qnHjWwHw)\
[2542. Maximum Subsequence Score](https://hackmd.io/5FRH1WNDS0e5CMXcu_ypqQ)
### Priority Queue+TreeMap
[1488. Avoid Flood in The City](https://hackmd.io/gKFb3WZtR3eNxikpO1CJpw)\
[1606. Find Servers That Handled Most Number of Requests](https://hackmd.io/y7AOPFnTRgymeyjvmtiwgw)
### Task Scheduler
都是借用了priority queue的idea 但是用了桶排序 因为元素个数都是有限的
如果不能有repeat pattern 那么先排出现次数最多的再排别的(前三题)\
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
**prev smaller item** -> monotonic **increasing** stack\
[1019. Next Greater Node In Linked List](https://hackmd.io/OZOq7H72T5m_AFULsw5Keg)\
[1856. Maximum Subarray Min-Product](https://hackmd.io/rExGf0PFSy6pQxyJtyGvtQ) (Window题)(可以和[1383. Maximum Performance of a Team](https://hackmd.io/bKCHp-8yTLi42s5emUM0WQ)以及[0857. Minimum Cost to Hire K Workers](https://hackmd.io/Ssaze_deSyi6x6qnHjWwHw)对比)\
[1063. Number of Valid Subarrays](https://hackmd.io/wkf9N1CaSWW5hIU-kUKRdA)\
[1966. Binary Searchable Numbers in an Unsorted Array](https://hackmd.io/6ibIKe8mS6CLGc2L6c9NWw)\
[0907. Sum of Subarray Minimums](https://hackmd.io/EyszVtjHSKmgqUQCIn-t-A)\
[2345. Finding the Number of Visible Mountains](https://hackmd.io/MT5NpzoQRMi6Hn8MA-lQOQ)\
[0853. Car Fleet](https://hackmd.io/NfOTVCXlSV2QgGnYoVhF4Q)\
[2104. Sum of Subarray Ranges](https://hackmd.io/N1TwDK9cQwuKHD8G0ZIyTA)
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
StringBuilder也可以看成stack\
[1209. Remove All Adjacent Duplicates in String II](https://hackmd.io/DOeKtFMuSZydHPXVbKsYyA)\
[0536. Construct Binary Tree from String](https://hackmd.io/m2_jgwwmS_iaxJ3Md55TKQ)\
[2296. Design a Text Editor](https://hackmd.io/5plBCFBITgSgW3uYFd9KoQ)\
[2434. Using a Robot to Print the Lexicographically Smallest String](https://hackmd.io/SWPeDgZnRCm0SQevUGeuoQ)
#### Parentheses
[0856. Score of Parentheses](https://hackmd.io/X4dO8hpbSPyyZxmQJsIHvg)\
[2116. Check if a Parentheses String Can Be Valid](https://hackmd.io/aXNEb1LTSJKb1QjOlgnFbw)
### Parse Expression
[0071. Simplify Path](https://hackmd.io/H8c-FO0TTOqNL5dacNZexA)\
[0224. Basic Calculator](https://hackmd.io/vwa99ktZThW6SxLy8R1kBQ)\
[0227. Basic Calculator II](https://hackmd.io/qV1I9kI-SMOLDSTyy744Ag)\
[0772. Basic Calculator III](https://hackmd.io/KNnsw05_QaGBO_nSjA-SSQ)

## Graph
[2077. Paths in Maze That Lead to Same Room](https://hackmd.io/GiY2wL09SjuzstyVuwbb1Q)
### One Outgoing Edge
[2359. Find Closest Node to Given Two Nodes](https://hackmd.io/rkWcS36jRWuZoBmKRuZH9g)\
[2374. Node With Highest Edge Score](https://hackmd.io/5Y1SnBv7RsSD__APokW97w)

## DFS
如果recursion里面不同分支只要有一个true 别的分支都不用看的话 就不需要记录每个node的结果([1306. Jump Game III](https://hackmd.io/DXDGFRc1SR2nttSNOosUYQ))
否则就需要记录每个node的结果\
[1306. Jump Game III](https://hackmd.io/DXDGFRc1SR2nttSNOosUYQ)\
[0200. Number Of Islands](https://hackmd.io/qbl68ROHQEObty3jQK_ItA)\
[0417. Pacific Atlantic Water Flow](https://hackmd.io/J7U3OUnKRkqjNbp2Pmjy_Q)
### matrix (避免重复)
[0562. Longest Line of Consecutive One in Matrix](https://hackmd.io/56Zexs7iTzG5ZBjUgg2RkQ)\
[0419. Battleships in a Board](https://hackmd.io/ttfskch1T9KylrMMkqHqJg)\
[1992. Find All Groups of Farmland](https://hackmd.io/CHHbwKV_R3SodD0m7VECbQ)
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
[1240. Tiling a Rectangle with the Fewest Squares](https://hackmd.io/agLq_D4QS5aSiQkNGyjmpw)\
[0679. 24 Game](https://hackmd.io/bv9x7GM0TH-ObArdnkkG3w)\
[1088. Confusing Number II](https://hackmd.io/S_3yNv8sRjeja1LBRekPhw)\
[2305. Fair Distribution of Cookies](https://hackmd.io/PyZsnMzJS7iygTghZY9ecA)\
[1718. Construct the Lexicographically Largest Valid Sequence](https://hackmd.io/RQLetjL5SKWS-XjTeddqXQ)
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
[0546. Remove Boxes](https://hackmd.io/T7eZJ9ZhQ9ayxS2ZVXdhKQ)(非常难想 没时间就跳过)\
[0756. Pyramid Transition Matrix](https://hackmd.io/e3HHCquFQpu8yG7RXpJHvg)\
[2646. Minimize the Total Price of the Trips](https://hackmd.io/SxPkuNLCSI2njX-lIhwKvQ)\
[2684. Maximum Number of Moves in a Grid](https://hackmd.io/MBjdfjYPScWoVf4RMEDFTQ)\
[2770. Maximum Number of Jumps to Reach the Last Index](https://hackmd.io/m1F8qtlUSJyPNyGubJTVDg)\
[2746. Decremental String Concatenation](https://hackmd.io/k-4VY38IQVSUU4rEJddBBQ)(经典)
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
[1810. Minimum Path Cost in a Hidden Grid](https://hackmd.io/QXJ1rUebQCqcr0ukhsWqRg)\
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
[1311. Get Watched Videos by Your Friends](https://hackmd.io/evsplVXwSlKp9PMdpIoyfw)\
[1559. Detect Cycles in 2D Grid](https://leetcode.com/problems/detect-cycles-in-2d-grid/submissions/)\
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
[0838. Push Dominoes](https://hackmd.io/RpV2rwrSQiKg4YLc1erpYQ)\
[1129. Shortest Path with Alternating Colors](https://hackmd.io/5W3g9nlwSi21RsBzEkpX5Q)
### Topological Sort
一个list of list的graph 一个int array记录每个点的degree
先把degree=0的加进queue里面 然后一点点bfs

[0210. Course Schedule II](https://hackmd.io/EzKnR3KLQayEp_SAYuXaYQ)\
[1136. Parallel Courses](https://hackmd.io/hP5U3AvSSwaPiBB4ch6Uaw)\
[2115. Find All Possible Recipes from Given Supplies](https://hackmd.io/Ksjixl-GS4i8IPUFVhLY0A)\
[2392. Build a Matrix With Conditions](https://hackmd.io/SSDkZWo3SKqk7RY65Yh7vQ)\
[2277. Closest Node to Path in Tree](https://hackmd.io/l_H1yuFdQnG6gajhmXgPKA)\
[2440. Create Components With Same Value](https://hackmd.io/PAWbHYEdTVq1buz9CmPD4g)
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
[1514. Path with Maximum Probability](https://hackmd.io/B7M8f6PUSdqHzZry7hDpSA)\
[2577. Minimum Time to Visit a Cell In a Grid](https://hackmd.io/k1vSBzNrT3qBcnO7CtToIA)\
[2642. Design Graph With Shortest Path Calculator](https://hackmd.io/F17iBk91TPuRSrvLFCn1Pg)
#### 2D Dijkstra
[2093. Minimum Cost to Reach City With Discounts](https://hackmd.io/VvFl9ny3Q1Ca1evfAMg0Iw)
#### 变式
找从起点到终点路径的最大的最小值或者最小的最大值
区别在于这里的题目：不需要记录从起点到现在点的最优解\
[1102. Path With Maximum Minimum Value](https://hackmd.io/QjOZ8IEyRTOJiMtn94A1FQ)\
[0778. Swim in Rising Water](https://hackmd.io/0P3Zi0RZQ1Stxj3pDvXciQ)
## Greedy
[0624. Maximum Distance in Arrays](https://hackmd.io/fWyuLHf9SK6RAiHQvWwU4w)\
[1578. Minimum Time to Make Rope Colorful](https://leetcode.com/problems/minimum-time-to-make-rope-colorful/)\
[1253. Reconstruct a 2-Row Binary Matrix](https://hackmd.io/50KYfhv-RdWejdAouFnyIQ)\
[2216. Minimum Deletions to Make Array Beautiful](https://hackmd.io/m7GV8k3IQsCLqiBz69_q5g)\
[2182. Construct String With Repeat Limit](https://hackmd.io/PR6JPID5RKeJ3-W7q8JMKw)\
[0670. Maximum Swap](https://hackmd.io/BRg5nV6yTJqspaUdaxQdSQ)\
[1727. Largest Submatrix With Rearrangements](https://leetcode.com/problems/largest-submatrix-with-rearrangements/)\
[1546. Maximum Number of Non-Overlapping Subarrays With Sum Equals Target](https://hackmd.io/hFLJpsHMT_2D499XIWuyYQ)\
[2311. Longest Binary Subsequence Less Than or Equal to K](https://hackmd.io/hm8hjl3tSLWBc0d3ttOUsg)\
[0792. Number of Matching Subsequences](https://hackmd.io/kJSKSTwjQ5mpwooWYJuZQQ)\
[2366. Minimum Replacements to Sort the Array](https://hackmd.io/FrwkQt_dS-m48pAfb5sQ5w)\
[2439. Minimize Maximum of Array](https://hackmd.io/ejVGqpfzSAiudUFNKWMzCQ)\
[2207. Maximize Number of Subsequences in a String](https://hackmd.io/vYY_MM65Qi6gbJ-srQ7yUw)\
[2522. Partition String Into Substrings With Values at Most K](https://hackmd.io/tjNex24oQrybd4fKKnLs1Q)\
[2087. Minimum Cost Homecoming of a Robot in a Grid](https://hackmd.io/GSVK8uw8RH61dKAjsvFP8w)\
[2086. Minimum Number of Food Buckets to Feed the Hamsters](https://hackmd.io/yodDL1GRQaOboRVmJWOHjw)\
[1899. Merge Triplets to Form Target Triplet](https://hackmd.io/PU1Y8a9lRfiCxh7HOkhRsA)\
[2541. Minimum Operations to Make Array Equal II](https://hackmd.io/Rsw86XJERdyApq1faFdm2A)\
[1702. Maximum Binary String After Change](https://hackmd.io/iTkDngiTTEuhheZoJDiL2g)\
[2592. Maximize Greatness of an Array](https://hackmd.io/QtBFzz-NTpKu2rwCZSyqDw)\
[2601. Prime Subtraction Operation](https://hackmd.io/aO_ZiVxaRSmT1EAbFpjvkA)\
[1710. Maximum Units on a Truck](https://hackmd.io/Azp1JADsRNizhVwrvm2YGQ)
### 典型题
[0055. Jump Game](https://leetcode.com/problems/jump-game/)\
[0045. Jump Game II](https://hackmd.io/eBarqjRNTIOUYBMU64wLKg)\
[0870. Advantage Shuffle](https://hackmd.io/w0INiSnmSJOkU2puietlOw)\
[2242. Maximum Score of a Node Sequence](https://hackmd.io/6XBAA7e4Sz2ttK3iSCFgwQ)\
[0910. Smallest Range II](https://hackmd.io/l0fVPqkiQG2vzFG1vErCNg)\
[0871. Minimum Number of Refueling Stops](https://hackmd.io/4kblNIOAREG95Yd9oBd4Kg)\
[2554. Maximum Number of Integers to Choose From a Range I](https://hackmd.io/8WSzFyiGRVilV5xszzchVg)\
[2560. House Robber IV](https://hackmd.io/QHqY5ENiR3ig9GsnoCFSMQ)\
[2587. Rearrange Array to Maximize Prefix Score](https://hackmd.io/orzt5TBsQgC43EQAM3-n5Q)\
[2616. Minimize the Maximum Difference of Pairs](https://hackmd.io/DvZPao7xSMewDofJ6sC4xA)
### Greedy+Sliding Window
[2271. Maximum White Tiles Covered by a Carpet](https://hackmd.io/7FnX3SCASZyuEec1uVk90w)\
[2772. Apply Operations to Make All Array Elements Equal to Zero](https://hackmd.io/i6u-Oj7zT1y0-53eZhImGQ)
### Greedy+Two Pointers
[2576. Find the Maximum Number of Marked Indices](https://hackmd.io/ywDm08ECTGOyV6pOqdpH2A)
### LIS
[0300. Longest Increasing Subsequence](https://hackmd.io/oPc5yL1oRhGtGP8UdRd3_g)(非常经典)\
[1964. Find the Longest Valid Obstacle Course at Each Position](https://hackmd.io/L_tAL8h3RpCeAvmC8-wtUw)\
[2111. Minimum Operations to Make the Array K-Increasing](https://hackmd.io/DloEOqTUStWAbxMlV5SF3g)\
[OA-001. Minimum Number of Groups of Non-overlapping Rectangles](https://hackmd.io/DO-FYACFR7mWnHy4J_Yiug)
### DI Sequence
[0942. DI String Match](https://hackmd.io/gE6jl366S_aqxpTzLNEpAg)\
[2375. Construct Smallest Number From DI String](https://hackmd.io/z0lYYhNJR1K5Jj5IOXQ1qw)\
[0484. Find Permutation](https://hackmd.io/4ujIWKjLTJuQceHC4FiAlw)
### Two Pass
[0135. Candy](https://hackmd.io/JkqMiZmmShydlXFmOl77bQ)\
[1840. Maximum Building Height](https://hackmd.io/beQ5zgTgRDOs1R8jVG_1sQ)
### Three Pass
**判断是否有edge case: 看在index 0之前切和在index n之后切是不是合理的切割方式**\
可以用1653和1664做比较\
[1525. Number of Good Ways to Split a String](https://hackmd.io/YFy7WOenTZKJIMFnIvCDTw)\
[1653. Minimum Deletions to Make String Balanced](https://hackmd.io/5scXhgTNT5C0dXGJ-f3w_g)\
[1664. Ways to Make a Fair Array](https://hackmd.io/D3O-YgNAR2SS1WVWIblhKQ)\
[1769. Minimum Number of Operations to Move All Balls to Each Box](https://hackmd.io/yIxRhPuHQZ6cNvmQ9kkj1A)\
[1638. Count Substrings That Differ by One Character](https://hackmd.io/SBqE6k-ER9WtRYuWQ4bU2A)\
[1671. Minimum Number of Removals to Make Mountain Array](https://hackmd.io/Y3AT-XbbQZKLxO3o71N1Dg)\
[2163. Minimum Difference in Sums After Removal of Elements](https://hackmd.io/QEbHY4v_TXG_QpQ_xcvViw)
### Sorting
[1846. Maximum Element After Decreasing and Rearranging](https://hackmd.io/poVifZuSQWeUTD7BSI2TWw)\
[0826. Most Profit Assigning Work](https://hackmd.io/z5bNLVGsSzCGE5AglNTQQg)\
[1402. Reducing Dishes](https://hackmd.io/dC_fjXQQT4y3W514zoCRwg)\
[1996. The Number of Weak Characters in the Game](https://hackmd.io/2UZGkGZaQzKQWc9s4WLLvw)\
[1564. Put Boxes Into the Warehouse I](https://hackmd.io/Z5QlgkWaQja7oXEvTPc2JQ)\
[1580. Put Boxes Into the Warehouse II](https://hackmd.io/9eSU753wSH6ZPsqolYtgAg)\
[0406. Queue Reconstruction by Height](https://hackmd.io/nd3GpGxWQZKaMylQigekIA)\
[2410. Maximum Matching of Players With Trainers](https://hackmd.io/V02t5DH0RNCZCV747NS_zA)\
[2358. Maximum Number of Groups Entering a Competition](https://hackmd.io/bXjvg1gFRSO_EACl6MNIng)\
[1705. Maximum Number of Eaten Apples](https://hackmd.io/hVhh2RqqQ7yNlfdOkQMqIQ)\
[1792. Maximum Average Pass Ratio](https://hackmd.io/BbRp_dzORMCJsamRv-Ys4w)\
[0502. IPO](https://hackmd.io/Af42eXaAQRWOGaUvFKj_tA)\
[1642. Furthest Building You Can Reach](https://hackmd.io/hbpU4A84RAe-XeDIXgiwrg)\
[2208. Minimum Operations to Halve Array Sum](https://hackmd.io/u2MQbHLzRqSIYFM5e6wqMQ)\
[2323. Find Minimum Time to Finish All Jobs II](https://hackmd.io/cRoWvcoVTkiX5CeGpbcJ0Q)\
[2165. Smallest Value of the Rearranged Number](https://hackmd.io/nRsZiX-qSUOV9bwIQQHZjA)\
[2589. Minimum Time to Complete All Tasks](https://hackmd.io/Y22ahKw5Sqa0hIJTYZuEEw)\
[2599. Make the Prefix Sum Non-negative](https://hackmd.io/Wl6UXoppR9OpwJaTbJPTLw)\
[2054. Two Best Non-Overlapping Events](https://hackmd.io/T0Ld4gfBTTmV8oKgNpk0qQ)
### State Machine
[0524. Longest Word in Dictionary through Deleting](https://hackmd.io/hZKZPqUxRyaISwaadQKxeg)\
[1055. Shortest Way to Form String](https://hackmd.io/EC562s-9QwKzCHOiR6Pyvw)\
[2055. Plates Between Candles](https://hackmd.io/ulJFsLWxS6K4xETiTcqqsA)\
[2370. Longest Ideal Subsequence](https://hackmd.io/ibr0WHRZR6G_8wycI0Qdow)
### Smear Top Elements
[2233. Maximum Product After K Increments](https://hackmd.io/O8P_ou0dTMShNERgRAej_A)\
[2333. Minimum Sum of Squared Difference](https://hackmd.io/FhLXvSfLS1OwafO7X47_4A)
### Parentheses
[1541. Minimum Insertions to Balance a Parentheses String](https://hackmd.io/Vn9tzAC6QV-R7uWpjFgynw)\
[1249. Minimum Remove to Make Valid Parentheses](https://hackmd.io/bQqvjRSvQZq1snaqqSgEDQ)\
[0921. Minimum Add to Make Parentheses Valid](https://hackmd.io/BW_TqN0oTsq6f0gxlYxXHw)\
[1963. Minimum Number of Swaps to Make the String Balanced](https://hackmd.io/35PDvD25ROuPysdPctFA2w)
### Interval
对区间排序的贪心法，有的需要sort by starting point，有的需要sort by ending point. 大致的规律是：

如果求的是maximum number of non-overlapping intervals，用sort by ending point的方法\
如果求的是minimum number of intervals to cover the whole range，用sort by starting point的方法\

[1272. Remove Interval](https://hackmd.io/4GRcjxk7R4i6IkjPQgchSQ)\
[1288. Remove Covered Intervals](https://hackmd.io/hAPJGIJXR_uMlii6mR5hLQ)
#### Maximum Number of Non-overlapping Intervals
[0435. Non-overlapping Intervals](https://hackmd.io/uFsAyMtgTiGM9LE-8ycrqA)\
[0646. Maximum Length of Pair Chain](https://hackmd.io/4ArioNycT_aV4WTpDfRBjw)
#### Maximum Profit Non-overlapping Interval
[2008. Maximum Earnings From Taxi](https://hackmd.io/uszy0XX3SOSyAB754hXTbw)\
[1235. Maximum Profit in Job Scheduling](https://hackmd.io/mEcrQmsWTkeLAg3nXw22sA)
#### Minimum Number of intervals to cover the whole range (Jump Game)
[1024. Video Stitching](https://hackmd.io/DLEdtqZQTC-_GZZbrfkRrg)\
[1326. Minimum Number of Taps to Open to Water a Garden](https://hackmd.io/QrzwQB8vQp2dJOMw_rs8mw)

### Constructive Problems
[0667. Beautiful Arrangement II](https://hackmd.io/XNW9FPr1SNWHpzuqmtHg4Q)\
[2007. Find Original Array From Doubled Array](https://hackmd.io/Y-esg71RQ5iNb5Knm5K0pA)\
[2498. Frog Jump II](https://hackmd.io/ikBxY7scS_-WUcCB-1ieAw)\
[2499. Minimum Total Cost to Make Arrays Unequal](https://hackmd.io/WLimdtjqR2eEYtft8-WSUA)
## Tree
[0572. Subtree of Another Tree](https://hackmd.io/oFMek64ETdCGrC_0NIR4rQ)\
[0958. Check Completeness of a Binary Tree](https://hackmd.io/EVLsEc5iTWCNbG3T710TgA)\
[1104. Path In Zigzag Labelled Binary Tree](https://hackmd.io/EVA8Pu5xSpWObcu4cf3uJw)\
[0226. Invert Binary Tree](https://hackmd.io/aaQaRXvoTXuEMxpnF9jU3Q)\
[0894. All Possible Full Binary Trees](https://hackmd.io/jJIxXlR4QTWkt9LTyV8nMw)\
[0951. Flip Equivalent Binary Trees](https://hackmd.io/_RoWQI31SFa6SdCO-TZPzg)\
[1120. Maximum Average Subtree](https://hackmd.io/mqRbiu-_QX6oasnRXhGsaQ)
### Binary Search Tree
[0098. Validate Binary Search Tree](https://hackmd.io/lTUSAW2EQVaTim1feD1YrA)\
[0285. Inorder Successor in BST](https://hackmd.io/nFez6sm8TD-eLu6PshxUfw)(经典)\
[0173. Binary Search Tree Iterator](https://hackmd.io/7BSUG7MBQ7mpEnKGhYW1YQ)\
[0235. Lowest Common Ancestor of a Binary Search Tree](https://hackmd.io/irC3SlpLSda4ljtH_iIVxg)\
[2476. Closest Nodes Queries in a Binary Search Tree](https://hackmd.io/Hml-s9i_RXW7p4EgQMSn-w)
### Traversal
#### Inorder Traversal
[2476. Closest Nodes Queries in a Binary Search Tree](https://hackmd.io/Hml-s9i_RXW7p4EgQMSn-w)
#### Inorder Traversal + Preorder Traversal
[0105. Construct Binary Tree from Preorder and Inorder Traversal](https://hackmd.io/_3SP-g24R_Gcdm840I_vUg)
#### Inorder Traversal + Postorder Traversal
[0106. Construct Binary Tree from Inorder and Postorder Traversal](https://hackmd.io/XVd0tJtlTbOwDRsNDBfp9w)
#### Level Order Traversal
[2471. Minimum Number of Operations to Sort a Binary Tree by Level](https://hackmd.io/A_yK1nswTE-2tAE9nPmCqA)\
[0513. Find Bottom Left Tree Value](https://hackmd.io/R58JxhlbT7OssTKbrF_BpA)\
[0637. Average of Levels in Binary Tree](https://hackmd.io/O02hytr6Sw6JqxXaVsh7Bg)\
[2583. Kth Largest Sum in a Binary Tree](https://hackmd.io/Bdxss1k1QjSBy2bW5KDJoA)\
[2641. Cousins in Binary Tree II](https://hackmd.io/ZtR8IzA7SQ-7dIrMZ-He-A)
### dfs + Tree
[0110. Balanced Binary Tree](https://hackmd.io/qytkvtqYQQSKtQq8QP1x9g)(经典)\
[2467. Most Profitable Path in a Tree](https://hackmd.io/wgTl8LzpQTCJ1siUYKtUHw)\
[2477. Minimum Fuel Cost to Report to the Capital](https://hackmd.io/TcFjlC7vTOmaoUbgEugtwA)\
[2445. Number of Nodes With Value One](https://hackmd.io/qrka8RCoQ4urQEf30NXC8Q)\
[0508. Most Frequent Subtree Sum](https://hackmd.io/-4Qw3rTOQcy8bhMs8mMsqA)
#### Height of Tree
[2458. Height of Binary Tree After Subtree Removal Queries](https://hackmd.io/dlZWap63RNmqEE9YHv38bg)
#### Path in a tree
需要一个global variable来存答案
因为每次dfs都只会找包含left/right child的subtree里的最优值(注意：一定是包含left/right tree)
但path需要把left subtree和right subtree的解加在一起\
[1022. Sum of Root To Leaf Binary Numbers](https://hackmd.io/V4AyUQyZTxGBZUnVjhrFpA)\
[0543. Diameter of Binary Tree](https://hackmd.io/FPZpR3NBQuCV_u2vTZaEvQ)(经典)\
[0124. Binary Tree Maximum Path Sum](https://hackmd.io/mi68cm-8Sb6V2g0ZXwCy3Q)(经典)\
[0549. Binary Tree Longest Consecutive Sequence II](https://hackmd.io/E80ctt87TcmNmZW-bx2gAw)\
[1522. Diameter of N-Ary Tree](https://hackmd.io/lu9uAfWDSS6V8yUnGRSBgw)\
[0687. Longest Univalue Path](https://hackmd.io/yr5bIriNQ3ahO_D6ah679Q)(经典)\
[2049. Count Nodes With the Highest Score](https://hackmd.io/tTfQSMKxRoKh7xAlV3PwHA)\
[2246. Longest Path With Different Adjacent Characters](https://hackmd.io/CxJftNNbS9CyGJTXJ2j8Pg)
##### Cost of Path
[2673. Make Costs of Paths Equal in a Binary Tree](https://hackmd.io/ZEF3r16WT_OxVeSZuZQL1w)
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
### Build Tree
[2196. Create Binary Tree From Descriptions](https://hackmd.io/rla8Ip7RT3K168eDWIsUKw)
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
[1101. The Earliest Moment When Everyone Become Friends](https://hackmd.io/wPYXfO1uThWhC_ZxLBZY9g)\
[2316. Count Unreachable Pairs of Nodes in an Undirected Graph](https://hackmd.io/1DNgBhf7RvqzdgrTp_VlGA)
[1202. Smallest String With Swaps](https://hackmd.io/eSIiROjkS4yq6QI1RhjmQg)\
[1722. Minimize Hamming Distance After Swap Operations](https://hackmd.io/Dr9cQU9NRPqvspNUPb1XZg)\
[0721. Accounts Merge](https://hackmd.io/E2AEXy2RSy6718CqqOLhNA)\
[0990. Satisfiability of Equality Equations](https://hackmd.io/zsQmaUycR--KoeZktOk5zw)\
[0785. Is Graph Bipartite?](https://hackmd.io/JhGlMsDdQB2981MMMjP-fQ)(两种解法)\
[0839. Similar String Groups](https://hackmd.io/MB4hkOjqQ16o7pUkG3rKrg)\
[2092. Find All People With Secret](https://hackmd.io/hwFbv3adRDulvBhoD1YzqQ)\
[2492. Minimum Score of a Path Between Two Cities](https://hackmd.io/AwbABRIOTluGFnEtZNCeFw)
### Reverse Union Find
[2382. Maximum Segment Sum After Removals](https://hackmd.io/RWkBUOs2RIWpXRdC95LdYQ)
### Union by an Order
[1697. Checking Existence of Edge Length Limited Paths](https://hackmd.io/pFeiq6JLSmSzs26pBw-L3Q)\
[2421. Number of Good Paths](https://hackmd.io/fiQDv27nQ7e-Rx86uMdL6w)
### Minimum Spanning Tree
[1135. Connecting Cities With Minimum Cost](https://hackmd.io/Fo-g8osYTGOAsqcF18Ljxw)\
[1168. Optimize Water Distribution in a Village](https://hackmd.io/jpwmOiMDRnCtNHtmKf8Lmg)
### Union by Index
[0947. Most Stones Removed with Same Row or Column](https://hackmd.io/S7lrCKT0QKSPqvteahktDw)\
[1632. Rank Transform of a Matrix](https://hackmd.io/5wVtncoBTc-sykHAtj8QKA)
### Factors
[1627. Graph Connectivity With Threshold](https://hackmd.io/P2s41S2FSxm2_0SF2HirgQ)
## Bit Manipulation
[0318. Maximum Product of Word Lengths](https://hackmd.io/6dKXgpkzQ6-NDUr0P9frbw)\
[1356. Sort Integers by The Number of 1 Bits](https://hackmd.io/-mnod4xZTfakGIyNTc_-jQ)\
[2275. Largest Combination With Bitwise AND Greater Than Zero](https://hackmd.io/Vwz7huQQS-CYWuAsOvUv_A)\
[2411. Smallest Subarrays With Maximum Bitwise OR](https://hackmd.io/ZpvC5bG4QnKWEv6aYWgSxQ)\
[1404. Number of Steps to Reduce a Number in Binary Representation to One](https://hackmd.io/mQ6nlTmIT1mWyCeydiBYZw)
### XOR
异或运算的性质
![](https://i.imgur.com/0FMV1XI.png)\
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
[2429. Minimize XOR](https://hackmd.io/LXIg8NoKTVGW91_uLnttRA)\
[0779. K-th Symbol in Grammar](https://hackmd.io/g0XUmDIYSSyutghCE2WAaw)\
[2527. Find Xor-Beauty of Array](https://hackmd.io/D2QLH61QQvWC_l2fTrrUyg)\
[2564. Substring XOR Queries](https://hackmd.io/CEeWxps3QL2aLedla5Bv6A)\
[1720. Decode XORed Array](https://hackmd.io/wWEoxlB0SVKcP6NdBfjBkA)
### OR
[2568. Minimum Impossible OR](https://hackmd.io/_xWnArgKTO6f2pAq06z9Bw)
### Bitmask
[0320. Generalized Abbreviation](https://hackmd.io/b9bB2QFORuKd1-H3IFa1qg)\
[1774. Closest Dessert Cost](https://hackmd.io/MC1wn6lhSPeHdvyJT5EQKg)(三进制)\
[2002. Maximum Product of the Length of Two Palindromic Subsequences](https://hackmd.io/I_cQd8R3QcyF9k4t3EP4ig)\
[1239. Maximum Length of a Concatenated String with Unique Characters](https://hackmd.io/awaBJbC1TlWNQ49kgWgNqg)\
[2135. Count Words Obtained After Adding a Letter](https://hackmd.io/4HXcFkyvTJ6EYYohz0lDkg)\
[0869. Reordered Power of 2](https://hackmd.io/DI2r73tdTXm5Fjx8So-cRw)(十进制)
#### Meet in the middle
[2035. Partition Array Into Two Arrays to Minimize Sum Difference](https://hackmd.io/I22jyyq6QmejNugcm3CUdQ)
## Deque
**Sliding Window Maximum** (在sliding window里找maximum) 模版:
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
[1696. Jump Game VI](https://hackmd.io/PkwAF5OZRUKwbtJZpNJMKQ)\
**单调deque**\
[2762. Continuous Subarrays](https://hackmd.io/DQ7-uaMfTBeBac5Rd_W9TQ)
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
[2416. Sum of Prefix Scores of Strings](https://hackmd.io/I4owiG_-RgGlvbAtyXamfg)\
[0425. Word Squares](https://hackmd.io/hrLSYddJQZOIqy50UY2UiA)
### Trie for non-string
[2352. Equal Row and Column Pairs](https://hackmd.io/oAaFKC6pRRmFm-kpg1qjUQ)
### Trie+DFS
[2452. Words Within Two Edits of Dictionary](https://hackmd.io/lOsKNu89Sy2_SO1a7rDILg)
## Linked List
翻转linked list
```
class Solution {
    public ListNode reverseList(ListNode head) {
        ListNode prev = null;
        ListNode curr = head;
        ListNode next;
        while(curr!=null){
            next = curr.next;
            curr.next = prev;
            prev = curr;
            curr = next;
        }
        return prev;
    }
}
```
需要swap node的时候看清题目要求是**要swap值还是swap node** ([1721. Swapping Nodes in a Linked List](https://hackmd.io/t7cDQNa5R3iyyw0SdZw_Gg))\
[0061. Rotate List](https://hackmd.io/fNN_O2qPT2OjcYV8VaQ4Nw)\
[0086. Partition List](https://hackmd.io/qbiIN4s2Rkyk-Fs_QsGK5Q)\
[0369. Plus One Linked List](https://hackmd.io/z67xI6jmTVWpEcD8GhOM8Q)\
[1474. Delete N Nodes After M Nodes of a Linked List](https://hackmd.io/SIxTI8hHTAKkbl2rNbMorQ)\
[0082. Remove Duplicates from Sorted List II](https://hackmd.io/VA1lmVyUQlOzeOLqI3mTlg)\
[1836. Remove Duplicates From an Unsorted Linked List](https://hackmd.io/8tLNzrYPTdWe3ssvqeg0tA)\
[0379. Design Phone Directory](https://hackmd.io/ztM5wkeEQvSsCGpTugxmGg)\
[1171. Remove Zero Sum Consecutive Nodes from Linked List](https://hackmd.io/S347XZc-Q2u1-62Wpzha3A)\
[0237. Delete Node in a Linked List](https://hackmd.io/CPPiWzYVTZmYVfiYwlLZww)\
[2046. Sort Linked List Already Sorted Using Absolute Values](https://hackmd.io/mp_hWTqlTfCGfHMj1zUOdg)\
[1721. Swapping Nodes in a Linked List](https://hackmd.io/t7cDQNa5R3iyyw0SdZw_Gg)

### Reverse Linked List
[0206. Reverse Linked List](https://hackmd.io/S8XKw5EbRsict3n4C7_0qg)\
[0092. Reverse Linked List II](https://hackmd.io/98PAuvfURuiUW_5X_bEbKw)\
[2487. Remove Nodes From Linked List](https://hackmd.io/mQG5JU3YTiSRaq2gXb3dSg)\
[2130. Maximum Twin Sum of a Linked List](https://hackmd.io/UeEY5fpgSrKePx_7_di0kw)

### 快慢指针
[0109. Convert Sorted List to Binary Search Tree](https://hackmd.io/xGmhY4bSQ7ewSkjhKZfDDA)\
[0142. Linked List Cycle II](https://hackmd.io/iiXmhYCfR32eRwFxjl876Q)\
[2130. Maximum Twin Sum of a Linked List](https://hackmd.io/UeEY5fpgSrKePx_7_di0kw)\
[2095. Delete the Middle Node of a Linked List](https://hackmd.io/ZeaqT940QUaxFvd2e747OA)

##  DP
[讲解](https://blog.csdn.net/u013309870/article/details/75193592)
[套路讲解](https://www.youtube.com/watch?app=desktop&v=FLbqgyJ-70I&t=6554s)
[套路ppt](https://docs.google.com/presentation/d/1F_Qp3kzw7jZkPpb7ll7J6-02285bCA3Z9nmU1e7a2rk/edit#slide=id.g82af7adac0_0_675)\
简单来说就是用已经解决过了的子问题的解去解新的问题\
[0221. Maximal Square](https://hackmd.io/0Ie3z7ZRSH6sB5fMh1ZP7g)\
[1277. Count Square Submatrices with All Ones](https://hackmd.io/rfyE5TsLSGmlkOMPANdsGQ)\
[2380. Time Needed to Rearrange a Binary String](https://hackmd.io/q8tVNfCGRw-VHP-q3erW5Q)\]
[2495. Number of Subarrays Having Even Product](https://hackmd.io/cU9tF0OZRKGz6qwPKh6t7Q)
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
[2400. Number of Ways to Reach a Position After Exactly k Steps](https://hackmd.io/wER00MrASZil427NsqQ44Q)\
[2393. Count Strictly Increasing Subarrays](https://hackmd.io/CZfj2WDLREODRhcFq_lc-g)\
[2369. Check if There is a Valid Partition For The Array
](https://hackmd.io/cy7QDw-dTxiAHAW57zkUqg)\
[1911. Maximum Alternating Subsequence Sum](https://hackmd.io/iUU3o61HQ12ZHVx_hinMhQ)\
[2100. Find Good Days to Rob the Bank](https://hackmd.io/dLyiJDP8QoiIX8R0fuZp2Q)\
[1997. First Day Where You Have Been in All the Rooms](https://leetcode.com/problems/first-day-where-you-have-been-in-all-the-rooms/description/)\
[2555. Maximize Win From Two Segments](https://hackmd.io/HKJMbIInThiVNpzZHnf_og)\
[2646. Minimize the Total Price of the Trips](https://hackmd.io/SxPkuNLCSI2njX-lIhwKvQ)\
[2771. Longest Non-decreasing Subarray From Two Arrays](https://hackmd.io/aAUF2EriSVqr3KhEWlU1jQ)
#### Kadane’s algorithm
Kadane’s algorithm 求最大subsequence和\
currMax记录以当前元素结尾的最大subsequence和\
ans记录整个遍历过程的最大subsequence和\
[2606. Find the Substring With Maximum Cost](https://hackmd.io/wg87LZp4Tc2iM5rkfCOeVQ)\
[0053. Maximum Subarray](https://hackmd.io/qpgZUbERQVOXcw9DSBI1Mw)


#### 变式 (把"权利"写进状态)
[0487. Max Consecutive Ones II](https://hackmd.io/8lcD9MH8RAqKwz7DVjNtGg)\
[1186. Maximum Subarray Sum with One Deletion](https://hackmd.io/mEeqqUmARlmmtyQR_chxVQ)\
[1746. Maximum Subarray Sum After One Operation](https://hackmd.io/qN2Bh6RxQAO7Xkv_oNGwdg)\
[0552. Student Attendance Record II](https://hackmd.io/_1beCVHnTjuoJjSgzfgV4Q)
### 基本型 II (时间序列加强版) $O(N^2)$
![](https://i.imgur.com/vEITlRV.png)
由于某些题需要设置初始值当作dp[0], 也就是需要让nums[0]对应到dp[1], 相比基本型I, 这里考虑这种情况会比较麻烦, 所以通常情况下会在前面加一个凑数的num或者char (例如[1043. Partition Array for Maximum Sum](https://hackmd.io/sSjKhGdcQrmWNvAvq0s6bw), [1105. Filling Bookcase Shelves](https://hackmd.io/SStKMDA2S2OdA5X256a7KA), [1416. Restore The Array](https://hackmd.io/6PmS-oOITbqSovcqAbppVw))

#### LIS
[0300. Longest Increasing Subsequence](https://hackmd.io/oPc5yL1oRhGtGP8UdRd3_g)\
[0673. Number of Longest Increasing Subsequence](https://hackmd.io/ggEUM5vIS36_nrs5h0VGMQ)\
##### LIS变式
[2501. Longest Square Streak in an Array](https://hackmd.io/6rorUPu3Q0a3Hitj6W2Rtw)

[0368. Largest Divisible Subset](https://hackmd.io/T9YlpxKmRjOCKFFdyiWDsg)\
[1626. Best Team With No Conflicts](https://hackmd.io/SIztzm-uQ2yzVNtop0zoxw)

[2209. Minimum White Tiles After Covering With Carpets](https://hackmd.io/UEAOe9NtRSSb7fQkrmefhw)(Good)\
[0983. Minimum Cost For Tickets](https://hackmd.io/9G_ZvJRARB6gUpo1ob1JCw)\
[2188. Minimum Time to Finish the Race](https://hackmd.io/OuEE-5SKRG6r3Fz8KFSJfQ)\
[2464. Minimum Subarrays in a Valid Split](https://hackmd.io/0BDxqHTlQ_eLVBqV4h2Utg)\
[2767. Partition String Into Minimum Beautiful Substrings](https://hackmd.io/Iq3vbVtISeioqdgKdeWRhA)
#### 分组题
找到前一个group的最后一个元素\
[1105. Filling Bookcase Shelves](https://hackmd.io/SStKMDA2S2OdA5X256a7KA)\
[1043. Partition Array for Maximum Sum](https://hackmd.io/sSjKhGdcQrmWNvAvq0s6bw)\
[1416. Restore The Array](https://hackmd.io/6PmS-oOITbqSovcqAbppVw)\
[2547. Minimum Cost to Split an Array](https://hackmd.io/jfxADG3WRVyv0JPtwwO6lw)\
[2052. Minimum Cost to Separate Sentence Into Rows](https://hackmd.io/5Fvhe7pKT3ulgT1AJdRqKw)
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
[0410. Split Array Largest Sum](https://hackmd.io/nNeGw-FeSyWghLf5ZB2C-Q)\
[2472. Maximum Number of Non-overlapping Palindrome Substrings](https://hackmd.io/a3qCcz_eQnaWaV9yhg5npw)\
[1039. Minimum Score Triangulation of Polygon](https://hackmd.io/DeG_gFXGT46K7IHUUZfCZg)
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
[1130. Minimum Cost Tree From Leaf Values](https://hackmd.io/7M8-WsJfRuq7mjHclMToyA)\
[1000. Minimum Cost to Merge Stones](https://hackmd.io/QRciXajURWuji7hJ8RiwYQ)\
[0823. Binary Trees With Factors](https://hackmd.io/jjDCGQvqSXuBymBcyEx2Eg)
### 背包问题
![](https://i.imgur.com/vbETTQv.png)
![](https://i.imgur.com/K3aHXJE.png)
[0474. Ones and Zeroes](https://hackmd.io/A71TsrJ_RIGo-0jIczcCNw)\
[0494. Target Sum](https://hackmd.io/BBt3Z9T0Tx-vNuZzFlZpGg)\
[0416. Partition Equal Subset Sum](https://hackmd.io/18plVWdQSjutpHD_ownwSg)\
[2291. Maximum Profit From Trading Stocks](https://hackmd.io/4xQawwDKS2mDMhinroeCnw)\
[1049. Last Stone Weight II](https://hackmd.io/yWIIxo5BQoSW_hZOX_fE-A)\
[1155. Number of Dice Rolls With Target Sum](https://hackmd.io/Ggss6gIST_iJbvuQZ6kNyA)\
[2585. Number of Ways to Earn Points](https://hackmd.io/SpLChJeDSYahBpdo4lOeXg)
#### 需要优化的背包问题
[1981. Minimize the Difference Between Target and Chosen Elements](https://hackmd.io/O_ABik1mTem5D5LSaq0ITA)\
[0879. Profitable Schemes](https://hackmd.io/Cg7s2gppSh-wVY2CJ0i3Mw)\
[0956. Tallest Billboard](https://hackmd.io/6Tv_k3eGSyqIcgKd5MDx7w)
#### 每个物品可以用无限多次
外层遍历状态 里层遍历coin
[0322. Coin Change](https://hackmd.io/4FjJq5P_Sc6miBP0IwKc6A)(经典)\
[0518. Coin Change 2](https://hackmd.io/azimrNJRRUK0CBaC2d0Ivg)(经典)\
[0691. Stickers to Spell Word](https://hackmd.io/g6-O9OjCRiqSgbKVNXC2Ig)\
[2466. Count Ways To Build Good Strings](https://hackmd.io/8WmbxJ2oR1CpMcIwNn6rxw)
### 状态压缩
[1125. Smallest Sufficient Team](https://hackmd.io/iziZ5qIEQjeGGCX5Aj_p3g)\
[0691. Stickers to Spell Word](https://hackmd.io/g6-O9OjCRiqSgbKVNXC2Ig)\
[1349. Maximum Students Taking Exam](https://hackmd.io/pIRFwFXgQGWTbTNDPwrYDg)\
[1411. Number of Ways to Paint N × 3 Grid](https://hackmd.io/AKffexhVRtGqAo1_PAqr2Q)\
[1931. Painting a Grid With Three Different Colors](https://hackmd.io/9pdSzNvwR6-_64BhTSQWKg)\
[2184. Number of Ways to Build Sturdy Brick Wall](https://hackmd.io/1R8nFxZ3T4uThpurkQVXgw)\
[2172. Maximum AND Sum of Array](https://hackmd.io/vc-71KEBTbKbhxILYakSnw)
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
[1301. Number of Paths with Max Score](https://hackmd.io/kApGbvmOTPeKpxkaxO5rfg)\
[2304. Minimum Path Cost in a Grid](https://hackmd.io/z-nOqk_LTsKEqs8fRU7jew)
### Rolling DP
[2369. Check if There is a Valid Partition For The Array
](https://hackmd.io/cy7QDw-dTxiAHAW57zkUqg)\
[2327. Number of People Aware of a Secret](https://hackmd.io/Hm59bhDlRHisd-TvZ8axGg)
## Recursion
[0427. Construct Quad Tree](https://hackmd.io/Egf4XnCPRRqBzU8O4ZhB_g)\
[0337. House Robber III](https://hackmd.io/moBB-Q7pRgyqfueB3Hx4EA)\
[2378. Choose Edges to Maximize Score in a Tree](https://hackmd.io/09i3KtqjSr6ArkaIuQRh_w)\
[0404. Sum of Left Leaves](https://hackmd.io/6cw6pPBfRuC99uWQtkGdHA)\
[0779. K-th Symbol in Grammar](https://hackmd.io/g0XUmDIYSSyutghCE2WAaw)
## Simulation
[2257. Count Unguarded Cells in the Grid](https://hackmd.io/ZmQOPyHORVmk081ZLgbjfw)\
[1894. Find the Student that Will Replace the Chalk](https://hackmd.io/Y4Jo2oLCQ4yNE-emJLeYjQ)\
[2120. Execution of All Suffix Instructions Staying in a Grid](https://hackmd.io/vZadj8YgS66je8F2taAD5w)\
[1706. Where Will the Ball Fall](https://hackmd.io/kC_WJ-rdRwqN4zEbQjwf2A)\
[2596. Check Knight Tour Configuration](https://hackmd.io/bV47pGkvTueX6d_0vECkXQ)\
[2593. Find Score of an Array After Marking All Elements](https://hackmd.io/yNRUw37MR0O0zm6AgIW1dg)\
[2679. Sum in a Matrix](https://hackmd.io/PtMi_GsuSQePnamQugi6SQ)\
[2766. Relocate Marbles](https://hackmd.io/FwG1gMwrTjCkmmkz0qxvrA)\
[2768. Number of Black Blocks](https://hackmd.io/dN7KvirzTBSIOv5Pa2-TwQ)
## 图形题
### 基本型I DP
[1039. Minimum Score Triangulation of Polygon](https://hackmd.io/DeG_gFXGT46K7IHUUZfCZg)
## Math
[0781. Rabbits in Forest](https://hackmd.io/GoToVbu1QYmhXOZJh3dlVw)\
[0780. Reaching Points](https://hackmd.io/Cv7T9O2NR3yxHnzgNzujmQ)\
[0458. Poor Pigs](https://hackmd.io/VWfrQ2MzRqqkR5PQzLDJ-A)\
[2195. Append K Integers With Minimal Sum](https://hackmd.io/jj2nAt9rSYCpk79SW-elEg)\
[2113. Elements in Array After Removing and Replacing Elements](https://hackmd.io/7asOKZZ2QnCu8RBrIXyN-A)\
[2125. Number of Laser Beams in a Bank](https://hackmd.io/QVmjyAuuTcyEBX_9CPjOhg)\
[2578. Split With Minimum Sum](https://leetcode.com/problems/split-with-minimum-sum/description/)\
[2579. Count Total Number of Colored Cells](https://hackmd.io/mNusnX4ASsGNRQGXGqqvSQ)\
[2489. Number of Substrings With Fixed Ratio](https://hackmd.io/BF-5UMALQQqPnLuMUgOYJg)\
[2645. Minimum Additions to Make Valid String](https://hackmd.io/5dRX14qgTx-ZYE5pZcORQg)\
[2750. Ways to Split Array Into Good Subarrays](https://hackmd.io/3rzK_KpxSaOCjpkGa3_cBg)\
[2780. Minimum Index of a Valid Split](https://hackmd.io/Usg9z8zqRmaFokFROzvAJw)
### 找规律
[2607. Make K-Subarray Sums Equal](https://hackmd.io/dAyeYzOGQziwFoJ9peBa6w)\
[1954. Minimum Garden Perimeter to Collect Enough Apples](https://hackmd.io/yv1RRCOUSRmtIZxycBufgw)\
[2745. Construct the Longest New String](https://hackmd.io/oGMNHJXwSzCg-OIn8ODBDg)
### Greatest Common Divisor
[2427. Number of Common Factors](https://hackmd.io/eitQmChnRaGw_OhNPbOQSA)\
[2447. Number of Subarrays With GCD Equal to K](https://hackmd.io/0-gZfdDARlCFnon9Pibang)\
[0453. Minimum Moves to Equal Array Elements](https://hackmd.io/ZVroSpuXQ1i498uRKIqbeg)\
[2028. Find Missing Observations](https://hackmd.io/mHWr0ZNtSFCwVZ4nWI8KRg)\
[2654. Minimum Number of Operations to Make All Array Elements Equal to 1](https://hackmd.io/23fvUkd_RpybvNLROy1jbg)\
[2748. Number of Beautiful Pairs](https://hackmd.io/5eBwcfe3SX2NOUkLzNM_cQ)
### Lowest Common Multiplier
[2513. Minimize the Maximum of Two Arrays](https://hackmd.io/2n5fUbyuRNK1leh1Gn3DmA)
### 距离所有点直线距离最近的点
[0296. Best Meeting Point](https://hackmd.io/iSJUkTnTTKu2AnB8iPowrA)
[2448. Minimum Cost to Make Array Equal](https://hackmd.io/DXfGz3FPTjygDK3q55Xnig)
### 计算角度
[1610. Maximum Number of Visible Points](https://hackmd.io/_W92uYTYQMmzPv9wFDIDbw)
### Triangle
[0976. Largest Perimeter Triangle](https://hackmd.io/85S3MNWnTn25wY1nmzKX6g)
### 位运算
[2438. Range Product Queries of Powers](https://hackmd.io/wZ8mgGG4TK-m9aGkcFG5dQ)
### 取余
[2453. Destroy Sequential Targets](https://hackmd.io/UqwYglKvTsqsE8N4ClcKCA)\
[2575. Find the Divisibility Array of a String](https://hackmd.io/J3ClAaJ2SwC0rkqjukIq5Q)\
[2598. Smallest Missing Non-negative Integer After Operations](https://hackmd.io/4off_E0cRLmC_5aoP34oVg)
### 解方程
[2485. Find the Pivot Integer](https://hackmd.io/PZ5Y4Z9OSTOa59WxHLBdVw)
### Prime & Sieve Algorithm
Sieve Algorithm
```python=
isPrime = [True] * maxNum
    isPrime[1] = False
    def buildSieve(self):
        for i in range(2, int(math.sqrt(self.maxNum))):
            if self.isPrime[i]:
                for j in range(i*i, self.maxNum, i):
                    self.isPrime[j] = False
```
注意1不是prime, 第二层循环之前先检查```i```是否为prime，防止重复遍历，第二层回圈从```i*i```开始\
[2507. Smallest Value After Replacing With Sum of Prime Factors](https://hackmd.io/W-JEZEGKTCGQveCm_7Rppg)\
[2521. Distinct Prime Factors of Product of Array](https://hackmd.io/wSoGjwjrT-O5ZPbCkenfDw)\
[2523. Closest Prime Numbers in Range](https://hackmd.io/vsIcTNCpTsO2MpHaKAzPmw)\
[2601. Prime Subtraction Operation](https://hackmd.io/aO_ZiVxaRSmT1EAbFpjvkA)\
[2614. Prime In Diagonal](https://hackmd.io/HCKwmIe9S-aeUMuPActO8Q)\
[2761. Prime Pairs With Target Sum](https://hackmd.io/m8nnlGXvTDuULtOR97N88w)
## Area
[0223. Rectangle Area](https://hackmd.io/5W7wV6vBTqifjEywz6mtGg)
## Line Sweep & 差分法
[0252. Meeting Rooms](https://hackmd.io/IEBJKDJMQKifMm502z5jiw)\
[1094. Car Pooling](https://hackmd.io/-FSHYs9DSYWKJW5TIUBTBg)(经典)\
[1893. Check if All the Integers in a Range Are Covered](https://hackmd.io/cbM9HQCNSNaPJUHKU1eccw)\
[1109. Corporate Flight Bookings](https://hackmd.io/dfft8CmbSxKdy9KbhJigXQ)\
[1589. Maximum Sum Obtained of Any Permutation](https://hackmd.io/RCXOpd_GQUOxbJwVjpfDBw)\
[2237. Count Positions on Street With Required](https://hackmd.io/H3qwtlMYTGeTlTpUNbqeJQ)\
[0056. Merge Intervals](https://hackmd.io/-Me1s3AUQCi4IPU8FslHyw)\
[0057. Insert Interval](https://hackmd.io/7Xg-MSxbQza--3rY_Um3cA)(重点复习 看笔记)\
[2381. Shifting Letters II](https://hackmd.io/DyCvlqiPScKQze7kwBrjcg)\
[2445. Number of Nodes With Value One](https://hackmd.io/qrka8RCoQ4urQEf30NXC8Q)\
[2559. Count Vowel Strings in Ranges](https://hackmd.io/4Y9eFIvBTFWLxX8iTW6Hzg)
### 2D Sweep Line
[2536. Increment Submatrices by One](https://hackmd.io/Omrkf3V8TiCwblCz0zd-Ng)
### TreeMap+Sweep Line
[2251. Number of Flowers in Full Bloom](https://hackmd.io/SlEo8THMSG2IQFjEy0qXKQ)(经典)\
[0732. My Calendar III](https://hackmd.io/v3_I8Np7RPSadXz9Z8D0ig)\
[0759. Employee Free Time](https://hackmd.io/HpHsgFsyTCK1kB_sUq2i2g)\
[1871. Jump Game VII](https://hackmd.io/cb46t-RNRTqyDQ3X8aiP_A)(经典)\
[0731. My Calendar II](https://hackmd.io/iKKe8lUqRUmVFMRJIJzFHA)\
[2054. Two Best Non-Overlapping Events](https://hackmd.io/T0Ld4gfBTTmV8oKgNpk0qQ)
## Count Subarray By Element
[1856. Maximum Subarray Min-Product](https://hackmd.io/rExGf0PFSy6pQxyJtyGvtQ)\
[0907. Sum of Subarray Minimums](https://hackmd.io/EyszVtjHSKmgqUQCIn-t-A)\
[2262. Total Appeal of A String](https://hackmd.io/JdYsGdTtRFapoMn5gkT2lg)\
[0828. Count Unique Characters of All Substrings of a Given String](https://hackmd.io/88Jj-Z_oSUiYD5BE342-Dg)
## Count Subarray By Iterating Right Boundary
[1063. Number of Valid Subarrays](https://hackmd.io/wkf9N1CaSWW5hIU-kUKRdA)\
[2495. Number of Subarrays Having Even Product](https://hackmd.io/cU9tF0OZRKGz6qwPKh6t7Q)(重点)
## Prefix Sum
[1031. Maximum Sum of Two Non-Overlapping Subarrays](https://hackmd.io/hSLeqvRvTSWn3kDV72XEIg)\
[1906. Minimum Absolute Difference Queries](https://hackmd.io/Ql-gTm8GS-iQh-LWVESJFA)\
[2017. Grid Game](https://hackmd.io/a95O-JFIRjiYTPExU0nbQQ)\
[2121. Intervals Between Identical Elements](https://hackmd.io/vRle-lSXQSWKeA1hw0rTvQ)\
[2145. Count the Hidden Sequences](https://hackmd.io/mtN56u_PTDa0UGkq-cfDgw)\
[2574. Left and Right Sum Differences](https://hackmd.io/FWqK69BBTj6i3RZbliRP2Q)\
[2640. Find the Score of All Prefixes of an Array](https://hackmd.io/0JyLrqLJRiWaiJ01TCwdAg)
### Simplify the sum of abs|diff|
将绝对值的和拆成```当前数字*比它小的数字个数-所有比它小的数字和+所有比它大的数字和-当前数字*比它大的数字和```
[2602. Minimum Operations to Make All Array Elements Equal](https://hackmd.io/ZXR1h6CER96MrOgxtoRo3w)\
[]
## Indexing 
具体关于swap的讲解在442里面\
[0287. Find the Duplicate Number](https://hackmd.io/hxOTm-zKQUKWmdoBsWVXYg)\
[0442. Find All Duplicates in an Array](https://hackmd.io/UnpI8ph4Q6icK2K1UxDHfg)\
[0448. Find All Numbers Disappeared in an Array](https://hackmd.io/ARYfPVzrQbK8WJnroF2hzA)\
[0645. Set Mismatch](https://hackmd.io/MR_-NLBvQVqOLLm3ZweCfg)
## String
[0068. Text Justification](https://hackmd.io/QSYg5KGdQ4SfzTX8wF7qvw)\
[0013. Roman to Integer](https://hackmd.io/p3TLBqn1Qj2cFIQ3GFnfmg)\
[1910. Remove All Occurrences of a Substring](https://hackmd.io/w9HB2xbSR_G8DH2TRHsjhg)\
[0796. Rotate String](https://hackmd.io/Cza3KeQFRKKQgHSqQ0i_6g)\
[2075. Decode the Slanted Ciphertext](https://hackmd.io/zbBNx86PQN-qBRWi1fM8lw)
## Design
[1352. Product of the Last K Numbers](https://hackmd.io/I6C-0C1RRhCc43bQVjnmqQ)\
[0642. Design Search Autocomplete System](https://hackmd.io/SCAbjINTS9mp7W8s7MtPlw)\
[0715. Range Module](https://hackmd.io/6rfFcVTBTUmDiK3KlaaOmQ)\
[2353. Design a Food Rating System](https://hackmd.io/wZkINjH0SsyXVFrzZHkhng)\
[1628. Design an Expression Tree With Evaluate Function](https://hackmd.io/JUKSeTfDRmqxNwz6DyHznw)\
[0355. Design Twitter](https://hackmd.io/O0H7TN7ZRIuz4v-ZIbkUxQ)\
[2166. Design Bitset](https://hackmd.io/Hez2wxP2Qu21nYGvKRQqNg)\
[2671. Frequency Tracker](https://hackmd.io/XKxSg-yBQUey3J3vOM5sVA)
## 计算长方形最大面积/最大边长
[0221. Maximal Square](https://hackmd.io/0Ie3z7ZRSH6sB5fMh1ZP7g)\
[1277. Count Square Submatrices with All Ones](https://hackmd.io/rfyE5TsLSGmlkOMPANdsGQ)\
[1727. Largest Submatrix With Rearrangements](https://leetcode.com/problems/largest-submatrix-with-rearrangements/)\
[0084. Largest Rectangle in Histogram](https://leetcode.com/problems/largest-rectangle-in-histogram/)\
[0085. Maximal Rectangle](https://hackmd.io/fMmT7YdPSs-VEYCIM3l5RA)\
[1504. Count Submatrices With All Ones](https://hackmd.io/86AP-3gOTmeWP2XtzCr1bg)
## Java不常见语法整理
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
- ```word.indexOf()```returns the position of the first occurrence of specified character(s) in a string([2185. Counting Words With a Given Prefix](https://hackmd.io/kiUsvgYWS5uvQnQKWgjAng))
- 用```Math.atan2()```计算角度 return value的范围是```[-pi,pi]```([1610. Maximum Number of Visible Points](https://hackmd.io/_W92uYTYQMmzPv9wFDIDbw
- ```s.lastIndexOf()```([0388. Longest Absolute File Path](https://hackmd.io/ZRs4b2URSx2lUMuYX7uMdA))
- ```s.startsWith(str, i)```可以检查从s[i]开始的substring是不是已```str```开头([0833. Find And Replace in String](https://hackmd.io/iptfcMhDR-iI_eKKiZ89ig))
- char array没有赋值的时候 每个位置的值都是0 [2325. Decode the Message](https://hackmd.io/H8_EJnGVTV6RXdl0DI_RVg)
## Python不常见语法
- ```d,r = divmod(sum, n)```直接算出divisor和residual
- ```bisect.bisect_left(nums, val)```, ```bisect.bisect_right(nums, val)```可以做binary search 返回应该把val插在哪个index 区别在于如果val已经存在在nums里，```bisect_left``` 返回的是这个数的最左边index 而```bisect_right```返回的是这个数的最右边index+1 具体用法[参考](https://blog.csdn.net/YMWM_/article/details/122378152)([1712. Ways to Split Array Into Three Subarrays](https://hackmd.io/VyYwo5xuTAaCcCokB-6BTw))
- ```defaultdict```和```dict```的差别在于前者会给一个不存在的key一个默认值 ([0355. Design Twitter](https://hackmd.io/O0H7TN7ZRIuz4v-ZIbkUxQ))
- ```list.extend()``` adds all the elements of an iterable (list, tuple, string etc.) to the end of the list ([0355. Design Twitter](https://hackmd.io/O0H7TN7ZRIuz4v-ZIbkUxQ))
- ```heapify()``` convert the iterable into a heap data structure;```heappushpop()``` method inserts a given item to the heap and then pops the smallest element from the heap ([0355. Design Twitter](https://hackmd.io/O0H7TN7ZRIuz4v-ZIbkUxQ))
- str是不能变更的数据结构 如果需要变更 先把它转成list ```s=list(s)``` 然后最后再把字母用```''.join(s)```合并成str ([0345. Reverse Vowels of a String](https://hackmd.io/JELlDncUR7KgwzlMZJAB1w))
- lowercase character -> 0, 1, ..., 25 ```ord(c)-ord('a')```; 0, 1, ..., 25 -> lowercase character ```chr(ord('a')+i)```([1002. Find Common Characters](https://hackmd.io/H5k1I9hCTpyRp89hvX22Kw))
- ```defaultdict()```括号里要设置默认值, 如果是int就会默认是0 ([2006. Count Number of Pairs With Absolute Difference K](https://hackmd.io/0EzOD00wQJOZ-KebRVGKKg))
- ```list.index()``` returns the position at the first occurrence of the specified value ([2091. Removing Minimum and Maximum From Array](https://hackmd.io/S5yg4zs2RwOSnhAKRn7tbg))
- The ```sort()``` method doesn't return any value. Rather, it changes the original list; If you want a function to return the sorted list rather than change the original list, use ```sorted()```([2545. Sort the Students by Their Kth Score](https://hackmd.io/4JKjhA9tTse0Ulk1PD-rUw))
- [lambda表达式](https://www.w3schools.com/python/python_lambda.asp)([2545. Sort the Students by Their Kth Score](https://hackmd.io/4JKjhA9tTse0Ulk1PD-rUw))
- ```zip()```和```zip(*)```((2679. Sum in a Matrix)[https://hackmd.io/PtMi_GsuSQePnamQugi6SQ])
## 注意事项
- 如果res是long，题目要求你return res%1000000007 
    ```(int)res%mod``` wrong ```(int)(res%mod)``` correct 前面一种方法会先把res变成int然后再算
- 如果index是一个int array(例如它是一个array的所有index的集合，我们不想排序array本身，而转而排序它的index)那我们不能写```Arrays.sort(index, (a,b)->(nums2[b]-nums2[a]))```而是要写成```Arrays.sort(index, (a,b)->Integer.compare(nums2[b], nums2[a])``` 同时index的数据类型还要设成Integer([0870. Advantage Shuffle](https://hackmd.io/w0INiSnmSJOkU2puietlOw))
- ```Arrays.sort(nums, Collections.reverseOrder())```的```nums```不能是int array，而要是Integer array
- 如果priority queue里面存的是integer，但是比较的是double，所以它自带的compare函数的参数应该是integer，而不是double，因此要写成```Queue<Integer> pq = new PriorityQueue<Integer>(Comparator.comparingDouble(i -> -prob[i]));```([1514. Path with Maximum Probability](https://hackmd.io/B7M8f6PUSdqHzZry7hDpSA)
- 考虑装进priority queue里面的元素会不会动([1514. Path with Maximum Probability](https://hackmd.io/B7M8f6PUSdqHzZry7hDpSA)
- ```list.add()``` – takes O(1) time, ```list.add(index, element)``` – on average runs in O(n) time, 因此尽量不用第二个
- 如果在java里面写```string.split(".")```是不会起作用的 要写```string.split("\\.")```([0165. Compare Version Numbers](https://hackmd.io/I1tXtG0PTdCpP0d-DLKw0g)) 但在python里面这样写没问题