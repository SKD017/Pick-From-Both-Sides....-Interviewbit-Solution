# Pick-From-Both-Sides....-Interviewbit-Solution


int Solution::solve(vector<int> &A, int B) 
    {
  
    int sum1 = 0;
    int sum2 = 0;
    int j = A.size()-1;
    for(int i=0;i<B;i++,j--)
    {
        sum1 += A[i];
        sum2 += A[j];
    }   
                              
    int sum3 = sum1;
    j = A.size()-1;
    int result =0;
    result = max(sum1, sum2);
    for(int i=B-1;i>=0;i--,j--)
    {
        sum3 = sum3 - A[i] + A[j];
        if(sum3>result)
        result = sum3;
    }
  
  return result;
}

// Code by Shubham Kumar Das
