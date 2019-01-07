```cpp
class Solution {
public:
    bool isPalindrome(int x) {
        
        if(x < 0) return false;
        else if( x == 0 ) return true;
        else
        {
            int len = (int)log10(double(x)) + 1;
            if( len == 1 ) return true;
            int count = len, num = x, res = 0;
            while(count--)
            {
                int rem = num % 10;
                res += rem * pow(10,count);
                num /= 10;
            }
            
            if(res == x) return true;
            else return false;
        }
        
    }
};

```
