class Solution {
public:
    double findMedianSortedArrays(int A[], int m, int B[], int n) {
        int temp = (m + n)/2;
        int Is_odd = m + n - (m + n)/2 - (m + n)/2;
        double result;
 
        if(!Is_odd)
        {
            result = (double)Search(A, m, B, n, temp) + (double)Search(A, m, B, n, temp + 1);
            return result/2;
        }
        else
        {
            result = (double)Search(A, m, B, n, temp + 1);
            return result;
        }
    }
    
    //search Kth large element in two sorted array, the key point is to compare A[m/2] and B[n/2] 
    //and compare K and n/2+m/2+1
    int Search(int a[], int n, int b[], int m, int k)  
    {  
            //assert(a && b);   
            if (n <= 0) return b[k-1];  
            if (m <= 0) return a[k-1];  
            if (k <= 1) return min(a[0], b[0]);   
            if (b[m/2] >= a[n/2])  
            {  
                 if ((n/2 + 1 + m/2) >= k)  
                     return Search(a, n, b, m/2, k);  
                 else  
                      return Search(a + n/2 + 1, n - (n/2 + 1), b, m, k - (n/2 + 1));  
            }  
            else  
            {  
                if ((m/2 + 1 + n/2) >= k)  
                      return Search( a, n/2,b, m, k);  
                else  
                      return Search( a, n, b + m/2 + 1, m - (m/2 + 1),k - (m/2 + 1));  
            }  
       } 
};
