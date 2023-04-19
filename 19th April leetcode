class Solution {
public:

    int ans = 0;
    void solve(TreeNode* root, int prev, int s){
        if(root==NULL){
            // ans=max(ans, s);
            return;
        }
        if(prev==-1){
            solve(root->left, 0, s+1);
            solve(root->right, 1, s+1);
        }
        else if(prev==0){
            solve(root->right, 1, s+1);
            solve(root->left, 0, 1);
        }
        else{
            solve(root->left, 0, s+1);
            solve(root->right, 1, 1);
        }
        ans=max(ans, s);
    }

    int longestZigZag(TreeNode* root) {
        solve(root, -1, 0);
        return ans;
    }
};
