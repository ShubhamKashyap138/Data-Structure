// C++ CODE

    int min_operations(vector<int>& nums) {
        // Code here
        int n = nums.size(),temp=1;
        vector<int> dp(n,1);
        for(int i=0;i<n;i++){
            for(int j=0;j<i;j++){
                if(nums[i]-nums[j]>=i-j){
                    dp[i]=max(dp[i],dp[j]+1);
                    temp=max(dp[i],temp);
                }
            }
        }
        return n-temp;
    }

// JAVA CODE

    public int min_operations(int []nums)
    {
        // Code here
        int n=nums.length,temp=1;
        int dp[]=new int[n];
        Arrays.fill(dp,1);
        for(int i=0;i<n;i++){
            for(int j=0;j<i;j++){
                if(nums[i]-nums[j]>=i-j){
                    dp[i]=Math.max(dp[i],dp[j]+1);
                    temp=Math.max(dp[i],temp);
                }
            }
        }
        return n-temp;
    }

// Time Complexity:- O(N^2)
// Space Complexity:- O(N)
