class Solution {
public:
    int reachNumber(int target) {
        
        target = abs(target);
        int pos = 0;
        int steps = 0;
        
        while(pos != target)
        {
            steps++;
            pos = pos + steps;
            if(pos > target && (pos - target)%2 == 0) return steps;
        }
        return steps;
    }
};
