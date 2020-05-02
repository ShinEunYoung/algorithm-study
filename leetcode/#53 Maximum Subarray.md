# 문제: Maximum Subarray

Given an integer array nums, find the contiguous subarray (containing at least one number) which has the largest sum and return its sum.


**Example:**
>**Input:** [-2,1,-3,4,-1,2,1,-5,4],
>
>**Output:** 6
>
>**Explanation:** [4,-1,2,1] has the largest sum = 6.


**Follow up:**

If you have figured out the O(n) solution, try coding another solution using the divide and conquer approach, which is more subtle.


# 코드

    /**
    * @param {number[]} nums
    * @return {number}
    */
    var maxSubArray = function(nums) {
        var max = -2147483648;
        
        var sum = 0; 
        
        for(var i = 0; i < nums.length; i++){
            sum = Math.max(nums[i], sum + nums[i]);
            max = Math.max(max, sum);
        }
        
        return max;
    };
    
Date: **2020.05.02**    
Status: **Accepted**  
Runtime: **84 ms(Rank: 20.41%)**  
Memory Usage: **35 MB(Rank: 98.15%)** 




