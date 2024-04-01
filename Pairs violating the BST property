// C++ CODE

    static void merge(vector<int> &nodes,int low,int mid,int high,int &ans){
        int a = mid-low+1;
        int b = high-mid;
        int arr1[a];
        int arr2[b];
        for(int i=0;i<a;i++)arr1[i]=nodes[low+i];
        for(int i=0;i<b;i++)arr2[i]=nodes[mid+1+i];
        int i=0,j=0,k=low;
        while(i<a and j<b){
            if(arr1[i]<=arr2[j]){
                nodes[k]=arr1[i];
                i++;
            }
            else{
                ans+=a-i;
                nodes[k]=arr2[j];
                j++;
            }
            k++;
        }
        while(i<a){
            nodes[k++]=arr1[i++];
        }
        while(j<b){
            nodes[k++]=arr2[j++];
        }
    }
    static void mergesort(vector<int> &nodes,int low,int high,int &ans){
        if(low>=high)return;
        int mid = (low+high)/2;
        mergesort(nodes,low,mid,ans);
        mergesort(nodes,mid+1,high,ans);
        merge(nodes,low,mid,high,ans);
    }
    static void help(Node *root,vector<int> &nodes){
        if(!root)return;
        help(root->left,nodes);
        nodes.push_back(root->data);
        help(root->right,nodes);
    }
    /*You are required to complete below function */
    int pairsViolatingBST(int n, Node *root) {
        // your code goes here
        vector<int> nodes;
        help(root,nodes);
        int ans = 0;
        mergesort(nodes,0,n-1,ans);
        return ans;
    }


// JAVA CODE

    static int ans = 0;
    static void merge(int arr[],int low, int mid, int high){
        int a = mid-low+1;
        int b = high-mid;
        int arr1[] = new int[a];
        int arr2[] = new int[b];
        for(int i=0;i<a;i++) arr1[i]=arr[low+i];
        for(int i=0;i<b;i++) arr2[i]=arr[mid+i+1];
        int i=0,k=low,j=0;
        while(i<a&&j<b){
            if(arr1[i]<=arr2[j]){
                arr[k]=arr1[i];
                i++;
            }
            else{
                ans+=a-i;
                arr[k]=arr2[j];
                j++;
            }
            k++;
        }
        while(i<a){
            arr[k++]=arr1[i++];
        }
        while(j<b){
            arr[k++]=arr2[j++];
        }
    }
    static void mergesort(int arr[], int low, int high){
        if(low>=high) return;
        int mid = (low+high)/2;
        mergesort(arr,low,mid);
        mergesort(arr,mid+1,high);
        merge(arr,low,mid,high);
    }
    static void help(Node root,ArrayList<Integer> nodes){
        if(root==null)return;
        help(root.left,nodes);
        nodes.add(root.data);
        help(root.right,nodes);
    }
    public static int pairsViolatingBST(int n, Node root) {
        // code here
        ans=0;
        ArrayList<Integer> nodes = new ArrayList<>();
        help(root,nodes);
        int arr[] = new int[nodes.size()];
        for(int i=0;i<nodes.size();i++)arr[i]=nodes.get(i);
        mergesort(arr,0,n-1);
        return ans;
    }


// Time Complexity:- O(NlogN)
// Space Complexity:- O(N)
