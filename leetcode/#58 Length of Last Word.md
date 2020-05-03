# 문제: Length of Last Word

Given a string s consists of upper/lower-case alphabets and empty space characters ```' '```, return the length of last word (last word means the last appearing word if we loop from left to right) in the string.

If the last word does not exist, return 0.

**Note:** A word is defined as a **maximal substring** consisting of non-space characters only.


**Example:**
>**Input:** "Hello World"
>
>**Output:** 5

# 코드

    /**
    * @param {string} s
    * @return {number}
    */
    var lengthOfLastWord = function(s) {
        let flag = false;
        let cnt = 0;
        
        for(var i = s.length-1; i >= 0; i--){
            if(flag && s[i] == " ") return s.length - i - cnt - 1;
            else if(s[i] != " ")    flag = true;
            else    ++cnt;
        }
        
        return s.length - cnt; 
    };

Date: **2020.05.03**    
Status: **Accepted**  
Runtime: **48 ms(Rank: 89.53%%)**  
Memory Usage: **34.1 MB(Rank: 7.69%)** 




