# 0007. Reverse Integer
Link: https://leetcode.com/problems/reverse-integer/
## Code
```
class Solution {
public:
    int reverse(int x) {
        int result = 0;
        while(x != 0){
            if(result>INT_MAX/10||result<INT_MIN/10){
                return 0;
            }
            result = result*10+x%10;
            x/=10;
        }
        return result;
    }
};
```
## 笔记
由于题目当中说如果reverse之后的数字比int能存的范围大，就return 0再加上result是用int存的，如果过大，会直接error，因此里面用到了result>INT_MAX/10或result<INT_MIN,代表result不能再乘10了，但给出的solution中判断条件是这样写的
```
pop = result % 10;
if (rev > INT_MAX/10 || (rev == INT_MAX / 10 && pop > 7)) return 0;
if (rev < INT_MIN/10 || (rev == INT_MIN / 10 && pop < -8)) return 0;
```
这样相比我之前的写法会更严谨一点

## Improvement
虽然和solution写的差不多，但是只有faster than 44.97% 所以还有待提升。