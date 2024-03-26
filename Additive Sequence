// C++

    string findSum(string a,string b){
        string ans="";
        int i=a.length()-1,j=b.length()-1,carry=0;
        while(i>=0 and j>=0){
            int sum = (a[i]-'0')+(b[j]-'0')+carry;
            ans+=(sum%10+'0');
            carry=sum/10;
            i--;
            j--;
        }
        while(i>=0){
            int sum = (a[i]-'0')+carry;
            ans+=(sum%10+'0');
            carry=sum/10;
            i--;
        }
        while(j>=0){
            int sum = (b[j]-'0')+carry;
            ans+=(sum%10+'0');
            carry=sum/10;
            j--;
        }
        if(carry){
            ans+=(carry+'0');
        }
        reverse(ans.begin(),ans.end());
        return ans;
    }
    bool help(string a,string b,string c){
        string sum = findSum(a,b);
        int i=0,j=0;
        while(i<c.length() and j<sum.length()){
            if(c[i]!=sum[j])return false;
            i++;
            j++;
        }
        if(j!=sum.length())return false;
        if(i==c.length())return true;
        c=c.substr(i);
        return help(b,sum,c);
    }
    bool isAdditiveSequence(string n) {
        // Your code here
        for(int i=0;i<n.length()/2;i++){
            for(int j=i+1;j<n.length()-1;j++){
                string a = n.substr(0,i+1);
                string b = n.substr(i+1,j-i);
                string c = n.substr(j+1);
                if(help(a,b,c))return true;
            }
        }
        return false;
    }

// JAVA CODE

    static String findSum(String a,String b){
        int i=a.length()-1,j=b.length()-1;
        StringBuilder ans = new StringBuilder();
        int carry=0;
        while(i>=0 && j>=0){
            int sum = (a.charAt(i)-'0')+(b.charAt(j)-'0')+carry;
            ans.append((char)sum%10);
            carry=sum/10;
            i--;
            j--;
        }
        while(i>=0){
            int sum = (a.charAt(i)-'0')+carry;
            ans.append((char)sum%10);
            carry=sum/10;
            i--;
        }
        while(j>=0){
            int sum = (b.charAt(j)-'0')+carry;
            ans.append((char)sum%10);
            carry=sum/10;
            j--;
        }
        if(carry!=0){
            ans.append((char)(carry+'0'));
        }
        StringBuilder temp = ans.reverse();
        return temp.toString();
    }
    static boolean help(String a,String b,String c){
        String sum = findSum(a,b);
        int i=0,j=0;
        while(i<c.length() && j<sum.length()){
            if(c.charAt(i)!=sum.charAt(j))return false;
            i++;
            j++;
        }
        if(j!=sum.length())return false;
        if(i==c.length())return true;
        c=c.substring(i);
        return help(b,sum,c);
    }
    public boolean isAdditiveSequence(String n) {
        // code here
        for(int i=0;i<n.length()/2;i++){
            for(int j=i+1;j<n.length()-1;j++){
                String a = n.substring(0,i+1);
                String b = n.substring(i+1,j+1);
                String c = n.substring(j+1);
                if(help(a,b,c))return true;
            }
        }
        return false;
    }

// Time Complexity:- O(N^3)
// Space Complexity:- O(N)
