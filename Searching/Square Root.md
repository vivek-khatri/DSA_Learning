# [Question](https://leetcode.com/problems/sqrtx/)

## Code
class Solution {

    public int mySqrt(int x) {
        int f=0,e=x;
        while(f<=e){
            int m = f+(e-f)/2;
            
            if((m!=0 ?(x/m < m):(x<m*m ))) e=m-1;

            else if((m!=0 ?(x/m > m):(x>m*m ))) f=m+1;

            else return m;
        }
        return e;
    }
}
