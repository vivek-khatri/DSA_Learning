# [Question](https://leetcode.com/problems/search-in-rotated-sorted-array-ii/)
## Code

class Solution {

    public boolean search(int[] nums, int target) {
        int f=0,e=nums.length-1;
        int k=0;
        while(f<=e){
            int m = f+(e-f)/2;
            if(nums[m]<nums[f]) {
                if(nums[m-1]>nums[m]){
                    k=m-1;break;
                }
                e = m - 1;
            }
            else if(nums[m]>nums[f]) {
                if(f!=nums.length-1){
                    if(nums[m]>nums[m+1]){
                        k=m;break;
                    }
                    f=m+1;
                }
                else {
                    k = f;
                    break;
                }
            }
            else{
                if(f==m){
                    k = f;break;}
                else{
                    f++;
                }
            }
        }
        int i = bs(0,k,nums,target);
        if(i==-1){
            i = bs(k+1,nums.length-1,nums,target);
        }
        
        if(i==-1)
            return false;
        return true;
    }
    
    public int bs(int f,int e, int[] nums, int x){
        while(f<=e){
            int m=f+(e-f)/2;
            if(nums[m]<x)
                f=m+1;
            else if(nums[m]>x)
                e=m-1;
            else return m;
        }
        return -1;
    }
}
