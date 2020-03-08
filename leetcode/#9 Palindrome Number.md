# 문제: Palindrome Number

Determine whether an integer is a palindrome. An integer is a palindrome when it reads the same backward as forward.


**Example 1:**
>Input: 121
>
>Output: true


**Example 2:**
>Input: -121
>
>Output: false
>
>Explanation: From left to right, it reads -121. From right to left, it becomes >121-. Therefore it is not a palindrome.


**Example 3:**
>Input: 10
>
>Output: false
>
>Explanation: Reads 01 from right to left. Therefore it is not a palindrome.


# 코드

    /**
    * @param {number} x
    * @return {boolean}
    */
    var isPalindrome = function(x) {
        let number = x.toString();
    //  console.log(number.slice(number.length - 1, number.length))
        
        while(number.length > 1){
            var first = number.slice(0, 1);
            var last = number.slice(number.length - 1, number.length);
            
            if(first !== last)  return false;
            
            number = number.slice(1, number.length - 1);
        }
        
        return true;
    };

Date: **2020.03.08**    
Status: **Accepted**  
Runtime: **172 ms(Rank: 94.45%)**  
Memory Usage: **45.3 MB**




