class Solution {
public:
    //DP Approach 
    vector<vector<int>> updateMatrix(vector<vector<int>>& matrix) {
       int n = matrix.size();
       int m = matrix[0].size();
       for(int i=0;i<n;i++){
           for(int j=0;j<m;j++){
               if(matrix[i][j]){
                   int top = (i>0) ? matrix[i-1][j] +1 : 1e8;
                   int left = (j>0) ? matrix[i][j-1] +1 : 1e8;
                   matrix[i][j] = min(top,left);
               }
           }
       } 
       for(int i=n-1;i>=0; --i){
           for(int j=m-1;j>=0; --j){
               int ele = matrix[i][j];
               if(ele){
                   int bottom = (i<n-1) ? matrix[i+1][j] +1 : 1e8;
                    int right = (j < m - 1) ? matrix[i][j + 1] + 1 : 1e8;
                   matrix[i][j] = min(ele,min(bottom,right));
               }
           }
       }
       return matrix;
    }
};
