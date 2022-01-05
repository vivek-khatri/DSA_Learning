# [Question](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/)
## Code

class Solution {

    public int[] searchRange(int[] nums, int target) {
        return new int[]{start(nums,target),end(nums,target)};
    }
    public int start(int[] nums,int target){
        int f=0,e=nums.length-1;
        int m= f +(e-f)/2;
        int i=-1;
        while(f<=e){
            if(nums[m]<target)
                f=m+1;
            else{ 
                e=m-1;
                i = (nums[m]==target) ? m:i;
            }
            m = f+(e-f)/2;
        }
        return i;
    }
    public int end(int[] nums,int target){
        int f=0,e=nums.length-1;
        int m= f +(e-f)/2;
        int i=-1;
        while(f<=e){
            if(nums[m]>target)
                e=m-1;
            else{ 
                f=m+1;
                i = (nums[m]==target) ? m:i;
            }
            m = f+(e-f)/2;
        }
        return i;
    }
}
