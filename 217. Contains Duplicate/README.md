```cpp

class Solution {
public:
    bool containsDuplicate(vector<int>& nums) {
        unordered_map<int,int> u_map;
        for(auto &it: nums)
        {
            u_map[it]++;
        }
        unordered_map<int, int>:: iterator itr; 
        for(itr = u_map.begin(); itr != u_map.end() ; itr++)
        {
            if( itr->second > 1 ) return true;
        }
        return false;
    }
};

```
