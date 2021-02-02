# 0001. Two Sum
Hash Table
Link: https://leetcode.com/problems/two-sum/
## 思路
最容易想到的就是暴力枚举，我们可以利用两层 for 循环来遍历每个元素，并查找满足条件的目标元素。不过这样时间复杂度为 O(N^2)，空间复杂度为 O(1)，时间复杂度较高，我们要想办法进行优化。

这里我们可以增加一个 Map 记录已经遍历过的数字及其对应的索引值。这样当遍历一个新数字的时候就去 Map 里查询 **target 与该数的差值是否已经在前面的数字中出现过**。如果出现过，就找到了答案，就不必再往下继续执行了。
## Keypoints
求和转换为求差
借助 Map 结构将数组中每个元素及其索引相互对应
以空间换时间，将查找时间从 O(N) 降低到 O(1)
## Code in C++
```
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        map<int,int> mymap;
        vector <int> result;
        for(int i = 0; i < nums.size();i++){
            int diff = target - nums[i];
            if(mymap.find(diff)!=mymap.end()&&mymap.find(diff)->second!=i){
                result.push_back(mymap.find(diff)->second);
                result.push_back(i);
                return result;
            }
            mymap.insert(pair<int,int>(nums[i],i));
        }        
        return {};
    }
};
```
# Error
**Non-void function does not return a value in all control paths.**
Solution: Add return {};

