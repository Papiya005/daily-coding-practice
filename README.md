# daily-coding-practice
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

problem no 1



daily coding, LeetCode, practice, algorithms
class Solution {
    public int[] twoSum(int[] nums, int target) {
     
      for(int i=0;i<nums.length;i++){
        int first=nums[i];
        for(int j=i+1;j<nums.length;j++){
            int second=nums[j];
            int sum=nums[i]+nums[j];
            if(sum==target){
                return new int[] {i,j};
            }
        }
      }
      return new int[]{};

        
    }
    public static void main(String args[]){
        Solution obj=new Solution();
        int[] nums={2,7,11,15};
        int target=9;
        int[] result=obj.twoSum(nums,target);
        System.out.println(result[0]+" "+result[1]);
    }
}
