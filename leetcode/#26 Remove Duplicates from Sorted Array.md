# 문제: Valid Parentheses

Given a sorted array nums, remove the duplicates in-place such that each element appear only once and return the new length.

Do not allocate extra space for another array, you must do this by **modifying the input array** in-place with O(1) extra memory.


**Example 1:**
>Given nums = [1,1,2],
>
>Your function should return length = 2, with the first two elements of nums >being 1 and 2 respectively.
>
>It doesn't matter what you leave beyond the returned length.


**Example 2:**
>Given nums = [0,0,1,1,1,2,2,3,3,4],
>
>Your function should return length = 5, with the first five elements of nums being modified to 0, 1, 2, 3, and 4 respectively.
>
>It doesn't matter what you leave beyond the returned length.





# 코드

    /**
    * @param {number[]} nums
    * @return {number}
    */
    var removeDuplicates = function(nums) { 
        var position = 1;
        for(var i = 0; i < nums.length - 1; i++){
            if(nums[i] != nums[i+1]){
                nums[position] = nums[i+1];
                ++position;
            }
        }
                
        return position;
    };

Date: **2020.05.02**    
Status: **Accepted**  
Runtime: **68 ms(Rank: 83.28%)**  
Memory Usage: **36.6 MB(Rank: 100%)** 




