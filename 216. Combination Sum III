class Solution {
    vector<vector<int>> ans;
    void dfs(int start, vector<int> &ds, int k, int target){
        if(k == 0){
            if(0 == target) ans.push_back(ds);
            return;
        }
        for(int i = start;i <= 9;i++){
            ds.push_back(i);
            dfs(i+1, ds, k-1, target-i);
            ds.pop_back();
        }
    }
public:
    vector<vector<int>> combinationSum3(int k, int n) {
        vector<int> ds;
        dfs(1, ds, k, n);
        return ans;
    }
};
