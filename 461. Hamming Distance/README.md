```cpp
class Solution {
public:
    int hammingDistance(int x, int y) {
        int result = __builtin_popcount(x ^ y);
        return result;
    }
};
```
