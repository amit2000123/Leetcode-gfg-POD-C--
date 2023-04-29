class Solution{
public:
    long long findNumber(long long n){
        long long ans = 0;
        int arr[5] = {9, 1, 3, 5, 7};
        string s;
        long long t = n, mul = 1;
        while(t)
        {
            ans += mul * arr[t%5];
            mul *= 10;
            if(t%5 == 0) --t;
            t /= 5;
        }
        return ans;
    }
};
