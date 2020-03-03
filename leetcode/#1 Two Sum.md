# 문제: Two Sum

Given an array of integers, return indices of the two numbers such that they add up to a specific target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.


**Example:**
>Given nums = [2, 7, 11, 15], target = 9,
>
>Because nums[0] + nums[1] = 2 + 7 = 9,
>
>return [0, 1]

# 코드 

    /**
    * @param {number[]} nums
    * @param {number} target
    * @return {number[]}
    */
    var twoSum = function(nums, target) {
        for(var i=0; i<nums.length; i++){
            for(var j=i+1; j<nums.length; j++){
                if(nums[i]+nums[j] === target){
                    return [i, j];
                }
            }
        }
    };

Date: **2020.03.02**    
Status: **Accepted**  
Runtime: **112 ms(Rank: 38.26%)**  
Memory Usage: **34.8 MB**
