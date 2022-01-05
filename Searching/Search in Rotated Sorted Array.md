# [Question](https://leetcode.com/problems/search-in-rotated-sorted-array/)
## Code

class Solution {

    public int search(int[] nums, int target) {
        int f=0,e=nums.length-1;
        int m=f+(e-f)/2;
        int k=0;
        while(f<=e){
            if(m!=nums.length-1 && nums[m]>nums[m+1]){
                k=m;break;
            }
            else if(nums[m]>=nums[f])
                f=m+1;
            else
                e=m-1;
            m=f+(e-f)/2;
        }
        
        int ans=bs(nums,target,0,k);
        if(ans!=-1)
            return ans;
        else
            return bs(nums,target,k+1,nums.length-1);
        
    }
    public int bs(int[] nums,int target,int f,int e){
        int m=f+(e-f)/2;
        while(f<=e){
            if(target<nums[m])
                e=m-1;
            else if(nums[m]<target)
                f=m+1;
            else
                return m;
            m=f+(e-f)/2;
        }
        return -1;
    }
}
