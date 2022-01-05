# [Question](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/)
## Code

class Solution {

    public int[] twoSum(int[] numbers, int target) {
        int f=0,e=numbers.length-1;
        while(f<e){
            if(numbers[f]+numbers[e] < target)
                f++;
            else if(numbers[f]+numbers[e] > target)
                e--;
            else return new int[]{f+1,e+1};
        }
        return new int[]{f+1,e+1};
    }
}
