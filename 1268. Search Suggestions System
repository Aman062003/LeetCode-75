class Solution {
public:
    vector<vector<string>> suggestedProducts(vector<string> &products, string &searchWord) {
        vector<vector<string>> res;
        sort(products.begin(), products.end());
        int l = 0, r = products.size() - 1;
        for (int i = 0; i < searchWord.size(); i++) {
            char ch = searchWord[i];
            while(l<=r && (products[l].size() <= i || products[l][i]!=ch)) l++;
            while(l<=r && (products[r].size() <= i || products[r][i]!=ch)) r--;
            res.push_back(vector<string>());
            int m = min(3, r - l + 1);
            for (int j = 0; j < m; j++) {
                res.back().push_back(products[l + j]);
            }
        }
        return res;
    }
};
