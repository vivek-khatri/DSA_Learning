# [Question](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/)
## Code

class Solution {

    public int findMin(int[] nums) {
        int f=0,e=nums.length-1;
        if(e!=0){
        while(f<=e){
            int m=f+(e-f)/2;
            if(((m==0 && nums[m]<nums[m+1]) || (m==nums.length-1 && nums[m]<nums[m-1]))||((m!=0 && m!=nums.length-1)&&(nums[m]<nums[m+1] && nums[m]<nums[m-1])))
                return nums[m];
            else if(nums[m]<nums[0])
                e=m-1;
            else
                f=m+1;
        }
            return nums[0];
        }
        return nums[0];
    }
}
