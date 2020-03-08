# 문제: Reverse Integer

Given a 32-bit signed integer, reverse digits of an integer.


**Example 1:**
>Input: 123
>
>Output: 321


**Example 2:**
>Input: -123
>
>Output: -321


**Example 3:**
>Input: 120
>
>Output: 21

**Note:**  
Assume we are dealing with an environment which could only store integers within the 32-bit signed integer range: [−231,  231 − 1]. For the purpose of this problem, assume that your function returns 0 when the reversed integer overflows.


# 코드

    /**
    * @param {number} x
    * @return {number}
    */
    var reverse = function(x) {
        
        let num = x >= 0 ? x : x *(-1);
        let acc = 10;
        result = num % 10;
        while( parseInt(num /10) > 0){
            num = parseInt(num /10);
            result += parseInt(num % 10).toString();
        }
        
        result =  x>0 ? result : result*(-1);
        
        return (result < (Math.pow(2, 31) * -1) || result > Math.pow(2, 31) - 1) ? 0 : result;
    };

Date: **2020.03.04**    
Status: **Accepted**  
Runtime: **76 ms(Rank: 67.34%)**  
Memory Usage: **36.5 MB**




