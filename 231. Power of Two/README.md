```cpp

class Solution {
public:
    bool isPowerOfTwo(int n) {
        if( n < 0 ) return false;
        n = abs(n);
        return n && (!(n & n-1));
    }
};

```
