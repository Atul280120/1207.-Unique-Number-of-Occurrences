# 1207.-Unique-Number-of-Occurrences    
// leetcode solution:-
bool uniqueOccurrences(vector<int>& arr) {
        map<int ,int>m;
        for(int i=0;i<arr.size();i++){
            m[arr[i]]++;
        }
       map<int,int> m2;
        for(auto x:m){
            m2[x.second]++;
        }
        for(auto x:m2){
            if(x.second>1)
            {
                return false;
            }
        }
        return true;
    }
