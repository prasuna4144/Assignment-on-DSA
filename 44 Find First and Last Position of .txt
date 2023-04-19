44: Find First and Last Position of Element in Sorted Array
solution:
class Solution {
    public int[] searchRange(int[] nums, int target) {
         int temp[]=new int[2];
         if(nums.length==0)
         {
             temp[0]=-1;
             temp[1]=-1;
         }
         for(int i=0;i<nums.length;i++)
         {
             if(nums[i]==target)
             {
                 temp[0]=i;
                 break;
             }
             else
             {
                 temp[0]=-1;
             }
         }
         for(int i=nums.length-1;i>=0;i--)
         {
             if(nums[i]==target)
             {
                 temp[1]=i;
                 break;
             }
             else
             temp[1]=-1;
         }
         return temp;
    }
}