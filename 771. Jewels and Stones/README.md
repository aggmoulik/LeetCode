```cpp
class Solution {
public:
    int numJewelsInStones(string J, string S) {
        
        int jewels = 0;
        for(auto ch: J)
        {
            int count = std::count(S.begin(),S.end(),ch);
            jewels += count;
        }
        return jewels;
    }
};

```
