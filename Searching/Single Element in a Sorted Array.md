# [Question](https://leetcode.com/problems/single-element-in-a-sorted-array/)
## Code

class Solution {

    public int singleNonDuplicate(int[] nums) {
        int f=0,e=nums.length-1;
        if(nums.length != 1){
            while(f<=e){
                int m=f+(e-f)/2;
                
                if(((m==0 && nums[0]!=nums[1])||(m==nums.length-1 && nums[m]!=nums[m-1]))||(nums[m]!=nums[m-1] && nums[m]!=nums[m+1]))
                    return nums[m];
                else if(nums[m]!=nums[m+1]){
                    if((e-m)%2==0)
                        e=m-2;
                    else
                        f=m+1;
                }
                else{
                    if((e-(m-1))%2==0)
                        e=m-1;
                    else
                        f=m+2;
                }
            }
        }
         return nums[0];
        
    }
}
