```cpp

class Solution {
public:
    vector<int> selfDividingNumbers(int left, int right) {

        vector<int> ans;

        for(int i = left; i <= right ;i++)
        {
            if( log10(double(i)) + 1 == 1 ) ans.push_back(i);
            else if( i % 10 == 0 ) continue;
            else
            {
                int count = (int)log10(double(i)) + 1;
                int num = i;
                int valid = 0;
                while(count--)
                {
                    int digit = num % 10;
                    if( !digit) break;
                    if( i % digit == 0 ) valid++;
                    num /= 10;
                }
                if( valid == (int)log10(double(i)) + 1 ) ans.push_back(i);
            }
        }
        return ans;
    }
};

```
