# assign-cookies
  public:
    int maxChildren(int N, int M, vector<int> &greed, vector<int> &sz) {
        // code here
        int count=0,i=0,j=0;
        sort(sz.begin(),sz.end());
        sort(greed.begin(),greed.end());
        while(i<N && j<M)
        {
            if(sz[j]>=greed[i])
            {
            count++;
            i++;
            j++;
           }
        
        else if(sz[j]<greed[i]){
            j++;
        }
        }
          return count;
    }
};
