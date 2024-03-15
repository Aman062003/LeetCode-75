class Solution {
public:
    int uniquePaths(int m, int n) {
        vector<vector<int>>dp(m+1,vector<int>(n+1,-1));
        return helper(m, n, 1, 1,dp);
    }

    int helper(int m, int n, int row, int col,vector<vector<int>>&dp) {
        if (row == m && col == n) {
            return 1;
        }
        if (row > m || col > n) {
            return 0;
        }

        if(dp[row][col] != -1)
        return dp[row][col];

        return dp[row][col] = helper(m, n, row + 1, col,dp)
              + helper(m, n, row, col + 1,dp);
    }
};
