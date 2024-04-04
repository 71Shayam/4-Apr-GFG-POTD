 long long sumSubstrings(string s){
        
        // your code here
         long long ans = 0,previous=0,mod=1e9+7;
        for(int i=0;i<s.length();i++){
            long long curr = (previous*10)%mod+(s[i]-'0')*(i+1)%mod;
            previous=curr;
            ans=(ans+curr)%mod;
        }
        return ans;
    }
