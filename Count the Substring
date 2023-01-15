  long long countSubstring(string S){
      int n = S.length();
      long long ans=0;
      int sum=0,onesekam=0;
      unordered_map<int,int> mm;
      for(auto x:S){
          if(x=='1')sum++;
          else sum--;
          if(sum<=0)onesekam++;
          mm[sum]++;
      }
      sum=0;
      for(int i=0;i<n;i++){
          ans+=(n-i-onesekam);
          if(S[i]=='1'){
              sum++;
              mm[sum]--;
              onesekam+=mm[sum];
          }
          else{
              sum--;
              mm[sum]--;
              onesekam--;
              onesekam-=mm[sum+1];
          }
      }
      return ans;
  }
