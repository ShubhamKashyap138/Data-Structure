// C++ CODE

    void help(vector<string> &ans,int zero,int one,string temp,int N){
        if(temp.length()==N){
            ans.push_back(temp);
            return;
        }
        if(one>zero)help(ans,zero+1,one,temp+'0',N);
        help(ans,zero,one+1,temp+'1',N);
        
    }
	vector<string> NBitBinary(int n)
	{
	    // Your code goes here
	    vector<string> ans;
	    help(ans,0,1,"1",n);
	    sort(ans.begin(),ans.end());
	    reverse(ans.begin(),ans.end());
	    return ans;
	}

// JAVA CODE

    static void help(ArrayList<String> ans,int zero,int one, StringBuilder temp, int N){
        if(temp.length()==N){
            ans.add(temp.toString());
            return;
        }
        if(one>zero){
            temp.append('0');
            help(ans,zero+1,one,temp,N);
            temp.deleteCharAt(temp.length()-1);
        }
        temp.append('1');
        help(ans,zero,one+1,temp,N);
        temp.deleteCharAt(temp.length()-1);
    }
    ArrayList<String> NBitBinary(int N) {
        // code here
        ArrayList<String> ans = new ArrayList<>();
        StringBuilder temp = new StringBuilder();
        temp.append('1');
	    help(ans,0,1,temp,N);
	    Collections.sort(ans);
	    Collections.reverse(ans);
	    return ans;
    }


// Time Complexity:- O(2^N)
// Space Complexity:- O(2^N)
