# 문제: Remove Element

Given an array nums and a value val, remove all instances of that value in-place and return the new length.

Do not allocate extra space for another array, you must do this by **modifying the input array** in-place with O(1) extra memory.

The order of elements can be changed. It doesn't matter what you leave beyond the new length.


**Example 1:**
>Given nums = **[3,2,2,3]**, val = **3**,
>
>Your function should return length = **2**, with the first two elements of nums being **2**.
>
>It doesn't matter what you leave beyond the returned length.


**Example 2:**
>Given nums = **[0,1,2,2,3,0,4,2]**, val = **2**,
>
>Your function should return length = **5**, with the first five elements of nums containing **0, 1, 3, 0**, and **4**.
>
>Note that the order of those five elements can be arbitrary.
>
>It doesn't matter what values are set beyond the returned length.



# 코드

    /**
    * @param {number[]} nums
    * @param {number} val
    * @return {number}
    */


    var removeElement = function(nums, val) {
        var cnt = 0;
        
        for(var i = 0; i < nums.length - cnt; i++){
            if(nums[i] == val){
                ++cnt;
                
                while(nums[nums.length - cnt] == val){
                    if(i + cnt == nums.length)
                        return nums.length - cnt;
                    
                    ++cnt;
                }
                        
                nums[i] = nums[nums.length - cnt];
                nums[nums.length - cnt] = val;
            }
        }
        return nums.length - cnt;
    };


Date: **2020.05.02**    
Status: **Accepted**  
Runtime: **52 ms(Rank: 85.40%)**  
Memory Usage: **33.7 MB(Rank: 94.44%)** 




